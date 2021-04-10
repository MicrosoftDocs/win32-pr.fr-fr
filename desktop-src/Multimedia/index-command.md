---
title: index, commande
description: La commande index contrôle l’affichage à l’écran d’un magnétoscope. Les périphériques VCR reconnaissent cette commande.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- commande d’index Windows Multimedia
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942896"
---
# <a name="index-command"></a><span data-ttu-id="685b1-105">index, commande</span><span class="sxs-lookup"><span data-stu-id="685b1-105">index command</span></span>

<span data-ttu-id="685b1-106">La commande index contrôle l’affichage à l’écran d’un magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="685b1-106">The index command controls a VCR's on-screen display.</span></span> <span data-ttu-id="685b1-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="685b1-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="685b1-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="685b1-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="685b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="685b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685b1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="685b1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="685b1-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="685b1-111">Identifier of an MCI device.</span></span> <span data-ttu-id="685b1-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="685b1-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="685b1-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span><span class="sxs-lookup"><span data-stu-id="685b1-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span></span>
</dt> <dd>

<span data-ttu-id="685b1-114">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="685b1-114">One of the following flags.</span></span>



| <span data-ttu-id="685b1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="685b1-115">Value</span></span> | <span data-ttu-id="685b1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="685b1-116">Meaning</span></span>                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685b1-117">arrêt</span><span class="sxs-lookup"><span data-stu-id="685b1-117">off</span></span>   | <span data-ttu-id="685b1-118">Désactive l’affichage à l’écran.</span><span class="sxs-lookup"><span data-stu-id="685b1-118">Turns off the on-screen display.</span></span>                                                                                         |
| <span data-ttu-id="685b1-119">sur</span><span class="sxs-lookup"><span data-stu-id="685b1-119">on</span></span>    | <span data-ttu-id="685b1-120">Active l’affichage à l’écran.</span><span class="sxs-lookup"><span data-stu-id="685b1-120">Turns on the on-screen display.</span></span> <span data-ttu-id="685b1-121">L’élément à afficher est spécifié par l’indicateur « index » de la commande [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="685b1-121">The item to be displayed is specified by the "index" flag of the [set](set.md) command.</span></span> |



 

</dd> <dt>

<span data-ttu-id="685b1-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="685b1-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="685b1-123">Peut être « Wait », « Notify » ou « test ».</span><span class="sxs-lookup"><span data-stu-id="685b1-123">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="685b1-124">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="685b1-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685b1-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="685b1-125">Return Value</span></span>

<span data-ttu-id="685b1-126">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="685b1-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="685b1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="685b1-127">Requirements</span></span>



| <span data-ttu-id="685b1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="685b1-128">Requirement</span></span> | <span data-ttu-id="685b1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="685b1-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="685b1-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685b1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="685b1-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685b1-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="685b1-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685b1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="685b1-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685b1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="685b1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="685b1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685b1-135">MCI</span><span class="sxs-lookup"><span data-stu-id="685b1-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="685b1-136">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="685b1-136">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="685b1-137">set</span><span class="sxs-lookup"><span data-stu-id="685b1-137">set</span></span>](set.md)
</dt> </dl>

 

