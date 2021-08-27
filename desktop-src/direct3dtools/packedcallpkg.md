---
description: Représente un package de quatre appels.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PackedCallPkg, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39be8828cf3ea0fbf773965db7272d566d43546b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626525"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span id="vspixengine.packedcallpkg"></span>PackedCallPkg, structure

Représente un package de quatre appels.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a>Membres

**pcp1**  
Premier appel dans le package.

**pcp2**  
Deuxième appel dans le package.

**pcp3**  
Troisième appel du package.

**pcp4**  
Quatrième appel du package.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



