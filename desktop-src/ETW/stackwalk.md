---
description: Cette classe est la classe parente pour les événements de suivi de pile.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: StackWalk, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1a5245964cf6a87c6bb09be0f3f83aa30b1b9337a2a5238be873d90ade90ba91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746529"
---
# <a name="stackwalk-class"></a>StackWalk, classe

Cette classe est la classe parente pour les événements de suivi de pile.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **StackWalk** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Pour activer le suivi de pile des événements de noyau, appelez la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) et spécifiez les événements de noyau et les types pour lesquels vous souhaitez capturer la trace de la pile. Pour activer le suivi de pile pour d’autres événements, définissez le membre **EnableProperty** de l' [**activation des \_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) sur **événement activer la trace de la \_ \_ \_ pile \_ de propriétés**.

Utilisez le type d’événement suivant pour identifier l’événement réel lors de la consommation d’événements.



| Type d'événement           | Description                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Valeur de type d’événement, 32 | Événement de suivi de pile. La classe MOF de l' [**\_ événement StackWalk**](stackwalk-event.md) définit les données d’événement pour cet événement. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 
