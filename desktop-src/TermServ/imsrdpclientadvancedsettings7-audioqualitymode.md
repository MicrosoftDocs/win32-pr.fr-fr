---
title: IMsRdpClientAdvancedSettings7 propriété AudioQualityMode
description: Spécifie ou récupère une valeur qui indique le paramètre de mode de qualité audio pour le son Redirigé. Par défaut, cette valeur est définie sur 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AudioQualityMode
- Services Bureau à distance de la propriété AudioQualityMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AudioQualityMode
- Services Bureau à distance de la propriété AudioQualityMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512815"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a><span data-ttu-id="591a9-109">IMsRdpClientAdvancedSettings7 :: AudioQualityMode, propriété</span><span class="sxs-lookup"><span data-stu-id="591a9-109">IMsRdpClientAdvancedSettings7::AudioQualityMode property</span></span>

<span data-ttu-id="591a9-110">Spécifie ou récupère une valeur qui indique le paramètre de mode de qualité audio pour le son Redirigé.</span><span class="sxs-lookup"><span data-stu-id="591a9-110">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span> <span data-ttu-id="591a9-111">Par défaut, cette valeur est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="591a9-111">By default this is set to 0.</span></span>

<span data-ttu-id="591a9-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="591a9-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="591a9-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="591a9-113">Syntax</span></span>


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a><span data-ttu-id="591a9-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="591a9-114">Property value</span></span>

<span data-ttu-id="591a9-115">Valeur qui spécifie le mode de qualité audio.</span><span class="sxs-lookup"><span data-stu-id="591a9-115">A value that specifies the audio quality mode.</span></span>

<span data-ttu-id="591a9-116">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="591a9-116">The possible values are:</span></span>

<dt>

<span data-ttu-id="591a9-117">0</span><span class="sxs-lookup"><span data-stu-id="591a9-117">0</span></span>
</dt> <dd>

<span data-ttu-id="591a9-118">Qualité audio dynamique.</span><span class="sxs-lookup"><span data-stu-id="591a9-118">Dynamic audio quality.</span></span> <span data-ttu-id="591a9-119">Il s’agit du paramètre de qualité audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="591a9-119">This is the default audio quality setting.</span></span> <span data-ttu-id="591a9-120">Le serveur ajuste de manière dynamique la qualité de sortie audio en réponse aux conditions du réseau et aux fonctionnalités du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="591a9-120">The server dynamically adjusts audio output quality in response to network conditions and the client and server capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="591a9-121">1</span><span class="sxs-lookup"><span data-stu-id="591a9-121">1</span></span>
</dt> <dd>

<span data-ttu-id="591a9-122">Qualité audio moyenne.</span><span class="sxs-lookup"><span data-stu-id="591a9-122">Medium audio quality.</span></span> <span data-ttu-id="591a9-123">Le serveur utilise un format fixe mais compressé pour la sortie audio.</span><span class="sxs-lookup"><span data-stu-id="591a9-123">The server uses a fixed but compressed format for audio output.</span></span>

</dd> <dt>

<span data-ttu-id="591a9-124">2</span><span class="sxs-lookup"><span data-stu-id="591a9-124">2</span></span>
</dt> <dd>

<span data-ttu-id="591a9-125">Haute qualité audio.</span><span class="sxs-lookup"><span data-stu-id="591a9-125">High audio quality.</span></span> <span data-ttu-id="591a9-126">Le serveur fournit une sortie audio au format PCM non compressé avec une charge de traitement inférieure pour la latence.</span><span class="sxs-lookup"><span data-stu-id="591a9-126">The server provides audio output in uncompressed PCM format with lower processing overhead for latency.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="591a9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="591a9-127">Requirements</span></span>



| <span data-ttu-id="591a9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="591a9-128">Requirement</span></span> | <span data-ttu-id="591a9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="591a9-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="591a9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="591a9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="591a9-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="591a9-131">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="591a9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="591a9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="591a9-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="591a9-133">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="591a9-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="591a9-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="591a9-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="591a9-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="591a9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="591a9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="591a9-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="591a9-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="591a9-138">IID</span><span class="sxs-lookup"><span data-stu-id="591a9-138">IID</span></span><br/>                      | <span data-ttu-id="591a9-139">IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="591a9-139">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="591a9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="591a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="591a9-141">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="591a9-141">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="591a9-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="591a9-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





