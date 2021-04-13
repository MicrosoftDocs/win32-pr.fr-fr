---
title: DRM_IndividualizedVersion
description: L' \_ attribut DRM IndividualizedVersion est stocké dans l’en-tête DRM et contient la version individuelle minimale requise pour accéder au contenu.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- Format Windows Media DRM_IndividualizedVersion
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314359"
---
# <a name="drm_individualizedversion"></a><span data-ttu-id="c5070-104">\_INDIVIDUALIZEDVERSION DRM</span><span class="sxs-lookup"><span data-stu-id="c5070-104">DRM\_IndividualizedVersion</span></span>

<span data-ttu-id="c5070-105">L’attribut **DRM \_ IndividualizedVersion** est stocké dans l’en-tête DRM et contient la version individuelle minimale requise pour accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="c5070-105">The **DRM\_IndividualizedVersion** attribute is stored in the DRM header and contains the minimum individualized version required to access the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c5070-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="c5070-106">Global Constant</span></span>

<span data-ttu-id="c5070-107">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="c5070-107">g\_wszWMDRM\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="c5070-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="c5070-108">Data Type</span></span>

<span data-ttu-id="c5070-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="c5070-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c5070-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c5070-110">Remarks</span></span>

<span data-ttu-id="c5070-111">Cet attribut est présent uniquement avec le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="c5070-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="c5070-112">Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="c5070-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="c5070-113">Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span><span class="sxs-lookup"><span data-stu-id="c5070-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c5070-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5070-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5070-115">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="c5070-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




