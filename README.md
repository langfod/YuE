<p align="center">
    <picture>
        <source srcset="./assets/logo/黑底.svg" media="(prefers-color-scheme: dark)">
        <img src="./assets/logo/白底.svg" width="40%">
    </picture>
</p>

<p align="center">
    <a href="https://map-yue.github.io/">Demo 🎶</a> &nbsp;|&nbsp; 📑 <a href="https://arxiv.org/abs/2503.08638">Paper</a>
    <br>
    <a href="https://huggingface.co/m-a-p/YuE-s1-7B-anneal-en-cot">YuE-s1-7B-anneal-en-cot 🤗</a> &nbsp;|&nbsp; <a href="https://huggingface.co/m-a-p/YuE-s1-7B-anneal-en-icl">YuE-s1-7B-anneal-en-icl 🤗</a> &nbsp;|&nbsp; <a href="https://huggingface.co/m-a-p/YuE-s1-7B-anneal-jp-kr-cot">YuE-s1-7B-anneal-jp-kr-cot 🤗</a>
    <br>
    <a href="https://huggingface.co/m-a-p/YuE-s1-7B-anneal-jp-kr-icl">YuE-s1-7B-anneal-jp-kr-icl 🤗</a> &nbsp;|&nbsp; <a href="https://huggingface.co/m-a-p/YuE-s1-7B-anneal-zh-cot">YuE-s1-7B-anneal-zh-cot 🤗</a> &nbsp;|&nbsp; <a href="https://huggingface.co/m-a-p/YuE-s1-7B-anneal-zh-icl">YuE-s1-7B-anneal-zh-icl 🤗</a>
    <br>
    <a href="https://huggingface.co/m-a-p/YuE-s2-1B-general">YuE-s2-1B-general 🤗</a> &nbsp;|&nbsp; <a href="https://huggingface.co/m-a-p/YuE-upsampler">YuE-upsampler 🤗</a>
</p>

---
Our model's name is **YuE (乐)**. In Chinese, the word means "music" and "happiness." Some of you may find words that start with Yu hard to pronounce. If so, you can just call it "yeah." We wrote a song with our model's name, see [here](assets/logo/yue.mp3).

