---
description: Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: D3DX10FilterTexture, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537234"
---
# <a name="d3dx10filtertexture-function"></a>D3DX10FilterTexture fonction)

Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTexture* 
</dt> <dd>

Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Objet de texture à filtrer. Consultez [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Niveau de mipmap dont les données sont utilisées pour générer le reste de la chaîne mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Indicateurs contrôlant la manière dont chaque miplevel est filtré (ou D3DX10 \_ par défaut pour \_ la zone de filtre d3dx10 \_ ). Consultez [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
