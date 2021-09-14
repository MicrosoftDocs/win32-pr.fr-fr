---
description: Les constantes suivantes identifient les files d’attente de travail de Media Foundation standard.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificateurs de file d’attente de travail (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d454e8b2a199a9c132bf6ea287f31d7d3e5102
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313566"
---
# <a name="work-queue-identifiers"></a>Identificateurs de file d’attente de travail

Les constantes suivantes identifient les files d’attente de travail de Media Foundation standard.

Les applications doivent utiliser \_ \_ la file d’attente de rappel MFASYNC \_ multithread ou utiliser une file d’attente de travail obtenue à partir de [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) si elles souhaitent contrôler la priorité d’exécution. Notez que les priorités de la file d’attente de travail de la plateforme par défaut peuvent changer dynamiquement lorsqu’une application appelle [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss). Pour plus d’informations sur les files d’attente de travail, consultez [files d’attente de travail](work-queues.md).




| Constante/valeur | Description | 
|----------------|-------------|
| <span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt><dt>0x00000001</dt></dl> | Dans la plupart des cas, les applications doivent utiliser <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> Cette file d’attente de travail est utilisée pour les opérations synchrones. L’utilisation de la file d’attente de travail standard peut courir le risque de blocage. Les applications peuvent créer une file d’attente synchrone privée en plus de la file d’attente multithread à l’aide de <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt><dt>0x00000002</dt></dl> | Pas pour l’utilisation générale des applications.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt><dt>0x00000003</dt></dl> | Pas pour l’utilisation générale des applications.<br /> Cette file d’attente de travail est utilisée en interne pour les opérations d’e/s telles que la lecture de fichiers et la lecture à partir du réseau.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt><dt>0x00000004</dt></dl> | Pas pour l’utilisation générale des applications.<br /> Cette file d’attente de travail est utilisée pour les rappels périodiques et les éléments de travail planifiés. Les fonctions suivantes placent les éléments de travail dans cette file d’attente :<br /><ul><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li></ul> | 
| <span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt><dt>0x00000005</dt></dl> | Cette file d’attente de travail multithread doit être utilisée dans la plupart des cas. <br /> Cette file d’attente de travail est utilisée pour les opérations asynchrones tout au long de Media Foundation.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt><dt>0x00000007</dt></dl> | Pas pour l’utilisation générale des applications. À la place, les applications doivent utiliser <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> | 




En outre, les constantes suivantes sont utilisées dans le cadre de la connexion aux files d’attente de travail.



| Constante/valeur                                                                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_ \_File d’attente de rappels \_ non définie**</dt> <dt>0x00000000</dt> </dl>           | File d’attente de travail non définie.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_ \_ \_ \_ Masque privé de la file d’attente de rappel**</dt> <dt>0xFFFF0000</dt> </dl> | Masque de bits pour distinguer les files d’attente de travail de plateforme de celles créées en appelant [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).<br/> Pour une file d’attente de travail créée par [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), la valeur suivante est différente de zéro :<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_ Mise en \_ file d’attente de rappel \_ toutes les**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Toutes les files d’attente de travail de plateforme.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes Media Foundation](media-foundation-constants.md)
</dt> <dt>

[Files d’attente de travail](work-queues.md)
</dt> <dt>

[Améliorations de la file d’attente de travail et du thread](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




