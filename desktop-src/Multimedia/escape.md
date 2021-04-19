---
title: Escape, commande
description: La commande Escape envoie des informations spécifiques à l’appareil à un appareil. Les appareils Videodisc reconnaissent cette commande.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- commande d’échappement Windows multimédia
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510113"
---
# <a name="escape-command"></a><span data-ttu-id="e6107-105">Escape, commande</span><span class="sxs-lookup"><span data-stu-id="e6107-105">escape command</span></span>

<span data-ttu-id="e6107-106">La commande Escape envoie des informations spécifiques à l’appareil à un appareil.</span><span class="sxs-lookup"><span data-stu-id="e6107-106">The escape command sends device-specific information to a device.</span></span> <span data-ttu-id="e6107-107">Les appareils Videodisc reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="e6107-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="e6107-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="e6107-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e6107-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6107-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6107-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e6107-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e6107-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="e6107-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e6107-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e6107-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e6107-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span><span class="sxs-lookup"><span data-stu-id="e6107-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span></span>
</dt> <dd>

<span data-ttu-id="e6107-114">Informations personnalisées à envoyer à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e6107-114">Custom information to send to the device.</span></span>

</dd> <dt>

<span data-ttu-id="e6107-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e6107-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e6107-116">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e6107-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e6107-117">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e6107-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6107-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6107-118">Return Value</span></span>

<span data-ttu-id="e6107-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="e6107-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="e6107-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="e6107-120">Examples</span></span>

<span data-ttu-id="e6107-121">La commande suivante envoie la chaîne d’échappement « SA » à l’appareil videodisc.</span><span class="sxs-lookup"><span data-stu-id="e6107-121">The following command sends the escape string "SA" to the videodisc device.</span></span>

``` syntax
escape videodisc SA
```

## <a name="requirements"></a><span data-ttu-id="e6107-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6107-122">Requirements</span></span>



| <span data-ttu-id="e6107-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6107-123">Requirement</span></span> | <span data-ttu-id="e6107-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6107-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e6107-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6107-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e6107-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6107-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e6107-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6107-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e6107-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6107-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e6107-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6107-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6107-130">MCI</span><span class="sxs-lookup"><span data-stu-id="e6107-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e6107-131">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="e6107-131">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

