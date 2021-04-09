---
title: commande Restore
description: La commande Restore copie une image continue d’un fichier vers la mémoire tampon de trame. Il s’agit de l’inverse de la commande de capture. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- commande Restore Windows Multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941692"
---
# <a name="restore-command"></a><span data-ttu-id="6620d-106">commande Restore</span><span class="sxs-lookup"><span data-stu-id="6620d-106">restore command</span></span>

<span data-ttu-id="6620d-107">La commande Restore copie une image continue d’un fichier vers la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="6620d-107">The restore command copies a still image from a file to the frame buffer.</span></span> <span data-ttu-id="6620d-108">Il s’agit de l’inverse de la commande de [capture](capture.md) .</span><span class="sxs-lookup"><span data-stu-id="6620d-108">This is the reverse of the [capture](capture.md) command.</span></span> <span data-ttu-id="6620d-109">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="6620d-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6620d-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="6620d-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6620d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6620d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6620d-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6620d-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6620d-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="6620d-113">Identifier of an MCI device.</span></span> <span data-ttu-id="6620d-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6620d-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6620d-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span><span class="sxs-lookup"><span data-stu-id="6620d-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span></span>
</dt> <dd>

<span data-ttu-id="6620d-116">Un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="6620d-116">One or more of the following flags.</span></span>



| <span data-ttu-id="6620d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6620d-117">Value</span></span>           | <span data-ttu-id="6620d-118">Signification</span><span class="sxs-lookup"><span data-stu-id="6620d-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6620d-119">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="6620d-119">at *rectangle*</span></span>  | <span data-ttu-id="6620d-120">Spécifie un rectangle par rapport à l’origine de la mémoire tampon du frame.</span><span class="sxs-lookup"><span data-stu-id="6620d-120">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="6620d-121">Le *rectangle* est spécifié en tant que *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="6620d-121">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="6620d-122">Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche et les coordonnées *x2 Y2* spécifient la largeur et la hauteur. Si cet indicateur n’est pas utilisé, l’image est copiée dans l’angle supérieur gauche de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="6620d-122">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.If this flag is not used, the image is copied to the upper left corner of the frame buffer.</span></span><br/> |
| <span data-ttu-id="6620d-123">à partir du *nom de fichier*</span><span class="sxs-lookup"><span data-stu-id="6620d-123">from *filename*</span></span> | <span data-ttu-id="6620d-124">Spécifie le nom du fichier image à rappeler.</span><span class="sxs-lookup"><span data-stu-id="6620d-124">Specifies the image filename to recall.</span></span> <span data-ttu-id="6620d-125">Cet indicateur est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6620d-125">This flag is required.</span></span>                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="6620d-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6620d-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6620d-127">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="6620d-127">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6620d-128">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6620d-128">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6620d-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6620d-129">Return Value</span></span>

<span data-ttu-id="6620d-130">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="6620d-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6620d-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6620d-131">Remarks</span></span>

<span data-ttu-id="6620d-132">Les appareils peuvent reconnaître un large éventail de formats d’image. une image bitmap indépendante du périphérique Windows est toujours reconnue.</span><span class="sxs-lookup"><span data-stu-id="6620d-132">Devices can recognize a variety of image formats; a Windows device-independent bitmap is always recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6620d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6620d-133">Requirements</span></span>



| <span data-ttu-id="6620d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6620d-134">Requirement</span></span> | <span data-ttu-id="6620d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6620d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6620d-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6620d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6620d-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6620d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6620d-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6620d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6620d-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6620d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6620d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6620d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6620d-141">MCI</span><span class="sxs-lookup"><span data-stu-id="6620d-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6620d-142">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="6620d-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6620d-143">attire</span><span class="sxs-lookup"><span data-stu-id="6620d-143">capture</span></span>](capture.md)
</dt> </dl>

 

