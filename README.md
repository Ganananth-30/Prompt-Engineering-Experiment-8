# Exp 8: Reproducing an Image Using Prompts for Image Generation
# Name : H GANANANTH
# Register No : 212225230070
# Date : 14.05.2026



## Aim:
To demonstrate the ability of text-to-image generation tools to reproduce an existing image by crafting precise prompts. The goal is to identify key elements within the image and use these details to generate an image as close as possible to the original.

# OUTPUT

1. Introduction

Image generation with AI has moved from a novelty to a professional skill in a remarkably short time. Tools
like DALL·E 3, Midjourney, and Stable Diffusion can produce photorealistic, painterly, or fantastical images
from text descriptions alone. But the quality of what they produce is determined almost entirely by the quality
of the prompt. A vague description produces a generic image; a precisely constructed prompt — one that
specifies subject, style, lighting, color palette, camera angle, and mood — produces something close to a
deliberate visual artwork.
This experiment explores the discipline of visual prompt engineering: the practice of analysing an existing
image, decomposing it into its constituent visual elements, and writing increasingly refined prompts that
attempt to reproduce it. The exercise reveals how AI image models interpret language, where they succeed,
and where they consistently fall short of a human’s visual intent.
The reference image chosen for this exercise is a futuristic neon cityscape at night — a scene rich in colour
contrast, lighting complexity, reflective surfaces, and architectural detail. It is an ideal test case because it
contains multiple elements that require precise description: the quality of neon light on wet surfaces, the
density and variation of building silhouettes, the colour temperature of the sky, and the overall atmosphere of
a speculative future city.

<img width="1028" height="592" alt="image" src="https://github.com/user-attachments/assets/6bc349a1-eb6f-4415-82b0-042eea247010" />

2.1 Visual Element Analysis
<img width="1095" height="818" alt="image" src="https://github.com/user-attachments/assets/2215b2a5-7fa7-418b-8005-64091470d7da" />

3. Prompts Used — Three Levels of Refinement
Three prompts were designed and submitted to two AI image generation tools: DALL·E 3 (via ChatGPT) and
Midjourney (v6). Each prompt was a deliberate step forward in precision, adding new visual descriptors based
on where the previous generation fell short.
3.1 Prompt v1 — Simple (Unrefined)
“A city at night with neon lights.”
This is the minimal, first-instinct prompt. It communicates the core subject (city) and two key attributes (night,
neon lights) but leaves every other visual decision to the model. It provides no information about architectural
style, color palette specifics, sky quality, reflections, camera angle, or mood. The model fills these gaps with
its statistical average of ‘neon city at night’ images from training data, which produces a recognisable but
entirely generic result.

Elements missing from v1: no style reference (cyberpunk, futuristic, neo-noir), no lighting quality (bloom, glow
radius), no sky description, no reflection, no colour specifics, no camera angle, no building density or height
variation, no atmosphere.

<img width="1158" height="492" alt="image" src="https://github.com/user-attachments/assets/5abe1796-e0fd-4a22-96c8-076aa238b029" />

3.2 Prompt v2 — Refined
“A futuristic cyberpunk cityscape at night, with tall skyscrapers featuring neon signs in cyan,
magenta, and yellow. Glowing windows cover the building facades. Dark navy sky with stars and
a full moon. Reflections of neon lights on a wet street or canal in the foreground. Cinematic
wide-angle perspective, high contrast, atmospheric fog.”
Prompt v2 adds six specific improvements: the cyberpunk style label, named neon colours, a sky description
(navy, stars, full moon), a reflection surface (wet street or canal), a camera angle (wide-angle), and an
atmospheric modifier (fog). Each addition constrains the model’s output space toward the reference image.
The result is recognisably closer to the original but still lacks the density of window detail, the specific colour
temperature of the moon, the irregular building rooflines, and the overall neo-noir mood quality.

3.3 Prompt v3 — Advanced (Final)
“Photorealistic render of a futuristic neo-noir cyberpunk megacity at night. Dense cluster of
skyscrapers with dramatically varied heights and irregular Art Deco-influenced silhouettes.
Facades covered in hundreds of small neon-lit windows in electric cyan, magenta, hot pink,
amber yellow, and deep violet. Large neon holographic signs with Japanese-style glyphs and
English text on the three tallest buildings. Deep navy-to-black sky gradient with scattered white
stars and a large warm-yellow full moon with a soft atmospheric halo. Foreground: a still canal
or flooded street perfectly reflecting all neon colours in broken ripple patterns. Lens flares at
each neon sign. Flying vehicles (small lights) in the mid-sky. Shot with a wide-angle lens at eye
level, slightly elevated. Colour grade: high contrast, deep shadows, vivid saturated neon

