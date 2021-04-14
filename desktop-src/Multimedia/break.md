---
title: Break, commande
description: La commande Break spécifie une clé pour abandonner une commande qui a été appelée à l’aide de \ 0034 ; Wait \ 0034 ; activé. Cette commande est une commande système MCI. elle est interprétée directement par MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- commande arrêter Windows multimédia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466786"
---
# <a name="break-command"></a><span data-ttu-id="4f4d5-105">Break, commande</span><span class="sxs-lookup"><span data-stu-id="4f4d5-105">break command</span></span>

<span data-ttu-id="4f4d5-106">La commande Break spécifie une clé pour abandonner une commande qui a été appelée à l’aide de l’indicateur « WAIT ».</span><span class="sxs-lookup"><span data-stu-id="4f4d5-106">The break command specifies a key to abort a command that was invoked using the "wait" flag.</span></span> <span data-ttu-id="4f4d5-107">Cette commande est une commande système MCI. elle est interprétée directement par MCI.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-107">This command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="4f4d5-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4f4d5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f4d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f4d5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4f4d5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4f4d5-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4f4d5-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4f4d5-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span><span class="sxs-lookup"><span data-stu-id="4f4d5-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span></span>
</dt> <dd>

<span data-ttu-id="4f4d5-114">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-114">One of the following flags.</span></span>



| <span data-ttu-id="4f4d5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f4d5-115">Value</span></span>                 | <span data-ttu-id="4f4d5-116">Signification</span><span class="sxs-lookup"><span data-stu-id="4f4d5-116">Meaning</span></span>                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4f4d5-117">sur le *Code de touche virtuelle*</span><span class="sxs-lookup"><span data-stu-id="4f4d5-117">on *virtual key code*</span></span> | <span data-ttu-id="4f4d5-118">Spécifie la clé qui abandonne une commande qui a été démarrée à l’aide de l’indicateur « WAIT ».</span><span class="sxs-lookup"><span data-stu-id="4f4d5-118">Specifies the key that aborts a command that was started using the "wait" flag.</span></span> |
| <span data-ttu-id="4f4d5-119">arrêt</span><span class="sxs-lookup"><span data-stu-id="4f4d5-119">off</span></span>                   | <span data-ttu-id="4f4d5-120">Désactive la clé d’arrêt actuelle.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-120">Disables the current break key.</span></span>                                                 |



 

</dd> <dt>

<span data-ttu-id="4f4d5-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="4f4d5-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4f4d5-122">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4f4d5-123">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="4f4d5-123">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4f4d5-124">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4f4d5-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f4d5-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f4d5-125">Return Value</span></span>

<span data-ttu-id="4f4d5-126">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f4d5-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4f4d5-127">Remarks</span></span>

<span data-ttu-id="4f4d5-128">Lorsque la touche arrêt est activée et que l’utilisateur appuie sur la touche identifiée par le code de la touche virtuelle spécifiée dans le paramètre *lpszVirtKey* , l’appareil renvoie le contrôle à l’application.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-128">When the break key is enabled and the user presses the key identified by the virtual-key code specified in the *lpszVirtKey* parameter, the device returns control to the application.</span></span> <span data-ttu-id="4f4d5-129">Si possible, la commande continue l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-129">If possible, the command continues execution.</span></span>

## <a name="examples"></a><span data-ttu-id="4f4d5-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="4f4d5-130">Examples</span></span>

<span data-ttu-id="4f4d5-131">La commande suivante définit F2 comme clé d’arrêt pour l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="4f4d5-131">The following command sets F2 as the break key for the "mysound" device.</span></span>

``` syntax
break mysound on 113
```

## <a name="requirements"></a><span data-ttu-id="4f4d5-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f4d5-132">Requirements</span></span>



| <span data-ttu-id="4f4d5-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f4d5-133">Requirement</span></span> | <span data-ttu-id="4f4d5-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f4d5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4f4d5-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f4d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4d5-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f4d5-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4f4d5-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f4d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4d5-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f4d5-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4f4d5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f4d5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4d5-140">MCI</span><span class="sxs-lookup"><span data-stu-id="4f4d5-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4f4d5-141">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="4f4d5-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

