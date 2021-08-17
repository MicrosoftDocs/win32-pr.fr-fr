---
description: Représente une description d’une tranche de texture.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureSliceDescriptor, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 915ef0158ca4c38eb6f9bbfe7bd3f1baf400b42a37b8f300e3f042bd610204c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119293"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor, structure

Représente une description d’une tranche de texture.

## <a name="syntax"></a>Syntaxe


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a>Membres

**width**  
Largeur (nombre d’échantillons dans l’axe des X) de la tranche.

**height**  
Hauteur (nombre d’échantillons sur l’axe des Y) de la tranche.

**blockRowBytes**  
Nombre d’octets par ligne dans chaque bloc.

**offset**  
Décalage de la tranche dans la texture entière.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



