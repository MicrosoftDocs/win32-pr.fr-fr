---
title: configurer la commande
description: La commande configurer affiche une boîte de dialogue qui permet de configurer l’appareil. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 17d99992-f432-4b8a-ae98-2a70637c29c3
keywords:
- commande configurer Windows Multimedia
topic_type:
- apiref
api_name:
- configure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f131159d389577e3c717e5630633bb46558d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739837"
---
# <a name="configure-command"></a><span data-ttu-id="a8b5c-105">configurer la commande</span><span class="sxs-lookup"><span data-stu-id="a8b5c-105">configure command</span></span>

<span data-ttu-id="a8b5c-106">La commande configurer affiche une boîte de dialogue qui permet de configurer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-106">The configure command displays a dialog box used to configure the device.</span></span> <span data-ttu-id="a8b5c-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="a8b5c-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("configure %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a8b5c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8b5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b5c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a8b5c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a8b5c-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a8b5c-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5c-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a8b5c-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a8b5c-114">Peut être « Wait », « Notify » ou « test ».</span><span class="sxs-lookup"><span data-stu-id="a8b5c-114">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="a8b5c-115">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a8b5c-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b5c-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8b5c-116">Return Value</span></span>

<span data-ttu-id="a8b5c-117">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b5c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8b5c-118">Requirements</span></span>



| <span data-ttu-id="a8b5c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8b5c-119">Requirement</span></span> | <span data-ttu-id="a8b5c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8b5c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a8b5c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8b5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b5c-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8b5c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8b5c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8b5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b5c-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8b5c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a8b5c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8b5c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b5c-126">MCI</span><span class="sxs-lookup"><span data-stu-id="a8b5c-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a8b5c-127">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="a8b5c-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

