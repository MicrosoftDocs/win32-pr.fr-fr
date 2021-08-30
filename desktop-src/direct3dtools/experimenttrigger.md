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
ms.openlocfilehash: ce4087e4e4ef30cedeb356730a0a7ae94252d4f3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625175"
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