Prompt v3 is the result of systematic gap-filling based on what v1 and v2 failed to reproduce. It adds: building
silhouette style (Art Deco-influenced, irregular), window density (hundreds of small windows), specific neon
sign detail (holographic, Japanese glyphs), moon quality (warm-yellow, atmospheric halo), reflection detail
(broken ripple pattern), lens flares, flying vehicles, shot parameters (wide-angle, eye level, slightly elevated),
colour grade description, two style references (Blade Runner 2049, Ghost in the Shell), and quality modifiers
(8K, ultra-detailed, volumetric fog).

<img width="762" height="676" alt="image" src="https://github.com/user-attachments/assets/d7ce5f62-8716-4e4f-a736-1a5a71e9a6cc" />

<img width="772" height="861" alt="image" src="https://github.com/user-attachments/assets/6c3b6d0c-0550-4168-aaff-0a5705221612" />

<img width="1437" height="762" alt="image" src="https://github.com/user-attachments/assets/ef8d68e3-8bc3-4571-a10c-bfee3c638261" />


<img width="1320" height="669" alt="image" src="https://github.com/user-attachments/assets/5c42e673-0ec9-4565-8235-b0230ca45d72" />

<img width="1276" height="533" alt="image" src="https://github.com/user-attachments/assets/4115bc0a-7d8c-48b2-b083-5d779d89e9c9" />


The scoring data confirms the visual impression. v1 scored an average of 2.4/10 across all six elements —
the city is recognisable but shares almost none of the visual character of the original. v2 averaged 6.0/10,
capturing the general structure and colour direction but lacking detail density and atmosphere. v3 averaged
8.5/10, achieving strong matches across five of six elements with only the neon sign text rendering falling
slightly short (the AI correctly placed signs but could not perfectly reproduce stylised glyphs and specific text
positioning).

5.4 Remaining Differences in v3
Even the best generated image (v3, advanced prompt) did not achieve a perfect match with the original. Three
categories of difference remained:
• Sign Typography: The original image contains specific neon sign text in a stylised typeface. AI image
generators can approximate neon signs but struggle with precise font rendering, particularly for non -
Latin characters. The generated signs have the right visual weight and position but differ in exact
lettering.
• Building Geometry: The original has a specific skyline shape — a distinctive tall cluster in the centreright
with a step-down to shorter buildings on the left. The generated image reproduced the density
and height variation but not the exact silhouette profile, which would require either a reference image
input (img2img) or a far more granular architectural description.
• Reflection Fidelity: The original shows a high-fidelity mirror reflection of the entire skyline in the
foreground water, with specific ripple distortion patterns. The generated reflection is present and
colourful but less precisely mirrored and with different ripple geometry.

6. DALL·E 3 vs Midjourney — Tool Comparison

<img width="1315" height="787" alt="image" src="https://github.com/user-attachments/assets/39cb4c52-d75c-45ed-8301-5ef42b1d7413" />


Midjourney v6 produced the closest match to the original at the advanced prompt level, driven by its superior
neon lighting quality and cinematic colour grading. DALL·E 3 was more literal in following instructions and
performed relatively better on text rendering, but its overall visual style was cleaner and less atmospheric than
the original’s neo-noir character. For a cyberpunk cityscape, Midjourney’s stylistic defaults are a better fit.


<img width="1364" height="633" alt="image" src="https://github.com/user-attachments/assets/8a77b492-b95f-4f2c-a3dd-4ad2f93fc50c" />

<img width="1228" height="531" alt="image" src="https://github.com/user-attachments/assets/9d6f71f0-558d-4c8c-a772-39755d636066" />

7.2 The Diminishing Returns Principle
An important finding of this experiment is that prompt additions do not produce linear improvements. The jump
from v1 to v2 (adding cyberpunk style, named colours, sky description, reflection, and camera angle) produced
the largest absolute improvement in similarity score (from 2.4 to 6.0 — a 150% increase). The jump from v2
to v3 (adding 15 additional specific elements) produced a smaller absolute improvement (6.0 to 8.5 — a 42%
increase).
This mirrors the pattern observed in text prompt engineering: the first round of refinement yields the largest
return. The core style label (‘cyberpunk’) and the reflection element were responsible for most of the v2
improvement. The v3 additions produced incremental refinement, not transformation. This has a practical
implication: when time is limited, prioritise style reference and one or two distinctive scene elements over
exhaustive specification.
7.3 What AI Image Models Cannot Yet Reproduce from Prompts Alone
This experiment also revealed three categories of visual detail that current text -to-image models consistently
fail to reproduce with high fidelity, regardless of prompt length:
• Specific Spatial Layout: The exact arrangement of buildings in a skyline — which buildings are tallest,
where the skyline peaks and valleys are — cannot be controlled through text alone. Image-to-image
(img2img) or ControlNet skeleton input is needed for precise silhouette replication.
• Typography and Sign Text: AI image generators can place neon signs at the right scale and
brightness but cannot reliably render specific text, especially in stylised or non-Latin fonts. Inpainting
or text overlay in post-processing is required for exact sign replication.
• Specific Ripple Geometry: The exact pattern of light reflections on water is determined by physics
(wind speed, surface tension, light source position) and cannot be described in prose with enough
precision for the model to reproduce a specific reflection pattern.

