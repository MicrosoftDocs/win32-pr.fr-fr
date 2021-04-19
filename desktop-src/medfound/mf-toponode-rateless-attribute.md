---
description: Spécifie si le récepteur multimédia associé à ce nœud de topologie est sans débit.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: Attribut MF_TOPONODE_RATELESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524077"
---
# <a name="mf_toponode_rateless-attribute"></a>\_Attribut sans \_ débit MF TOPONODE

Spécifie si le récepteur multimédia associé à ce nœud de topologie est sans débit.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds de sortie (**\_ nœud de \_ sortie \_ de topologie MF**).

Si la valeur de cet attribut est différente de zéro, la session multimédia traite le récepteur multimédia comme un récepteur sans débit, que le récepteur multimédia renvoie ou non la caractéristique de **\_ débit MEDIASINK** . Si cet attribut n’est pas défini, le récepteur multimédia est supposé ne pas être sans débit.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSink::GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