YuE is a groundbreaking series of open-source foundation models designed for music generation, specifically for transforming lyrics into full songs (lyrics2song). It can generate a complete song, lasting several minutes, that includes both a catchy vocal track and accompaniment track. YuE is capable of modeling diverse genres/languages/vocal techniques. Please visit the [**Demo Page**](https://map-yue.github.io/) for amazing vocal performance.

## News and Updates
* 📌 Join Us on Discord! [<img alt="join discord" src="https://img.shields.io/discord/842440537755353128?color=%237289da&logo=discord"/>](https://discord.gg/ssAyWMnMzu)

* **2025.06.04 🔥** Now YuE supports LoRA finetune.
* **2025.03.12 🔥 Paper Released🎉**: We now release [YuE technical report](https://arxiv.org/abs/2503.08638)!!! We discuss all the technical details, findings, and lessons learned. Enjoy, and feel free to cite us~
* **2025.03.11 🫶** Now YuE supports incremental song generation!!! See [YuE-UI by joeljuvel](https://github.com/joeljuvel/YuE-UI). YuE-UI is a Gradio-based interface supporting batch generation, output selection, and continuation. You can flexibly experiment with audio prompts and different model settings, visualize your progress on an interactive timeline, rewind actions, quickly preview audio outputs at stage 1 before committing to refinement, and fully save/load your sessions (JSON format). Optimized to run smoothly even on GPUs with just 8GB VRAM using quantized models.
* **2025.02.17 🫶** Now YuE supports music continuation and Google Colab! See [YuE-extend by Mozer](https://github.com/Mozer/YuE-extend).
* **2025.02.07 🎉** Get YuE for Windows on [pinokio](https://pinokio.computer).

* **2025.01.30 🔥 Inference Update**: We now support dual-track ICL mode! You can prompt the model with a reference song, and it will generate a new song in a similar style (voice cloning [demo by @abrakjamson](https://x.com/abrakjamson/status/1885932885406093538), music style transfer [demo by @cocktailpeanut](https://x.com/cocktailpeanut/status/1886456240156348674), etc.). Try it out! 🔥🔥🔥 P.S. Be sure to check out the demos first—they're truly impressive. 

* **2025.01.30 🔥 Announcement: A New Era Under Apache 2.0 🔥**: We are thrilled to announce that, in response to overwhelming requests from our community, **YuE** is now officially licensed under the **Apache 2.0** license. We sincerely hope this marks a watershed moment—akin to what Stable Diffusion and LLaMA have achieved in their respective fields—for music generation and creative AI. 🎉🎉🎉

* **2025.01.29 🎉**: We have updated the license description. we **ENCOURAGE** artists and content creators to sample and incorporate outputs generated by our model into their own works, and even monetize them. The only requirement is to credit our name: **YuE by HKUST/M-A-P** (alphabetic order).
* **2025.01.28 🫶**: Thanks to Fahd for creating a tutorial on how to quickly get started with YuE. Here is his [demonstration](https://www.youtube.com/watch?v=RSMNH9GitbA).
* **2025.01.26 🔥**: We have released the **YuE** series.

<br>

## Requirements

  Give unrestricted script access to powershell so venv can work:

- Open an administrator powershell window
- Type `Set-ExecutionPolicy Unrestricted` and answer A
- Close admin powershell window

~~Python >=3.8 is recommended.~~

~~Install dependencies with the following command:~~

~~```
pip install -r requirements.txt
~~```~~

~~### **Important: Install FlashAttention 2**~~
~~For saving GPU memory, **FlashAttention 2 is mandatory**. Without it, large sequence lengths will lead to out-of-memory (OOM) errors, especially on GPUs with limited memory. Install it using the following command:~~
~~```
pip install flash-attn --no-build-isolation
~~```~~
~~Before installing FlashAttention, ensure that your CUDA environment is correctly set up. ~~
~~For example, if you are using CUDA 11.8:~~
~~- If using a module system:~~
~~``` module load cuda11.8/toolkit/11.8.0 ```~~
~~- Or manually configure CUDA in your shell:~~
~~```
    export PATH=/usr/local/cuda-11.8/bin:$PATH
    export LD_LIBRARY_PATH=/usr/local/cuda-11.8/lib64:$LD_LIBRARY_PATH
~~```~~
---
## TODOs📋

- [ ] Support stemgen mode https://github.com/multimodal-art-projection/YuE/issues/21
- [ ] Support llama.cpp https://github.com/ggerganov/llama.cpp/issues/11467
- [ ] Support transformers tensor parallel. https://github.com/multimodal-art-projection/YuE/issues/7
- [ ] Online serving on huggingface space.
- [ ] Support vLLM and sglang https://github.com/multimodal-art-projection/YuE/issues/66
- [x] Release paper to Arxiv.
- [x] Example LoRA finetune code using 🤗 Transformers.
- [x] Support Colab: [YuE-extend by Mozer](https://github.com/Mozer/YuE-extend)
- [x] Support gradio interface. https://github.com/multimodal-art-projection/YuE/issues/1
- [x] Support dual-track ICL mode.
- [x] Fix "instrumental" naming bug in output files. https://github.com/multimodal-art-projection/YuE/pull/26
- [x] Support seeding https://github.com/multimodal-art-projection/YuE/issues/20
- [x] Allow `--repetition_penalty` to customize repetition penalty. https://github.com/multimodal-art-projection/YuE/issues/45

---

## Hardware and Performance

### **GPU Memory**
YuE requires significant GPU memory for generating long sequences. Below are the recommended configurations:
- **For GPUs with 24GB memory or less**: Run **up to 2 sessions** to avoid out-of-memory (OOM) errors. Thanks to the community, there are [YuE-exllamav2](https://github.com/sgsdxzy/YuE-exllamav2) and [YuEGP](https://github.com/deepbeepmeep/YuEGP) for those with limited GPU resources. While both enhance generation speed and coherence, they may compromise musicality. (P.S. Better prompts & ICL help!)
- **For full song generation** (many sessions, e.g., 4 or more): Use **GPUs with at least 80GB memory**. i.e. H800, A100, or multiple RTX4090s with tensor parallel.

To customize the number of sessions, the interface allows you to specify the desired session count. By default, the model runs **2 sessions** (1 verse + 1 chorus) to avoid OOM issue.

### **Execution Time**
On an **H800 GPU**, generating 30s audio takes **150 seconds**.
On an **RTX 4090 GPU**, generating 30s audio takes approximately **360 seconds**. 

---

## 🪟 Windows Users Quickstart
- For a **one-click installer**, use [Pinokio](https://pinokio.computer).  
- To use **Gradio with Docker**, see: [YuE-for-Windows](https://github.com/sdbds/YuE-for-windows)

## 🐧 Linux/WSL Users Quickstart
For a **quick start**, watch this **video tutorial** by Fahd: [Watch here](https://www.youtube.com/watch?v=RSMNH9GitbA).  
If you're new to **machine learning** or the **command line**, we highly recommend watching this video first.  

To use a **GUI/Gradio** interface, check out:  
- [YuE-exllamav2-UI](https://github.com/WrongProtocol/YuE-exllamav2-UI)
- [YuEGP](https://github.com/deepbeepmeep/YuEGP)
- [YuE-Interface](https://github.com/alisson-anjos/YuE-Interface)  

### 1. Install environment and dependencies
~~Make sure properly install flash attention 2 to reduce VRAM usage.~~ 
~~```bash~~
~~# We recommend using conda to create a new environment.~~
~~conda create -n yue python=3.8 # Python >=3.8 is recommended.
conda activate yue~~
~~# install cuda >= 11.8~~
~~conda install pytorch torchvision torchaudio cudatoolkit=11.8 -c pytorch -c nvidia
pip install -r <(curl -sSL https://raw.githubusercontent.com/multimodal-art-projection/YuE/main/requirements.txt)

~~# For saving GPU memory, FlashAttention 2 is mandatory.~~
~~# Without it, long audio may lead to out-of-memory (OOM) errors.~~
~~# Be careful about matching the cuda version and flash-attn version
pip install flash-attn --no-build-isolation~~
~~```~~

### 2. Download the infer code and tokenizer
```bash
# Make sure you have git-lfs installed (https://git-lfs.com)
# if you don't have root, see https://github.com/git-lfs/git-lfs/issues/4134#issuecomment-1635204943
sudo apt update
sudo apt install git-lfs
git lfs install
git clone https://github.com/sdbds/YuE-for-windows.git
```
~~cd YuE/inference/~~
~~git clone https://huggingface.co/m-a-p/xcodec_mini_infer~~

~~Here’s a quick guide to help you generate music with **YuE** using 🤗 Transformers. Before running the code, make sure your environment is properly set up, and that all dependencies are installed.~~

powershell run with `1、install-uv-qinglong.ps1` (right click then choose `use powershell run`) auto install in one-clik

### 3. Run the inference
Now generate music with **YuE** using 🤗 Transformers. Make sure your step [1](#1-install-environment-and-dependencies) and [2](#2-download-the-infer-code-and-tokenizer) are properly set up. 

Note:
- Set `--run_n_segments` to the number of lyric sections if you want to generate a full song. Additionally, you can increase `--stage2_batch_size` based on your available GPU memory.

powershell run with `2、run.ps1` (right click then choose `use powershell run`)

You can edit  `2、run.ps1` for setting args below:

In the following example, customize the `genres` and `lyrics` in the script, then execute it to generate a song with **YuE**.
- You may customize the prompt in `genre.txt` and `lyrics.txt`. See prompt engineering guide [here](#prompt-engineering-guide).

- You can increase `--stage2_batch_size` to speed up the inference, but be careful for OOM.

- LM ckpts will be automatically downloaded from huggingface. 


~~```bash~~    
~# This is the CoT mode.
cd YuE/inference/
python infer.py \
    --cuda_idx 0 \
    --stage1_model m-a-p/YuE-s1-7B-anneal-en-cot \
    --stage2_model m-a-p/YuE-s2-1B-general \
    --genre_txt ../prompt_egs/genre.txt \
    --lyrics_txt ../prompt_egs/lyrics.txt \
    --run_n_segments 2 \
    --stage2_batch_size 4 \
    --output_dir ../output \
    --max_new_tokens 3000 \
    --repetition_penalty 1.1
~~```~~

We also support music in-context-learning (provide a reference song), there are 2 types: single-track (mix/vocal/instrumental) and dual-track. 

Note: 
- ICL requires a different ckpt, e.g. `m-a-p/YuE-s1-7B-anneal-en-icl`.

- Music ICL generally requires a 30s audio segment. The model will write new songs with similar style of the provided audio, and may improve musicality.

- Dual-track ICL works better in general, requiring both vocal and instrumental tracks.

- For single-track ICL, you can provide a mix, vocal, or instrumental track.

- You can separate the vocal and instrumental tracks using [python-audio-separator](https://github.com/nomadkaraoke/python-audio-separator) or [Ultimate Vocal Remover GUI](https://github.com/Anjok07/ultimatevocalremovergui).

~~```bash~~
~# This is the dual-track ICL mode.
~# To turn on dual-track mode, enable `--use_dual_tracks_prompt`
~# and provide `--vocal_track_prompt_path`, `--instrumental_track_prompt_path`, 
~# `--prompt_start_time`, and `--prompt_end_time`
~# The ref audio is taken from GTZAN test set.
cd YuE/inference/
python infer.py \
    --cuda_idx 0 \
    --stage1_model m-a-p/YuE-s1-7B-anneal-en-icl \
    --stage2_model m-a-p/YuE-s2-1B-general \
    --genre_txt ../prompt_egs/genre.txt \
    --lyrics_txt ../prompt_egs/lyrics.txt \
    --run_n_segments 2 \
    --stage2_batch_size 4 \
    --output_dir ../output \
    --max_new_tokens 3000 \
    --repetition_penalty 1.1 \
    --use_dual_tracks_prompt \
    --vocal_track_prompt_path ../prompt_egs/pop.00001.Vocals.mp3 \
    --instrumental_track_prompt_path ../prompt_egs/pop.00001.Instrumental.mp3 \
    --prompt_start_time 0 \
    --prompt_end_time 30 
~~~```~~~

~~~```bash~~~
# This is the single-track (mix/vocal/instrumental) ICL mode.
# To turn on single-track ICL, enable `--use_audio_prompt`, 
# and provide `--audio_prompt_path` , `--prompt_start_time`, and `--prompt_end_time`. 
# The ref audio is taken from GTZAN test set.
cd YuE/inference/
python infer.py \
    --cuda_idx 0 \
    --stage1_model m-a-p/YuE-s1-7B-anneal-en-icl \
    --stage2_model m-a-p/YuE-s2-1B-general \
    --genre_txt ../prompt_egs/genre.txt \
    --lyrics_txt ../prompt_egs/lyrics.txt \
    --run_n_segments 2 \
    --stage2_batch_size 4 \
    --output_dir ../output \
    --max_new_tokens 3000 \
    --repetition_penalty 1.1 \
    --use_audio_prompt \
    --audio_prompt_path ../prompt_egs/pop.00001.mp3 \
    --prompt_start_time 0 \
    --prompt_end_time 30
~~```~~
 
## Prompt Engineering Guide
The prompt consists of three parts: genre tags, lyrics, and ref audio.

### Genre Tagging Prompt
1. An example genre tagging prompt can be found [here](prompt_egs/genre.txt).

2. A stable tagging prompt usually consists of five components: genre, instrument, mood, gender, and timbre. All five should be included if possible, separated by space (space delimiter).

3. Although our tags have an open vocabulary, we have provided the top 200 most commonly used [tags](./top_200_tags.json). It is recommended to select tags from this list for more stable results.

3. The order of the tags is flexible. For example, a stable genre tagging prompt might look like: "inspiring female uplifting pop airy vocal electronic bright vocal vocal."

4. Additionally, we have introduced the "Mandarin" and "Cantonese" tags to distinguish between Mandarin and Cantonese, as their lyrics often share similarities.

### Lyrics Prompt
1. An example lyric prompt can be found [here](prompt_egs/lyrics.txt).

2. We support multiple languages, including but not limited to English, Mandarin Chinese, Cantonese, Japanese, and Korean. The default top language distribution during the annealing phase is revealed in [issue 12](https://github.com/multimodal-art-projection/YuE/issues/12#issuecomment-2620845772). A language ID on a specific annealing checkpoint indicates that we have adjusted the mixing ratio to enhance support for that language.

3. The lyrics prompt should be divided into sessions, with structure labels (e.g., [verse], [chorus], [bridge], [outro]) prepended. Each session should be separated by 2 newline character "\n\n".

4. **DONOT** put too many words in a single segment, since each session is around 30s (`--max_new_tokens 3000` by default).

5. We find that [intro] label is less stable, so we recommend starting with [verse] or [chorus].

6. For generating music with no vocal (instrumental only), see [issue 18](https://github.com/multimodal-art-projection/YuE/issues/18).


### Audio Prompt

1. Audio prompt is optional. Providing ref audio for ICL usually increase the good case rate, and result in less diversity since the generated token space is bounded by the ref audio. CoT only (no ref) will result in a more diverse output.

2. We find that dual-track ICL mode gives the best musicality and prompt following. 

3. Use the chorus part of the music as prompt will result in better musicality.

4. Around 30s audio is recommended for ICL.

5. For music continuation, see [YuE-extend by Mozer](https://github.com/Mozer/YuE-extend). Also supports Colab.

---

## License Agreement \& Disclaimer  
- The YuE model (including its weights) is now released under the **Apache License, Version 2.0**. We do not make any profit from this model, and we hope it can be used for the betterment of human creativity.
- **Use & Attribution**: 
    - We encourage artists and content creators to freely incorporate outputs generated by YuE into their own works, including commercial projects. 
    - We encourage attribution to the model’s name (“YuE by HKUST/M-A-P”), especially for public and commercial use. 
- **Originality & Plagiarism**: It is the sole responsibility of creators to ensure that their works, derived from or inspired by YuE outputs, do not plagiarize or unlawfully reproduce existing material. We strongly urge users to perform their own due diligence to avoid copyright infringement or other legal violations.
- **Recommended Labeling**: When uploading works to streaming platforms or sharing them publicly, we **recommend** labeling them with terms such as: “AI-generated”, “YuE-generated", “AI-assisted” or “AI-auxiliated”. This helps maintain transparency about the creative process.
- **Disclaimer of Liability**: 
    - We do not assume any responsibility for the misuse of this model, including (but not limited to) illegal, malicious, or unethical activities. 
    - Users are solely responsible for any content generated using the YuE model and for any consequences arising from its use. 
    - By using this model, you agree that you understand and comply with all applicable laws and regulations regarding your generated content.

---

## Acknowledgements
The project is co-lead by HKUST and M-A-P (alphabetic order). Also thanks moonshot.ai, bytedance, 01.ai, and geely for supporting the project.
A friendly link to HKUST Audio group's [huggingface space](https://huggingface.co/HKUSTAudio). 

We deeply appreciate all the support we received along the way. Long live open-source AI!

---

## Citation

If you find our paper and code useful in your research, please consider giving a star :star: and citation :pencil: :)

```BibTeX
@misc{yuan2025yuescalingopenfoundation,
      title={YuE: Scaling Open Foundation Models for Long-Form Music Generation}, 
      author={Ruibin Yuan and Hanfeng Lin and Shuyue Guo and Ge Zhang and Jiahao Pan and Yongyi Zang and Haohe Liu and Yiming Liang and Wenye Ma and Xingjian Du and Xinrun Du and Zhen Ye and Tianyu Zheng and Zhengxuan Jiang and Yinghao Ma and Minghao Liu and Zeyue Tian and Ziya Zhou and Liumeng Xue and Xingwei Qu and Yizhi Li and Shangda Wu and Tianhao Shen and Ziyang Ma and Jun Zhan and Chunhui Wang and Yatian Wang and Xiaowei Chi and Xinyue Zhang and Zhenzhu Yang and Xiangzhou Wang and Shansong Liu and Lingrui Mei and Peng Li and Junjie Wang and Jianwei Yu and Guojian Pang and Xu Li and Zihao Wang and Xiaohuan Zhou and Lijun Yu and Emmanouil Benetos and Yong Chen and Chenghua Lin and Xie Chen and Gus Xia and Zhaoxiang Zhang and Chao Zhang and Wenhu Chen and Xinyu Zhou and Xipeng Qiu and Roger Dannenberg and Jiaheng Liu and Jian Yang and Wenhao Huang and Wei Xue and Xu Tan and Yike Guo},
      year={2025},
      eprint={2503.08638},
      archivePrefix={arXiv},
      primaryClass={eess.AS},
      url={https://arxiv.org/abs/2503.08638}, 
}

@misc{yuan2025yue,
  title={YuE: Open Music Foundation Models for Full-Song Generation},
  author={Ruibin Yuan and Hanfeng Lin and Shawn Guo and Ge Zhang and Jiahao Pan and Yongyi Zang and Haohe Liu and Xingjian Du and Xeron Du and Zhen Ye and Tianyu Zheng and Zhengxuan Jiang and Yinghao Ma and Minghao Liu and Lijun Yu and Zeyue Tian and Ziya Zhou and Liumeng Xue and Xingwei Qu and Yizhi Li and Tianhao Shen and Ziyang Ma and Shangda Wu and Jun Zhan and Chunhui Wang and Yatian Wang and Xiaohuan Zhou and Xiaowei Chi and Xinyue Zhang and Zhenzhu Yang and Yiming Liang and Xiangzhou Wang and Shansong Liu and Lingrui Mei and Peng Li and Yong Chen and Chenghua Lin and Xie Chen and Gus Xia and Zhaoxiang Zhang and Chao Zhang and Wenhu Chen and Xinyu Zhou and Xipeng Qiu and Roger Dannenberg and Jiaheng Liu and Jian Yang and Stephen Huang and Wei Xue and Xu Tan and Yike Guo}, 
  howpublished={\url{https://github.com/multimodal-art-projection/YuE}},
  year={2025},
  note={GitHub repository}
}
```
<br>
