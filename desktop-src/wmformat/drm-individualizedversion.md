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
# <a name="drm_individualizedversion"></a>\_INDIVIDUALIZEDVERSION DRM

L’attribut **DRM \_ IndividualizedVersion** est stocké dans l’en-tête DRM et contient la version individuelle minimale requise pour accéder au contenu.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




