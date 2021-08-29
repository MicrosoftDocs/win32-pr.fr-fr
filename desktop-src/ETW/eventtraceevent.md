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
ms.openlocfilehash: 0e8e4c369eab647d51fbb690338ff9451a010bfac69af68ec1209ada10db4018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395037"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_En-tête EventTrace**](eventtrace-header.md)
</dt> </dl>

 

 




