---
title: DRM_Flags
description: La \_ propriété indicateurs DRM est utilisée avec le contenu DRM version 1 uniquement pour spécifier les droits qui seront contenus dans la licence locale.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- Format Windows Media DRM_Flags
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940679"
---
# <a name="drm_flags"></a>\_Indicateurs DRM

La **propriété \_ indicateurs DRM** est utilisée avec le contenu DRM version 1 uniquement pour spécifier les droits qui seront contenus dans la licence locale. Les droits sont spécifiés avec les valeurs définies par le type d’énumération des **\_ droits WMT** . Il est possible de sélectionner plusieurs valeurs en les associant à l' **opérateur de bits or.**

## <a name="global-constant"></a>Constante globale

\_indicateurs wszWMDRM \_ g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Lors de l’accès à l’interface **IWMHeaderInfo3** de l’objet Writer, vous pouvez ajouter ou modifier cette valeur. Dans d’autres objets (éditeur de métadonnées, lecteur et lecteur synchrone), cette valeur est en lecture seule. Utilisez [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) pour définir cette propriété lors de la création de contenu DRM version 1.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




