# AI Prompt Engineering Handbook

> The definitive resource for crafting effective prompts across different AI models and generations
> Maintained by [ImagineAnything.ai](https://www.imagineanything.ai/)

![GitHub stars](https://img.shields.io/github/stars/yourusername/ai-prompt-handbook?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/ai-prompt-handbook?style=social)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🌟 Why This Handbook Exists

Creating high-quality AI-generated content requires more than just basic prompts. Each AI model has its own "language" and responds differently to various prompting techniques. This handbook aims to bridge the gap between generic prompting and expert-level results by providing:

- **Model-specific techniques** that leverage the unique strengths of each AI platform
- **Proven formulas and templates** for consistent, high-quality generation
- **Troubleshooting guides** for common issues and limitations
- **Workflow optimization** strategies for different use cases
- **Parameter reference sheets** for fine-tuning your results

## 📚 Table of Contents

1. [Image Generation Models](#image-generation-models)
2. [Text Generation Models](#text-generation-models)
3. [Audio Generation Models](#audio-generation-models)
4. [Video Generation Models](#video-generation-models)
5. [Multimodal Techniques](#multimodal-techniques)
6. [Advanced Techniques](#advanced-techniques)
7. [Troubleshooting Guide](#troubleshooting-guide)
8. [Parameter Reference](#parameter-reference)
9. [Real-world Case Studies](#real-world-case-studies)
10. [Contributing](#contributing)

## 🖼️ Image Generation Models

### Midjourney

#### Anatomy of a Midjourney Prompt

```
/imagine [image style] [subject] [action/pose] [lighting] [camera angle] [additional details] --ar [aspect ratio] --v [version] --q [quality] --s [stylize]
```

#### Prompt Templates

| Use Case | Prompt Template | Example |
|----------|----------------|---------|
| Portrait Photography | `[subject], portrait photography, [lighting], [camera lens], [film type], [photographer style] --ar 2:3 --v 5 --q 2` | `elegant woman with auburn hair, portrait photography, golden hour lighting, 85mm lens, Kodak Portra 400, style of Annie Leibovitz --ar 2:3 --v 5 --q 2` |
| Product Shots | `[product] on [background], product photography, [lighting setup], commercial, advertising, [style] --ar 1:1 --v 5` | `minimalist white ceramic coffee mug on marble countertop, product photography, soft diffused lighting, commercial, advertising, clean modern style --ar 1:1 --v 5` |
| Fantasy Scenes | `[scene description], fantasy art, [artist references], [color palette], [mood], dramatic, detailed --v 5 --s 750` | `ancient wizard's library with floating books and magical artifacts, fantasy art, style of Greg Rutkowski and Peter Mohrbacher, deep blues and amber highlights, mysterious, dramatic, detailed --v 5 --s 750` |

#### Parameter Guide

| Parameter | Effect | Range | Notes |
|-----------|--------|-------|-------|
| --v | Model version | 1-6 | V5 and V6 are most current |
| --q | Quality | 0.25-2 | Higher values = more detail but slower |
| --s | Stylize | 0-1000 | Higher values = more artistic interpretation |
| --ar | Aspect ratio | 1:1, 16:9, etc. | Common ratios: 1:1, 3:2, 16:9, 9:16 |
| --c | Chaos | 0-100 | Higher values = more unexpected results |

#### Style Reference

| Artistic Style | Keywords | Example |
|----------------|----------|---------|
| Photorealistic | `photorealistic, 8k uhd, detailed, photography` | `photorealistic winter forest, 8k uhd, detailed, photography, volumetric lighting, mist` |
| Anime/Manga | `anime, manga, studio ghibli, illustration` | `anime girl with blue hair, manga style, studio ghibli inspired, soft illustration` |
| Painterly | `oil painting, [artist name], painterly, detailed brushstrokes` | `mountain landscape, oil painting, style of Thomas Kinkade, painterly, detailed brushstrokes` |

### Stable Diffusion

#### Anatomy of a Stable Diffusion Prompt

```
[quality boosters] [subject] [subject details] [environment] [lighting] [composition] [render style] [artist style] [negative prompt: unwanted elements]
```

#### Prompt Templates

| Use Case | Prompt Template | Example |
|----------|----------------|---------|
| Character Concept Art | `[(quality boosters)], [character description], [clothing], [pose/action], [environment], [lighting], [style], [artist references]` | `highly detailed, concept art, female rogue thief, leather armor with hood, crouching on rooftop, medieval city at night, moonlight, detailed, matte painting, artstation, style of Craig Mullins and Eytan Zana` |
| Landscapes | `[(quality boosters)], [landscape type], [time of day], [weather], [lighting], [mood], [style], [artist references]` | `highly detailed, masterpiece, ultra realistic, 8k, epic mountain range, sunrise, clear sky with whispy clouds, golden light, serene atmosphere, hyperrealistic, style of Albert Bierstadt` |
| Abstract Art | `abstract [theme/concept], [color palette], [texture], [composition], [style], [artist references]` | `abstract representation of consciousness, deep blues and purples with hints of gold, fluid texture, asymmetrical composition, digital art, style of Android Jones and Peter Mohrbacher` |

#### Important Negative Prompts

```
negative prompt: deformed, bad anatomy, disfigured, poorly drawn face, mutation, mutated, extra limb, ugly, poorly drawn hands, missing limb, floating limbs, disconnected limbs, malformed hands, blurry, ((((ugly)))), (((distorted))), ((oversaturated)), ((undersaturated)), unnatural colors
```

#### LoRA and Embeddings

| Type | How to Use | Example |
|------|------------|---------|
| LoRA | `<lora:LoraName:weight>` | `beautiful portrait of a woman <lora:epiNoiseoffset:0.6>` |
| Textual Inversion | `embedding:name` | `embedding:NegativeHand portrait of young woman` |

### DALL-E 3

#### Anatomy of a DALL-E 3 Prompt

```
[create a/generate a] [detail level] [style] [subject] [action/pose] [environment] [lighting] [additional details]
```

#### Prompt Templates

| Use Case | Prompt Template | Example |
|----------|----------------|---------|
| Artistic Illustrations | `Create a detailed [style] illustration of [subject] [action/environment]. Include [specific details] and use a [color palette/mood] aesthetic.` | `Create a detailed watercolor illustration of a small cafe on a rainy Parisian street. Include people with umbrellas walking by and reflections in puddles. Use a muted, romantic color palette with touches of warm light from windows.` |
| Concept Design | `Generate a [detail level] concept design for a [subject]. The design should feature [specific elements] in a [style/aesthetic] style.` | `Generate a highly detailed concept design for a futuristic electric motorcycle. The design should feature sleek aerodynamic curves, minimal exposed mechanics, and ambient blue lighting accents in a cyberpunk style.` |
| Scenes/Environments | `Create a [mood] scene showing [environment] with [subjects/elements]. Use [lighting] and a [style] aesthetic.` | `Create a mystical scene showing an ancient forest temple with stone guardians covered in moss. Use dappled sunlight through a dense canopy and a fantasy illustration aesthetic.` |

#### Key Strategies for DALL-E 3

1. **Be Specific**: Unlike other models, DALL-E 3 benefits from longer, more detailed prompts.
2. **Describe What You Want**: Focus on describing the desired outcome rather than technical parameters.
3. **Reference Specific Styles**: Name artists or art movements for stylistic influence.
4. **Include Composition Details**: Mention camera angles, perspective, and framing.

## 💬 Text Generation Models

### GPT-4 & Claude

#### Prompt Frameworks

| Framework | Structure | Best For |
|-----------|-----------|----------|
| Role-Play Framework | `You are a [specific expert]. Your task is to [specific action]. [Additional context]. [First question/request]` | Expert content creation, specialized knowledge |
| Step-by-Step Framework | `I need a comprehensive guide on [topic]. Please break down the process into detailed steps, covering [specific aspects].` | Tutorials, instructions, explanations |
| Few-Shot Learning | `Here are some examples of [type of content]:\n\nExample 1: [input] -> [output]\nExample 2: [input] -> [output]\n\nNow, create a similar [type of content] for: [new input]` | Consistent formatting, specific response patterns |
| Chain-of-Thought | `Think through [problem] step by step. First, consider [aspect 1]. Then, analyze [aspect 2]. Finally, conclude with [aspect 3].` | Complex problem solving, reasoning |

#### Specificity Techniques

| Technique | Example | Effect |
|-----------|---------|--------|
| Output Format Specification | `Format your response as a markdown table with the following columns: [column1], [column2], [column3]` | Controls exact output structure |
| Tone Specification | `Write in a [conversational/professional/academic] tone that [specific characteristics]` | Controls writing style |
| Length Control | `Provide a [brief/comprehensive] response in approximately [X] words/paragraphs` | Controls response length |
| Audience Targeting | `Write this explanation for [specific audience, e.g., "a 10-year-old" or "a technical expert"]` | Adjusts complexity level |

### Specialized Text Generation

#### SEO Content Framework

```
Topic: [your topic]
Target Keywords: [primary keyword, secondary keywords]
Search Intent: [informational/commercial/navigational]
Word Count: [target length]
Tone: [professional/conversational/authoritative]

Please write a comprehensive article that covers [topic] in depth. The article should:
1. Include an engaging introduction that hooks the reader
2. Contain [number] main sections covering [list main points]
3. Incorporate all target keywords naturally
4. Include appropriate headings and subheadings (H2, H3)
5. End with a conclusion that includes a call to action
6. Add relevant internal linking suggestions in [brackets]
```

#### Social Media Templates

| Platform | Template | Example |
|----------|----------|---------|
| Twitter/X | `Hook that creates curiosity or emotion in <140 chars>\n\nKey point 1\nKey point 2\nKey point 3\n\nCall to action\n\n#hashtag1 #hashtag2` | `I increased my AI art sales by 350% last month without spending more time creating.\n\nThe secret?\n• Custom prompt templates\n• Model-specific workflows\n• Strategic negative prompts\n\nGet my free guide: [link]\n\n#AIArt #PromptEngineering` |
| LinkedIn | `[Attention-grabbing statement]\n\n[Personal story or context]\n\n[Problem identification]\n\n[Solution presentation]\n\n[Results or benefits]\n\n[Lessons learned]\n\n[Call to action]\n\n#hashtag1 #hashtag2 #hashtag3` | `I helped a digital artist increase their output by 5x while improving quality.\n\nThey were struggling with inconsistent results from AI tools, spending hours tweaking prompts.\n\nWe implemented structured prompt templates and model-specific workflows.\n\nResults after 2 weeks:\n• Generation time cut from 45 to 9 minutes\n• Client approval rate up 72%\n• Consistent style across all pieces\n\nThe lesson? Systematic prompt engineering beats trial and error every time.\n\nNeed help optimizing your AI workflow? Comment "info" below.\n\n#AIProductivity #DigitalArt #WorkflowOptimization` |

## 🔊 Audio Generation Models

### Music Generation

#### MusicLM and AudioCraft Prompt Structure

```
[genre/style] [instruments] [mood/emotion] [tempo] [additional characteristics] [reference artists/songs]
```

#### MusicGen Templates

| Use Case | Template | Example |
|----------|----------|---------|
| Background Music | `Create a [mood] [genre] track with [instruments]. The piece should be [tempo] and evoke a feeling of [emotion]. Similar to the style of [artist].` | `Create a relaxing ambient track with soft synthesizers and distant piano. The piece should be slow-paced and evoke a feeling of floating in space. Similar to the style of Brian Eno.` |
| Sound Design | `Generate a [description] sound effect suitable for [context]. It should include [specific sound characteristics] and convey [intended impact].` | `Generate a futuristic spaceship powering up sound effect suitable for a sci-fi game. It should include low humming that builds to a high-pitched stabilization and convey massive energy contained within a sleek vessel.` |

### Speech Synthesis

#### ElevenLabs and PlayHT Prompt Structure

```
[Speaker: emotional state, intensity, speaking style, environment] "Text to be spoken"
```

#### Speech Templates

| Use Case | Template | Example |
|----------|----------|---------|
| Narration | `[Narrator: calm, engaging, storytelling voice in a quiet studio] "Text to be narrated"` | `[Narrator: calm, engaging, storytelling voice in a quiet studio] "The ancient legend tells of a crystal that could harness the power of the stars themselves. For centuries, it remained hidden, until one fateful evening..."` |
| Character Voice | `[Character: age, gender, accent, emotional state, unique vocal characteristics] "Dialogue"` | `[Character: elderly male with British accent, slightly raspy voice, warm and wise tone, speaking slowly] "I've seen many things in my long years, child, but nothing quite like what you've discovered here."` |

## 🎬 Video Generation Models

### Runway Gen-2 and Pika

#### Prompt Structure

```
[scene description] [style] [camera movement] [lighting] [environment] [additional details]
```

#### Video Templates

| Use Case | Template | Example |
|----------|----------|---------|
| Product Showcase | `[product] [environment], [movement/transition], [style], [lighting], [camera angle/movement]` | `White smartphone floating in a minimalist white environment, slowly rotating 360 degrees, photorealistic, soft diffused lighting, close-up camera tracking shot` |
| Scene Transition | `Transition from [scene 1] to [scene 2] through [transition effect], [style], [camera movement]` | `Transition from bustling cityscape to serene forest through particle dissolve effect, cinematic style, smooth drone camera pulling back` |

## 🔄 Multimodal Techniques

### Text-to-Image-to-Video Workflow

| Step | Tool | Template | 
|------|------|----------|
| 1. Concept | GPT-4 | `Create a detailed scene description for [concept] that would work well for an AI-generated image and video. Include setting, subjects, lighting, mood, and style.` |
| 2. Image | Midjourney/DALL-E | `[GPT-4 output modified for image model]` |
| 3. Video | Runway/Pika | `[Brief description of image] with [movement/camera action], [style reinforcement]` |

### Advanced Chaining Examples

| Chain | Purpose | Example Workflow |
|-------|---------|------------------|
| Character Creation | Creating consistent characters across media | 1. GPT-4: Character profile and description<br>2. Midjourney: Character visualization<br>3. ElevenLabs: Character voice<br>4. Runway: Character animation |
| Product Marketing | Complete product marketing package | 1. GPT-4: Product description and marketing copy<br>2. DALL-E: Product images<br>3. AudioCraft: Background music<br>4. Pika: Product showcase video |

## 🧠 Advanced Techniques

### Negative Prompting Strategies

| Model | Technique | Example |
|-------|-----------|---------|
| Stable Diffusion | Weight-based negatives | `beautiful landscape, mountains --neg bad art, blurry, distorted:1.5` |
| Midjourney | Compositional negatives | `character portrait --no glasses, hats, jewelry` |

### Parameter Optimization

| Model | Parameter | Optimization Strategy |
|-------|-----------|----------------------|
| Stable Diffusion | CFG Scale | Start at 7.0, increase for accuracy, decrease for creativity |
| Stable Diffusion | Steps | 20 steps for quick tests, 40-50 for final images |
| Midjourney | Stylize | 0-250 for photorealism, 500-1000 for artistic styles |

## 🛠 Troubleshooting Guide

### Common Issues and Solutions

| Issue | Possible Causes | Solutions |
|-------|----------------|-----------|
| Distorted Faces | Prompt complexity, model limitations | • Add "detailed face, realistic features" to prompt<br>• Use face-focused negative prompts<br>• Try different model version |
| Inconsistent Style | Conflicting style references, weak style signals | • Reduce number of style references<br>• Increase weight of primary style<br>• Use dedicated LoRAs or embeddings |
| Poor Composition | Lack of composition guidance, competing elements | • Add explicit composition terms: "rule of thirds, balanced composition"<br>• Simplify scene elements<br>• Add camera position guidance |

### Model-Specific Limitations

| Model | Known Limitations | Workarounds |
|-------|-------------------|------------|
| Midjourney | Text rendering | • Use simple text phrases<br>• Request "clear legible text"<br>• Consider post-processing |
| DALL-E 3 | Multiple subjects with specific arrangements | • Break complex scenes into multiple generations<br>• Focus on one main subject with detailed context |
| Stable Diffusion | Hands and limbs | • Use "perfect hands" in positive prompt<br>• Include detailed hand descriptions in negative prompt<br>• Use dedicated hand LoRAs |

## 📊 Parameter Reference

### Stable Diffusion Web UI

| Parameter | Range | Function | Recommended Setting |
|-----------|-------|----------|---------------------|
| CFG Scale | 1-30 | Prompt adherence vs. creativity | 7-8 |
| Sampling Steps | 10-150 | Detail level and refinement | 30-50 |
| Sampler | Various | Diffusion algorithm | Euler a (speed), DPM++ 2M Karras (quality) |
| Seed | -1 or number | Randomization control | -1 (random) or save seeds of good images |

### ComfyUI Nodes

| Node Type | Purpose | Key Parameters |
|-----------|---------|----------------|
| KSampler | Core sampling | steps, cfg, sampler_name, seed |
| CLIPTextEncode | Prompt encoding | text (prompt), clip model |
| VAEDecode | Image decoding | samples, vae |

## 📝 Real-world Case Studies

### Case Study 1: Product Photography Optimization

A small e-commerce business increased their product image consistency and reduced generation time by 70% using the following workflow:

1. **Template Creation**:
   ```
   professional product photography of [product] on [background], commercial lighting setup, 8k, product centered, detailed texture, [product-specific details], advertising quality
   ```

2. **Negative Prompt Standardization**:
   ```
   deformed, distorted, text, watermark, low quality, blurry, duplicated, extra items, cropped
   ```

3. **Parameter Optimization**:
   - Stable Diffusion XL
   - CFG: 7.5
   - Steps: 30
   - Size: 1024x1024
   - Saved successful seeds for similar products

### Case Study 2: Architectural Visualization Pipeline

An architectural firm developed a consistent pipeline for concept visualization:

1. **Initial Concept (GPT-4)**:
   - Detailed building description based on client requirements
   - Material specifications and environmental context

2. **Exterior Visualization (Midjourney)**:
   ```
   photorealistic architectural visualization of [building description], exterior view, professional photography, midday clear sky, hyperrealistic materials, detailed textures, cinematic lighting, architectural magazine quality --ar 16:9 --v 5
   ```

3. **Interior Visualization (Stable Diffusion)**:
   ```
   interior design visualization, [room type], [style], natural lighting from large windows, detailed materials, photorealistic rendering, architectural digest quality
   ```

4. **Animation (Runway Gen-2)**:
   ```
   slow camera pan through modern [room type] interior, soft natural lighting, photoreal, architectural visualization
   ```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### How to Contribute

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-contribution`)
3. Commit your changes (`git commit -m 'Add some amazing contribution'`)
4. Push to the branch (`git push origin feature/amazing-contribution`)
5. Open a Pull Request

### Contribution Guidelines

- Keep examples practical and tested
- Include both the template and a concrete example
- Document any model-specific quirks or requirements
- Credit original sources where applicable

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/ai-prompt-handbook&type=Date)](https://star-history.com/#yourusername/ai-prompt-handbook&Date)

## 🙏 Acknowledgements

Special thanks to all contributors and the AI generation community for sharing their knowledge and experiences.

---

If you find this handbook useful, please consider giving it a star ⭐ on GitHub and sharing it with others.
