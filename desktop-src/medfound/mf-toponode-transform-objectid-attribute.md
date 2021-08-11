---
description: Identificateur de classe (CLSID) de la Media Foundation transformation (MFT) associée à ce nœud de topologie.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Attribut MF_TOPONODE_TRANSFORM_OBJECTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b5013bc43f07e08e1a2c26530e9325595e62666986516029ef9d76e2c72ffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244313"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>\_ \_ Attribut ObjectID de transformation TOPONODE MF \_

Identificateur de classe (CLSID) de la Media Foundation transformation (MFT) associée à ce nœud de topologie.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).

Les applications peuvent utiliser cet attribut pour initialiser une de nœud. Si vous définissez cet attribut, il n’est pas nécessaire d’appeler [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) avec un pointeur vers un objet MFT ou activation. À l’inverse, si vous appelez **setObject**, vous n’avez pas besoin de définir cet attribut. Pour plus d’informations, consultez [création de topologies](creating-topologies.md).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Création de topologies](creating-topologies.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




