---
title: commande de réalisation
description: La commande de réalisation indique à un appareil de sélectionner et de réaliser sa palette dans le contexte d’affichage de la fenêtre affichée. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- Réalisez une commande multimédia Windows
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942688"
---
# <a name="realize-command"></a><span data-ttu-id="e6625-105">commande de réalisation</span><span class="sxs-lookup"><span data-stu-id="e6625-105">realize command</span></span>

<span data-ttu-id="e6625-106">La commande de réalisation indique à un appareil de sélectionner et de réaliser sa palette dans le contexte d’affichage de la fenêtre affichée.</span><span class="sxs-lookup"><span data-stu-id="e6625-106">The realize command instructs a device to select and realize its palette into the display context of the displayed window.</span></span> <span data-ttu-id="e6625-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="e6625-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="e6625-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="e6625-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e6625-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6625-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6625-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e6625-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e6625-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="e6625-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e6625-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e6625-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e6625-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span><span class="sxs-lookup"><span data-stu-id="e6625-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span></span>
</dt> <dd>

<span data-ttu-id="e6625-114">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="e6625-114">One of the following flags.</span></span>



| <span data-ttu-id="e6625-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6625-115">Value</span></span>      | <span data-ttu-id="e6625-116">Signification</span><span class="sxs-lookup"><span data-stu-id="e6625-116">Meaning</span></span>                                                                   |
|------------|---------------------------------------------------------------------------|
| <span data-ttu-id="e6625-117">background</span><span class="sxs-lookup"><span data-stu-id="e6625-117">background</span></span> | <span data-ttu-id="e6625-118">Réalise la palette sous forme de palette d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e6625-118">Realizes the palette as a background palette.</span></span>                             |
| <span data-ttu-id="e6625-119">normal</span><span class="sxs-lookup"><span data-stu-id="e6625-119">normal</span></span>     | <span data-ttu-id="e6625-120">Réalise la palette pour une fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="e6625-120">Realizes the palette for a top-level window.</span></span> <span data-ttu-id="e6625-121">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="e6625-121">This is the default setting.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e6625-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e6625-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e6625-123">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e6625-123">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e6625-124">Pour les appareils vidéo numériques, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="e6625-124">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="e6625-125">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e6625-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6625-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6625-126">Return Value</span></span>

<span data-ttu-id="e6625-127">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="e6625-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6625-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e6625-128">Remarks</span></span>

<span data-ttu-id="e6625-129">Utilisez cette commande uniquement si votre application utilise un handle de fenêtre et reçoit un message **WM \_ QUERYNEWPALLETTE** ou **WM \_ PALETTECHANGED** .</span><span class="sxs-lookup"><span data-stu-id="e6625-129">Use this command only if your application uses a window handle and receives a **WM\_QUERYNEWPALLETTE** or **WM\_PALETTECHANGED** message.</span></span>

## <a name="examples"></a><span data-ttu-id="e6625-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="e6625-130">Examples</span></span>

<span data-ttu-id="e6625-131">La commande suivante indique à l’appareil « MyVideo » de réaliser sa palette.</span><span class="sxs-lookup"><span data-stu-id="e6625-131">The following command tells the "myvideo" device to realize its palette.</span></span>

``` syntax
realize myvideo normal
```

## <a name="requirements"></a><span data-ttu-id="e6625-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6625-132">Requirements</span></span>



| <span data-ttu-id="e6625-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6625-133">Requirement</span></span> | <span data-ttu-id="e6625-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6625-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e6625-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6625-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e6625-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6625-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e6625-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6625-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e6625-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6625-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e6625-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6625-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6625-140">MCI</span><span class="sxs-lookup"><span data-stu-id="e6625-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e6625-141">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="e6625-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

