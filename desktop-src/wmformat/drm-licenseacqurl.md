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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295930"
---
# <a name="drm_licenseacqurl"></a>\_LICENSEACQURL DRM

L’attribut **DRM \_ LicenseAcqURL** contient l’adresse d’une page Web à laquelle l’application cliente peut accéder pour obtenir une licence de contenu pour le contenu DRM version 7.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ LicenseAcqURL

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




