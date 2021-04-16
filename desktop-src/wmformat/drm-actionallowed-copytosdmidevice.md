---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: L' \_ attribut DRM ActionAllowed \_ CopyToSDMIDevice indique si le contenu peut être copié sur un appareil SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- Format Windows Media DRM_ActionAllowed_CopyToSDMIDevice
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381458"
---
# <a name="drm_actionallowed_copytosdmidevice"></a><span data-ttu-id="75fd4-104">\_ACTIONALLOWED DRM \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="75fd4-104">DRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

<span data-ttu-id="75fd4-105">L’attribut **DRM \_ ActionAllowed \_ CopyToSDMIDevice** indique si le contenu peut être copié sur un appareil SDMI.</span><span class="sxs-lookup"><span data-stu-id="75fd4-105">The **DRM\_ActionAllowed\_CopyToSDMIDevice** attribute indicates whether the content is allowed to be copied to an SDMI device.</span></span>

## <a name="global-constant"></a><span data-ttu-id="75fd4-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="75fd4-106">Global Constant</span></span>

<span data-ttu-id="75fd4-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="75fd4-107">g\_wszWMDRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="75fd4-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="75fd4-108">Data Type</span></span>

<span data-ttu-id="75fd4-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="75fd4-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="75fd4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="75fd4-110">Remarks</span></span>

<span data-ttu-id="75fd4-111">Les licences Windows Media DRM 10 utilisent l’action de copie pour limiter la copie sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="75fd4-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="75fd4-112">Vous devez vérifier la propriété de [**\_ \_ copie DRM ActionAllowed**](drm-actionallowed-copy.md) pour déterminer si la copie est autorisée.</span><span class="sxs-lookup"><span data-stu-id="75fd4-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="75fd4-113">Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="75fd4-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="75fd4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75fd4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75fd4-115">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="75fd4-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




