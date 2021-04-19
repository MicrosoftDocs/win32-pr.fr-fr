---
title: DRM_IsDRMCached
description: La \_ propriété DRM IsDRMCached indique si les informations de licence DRM version 1 ont été stockées sur l’ordinateur local.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- Format Windows Media DRM_IsDRMCached
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106545736"
---
# <a name="drm_isdrmcached"></a><span data-ttu-id="7bb0e-104">\_ISDRMCACHED DRM</span><span class="sxs-lookup"><span data-stu-id="7bb0e-104">DRM\_IsDRMCached</span></span>

<span data-ttu-id="7bb0e-105">La propriété **DRM \_ IsDRMCached** indique si les informations de licence DRM version 1 ont été stockées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7bb0e-105">The **DRM\_IsDRMCached** property indicates whether DRM version 1 license information has been stored on the local machine.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7bb0e-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="7bb0e-106">Global Constant</span></span>

<span data-ttu-id="7bb0e-107">g \_ wszWMDRM \_ IsDRMCached</span><span class="sxs-lookup"><span data-stu-id="7bb0e-107">g\_wszWMDRM\_IsDRMCached</span></span>

## <a name="data-type"></a><span data-ttu-id="7bb0e-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bb0e-108">Data Type</span></span>

<span data-ttu-id="7bb0e-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="7bb0e-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="7bb0e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7bb0e-110">Remarks</span></span>

<span data-ttu-id="7bb0e-111">Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="7bb0e-111">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="7bb0e-112">Cela est **vrai** lorsque l’URL d’acquisition de licence correspond à l’une des deux URL connues utilisées pour l’acquisition de licences locales dans DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="7bb0e-112">It is **TRUE** when the license acquisition URL matches one of two know URLs used for local license acquisition in DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bb0e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bb0e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb0e-114">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="7bb0e-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




