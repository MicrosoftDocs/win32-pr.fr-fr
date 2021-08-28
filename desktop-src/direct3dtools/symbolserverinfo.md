---
description: Représente des informations sur le serveur de symboles de débogage.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SymbolServerInfo, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 28f85445e6affc006c5c0898df1c85d71693a66d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632087"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo, structure

Représente des informations sur le serveur de symboles de débogage.

## <a name="syntax"></a>Syntaxe


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Membres

**symbolPath**  
Chaîne COM contenant le chemin d’accès du serveur de symboles.

**symbolCacheDir**  
Chaîne COM contenant le répertoire de cache du serveur de symboles.

**publicSymbolServerName**  
Chaîne COM contenant le nom public du serveur de symboles.

**symbolExcludeList**  
Chaîne COM qui spécifie la liste de symboles à exclure.

**symbolIncludeList**  
Chaîne COM qui spécifie la liste de symboles à inclure.

**useExcludeList**  
true si la liste d’exclusion est ignorée ; Sinon, false.

**useMSSymbolServer**  
true si vous utilisez le serveur de symboles Microsoft ; Sinon, false.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



