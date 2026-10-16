# Third-party notices and model licensing

The root [LICENSE](LICENSE) applies to original Foley-Omni source code.
The [MODEL_LICENSE](MODEL_LICENSE) applies to the Foley-Omni checkpoint
`ckpts/Foley-Omni/v2st.pth`, to the extent of rights held by the Foley-Omni
contributors. Neither license replaces the licenses of third-party code,
weights, tokenizers, datasets, or media.

## Source code

Existing copyright and attribution headers remain in place. Third-party
code and adaptations retain the applicable upstream terms, including the
exceptions listed below.

| Component and local scope | Upstream terms and notices |
| --- | --- |
| Wan-derived modules and utilities under `foley_omni/`, including files bearing Alibaba Wan Team copyright headers | [Wan2.2](https://github.com/Wan-Video/Wan2.2), [Apache-2.0](https://github.com/Wan-Video/Wan2.2/blob/main/LICENSE.txt); a copy of Apache-2.0 is in [LICENSE](LICENSE). |
| DiT implementation developed with reference to Ovi, as acknowledged in the README | [Ovi](https://github.com/character-ai/Ovi), [Apache-2.0](https://github.com/character-ai/Ovi/blob/main/LICENSE). |
| MMAudio code under `mmaudio/` and `foley_omni/modules/mmaudio/` | [MMAudio](https://github.com/hkchengrex/MMAudio), MIT, Copyright (c) 2024 Sony Research Inc.; [license copy](third_party_licenses/MMAudio-LICENSE). Nested third-party components retain their separate terms below. |
| `ext/autoencoder/edm2_utils.py` in both MMAudio trees | [EDM2](https://github.com/NVlabs/edm2), **CC BY-NC-SA 4.0**, Copyright (c) 2024 NVIDIA CORPORATION & AFFILIATES; [license copy](third_party_licenses/EDM2-LICENSE.txt). These files are not licensed under Apache-2.0 or MIT. |
| `ext/bigvgan/` and `ext/bigvgan_v2/` in both MMAudio trees | NVIDIA BigVGAN, MIT; [BigVGAN license](third_party_licenses/BigVGAN-LICENSE) and [BigVGAN v2 license](third_party_licenses/BigVGAN-v2-LICENSE), plus the included component notices below. |
| `mmaudio/mmaudio/ext/synchformer/` | [Synchformer](https://github.com/v-iashin/Synchformer), MIT, Copyright (c) 2024 Vladimir Iashin; [license copy](third_party_licenses/Synchformer-LICENSE). The Motionformer-derived `video_model_builder.py` and `vit_helper.py` retain their Facebook and Ross Wightman notices and [Motionformer's Apache-2.0 terms](https://github.com/facebookresearch/Motionformer/blob/main/LICENSE). |
| CLIP/OpenCLIP-derived implementation in `foley_omni/modules/clip.py` | MIT notices from [OpenAI CLIP](third_party_licenses/CLIP-LICENSE) and [OpenCLIP](third_party_licenses/OpenCLIP-LICENSE), in addition to the Wan attribution. |
| Transformers/Diffusers-derived implementations identified in `t5.py`, `xlm_roberta.py`, and the flow-matching solvers | [Transformers](https://github.com/huggingface/transformers/blob/main/LICENSE) and [Diffusers](https://github.com/huggingface/diffusers/blob/main/LICENSE), Apache-2.0. |
| `foley_omni/distributed_comms/communications.py` | Copyright (c) Microsoft Corporation; the file declares SPDX-License-Identifier: Apache-2.0. |

The following BigVGAN component notices are preserved from MMAudio's
`incl_licenses/` directories in [third_party_licenses/](third_party_licenses/).
They apply to the corresponding included or adapted code in both local
MMAudio trees.

| Upstream notice | Component / copyright holder | License |
| --- | --- | --- |
| [LICENSE_1](third_party_licenses/BigVGAN-LICENSE_1) | HiFi-GAN / Jungil Kong | MIT |
| [LICENSE_2](third_party_licenses/BigVGAN-LICENSE_2) | Snake / Edward Dixon | MIT |
| [LICENSE_3](third_party_licenses/BigVGAN-LICENSE_3) | alias-free-torch | Apache-2.0 |
| [LICENSE_4](third_party_licenses/BigVGAN-LICENSE_4) | Seungwon Park | BSD-3-Clause |
| [LICENSE_5](third_party_licenses/BigVGAN-LICENSE_5) | Julius / Alexandre Défossez | MIT |
| [LICENSE_6](third_party_licenses/BigVGAN-LICENSE_6) | Descript | MIT |
| [LICENSE_7](third_party_licenses/BigVGAN-LICENSE_7) | Charactr Inc. | MIT |
| [LICENSE_8](third_party_licenses/BigVGAN-LICENSE_8) | Amphion | MIT |

The MMAudio/BigVGAN/Synchformer license copies were retrieved from
[MMAudio revision 974010a](https://github.com/hkchengrex/MMAudio/tree/974010a026c731054592d8f777218bd9d85a6c24).
This records the source of the notices; it does not assert that every
vendored source file matches that upstream revision.

## Released checkpoints and runtime downloads

The [Hugging Face release](https://huggingface.co/CocoBro/Foley-Omni)
contains the Foley-Omni checkpoint together with third-party assets.
The MIT designation for Foley-Omni does not relicense the whole bundle.

| Asset | Source and applicable terms |
| --- | --- |
| `ckpts/Foley-Omni/v2st.pth` | Foley-Omni checkpoint: [MIT](MODEL_LICENSE), consistent with the Foley-Omni model card, subject to any applicable third-party rights. |
| `ckpts/Wan2.2-TI2V-5B/models_t5_umt5-xxl-enc-bf16.pth` and `ckpts/Wan2.2-TI2V-5B/google/umt5-xxl/*` | Text encoder and tokenizer redistributed from [Wan2.2-TI2V-5B](https://huggingface.co/Wan-AI/Wan2.2-TI2V-5B), whose model card specifies Apache-2.0; see also [Google UMT5-XXL](https://huggingface.co/google/umt5-xxl). |
| `ckpts/mmaudio/ext_weights/v1-16.pth` | Audio VAE distributed through [MMAudio's v0.1 release](https://github.com/hkchengrex/MMAudio/releases/tag/v0.1); retains its upstream checkpoint terms. See the checkpoint note below. |
| `ckpts/mmaudio/ext_weights/best_netG.pt` | 16 kHz vocoder distributed through MMAudio; MMAudio credits [Make-An-Audio 2](https://github.com/bytedance/Make-An-Audio-2) for this pretrained BigVGAN model. The originating checkpoint's terms remain applicable. |
| `ckpts/mmaudio/ext_weights/synchformer_state_dict.pth` | Synchformer feature extractor distributed through MMAudio; consult [Synchformer](https://github.com/v-iashin/Synchformer) and the supplying MMAudio release for the checkpoint's terms. |
| `apple/DFN5B-CLIP-ViT-H-14-384`, fetched by `open_clip` on first use | Separately downloaded image encoder. Its [model repository](https://huggingface.co/apple/DFN5B-CLIP-ViT-H-14-384) and accompanying terms govern that model; Foley-Omni's licenses do not cover it. |

**MMAudio checkpoint note:** MMAudio distinguishes its MIT-licensed code
from its [Hugging Face model release](https://huggingface.co/hkchengrex/MMAudio),
which is explicitly **CC BY-NC 4.0 (non-commercial)**. The auxiliary assets
above are distributed via its GitHub release and include models from other
projects. Consult the terms for the particular asset and its original
source; do not infer a checkpoint license from MMAudio's MIT code license
or from Foley-Omni's MIT model tag. Foley-Omni grants no additional rights
to those assets.

The non-commercial terms identified above, including those of the vendored
EDM2 code, mean that the Apache-2.0 and MIT licenses for Foley-Omni alone
do not authorize commercial use of every component in the complete pipeline.

## Training data and media

Training data sources are described in
[Appendix C.1 and Table 9 of the paper](https://arxiv.org/html/2606.03672v1).
They include public datasets and internal collections. The code and model
licenses do not grant rights to the underlying datasets, recordings, videos,
or other third-party material, and do not replace any applicable upstream
terms. Consult the relevant dataset and media owners' terms when obtaining,
using, or redistributing those materials.

This release does not provide a dataset-by-dataset rights clearance or
certify that every downstream use is cleared. The MIT grant for the
Foley-Omni checkpoint is limited to rights held by the Foley-Omni contributors.
Example media and any future benchmark release are not covered by that
checkpoint license.
