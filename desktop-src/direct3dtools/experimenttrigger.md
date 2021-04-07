---
description: Représente des informations sur le déclencheur d’expérimentation.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ExperimentTrigger, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846213"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger, structure

Représente des informations sur le déclencheur d’expérimentation.

## <a name="syntax"></a>Syntaxe


```C++
} ExperimentTrigger;
```

## <a name="members"></a>Membres

**type**  
Type d’expérimentation (capture) déclenché.

**key**  
Lorsque le type est égal à EXPERIMENTTRIGGERTYPE :: KEY, la clé utilisée pour déclencher la capture.

**frameNumber**  
Lorsque le type est égal à EXPERIMENTTRIGGERTYPE :: FRAMENUMBER, numéro de frame qui déclenchera la capture.

**captureCount**  
Nombre de frames séquentiels à capturer.

**actionIID**  
ID de l’événement d’action (capture d’écran, capture de frame, etc.).

**actionPlayload**  
Pointeur vers la charge utile d’événement d’action.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



