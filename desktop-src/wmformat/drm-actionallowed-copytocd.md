---
title: DRM_ActionAllowed_CopyToCD
description: L' \_ attribut DRM ActionAllowed \_ CopyToCD indique si le contenu peut être copié sur un CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- Format Windows Media DRM_ActionAllowed_CopyToCD
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511473"
---
# <a name="drm_actionallowed_copytocd"></a><span data-ttu-id="3d6db-104">\_ACTIONALLOWED DRM \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="3d6db-104">DRM\_ActionAllowed\_CopyToCD</span></span>

<span data-ttu-id="3d6db-105">L’attribut **DRM \_ ActionAllowed \_ CopyToCD** indique si le contenu peut être copié sur un CD.</span><span class="sxs-lookup"><span data-stu-id="3d6db-105">The **DRM\_ActionAllowed\_CopyToCD** attribute indicates whether the content is allowed to be copied to a CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3d6db-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="3d6db-106">Global Constant</span></span>

<span data-ttu-id="3d6db-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="3d6db-107">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>

## <a name="data-type"></a><span data-ttu-id="3d6db-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="3d6db-108">Data Type</span></span>

<span data-ttu-id="3d6db-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="3d6db-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="3d6db-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3d6db-110">Remarks</span></span>

<span data-ttu-id="3d6db-111">Les licences Windows Media DRM 10 utilisent l’action copier pour limiter la copie sur CD.</span><span class="sxs-lookup"><span data-stu-id="3d6db-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to CD.</span></span> <span data-ttu-id="3d6db-112">Vous devez vérifier la propriété de [**\_ \_ copie DRM ActionAllowed**](drm-actionallowed-copy.md) pour déterminer si la copie est autorisée.</span><span class="sxs-lookup"><span data-stu-id="3d6db-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="3d6db-113">Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="3d6db-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="3d6db-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d6db-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6db-115">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="3d6db-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




