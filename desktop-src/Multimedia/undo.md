---
title: commande Undo
description: La commande Annuler annule l’action effectuée par la commande de copie, de suppression, d’annulation ou de collage réussie la plus récente. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- commande Annuler Windows Multimedia
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033225"
---
# <a name="undo-command"></a><span data-ttu-id="d967a-105">commande Undo</span><span class="sxs-lookup"><span data-stu-id="d967a-105">undo command</span></span>

<span data-ttu-id="d967a-106">La commande Annuler annule l’action effectuée par la commande de [copie](copy.md), de [suppression](delete.md) [, d'](cut.md)annulation ou de [Collage](paste.md) réussie la plus récente.</span><span class="sxs-lookup"><span data-stu-id="d967a-106">The undo command reverses the action taken by the most recent successful [copy](copy.md), [cut](cut.md), [delete](delete.md), undo, or [paste](paste.md) command.</span></span> <span data-ttu-id="d967a-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="d967a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d967a-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="d967a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d967a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d967a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d967a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d967a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d967a-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="d967a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d967a-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d967a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d967a-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d967a-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d967a-114">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="d967a-114">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="d967a-115">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d967a-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d967a-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d967a-116">Return Value</span></span>

<span data-ttu-id="d967a-117">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d967a-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d967a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d967a-118">Requirements</span></span>



| <span data-ttu-id="d967a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d967a-119">Requirement</span></span> | <span data-ttu-id="d967a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d967a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d967a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d967a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d967a-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d967a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d967a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d967a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d967a-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d967a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d967a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d967a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d967a-126">MCI</span><span class="sxs-lookup"><span data-stu-id="d967a-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d967a-127">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="d967a-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d967a-128">copy</span><span class="sxs-lookup"><span data-stu-id="d967a-128">copy</span></span>](copy.md)
</dt> <dt>

[<span data-ttu-id="d967a-129">réduis</span><span class="sxs-lookup"><span data-stu-id="d967a-129">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="d967a-130">delete</span><span class="sxs-lookup"><span data-stu-id="d967a-130">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="d967a-131">coller</span><span class="sxs-lookup"><span data-stu-id="d967a-131">paste</span></span>](paste.md)
</dt> </dl>

 

