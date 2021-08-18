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
ms.openlocfilehash: 85d7c9f64a7d4d00e95f8e877e7f33c9e6a8177977eff3b523c25cc1432ac57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704681"
---
# <a name="drm_individualizedversion"></a>\_INDIVIDUALIZEDVERSION DRM

L’attribut **DRM \_ IndividualizedVersion** est stocké dans l’en-tête DRM et contient la version individuelle minimale requise pour accéder au contenu.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




