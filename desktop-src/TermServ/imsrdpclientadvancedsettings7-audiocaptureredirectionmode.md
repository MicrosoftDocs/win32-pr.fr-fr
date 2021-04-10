---
title: IMsRdpClientAdvancedSettings7 propriété AudioCaptureRedirectionMode
description: Spécifie ou récupère une valeur booléenne qui indique si le périphérique d’entrée audio par défaut est redirigé du client vers la session à distance.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AudioCaptureRedirectionMode
- Services Bureau à distance de la propriété AudioCaptureRedirectionMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AudioCaptureRedirectionMode
- Services Bureau à distance de la propriété AudioCaptureRedirectionMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AudioCaptureRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c752315067ed70103da2e048e9e8f613665ae919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942334"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a><span data-ttu-id="4e6fd-108">IMsRdpClientAdvancedSettings7 :: AudioCaptureRedirectionMode, propriété</span><span class="sxs-lookup"><span data-stu-id="4e6fd-108">IMsRdpClientAdvancedSettings7::AudioCaptureRedirectionMode property</span></span>

<span data-ttu-id="4e6fd-109">Spécifie ou récupère une valeur booléenne qui indique si le périphérique d’entrée audio par défaut est redirigé du client vers la session à distance.</span><span class="sxs-lookup"><span data-stu-id="4e6fd-109">Specifies or retrieves a Boolean value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span>

<span data-ttu-id="4e6fd-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4e6fd-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6fd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e6fd-111">Syntax</span></span>


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a><span data-ttu-id="4e6fd-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4e6fd-112">Property value</span></span>

<span data-ttu-id="4e6fd-113">Valeur **\_ booléenne variant** qui spécifie si la capture audio est redirigée.</span><span class="sxs-lookup"><span data-stu-id="4e6fd-113">A **VARIANT\_BOOL** value that specifies whether audio capture is redirected.</span></span> <span data-ttu-id="4e6fd-114">Spécifiez la **\_ valeur variant true** si vous souhaitez rediriger la capture audio.</span><span class="sxs-lookup"><span data-stu-id="4e6fd-114">Specify **VARIANT\_TRUE** if you want audio capture to be redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e6fd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e6fd-115">Requirements</span></span>



| <span data-ttu-id="4e6fd-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e6fd-116">Requirement</span></span> | <span data-ttu-id="4e6fd-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e6fd-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6fd-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e6fd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4e6fd-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e6fd-119">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="4e6fd-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e6fd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4e6fd-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4e6fd-121">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="4e6fd-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4e6fd-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e6fd-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fd-123"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4e6fd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4e6fd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e6fd-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fd-125"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4e6fd-126">IID</span><span class="sxs-lookup"><span data-stu-id="4e6fd-126">IID</span></span><br/>                      | <span data-ttu-id="4e6fd-127">IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="4e6fd-127">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e6fd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e6fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e6fd-129">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4e6fd-129">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4e6fd-130">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4e6fd-130">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





