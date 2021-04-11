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
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950123"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



