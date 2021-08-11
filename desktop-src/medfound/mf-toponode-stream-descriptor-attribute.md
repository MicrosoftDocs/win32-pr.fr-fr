---
description: Contient un pointeur vers le descripteur de flux pour la source du média.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: Attribut MF_TOPONODE_STREAM_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92517560f0a1f60681afc1209d6d14d3e3c5d663958d365d18b20558c0003199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244323"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>\_Attribut de \_ descripteur de flux TOPONODE MF \_

Contient un pointeur vers le descripteur de flux pour la source du média.

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).

La valeur de l’attribut est un pointeur vers l’interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) du descripteur de flux. Cet attribut est obligatoire.

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

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes :: Setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




