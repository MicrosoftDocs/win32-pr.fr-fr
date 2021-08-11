---
description: Contient l’identificateur de classe (CLSID) d’une transformation de Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Attribut MFT_TRANSFORM_CLSID_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0122b783d8b321aa2a5c7788a589e19625b6a2bde8e37b0b659b0a1192f8c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240197"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>Attribut de l' \_ \_ attribut CLSID de transformation MFT \_

Contient l’identificateur de classe (CLSID) d’une transformation de Media Foundation (MFT).

## <a name="data-type"></a>Type de données

**GUID**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Notes

Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Cet attribut est utilisé en interne par l’objet d’activation lorsqu’il crée la table MFT. Les applications ne doivent pas utiliser ce CLSID directement pour créer la table MFT, car il se peut que l’objet d’activation doive initialiser la table MFT. Par conséquent, pour créer une instance de la MFT, appelez [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sur l’objet d’activation.

Notez que la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporte différemment de la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) à cet égard. La fonction **MFTEnum** retourne des CLSID, que l’application transmet à la fonction **CoCreateInstance** . La fonction **MFTEnumEx** retourne des objets d’activation plutôt que des CLSID.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




