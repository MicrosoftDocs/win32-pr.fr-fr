---
title: commande sysinfo
description: La commande sysinfo récupère les informations système de MCI. La commande sysinfo est une commande système MCI. elle est interprétée directement par MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- commande sysinfo Windows multimédia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516499"
---
# <a name="sysinfo-command"></a><span data-ttu-id="02e57-105">commande sysinfo</span><span class="sxs-lookup"><span data-stu-id="02e57-105">sysinfo command</span></span>

<span data-ttu-id="02e57-106">La commande sysinfo récupère les informations système de MCI.</span><span class="sxs-lookup"><span data-stu-id="02e57-106">The sysinfo command retrieves MCI system information.</span></span> <span data-ttu-id="02e57-107">La commande sysinfo est une commande système MCI. elle est interprétée directement par MCI.</span><span class="sxs-lookup"><span data-stu-id="02e57-107">The sysinfo command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="02e57-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="02e57-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a><span data-ttu-id="02e57-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02e57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e57-110">*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="02e57-110">*lpszDeviceID*</span></span> 
</dt> <dd>

<span data-ttu-id="02e57-111">Identificateur d’un type d’appareil ou d’appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="02e57-111">Identifier of an MCI device or device type.</span></span> <span data-ttu-id="02e57-112">Si un type d’appareil est spécifié, il doit s’agir d’un nom de type d’appareil MCI standard, tel qu’indiqué dans la documentation de référence de la commande [**Capability**](capability.md) .</span><span class="sxs-lookup"><span data-stu-id="02e57-112">If a device type is specified, it must be a standard MCI device-type name, as listed in the reference material for the [**capability**](capability.md) command.</span></span> <span data-ttu-id="02e57-113">Vous pouvez spécifier « All » lorsque l’indicateur spécifié dans *lpszRequest* autorise cette possibilité.</span><span class="sxs-lookup"><span data-stu-id="02e57-113">You can specify "all" when the flag specified in *lpszRequest* allows that possibility.</span></span>

</dd> <dt>

<span data-ttu-id="02e57-114">*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="02e57-114">*lpszRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="02e57-115">Un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="02e57-115">One of the following flags.</span></span>



