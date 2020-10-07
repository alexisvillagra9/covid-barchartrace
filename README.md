### REQUERIMIENTOS WINDOS
Como vamos a usar la libreria **"Bar Chart Race"** se debe tener previamente instalado unos codecs para imagen y video.

##### IMAGEMAGICK
Primero instalaremos el ImageMagick (necesaria para crear los gif animado)
Yo use la version **ImageMagick-7.0.10-33-Q16-HDRI-x64-dll.exe** de la  [PAGINA OFICIAL](https://imagemagick.org/script/download.php#windows)
Una vez instalado comprobaremos que se hayan creado las variables de entorno con el siguiente comando en nuestra terminal de windows:
```sh
magick -version
```
La respuesta a dicho comando deberia ser similar a la siguiente:
```sh
Version: ImageMagick 7.0.10-33 Q16 x64 2020-10-04 http://www.imagemagick.org
Copyright: Copyright (C) 1999-2018 ImageMagick Studio LLC
License: http://www.imagemagick.org/script/license.php
Visual C++: 192729111
Features: Cipher DPC HDRI Modules OpenCL OpenMP(2.0)
Delegates (built-in): bzlib cairo flif freetype gslib heic jng jp2 jpeg lcms lqr lzma openexr pangocairo png ps raw rsvg tiff webp xml zlib
```

##### FFMPEG
Segundo instalaremos el ffmpeg (necesaria para crear los videos)
Yo use la version **ffmpeg-N-99484-ga086b73e1f-win64-gpl-shared-vulkan.zip** de la siguiente [PAGINA](https://github.com/BtbN/FFmpeg-Builds/releases)
Una vez descargado el .zip seguimos los siguientes pasos:
* Extraer la carpeta
* Renombrar *"ffmpeg-N-99481-g1e97fbb3b6-win64-gpl-shared-vulkan"* por *"ffmpeg"*
* Copiar y pegar la carpeta en la raiz del disco C:\
* Ejecutar el siguiente comando:
* Agregar la ruta *"C:\ffmpeg\bin"* en la variable de entorno *"PATH"*
    1. Buscar en el incio de windows: "Editar las variables de entorno"
    ![](https://lh4.googleusercontent.com/yCHEhojrbTO35cAvULYWYkX67kB65sgPtFG8wyv7EYMK9Q7n0ADa8acnA8YI0lU23KsJyOM1x4NuBg=w300-h757)
    2. Luego hacer click en *"Variables de entorno"*
    ![](https://lh4.googleusercontent.com/oc7FQHsH2L_FO6ZadWjyw20vh9hBzyIGnR85l9_uwPxPrt0-6fyUnZmBiFOAJajN-0GiwgjwDTdZMg=w300-h757)
    3. Editar la variable Paht
    ![](https://lh3.googleusercontent.com/EdF05nhsD1f2FGsu_T5foJEl7pib6xVmCcl3dMV5MURnKiymuT9X9MgS7X_Ef-TNTPw7CbYHD_odGg=w300-h757)
    4. Y por ultimo agregar la siguiente ruta *"C:\ffmpeg\bin"* y guardamos los cambios
    ![](https://lh4.googleusercontent.com/hEbvkHETiGxCeZJrXf6i8rO3pSxDRa6PADJGK8qPFxETZc6nFEKb-rGi4ytlf8YGcFdCGPP37x227A=w300-h757)

Una vez instalado comprobaremos que se hayan creado las variables de entorno con el siguiente comando en nuestra terminal de windows:
```sh
ffmpeg -version
```
La respuesta a dicho comando deberia ser similar a la siguiente:
```sh
ffmpeg version 4.2.3 Copyright (c) 2000-2020 the FFmpeg developers
built with gcc 9.3.1 (GCC) 20200523
configuration: --enable-gpl --enable-version3 --enable-sdl2 --enable-fontconfig --enable-gnutls --enable-iconv --enable-libass --enable-libdav1d --enable-libbluray --enable-libfreetype --enable-libmp3lame --enable-libopencore-amrnb --enable-libopencore-amrwb --enable-libopenjpeg --enable-libopus --enable-libshine --enable-libsnappy --enable-libsoxr --enable-libtheora --enable-libtwolame --enable-libvpx --enable-libwavpack --enable-libwebp --enable-libx264 --enable-libx265 --enable-libxml2 --enable-libzimg --enable-lzma --enable-zlib --enable-gmp --enable-libvidstab --enable-libvorbis --enable-libvo-amrwbenc --enable-libmysofa --enable-libspeex --enable-libxvid --enable-libaom --enable-libmfx --enable-amf --enable-ffnvcodec --enable-cuvid --enable-d3d11va --enable-nvenc --enable-nvdec --enable-dxva2 --enable-avisynth --enable-libopenmpt
libavutil      56. 31.100 / 56. 31.100
libavcodec     58. 54.100 / 58. 54.100
libavformat    58. 29.100 / 58. 29.100
libavdevice    58.  8.100 / 58.  8.100
libavfilter     7. 57.100 /  7. 57.100
libswscale      5.  5.100 /  5.  5.100
libswresample   3.  5.100 /  3.  5.100
libpostproc    55.  5.100 / 55.  5.100
```
Por ultimo instalamos la libreria con el siguiente comando:
```sh
conda install -c conda-forge bar_chart_race
```

El resto es tan solo ejecutar el codigo del repositorio.