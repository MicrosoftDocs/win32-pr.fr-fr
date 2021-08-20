---
description: 'Thread, classe : cette classe est la classe parente pour les événements de thread. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: b587441358d78d3300276ac3b59db2512f697ad95411bcc9b145df52180e4154
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813983"
---
# <a name="thread-class"></a>Thread (classe)

Cette classe est la classe parente pour les événements de thread.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **thread** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Pour activer les événements de thread dans une session de journalisation du noyau NT, spécifiez l’indicateur de thread de l' **indicateur de \_ trace \_ \_ d’événements** dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de thread en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ThreadGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement de thread réel lors de la consommation d’événements.



| Type d'événement                                                      | Description                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ \_ \_ Fin du type de suivi**(la valeur du type d’événement est 2)<br/>   | Événement de fin de thread. La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement.                                                                                                        |
| **Événement \_ \_ \_ Début du type de suivi**(la valeur du type d’événement est 1)<br/> | Événement de démarrage du thread. La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement.                                                                                                      |
| Valeur de type d’événement, 3                                             | Démarrez l’événement de thread de collecte de données. Énumère les threads en cours d’exécution au moment du démarrage de la session du noyau. La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement. |
| Valeur de type d’événement, 4                                             | Événement de thread de collecte de données de fin. Énumère les threads en cours d’exécution au moment de la fin de la session du noyau. La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement.     |



 

Les événements de démarrage de processus et de thread peuvent être consignés dans le contexte du processus parent ou du thread. Par conséquent, les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) peuvent ne pas correspondre au processus et au thread en cours de création. C’est pourquoi ces événements contiennent les identificateurs de processus et de thread dans les données d’événement (en plus de ceux de l’en-tête d’événement).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Thread \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ v0**](thread-v0.md)
</dt> <dt>

[**Thread \_ v1**](thread-v1.md)
</dt> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 
