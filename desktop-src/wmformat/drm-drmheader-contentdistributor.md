---
title: DRM_DRMHeader_ContentDistributor
description: L' \_ attribut DRM DRMHeader \_ ContentDistributor contient une chaîne identifiying le serveur de distribution de contenu.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- Format Windows Media DRM_DRMHeader_ContentDistributor
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509837"
---
# <a name="drm_drmheader_contentdistributor"></a><span data-ttu-id="031b6-104">\_DRMHEADER DRM \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="031b6-104">DRM\_DRMHeader\_ContentDistributor</span></span>

<span data-ttu-id="031b6-105">L’attribut **DRM \_ DRMHeader \_ ContentDistributor** contient une chaîne identifiying le serveur de distribution de contenu.</span><span class="sxs-lookup"><span data-stu-id="031b6-105">The **DRM\_DRMHeader\_ContentDistributor** attribute contains a string identifiying the content distributor.</span></span>

## <a name="global-constant"></a><span data-ttu-id="031b6-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="031b6-106">Global Constant</span></span>

<span data-ttu-id="031b6-107">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="031b6-107">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>

## <a name="data-type"></a><span data-ttu-id="031b6-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="031b6-108">Data Type</span></span>

<span data-ttu-id="031b6-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="031b6-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="031b6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="031b6-110">Remarks</span></span>

<span data-ttu-id="031b6-111">L’ID de contenu est facultatif et est déterminé uniquement par le créateur du contenu.</span><span class="sxs-lookup"><span data-stu-id="031b6-111">The content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="031b6-112">L’objet enregistreur n’a aucun effet avec cet attribut.</span><span class="sxs-lookup"><span data-stu-id="031b6-112">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="031b6-113">Cet attribut est présent uniquement avec le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="031b6-113">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="031b6-114">Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="031b6-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="031b6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="031b6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031b6-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="031b6-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




