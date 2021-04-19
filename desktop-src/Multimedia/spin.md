---
title: spin, commande
description: La commande toupie commence à tourner un disque ou arrête le disque. Les appareils Videodisc reconnaissent cette commande.
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- commande toupie Windows multimédia
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536912"
---
# <a name="spin-command"></a><span data-ttu-id="da030-105">spin, commande</span><span class="sxs-lookup"><span data-stu-id="da030-105">spin command</span></span>

<span data-ttu-id="da030-106">La commande toupie commence à tourner un disque ou arrête le disque.</span><span class="sxs-lookup"><span data-stu-id="da030-106">The spin command starts spinning a disc or stops the disc from spinning.</span></span> <span data-ttu-id="da030-107">Les appareils Videodisc reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="da030-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="da030-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="da030-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="da030-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da030-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da030-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="da030-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="da030-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="da030-111">Identifier of an MCI device.</span></span> <span data-ttu-id="da030-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="da030-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="da030-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span><span class="sxs-lookup"><span data-stu-id="da030-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span></span>
</dt> <dd>

<span data-ttu-id="da030-114">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="da030-114">One of the following flags.</span></span>



| <span data-ttu-id="da030-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="da030-115">Value</span></span> | <span data-ttu-id="da030-116">Signification</span><span class="sxs-lookup"><span data-stu-id="da030-116">Meaning</span></span>                       |
|-------|-------------------------------|
| <span data-ttu-id="da030-117">Éteindre</span><span class="sxs-lookup"><span data-stu-id="da030-117">down</span></span>  | <span data-ttu-id="da030-118">Arrête la rotation du disque.</span><span class="sxs-lookup"><span data-stu-id="da030-118">Stops the disc from spinning.</span></span> |
| <span data-ttu-id="da030-119">up</span><span class="sxs-lookup"><span data-stu-id="da030-119">up</span></span>    | <span data-ttu-id="da030-120">Démarre la rotation du disque.</span><span class="sxs-lookup"><span data-stu-id="da030-120">Starts spinning the disc.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="da030-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="da030-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="da030-122">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="da030-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="da030-123">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="da030-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da030-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da030-124">Return Value</span></span>

<span data-ttu-id="da030-125">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="da030-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="da030-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="da030-126">Examples</span></span>

<span data-ttu-id="da030-127">La commande suivante démarre un appareil videodisc.</span><span class="sxs-lookup"><span data-stu-id="da030-127">The following command starts spinning a videodisc device.</span></span>

``` syntax
spin videodisc up
```

## <a name="requirements"></a><span data-ttu-id="da030-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da030-128">Requirements</span></span>



| <span data-ttu-id="da030-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da030-129">Requirement</span></span> | <span data-ttu-id="da030-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="da030-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="da030-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da030-131">Minimum supported client</span></span><br/> | <span data-ttu-id="da030-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da030-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="da030-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da030-133">Minimum supported server</span></span><br/> | <span data-ttu-id="da030-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da030-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="da030-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da030-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da030-136">MCI</span><span class="sxs-lookup"><span data-stu-id="da030-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="da030-137">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="da030-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

