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
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521588"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



