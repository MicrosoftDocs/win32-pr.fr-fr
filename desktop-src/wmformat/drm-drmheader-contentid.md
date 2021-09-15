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
ms.openlocfilehash: e66edd858451e5d1a58b2a91f9f2362d4cabe9da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521093"
---
# <a name="drm_drmheader_contentid"></a>\_DRMHEADER DRM \_ contentid

L’attribut **DRM \_ DRMHeader \_ contentID** contient le contentid qui a été généré par le propriétaire du contenu.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ contentid

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Pour définir l’ID de contenu sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ contentid**](drm-contentid.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




