# Brain Teasers — Android releases

Downloads for **Brain Teasers**, a collection of logic puzzles for Android: Panda Pairs, Sudoku,
Star Battle, Nonogram, Sun & Moon, Slitherlink, Trail, Minesweeper and Lights Out. Every puzzle is
generated on your phone and has exactly one solution, with daily puzzles, streaks, written hints that
teach you how to play, and shareable puzzle codes.

## Install

1. Open the [latest release](https://github.com/eric256/BrainTeasers-releases/releases/latest) on your
   Android phone (Android 8.0 or newer).
2. Download the `.apk` file under **Assets**.
3. Open it. If Android asks, allow your browser or files app to install unknown apps, then tap **Install**.

## Updates

The app checks this page for new versions about once a day (or tap **Check for updates** at the bottom
of the home screen). When one is available it shows what's new and can download and install it for you.
You can also choose **Later** or **Skip this version**.

## Is the download genuine?

Every release is signed with the same key. Android refuses to install an update signed with a different
key, so updates can only come from the same publisher. You can check a download yourself:

- **Checksum:** each release's notes list the APK's `SHA-256`.
- **Signing certificate (SHA-256):**
  `9A:E6:0A:88:82:DD:A8:48:11:21:FB:72:E9:77:21:95:DF:EE:7D:00:98:83:BE:44:12:74:C7:4E:A6:F6:30:BB`
  (check with `apksigner verify --print-certs BrainTeasers-x.y.z.apk`).

## Privacy

The app has no accounts, ads or analytics. Your history, streaks and gallery stay on your phone. The only
network access is checking this repository for updates and downloading them.

## Open-source software

Brain Teasers uses open-source libraries under the Apache License 2.0. The full list is in the app under
**Open-source licenses** at the bottom of the home screen.

## For maintainers: publishing a version

Add a folder `releases/vX.Y.Z/` containing the signed `BrainTeasers-X.Y.Z.apk` and `notes.md`, then push to
`main`. The **Publish releases** workflow creates the GitHub release, attaches the APK, checks (or adds)
the `SHA-256:` line the app uses to verify downloads, and marks it as the latest release. Existing releases
are never changed. The `publish_release.sh` script in the app's source repository does all of this.
