---
title: Fonctions DWM
description: Cette section contient des informations sur les fonctions de Gestionnaire de fenêtrage (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Gestionnaire de fenêtrage (DWM), référence
- DWM (Gestionnaire de fenêtrage), référence
- Gestionnaire de fenêtrage (DWM), fonctions
- DWM (Gestionnaire de fenêtrage), fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316602"
---
# <a name="dwm-functions"></a><span data-ttu-id="c7541-107">Fonctions DWM</span><span class="sxs-lookup"><span data-stu-id="c7541-107">DWM Functions</span></span>

<span data-ttu-id="c7541-108">Cette section contient des informations sur les fonctions de Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="c7541-108">This section contains information about the Desktop Window Manager (DWM) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c7541-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c7541-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7541-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c7541-110">Topic</span></span></th>
<th><span data-ttu-id="c7541-111">Description</span><span class="sxs-lookup"><span data-stu-id="c7541-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7541-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-113">Cette fonction n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c7541-113">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-115">Procédure de fenêtre par défaut pour le test de positionnement DWM au sein de la zone non cliente.</span><span class="sxs-lookup"><span data-stu-id="c7541-115">Default window procedure for DWM hit testing within the non-client area.</span></span><br/> <span data-ttu-id="c7541-116">Vous devez également vous assurer que <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> est appelé pour le message <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c7541-116">You also need to ensure that <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> message.</span></span> <span data-ttu-id="c7541-117">Si <strong>DwmDefWindowProc</strong> n’est pas appelé pour le message <strong>WM_NCMOUSELEAVE</strong> , DWM ne supprime pas la mise en surbrillance des boutons <strong>agrandir</strong>, <strong>réduire</strong>et <strong>Fermer</strong> lorsque le curseur quitte la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c7541-117">If <strong>DwmDefWindowProc</strong> is not called for the <strong>WM_NCMOUSELEAVE</strong> message, DWM does not remove the highlighting from the <strong>Maximize</strong>, <strong>Minimize</strong>, and <strong>Close</strong> buttons when the cursor leaves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-119">Cette fonction n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c7541-119">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-121">Active l’effet de flou sur une fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c7541-121">Enables the blur effect on a specified window.</span></span><br/></td><span data-ttu-id="c7541-122">
<b>Remarque</b> À partir de Windows 8, l’appel de cette fonction n’entraîne pas l’effet de flou, en raison d’un changement de style dans la manière dont les fenêtres sont affichées.</span><span class="sxs-lookup"><span data-stu-id="c7541-122">
<b>Note</b> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-124">Active ou désactive la composition DWM.</span><span class="sxs-lookup"><span data-stu-id="c7541-124">Enables or disables DWM composition.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c7541-125">Cette fonction est déconseillée à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c7541-125">This function is deprecated as of Windows 8.</span></span> <span data-ttu-id="c7541-126">DWM ne peut plus être désactivé par programmation.</span><span class="sxs-lookup"><span data-stu-id="c7541-126">DWM can no longer be programmatically disabled.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-128">Notifie le DWM d’accepter ou de refuser la planification de service de planification de classe multimédia (MMCSS) pendant que le processus appelant est actif.</span><span class="sxs-lookup"><span data-stu-id="c7541-128">Notifies the DWM to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-130">Étend le frame de fenêtre dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="c7541-130">Extends the window frame into the client area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-132">Émet un appel de vidage qui bloque l’appelant jusqu’au présent suivant, lorsque toutes les mises à jour de surface Microsoft DirectX actuellement en suspens ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="c7541-132">Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made.</span></span> <span data-ttu-id="c7541-133">Cela compense les scènes très complexes ou les processus appelant avec une priorité très faible.</span><span class="sxs-lookup"><span data-stu-id="c7541-133">This compensates for very complex scenes or calling processes with very low priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-135">Récupère la couleur actuelle utilisée pour la composition du verre DWM.</span><span class="sxs-lookup"><span data-stu-id="c7541-135">Retrieves the current color used for DWM glass composition.</span></span> <span data-ttu-id="c7541-136">Cette valeur est basée sur le modèle de couleurs actuel et peut être modifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7541-136">This value is based on the current color scheme and can be modified by the user.</span></span> <span data-ttu-id="c7541-137">Les applications peuvent écouter les modifications de couleur en gérant la notification de <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c7541-137">Applications can listen for color changes by handling the <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-139">Récupère les informations de minutage de la composition actuelle pour une fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c7541-139">Retrieves the current composition timing information for a specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-141">Cette fonction n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c7541-141">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-143">Cette fonction n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c7541-143">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-145">Récupère les attributs de transport.</span><span class="sxs-lookup"><span data-stu-id="c7541-145">Retrieves transport attributes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span></span><br/></td>
<td><blockquote><span data-ttu-id="c7541-147">
<strong>Remarque</strong>  Cette fonction est publiquement disponible, mais non fonctionnelle, pour Windows 10, version 1803.</span><span class="sxs-lookup"><span data-stu-id="c7541-147">
<strong>Note</strong>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</span></span>
</blockquote>
<span data-ttu-id="c7541-148">Vérifie la configuration requise pour obtenir des onglets dans la barre de titre de l’application pour la fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c7541-148">Checks the requirements needed to get tabs in the application title bar for the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-150">Récupère la valeur actuelle d’un attribut spécifié appliqué à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c7541-150">Retrieves the current value of a specified attribute applied to a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-152">Appelée par une application pour indiquer que toutes les images bitmap sous forme fournies précédemment à partir d’une fenêtre, à la fois des miniatures et des représentations de lecture, doivent être actualisées.</span><span class="sxs-lookup"><span data-stu-id="c7541-152">Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-154">Obtient une valeur qui indique si la composition DWM est activée.</span><span class="sxs-lookup"><span data-stu-id="c7541-154">Obtains a value that indicates whether DWM composition is enabled.</span></span> <span data-ttu-id="c7541-155">Les applications sur les ordinateurs exécutant Windows 7 ou une version antérieure peuvent écouter les changements d’état de composition en gérant la notification de <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c7541-155">Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-157">Modifie le nombre d’actualisations de l’analyse à l’aide desquelles le frame précédent s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c7541-157">Changes the number of monitor refreshes through which the previous frame will be displayed.</span></span> <br/> <span data-ttu-id="c7541-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7541-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="c7541-159">À partir de Windows 8.1, les appels à <strong>DwmModifyPreviousDxFrameDuration</strong> retournent toujours E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c7541-159">Starting with Windows 8.1, calls to <strong>DwmModifyPreviousDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-161">Récupère la taille source de la miniature DWM.</span><span class="sxs-lookup"><span data-stu-id="c7541-161">Retrieves the source size of the DWM thumbnail.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-163">Crée une relation de miniature DWM entre les fenêtres de destination et sources.</span><span class="sxs-lookup"><span data-stu-id="c7541-163">Creates a DWM thumbnail relationship between the destination and source windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-165">Notifie DWM qu’un contact tactile a été reconnu comme un geste et que le DWM doit dessiner des commentaires pour ce mouvement.</span><span class="sxs-lookup"><span data-stu-id="c7541-165">Notifies DWM that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-167">Définit le nombre d’actualisations de l’analyse à l’aide desquelles afficher le frame présenté.</span><span class="sxs-lookup"><span data-stu-id="c7541-167">Sets the number of monitor refreshes through which to display the presented frame.</span></span> <br/> <span data-ttu-id="c7541-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7541-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="c7541-169">À partir de Windows 8.1, les appels à <strong>DwmSetDxFrameDuration</strong> retournent toujours E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c7541-169">Starting with Windows 8.1, calls to <strong>DwmSetDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-171">Définit une image bitmap statique, sous forme pour afficher un <em>aperçu instantané</em> (également appelé <em>Aperçu avant impression</em>) d’une fenêtre ou d’un onglet. La barre des tâches peut utiliser cette image bitmap pour afficher un aperçu complet d’une fenêtre ou d’un onglet.</span><span class="sxs-lookup"><span data-stu-id="c7541-171">Sets a static, iconic bitmap to display a <em>live preview</em> (also known as a <em>Peek preview</em>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-173">Définit une image bitmap statique, sous forme sur une fenêtre ou un onglet à utiliser comme représentation miniature.</span><span class="sxs-lookup"><span data-stu-id="c7541-173">Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation.</span></span> <span data-ttu-id="c7541-174">La barre des tâches peut utiliser cette image bitmap comme cible de commutateur de miniatures pour la fenêtre ou l’onglet.</span><span class="sxs-lookup"><span data-stu-id="c7541-174">The taskbar can use this bitmap as a thumbnail switch target for the window or tab.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-176">Définit les paramètres présents pour la composition de frame.</span><span class="sxs-lookup"><span data-stu-id="c7541-176">Sets the present parameters for frame composition.</span></span> <br/> <span data-ttu-id="c7541-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7541-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> is no longer supported.</span></span> <span data-ttu-id="c7541-178">À partir de Windows 8.1, les appels à <strong>DwmSetPresentParameters</strong> retournent toujours E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c7541-178">Starting with Windows 8.1, calls to <strong>DwmSetPresentParameters</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-180">Définit la valeur des attributs de rendu non-client pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c7541-180">Sets the value of non-client rendering attributes for a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-182">Appelé par une application ou une infrastructure pour spécifier le type de retour visuel à dessiner en réponse à un contact tactile ou de stylet particulier.</span><span class="sxs-lookup"><span data-stu-id="c7541-182">Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-184">Active les commentaires graphiques des interactions tactiles et de glissement pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7541-184">Enables the graphical feedback of touch and drag interactions to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-186">Coordonne les animations des fenêtres outil avec le DWM.</span><span class="sxs-lookup"><span data-stu-id="c7541-186">Coordinates the animations of tool windows with the DWM.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7541-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-188">Supprime une relation de miniature DWM créée par la fonction <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c7541-188">Removes a DWM thumbnail relationship created by the <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7541-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7541-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7541-190">Met à jour les propriétés d’une miniature DWM.</span><span class="sxs-lookup"><span data-stu-id="c7541-190">Updates the properties for a DWM thumbnail.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

