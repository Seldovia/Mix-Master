# Mix Master

Fully automated mixing and mastering. Mix Master 1.0.0 is a Windows desktop app.

This repo hosts the installer and the files the app downloads on first start. It does not contain the source code.

## What it does

- Drop one mixed track and Mix Master remasters it to match a reference track.
- Drop several stems and it mixes them to the reference, then masters the result.
- Every run matches a reference: a genre from the list, or a track of your own.

Steps behind a run:

- Single track: ITO-Master mastering, then peak normalization.
- Single track with "Mix from stems": 6-stem split with BS-RoFormer, mixing with music_mixing_style_transfer, ITO-Master mastering, peak normalization.
- Stem files: music_mixing_style_transfer, ITO-Master, peak normalization.

## Download and install

1. Open the [Mix Master 1.0.0 release](https://github.com/Seldovia/Mix-Master/releases/tag/v1.0.0).
2. Download `MixMaster_Setup.exe` (460 MB) and run it. No admin rights needed.
3. On first start the app downloads about 4.6 GB of engine and models from this repo. Keep the window open until it finishes.

SHA-256 of `MixMaster_Setup.exe`:
`F64CBAB9ADD574AA8CA870E63D83140BC93A84F116287AD4E8E94CD161753EFF`

## How to use

Drop a file or files onto the window, pick a reference, and start.

- **Mix from stems**: splits a single track into stems and remixes it.
- **Stems**: choose which stems stay in the mix.
- **Save stems**: choose which stems are saved next to the master.
- **Normalize stems**: evens out stem levels before the mix.
- **Balance guitars**: separates lead and rhythm guitar and levels them before the mix.
- **Peak level**: how loud the loudest moments of the master get.
- **Reference**: pick a genre from the list, or use your own track.

## System needs

- Windows
- NVIDIA GPU recommended. Tested on an RTX 3070 with 8 GB.
- About 4.6 GB of disk space for the downloaded engine and models, plus the 460 MB installer.

## Credits and licences

Mix Master uses these projects:

- BS-RoFormer SW, for splitting a track into six stems.
- [Music-Source-Separation-Training](https://github.com/ZFTurbo/Music-Source-Separation-Training) by ZFTurbo, the code that runs the separation models.
- music_mixing_style_transfer, for mixing stems to a reference.
- ITO-Master, for mastering to a reference.
- Mel-Band RoFormer duet model and HT-Demucs lead/rhythm guitar model, both by drypaint, for the guitar balance option.
- CREPE, for pitch tracking in the guitar balance option.

Most of the separation models are community uploads that state no licence. Mix Master is for personal use.

