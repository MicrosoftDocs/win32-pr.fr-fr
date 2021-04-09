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
# <a name="video-capture-reference"></a><span data-ttu-id="785db-106">Référence de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="785db-106">Video Capture Reference</span></span>

<span data-ttu-id="785db-107">Cette section décrit les fonctions, structures, messages et macros associés à la classe de fenêtre AVICap.</span><span class="sxs-lookup"><span data-stu-id="785db-107">This section describes the functions, structures, messages, and macros associated with the AVICap window class.</span></span> <span data-ttu-id="785db-108">Ces éléments sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="785db-108">These elements are grouped as follows.</span></span>

## <a name="basic-capture-operations"></a><span data-ttu-id="785db-109">Opérations de capture de base</span><span class="sxs-lookup"><span data-stu-id="785db-109">Basic Capture Operations</span></span>

-   [<span data-ttu-id="785db-110">**capCreateCaptureWindow**</span><span class="sxs-lookup"><span data-stu-id="785db-110">**capCreateCaptureWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [<span data-ttu-id="785db-111">**arrêt de l' \_ embout WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-111">**WM\_CAP\_ABORT**</span></span>](wm-cap-abort.md)
-   [<span data-ttu-id="785db-112">**\_connexion du \_ pilote WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="785db-112">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="785db-113">**séquence de l' \_ embout WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-113">**WM\_CAP\_SEQUENCE**</span></span>](wm-cap-sequence.md)
-   [<span data-ttu-id="785db-114">**arrêt de l' \_ embout WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-114">**WM\_CAP\_STOP**</span></span>](wm-cap-stop.md)

## <a name="capture-windows"></a><span data-ttu-id="785db-115">Capturer des fenêtres</span><span class="sxs-lookup"><span data-stu-id="785db-115">Capture Windows</span></span>

-   [<span data-ttu-id="785db-116">**CAPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="785db-116">**CAPSTATUS**</span></span>](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [<span data-ttu-id="785db-117">**capGetDriverDescription**</span><span class="sxs-lookup"><span data-stu-id="785db-117">**capGetDriverDescription**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [<span data-ttu-id="785db-118">**\_connexion du \_ pilote WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="785db-118">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="785db-119">**déconnexion du \_ pilote WM Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-119">**WM\_CAP\_DRIVER\_DISCONNECT**</span></span>](wm-cap-driver-disconnect.md)
-   [<span data-ttu-id="785db-120">**État de l’extraction de l' \_ embout WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-120">**WM\_CAP\_GET\_STATUS**</span></span>](wm-cap-get-status.md)

## <a name="capture-drivers"></a><span data-ttu-id="785db-121">Pilotes de capture</span><span class="sxs-lookup"><span data-stu-id="785db-121">Capture Drivers</span></span>

-   [<span data-ttu-id="785db-122">**CAPDRIVERCAPS**</span><span class="sxs-lookup"><span data-stu-id="785db-122">**CAPDRIVERCAPS**</span></span>](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [<span data-ttu-id="785db-123">**\_prise en cache du pilote WM \_ \_ \_ Caps**</span><span class="sxs-lookup"><span data-stu-id="785db-123">**WM\_CAP\_DRIVER\_GET\_CAPS**</span></span>](wm-cap-driver-get-caps.md)
-   [<span data-ttu-id="785db-124">**nom d’accès du \_ pilote WM Cap \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-124">**WM\_CAP\_DRIVER\_GET\_NAME**</span></span>](wm-cap-driver-get-name.md)
-   [<span data-ttu-id="785db-125">**\_ \_ version obtenue du pilote WM Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-125">**WM\_CAP\_DRIVER\_GET\_VERSION**</span></span>](wm-cap-driver-get-version.md)
-   [<span data-ttu-id="785db-126">**AUDIOFORMAT WM- \_ \_ recevoir \_**</span><span class="sxs-lookup"><span data-stu-id="785db-126">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="785db-127">**VIDEOFORMAT WM- \_ \_ recevoir \_**</span><span class="sxs-lookup"><span data-stu-id="785db-127">**WM\_CAP\_GET\_VIDEOFORMAT**</span></span>](wm-cap-get-videoformat.md)
-   [<span data-ttu-id="785db-128">**WM \_ Cap \_ Set \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="785db-128">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)
-   [<span data-ttu-id="785db-129">**WM \_ Cap \_ Set \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="785db-129">**WM\_CAP\_SET\_VIDEOFORMAT**</span></span>](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a><span data-ttu-id="785db-130">Mode Aperçu et superposition du pilote de capture</span><span class="sxs-lookup"><span data-stu-id="785db-130">Capture Driver Preview and Overlay Modes</span></span>

-   [<span data-ttu-id="785db-131">**superposition du \_ jeu de bouchons WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-131">**WM\_CAP\_SET\_OVERLAY**</span></span>](wm-cap-set-overlay.md)
-   [<span data-ttu-id="785db-132">**WM \_ Cap \_ Set \_ preview**</span><span class="sxs-lookup"><span data-stu-id="785db-132">**WM\_CAP\_SET\_PREVIEW**</span></span>](wm-cap-set-preview.md)
-   [<span data-ttu-id="785db-133">**WM \_ Cap \_ Set \_ PREVIEWRATE**</span><span class="sxs-lookup"><span data-stu-id="785db-133">**WM\_CAP\_SET\_PREVIEWRATE**</span></span>](wm-cap-set-previewrate.md)
-   [<span data-ttu-id="785db-134">**mise à l' \_ échelle WM Cap \_ Set \_**</span><span class="sxs-lookup"><span data-stu-id="785db-134">**WM\_CAP\_SET\_SCALE**</span></span>](wm-cap-set-scale.md)
-   [<span data-ttu-id="785db-135">**défilement de l' \_ ensemble de bouchon WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-135">**WM\_CAP\_SET\_SCROLL**</span></span>](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a><span data-ttu-id="785db-136">Boîtes de dialogue capturer le pilote vidéo</span><span class="sxs-lookup"><span data-stu-id="785db-136">Capture Driver Video Dialog Boxes</span></span>

-   [<span data-ttu-id="785db-137">**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**</span><span class="sxs-lookup"><span data-stu-id="785db-137">**WM\_CAP\_DLG\_VIDEOCOMPRESSION**</span></span>](wm-cap-dlg-videocompression.md)
-   [<span data-ttu-id="785db-138">**WM \_ Cap \_ DLG \_ VIDEODISPLAY**</span><span class="sxs-lookup"><span data-stu-id="785db-138">**WM\_CAP\_DLG\_VIDEODISPLAY**</span></span>](wm-cap-dlg-videodisplay.md)
-   [<span data-ttu-id="785db-139">**WM \_ Cap \_ DLG \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="785db-139">**WM\_CAP\_DLG\_VIDEOFORMAT**</span></span>](wm-cap-dlg-videoformat.md)
-   [<span data-ttu-id="785db-140">**WM \_ Cap \_ DLG \_ VIDEOSOURCE**</span><span class="sxs-lookup"><span data-stu-id="785db-140">**WM\_CAP\_DLG\_VIDEOSOURCE**</span></span>](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a><span data-ttu-id="785db-141">Format audio</span><span class="sxs-lookup"><span data-stu-id="785db-141">Audio Format</span></span>

-   [<span data-ttu-id="785db-142">**AUDIOFORMAT WM- \_ \_ recevoir \_**</span><span class="sxs-lookup"><span data-stu-id="785db-142">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="785db-143">**WM \_ Cap \_ Set \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="785db-143">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a><span data-ttu-id="785db-144">Paramètres de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="785db-144">Video Capture Settings</span></span>

-   [<span data-ttu-id="785db-145">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="785db-145">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="785db-146">**\_configuration de \_ la \_ séquence \_ d’extraction de l’embout WM**</span><span class="sxs-lookup"><span data-stu-id="785db-146">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="785db-147">**configuration de la séquence du jeu WM \_ Cap \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-147">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a><span data-ttu-id="785db-148">Capturer un fichier et des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="785db-148">Capture File and Buffers</span></span>

-   [<span data-ttu-id="785db-149">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="785db-149">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="785db-150">**\_allocation du \_ fichier d’embout WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-150">**WM\_CAP\_FILE\_ALLOCATE**</span></span>](wm-cap-file-allocate.md)
-   [<span data-ttu-id="785db-151">**fichier \_ de \_ \_ capture d’extraction de fichier \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-151">**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**</span></span>](wm-cap-file-get-capture-file.md)
-   [<span data-ttu-id="785db-152">**\_fichier d' \_ \_ enregistrement WM Cap**</span><span class="sxs-lookup"><span data-stu-id="785db-152">**WM\_CAP\_FILE\_SAVEAS**</span></span>](wm-cap-file-saveas.md)
-   [<span data-ttu-id="785db-153">**\_fichier de \_ capture de jeu de fichiers WM Cap \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-153">**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**</span></span>](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a><span data-ttu-id="785db-154">Utilisation directe des données de capture</span><span class="sxs-lookup"><span data-stu-id="785db-154">Directly Using Capture Data</span></span>

-   [<span data-ttu-id="785db-155">**nofile de séquence de l' \_ embout WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-155">**WM\_CAP\_SEQUENCE\_NOFILE**</span></span>](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a><span data-ttu-id="785db-156">Capturer à partir d’un périphérique MCI</span><span class="sxs-lookup"><span data-stu-id="785db-156">Capture from MCI Device</span></span>

-   [<span data-ttu-id="785db-157">**\_appareil WM \_ Set \_ MCI \_**</span><span class="sxs-lookup"><span data-stu-id="785db-157">**WM\_CAP\_SET\_MCI\_DEVICE**</span></span>](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a><span data-ttu-id="785db-158">Capture manuelle des frames</span><span class="sxs-lookup"><span data-stu-id="785db-158">Manual Frame Capture</span></span>

-   [<span data-ttu-id="785db-159">**\_ \_ cadre unique WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="785db-159">**WM\_CAP\_SINGLE\_FRAME**</span></span>](wm-cap-single-frame.md)
-   [<span data-ttu-id="785db-160">**\_fermeture de \_ \_ Frame unique WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="785db-160">**WM\_CAP\_SINGLE\_FRAME\_CLOSE**</span></span>](wm-cap-single-frame-close.md)
-   [<span data-ttu-id="785db-161">**\_ \_ Frame unique WM \_ embout \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="785db-161">**WM\_CAP\_SINGLE\_FRAME\_OPEN**</span></span>](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a><span data-ttu-id="785db-162">Capture de Still-Image</span><span class="sxs-lookup"><span data-stu-id="785db-162">Still-Image Capture</span></span>

-   [<span data-ttu-id="785db-163">**WM \_ - \_ modifier la \_ copie**</span><span class="sxs-lookup"><span data-stu-id="785db-163">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="785db-164">**\_fichier WM \_ \_ SAVEDIB**</span><span class="sxs-lookup"><span data-stu-id="785db-164">**WM\_CAP\_FILE\_SAVEDIB**</span></span>](wm-cap-file-savedib.md)
-   [<span data-ttu-id="785db-165">**FRAME de manipulation de l' \_ embout WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-165">**WM\_CAP\_GRAB\_FRAME**</span></span>](wm-cap-grab-frame.md)
-   [<span data-ttu-id="785db-166">**nostop de la \_ \_ \_ trame de manipulation de l’embout WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-166">**WM\_CAP\_GRAB\_FRAME\_NOSTOP**</span></span>](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a><span data-ttu-id="785db-167">Options de capture avancées</span><span class="sxs-lookup"><span data-stu-id="785db-167">Advanced Capture Options</span></span>

-   [<span data-ttu-id="785db-168">**jeu de fichiers de l' \_ embout WM \_ \_ \_ INFOCHUNK**</span><span class="sxs-lookup"><span data-stu-id="785db-168">**WM\_CAP\_FILE\_SET\_INFOCHUNK**</span></span>](wm-cap-file-set-infochunk.md)
-   [<span data-ttu-id="785db-169">**WM \_ Cap \_ Obtient \_ les \_ données utilisateur**</span><span class="sxs-lookup"><span data-stu-id="785db-169">**WM\_CAP\_GET\_USER\_DATA**</span></span>](wm-cap-get-user-data.md)
-   [<span data-ttu-id="785db-170">**WM \_ Cap \_ définir \_ les \_ données utilisateur**</span><span class="sxs-lookup"><span data-stu-id="785db-170">**WM\_CAP\_SET\_USER\_DATA**</span></span>](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a><span data-ttu-id="785db-171">Utilisation des palettes</span><span class="sxs-lookup"><span data-stu-id="785db-171">Working with Palettes</span></span>

-   [<span data-ttu-id="785db-172">**WM \_ - \_ modifier la \_ copie**</span><span class="sxs-lookup"><span data-stu-id="785db-172">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="785db-173">**CRÉATION d’une base de \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-173">**WM\_CAP\_PAL\_AUTOCREATE**</span></span>](wm-cap-pal-autocreate.md)
-   [<span data-ttu-id="785db-174">**WM \_ Cap- \_ PAL \_ MANUALCREATE**</span><span class="sxs-lookup"><span data-stu-id="785db-174">**WM\_CAP\_PAL\_MANUALCREATE**</span></span>](wm-cap-pal-manualcreate.md)
-   [<span data-ttu-id="785db-175">**PAL de WM \_ Cap \_ \_ Open**</span><span class="sxs-lookup"><span data-stu-id="785db-175">**WM\_CAP\_PAL\_OPEN**</span></span>](wm-cap-pal-open.md)
-   [<span data-ttu-id="785db-176">**\_coller WM capuchon \_ PAL \_**</span><span class="sxs-lookup"><span data-stu-id="785db-176">**WM\_CAP\_PAL\_PASTE**</span></span>](wm-cap-pal-paste.md)
-   [<span data-ttu-id="785db-177">**\_enregistrement WM Cap \_ PAL \_**</span><span class="sxs-lookup"><span data-stu-id="785db-177">**WM\_CAP\_PAL\_SAVE**</span></span>](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a><span data-ttu-id="785db-178">Donner à d’autres applications</span><span class="sxs-lookup"><span data-stu-id="785db-178">Yielding to Other Applications</span></span>

-   [<span data-ttu-id="785db-179">**\_configuration de \_ la \_ séquence \_ d’extraction de l’embout WM**</span><span class="sxs-lookup"><span data-stu-id="785db-179">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="785db-180">**\_jeu de \_ \_ rappels de la définition du jeu WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-180">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="785db-181">**configuration de la séquence du jeu WM \_ Cap \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-181">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a><span data-ttu-id="785db-182">Fonctions de rappel AVICap</span><span class="sxs-lookup"><span data-stu-id="785db-182">AVICap Callback Functions</span></span>

-   [<span data-ttu-id="785db-183">**capControlCallback**</span><span class="sxs-lookup"><span data-stu-id="785db-183">**capControlCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [<span data-ttu-id="785db-184">**capErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="785db-184">**capErrorCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [<span data-ttu-id="785db-185">**capStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="785db-185">**capStatusCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [<span data-ttu-id="785db-186">**capVideoStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="785db-186">**capVideoStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [<span data-ttu-id="785db-187">**capWaveStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="785db-187">**capWaveStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [<span data-ttu-id="785db-188">**capYieldCallback**</span><span class="sxs-lookup"><span data-stu-id="785db-188">**capYieldCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [<span data-ttu-id="785db-189">**WM \_ Cap \_ Set \_ callback \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="785db-189">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)
-   [<span data-ttu-id="785db-190">**erreur de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-190">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="785db-191">**FRAME de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-191">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)
-   [<span data-ttu-id="785db-192">**État de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="785db-192">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="785db-193">**WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM**</span><span class="sxs-lookup"><span data-stu-id="785db-193">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="785db-194">**WM \_ Cap \_ Set \_ callback \_ WAVESTREAM**</span><span class="sxs-lookup"><span data-stu-id="785db-194">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)
-   [<span data-ttu-id="785db-195">**\_jeu de \_ \_ rappels de la définition du jeu WM \_**</span><span class="sxs-lookup"><span data-stu-id="785db-195">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a><span data-ttu-id="785db-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="785db-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="785db-197">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="785db-197">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




