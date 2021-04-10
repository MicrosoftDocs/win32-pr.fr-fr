---
title: DRM_DRMHeader_LicenseAcqURL
description: L' \_ attribut DRM DRMHeader \_ LicenseAcqURL contient l’URL d’acquisition de licence pour une licence DRM version 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- Format Windows Media DRM_DRMHeader_LicenseAcqURL
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030800"
---
# <a name="drm_drmheader_licenseacqurl"></a><span data-ttu-id="8024f-104">\_DRMHEADER DRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="8024f-104">DRM\_DRMHeader\_LicenseAcqURL</span></span>

<span data-ttu-id="8024f-105">L’attribut **DRM \_ DRMHeader \_ LICENSEACQURL** contient l’URL d’acquisition de licence pour une licence DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="8024f-105">The **DRM\_DRMHeader\_LicenseAcqURL** attribute contains the license acquisition URL for a DRM version 7 license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8024f-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="8024f-106">Global Constant</span></span>

<span data-ttu-id="8024f-107">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="8024f-107">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="8024f-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="8024f-108">Data Type</span></span>

<span data-ttu-id="8024f-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="8024f-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="8024f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8024f-110">Remarks</span></span>

<span data-ttu-id="8024f-111">Cet attribut est présent uniquement avec le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="8024f-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="8024f-112">Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="8024f-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="8024f-113">Pour définir l’URL d’acquisition de licence sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md) .</span><span class="sxs-lookup"><span data-stu-id="8024f-113">To set the license acquisition URL on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_LicenseAcqURL**](drm-licenseacqurl.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="8024f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8024f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8024f-115">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="8024f-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




