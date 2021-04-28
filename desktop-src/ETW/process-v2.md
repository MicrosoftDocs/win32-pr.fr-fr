---
description: Classe Process_V2-cette classe est la classe parente des événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Classe Process_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: 77d700e7847d0ad19a019985a4e19343ce8f383d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106297"
---
# <a name="process_v2-class"></a>Process \_ v2 (classe)

Cette classe est la classe parente des événements de processus.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **Process** ne définit aucun membre.

## <a name="remarks"></a>Notes 

Pour activer les événements de processus dans une session de journalisation du noyau NT, spécifiez l’indicateur de **\_ \_ \_ processus indicateur de suivi d’événement** dans le membre **EnableFlags** d’une structure de [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Vous pouvez également spécifier l’indicateur suivant :

-   **compteurs de processus de l' \_ indicateur de trace d’événements \_ \_ \_**

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de processus en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ProcessGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement de processus réel lors de la consommation d’événements.



| Type d'événement                                                      | Description                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ \_ \_ Fin du type de suivi**(la valeur du type d’événement est 2)<br/>   | Événement de fin de processus. La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.                                                                                                          |
| **Événement \_ \_ \_ Début du type de suivi**(la valeur du type d’événement est 1)<br/> | Événement de démarrage du processus. La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.                                                                                                        |
| Valeur de type d’événement, 3                                             | Démarrez l’événement processus de collecte de données. Énumère les processus en cours d’exécution au moment du démarrage de la session du noyau. La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement. |
| Valeur de type d’événement, 4                                             | Événement de fin de processus de collecte de données. Énumère les processus en cours d’exécution au moment de la fin de la session du noyau. La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.     |
| Valeur de type d’événement, 32                                            | Événement des compteurs de performances. La classe MOF [**process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) définit les données d’événement pour cet événement.                                                                                          |
| Valeur de type d’événement, 33                                            | Arrêt des compteurs de performances au début de la session. La classe MOF [**process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) définit les données d’événement pour cet événement.                                                     |
| Valeur de type d’événement, 39                                            | Événement de processus obsolète. La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.                                                                                                      |



 

Les événements de démarrage de processus et de thread peuvent être consignés dans le contexte du processus parent ou du thread. Par conséquent, les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) peuvent ne pas correspondre au processus et au thread en cours de création. C’est pourquoi ces événements contiennent les identificateurs de processus et de thread dans les données d’événement (en plus de ceux de l’en-tête d’événement).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Processus**](process.md)
</dt> <dt>

[**Traiter \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Processus \_ v0**](process-v0.md)
</dt> <dt>

[**Traiter \_ v1**](process-v1.md)
</dt> </dl>

 

 
