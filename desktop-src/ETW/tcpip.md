---
description: Cette classe est la classe parente pour les événements TCP/IP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972486"
---
# <a name="tcpip-class"></a>TcpIp (classe)

Cette classe est la classe parente pour les événements TCP/IP.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **TcpIp** ne définit aucun membre.

## <a name="remarks"></a>Notes

Pour activer les événements TCP/IP dans une session de journalisation du noyau NT, spécifiez l’indicateur de **trace d’événement indicateur \_ \_ \_ réseau \_ tcpip** dans le membre **EnableFlags** d’une structure de propriétés de [**\_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements TCP/IP en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**TcpIpGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement réseau (TCP/IP) réel lors de la consommation d’événements.



| Type d'événement                                                            | Description                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ Type de suivi \_ \_ Accept**(la valeur de type d’événement est 15)<br/>     | Accepter un événement pour le protocole IPv4. La classe MOF [**\_ TypeGroup2**](tcpip-typegroup2.md) MOF définit les données d’événement pour cet événement.                                                            |
| **Événement \_ Type de suivi \_ \_ Connect**(la valeur de type d’événement est 12)<br/>    | Événement Connect pour le protocole IPv4. La classe MOF [**\_ TypeGroup2**](tcpip-typegroup2.md) MOF définit les données d’événement pour cet événement.                                                           |
| **Événement \_ Type de TRACE \_ \_ Disconnect**(la valeur du type d’événement est 13)<br/> | Événement de déconnexion pour le protocole IPv4. La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                        |
| **Événement \_ \_ \_ Réception du type de suivi**(la valeur du type d’événement est 11)<br/>    | Événement de réception pour le protocole IPv4. La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                           |
| **Événement \_ \_REconnexion \_ du type de suivi**(la valeur du type d’événement est 16)<br/>  | Événement de reconnexion pour le protocole IPv4. (Une tentative de connexion a échoué et une autre tentative est effectuée.) La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement. |
| **Événement \_ \_REtransmission \_ du type de suivi**(la valeur du type d’événement est 14)<br/> | Événement de retransmission pour le protocole IPv4. La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                        |
| **Événement \_ Type de TRACE \_ \_ Send**(la valeur du type d’événement est 10)<br/>       | Envoi d’un événement pour le protocole IPv4. La classe MOF [**\_ SendIPV4**](tcpip-sendipv4.md) MOF définit les données d’événement pour cet événement.                                                                  |
| Valeur de type d’événement, 17                                                  | Événement d’échec. La classe MOF d' [**\_ échec TcpIp**](tcpip-fail.md) définit les données d’événement pour cet événement.                                                                                            |
| Valeur de type d’événement, 18                                                  | Événement TCP Copy pour le protocole IPv4. La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                          |
| Valeur de type d’événement, 26                                                  | Envoi d’un événement pour le protocole IPv6. La classe MOF [**\_ SendIPV6**](tcpip-sendipv6.md) MOF définit les données d’événement pour cet événement.                                                                  |
| Valeur de type d’événement, 27                                                  | Événement Receive pour le protocole IPv6. La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.                                                           |
| Valeur du type d’événement, 28                                                  | Événement Connect pour le protocole IPv6. La classe MOF [**\_ TypeGroup4**](tcpip-typegroup4.md) MOF définit les données d’événement pour cet événement.                                                           |
| Valeur de type d’événement, 29                                                  | Événement de déconnexion pour le protocole IPv6. La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.                                                        |
| Valeur de type d’événement, 30                                                  | Événement de retransmission pour le protocole IPv6. La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.                                                        |
| Valeur de type d’événement 31                                                  | Accepter un événement pour le protocole IPv6. La classe MOF [**\_ TypeGroup4**](tcpip-typegroup4.md) MOF définit les données d’événement pour cet événement.                                                            |
| Valeur de type d’événement, 32                                                  | Événement de reconnexion pour le protocole IPv6. (Une tentative de connexion a échoué et une autre tentative est effectuée.) La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement. |
| Valeur de type d’événement, 34                                                  | Événement TCP Copy pour le protocole IPv6. La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.                                                          |



 

Vous pouvez suivre les événements réseau dans un processus source et de destination à l’aide de la propriété **ProcessID** . Étant donné que certains événements réseau sont journalisés par des threads distincts, vous ne pourrez peut-être pas utiliser les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête Event Trace**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour identifier le processus ou le thread à l’origine des activités réseau.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Échec de TcpIp \_**](tcpip-fail.md)
</dt> <dt>

[**TcpIp \_ SendIPV4**](tcpip-sendipv4.md)
</dt> <dt>

[**TcpIp \_ SendIPV6**](tcpip-sendipv6.md)
</dt> <dt>

[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md)
</dt> <dt>

[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md)
</dt> <dt>

[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md)
</dt> <dt>

[**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md)
</dt> <dt>

[**TcpIp \_ v0**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ v1**](tcpip-v1.md)
</dt> </dl>

 

 
