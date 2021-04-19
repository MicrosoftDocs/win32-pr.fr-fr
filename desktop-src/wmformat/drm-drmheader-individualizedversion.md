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
# <a name="drm_drmheader_individualizedversion"></a>\_DRMHEADER DRM \_ IndividualizedVersion

L’attribut **DRM \_ DRMHeaderIndividualizedVersion** contient la version individuelle minimale requise pour lire le fichier.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Pour définir la version individualisée (également appelée « version de sécurité ») sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




