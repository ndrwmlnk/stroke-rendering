# Stroke-based-painting
Repository for the survey on stroke-based painterly rendering algorithms

_Note:_ Not all GitHub links are the official implementations!

## Greedy heuristics
__Edge alignment:__  Align stroke direction with edges and contours of image.

 - _Low-level:_ e.g. edges from Sobel filter or Canny edge detection

 - _High-level:_ e.g. semantic / salient edges and contours of objects

__Region approximation__: Replace image segments with strokes.

 - _Image moments:_ Soft / fuzzy image segmentation algorithms

 - _imgage segmentation_ "Normal" image segmentation algorithms (hard edges)

Name  | Algorithm | Notes / Description
------------- | ------------- | - 
Paint by numbers: Abstract image representations | Low-level edge alignment | The first painterly rendering paper!
Processing images and video for an impressionist effect | Low-level edge alignment | 
Painterly rendering with curved brush strokes of multiple sizes | Low-level edge alignment | First algorithm with curved strokes. [[Java]](https://github.com/hertzmann/painterJava) [[Python (Unofficial)]](https://github.com/pschaldenbrand/PyPainterly)
Image and video based painterly animation | Low-level edge alignment | 
Painterly rendering controlled by multiscale image features | Low-level edge alignment | 
Interactive painterly stylization of images, videos and 3D animations | Low-level edge alignment | 
Contour-driven Sumi-e rendering of real photos | Low-level edge alignment | Connected to [Artist Agent](https://arxiv.org/abs/1206.4634)
Painterly rendering with content-dependent natural paint strokes | Low-level edge alignment | 
Painterly rendering using image salience | High-level edge alignment | 
Abstracted painterly renderings using eye-tracking data | High-level edge alignment | 
From image parsing to painterly rendering | High-level edge alignment | 
Video painting with space-time-varying style parameters | High-level edge alignment | 
Artistic composition for painterly rendering | High-level edge alignment | 
An algorithm for automatic painterly rendering based on local source image approximation | Image moments | 
Multiscale moment-based painterly rendering | Image moments | 
Artistic vision: painterly rendering using computer vision techniques | Image segmentation | 
Empathic painting: interactive stylization through observed emotional state | Image segmentation | 
Emotionally aware automated portrait painting | Image segmentation | 
Abstract art by shape classification | Image segmentation | 
A generic framework for the structured abstraction of images | Image segmentation | [[Code]](https://github.com/nounsse/Image-Abstraction)


## Iterative error minimization

__Brute force:__ Systematically try out many different paramters until a good result is achieved
 - _Stroke database:_ Choose best stroke from database

__Randomized search:__ Randomly perturb stroke parameters to find good painting. Different stochastic optimization algorithms are possible.
 - _Hill climbing_
 - _Simulated annealing_
 - _Genetic / evolutionary optimization_

__Gradient descent:__ Change parameters in negative gradient direction. Good and fast results, but usually requires differentiable rendering.

Name  | Algorithm | Notes / Description
------------- | ------------- | -
Paint by Numbers  | Hill climbing | The first painterly rendering paper!
Paint by relaxation | Brute force | 
Anipaint: Interactive painterly animation from video | Brute force | 
Interactive painterly rendering with artistic error correction | Stroke database | 
A painterly rendering based on stroke profile and database | Stroke database | 
Stroke based painterly rendering with mass data through auto warping generation | Stroke database | 
Portrait painting using active templates | Stroke database | 
Random paintbrush transformation | Hill climbing | 
Optimization of paintbrush rendering of images by dynamic mcmc methods | Hill climbing | 
Genetic paint: A search for salient paintings | Genetic / evolutionary optimization | 
A unified scheme for adaptive stroke-based rendering | Simulated annealing | 
Image-based painterly rendering by evolutionary algorithm | Genetic / evolutionary optimization | 
Evolved art with transparent, overlapping, and geometric shapes | Genetic / evolutionary optimization | [[Code]](https://github.com/joacber/Evolved-art-with-transparent-overlapping-and-geometric-shapes)
Paintings, polygons and plant propagation | Genetic / evolutionary optimization, Simulated annealing, Hill climbing | [[Code]](https://github.com/paintingbrushstroke/paintings)
Automatic and interactive evolution of vector graphics images with genetic algorithms | Genetic / evolutionary optimization | 
Incremental Evolution of Stylized Images | Genetic / evolutionary optimization | [[Code]](https://github.com/floAr/EvolutionaryArtistUnity)
Generative art using neural visual grammars and dual encoders | Genetic / evolutionary optimization | [[Code]](https://github.com/deepmind/arnheim)
Modern evolution strategies for creativity: Fitting concrete images and abstract concepts | Genetic / evolutionary optimization | [[Code]](https://github.com/google/brain-tokyo-workshop/tree/master/es-clip)
Customizing painterly rendering styles using stroke processes | Reaction-diffusion process | [[Code]](https://github.com/mingtianzhao/stroke_processes)
Neural painters: A learned differentiable constraint for generating brushstroke paintings | Gradient descent | [[Code]](https://github.com/reiinakano/neural-painters-pytorch)
Differentiable vector graphics rasterization for editing and learning | Gradient descent | [[Code]](https://github.com/BachiLi/diffvg)
Stylized neural painting | Gradient descent | [[Code]](https://github.com/jiupinjia/stylized-neural-painting)
From Objects to a Whole Painting | Gradient descent | 
Rethinking style transfer: From pixels to parameterized brushstrokes | Gradient descent | [[Code]](https://github.com/CompVis/brushstroke-parameterized-style-transfer)
Differentiable drawing and sketching | Gradient descent | [[Code]](https://github.com/jonhare/DifferentiableSketching)
CLIPDraw: Exploring text-to-drawing synthesis through language-image encoders | Gradient descent | [[Code]](https://github.com/kvfrans/clipdraw)
StyleCLIPDraw: Coupling Content and Style in Text-to-Drawing Translation |  Gradient descent | [[Code]](https://github.com/pschaldenbrand/StyleCLIPDraw)
CLIP-CLOP: CLIP-Guided Collage and Photomontage | Gradient descent |  [[Code]](https://github.com/deepmind/arnheim)

## Deep learning

__Supervised Learning:__ Predicts sequence of stroke parameters from pixel canvas by using differentiable rendering

__Deep Reinforcement Learning (DRL):__ Agent predicts next stroke to paint, given canvas and target.
 - _Model-free DRL:_ Does not use differentiable rendering
 - _Model-based DRL:_ Uses differentiable rendering

Name  | Architecture | Notes / Description
------------- | ------------- | -
Unsupervised image to sequence translation with canvas-drawer networks | Supervised learning | [[Unofficial code]](https://github.com/wgoldie/canvasdrawer)
Strokenet: A neural painting environment | Supervised learning | [[Code]](https://github.com/vexilligera/strokenet)
Paint transformer: Feed forward neural painting with stroke prediction | Supervised learning | [[Code]](https://github.com/Huage001/PaintTransformer)
Synthesizing programs for images using reinforced adversarial learning ("SPIRAL") | Model-free DRL | [[Code]](https://github.com/deepmind/spiral)
Unsupervised doodling and painting with improved spiral ("SPIRAL++")| Model-free DRL | [[Unofficial code]](https://github.com/urw7rs/spiralpp)
Paintbot: A reinforcement learning approach for natural media painting | Model-free DRL | 
LpaintB: Learning to paint from self-supervision | Model-free DRL | 
Learning to paint with model-based deep reinforcement learning | Model-based DRL | [[Code]](https://github.com/megvii-research/ICCV2019-LearningToPaint)
Demystify Painting with RL | Model-based DRL | 
Content masked loss: Human-like brush stroke planning in a reinforcement learning painting agent | Model-based DRL | [[Code]](https://github.com/pschaldenbrand/ContentMaskedLoss)
Combining semantic guidance and deep reinforcement learning for generating human level paintings | Model-based DRL | [[Code]](https://github.com/1jsingh/semantic-guidance)
Intelli-Paint: Towards Developing Human-like Painting Agents | Model-based DRL | 

## Video painting

Different techniques for extending painterly rendering algorithms to handle video.

Name  | GitHub | Notes / Description
------------- | ------------- | -
Primitive Pictures | [[Code]](https://github.com/fogleman/primitive) |  Ready to use application / GitHub for video painting
AniPainter | [[Code]](https://github.com/pschaldenbrand/AniPainter)| Digitally painted and robot painted videos
Processing images and video for an impressionist effect |   | 
Painterly rendering for video and interaction |   | 
Image and video based painterly animation |   | 
Video painting with space-time-varying style parameters |  | 
Motion map generation for maintaining the temporalcoherence of brush strokes |   | 
Interactive painterly stylization of images, videos and 3D animations |   | 
Painterly animation using video semantics and feature correspondence |   | 
Anipaint: Interactive painterly animation from video |   | 

