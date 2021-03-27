---
description: Cette classe est la classe parente pour les événements de compteur de performance. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: PerfInfo, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972226"
---
# <a name="perfinfo-class"></a>PerfInfo, classe

Cette classe est la classe parente pour les événements de compteur de performance.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **PerfInfo** ne définit aucun membre.

## <a name="remarks"></a>Notes

Pour activer les événements DPC (appels de procédure différés) dans une session de journalisation du noyau NT, spécifiez l’indicateur  DPC de l’indicateur de suivi d' **événement \_ \_ \_** dans le membre EnableFlags d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Vous pouvez également spécifier un ou plusieurs des indicateurs suivants :

-   **indicateur de suivi d’événement, \_ \_ \_ interruption**
-   **\_profil d' \_ indicateur de trace d’événements \_**
-   **indicateur de suivi d’événement \_ \_ \_ SYSTEMCALL**

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements DPC en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**PerfInfoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement réel lors de la consommation d’événements.



| Type d'événement           | Description                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Valeur de type d’événement, 46 | Événement de profil échantillonné. La classe MOF [**SampledProfile**](sampledprofile.md) définit les données d’événement pour cet événement. |
| Valeur de type d’événement, 51 | Événement d’entrée d’appel système. La classe MOF [**SysCallEnter**](syscallenter.md) définit les données d’événement pour cet événement.   |
| Valeur de type d’événement, 52 | Événement de sortie de l’appel système. La classe MOF [**SysCallExit**](syscallexit.md) définit les données d’événement pour cet événement.      |
| Valeur de type d’événement, 66 | Événement DPC lié à un thread. La classe MOF [**DPC**](dpc.md) définit les données d’événement pour cet événement.                          |
| Valeur de type d’événement, 67 | Événement de routine de service d’interruption (ISR). La classe MOF [**ISR**](isr.md) définit les données d’événement pour cet événement.       |
| Valeur de type d’événement, 68 | Événement DPC. La classe MOF [**DPC**](dpc.md) définit les données d’événement pour cet événement.                                   |
| Valeur de type d’événement, 69 | Événement du minuteur DPC. La classe MOF [**DPC**](dpc.md) définit les données d’événement pour cet événement.                             |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 
