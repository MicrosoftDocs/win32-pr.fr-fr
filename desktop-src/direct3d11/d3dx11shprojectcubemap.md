---
title: D3DX11SHProjectCubeMap, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez que, au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque mathématique des harmoniques sphériques, SHProjectCubeMap.'
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- Fonction D3DX11SHProjectCubeMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992260"
---
# <a name="d3dx11shprojectcubemap-function"></a>D3DX11SHProjectCubeMap fonction)

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [mathématique des harmoniques sphériques](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) , **SHProjectCubeMap**.

 

Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* 
</dt> <dd>

Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*Commande* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ordre de l’évaluation SH, génère les coefficients de commande ^ 2 dont le degré est la commande-1. La plage valide est comprise entre 2 et 6.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Type : **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Pointeur vers un [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) qui représente un carte cubique qui va être projeté dans des harmoniques sphériques.

</dd> <dt>

*pROut* 
</dt> <dd>

Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Vecteur SH de sortie pour le rouge.

</dd> <dt>

*pGOut* 
</dt> <dd>

Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Vecteur SH de sortie pour le vert.

</dd> <dt>

*pBOut* 
</dt> <dd>

Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Vecteur SH de sortie pour le bleu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

