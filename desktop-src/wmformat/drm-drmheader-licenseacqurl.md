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
# <a name="drm_drmheader_licenseacqurl"></a>\_DRMHEADER DRM \_ LicenseAcqURL

L’attribut **DRM \_ DRMHeader \_ LICENSEACQURL** contient l’URL d’acquisition de licence pour une licence DRM version 7.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Pour définir l’URL d’acquisition de licence sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




