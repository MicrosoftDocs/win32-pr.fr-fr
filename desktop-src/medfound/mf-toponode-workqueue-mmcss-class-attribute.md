---
description: Spécifie une tâche du service Planificateur de classes multimédias (MMCSS) pour une branche de topologie.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: Attribut MF_TOPONODE_WORKQUEUE_MMCSS_CLASS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6630cf22d3afe270b2a032304fd9de3118e73e75e28da4116418894271237a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739843"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Class attribut

Spécifie une tâche du [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) pour une branche de topologie.

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**). Cet attribut est facultatif.

Cet attribut requiert l’attribut d' [ \_ \_ \_ ID WORKQUEUE TOPONODE MF](mf-toponode-workqueue-id-attribute.md) . Si vous définissez cet attribut, vous devez également définir l’attribut d' **\_ \_ \_ ID de WORKQUEUE TOPONODE MF** sur le même nœud.

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

[**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ID de \_ WORKQUEUE \_ TOPONODE MF**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[Files d’attente de travail](work-queues.md)
</dt> </dl>

 

 
