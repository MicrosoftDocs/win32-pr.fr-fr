---
description: Méthode implémentée par l’utilisateur pour ouvrir et lire le contenu d’un \# fichier include de nuanceur.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude :: Open, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998578"
---
# <a name="id3dxincludeopen-method"></a>ID3DXInclude :: Open, méthode

Méthode implémentée par l’utilisateur pour ouvrir et lire le contenu d’un \# fichier include de nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IncludeType* \[ dans\]
</dt> <dd>

Type : **[ **D3DXINCLUDE \_**](./d3dxinclude-type.md)**

Emplacement du \# fichier include. Consultez [**\_ type D3DXINCLUDE**](./d3dxinclude-type.md).

</dd> <dt>

*pFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom du \# fichier include.

</dd> <dt>

*pParentData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers le conteneur qui inclut le \# fichier include. Le compilateur peut passer NULL dans *pParentData*. Pour plus d’informations, consultez la section « recherche de fichiers include » dans [compiler un effet (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).

</dd> <dt>

*ppData* \[ à\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Pointeur vers la mémoire tampon retournée qui contient les directives include. Ce pointeur reste valide jusqu’à ce que [**ID3DXInclude :: Close**](id3dxinclude--close.md) soit appelé.

</dd> <dt>

*pBytes* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Nombre d’octets retournés dans ppData.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la lecture du \# fichier include, l’API qui a provoqué l’appel du rappel échoue. Il s’agit de l’un des éléments suivants :

-   Le nuanceur HLSL échouera à l’une des \* \* \* fonctions D3DXCompileShader.
-   Le nuanceur d’assembly échouera à l’une des \* \* \* fonctions D3DXAssembleShader.
-   L’effet échouera à l’une des \* \* \* fonctions D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude :: Close**](id3dxinclude--close.md)
</dt> </dl>

 

 
