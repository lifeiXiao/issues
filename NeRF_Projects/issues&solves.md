## issue: linux download_error Imageio: 'libfreeimage-3.16.0-linux64.so'
### solve: 
find path :

```import imageio```         

```imageio.core.util.appdata_dir("imageio")```

download libfreeimage-3.16.0-linux64.so by hand and cut to the path root/.imageio/freeimage/(most common path, certain path is according to fact) 

## issue: import pyngp as ngp # noqa
ImportError: /home/tim/anaconda3/envs/ngp/bin/../lib/libstdc++.so.6: version `GLIBCXX_3.4.30' not found (required by /home/tim/nerf/instant-ngp/build/pyngp.cpython-310-x86_64-linux-gnu.so)
### solve:
``` conda install -c conda-forge libstdcxx-ng=12 ```

