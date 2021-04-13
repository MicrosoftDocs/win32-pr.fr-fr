---
title: Réglage de la vitesse, du volume et du zoom
description: Réglage de la vitesse, du volume et du zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed macro)
- MCIWndGetSpeed macro)
- MCIWndSetVolume macro)
- MCIWndGetVolume macro)
- MCIWndSetZoom macro)
- MCIWndGetZoom macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379983"
---
# <a name="adjusting-speed-volume-and-zoom"></a><span data-ttu-id="1242f-109">Réglage de la vitesse, du volume et du zoom</span><span class="sxs-lookup"><span data-stu-id="1242f-109">Adjusting Speed, Volume, and Zoom</span></span>

<span data-ttu-id="1242f-110">Les macros vitesse, volume et zoom fournissent les fonctionnalités des commandes **affichage**, **volume** et **Vitesse** du menu MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="1242f-110">The speed, volume, and zoom macros provide the functionality of the **View**, **Volume**, and **Speed** commands on the MCIWnd menu.</span></span> <span data-ttu-id="1242f-111">Les macros décrites dans cette section sont généralement utilisées avec des vidéos et d’autres périphériques qui affichent des images pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="1242f-111">The macros described in this section are generally used with video and other devices that display images during playback.</span></span>

<span data-ttu-id="1242f-112">Certains appareils prennent en charge plusieurs modifications de vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="1242f-112">Some devices support multiple playback speed changes.</span></span> <span data-ttu-id="1242f-113">Vous pouvez définir la vitesse de lecture de ces périphériques à l’aide de la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="1242f-113">You can set the playback speed for these devices by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span> <span data-ttu-id="1242f-114">Cette macro définit la vitesse de lecture sur 1000.</span><span class="sxs-lookup"><span data-stu-id="1242f-114">This macro defines the playback speed as 1000.</span></span> <span data-ttu-id="1242f-115">Des valeurs plus élevées indiquent des vitesses plus rapides.</span><span class="sxs-lookup"><span data-stu-id="1242f-115">Higher values indicate faster speeds.</span></span> <span data-ttu-id="1242f-116">Des valeurs inférieures indiquent des vitesses plus lentes.</span><span class="sxs-lookup"><span data-stu-id="1242f-116">Lower values indicate slower speeds.</span></span>

<span data-ttu-id="1242f-117">Vous pouvez récupérer la vitesse de lecture actuelle à l’aide de la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="1242f-117">You can retrieve the current playback speed by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span> <span data-ttu-id="1242f-118">Cette macro utilise les mêmes valeurs et la même plage que celles utilisées par **MCIWndSetSpeed**.</span><span class="sxs-lookup"><span data-stu-id="1242f-118">This macro uses the same values and range as those used by **MCIWndSetSpeed**.</span></span>

<span data-ttu-id="1242f-119">Certains appareils prennent en charge les modifications de volume.</span><span class="sxs-lookup"><span data-stu-id="1242f-119">Some devices support volume changes.</span></span> <span data-ttu-id="1242f-120">Vous pouvez ajuster ou définir le volume à l’aide de la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="1242f-120">You can adjust or set the volume by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span> <span data-ttu-id="1242f-121">Cette macro définit le niveau de volume normal en tant que 1000.</span><span class="sxs-lookup"><span data-stu-id="1242f-121">This macro defines the normal volume level as 1000.</span></span> <span data-ttu-id="1242f-122">Des valeurs plus élevées indiquent des volumes plus forts.</span><span class="sxs-lookup"><span data-stu-id="1242f-122">Higher values indicate louder volumes.</span></span> <span data-ttu-id="1242f-123">Les valeurs inférieures indiquent des volumes plus silencieux.</span><span class="sxs-lookup"><span data-stu-id="1242f-123">Lower values indicate quieter volumes.</span></span>

<span data-ttu-id="1242f-124">Vous pouvez récupérer le niveau de volume actuel à l’aide de la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="1242f-124">You can retrieve the current volume level by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span> <span data-ttu-id="1242f-125">Cette macro utilise les mêmes valeurs numériques et plages que celles utilisées par **MCIWndSetVolume**.</span><span class="sxs-lookup"><span data-stu-id="1242f-125">This macro uses the same numerical values and range as those used by **MCIWndSetVolume**.</span></span>

<span data-ttu-id="1242f-126">Pour les appareils qui utilisent une fenêtre de lecture, MCIWnd prend en charge une fonctionnalité de zoom qui définit la taille de l’image de lecture.</span><span class="sxs-lookup"><span data-stu-id="1242f-126">For devices that use a playback window, MCIWnd supports a zoom feature that sets the size of the playback image.</span></span> <span data-ttu-id="1242f-127">Vous pouvez définir la taille de l’image de lecture à l’aide de la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="1242f-127">You can set the playback image size by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span> <span data-ttu-id="1242f-128">La macro redéfinit la taille de l’image de lecture tout en conservant les proportions constantes de l’image.</span><span class="sxs-lookup"><span data-stu-id="1242f-128">The macro redefines the playback image size while maintaining a constant aspect ratio for the image.</span></span> <span data-ttu-id="1242f-129">La valeur de zoom est définie sous la forme d’un pourcentage de la taille de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="1242f-129">The zoom value is defined as a percentage of the original image size.</span></span> <span data-ttu-id="1242f-130">Ainsi, 100 représente la taille d’image d’origine, 50 indique que l’image affichée est la moitié de sa taille d’origine et 200 indique que l’image affichée est deux fois sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="1242f-130">Thus, 100 represents the original image size, 50 indicates the image shown is half its original size, and 200 indicates that the image shown is twice its original size.</span></span>

<span data-ttu-id="1242f-131">Vous pouvez récupérer la valeur de zoom actuelle à l’aide de la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="1242f-131">You can retrieve the current zoom value by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span> <span data-ttu-id="1242f-132">Cette macro utilise les mêmes valeurs et la même plage que celles utilisées par **MCIWndSetZoom**.</span><span class="sxs-lookup"><span data-stu-id="1242f-132">This macro uses the same values and range as those used by **MCIWndSetZoom**.</span></span>

> [!Note]  
> <span data-ttu-id="1242f-133">Les pilotes audio et Waveform-Audio MCI standard ne prennent pas en charge les modifications de volume ou de vitesse.</span><span class="sxs-lookup"><span data-stu-id="1242f-133">The standard MCI CD audio and waveform-audio drivers do not support volume or speed changes.</span></span>

 

 

 




