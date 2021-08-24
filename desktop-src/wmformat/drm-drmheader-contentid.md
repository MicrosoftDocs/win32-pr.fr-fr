---
title: DRM_DRMHeader_ContentID
description: L' \_ attribut DRM DRMHeader \_ contentid contient le contentid qui a été généré par le propriétaire du contenu.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- Format Windows Media DRM_DRMHeader_ContentID
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b17df75902ec41eed935a9b10dbbf4799c92bae2a54c76b4ed676c9e7a3a572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586426"
---
# <a name="drm_drmheader_contentid"></a>\_DRMHEADER DRM \_ contentid

L’attribut **DRM \_ DRMHeader \_ contentID** contient le contentid qui a été généré par le propriétaire du contenu.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ contentid

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Pour définir l’ID de contenu sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ contentid**](drm-contentid.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




