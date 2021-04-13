---
description: Identificateur de classe (CLSID) de la Media Foundation transformation (MFT) associée à ce nœud de topologie.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Attribut MF_TOPONODE_TRANSFORM_OBJECTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527418"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
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

 

 




