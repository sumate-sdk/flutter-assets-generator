# Flutter Assets Generator

Please support me if this package is useful for you. My laptop is broken soon so your kindness is really help me a lot, Thanks.

<a href="https://www.buymeacoffee.com/flutter.gen" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee, Please." style="height: 60px !important;width: 217px !important;" ></a>

> <https://www.buymeacoffee.com/flutter.gen>

PS. if you need add any features or find problem please let me know.

<br />
<br />

## Update your pubspec.yaml file

``` yaml

flutter:
  assets:
    - assets/sound/
    - assets/images/icon/
    - assets/images/background/
    ...

```

<br />
<br />

## Command

In VSCode press `Command + Shift + P` then select option

`Flutter Assets Generator: Assets` >>> Generate code from pubspec.yaml assets.

`Flutter Assets Generator: Config file` >>> Generate generate config file `.flutgenrc` in root workplace

<br />
<br />


## Condition

- asset filename must be `[a-z]`,`[A-Z]`,`[0-9]`, `space` ,`-`,`_`
- filename can only have one `.` for file type
- filename can't be lead with `[0-9]`

<br />
<br />

## Config file

default config file for generated result

``` json

{
  "assets" : {
    "output-path": "lib",
    "filename": "assets.dart"
  }
}

```

<br />
<br />

## Example generated file

``` dart

class Assets {
  Assets._();

  static final sound = _AssetsSound._();
  static final images = _AssetsImages._();
  ...
}

...

class _AssetsSound {
  _AssetsSound._();

  final helloWorldMP3 => "assets/sound/hello world.mp3";
  final hiACC => "assets/hi.acc";
  ...
}

class _AssetsImages {
  _AssetsImages._();

  final icon = _AssetsImagesIcon._();
  final background = _AssetsImagesBackground._();
  ...
}

class _AssetsImagesIcon {
  _AssetsImagesIcon._();

  final chatIconSVG => "assets/images/icon/chatIcon.svg";
  final facebookPNG => "assets/images/icon/Facebook.png";
  final googlePlusJPG => "assets/images/icon/google-plus.jps";
  ...
}

...

```

<br />
<br />

## Known Issues

Nothing for now if you need to add function or found an errors please let me know.

<br />
<br />

## Release Notes

### 1.0.0

This is package come from old package `Flutter Generators` that I had unpublish it.
This version I add `.flutgenrc` for config output path and filename.
