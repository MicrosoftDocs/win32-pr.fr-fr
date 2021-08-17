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
ms.openlocfilehash: d0944b843c8deb38012242111b6c5057ccf7cb8557c69caefe9a87283d2ae418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328739"
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

## <a name="remarks"></a>Remarques

Le type d’événement RTLostEvent indique qu’un ou plusieurs événements ont été perdus. Le type d’événement RTLostBuffer indique qu’une ou plusieurs mémoires tampons ont été perdues. Les types d’événements RTLostEvent et RTLostBuffer sont remis avant le traitement des événements de la mémoire tampon.

RTLostFile indique que le fichier de stockage utilisé par le journal automatique pour capturer les événements a été perdu.

Le fait de perdre des événements dépend de la fréquence à laquelle les événements sont journalisés et du temps passé par le consommateur à traiter les événements.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Événement perdu**](lost-event.md)
</dt> </dl>

 

 




