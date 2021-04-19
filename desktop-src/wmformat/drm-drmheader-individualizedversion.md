---
title: DRM_DRMHeader_IndividualizedVersion
description: L' \_ attribut DRM DRMHeaderIndividualizedVersion contient la version individuelle minimale requise pour lire le fichier.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- Format Windows Media DRM_DRMHeader_IndividualizedVersion
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511470"
---
# <a name="drm_drmheader_individualizedversion"></a><span data-ttu-id="1247f-104">\_DRMHEADER DRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="1247f-104">DRM\_DRMHeader\_IndividualizedVersion</span></span>

<span data-ttu-id="1247f-105">L’attribut **DRM \_ DRMHeaderIndividualizedVersion** contient la version individuelle minimale requise pour lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="1247f-105">The **DRM\_DRMHeaderIndividualizedVersion** attribute contains the minimum individualized version required to play back the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1247f-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="1247f-106">Global Constant</span></span>

<span data-ttu-id="1247f-107">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="1247f-107">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="1247f-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="1247f-108">Data Type</span></span>

<span data-ttu-id="1247f-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1247f-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="1247f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1247f-110">Remarks</span></span>

<span data-ttu-id="1247f-111">Cet attribut est présent uniquement avec le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="1247f-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="1247f-112">Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="1247f-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="1247f-113">Pour définir la version individualisée (également appelée « version de sécurité ») sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1247f-113">To set the individualized version (also called the security version) on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_IndividualizedVersion**](drm-individualizedversion.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="1247f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1247f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1247f-115">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="1247f-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




