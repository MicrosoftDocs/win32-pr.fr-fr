---
title: Use_Advanced_DRM
description: L' \_ attribut use Advanced \_ DRM spécifie si la version 7 de DRM est utilisée pour protéger le contenu.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Format Windows Media Use_Advanced_DRM
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a11731fbe212c8b87cd52300da1885206230c7329491a6512ab3c261923c74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658219"
---
# <a name="use_advanced_drm"></a>Utiliser \_ \_ DRM avancé

L’attribut **use \_ Advanced \_ DRM** spécifie si la version 7 de DRM est utilisée pour protéger le contenu.

## <a name="global-constant"></a>Constante globale

g \_ wszWMUse \_ - \_ DRM avancé

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Il s’agit d’une propriété en lecture-écriture qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) et définie à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Cette propriété n’est pas accessible à partir de l’objet lecteur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




