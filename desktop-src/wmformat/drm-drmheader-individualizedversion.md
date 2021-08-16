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
ms.openlocfilehash: 5793fa81a7c6c57542991d582607edb0cf3e38b62b037ad46974a4211a7ef8ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931179"
---
# <a name="drm_drmheader_individualizedversion"></a>\_DRMHEADER DRM \_ IndividualizedVersion

L’attribut **DRM \_ DRMHeaderIndividualizedVersion** contient la version individuelle minimale requise pour lire le fichier.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Pour définir la version individualisée (également appelée « version de sécurité ») sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




