---
description: Charge dans la mémoire une mémoire tampon de transfert luminance (PRT) précalculée qui a été enregistrée sur le disque.
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: D3DXLoadPRTBufferFromFile, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921424"
---
# <a name="d3dxloadprtbufferfromfile-function"></a>D3DXLoadPRTBufferFromFile fonction)

Charge dans la mémoire une mémoire tampon de transfert luminance (PRT) précalculée qui a été enregistrée sur le disque.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom du fichier à partir duquel charger les données de la mémoire tampon.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadPRTBufferFromFileW. Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadPRTBufferFromFileA.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
