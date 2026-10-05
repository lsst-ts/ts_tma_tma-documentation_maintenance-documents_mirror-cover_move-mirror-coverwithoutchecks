# Move Mirror Cover without checks

>[!IMPORTANT]
> This procedure must be performed by authorized, trained personnel with extreme caution. Use only for specific tests and under visual supervision.

## Introduction

The four mirror covers operate only above a minimum TMA elevation of 15 degrees. Checks on TMA elevation and mirror-cover
collisions prevent the fabric from folding incorrectly below 15 degrees and avoid damage.

For some engineering tasks, operating the mirror covers below 15 degrees is necessary. This document describes the
procedure for doing so at the horizon, which requires disabling verifications in the TMA EUI Mirror cover settings.
It must always be done in situ, manually, and with extreme caution.

The verification settings are:

`MinElevationPosition` : minimum value of elevation allowed for moving the mirror cover, common for all mirror covers.

`DisableCollisionCheck`:  boolean that checks for each mirror cover the rest of the mirror cover positions. Each mirror cover has an instance, accessed using the top right control that says instance.  It should always be FALSE during regular operations.

## Precondition

- An engineering/maintenance task requires to operate the mirror covers when TMA elevation is below 15 degrees.
- Be authorized to perform this procedure.

## Procedure

> [!IMPORTANT]
> Retracting the mirror covers at horizon:
>
>
> To provide access from the Deployable Platforms there is no need to fully retract them (130 degrees), instead retract to ~ 40 degrees for each mirror cover.

1. Go to Home > Monitor & Control > Mirror Cover System > [Mirror Cover General View](https://ts-tma.lsst.io/docs/tma_eui-manual-english/02_Monitor&Control/021_MirrorCoverGeneralView.html#mirror-cover-general-view-screen-main-view ).
2. Power OFF ALL the mirror covers.
3. Got to Home > Settings > [Mirror cover settings](https://ts-tma.lsst.io/docs/tma_eui-manual-english/03_Settings/010_MirrorCoverSettings.html)
4. Change the settings by writing **DO NOT SAVE THEM**:
    1. Select `MinElevationPosition`  set to `0` and  WRITE.
    2. Disable the collision check for each of the 4 instances (refer to the image in the [Mirror Cover Setting window](https://ts-tma.lsst.io/docs/tma_eui-manual-english/03_Settings/010_MirrorCoverSettings.html) instances: MC1, MC2, MC3, MC4)
         1. Set DisableCollisionCheck to `TRUE`
         2. Select one instance
         3. Press WRITE
         4. Repeat steps ii and iii for each instance, this means 4 times total
5. Go to Home > Monitor & Control > Mirror Cover System > [Mirror Cover General View](https://ts-tma.lsst.io/docs/tma_eui-manual-english/02_Monitor&Control/021_MirrorCoverGeneralView.html#mirror-cover-general-view-screen-main-view ).
6. Following the order for retract or extend listed below, **FOR EACH** mirror cover:
     1. Power ON the mirror cover you want to operate
     2. Set position in degrees
     3. Set maximum speed of 0.5 deg/s
     4. Press <code>MOVE</code>
     5. Repeat all the sub-steps in step 6 for the other mirror covers in the appropriate order.

### Retract order  

When retracting the mirror covers manually at horizon, the order is:

1. Mirror cover X-
2. Mirror cover Y+
3. Mirror cover Y-
4. Mirror cover X+

### Extend order

When extending the mirror covers manually at horizon, the order is:

1. Mirror cover X+
2. Mirror cover Y-
3. Mirror cover Y+
4. Mirror cover X-
