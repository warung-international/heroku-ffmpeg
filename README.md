# heroku-ffmpeg

Push: [![Test](https://github.com/warung-international/heroku-ffmpeg/workflows/Test/badge.svg?branch=master&event=push)](https://github.com/warung-international/heroku-ffmpeg/actions?query=workflow%3ATest+event%3Apush+branch%3Amaster)  

> This is a fork of the [original repository](https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest). All thanks to the past contributors.

A Heroku buildpack for ffmpeg that always downloads the latest [static build](http://johnvansickle.com/ffmpeg/).
Unlike other build packs, I never compile anything.

## Usage

Run the following from the heroku command line:

```
heroku buildpacks:add --index 1 https://github.com/warung-international/heroku-ffmpeg.git
```

You can set a custom download URL by setting the variable `FFMPEG_DOWNLOAD_URL`.

Note: This buildpack should be added before the main language buildpack (by using `--index 1`),
since the application process types are calculated from the last buildpack in the list if no
`Procfile` is specified.
