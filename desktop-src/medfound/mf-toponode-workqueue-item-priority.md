---
description: Spécifie la priorité de l’élément de travail pour une branche de la topologie.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Attribut MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313874"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>Attribut de priorité de l' \_ \_ élément WORKQUEUE TOPONODE \_ MF \_

Spécifie la priorité de l’élément de travail pour une branche de la topologie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**). L’attribut est facultatif.

Cet attribut requiert l’attribut d' [ \_ \_ \_ ID WORKQUEUE MF TOPONODE](mf-toponode-workqueue-id-attribute.md) sur le même nœud.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[Améliorations de la file d’attente de travail et du thread](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ID de \_ WORKQUEUE \_ TOPONODE MF**](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




