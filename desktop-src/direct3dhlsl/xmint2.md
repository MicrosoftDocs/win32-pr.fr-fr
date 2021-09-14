---
title: XMINT2, structure
description: Décrit un vecteur d’entiers 2D.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2 structure HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5dfe4aab8a23dbf1b7921742272b0d2b0ab2382
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918068"
---
# <a name="xmint2-structure"></a>XMINT2, structure

Décrit un vecteur d’entiers 2D.

## <a name="syntax"></a>Syntaxe


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
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

</dd> </dl>



## <a name="remarks"></a>Notes

Cette structure est définie dans l' ``D3DX\_DXGIFormatConvert.inl`` en-tête dans le kit de développement logiciel (SDK) DirectX (juin 2010) pour une utilisation à partir de C++. la dernière version de cet en-tête dans le Package [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet ne le définit plus et s’appuie sur [DirectX :: XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) dans DirectXMath à la place.



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures](format-conversion-structures.md)
</dt> <dt>

[Décompresser et compresser le \_ format DXGI pour la modification des images In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>