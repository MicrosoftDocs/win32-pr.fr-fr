---
description: Représente des informations sur une demande de débogueur de nuanceur.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DebugShaderRequestInfo, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9691b13936ca8ec8e75aa02d9525a9d57143b19e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628458"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo, structure

Représente des informations sur une demande de débogueur de nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>Membres

**mode**  
Étape de pipeline à déboguer.

**1001**  
ID de l’événement Graphics à déboguer.

**frameNumber**  
Frame à déboguer.

**vertex**  
Vertex à déboguer.

**pixellisé**  
Pixel à déboguer.

**groupCoordinates**  
Coordonnées du groupe à déboguer.

**threadCoordinates**  
Coordonnées du thread à déboguer

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



