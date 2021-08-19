---
description: Cette classe est la classe parente des événements d’appel de procédure locale avancés. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: Classe ALPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 435b55c44f06b6be062653a45e14a1a890e026371d8bd8e649c87ce3542118c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070289"
---
# <a name="alpc-class"></a>Classe ALPC

Cette classe est la classe parente des événements d’appel de procédure locale avancés.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **ALPC** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Pour activer les événements d’appel de procédure locale avancée dans une session de journalisation du noyau NT, spécifiez l’indicateur de **suivi d’événement \_ \_ \_ ALPC** dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements ALPC en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ALPCGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement ALPC réel lors de la consommation d’événements.



| Type d'événement           | Description                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Valeur de type d’événement, 33 | Événement d’envoi de message. La classe MOF de [**\_ \_ message d’envoi ALPC**](alpc-send-message.md) définit les données d’événement pour cet événement.                           |
| Valeur de type d’événement, 34 | Recevoir un événement de message. La classe MOF de [**\_ \_ message de réception ALPC**](alpc-receive-message.md) définit les données d’événement pour cet événement.                  |
| Valeur de type d’événement, 35 | Attente d’un événement de réponse. La classe MOF [**\_ \_ d’attente de \_ réponse ALPC**](alpc-wait-for-reply.md) définit les données d’événement pour cet événement.                    |
| Valeur de type d’événement, 36 | Attendez l’événement du nouveau message. La classe MOF [**\_ wait \_ for \_ New \_ message**](alpc-wait-for-new-message.md) MOF définit les données d’événement pour cet événement. |
| Valeur de type d’événement, 37 | Arrêter l’événement en attente. La classe MOF d' [**\_ inattente ALPC**](alpc-unwait.md) définit les données d’événement pour cet événement.                                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

