---
title: IMsRdpClientAdvancedSettings7 propriété VideoPlaybackMode
description: Spécifie ou récupère une valeur qui indique le mode de lecture vidéo.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété VideoPlaybackMode
- Services Bureau à distance de la propriété VideoPlaybackMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété VideoPlaybackMode
- Services Bureau à distance de la propriété VideoPlaybackMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385287"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a><span data-ttu-id="98046-108">IMsRdpClientAdvancedSettings7 :: VideoPlaybackMode, propriété</span><span class="sxs-lookup"><span data-stu-id="98046-108">IMsRdpClientAdvancedSettings7::VideoPlaybackMode property</span></span>

<span data-ttu-id="98046-109">Spécifie ou récupère une valeur qui indique le mode de lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="98046-109">Specifies or retrieves a value that indicates the video playback mode.</span></span>

<span data-ttu-id="98046-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="98046-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98046-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98046-111">Syntax</span></span>


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a><span data-ttu-id="98046-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="98046-112">Property value</span></span>

<span data-ttu-id="98046-113">Valeur qui spécifie le mode de lecture de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="98046-113">A value that specifies the video playback mode.</span></span>

<span data-ttu-id="98046-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98046-114">The possible values are:</span></span>

<dt>

<span data-ttu-id="98046-115">1</span><span class="sxs-lookup"><span data-stu-id="98046-115">1</span></span>
</dt> <dd>

<span data-ttu-id="98046-116">Mode de lecture vidéo par défaut.</span><span class="sxs-lookup"><span data-stu-id="98046-116">The default video playback mode.</span></span> <span data-ttu-id="98046-117">Lorsque le mode de lecture vidéo est défini sur cette valeur, la redirection vidéo est contrôlée par la propriété [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) .</span><span class="sxs-lookup"><span data-stu-id="98046-117">When the video playback mode is set to this value, video redirection is controlled by the [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) property.</span></span> <span data-ttu-id="98046-118">Lorsque la propriété **AudioRedirectionMode** est définie sur **\_ \_ redirect mode audio**, la vidéo est décodée et rendue sur le client.</span><span class="sxs-lookup"><span data-stu-id="98046-118">When the **AudioRedirectionMode** property is set to **AUDIO\_MODE\_REDIRECT**, video is decoded and rendered on the client.</span></span>

</dd> <dt>

<span data-ttu-id="98046-119">0</span><span class="sxs-lookup"><span data-stu-id="98046-119">0</span></span>
</dt> <dd>

<span data-ttu-id="98046-120">La redirection de lecture vidéo est désactivée, même si [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) est défini sur **\_ \_ redirection audio mode**.</span><span class="sxs-lookup"><span data-stu-id="98046-120">Video playback redirection is disabled, even when [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) is set to **AUDIO\_MODE\_REDIRECT**.</span></span> <span data-ttu-id="98046-121">Dans ce mode, la vidéo est décodée et rendue sur le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="98046-121">In this mode, video is decoded and rendered on the RD Session Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98046-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98046-122">Requirements</span></span>



| <span data-ttu-id="98046-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98046-123">Requirement</span></span> | <span data-ttu-id="98046-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="98046-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98046-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98046-125">Minimum supported client</span></span><br/> | <span data-ttu-id="98046-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="98046-126">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="98046-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98046-127">Minimum supported server</span></span><br/> | <span data-ttu-id="98046-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="98046-128">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="98046-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="98046-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="98046-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98046-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="98046-131">DLL</span><span class="sxs-lookup"><span data-stu-id="98046-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98046-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98046-132"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="98046-133">IID</span><span class="sxs-lookup"><span data-stu-id="98046-133">IID</span></span><br/>                      | <span data-ttu-id="98046-134">IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="98046-134">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98046-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98046-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98046-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="98046-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="98046-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="98046-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





