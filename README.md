# lilypond-reusable-workflows

See [re-using workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows) to find out about this setup.

These workflows are mainly intended to be used by other workflows used to build and *release* the music sheets. A [complementary template repository](https://github.com/VinLudens/lilypond-workflow-template) makes use of the reusable workflows defined here.

# How to use this?

## compile-lilypond.yml

Takes the following inputs
- `LILYPOND_VERSION` indicating the lilypond version used for compiling
- `MAIN_FILE` indicating the **base name** of the file to be compiled (without the file extension)

See [Usage Example](https://github.com/VinLudens/lilypond-workflow-template/blob/main/.github/workflows/compile-lilypond.yml)

## make-release.yml

Takes the following inputs
- `MAIN_FILE` must have the same value as previously

This workflow further requires `permission.contents = write`.

See [Usage Example](https://github.com/VinLudens/lilypond-workflow-template/blob/main/.github/workflows/make-release.yml)

## release-branch.yml

Takes the following inputs
- `MAIN_FILE` must have the same value as previously
- `RELEASE_BRANCH` indicating the name of the branch in which to put *GitHub Release* assets

This workflow further requires `permission.contents = write`.

See [Usage Example](https://github.com/VinLudens/lilypond-workflow-template/blob/main/.github/workflows/release-branch.yml)
