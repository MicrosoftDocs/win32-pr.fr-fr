---
description: 'Classe UdpIp : cette classe est la classe parente pour les événements UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105387"
---
# <a name="udpip-class"></a>UdpIp, classe

Cette classe est la classe parente pour les événements UDP/IP.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **UdpIp** ne définit aucun membre.

## <a name="remarks"></a>Notes 

Pour activer les événements UDP/IP dans une session de journalisation du noyau NT, spécifiez l’indicateur de **trace d’événements indicateur \_ \_ \_ réseau \_ tcpip** dans le membre **EnableFlags** d’une structure de propriétés de [**\_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements UDP/IP en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**UdpIpGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement réseau (UDP/IP) réel lors de la consommation d’événements.



| Type d'événement                                                         | Description                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ \_ \_ Réception du type de suivi**(la valeur du type d’événement est 11)<br/> | Événement de réception pour le protocole IPv4. La classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF définit les données d’événement pour cet événement. |
| **Événement \_ Type de TRACE \_ \_ Send**(la valeur du type d’événement est 10)<br/>    | Envoi d’un événement pour le protocole IPv4. La classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF définit les données d’événement pour cet événement.    |
| Valeur de type d’événement, 17                                               | Événement d’échec. La classe MOF [**\_ Fail UdpIp**](udpip-fail.md) définit les données d’événement pour cet événement.                                  |
| Valeur de type d’événement, 26                                               | Envoi d’un événement pour le protocole IPv6. La classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF définit les données d’événement pour cet événement.    |
| Valeur de type d’événement, 27                                               | Événement Receive pour le protocole IPv6. La classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF définit les données d’événement pour cet événement. |



 

Vous pouvez suivre les événements réseau dans un processus source et de destination à l’aide de la propriété **ProcessID** . Étant donné que certains événements réseau sont journalisés par des threads distincts, vous ne pourrez peut-être pas utiliser les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête Event Trace**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour identifier le processus ou le thread à l’origine des activités réseau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Échec de UdpIp \_**](udpip-fail.md)
</dt> <dt>

[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ v0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ v1**](udpip-v1.md)
</dt> </dl>

 

 
