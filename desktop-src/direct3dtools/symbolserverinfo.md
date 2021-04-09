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
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108938"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



