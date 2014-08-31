android_external_helper_cmupdaterincremental
============================================

Utility makefile for building incremental updates (for CMUpdater) so one doesn't have to duplicate the parameters for ota_from_targetfiles.

Usage:
```bash
brunch deviceid

# Run the following commands for each targetfiles package you want
# to build an incremental update (to the currently built rom):

export INCREMENTAL_SOURCE_BUILD_ID=f1785074ab
export INCREMENTAL_SOURCE_TARGETFILES_ZIP=path/to/cm_deviceid-target_files-$INCREMENTAL_SOURCE_BUILD_ID.zip

# (optional) export OTA_FROM_TARGET_SCRIPT_EXTRA_OPTS=(anything you want)

make ONE_SHOT_MAKEFILE=external/helper_cmupdaterincremental/build.mk cmupdaterincremental
```

