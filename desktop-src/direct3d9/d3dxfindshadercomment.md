---
description: Recherche un commentaire particulier dans un nuanceur. Le commentaire est identifié par un code à quatre caractères (FOURCC) dans le premier DWORD du commentaire.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: D3DXFindShaderComment, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523826"
---
# <a name="d3dxfindshadercomment-function"></a>D3DXFindShaderComment fonction)

Recherche un commentaire particulier dans un nuanceur. Le commentaire est identifié par un code à quatre caractères (FOURCC) dans le premier DWORD du commentaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers le flux de fonction de nuanceur DWORD.

</dd> <dt>

*FourCC* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Code FOURCC qui identifie le bloc de commentaires. Consultez [formats FourCC](d3dformat.md).

</dd> <dt>

*ppData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Retourne un pointeur vers les données de commentaire (à l’exclusion du jeton de commentaire et du code FOURCC). Cette valeur peut être **null**.

</dd> <dt>

*pSizeInBytes* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Retourne la taille des données de commentaire en octets. Cette valeur peut être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si le commentaire est introuvable et qu’aucune autre erreur ne s’est produite, S \_ false est retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
