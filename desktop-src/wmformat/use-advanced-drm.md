---
title: Use_Advanced_DRM
description: L' \_ attribut use Advanced \_ DRM spécifie si la version 7 de DRM est utilisée pour protéger le contenu.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Format Windows Media Use_Advanced_DRM
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8720d5b401a1a1cec5240920bfb4a3811012420
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104198737"
---
# <a name="use_advanced_drm"></a><span data-ttu-id="8c701-104">Utiliser \_ \_ DRM avancé</span><span class="sxs-lookup"><span data-stu-id="8c701-104">Use\_Advanced\_DRM</span></span>

<span data-ttu-id="8c701-105">L’attribut **use \_ Advanced \_ DRM** spécifie si la version 7 de DRM est utilisée pour protéger le contenu.</span><span class="sxs-lookup"><span data-stu-id="8c701-105">The **Use\_Advanced\_DRM** attribute specifies whether DRM version 7 is used to protect the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8c701-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="8c701-106">Global Constant</span></span>

<span data-ttu-id="8c701-107">g \_ wszWMUse \_ - \_ DRM avancé</span><span class="sxs-lookup"><span data-stu-id="8c701-107">g\_wszWMUse\_Advanced\_DRM</span></span>

## <a name="data-type"></a><span data-ttu-id="8c701-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="8c701-108">Data Type</span></span>

<span data-ttu-id="8c701-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="8c701-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="8c701-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8c701-110">Remarks</span></span>

<span data-ttu-id="8c701-111">Il s’agit d’une propriété en lecture-écriture qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) et définie à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="8c701-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="8c701-112">Cette propriété n’est pas accessible à partir de l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="8c701-112">This property is not accessible from the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c701-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c701-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c701-114">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="8c701-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




