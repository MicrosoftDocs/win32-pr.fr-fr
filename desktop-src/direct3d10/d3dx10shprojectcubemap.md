---
description: Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: D3DX10SHProjectCubeMap, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fa30724bed56e86d16626133ab32e3494d3c71d6ffa839be1520518c97a77fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990459"
---
# <a name="d3dx10shprojectcubemap-function"></a>D3DX10SHProjectCubeMap fonction)

Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Commande* 
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH, génère la commande ^ 2 coefs, le degré est Order-1.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Type : **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Carte cubique qui va être projeté dans des harmoniques sphériques. Consultez [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).

</dd> <dt>

*pROut* 
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Vecteur SH de sortie pour le rouge.

</dd> <dt>

*pGOut* 
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Vecteur SH de sortie pour le vert.

</dd> <dt>

*pBOut* 
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Vecteur SH de sortie pour le bleu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
