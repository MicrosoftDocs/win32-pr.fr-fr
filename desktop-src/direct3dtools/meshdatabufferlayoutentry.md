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
ms.openlocfilehash: 44cc67402c69b690ba9070fa51bf8d26f316faa7d10ac991226db2c05b6d6a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282270"
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

 

 



