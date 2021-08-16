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
ms.openlocfilehash: a82edc09cf28ab5b46f4dc6df91f266927294209c69ff11289324d01cedbd23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848478"
---
# <a name="drm_licenseacqurl"></a>\_LICENSEACQURL DRM

L’attribut **DRM \_ LicenseAcqURL** contient l’adresse d’une page Web à laquelle l’application cliente peut accéder pour obtenir une licence de contenu pour le contenu DRM version 7.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ LicenseAcqURL

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




