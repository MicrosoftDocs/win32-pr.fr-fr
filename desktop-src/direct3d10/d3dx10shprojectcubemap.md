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
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525879"
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

 

 
