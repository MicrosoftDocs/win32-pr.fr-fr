---
description: Représente une description d’un format de texture.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureFormatDesc, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b868c1b248d2d2a37422acbb5cfe1ae3feede804
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622295"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc, structure

Représente une description d’un format de texture.

## <a name="syntax"></a>Syntaxe


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a>Membres

**dxgiFormat**  
Format DXGI de la texture.

**dataFormat**  
Format de données de la texture.

**blockBytes**  
Nombre d’octets dans un bloc de données.

**blockHeight**  
Hauteur (échantillons de nombre sur l’axe des Y) du bloc.

**blockWidth**  
Largeur (nombre d’échantillons dans l’axe des X) du bloc.

**channelX**  
Décrit les propriétés du canal X. Pour plus d’informations, consultez la structure PixEngineChannelDescription.

**canalisation**  
Décrit les propriétés du canal Y. Pour plus d’informations, consultez la structure PixEngineChannelDescription.

**channelZ**  
Décrit les propriétés du Canal Z. Pour plus d’informations, consultez la structure PixEngineChannelDescription.

**channelW**  
Décrit les propriétés du canal W. Pour plus d’informations, consultez la structure PixEngineChannelDescription.

**swizzle**  
Décrit le Swizzle (échange de canal) appliqué à l’exemple.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



