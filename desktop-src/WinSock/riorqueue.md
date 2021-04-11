---
description: Spécifie un descripteur de socket utilisé par les demandes d’envoi et de réception avec les extensions d’e/s inscrites par Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318873"
---
# <a name="rio_rq"></a>RIO \_ RQ

Le typedef **Rio \_ RQ** spécifie un descripteur de socket utilisé par les demandes d’envoi et de réception avec les extensions d’e/s inscrites Winsock.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**RIO \_ RQ**
</dt> <dd>

Type de données qui spécifie un descripteur de socket utilisé par les demandes d’envoi et de réception.

</dd> </dl>

## <a name="remarks"></a>Notes

Les extensions d’e/s inscrites par Winsock fonctionnent principalement sur un objet **Rio \_ RQ** plutôt que sur un Socket. Une application obtient un **Rio \_ RQ** pour un socket existant à l’aide de la fonction [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) . Le socket d’entrée doit avoir été créé en appelant la fonction [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) avec l’indicateur WSA de l' **\_ indicateur \_ Rio** défini dans le paramètre *dwFlags* .

Après avoir obtenu un objet **Rio \_ RQ** , le descripteur de Socket sous-jacent reste valide. Une application peut continuer à utiliser le Socket sous-jacent pour définir et interroger les options de socket, émettre des IOCTL et finalement fermer le Socket.

> [!Note]  
> À des fins d’efficacité, l’accès aux files d’attente de saisie semi-automatique ([**Rio \_ CQ**](riocqueue.md) structs) et aux files d’attente de requêtes (structs de **Rio \_ RQ** ) ne sont pas protégés par les primitives de synchronisation. Si vous avez besoin d’accéder à une file d’attente de saisie semi-automatique ou de demande à partir de plusieurs threads, l’accès doit être coordonné par une section critique, un verrou d’écriture de lecteur allégé ou un mécanisme similaire. Ce verrouillage n’est pas nécessaire pour l’accès par un seul thread. Différents threads peuvent accéder à des files d’attente de demandes/de saisie semi-automatique distinctes sans verrous. La nécessité d’une synchronisation se produit uniquement lorsque plusieurs threads essaient d’accéder à la même file d’attente. La synchronisation est également requise si plusieurs threads émettent un problème d’envoi et de réception sur le même socket, car les opérations d’envoi et de réception utilisent la file d’attente des demandes du Socket.

 

Le typedef [**Rio \_ RQ**](riocqueue.md) est défini dans le fichier d’en-tête *Mswsockdef. h* qui est automatiquement inclus dans le fichier d’en-tête *mswsock. h* . Le fichier d’en-tête *Mswsockdef. h* ne doit jamais être utilisé directement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Mswsockdef. h (inclure mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
