---
description: Classe parente pour les événements d’en-tête de journal. Cette classe est toujours la première classe de trace d’événements envoyée à un consommateur (cet événement n’est pas envoyé aux consommateurs en temps réel). La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: EventTraceEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972207"
---
# <a name="eventtraceevent-class"></a>EventTraceEvent, classe

Classe parente pour les événements d’en-tête de journal. Cette classe est toujours la première classe de trace d’événements envoyée à un consommateur (cet événement n’est pas envoyé aux consommateurs en temps réel).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **EventTraceEvent** ne définit aucun membre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_En-tête EventTrace**](eventtrace-header.md)
</dt> </dl>

 

 




