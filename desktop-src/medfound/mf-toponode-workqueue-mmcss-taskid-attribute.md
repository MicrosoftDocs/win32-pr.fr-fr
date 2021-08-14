---
description: Spécifie un identificateur de tâche du service Planificateur de classes multimédias (MMCSS) pour une branche de topologie.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Attribut MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf75dc911c9d00cab2d21d937ef16a43b38cc4271299c6fae4f2ed7381ec63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739627"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId, attribut

Spécifie un identificateur de tâche du service Planificateur de classes multimédias (MMCSS) pour une branche de topologie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**). Cet attribut est facultatif.

Cet attribut est ignoré, sauf si les attributs suivants sont également définis :

-   [**\_ID de \_ WORKQUEUE \_ TOPONODE MF**](mf-toponode-workqueue-id-attribute.md)
-   [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS, \_ classe**](mf-toponode-workqueue-mmcss-class-attribute.md)

Si l’application inscrit l’un de ses propres threads avec MMCSS, vous pouvez utiliser cet attribut pour associer la file d’attente de travail de la topologie au groupe MMCSS de l’application. Affectez à l’attribut une valeur égale à l’identificateur de tâche que l’application a reçu quand elle est inscrite auprès de MMCSS. (L’identificateur de tâche est retourné dans le paramètre *TaskIndex* de la fonction [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) . Pour plus d’informations, consultez la rubrique [fonctions de processus et de thread](../procthread/process-and-thread-functions.md).)

Si vous souhaitez que MMCSS assigne un nouvel identificateur de tâche pour la topologie, définissez l’attribut de [**\_ \_ \_ \_ classe WORKQUEUE MMCSS TOPONODE MF**](mf-toponode-workqueue-mmcss-class-attribute.md) , mais ne définissez pas l’attribut **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId** .

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

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[Files d’attente de travail](work-queues.md)
</dt> </dl>

 

 