| <span data-ttu-id="02e57-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="02e57-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="02e57-117">Signification</span><span class="sxs-lookup"><span data-stu-id="02e57-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <span data-ttu-id="02e57-118"><dt>**installname**</dt></span><span class="sxs-lookup"><span data-stu-id="02e57-118"><dt>**installname**</dt></span></span> </dl>               | <span data-ttu-id="02e57-119">Retourne le nom indiqué dans le registre ou le fichier SYSTEM.INI utilisé pour installer l’appareil ouvert avec l’identificateur de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="02e57-119">Returns the name listed in the registry or the SYSTEM.INI file used to install the open device with the specified device identifier.</span></span><br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <span data-ttu-id="02e57-120"><dt>**spécifiée**</dt></span><span class="sxs-lookup"><span data-stu-id="02e57-120"><dt>**quantity**</dt></span></span> </dl>                        | <span data-ttu-id="02e57-121">Retourne le nombre de périphériques MCI listés dans le registre ou le fichier SYSTEM.INI du type spécifié dans le paramètre *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="02e57-121">Returns the number of MCI devices listed in the registry or the SYSTEM.INI file of the type specified in the *lpszDeviceID* parameter.</span></span> <span data-ttu-id="02e57-122">Cet identificateur de périphérique doit être un nom de type d’appareil MCI standard.</span><span class="sxs-lookup"><span data-stu-id="02e57-122">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="02e57-123">Tous les chiffres après le type d’appareil sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="02e57-123">Any digits after the device type are ignored.</span></span> <span data-ttu-id="02e57-124">La spécification de « All » pour *lpszDeviceID* retourne le nombre total de périphériques MCI dans le système.</span><span class="sxs-lookup"><span data-stu-id="02e57-124">Specifying "all" for *lpszDeviceID* returns the total number of MCI devices in the system.</span></span><br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <span data-ttu-id="02e57-125"><dt>**quantité ouverte**</dt></span><span class="sxs-lookup"><span data-stu-id="02e57-125"><dt>**quantity open**</dt></span></span> </dl>         | <span data-ttu-id="02e57-126">Retourne le nombre d’appareils MCI ouverts du type spécifié dans *lpszDeviceID*.</span><span class="sxs-lookup"><span data-stu-id="02e57-126">Returns the number of open MCI devices of the type specified in *lpszDeviceID*.</span></span> <span data-ttu-id="02e57-127">Cet identificateur de périphérique doit être un nom de type d’appareil MCI standard.</span><span class="sxs-lookup"><span data-stu-id="02e57-127">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="02e57-128">Si vous spécifiez « All » pour *lpszDeviceID* , le nombre total d’appareils MCI ouverts dans le système est retourné.</span><span class="sxs-lookup"><span data-stu-id="02e57-128">Specifying "all" for *lpszDeviceID* returns the total number of open MCI devices in the system.</span></span><br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <span data-ttu-id="02e57-129"><dt>\* \* nom \* index \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="02e57-129"><dt>\*\*name \*index\*\*\*</dt></span></span> </dl>                | <span data-ttu-id="02e57-130">Retourne le nom d’un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="02e57-130">Returns the name of an MCI device.</span></span> <span data-ttu-id="02e57-131">L’identificateur d’appareil doit être un nom de type d’appareil MCI standard.</span><span class="sxs-lookup"><span data-stu-id="02e57-131">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="02e57-132">L' *index* est compris entre 1 et le nombre d’appareils de ce type.</span><span class="sxs-lookup"><span data-stu-id="02e57-132">The *index* ranges from 1 to the number of devices of that type.</span></span> <span data-ttu-id="02e57-133">Si « ALL » est spécifié pour *lpszDeviceID*, *index* est compris entre 1 et le nombre total d’appareils dans le système.</span><span class="sxs-lookup"><span data-stu-id="02e57-133">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of devices in the system.</span></span><br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <span data-ttu-id="02e57-134"><dt>***index* de nom ouvert**</dt></span><span class="sxs-lookup"><span data-stu-id="02e57-134"><dt>**name *index* open**</dt></span></span> </dl> | <span data-ttu-id="02e57-135">Retourne le nom d’un périphérique MCI ouvert.</span><span class="sxs-lookup"><span data-stu-id="02e57-135">Returns the name of an open MCI device.</span></span> <span data-ttu-id="02e57-136">L’identificateur d’appareil doit être un nom de type d’appareil MCI standard.</span><span class="sxs-lookup"><span data-stu-id="02e57-136">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="02e57-137">L' *index* est compris entre 1 et le nombre d’appareils ouverts de ce type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="02e57-137">The *index* ranges from 1 to the number of open devices of that device type.</span></span> <span data-ttu-id="02e57-138">Si « ALL » est spécifié pour *lpszDeviceID*, *index* est compris entre 1 et le nombre total d’appareils ouverts dans le système.</span><span class="sxs-lookup"><span data-stu-id="02e57-138">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of open devices in the system.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="02e57-139">*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="02e57-139">*lpszFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="02e57-140">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="02e57-140">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="02e57-141">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="02e57-141">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="02e57-142">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="02e57-142">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="02e57-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="02e57-143">Examples</span></span>

<span data-ttu-id="02e57-144">La commande suivante retourne le nombre de périphériques audio Wave ouverts.</span><span class="sxs-lookup"><span data-stu-id="02e57-144">The following command returns the number of open waveform-audio devices.</span></span>

``` syntax
sysinfo waveaudio quantity open
```

<span data-ttu-id="02e57-145">La commande suivante renvoie le nom (l’alias d’appareil) du premier périphérique Wave-Audio ouvert.</span><span class="sxs-lookup"><span data-stu-id="02e57-145">The following command returns the name (device alias) of the first open waveform-audio device.</span></span>

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a><span data-ttu-id="02e57-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02e57-146">Requirements</span></span>



| <span data-ttu-id="02e57-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02e57-147">Requirement</span></span> | <span data-ttu-id="02e57-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="02e57-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="02e57-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02e57-149">Minimum supported client</span></span><br/> | <span data-ttu-id="02e57-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02e57-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02e57-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02e57-151">Minimum supported server</span></span><br/> | <span data-ttu-id="02e57-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02e57-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="02e57-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02e57-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e57-154">MCI</span><span class="sxs-lookup"><span data-stu-id="02e57-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="02e57-155">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="02e57-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="02e57-156">**Faculté**</span><span class="sxs-lookup"><span data-stu-id="02e57-156">**capability**</span></span>](capability.md)
</dt> </dl>

 

