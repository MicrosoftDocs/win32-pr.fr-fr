---
title: DRM_DRMHeader_KeyID
description: L' \_ attribut DRM DRMHeader \_ KeyId contient l’ID de clé du fichier.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- Format Windows Media DRM_DRMHeader_KeyID
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11d940c9ea76095983542aab380b9abd82c7b037bf0180f532e6f540438a305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931159"
---
# <a name="drm_drmheader_keyid"></a>\_DRMHEADER DRM \_ KeyId

L’attribut **DRM \_ DRMHeader \_ KEYID** contient l’ID de clé du fichier.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ KeyId

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Pour définir l’ID de clé sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ KeyId**](drm-keyid.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




