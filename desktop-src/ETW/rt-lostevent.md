---
description: Cette classe de type d’événement est utilisée pour indiquer que les événements ont été perdus dans une session en temps réel. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: Classe RT_LostEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526385"
---
# <a name="rt_lostevent-class"></a>RT \_ LostEvent, classe

Cette classe de type d’événement est utilisée pour indiquer que les événements ont été perdus dans une session en temps réel.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Membres

La classe **RT \_ LostEvent** ne définit aucun membre.

## <a name="remarks"></a>Notes

Le type d’événement RTLostEvent indique qu’un ou plusieurs événements ont été perdus. Le type d’événement RTLostBuffer indique qu’une ou plusieurs mémoires tampons ont été perdues. Les types d’événements RTLostEvent et RTLostBuffer sont remis avant le traitement des événements de la mémoire tampon.

RTLostFile indique que le fichier de stockage utilisé par le journal automatique pour capturer les événements a été perdu.

Le fait de perdre des événements dépend de la fréquence à laquelle les événements sont journalisés et du temps passé par le consommateur à traiter les événements.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Événement perdu**](lost-event.md)
</dt> </dl>

 

 




