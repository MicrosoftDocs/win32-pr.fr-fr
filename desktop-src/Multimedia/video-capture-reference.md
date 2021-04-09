---
title: Référence de capture vidéo
description: Référence de capture vidéo
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video for Windows (VFW), référence de capture vidéo
- VFW (vidéo pour Windows), référence de capture vidéo
- AVICap, référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028808"
---
# <a name="video-capture-reference"></a>Référence de capture vidéo

Cette section décrit les fonctions, structures, messages et macros associés à la classe de fenêtre AVICap. Ces éléments sont regroupés comme suit.

## <a name="basic-capture-operations"></a>Opérations de capture de base

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**arrêt de l' \_ embout WM \_**](wm-cap-abort.md)
-   [**\_connexion du \_ pilote WM Cap \_**](wm-cap-driver-connect.md)
-   [**séquence de l' \_ embout WM \_**](wm-cap-sequence.md)
-   [**arrêt de l' \_ embout WM \_**](wm-cap-stop.md)

## <a name="capture-windows"></a>Capturer des fenêtres

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**\_connexion du \_ pilote WM Cap \_**](wm-cap-driver-connect.md)
-   [**déconnexion du \_ pilote WM Cap \_ \_**](wm-cap-driver-disconnect.md)
-   [**État de l’extraction de l' \_ embout WM \_ \_**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Pilotes de capture

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**\_prise en cache du pilote WM \_ \_ \_ Caps**](wm-cap-driver-get-caps.md)
-   [**nom d’accès du \_ pilote WM Cap \_ \_ \_**](wm-cap-driver-get-name.md)
-   [**\_ \_ version obtenue du pilote WM Cap \_ \_**](wm-cap-driver-get-version.md)
-   [**AUDIOFORMAT WM- \_ \_ recevoir \_**](wm-cap-get-audioformat.md)
-   [**VIDEOFORMAT WM- \_ \_ recevoir \_**](wm-cap-get-videoformat.md)
-   [**WM \_ Cap \_ Set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)
-   [**WM \_ Cap \_ Set \_ VIDEOFORMAT**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Mode Aperçu et superposition du pilote de capture

-   [**superposition du \_ jeu de bouchons WM \_ \_**](wm-cap-set-overlay.md)
-   [**WM \_ Cap \_ Set \_ preview**](wm-cap-set-preview.md)
-   [**WM \_ Cap \_ Set \_ PREVIEWRATE**](wm-cap-set-previewrate.md)
-   [**mise à l' \_ échelle WM Cap \_ Set \_**](wm-cap-set-scale.md)
-   [**défilement de l' \_ ensemble de bouchon WM \_ \_**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Boîtes de dialogue capturer le pilote vidéo

-   [**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md)
-   [**WM \_ Cap \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md)
-   [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md)
-   [**WM \_ Cap \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Format audio

-   [**AUDIOFORMAT WM- \_ \_ recevoir \_**](wm-cap-get-audioformat.md)
-   [**WM \_ Cap \_ Set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Paramètres de capture vidéo

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_configuration de \_ la \_ séquence \_ d’extraction de l’embout WM**](wm-cap-get-sequence-setup.md)
-   [**configuration de la séquence du jeu WM \_ Cap \_ \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Capturer un fichier et des mémoires tampons

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_allocation du \_ fichier d’embout WM \_**](wm-cap-file-allocate.md)
-   [**fichier \_ de \_ \_ capture d’extraction de fichier \_ WM \_**](wm-cap-file-get-capture-file.md)
-   [**\_fichier d' \_ \_ enregistrement WM Cap**](wm-cap-file-saveas.md)
-   [**\_fichier de \_ capture de jeu de fichiers WM Cap \_ \_ \_**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Utilisation directe des données de capture

-   [**nofile de séquence de l' \_ embout WM \_ \_**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Capturer à partir d’un périphérique MCI

-   [**\_appareil WM \_ Set \_ MCI \_**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Capture manuelle des frames

-   [**\_ \_ cadre unique WM \_ Cap**](wm-cap-single-frame.md)
-   [**\_fermeture de \_ \_ Frame unique WM Cap \_**](wm-cap-single-frame-close.md)
-   [**\_ \_ Frame unique WM \_ embout \_ ouvert**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Capture de Still-Image

-   [**WM \_ - \_ modifier la \_ copie**](wm-cap-edit-copy.md)
-   [**\_fichier WM \_ \_ SAVEDIB**](wm-cap-file-savedib.md)
-   [**FRAME de manipulation de l' \_ embout WM \_ \_**](wm-cap-grab-frame.md)
-   [**nostop de la \_ \_ \_ trame de manipulation de l’embout WM \_**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Options de capture avancées

-   [**jeu de fichiers de l' \_ embout WM \_ \_ \_ INFOCHUNK**](wm-cap-file-set-infochunk.md)
-   [**WM \_ Cap \_ Obtient \_ les \_ données utilisateur**](wm-cap-get-user-data.md)
-   [**WM \_ Cap \_ définir \_ les \_ données utilisateur**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Utilisation des palettes

-   [**WM \_ - \_ modifier la \_ copie**](wm-cap-edit-copy.md)
-   [**CRÉATION d’une base de \_ \_ \_**](wm-cap-pal-autocreate.md)
-   [**WM \_ Cap- \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md)
-   [**PAL de WM \_ Cap \_ \_ Open**](wm-cap-pal-open.md)
-   [**\_coller WM capuchon \_ PAL \_**](wm-cap-pal-paste.md)
-   [**\_enregistrement WM Cap \_ PAL \_**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Donner à d’autres applications

-   [**\_configuration de \_ la \_ séquence \_ d’extraction de l’embout WM**](wm-cap-get-sequence-setup.md)
-   [**\_jeu de \_ \_ rappels de la définition du jeu WM \_**](wm-cap-set-callback-yield.md)
-   [**configuration de la séquence du jeu WM \_ Cap \_ \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Fonctions de rappel AVICap

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**WM \_ Cap \_ Set \_ callback \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)
-   [**erreur de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-error.md)
-   [**FRAME de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-frame.md)
-   [**État de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-status.md)
-   [**WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ Cap \_ Set \_ callback \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)
-   [**\_jeu de \_ \_ rappels de la définition du jeu WM \_**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 




