---
description: Spécifie une file d’attente de travail pour une branche de topologie.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: Attribut MF_TOPONODE_WORKQUEUE_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114022"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>\_Attribut d' \_ ID WORKQUEUE TOPONODE \_ MF

Spécifie une file d’attente de travail pour une branche de topologie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**). L’attribut est facultatif.

La valeur de l’attribut est un identificateur défini par l’application pour la file d’attente de travail.

Les applications peuvent utiliser cet attribut pour assigner des files d’attente de travail à des branches de la topologie. Chaque nœud source de la topologie définit une branche. La branche comprend chaque nœud de topologie qui reçoit des données de ce nœud.

Si vous définissez cet attribut, appelez la méthode [**IMFWorkQueueServices :: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sur la topologie résolue. Plusieurs branches de la topologie peuvent partager la même file d’attente de travail, et les files d’attente de travail peuvent être réutilisées entre les topologies.

> [!Note]  
> La valeur de cet attribut n’est pas la même que celle de l’identificateur retourné par la fonction [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) . La valeur de l’attribut est un identificateur défini par l’application et est utilisée pour associer des branches de topologie à des files d’attente de travail. Lorsque la session multimédia alloue une nouvelle file d’attente de travail, elle stocke l’identificateur de file d’attente de travail réel en interne.

 

Si cet attribut est défini, l’application peut également affecter la branche à une tâche du service Planificateur de classes multimédias (MMCSS), en définissant l’attribut de [**\_ \_ \_ \_ classe WORKQUEUE MMCSS TOPONODE MF**](mf-toponode-workqueue-mmcss-class-attribute.md) .

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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS, \_ classe**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[Files d’attente de travail](work-queues.md)
</dt> </dl>

 

 




