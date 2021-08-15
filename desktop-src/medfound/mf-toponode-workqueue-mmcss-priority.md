---
description: Spécifie la priorité de thread relative pour une branche de la topologie.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Attribut MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1b131e6c8b0f379e5e7951498c52f7c0d7a3eab83b75fed4ab9e8100721668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874792"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Priority attribut

Spécifie la priorité de thread relative pour une branche de la topologie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**). L’attribut est facultatif.

Cet attribut requiert l' [ \_ ID de \_ WORKQUEUE \_ MF TOPONODE](mf-toponode-workqueue-id-attribute.md) et les attributs de classe de la [ \_ \_ \_ \_ classe MMCSS TOPONODE WORKQUEUE](mf-toponode-workqueue-mmcss-class-attribute.md) sur le même nœud.

La valeur de l’attribut est la priorité de thread relative de la file d’attente de travail pour cette branche de la topologie. Le [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) utilise la priorité relative lorsqu’il définit la priorité du thread. Pour plus d’informations, consultez [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



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
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
