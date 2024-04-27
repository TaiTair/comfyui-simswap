# Simswap Node for ComfyUI

A hacky implementation of Simswap based on [Comfyui ReActor Node 0.5.1](https://github.com/Gourieff/comfyui-reactor-node) and [Simswap](https://github.com/neuralchen/SimSwap)

I just put this together so that I could use Simswap in my workflows. It's probably bloated with lots of unnecessary code and probably does not work optimally. A lot of the options for Simswap are not exposed and the default values are being used. But it is able to use the simswap model, uniface and also ghost.

## Installation

git clone this repo into your comfyui/custom_nodes directory

## Models

Download the simswap models from here and place them under comfyui/models/simswap: https://huggingface.co/netrunner-exe/Insight-Swap-models-onnx/tree/main  
Download the arcface model from here and place it under comfyui/models/simswap: https://github.com/neuralchen/SimSwap/blob/main/docs/guidance/preparation.md  
Download the mask from here and place it under comfyui/models/simswap: https://github.com/zllrunning/face-makeup.PyTorch/blob/master/cp/79999_iter.pth  
Download the 512 Net_G model from here and place it under comfyui/models/simswap: https://github.com/neuralchen/SimSwap/releases/download/512_beta/512.zip  
^ It should look like comfyui/models/simswap/512/550000_net_G.pth

Edit: I just noticed the insightface model link was broken so I replaced it.  
Download the insightface models from here: https://huggingface.co/immich-app/antelopev2/tree/main  
You need to rename them both and place them in comfyui/models/simswap/antelope  
The recognition model should be named glintr100.onnx  
The detection model should be named scrfd_10g_bnkps.onnx  

## Test

Load up comfyui - place the node and try it out! So far my best results were with ghost_unet_3block, restore face set to gfpgan, codeformer weight to 1.00 and restore face visibility to 0.8.

## Final Notes

My objective for this was just to get the simswap model working in ComfyUI for my own workflows. I will not be maintaining it or adding to it. If anyone wants to take over the repo then feel free to contact me. Also feel free to put in your own pull requests!

<a name="credits">

## Thanks and Credits

Thanks to all the creators mentioned in the Reactor Credits.

<details>
	<summary><a>Click to expand</a></summary>

<br>

|file|source|license|
|----|------|-------|
|[buffalo_l.zip](https://huggingface.co/datasets/Gourieff/ReActor/blob/main/models/buffalo_l.zip) | [DeepInsight](https://github.com/deepinsight/insightface) | ![license](https://img.shields.io/badge/license-non_commercial-red) |
| [codeformer-v0.1.0.pth](https://huggingface.co/datasets/Gourieff/ReActor/blob/main/models/facerestore_models/codeformer-v0.1.0.pth) | [sczhou](https://github.com/sczhou/CodeFormer) | ![license](https://img.shields.io/badge/license-non_commercial-red) |
| [GFPGANv1.3.pth](https://huggingface.co/datasets/Gourieff/ReActor/blob/main/models/facerestore_models/GFPGANv1.3.pth) | [TencentARC](https://github.com/TencentARC/GFPGAN) | ![license](https://img.shields.io/badge/license-Apache_2.0-green.svg) |
| [GFPGANv1.4.pth](https://huggingface.co/datasets/Gourieff/ReActor/blob/main/models/facerestore_models/GFPGANv1.4.pth) | [TencentARC](https://github.com/TencentARC/GFPGAN) | ![license](https://img.shields.io/badge/license-Apache_2.0-green.svg) |
| [inswapper_128.onnx](https://github.com/facefusion/facefusion-assets/releases/download/models/inswapper_128.onnx) | [DeepInsight](https://github.com/deepinsight/insightface) | ![license](https://img.shields.io/badge/license-non_commercial-red) |
| [inswapper_128_fp16.onnx](https://github.com/facefusion/facefusion-assets/releases/download/models/inswapper_128_fp16.onnx) | [Hillobar](https://github.com/Hillobar/Rope) | ![license](https://img.shields.io/badge/license-non_commercial-red) |

[BasicSR](https://github.com/XPixelGroup/BasicSR) - [@XPixelGroup](https://github.com/XPixelGroup) <br>
[facexlib](https://github.com/xinntao/facexlib) - [@xinntao](https://github.com/xinntao) <br>

[@s0md3v](https://github.com/s0md3v), [@henryruhs](https://github.com/henryruhs) - the original Roop App <br>
[@ssitu](https://github.com/ssitu) - the first version of [ComfyUI_roop](https://github.com/ssitu/ComfyUI_roop) extension <br>
[neuralchen](https://github.com/neuralchen/SimSwap) - The official implementation of Simswap <br><br>

And thanks to anyone else that was involved in the creation of this node that I failed to mention.
</details>