8. Reflection — Lessons in Visual Prompt Engineering
8.1 The Analysis-First Principle
The most important lesson from this exercise is that effective image prompting begins before writing a single
word. Spending five minutes systematically analysing the original image — breaking it into sky, buildings,
lighting, reflections, mood, camera angle, and colour palette — produced a far more complete prompt than
free-writing from visual impression. Every element of the analysis table in Section 2 contributed at least one
clause to the v3 prompt. Visual analysis and prompt design are the same cognitive task in different registers.
8.2 Style References as Shortcuts
Adding ‘Blade Runner 2049 meets Ghost in the Shell’ to the prompt produced an immediate, dramatic
improvement in atmospheric quality that would have taken many more descriptive words to approximate. Style
references work because the AI model has processed thousands of images tagged with these cultural
references and has a rich internal representation of their visual characteristics. A two-word style reference can
encode what twenty descriptive adjectives cannot. This is one of the most powerful and underused techniques
in visual prompt engineering.
8.3 What Would Be Done Differently
If this experiment were repeated, the first change would be to use the img2img (image-to-image) workflow for
v2 and v3, using a rough sketch or a low-detail generated image as a structural guide for subsequent
generations. This would address the building silhouette and spatial layout limitation identified in Section 7.3.
The second change would be to use negative prompts more aggressively. Both DALL·E 3 and Midjourney
support negative prompting (specifying what should NOT appear). Negative prompts like ‘no daylight, no
desaturated colours, no modern glass office buildings, no cars’ would have helped sharpen the cyberpunk
aesthetic earlier in the process.
8.4 Key Takeaways
• Analyse before you describe. A structured visual analysis produces a complete prompt; free-writing
produces a partial one.
• Name the style. Two-word cultural references (Blade Runner, Ghost in the Shell) encode more visual
information than twenty adjectives.
• Name the colours. ‘Neon lights’ defaults to yellow. ‘Electric cyan, magenta, amber, and violet neon’
produces the right palette.
• The first refinement yields the largest return. Cyberpunk label + reflection + named colours account
for most of the v1→v2 improvement.
• Text and exact spatial layout require non-prompt techniques. Inpainting, ControlNet, and img2img
workflows fill the gaps that text alone cannot close.
• Test across two tools. DALL·E 3 and Midjourney respond differently to the same prompt. Testing both
reveals which tool’s defaults better match the target image style.


9. Conclusion
    
This experiment demonstrated that reproducing a complex visual image through text prompts is a systematic
discipline, not a creative guessing game. By decomposing the original futuristic cityscape into its constituent
visual elements, designing three progressively refined prompts, and evaluating the outputs against a
consistent scoring framework, the exercise produced a final generated image that matched the original at an
8.5/10 similarity level across six key visual dimensions.
The progression from v1 (2.4/10) to v3 (8.5/10) illustrates the compounding value of prompt refinement in
visual AI. Each addition — a style reference, a named colour, a reflection surface, a quality modifier — narrows
the space of possible outputs toward the intended target. The model’s capabilities are largely fixed; the prompt
is the only variable the engineer controls, and controlling it with precision is what separates a generic output
from a purposeful one.
The remaining gap between v3 and the original (8.5 rather than 10) reflects the genuine limitations of text -toimage
generation at its current state of development: spatial layout, typography, and exact reflection geometry
cannot be fully controlled through prompt text alone. These are engineering problems, and the solutions
(img2img, ControlNet, inpainting) are already available. Combining strong prompt engineering with these
complementary techniques brings photorealistic image reproduction within practical reach.

References
1. OpenAI. (2024). DALL·E 3 Image Generation API Documentation.
https://platform.openai.com/docs/guides/images
2. Midjourney. (2024). Midjourney v6 Prompt Reference. https://docs.midjourney.com
3. Rombach, R., et al. (2022). High-Resolution Image Synthesis with Latent Diffusion Models. CVPR 2022.
Stability AI.
4. Saharia, C., et al. (2022). Photorealistic Text-to-Image Diffusion Models with Deep Language
Understanding (Imagen). NeurIPS 2022. Google Brain.
5. White, J., et al. (2023). A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT.
arXiv:2302.11382.
6. Zhang, L., & Agrawala, M. (2023). Adding Conditional Control to Text -to-Image Diffusion Models
(ControlNet). arXiv:2302.05543.

# RESULT :
The prompt-based image reproduction experiment was executed successfully, and the generated images closely matched the original images using refined prompts.
