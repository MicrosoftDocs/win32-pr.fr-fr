---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: L' \_ attribut DRM ActionAllowed \_ CopyToNonSDMIDevice indique si le contenu peut être copié sur un appareil non-SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- Format Windows Media DRM_ActionAllowed_CopyToNonSDMIDevice
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030832"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a><span data-ttu-id="62390-104">\_ACTIONALLOWED DRM \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="62390-104">DRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

<span data-ttu-id="62390-105">L’attribut **DRM \_ ActionAllowed \_ CopyToNonSDMIDevice** indique si le contenu peut être copié sur un appareil non-SDMI</span><span class="sxs-lookup"><span data-stu-id="62390-105">The **DRM\_ActionAllowed\_CopyToNonSDMIDevice** attribute indicates whether the content is allowed to be copied to a non-SDMI device</span></span>

## <a name="global-constant"></a><span data-ttu-id="62390-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="62390-106">Global Constant</span></span>

<span data-ttu-id="62390-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="62390-107">g\_wszWMDRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="62390-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="62390-108">Data Type</span></span>

<span data-ttu-id="62390-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="62390-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="62390-110">Notes</span><span class="sxs-lookup"><span data-stu-id="62390-110">Remarks</span></span>

<span data-ttu-id="62390-111">Les licences Windows Media DRM 10 utilisent l’action de copie pour limiter la copie sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="62390-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="62390-112">Vous devez vérifier la propriété de [**\_ \_ copie DRM ActionAllowed**](drm-actionallowed-copy.md) pour déterminer si la copie est autorisée.</span><span class="sxs-lookup"><span data-stu-id="62390-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="62390-113">Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="62390-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="62390-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62390-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62390-115">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="62390-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




