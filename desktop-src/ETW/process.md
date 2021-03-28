---
description: Cette classe est la classe parente des événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Process, classe
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
ms.openlocfilehash: b014262044db9e227bec5af2b351d1392c243c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973567"
---
# <a name="process-class"></a>Process, classe

Cette classe est la classe parente des événements de processus.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
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



 

Les événements de démarrage de processus et de thread peuvent être consignés dans le contexte du processus parent ou du thread. Par conséquent, les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) peuvent ne pas correspondre au processus et au thread en cours de création. C’est pourquoi ces événements contiennent les identificateurs de processus et de thread dans les données d’événement (en plus de ceux de l’en-tête d’événement).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Traiter \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Processus \_ v0**](process-v0.md)
</dt> <dt>

[**Traiter \_ v1**](process-v1.md)
</dt> <dt>

[**Traitement \_ v2**](process-v2.md)
</dt> </dl>

 

 
