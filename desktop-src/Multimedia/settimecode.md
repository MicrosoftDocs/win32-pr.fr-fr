---
title: commande settimecode
description: La commande settimecode active ou désactive l’enregistrement du code temporel pour un magnétoscope. Les périphériques VCR reconnaissent cette commande.
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- commande settimecode multimédia Windows
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32092e5af7c77cdc274491b20663218d39a1ec1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743901"
---
# <a name="settimecode-command"></a><span data-ttu-id="0ae1a-105">commande settimecode</span><span class="sxs-lookup"><span data-stu-id="0ae1a-105">settimecode command</span></span>

<span data-ttu-id="0ae1a-106">La commande settimecode active ou désactive l’enregistrement du code temporel pour un magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-106">The settimecode command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="0ae1a-107">Les périphériques VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="0ae1a-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0ae1a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ae1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ae1a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0ae1a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0ae1a-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0ae1a-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0ae1a-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span><span class="sxs-lookup"><span data-stu-id="0ae1a-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span></span>
</dt> <dd>

<span data-ttu-id="0ae1a-114">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-114">One of the following flags.</span></span>



| <span data-ttu-id="0ae1a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ae1a-115">Value</span></span>      | <span data-ttu-id="0ae1a-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0ae1a-116">Meaning</span></span>                          |
|------------|----------------------------------|
| <span data-ttu-id="0ae1a-117">enregistrer sur</span><span class="sxs-lookup"><span data-stu-id="0ae1a-117">record on</span></span>  | <span data-ttu-id="0ae1a-118">Définit le magnétoscope pour enregistrer le code temporel.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-118">Sets the VCR to record timecode.</span></span> |
| <span data-ttu-id="0ae1a-119">enregistrement désactivé</span><span class="sxs-lookup"><span data-stu-id="0ae1a-119">record off</span></span> | <span data-ttu-id="0ae1a-120">Désactive l’enregistrement du code temporel.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-120">Disables timecode recording.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="0ae1a-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0ae1a-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0ae1a-122">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-122">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="0ae1a-123">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0ae1a-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ae1a-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0ae1a-124">Return Value</span></span>

<span data-ttu-id="0ae1a-125">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="0ae1a-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ae1a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ae1a-126">Requirements</span></span>



| <span data-ttu-id="0ae1a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ae1a-127">Requirement</span></span> | <span data-ttu-id="0ae1a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ae1a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0ae1a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ae1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0ae1a-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ae1a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0ae1a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ae1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0ae1a-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ae1a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0ae1a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ae1a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae1a-134">MCI</span><span class="sxs-lookup"><span data-stu-id="0ae1a-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0ae1a-135">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="0ae1a-135">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

