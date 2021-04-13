---
description: Définit un type de données de déclaration de vertex.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Énumération D3DDECLTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322729"
---
# <a name="d3ddecltype-enumeration"></a>Énumération D3DDECLTYPE

Définit un type de données de déclaration de vertex.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**
</dt> <dd>

Float à un composant développé sur (float, 0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**
</dt> <dd>

Float à deux composants développé sur (float, float, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**
</dt> <dd>

Float à trois composants développé sur (float, float, float, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ float4**
</dt> <dd>

Float à quatre composants développé sur (float, float, float, float).

</dd> <dt>

<span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**
</dt> <dd>

Octets compressés à quatre composants, non signés, mappés à 0 à 1 plage. L’entrée est un [**D3DCOLOR**](d3dcolor.md) et est développé en ordre RVBA.

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**
</dt> <dd>

Octet non signé de quatre composants.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**
</dt> <dd>

Deux composants, signés Short, étendus à (valeur, valeur, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**
</dt> <dd>

Quatre-Components, signés Short, étendus à (valeur, valeur, valeur, valeur).

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**
</dt> <dd>

Octet à quatre composants avec chaque octet normalisé en divisant avec 255.0 f.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**
</dt> <dd>

Normald, à deux composants, signé à Short, étendu à (First Short/32767.0, second Short/32767.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**
</dt> <dd>

Normalized, quatre-Components, signés Short, étendus à (First Short/32767.0, second Short/32767.0, Third Short/32767.0, quatrième Short/32767.0).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**
</dt> <dd>

Normald, deux composants, unsigned short, Expanded to (First Short/65535.0, Short Short/65535.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**
</dt> <dd>

Normald, quatre composants, unsigned short, Expanded à (First Short/65535.0, second Short/65535.0, Third Short/65535.0, quatrième Short/65535.0).

</dd> <dt>

<span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**
</dt> <dd>

Le format 3 composants, non signé, 10 10 10 développé sur (valeur, valeur, valeur, 1).

</dd> <dt>

<span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**
</dt> <dd>

Format à trois composants, signé, 10 10 10 normalisé et développé pour (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**
</dt> <dd>

Virgule flottante à deux composants, 16 bits, développée à (valeur, valeur, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**
</dt> <dd>

Virgule flottante à quatre composants, 16 bits et développée en (valeur, valeur, valeur, valeur).

</dd> <dt>

<span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE \_ INutilisé**
</dt> <dd>

Le champ de type dans la déclaration n’est pas utilisé. Il est conçu pour être utilisé avec D3DDECLMETHOD \_ UV et D3DDECLMETHOD \_ LOOKUPPRESAMPLED.

</dd> </dl>

## <a name="remarks"></a>Notes

Les données de vertex sont déclarées avec un tableau de structures [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Chaque élément du tableau contient un type de données de déclaration de vertex.

Utilisez l’outil visionneuse de la prise en charge DirectX (DXCapsViewer.exe) pour déterminer les types pris en charge sur votre appareil. Vous pouvez obtenir cet outil et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX. Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DDECLMETHOD**](./d3ddeclmethod.md)
</dt> </dl>

 

 
