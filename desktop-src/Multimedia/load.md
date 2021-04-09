---
title: commande Load
description: La commande Load charge un fichier dans un format spécifique à l’appareil. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- commande de chargement multimédia Windows
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742493"
---
# <a name="load-command"></a><span data-ttu-id="6fed7-105">commande Load</span><span class="sxs-lookup"><span data-stu-id="6fed7-105">load command</span></span>

<span data-ttu-id="6fed7-106">La commande Load charge un fichier dans un format spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6fed7-106">The load command loads a file in a device-specific format.</span></span> <span data-ttu-id="6fed7-107">Les appareils vidéo et vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="6fed7-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="6fed7-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="6fed7-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6fed7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fed7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fed7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6fed7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6fed7-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="6fed7-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6fed7-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6fed7-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6fed7-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span><span class="sxs-lookup"><span data-stu-id="6fed7-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="6fed7-114">Chemin d’accès et nom de fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="6fed7-114">Path and filename to load.</span></span> <span data-ttu-id="6fed7-115">Pour les périphériques de superposition vidéo, cela peut également inclure un rectangle cible pour les données.</span><span class="sxs-lookup"><span data-stu-id="6fed7-115">For video-overlay devices, this can also include a target rectangle for the data.</span></span> <span data-ttu-id="6fed7-116">Pour spécifier un rectangle cible, spécifiez « at » suivi de **x1 Y1 x2 Y2**, où **x1 Y1** spécifient l’angle supérieur gauche du rectangle, et **x2 Y2** spécifient la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="6fed7-116">To specify a target rectangle, specify "at" followed by **X1 Y1 X2 Y2**, where **X1 Y1** specify the upper left corner of the rectangle, and **X2 Y2** specify the width and height.</span></span> <span data-ttu-id="6fed7-117">Le rectangle est relatif à l’origine de la mémoire tampon vidéo.</span><span class="sxs-lookup"><span data-stu-id="6fed7-117">The rectangle is relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="6fed7-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6fed7-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6fed7-119">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="6fed7-119">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="6fed7-120">Pour les appareils vidéo numériques, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="6fed7-120">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="6fed7-121">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6fed7-121">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fed7-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6fed7-122">Return Value</span></span>

<span data-ttu-id="6fed7-123">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="6fed7-123">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fed7-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6fed7-124">Remarks</span></span>

<span data-ttu-id="6fed7-125">L’appareil « vidboard » envoie un message de notification lorsque le chargement est terminé.</span><span class="sxs-lookup"><span data-stu-id="6fed7-125">The "vidboard" device sends a notification message when the loading is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="6fed7-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="6fed7-126">Examples</span></span>

<span data-ttu-id="6fed7-127">La commande suivante charge un fichier dans le périphérique « vidboard ».</span><span class="sxs-lookup"><span data-stu-id="6fed7-127">The following command loads a file into the "vidboard" device.</span></span>

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a><span data-ttu-id="6fed7-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fed7-128">Requirements</span></span>



| <span data-ttu-id="6fed7-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fed7-129">Requirement</span></span> | <span data-ttu-id="6fed7-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fed7-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6fed7-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fed7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6fed7-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fed7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6fed7-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fed7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6fed7-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fed7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6fed7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fed7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fed7-136">MCI</span><span class="sxs-lookup"><span data-stu-id="6fed7-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6fed7-137">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="6fed7-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

