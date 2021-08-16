---
description: Identificateur de flux du récepteur de flux associé à ce nœud de topologie.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: Attribut MF_TOPONODE_STREAMID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cf1edc8918af91144de4f408e7913c3f40b1f0246059bc5bf9e4f1193a1cf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739888"
---
# <a name="mf_toponode_streamid-attribute"></a>\_ \_ Attribut STREAMID TOPONODE MF

Identificateur de flux du récepteur de flux associé à ce nœud de topologie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux nœuds de sortie (**\_ nœud de \_ sortie \_ de topologie MF**).

Lorsque la session multimédia charge la topologie, elle interroge le récepteur de média pour obtenir un récepteur de flux avec l’identificateur spécifié. En cas d’échec, elle tente d’ajouter un nouveau récepteur de flux au récepteur multimédia.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




