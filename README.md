# freeswitch-mod_av
ai修改mod_av 支持硬解码、硬编码，To enable AI to modify the mod_av module to support hardware decoding and encoding


# 本例子在ubuntu 24.04 下cuda gpu测试通过 安装freeswitch只要替换下mod_av/avcode.c 即可 


# ffmpeg 需要安装支持硬解 
ffmpeg -hide_banner -decoders | grep -E "cuvid|nvdec|cuda" 


 V..... av1_cuvid            Nvidia CUVID AV1 decoder (codec av1)
 V..... h264_cuvid           Nvidia CUVID H264 decoder (codec h264)
 V..... hevc_cuvid           Nvidia CUVID HEVC decoder (codec hevc)
 V..... mjpeg_cuvid          Nvidia CUVID MJPEG decoder (codec mjpeg)
 V..... mpeg1_cuvid          Nvidia CUVID MPEG1VIDEO decoder (codec mpeg1video)
 V..... mpeg2_cuvid          Nvidia CUVID MPEG2VIDEO decoder (codec mpeg2video)
 V..... mpeg4_cuvid          Nvidia CUVID MPEG4 decoder (codec mpeg4)
 V..... vc1_cuvid            Nvidia CUVID VC1 decoder (codec vc1)
 V..... vp8_cuvid            Nvidia CUVID VP8 decoder (codec vp8)
 V..... vp9_cuvid            Nvidia CUVID VP9 decoder (codec vp9)


ffmpeg -hide_banner -encoders | grep -E "nvenc"


 V....D av1_nvenc            NVIDIA NVENC av1 encoder (codec av1)
 V....D h264_nvenc           NVIDIA NVENC H.264 encoder (codec h264)
 V....D hevc_nvenc           NVIDIA NVENC hevc encoder (codec hevc)

# 测试 16g gpu 大概能支持30人左右 720p,
