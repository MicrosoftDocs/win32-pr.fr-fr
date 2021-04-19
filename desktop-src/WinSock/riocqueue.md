---
description: Spécifie un descripteur de file d’attente d’achèvement utilisé pour la notification d’achèvement d’e/s par envoi et réception de demandes avec les extensions d’e/s inscrites Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518418"
---
# <a name="rio_cq"></a>RIO \_ CQ

**Rio \_ CQ** typedef spécifie un descripteur de file d’attente d’achèvement utilisé pour la notification d’achèvement d’e/s par envoi et réception de demandes avec les extensions d’e/s inscrites Winsock.


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

**RIO \_ CQ**
</dt> <dd>

Type de données qui spécifie un descripteur de file d’attente d’achèvement utilisé pour la notification d’achèvement d’e/s par les demandes d’envoi et de réception.

</dd> </dl>

## <a name="remarks"></a>Notes

L’objet **Rio \_ CQ** est utilisé pour la notification d’achèvement d’e/s des demandes d’envoi et de réception de réseau par les extensions d’e/s inscrites par Winsock.

Une application peut utiliser la fonction [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) pour demander une notification quand une file d’attente de saisie semi-automatique **Rio \_ CQ** n’est pas vide. Une application peut également interroger l’État à tout moment d’une file d’attente de saisie semi-automatique **Rio \_ CQ** de façon non bloquante à l’aide de la fonction [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .

L’objet **Rio \_ CQ** est créé à l’aide de la fonction [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) . Au moment de la création, l’application doit spécifier la taille de la file d’attente, qui détermine le nombre d’entrées de saisie semi-automatique qu’elle peut contenir. Quand une application appelle la fonction [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) pour obtenir une poignée [**Rio \_ RQ**](riorqueue.md) , l’application doit spécifier un handle de **Rio \_ CQ** pour les saisies semi-automatiques d’envoi et un handle de **Rio \_ CQ** pour les saisies semi-automatiques. Ces handles peuvent être identiques lorsque la même file d’attente doit être utilisée pour l’envoi et la réception. La fonction **RIOCreateRequestQueue** nécessite également un nombre maximal d’opérations d’envoi et de réception en attente, qui sont facturées en fonction de la capacité de la file d’attente de saisie semi-automatique ou des files d’attente associées. Si les files d’attente n’ont pas suffisamment de capacité restante, l’appel **RIOCreateRequestQueue** échoue avec [WSAENOBUFS](windows-sockets-error-codes-2.md).

Le comportement de notification pour une file d’attente de saisie semi-automatique est défini lors de la création de **Rio \_ CQ** .

Pour une file d’attente de saisie semi-automatique qui utilise un événement, le membre de **type** de la structure de [**\_ \_ fin de notification Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) est défini sur l’exécution de l' **\_ événement \_ Rio**. Le membre **Event. EventHandle** doit contenir le descripteur d’un événement créé par la fonction [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) ou [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) . Pour recevoir la saisie semi-automatique de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l’application doit attendre le handle d’événement spécifié à l’aide de [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ou d’une routine d’attente similaire. Si l’application prévoit de réinitialiser et de réutiliser l’événement, l’application peut réduire la charge en définissant le membre **Event. NotifyReset** sur une valeur différente de zéro. Cela entraîne la réinitialisation automatique de l’événement par la fonction **RIONotify** lorsque la notification se produit. Cela réduit le besoin d’appeler la fonction [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) pour réinitialiser l’événement entre les appels à la fonction **RIONotify** .

Pour une file d’attente de saisie semi-automatique qui utilise un port de terminaison d’e/s, le membre de **type** de la structure de [**\_ \_ fin de notification Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) a la valeur **Rio \_ IOCP \_ completion**. Le membre **Iocp. IocpHandle** doit contenir le descripteur d’un port de terminaison d’e/s créé par la fonction [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) . Pour recevoir la saisie semi-automatique de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l’application doit appeler la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ou [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) . L’application doit fournir un objet [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dédié pour la file d’attente de saisie semi-automatique, et elle peut également utiliser le membre **Iocp. CompletionKey** pour distinguer les demandes **RIONotify** sur la file d’attente d’achèvement des autres terminaisons d’e/s, y compris les saisies semi-automatiques **RIONotify** pour d’autres files d’attente de saisie semi-automatique.

> [!Note]  
> À des fins d’efficacité, l’accès aux files d’attente de saisie semi-automatique (**Rio \_ CQ** structs) et aux files d’attente de requêtes (structs de [**Rio \_ RQ**](riorqueue.md) ) ne sont pas protégés par les primitives de synchronisation. Si vous avez besoin d’accéder à une file d’attente de saisie semi-automatique ou de demande à partir de plusieurs threads, l’accès doit être coordonné par une section critique, un verrou d’écriture de lecteur allégé ou un mécanisme similaire. Ce verrouillage n’est pas nécessaire pour l’accès par un seul thread. Différents threads peuvent accéder à des files d’attente de demandes/de saisie semi-automatique distinctes sans verrous. La nécessité d’une synchronisation se produit uniquement lorsque plusieurs threads essaient d’accéder à la même file d’attente. La synchronisation est également requise si plusieurs threads émettent un problème d’envoi et de réception sur le même socket, car les opérations d’envoi et de réception utilisent la file d’attente des demandes du Socket.

 

Si plusieurs threads tentent d’accéder au même **Rio \_ CQ** à l’aide de [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l’accès doit être coordonné par une section critique, un verrou de writer de lecteur Slim ou un mécanisme d’exclusion mutuelle similaire. Si les files d’attente de saisie semi-automatique ne sont pas partagées, l’exclusion mutuelle n’est pas nécessaire.

Lorsqu’une file d’attente de saisie semi-automatique n’est plus nécessaire, une application peut la fermer à l’aide de la fonction [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .

Le **typedef \_ CQ CQ** est défini dans le fichier d’en-tête *Mswsockdef. h* qui est automatiquement inclus dans le fichier d’en-tête *mswsock. h* . Le fichier d’en-tête *Mswsockdef. h* ne doit jamais être utilisé directement.

## <a name="thread-safety"></a>Cohérence de thread

Si plusieurs threads tentent d’accéder au même **Rio \_ CQ** à l’aide de [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l’accès doit être coordonné par une section critique, un verrou de writer de lecteur Slim ou un mécanisme d’exclusion mutuelle similaire. Si les files d’attente de saisie semi-automatique ne sont pas partagées, l’exclusion mutuelle n’est pas nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Mswsockdef. h (inclure mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[**AVEC chevauchement**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[**achèvement de la \_ notification Rio \_**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[**\_type de \_ fin de notification Rio \_**](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[**RIO \_ RQ**](riorqueue.md)
</dt> <dt>

[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))
</dt> <dt>

[**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
