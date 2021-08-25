---
title: XMUINT4, structure
description: Décrit un vecteur d’entier non signé 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 structure HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932168d2d251d5506727503053cb56cab2e50e57209276649beb35932478ab26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981469"
---
# <a name="xmuint4-structure"></a>XMUINT4, structure

Décrit un vecteur d’entier non signé 4D.

## <a name="syntax"></a>Syntaxe


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a>Membres

<dl> <dt>

**x**
</dt> <dd>

composant x du vecteur.

</dd> <dt>

**y**
</dt> <dd>

composant y du vecteur.

<dl> <dt>

**Lettre**
</dt> <dd>

composant z du vecteur.

<dl> <dt>

**w**
</dt> <dd>

composant w du vecteur.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Remarques

Cette structure est définie dans l' ``D3DX\_DXGIFormatConvert.inl`` en-tête dans le kit de développement logiciel (SDK) DirectX (juin 2010) pour une utilisation à partir de C++. la dernière version de cet en-tête dans le Package [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet ne le définit plus et s’appuie sur [DirectX :: XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) dans DirectXMath à la place.




## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures](format-conversion-structures.md)
</dt> <dt>

[Décompresser et compresser le \_ format DXGI pour la modification des images In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>