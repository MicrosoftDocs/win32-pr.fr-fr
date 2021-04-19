---
title: commande Mark
description: La commande Mark contrôle l’enregistrement et l’effacement des marques sur la bande vidéo. Les périphériques VCR reconnaissent cette commande.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- commande Mark Windows Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510532"
---
# <a name="mark-command"></a><span data-ttu-id="d0530-105">commande Mark</span><span class="sxs-lookup"><span data-stu-id="d0530-105">mark command</span></span>

<span data-ttu-id="d0530-106">La commande Mark contrôle l’enregistrement et l’effacement des marques sur la bande vidéo.</span><span class="sxs-lookup"><span data-stu-id="d0530-106">The mark command controls recording and erasing of marks on the videotape.</span></span> <span data-ttu-id="d0530-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="d0530-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="d0530-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="d0530-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d0530-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0530-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0530-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d0530-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d0530-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="d0530-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d0530-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d0530-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d0530-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span><span class="sxs-lookup"><span data-stu-id="d0530-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span></span>
</dt> <dd>

<span data-ttu-id="d0530-114">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0530-114">One of the following flags.</span></span>



| <span data-ttu-id="d0530-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0530-115">Value</span></span> | <span data-ttu-id="d0530-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d0530-116">Meaning</span></span>                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0530-117">erase</span><span class="sxs-lookup"><span data-stu-id="d0530-117">erase</span></span> | <span data-ttu-id="d0530-118">Efface une marque à la position actuelle, s’il en existe une.</span><span class="sxs-lookup"><span data-stu-id="d0530-118">Erases a mark at the current position, if one exists.</span></span> <span data-ttu-id="d0530-119">Pour effacer une marque, commencez par Rechercher la marque, puis émettez la commande marquer l’effacement.</span><span class="sxs-lookup"><span data-stu-id="d0530-119">To erase a mark, first seek to the mark and then issue the mark "erase" command.</span></span> |
| <span data-ttu-id="d0530-120">écrire</span><span class="sxs-lookup"><span data-stu-id="d0530-120">write</span></span> | <span data-ttu-id="d0530-121">Écrit une marque à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d0530-121">Writes a mark at the current position.</span></span> <span data-ttu-id="d0530-122">Il se peut que le magnétoscope doive être en mode lecture ou enregistrement pour que cette commande aboutisse.</span><span class="sxs-lookup"><span data-stu-id="d0530-122">The VCR might need to be in play or record mode for this command to succeed.</span></span>                    |



 

</dd> <dt>

<span data-ttu-id="d0530-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d0530-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d0530-124">Peut être « Wait », « Notify » ou « test ».</span><span class="sxs-lookup"><span data-stu-id="d0530-124">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="d0530-125">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d0530-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0530-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0530-126">Return Value</span></span>

<span data-ttu-id="d0530-127">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d0530-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0530-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d0530-128">Remarks</span></span>

<span data-ttu-id="d0530-129">Les marques sont des signaux spéciaux écrits dans le contenu qui peuvent être détectés par le magnétoscope lors de recherches à grande vitesse.</span><span class="sxs-lookup"><span data-stu-id="d0530-129">Marks are special signals written to the content that can be detected by the VCR during high-speed searches.</span></span> <span data-ttu-id="d0530-130">Les marques sont spécifiques au magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="d0530-130">Marks are VCR specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0530-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0530-131">Requirements</span></span>



| <span data-ttu-id="d0530-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0530-132">Requirement</span></span> | <span data-ttu-id="d0530-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0530-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d0530-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0530-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d0530-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0530-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d0530-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0530-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d0530-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0530-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d0530-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0530-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0530-139">MCI</span><span class="sxs-lookup"><span data-stu-id="d0530-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d0530-140">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="d0530-140">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

