---
title: IMsRdpClientAdvancedSettings5 propriété AudioRedirectionMode
description: Définit et récupère le mode de redirection audio et les différentes options de redirection audio.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AudioRedirectionMode
- Services Bureau à distance de la propriété AudioRedirectionMode, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété AudioRedirectionMode
- Services Bureau à distance de la propriété AudioRedirectionMode, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété AudioRedirectionMode
- Services Bureau à distance de la propriété AudioRedirectionMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AudioRedirectionMode
- Services Bureau à distance de la propriété AudioRedirectionMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40be8b8e63f210d060c0f585c9fe31328ac6ed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317186"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a><span data-ttu-id="bcbba-112">IMsRdpClientAdvancedSettings5 :: AudioRedirectionMode, propriété</span><span class="sxs-lookup"><span data-stu-id="bcbba-112">IMsRdpClientAdvancedSettings5::AudioRedirectionMode property</span></span>

<span data-ttu-id="bcbba-113">Définit et récupère le mode de redirection audio et les différentes options de redirection audio.</span><span class="sxs-lookup"><span data-stu-id="bcbba-113">Sets and retrieves the audio redirection mode and different audio redirection options.</span></span>

<span data-ttu-id="bcbba-114">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bcbba-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbba-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcbba-115">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="bcbba-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bcbba-116">Property value</span></span>

<span data-ttu-id="bcbba-117">Définit des valeurs différentes pour le mode de redirection audio.</span><span class="sxs-lookup"><span data-stu-id="bcbba-117">Sets different values for the audio redirection mode.</span></span> <span data-ttu-id="bcbba-118">Ce paramètre a les valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="bcbba-118">This parameter has the following possible values.</span></span>

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

<span data-ttu-id="bcbba-119">**Audio \_ Redirection de MODE \_ 0** (la redirection audio est activée et l’option de redirection est « apporter à cet ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="bcbba-119">**AUDIO\_MODE\_REDIRECT 0** (Audio redirection is enabled and the option for redirection is "Bring to this computer".</span></span> <span data-ttu-id="bcbba-120">Il s’agit du mode par défaut.)</span><span class="sxs-lookup"><span data-stu-id="bcbba-120">This is the default mode.)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

<span data-ttu-id="bcbba-121">**Audio \_ Lecture en MODE \_ \_ sur le \_ serveur 1** (la redirection audio est activée et l’option est « conserver sur l’ordinateur distant ».</span><span class="sxs-lookup"><span data-stu-id="bcbba-121">**AUDIO\_MODE\_PLAY\_ON\_SERVER 1** (Audio redirection is enabled and the option is "Leave at remote computer".</span></span> <span data-ttu-id="bcbba-122">L’option « conserver sur l’ordinateur distant » est prise en charge uniquement lors de la connexion à distance à un ordinateur hôte qui exécute Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bcbba-122">The "Leave at remote computer" option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="bcbba-123">Si la connexion est vers un ordinateur hôte qui exécute Windows Server 2008, l’option « conserver sur l’ordinateur distant » est remplacée par « ne pas lire ».)</span><span class="sxs-lookup"><span data-stu-id="bcbba-123">If the connection is to a host computer that is running Windows Server 2008, the option "Leave at remote computer" is changed to "Do not play".)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

<span data-ttu-id="bcbba-124">**Audio \_ MODE \_ aucun 2** (la redirection audio est activée et le mode est « ne pas lire ».)</span><span class="sxs-lookup"><span data-stu-id="bcbba-124">**AUDIO\_MODE\_NONE 2** (Audio redirection is enabled and the mode is "Do not play".)</span></span>


<span data-ttu-id="bcbba-125"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bcbba-125"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bcbba-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcbba-126">Requirements</span></span>



| <span data-ttu-id="bcbba-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcbba-127">Requirement</span></span> | <span data-ttu-id="bcbba-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcbba-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbba-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcbba-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbba-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcbba-130">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bcbba-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcbba-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbba-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcbba-132">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bcbba-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bcbba-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcbba-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcbba-134"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bcbba-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bcbba-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcbba-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcbba-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bcbba-137">IID</span><span class="sxs-lookup"><span data-stu-id="bcbba-137">IID</span></span><br/>                      | <span data-ttu-id="bcbba-138">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="bcbba-138">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcbba-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcbba-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbba-140">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bcbba-140">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bcbba-141">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bcbba-141">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bcbba-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bcbba-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bcbba-143">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bcbba-143">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





