# ReVanced 

[![CI](https://github.com/j-hc/revanced-magisk-module/actions/workflows/ci.yml/badge.svg?event=schedule)](https://github.com/j-hc/revanced-magisk-module/actions/workflows/ci.yml)

Extensive ReVanced builder  

Get the [latest CI release](https://github.com/j-hc/revanced-magisk-module/releases).

Use [**zygisk-detach**](https://github.com/j-hc/zygisk-detach) to detach YouTube and YT Music from Play Store if you are using magisk modules. 

<details><summary><big>Features</big></summary>
<ul>
 <li> Supports all present and future ReVanced apps (including projects implementing the same API)</li>
 <li> Can build Magisk modules and non-root APKs</li>
 <li> Updated daily with the latest versions of apps and patches</li>
 <li> Optimizes APKs and modules for size</li>
 <li> Modules</li>
    <ul>
     <li> recompile invalidated odex for faster usage</li>
     <li> receive updates from Magisk app</li>
     <li> do not break safetynet or trigger root detections</li>
     <li> handle installation of the correct version of the stock app and all that</li>
     <li> support Magisk and KernelSU</li>
    </ul>
</ul>
</details>

## ReVanced config
```console
"disable_resuming_shorts_player": true,
"disable_signin_to_tv_popup": true,
"gradient_loading_screen": true,
"header_logo": "premium",
"hide_ask_button": true,
"hide_ask_section": true,
"hide_autoplay_button": false,
"hide_filter_bar_feed_in_related_videos": true,
"hide_for_you_shelf": true,
"hide_how_this_was_made_section": true,
"hide_join_button": true,
"hide_player_flyout_listen_with_youtube_music": true,
"hide_player_flyout_sleep_timer": true,
"hide_player_flyout_video_quality_footer": true,
"hide_promote_button": true,
"hide_remix_button": true,
"hide_report_button": true,
"hide_share_button": true,
"open_videos_fullscreen_portrait": true,
"playback_speed_dialog_button": true,
"remove_viewer_discretion_dialog": true,
"ryd_toast_on_connection_error": false,
"shorts_disable_background_playback": true,
"shorts_quality_default_mobile": 2160,
"shorts_quality_default_wifi": 2160,
"video_quality_default_mobile": 2160,
"video_quality_default_wifi": 2160,
"video_quality_dialog_button": true,
"sb_auto_hide_skip_button_duration": "three_seconds",
"sb_interaction": "skip",
"sb_local_time_saved_milliseconds": 15079,
"sb_local_time_saved_number_segments": 2,
"sb_selfpromo": "skip",
"sb_sponsor": "skip",
"sb_toast_on_connection_error": false,
"sb_toast_on_skip": false
```

## To include/exclude patches or patch other apps

 * Star the repo :eyes:
 * Use the repo as a [template](https://github.com/new?template_name=revanced-magisk-module&template_owner=j-hc)
 * Customize [`config.toml`](./config.toml) using [rvmm-config-gen](https://j-hc.github.io/rvmm-config-gen/)
 * Run the build [workflow](../../actions/workflows/build.yml)
 * Grab your modules and APKs from [releases](../../releases)

also see here [`CONFIG.md`](./CONFIG.md)

## If you are having trouble with the classic mount method of the modules
such as,
- **"Reflash needed"** error after reboots
- **"Suspicious mount detected"** warnings from root detector apps

You can consider using [rvmm-zygisk-mount](https://github.com/j-hc/rvmm-zygisk-mount)

## Building Locally
### On Termux
```console
bash <(curl -sSf https://raw.githubusercontent.com/j-hc/revanced-magisk-module/main/build-termux.sh)
```

### On Linux
```console
$ git clone https://github.com/j-hc/revanced-magisk-module --depth 1
$ cd revanced-magisk-module
$ ./build.sh
```
