---
description: Ces indicateurs sont utilisés par les fonctions qui opèrent sur un ou plusieurs canaux dans une texture.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Énumération D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323230"
---
# <a name="d3dx10_channel_flag-enumeration"></a>\_Énumération de l’indicateur de canal d3dx10 \_

Ces indicateurs sont utilisés par les fonctions qui opèrent sur un ou plusieurs canaux dans une texture.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 \_ canal \_ rouge**
</dt> <dd>

Indique que le canal rouge doit être utilisé.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 le \_ canal \_ bleu**
</dt> <dd>

Indique que le canal bleu doit être utilisé.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Canal d3dx10 \_ vert**
</dt> <dd>

Indique que le canal vert doit être utilisé.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10 \_ canal \_ alpha**
</dt> <dd>

Indique que le canal alpha doit être utilisé.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_Luminance du canal d3dx10 \_**
</dt> <dd>

Indique que les luminaces des canaux rouge, vert et bleu doivent être utilisés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




