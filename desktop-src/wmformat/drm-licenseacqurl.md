---
title: DRM_LicenseAcqURL
description: L' \_ attribut DRM LicenseAcqURL contient l’adresse d’une page Web à laquelle l’application cliente peut accéder pour obtenir une licence de contenu pour le contenu DRM version 7.
ms.assetid: bee29e39-ded8-439d-9164-fc318cb535c0
keywords:
- Format Windows Media DRM_LicenseAcqURL
topic_type:
- apiref
api_name:
- DRM_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231efc4334a4d893b4bdd1e7545bd50b1bed2a5c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507803"
---
# <a name="drm_licenseacqurl"></a><span data-ttu-id="0f528-104">\_LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="0f528-104">DRM\_LicenseAcqURL</span></span>

<span data-ttu-id="0f528-105">L’attribut **DRM \_ LicenseAcqURL** contient l’adresse d’une page Web à laquelle l’application cliente peut accéder pour obtenir une licence de contenu pour le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="0f528-105">The **DRM\_LicenseAcqURL** attribute contains the address of a Web page that the client application can navigate to in order to obtain a content license for DRM version 7 content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0f528-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="0f528-106">Global Constant</span></span>

<span data-ttu-id="0f528-107">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="0f528-107">g\_wszWMDRM\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="0f528-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="0f528-108">Data Type</span></span>

<span data-ttu-id="0f528-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0f528-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="0f528-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0f528-110">Remarks</span></span>

<span data-ttu-id="0f528-111">Cet attribut peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="0f528-111">This attribute can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="0f528-112">Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).</span><span class="sxs-lookup"><span data-stu-id="0f528-112">The same file attribute can be retrieved using [**DRM\_DRMHeader\_LicenseAcqURL**](drm-drmheader-licenseacqurl.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0f528-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f528-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f528-114">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="0f528-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




