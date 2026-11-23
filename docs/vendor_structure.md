# Vendor Structure: A505f-vendor.img

File tree of the vendor image used in this project (A505FDDS9CUK1, Android 11 base, SDK 30).
It was mounted and listed. No files are included, only names.

```
├── bin
│   ├── acpi
│   ├── applypatch
│   ├── awk
│   ├── base64
│   ├── basename
│   ├── blockdev
│   ├── boringssl_self_test32
│   ├── boringssl_self_test64
│   ├── cal
│   ├── cat
│   ├── cbd
│   ├── chattr
│   ├── chcon
│   ├── chgrp
│   ├── chmod
│   ├── chown
│   ├── chroot
│   ├── chrt
│   ├── cksum
│   ├── clear
│   ├── cmp
│   ├── comm
│   ├── cp
│   ├── cpio
│   ├── cut
│   ├── date
│   ├── dd
│   ├── devmem
│   ├── df
│   ├── diff
│   ├── dirname
│   ├── dmesg
│   ├── dos2unix
│   ├── du
│   ├── dumpsys
│   ├── echo
│   ├── egrep
│   ├── env
│   ├── expand
│   ├── expr
│   ├── fallocate
│   ├── false
│   ├── fgrep
│   ├── file
│   ├── find
│   ├── flock
│   ├── fmt
│   ├── free
│   ├── fsync
│   ├── getconf
│   ├── getenforce
│   ├── getevent
│   ├── getprop
│   ├── grep
│   ├── groups
│   ├── gunzip
│   ├── gzip
│   ├── head
│   ├── hostname
│   ├── hw
│   │   ├── android.hardware.audio.service
│   │   ├── android.hardware.bluetooth@1.0-service
│   │   ├── android.hardware.camera.provider@2.5-service_64
│   │   ├── android.hardware.cas@1.2-service
│   │   ├── android.hardware.configstore@1.1-service
│   │   ├── android.hardware.drm@1.3-service.clearkey
│   │   ├── android.hardware.drm@1.3-service.widevine
│   │   ├── android.hardware.gatekeeper@1.0-service
│   │   ├── android.hardware.graphics.allocator@2.0-service
│   │   ├── android.hardware.graphics.composer@2.2-service
│   │   ├── android.hardware.health@2.1-service
│   │   ├── android.hardware.keymaster@4.0-service.samsung
│   │   ├── android.hardware.light@2.0-service.samsung
│   │   ├── android.hardware.media.omx@1.0-service
│   │   ├── android.hardware.memtrack@1.0-service
│   │   ├── android.hardware.power-service.samsung-libperfmgr
│   │   ├── android.hardware.sensors@2.1-service.samsung-multihal
│   │   ├── android.hardware.thermal@2.0-service.samsung
│   │   ├── android.hardware.usb@1.1-service.typec
│   │   ├── android.hardware.vibrator@1.3-service.samsung
│   │   ├── android.hardware.wifi@1.0-service
│   │   ├── gps.sh
│   │   ├── gpsd
│   │   ├── hostapd
│   │   ├── macloader
│   │   ├── rild
│   │   ├── vendor.lineage.biometrics.fingerprint.inscreen@1.0-service.a50
│   │   ├── vendor.lineage.fastcharge@1.0-service.samsung
│   │   ├── vendor.lineage.livedisplay@2.0-service.samsung-exynos
│   │   ├── vendor.lineage.touch@1.0-service.samsung
│   │   ├── vendor.lineage.trust@1.0-service
│   │   ├── vendor.samsung.hardware.biometrics.fingerprint@2.1-service.a50
│   │   ├── vendor.samsung.hardware.gnss@2.0-service
│   │   ├── wpa_supplicant
│   ├── hwclock
│   ├── i2cdetect
│   ├── i2cdump
│   ├── i2cget
│   ├── i2cset
│   ├── iconv
│   ├── id
│   ├── ifconfig
│   ├── inotifyd
│   ├── insmod
│   ├── install
│   ├── install-recovery.sh
│   ├── ionice
│   ├── iorenice
│   ├── kill
│   ├── killall
│   ├── ln
│   ├── load_policy
│   ├── log
│   ├── logname
│   ├── logwrapper
│   ├── losetup
│   ├── ls
│   ├── lsattr
│   ├── lsmod
│   ├── lsof
│   ├── lspci
│   ├── lsusb
│   ├── md5sum
│   ├── microcom
│   ├── mkdir
│   ├── mkfifo
│   ├── mknod
│   ├── mkswap
│   ├── mktemp
│   ├── modinfo
│   ├── modprobe
│   ├── more
│   ├── mount
│   ├── mountpoint
│   ├── mv
│   ├── nc
│   ├── netcat
│   ├── netstat
│   ├── nice
│   ├── nl
│   ├── nohup
│   ├── nproc
│   ├── nsenter
│   ├── od
│   ├── paste
│   ├── patch
│   ├── pgrep
│   ├── pidof
│   ├── pkill
│   ├── pmap
│   ├── printenv
│   ├── printf
│   ├── ps
│   ├── pwd
│   ├── readelf
│   ├── readlink
│   ├── realpath
│   ├── renice
│   ├── restorecon
│   ├── rm
│   ├── rmdir
│   ├── rmmod
│   ├── runcon
│   ├── secril_config_svc
│   ├── sed
│   ├── sendevent
│   ├── seq
│   ├── setenforce
│   ├── setprop
│   ├── setsid
│   ├── sh
│   ├── sha1sum
│   ├── sha224sum
│   ├── sha256sum
│   ├── sha384sum
│   ├── sha512sum
│   ├── sleep
│   ├── sort
│   ├── split
│   ├── start
│   ├── start-ssh
│   ├── stat
│   ├── stop
│   ├── strings
│   ├── stty
│   ├── swapoff
│   ├── swapon
│   ├── sync
│   ├── sysctl
│   ├── tac
│   ├── tail
│   ├── tar
│   ├── taskset
│   ├── tee
│   ├── test
│   ├── time
│   ├── timeout
│   ├── toolbox
│   ├── top
│   ├── touch
│   ├── toybox_vendor
│   ├── tr
│   ├── true
│   ├── truncate
│   ├── tty
│   ├── tzdaemon
│   ├── tzts_daemon
│   ├── ulimit
│   ├── umount
│   ├── uname
│   ├── uniq
│   ├── unix2dos
│   ├── unlink
│   ├── unshare
│   ├── uptime
│   ├── usleep
│   ├── uudecode
│   ├── uuencode
│   ├── uuidgen
│   ├── vmstat
│   ├── vndservice
│   ├── vndservicemanager
│   ├── watch
│   ├── wc
│   ├── which
│   ├── whoami
│   ├── wlbtd
│   ├── xargs
│   ├── xxd
│   ├── yes
│   ├── zcat
├── build.prop
├── default.prop
├── etc
│   ├── NOTICE.xml.gz
│   ├── a2dp_in_audio_policy_configuration.xml
│   ├── audio_effects.xml
│   ├── audio_policy_configuration.xml
│   ├── audio_policy_engine_configuration.xml
│   ├── audio_policy_engine_default_stream_volumes.xml
│   ├── audio_policy_engine_product_strategies.xml
│   ├── audio_policy_engine_stream_volumes.xml
│   ├── audio_policy_volumes.xml
│   ├── bluetooth
│   │   ├── bt_did.conf
│   │   ├── bt_vendor.conf
│   ├── bluetooth_audio_policy_configuration.xml
│   ├── default_volume_tables.xml
│   ├── dolby
│   │   ├── dax-default.xml
│   ├── floating_feature.xml
│   ├── fs_config_dirs
│   ├── fs_config_files
│   ├── fstab.exynos9610
│   ├── gnss
│   │   ├── gps.cfg
│   ├── group
│   ├── init
│   │   ├── android.hardware.audio.service.rc
│   │   ├── android.hardware.bluetooth@1.0-service.rc
│   │   ├── android.hardware.camera.provider@2.5-service_64.rc
│   │   ├── android.hardware.cas@1.2-service.rc
│   │   ├── android.hardware.configstore@1.1-service.rc
│   │   ├── android.hardware.drm@1.3-service.clearkey.rc
│   │   ├── android.hardware.drm@1.3-service.widevine.rc
│   │   ├── android.hardware.gatekeeper@1.0-service.rc
│   │   ├── android.hardware.graphics.allocator@2.0-service.rc
│   │   ├── android.hardware.graphics.composer@2.2-service.rc
│   │   ├── android.hardware.health@2.1-service.rc
│   │   ├── android.hardware.keymaster@4.0-service.samsung.rc
│   │   ├── android.hardware.light@2.0-service.samsung.rc
│   │   ├── android.hardware.media.omx@1.0-service.rc
│   │   ├── android.hardware.memtrack@1.0-service.rc
│   │   ├── android.hardware.power-service.samsung-libperfmgr.rc
│   │   ├── android.hardware.sensors@2.1-service.samsung-multihal.rc
│   │   ├── android.hardware.thermal@2.0-service.samsung.rc
│   │   ├── android.hardware.usb@1.1-service.typec.rc
│   │   ├── android.hardware.vibrator@1.3-service.samsung.rc
│   │   ├── android.hardware.wifi.supplicant-service.rc
│   │   ├── android.hardware.wifi@1.0-service.rc
│   │   ├── boringssl_self_test.rc
│   │   ├── hostapd.android.rc
│   │   ├── init.baseband.rc
│   │   ├── init.exynos9610.rc
│   │   ├── init.exynos9610.usb.rc
│   │   ├── init.gps.rc
│   │   ├── init.samsung.rc
│   │   ├── init.vendor.rilchip.rc
│   │   ├── init.vendor.rilcommon.rc
│   │   ├── teegris_v3.rc
│   │   ├── vendor.lineage.biometrics.fingerprint.inscreen@1.0-service.a50.rc
│   │   ├── vendor.lineage.fastcharge@1.0-service.samsung.rc
│   │   ├── vendor.lineage.livedisplay@2.0-service.samsung-exynos.rc
│   │   ├── vendor.lineage.touch@1.0-service.samsung.rc
│   │   ├── vendor.lineage.trust@1.0-service.rc
│   │   ├── vendor.samsung.hardware.biometrics.fingerprint@2.1-service.a50.rc
│   │   ├── vendor.samsung.hardware.gnss@2.0-service.rc
│   │   ├── vendor_flash_recovery.rc
│   │   ├── vndservicemanager.rc
│   │   ├── wifi.rc
│   │   ├── wifi_slsi.rc
│   ├── media_codecs.xml
│   ├── media_codecs_google_audio.xml
│   ├── media_codecs_google_telephony.xml
│   ├── media_codecs_google_video.xml
│   ├── media_codecs_performance.xml
│   ├── media_profiles_V1_0.xml
│   ├── mixer_gains.xml
│   ├── mixer_paths.xml
│   ├── mkshrc
│   ├── passwd
│   ├── permissions
│   │   ├── android.hardware.audio.low_latency.xml
│   │   ├── android.hardware.audio.pro.xml
│   │   ├── android.hardware.bluetooth.xml
│   │   ├── android.hardware.bluetooth_le.xml
│   │   ├── android.hardware.camera.ar.xml
│   │   ├── android.hardware.camera.autofocus.xml
│   │   ├── android.hardware.camera.flash-autofocus.xml
│   │   ├── android.hardware.camera.front.xml
│   │   ├── android.hardware.camera.full.xml
│   │   ├── android.hardware.camera.raw.xml
│   │   ├── android.hardware.camera.xml
│   │   ├── android.hardware.fingerprint.xml
│   │   ├── android.hardware.location.gps.xml
│   │   ├── android.hardware.opengles.aep.xml
│   │   ├── android.hardware.sensor.accelerometer.xml
│   │   ├── android.hardware.sensor.compass.xml
│   │   ├── android.hardware.sensor.gyroscope.xml
│   │   ├── android.hardware.sensor.light.xml
│   │   ├── android.hardware.sensor.stepcounter.xml
│   │   ├── android.hardware.sensor.stepdetector.xml
│   │   ├── android.hardware.telephony.gsm.xml
│   │   ├── android.hardware.telephony.ims.xml
│   │   ├── android.hardware.touchscreen.multitouch.jazzhand.xml
│   │   ├── android.hardware.usb.accessory.xml
│   │   ├── android.hardware.usb.host.xml
│   │   ├── android.hardware.vulkan.compute.xml
│   │   ├── android.hardware.vulkan.level.xml
│   │   ├── android.hardware.vulkan.version.xml
│   │   ├── android.hardware.wifi.direct.xml
│   │   ├── android.hardware.wifi.passpoint.xml
│   │   ├── android.hardware.wifi.xml
│   │   ├── android.software.app_widgets.xml
│   │   ├── android.software.device_id_attestation.xml
│   │   ├── android.software.freeform_window_management.xml
│   │   ├── android.software.midi.xml
│   │   ├── android.software.picture_in_picture.xml
│   │   ├── android.software.sip.voip.xml
│   │   ├── android.software.vulkan.deqp.level.xml
│   │   ├── handheld_core_hardware.xml
│   │   ├── vendor.lineage.biometrics.fingerprint.inscreen.xml
│   ├── plmn_delta.bin
│   ├── plmn_delta_attaio.bin
│   ├── plmn_delta_hktw.bin
│   ├── plmn_delta_usagsm.bin
│   ├── plmn_se13.bin
│   ├── powerhint.json
│   ├── public.libraries.txt
│   ├── r_submix_audio_policy_configuration.xml
│   ├── seccomp_policy
│   │   ├── configstore@1.1.policy
│   ├── selinux
│   │   ├── plat_pub_versioned.cil
│   │   ├── plat_sepolicy_vers.txt
│   │   ├── precompiled_sepolicy
│   │   ├── precompiled_sepolicy.plat_sepolicy_and_mapping.sha256
│   │   ├── precompiled_sepolicy.product_sepolicy_and_mapping.sha256
│   │   ├── precompiled_sepolicy.system_ext_sepolicy_and_mapping.sha256
│   │   ├── selinux_denial_metadata
│   │   ├── vendor_file_contexts
│   │   ├── vendor_hwservice_contexts
│   │   ├── vendor_mac_permissions.xml
│   │   ├── vendor_property_contexts
│   │   ├── vendor_seapp_contexts
│   │   ├── vendor_sepolicy.cil
│   │   ├── vendor_service_contexts
│   │   ├── vndservice_contexts
│   ├── sensors
│   │   ├── hals.conf
│   ├── sysconfig
│   │   ├── component-overrides.xml
│   ├── thermal_info_config.json
│   ├── usb_audio_policy_configuration.xml
│   ├── vintf
│   │   ├── compatibility_matrix.xml
│   │   ├── manifest
│   │   ├── manifest.xml
│   ├── wifi
│   │   ├── hydra_config.sdb
│   │   ├── indoorchannel.info
│   │   ├── mx140.bin
│   │   ├── mx140_bt.hcf
│   │   ├── mx140_t.bin
│   │   ├── mx140_t_wlan.hcf
│   │   ├── mx140_t_wlan_sw.hcf
│   │   ├── mx140_t_wlan_t.hcf
│   │   ├── mx140_t_wlan_t_sw.hcf
│   │   ├── mx140_wlan.hcf
│   │   ├── mx140_wlan_sw.hcf
│   │   ├── mx140_wlan_t.hcf
│   │   ├── mx140_wlan_t_sw.hcf
│   │   ├── p2p_supplicant_overlay.conf
│   │   ├── platform.txt
│   │   ├── slsi_reg_database.bin
│   │   ├── wpa_supplicant.conf
│   │   ├── wpa_supplicant_overlay.conf
├── firmware
│   ├── APBargeIn_AUDIO_SLSI.bin
│   ├── APBiBF_AUDIO_SLSI.bin
│   ├── AP_AUDIO_SLSI.bin
│   ├── CC_DRAM_CODE_FLASH.bin
│   ├── CC_DTCM_CODE_FLASH.bin
│   ├── CC_ITCM_CODE_FLASH.bin
│   ├── SoundBoosterParam.bin
│   ├── Tfa9872.cnt
│   ├── WithLightFixNoBN.SDNNmodel
│   ├── calliope_dram.bin
│   ├── calliope_iva.bin
│   ├── calliope_sram.bin
│   ├── dax_param.bin
│   ├── default_configuration.hfd.cfg.json
│   ├── fimc_is_lib.bin
│   ├── fimc_is_rta.bin
│   ├── kernel_bin_enf.bin
│   ├── kernel_bin_inception.bin
│   ├── kernel_bin_mfb.bin
│   ├── kernel_bin_mobile_vgg.bin
│   ├── kernel_bin_nfd.bin
│   ├── mfc_fw.bin
│   ├── pp_cfg.json
│   ├── setfile_2x5.bin
│   ├── setfile_4ha.bin
│   ├── setfile_gc5035.bin
│   ├── setfile_imx576.bin
│   ├── tfadsp.bin
│   ├── tracker_cfg.json
├── lib
│   ├── android.hardware.audio.common-util.so
│   ├── android.hardware.audio.common@6.0-util.so
│   ├── egl
│   │   ├── libGLES_mali.so
│   ├── hw
│   │   ├── android.hardware.audio.effect@6.0-impl.so
│   │   ├── android.hardware.audio@6.0-impl.so
│   │   ├── android.hardware.bluetooth.audio@2.0-impl.so
│   │   ├── android.hardware.graphics.mapper@2.0-impl.so
│   │   ├── android.hardware.renderscript@1.0-impl.so
│   │   ├── android.hardware.soundtrigger@2.0-impl.so
│   │   ├── audio.bluetooth.default.so
│   │   ├── audio.primary.default.so
│   │   ├── audio.primary.exynos9610.so
│   │   ├── audio.r_submix.default.so
│   │   ├── audio.usb.default.so
│   │   ├── camera.exynos9610.so
│   │   ├── gatekeeper.exynos9610.so
│   │   ├── gralloc.default.so
│   │   ├── gralloc.exynos9610.so
│   │   ├── hwcomposer.exynos9610.so
│   │   ├── local_time.default.so
│   │   ├── memtrack.exynos9610.so
│   │   ├── power.default.so
│   │   ├── sensors.sensorhub.so
│   │   ├── vibrator.default.so
│   │   ├── vulkan.universal9610.so
│   ├── libExynosHWCService.so
│   ├── libExynosOMX_Core.so
│   ├── libExynosOMX_Resourcemanager.so
│   ├── libGLES_mali.so
│   ├── libGrallocWrapper.so
│   ├── libOpenCL.so
│   ├── libOpenCL.so.1
│   ├── libOpenCL.so.1.1
│   ├── libSEF.quram.so
│   ├── libSamsungPostProcessConvertor.so
│   ├── lib_SamsungRec_07001.so
│   ├── lib_SoundAlive_SRC384_ver320.so
│   ├── lib_soundaliveresampler.so
│   ├── libaboxpcmdump.so
│   ├── libacryl.so
│   ├── libacryl_plugin_slsi_hdr10.so
│   ├── libalsautils.so
│   ├── libalsautils_sec.so
│   ├── libaudio-ril.so
│   ├── libaudio_soundtrigger.so
│   ├── libaudioproxy.so
│   ├── libavservices_minijail.so
│   ├── libbauthserver.so
│   ├── libbauthtzcommon.so
│   ├── libbluetooth_audio_session.so
│   ├── libcsc.so
│   ├── libdatamod.so
│   ├── libeffects.so
│   ├── libeffectsconfig.so
│   ├── libegis_fp_normal_sensor_test.so
│   ├── libepicoperator.so
│   ├── libexynoscamera3.so
│   ├── libexynosdisplay.so
│   ├── libexynosgraphicbuffer.so
│   ├── libexynosgscaler.so
│   ├── libexynosscaler.so
│   ├── libexynosutils.so
│   ├── libexynosv4l2.so
│   ├── libfloatingfeature.so
│   ├── libgf_in_system_lib.so
│   ├── libgiantmscl.so
│   ├── libhidltransport.so
│   ├── libhwbinder.so
│   ├── libhwjpeg.so
│   ├── libion_exynos.so
│   ├── libmdf.so
│   ├── libnbaio_mono.so
│   ├── liboemcrypto.so
│   ├── libopus.so
│   ├── libprofileparamstorage.so
│   ├── libprotobuf-cpp-full-3.9.1.so
│   ├── libprotobuf-cpp-lite-3.9.1.so
│   ├── libqfp_sensortest.so
│   ├── librecordalive.so
│   ├── libreference-ril.so
│   ├── libril-samsung.so
│   ├── libril.so
│   ├── librilutils.so
│   ├── libsamsungDiamondVoice.so
│   ├── libsecaudiocoreutils.so
│   ├── libsecaudioinfo.so
│   ├── libsecnativefeature.so
│   ├── libsecril-client.so
│   ├── libsecure_storage.so
│   ├── libsemnativecarrierfeature.so
│   ├── libsensorlistener.so
│   ├── libsensorndkbridge.so
│   ├── libshim_sensorndkbridge.so
│   ├── libstagefright_amrnb_common.so
│   ├── libstagefright_enc_common.so
│   ├── libstagefright_flacdec.so
│   ├── libstagefright_soft_aacdec.so
│   ├── libstagefright_soft_aacenc.so
│   ├── libstagefright_soft_amrdec.so
│   ├── libstagefright_soft_amrnbenc.so
│   ├── libstagefright_soft_amrwbenc.so
│   ├── libstagefright_soft_avcdec.so
│   ├── libstagefright_soft_avcenc.so
│   ├── libstagefright_soft_flacdec.so
│   ├── libstagefright_soft_flacenc.so
│   ├── libstagefright_soft_g711dec.so
│   ├── libstagefright_soft_gsmdec.so
│   ├── libstagefright_soft_hevcdec.so
│   ├── libstagefright_soft_mp3dec.so
│   ├── libstagefright_soft_mpeg2dec.so
│   ├── libstagefright_soft_mpeg4dec.so
│   ├── libstagefright_soft_mpeg4enc.so
│   ├── libstagefright_soft_opusdec.so
│   ├── libstagefright_soft_rawdec.so
│   ├── libstagefright_soft_vorbisdec.so
│   ├── libstagefright_soft_vpxdec.so
│   ├── libstagefright_soft_vpxenc.so
│   ├── libstagefright_softomx.so
│   ├── libstagefright_softomx_plugin.so
│   ├── libstagefrighthw.so
│   ├── libsynaFpSensorTestNwd.so
│   ├── libteecl.so
│   ├── libtinycompress.so
│   ├── libuniapi.so
│   ├── libuniplugin.so
│   ├── libuuid.so
│   ├── libvorbisidec.so
│   ├── libvpx.so
│   ├── libwebrtc_audio_preprocessing.so
│   ├── libwvhidl.so
│   ├── mediacas
│   │   ├── libclearkeycasplugin.so
│   ├── mediadrm
│   │   ├── libdrmclearkeyplugin.so
│   ├── omx
│   │   ├── libOMX.Exynos.AVC.Decoder.so
│   │   ├── libOMX.Exynos.AVC.Encoder.so
│   │   ├── libOMX.Exynos.HEVC.Decoder.so
│   │   ├── libOMX.Exynos.HEVC.Encoder.so
│   │   ├── libOMX.Exynos.MPEG4.Decoder.so
│   │   ├── libOMX.Exynos.MPEG4.Encoder.so
│   │   ├── libOMX.Exynos.VP8.Decoder.so
│   │   ├── libOMX.Exynos.VP8.Encoder.so
│   │   ├── libOMX.Exynos.VP9.Decoder.so
│   │   ├── libOMX.Exynos.VP9.Encoder.so
│   │   ├── libOMX.Exynos.WMV.Decoder.so
│   ├── sensors.grip.so
│   ├── soundfx
│   │   ├── libaudioeffectoffload.so
│   │   ├── libaudiopreprocessing.so
│   │   ├── libbundlewrapper.so
│   │   ├── libdownmix.so
│   │   ├── libdynproc.so
│   │   ├── libeffectproxy.so
│   │   ├── libldnhncr.so
│   │   ├── libreverbwrapper.so
│   │   ├── libswdap.so
│   │   ├── libvisualizer.so
│   ├── vendor.samsung.hardware.radio.bridge@2.0.so
│   ├── vendor.samsung.hardware.radio@2.0.so
│   ├── vendor.samsung.hardware.radio@2.1.so
│   ├── vndk
│   │   ├── libaudioroute.so
│   │   ├── libtinyalsa.so
├── lib64
│   ├── android.hardware.camera.provider@2.4-legacy.so
│   ├── android.hardware.camera.provider@2.5-legacy.so
│   ├── android.hardware.graphics.composer@2.1-resources.so
│   ├── android.hardware.graphics.composer@2.2-resources.so
│   ├── android.hardware.sensors@2.0-ScopedWakelock.so
│   ├── camera.device@1.0-impl.so
│   ├── camera.device@3.2-impl.so
│   ├── camera.device@3.3-impl.so
│   ├── camera.device@3.4-impl.so
│   ├── camera.device@3.5-impl.so
│   ├── egl
│   │   ├── libGLES_mali.so
│   ├── hw
│   │   ├── android.hardware.bluetooth@1.0-impl.so
│   │   ├── android.hardware.gatekeeper@1.0-impl.so
│   │   ├── android.hardware.gnss@2.1-impl.so
│   │   ├── android.hardware.graphics.allocator@2.0-impl.so
│   │   ├── android.hardware.graphics.mapper@2.0-impl.so
│   │   ├── android.hardware.health@2.0-impl-2.1.so
│   │   ├── android.hardware.memtrack@1.0-impl.so
│   │   ├── android.hardware.renderscript@1.0-impl.so
│   │   ├── audio.bluetooth.default.so
│   │   ├── audio.primary.default.so
│   │   ├── audio.r_submix.default.so
│   │   ├── audio.usb.default.so
│   │   ├── camera.exynos9610.so
│   │   ├── gatekeeper.exynos9610.so
│   │   ├── gralloc.default.so
│   │   ├── gralloc.exynos9610.so
│   │   ├── hwcomposer.exynos9610.so
│   │   ├── local_time.default.so
│   │   ├── memtrack.exynos9610.so
│   │   ├── power.default.so
│   │   ├── sensors.sensorhub.so
│   │   ├── vendor.samsung.hardware.gnss@2.0-impl.so
│   │   ├── vibrator.default.so
│   │   ├── vulkan.universal9610.so
│   ├── libExynosHWCService.so
│   ├── libExynosOMX_Core.so
│   ├── libExynosOMX_Resourcemanager.so
│   ├── libGLES_mali.so
│   ├── libGrallocWrapper.so
│   ├── libOpenCL.so
│   ├── libOpenCL.so.1
│   ├── libOpenCL.so.1.1
│   ├── libSEF.quram.so
│   ├── libacryl.so
│   ├── libacryl_plugin_slsi_hdr10.so
│   ├── libalsautils.so
│   ├── libbauthserver.so
│   ├── libbauthtzcommon.so
│   ├── libbluetooth_audio_session.so
│   ├── libbt-vendor.so
│   ├── libcsc.so
│   ├── libeffects.so
│   ├── libeffectsconfig.so
│   ├── libegis_fp_normal_sensor_test.so
│   ├── libengmode_client.so
│   ├── libepicoperator.so
│   ├── libexynoscamera3.so
│   ├── libexynosdisplay.so
│   ├── libexynosgraphicbuffer.so
│   ├── libexynosgscaler.so
│   ├── libexynosscaler.so
│   ├── libexynosutils.so
│   ├── libexynosv4l2.so
│   ├── libfloatingfeature.so
│   ├── libgf_in_system_lib.so
│   ├── libgiantmscl.so
│   ├── libhidltransport.so
│   ├── libhwbinder.so
│   ├── libhwc2on1adapter.so
│   ├── libhwc2onfbadapter.so
│   ├── libhwjpeg.so
│   ├── libhwminijail.so
│   ├── libion_exynos.so
│   ├── libiwt.so
│   ├── libkeymaster4.so
│   ├── libkeymaster4_1support.so
│   ├── libkeymaster4support.so
│   ├── libkeymaster_helper.so
│   ├── libkeymaster_messages.so
│   ├── libkeymaster_portable.so
│   ├── libkeystore-engine-wifi-hidl.so
│   ├── libkeystore-wifi-hidl.so
│   ├── libmdf.so
│   ├── libnbaio_mono.so
│   ├── libperfmgr.so
│   ├── libprotobuf-cpp-full-3.9.1.so
│   ├── libprotobuf-cpp-lite-3.9.1.so
│   ├── libpuresoftkeymasterdevice.so
│   ├── libqfp_sensortest.so
│   ├── libreference-ril.so
│   ├── libril-samsung.so
│   ├── libril.so
│   ├── librilutils.so
│   ├── libsec-ril-dsds.so
│   ├── libsec-ril.so
│   ├── libsecaudioinfo.so
│   ├── libsecnativefeature.so
│   ├── libsecril-client.so
│   ├── libsecure_storage.so
│   ├── libsemnativecarrierfeature.so
│   ├── libsensorlistener.so
│   ├── libsensorndkbridge.so
│   ├── libshim_sensorndkbridge.so
│   ├── libskeymaster4device.so
│   ├── libsoft_attestation_cert.so
│   ├── libstagefrighthw.so
│   ├── libsynaFpSensorTestNwd.so
│   ├── libteecl.so
│   ├── libtinycompress.so
│   ├── libuniapi.so
│   ├── libuniplugin.so
│   ├── libuuid.so
│   ├── libvkmanager_vendor.so
│   ├── libwebrtc_audio_preprocessing.so
│   ├── libwifi-hal.so
│   ├── libwrappergps.so
│   ├── mediacas
│   │   ├── libclearkeycasplugin.so
│   ├── mediadrm
│   │   ├── libdrmclearkeyplugin.so
│   ├── omx
│   │   ├── libOMX.Exynos.AVC.Decoder.so
│   │   ├── libOMX.Exynos.AVC.Encoder.so
│   │   ├── libOMX.Exynos.HEVC.Decoder.so
│   │   ├── libOMX.Exynos.HEVC.Encoder.so
│   │   ├── libOMX.Exynos.MPEG4.Decoder.so
│   │   ├── libOMX.Exynos.MPEG4.Encoder.so
│   │   ├── libOMX.Exynos.VP8.Decoder.so
│   │   ├── libOMX.Exynos.VP8.Encoder.so
│   │   ├── libOMX.Exynos.VP9.Decoder.so
│   │   ├── libOMX.Exynos.VP9.Encoder.so
│   │   ├── libOMX.Exynos.WMV.Decoder.so
│   ├── pixel-power-ext-V1-ndk_platform.so
│   ├── sensors.grip.so
│   ├── sensors.inputvirtual.so
│   ├── soundfx
│   │   ├── libaudioeffectoffload.so
│   │   ├── libaudiopreprocessing.so
│   │   ├── libbundlewrapper.so
│   │   ├── libdownmix.so
│   │   ├── libdynproc.so
│   │   ├── libeffectproxy.so
│   │   ├── libldnhncr.so
│   │   ├── libreverbwrapper.so
│   │   ├── libvisualizer.so
│   ├── vendor.lineage.biometrics.fingerprint.inscreen@1.0.so
│   ├── vendor.lineage.fastcharge@1.0.so
│   ├── vendor.lineage.livedisplay@2.0.so
│   ├── vendor.lineage.power-V1-ndk_platform.so
│   ├── vendor.lineage.touch@1.0.so
│   ├── vendor.lineage.trust@1.0.so
│   ├── vendor.samsung.hardware.biometrics.fingerprint@2.1.so
│   ├── vendor.samsung.hardware.gnss@2.0.so
│   ├── vendor.samsung.hardware.radio.bridge@2.0.so
│   ├── vendor.samsung.hardware.radio.channel@2.0.so
│   ├── vendor.samsung.hardware.radio@2.0.so
│   ├── vendor.samsung.hardware.radio@2.1.so
├── lost+found
├── odm
│   ├── etc
│   │   ├── NOTICE.xml.gz
│   │   ├── build.prop
│   │   ├── group
│   │   ├── passwd
├── overlay
│   ├── CarrierConfig__auto_generated_rro_vendor.apk
│   ├── EmergencyInfo__auto_generated_rro_vendor.apk
│   ├── LineageParts__auto_generated_rro_vendor.apk
│   ├── LineageSetupWizard__auto_generated_rro_vendor.apk
│   ├── Seedvault__auto_generated_rro_vendor.apk
│   ├── SettingsProvider__auto_generated_rro_vendor.apk
│   ├── Settings__auto_generated_rro_vendor.apk
│   ├── SystemUI__auto_generated_rro_vendor.apk
│   ├── TeleService__auto_generated_rro_vendor.apk
│   ├── Telecom__auto_generated_rro_vendor.apk
│   ├── Traceur__auto_generated_rro_vendor.apk
│   ├── WifiOverlay
│   │   ├── WifiOverlay.apk
│   ├── framework-res__auto_generated_rro_vendor.apk
│   ├── org.lineageos.platform-res__auto_generated_rro_vendor.apk
├── recovery-from-boot.p
├── tee
│   ├── 00000000-0000-0000-0000-00000000dead
│   ├── 00000000-0000-0000-0000-000000010081
│   ├── 00000000-0000-0000-0000-000000020081
│   ├── 00000000-0000-0000-0000-000000534b4d
│   ├── 00000000-0000-0000-0000-000046495645
│   ├── 00000000-0000-0000-0000-0050524f4341
│   ├── 00000000-0000-0000-0000-00535453540c
│   ├── 00000000-0000-0000-0000-0053545354ab
│   ├── 00000000-0000-0000-0000-00575644524d
│   ├── 00000000-0000-0000-0000-446e6c6f6164
│   ├── 00000000-0000-0000-0000-46494e474502
│   ├── 00000000-0000-0000-0000-46494e474552
│   ├── 00000000-0000-0000-0000-474154454b45
│   ├── 00000000-0000-0000-0000-4b45594d5354
│   ├── 00000000-0000-0000-0000-505256544545
│   ├── 00000000-0000-0000-0000-535355504341
│   ├── 00000000-0000-0000-0000-564c544b5052
│   ├── 00000000-0000-0000-0000-656e676d6f64
│   ├── 00000000-0000-0000-0000-657365636f6d
│   ├── 00000000-0000-0000-0000-6d73745f5441
│   ├── 00000000-5452-5553-544f-525355414c50
│   ├── driver
│   │   ├── 00000000-0000-0000-0000-00535453540b
│   │   ├── 00000000-0000-0000-0000-4d53546d7374
│   │   ├── 00000000-0000-0000-0000-545241545453
│   │   ├── 00000000-0000-0000-0000-564c544b4456
│   ├── ffffffff-0000-0000-0000-000000000030
│   ├── tui
│   │   ├── resolution_common
├── ueventd.rc
├── usr
│   ├── keylayout
│   │   ├── sec_touchscreen.kl
─────────────────────────────────────────
✅ Pemetaan selesai! Hasil disimpan di: /Download/Telegram/struktur_vendor_a505f.txt
```
