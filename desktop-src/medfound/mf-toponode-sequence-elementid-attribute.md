---
description: Spécifie l’élément qui contient ce nœud source.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Attribut MF_TOPONODE_SEQUENCE_ELEMENTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523617"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>\_ \_ Attribut ELEMENTID de séquence TOPONODE MF \_

Spécifie l’élément qui contient ce nœud source.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).

Le pipeline multimédia utilise cet attribut pour déterminer quand les sources multimédias font partie du même élément. Le pipeline traite tous les nœuds sources qui font partie du même élément comme ayant la même horloge.

Lorsque le pipeline met en file d’attente une nouvelle topologie qui contient des nœuds sources qui font partie d’un élément présent dans la topologie précédente, le pipeline traite ces nœuds sources comme ayant la même horloge que les nœuds sources de cet élément dans la topologie précédente.

> [!Note]  
> Le pipeline de média ne corrige pas les horodatages pour les nœuds sources ayant des taux d’horloge différents.

 

Une source de média qui peut fournir des topologies doit implémenter l’interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) ou l’interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) . Une source de média qui fournit des topologies doit définir l’attribut d' **\_ \_ \_ ELEMENTID de séquence TOPONODE MF** sur chaque nœud source qu’elle crée.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



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

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 




