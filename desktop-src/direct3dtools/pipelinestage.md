---
description: Représente une étape de pipeline, y compris les détails du nuanceur utilisé.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PipeLineStage, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10f1d1780404303109a72fe1a12023bc35b2c0ca
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625165"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>PipeLineStage, structure

Représente une étape de pipeline, y compris les détails du nuanceur utilisé.

## <a name="syntax"></a>Syntaxe


```C++
} PipeLineStage;
```

## <a name="members"></a>Membres

**StageId**  
ID de l’étape de pipeline.

**Débogable**  
true si l’étape de pipeline prend en charge le débogage ; Sinon, false.

**StageName**  
Chaîne COM contenant le nom de l’étape de pipeline.

**GuaranteedOutput**  
true si l’étape de pipeline a toujours une sortie de pipeline ; Sinon, false.

**DebugEntryPoint**  
Chaîne COM contenant le nom du point d’entrée du nuanceur, le cas échéant.

**ShaderFile**  
Chaîne COM contenant le chemin d’accès du fichier source du nuanceur.

**ShaderByteStreamPtr**  
FILEPTR pour le flux d’octets du nuanceur. Cette valeur est retournée pour déboguer.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



