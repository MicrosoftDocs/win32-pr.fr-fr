---
description: Méthode implémentée par l’utilisateur pour la fermeture d’un \# fichier include de nuanceur.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude :: Close, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525300"
---
# <a name="id3dxincludeclose-method"></a>ID3DXInclude :: Close, méthode

Méthode implémentée par l’utilisateur pour la fermeture d’un \# fichier include de nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers la mémoire tampon retournée qui contient les directives include. Il s’agit du pointeur qui a été retourné par l’appel [**ID3DXInclude :: Open**](id3dxinclude--open.md) correspondant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la lecture du \# fichier include, l’API qui a provoqué l’appel du rappel échoue. Il s’agit de l’un des éléments suivants :

-   Le nuanceur HLSL échouera à l’une des \* \* \* fonctions D3DXCompileShader.
-   Le nuanceur d’assembly échouera à l’une des \* \* \* fonctions D3DXAssembleShader.
-   L’effet échouera à l’une des \* \* \* fonctions D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .

## <a name="remarks"></a>Notes

Si [**ID3DXInclude :: Open**](id3dxinclude--open.md) a réussi, l’appel de **ID3DXInclude :: Close** est garanti avant que l’API utilisant cette interface retourne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude :: Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
