---
description: Représente des informations sur un frame sur la pile des appels.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallStackFrame, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c6cb4b0e32213165149d7df8c7bf334049e37399
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631337"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>CallStackFrame, structure

Représente des informations sur un frame sur la pile des appels.

## <a name="syntax"></a>Syntaxe


```C++
} CallStackFrame;
```

## <a name="members"></a>Membres

**functionName**  
Chaîne COM contenant le nom de la fonction associée.

**sourceFile**  
Chaîne COM contenant le chemin d’accès du fichier source associé.

**NomModule**  
Chaîne COM contenant le nom du module de code associé.

**lineNumber**  
Numéro de ligne associé.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



