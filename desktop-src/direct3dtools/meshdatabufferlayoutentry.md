---
description: Représente des informations sur une seule entrée dans la disposition de la mémoire tampon d’un maillage.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MeshDataBufferLayoutEntry, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747573"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry, structure

Représente des informations sur une seule entrée dans la disposition de la mémoire tampon d’un maillage.

## <a name="syntax"></a>Syntaxe


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Membres

**pName**  
Chaîne COM contenant le nom de l’entrée.

**numComponents**  
Nombre de composants homogènes (valeurs) qui composent cette entrée.

**isPosition**  
true si l’entrée est une position ; Sinon, false.

**format**  
Le format de données de l’entrée (Register). Pour plus d’informations, consultez l' \_ énumération de format de registre.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



