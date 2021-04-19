---
description: Crée une mémoire tampon de transfert luminance (PRT) précalculée qui peut être compressée ou remplie par un simulateur. Cette fonction doit être utilisée pour créer des mémoires tampons par vertex ou de volume.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: D3DXCreatePRTBuffer, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545284"
---
# <a name="d3dxcreateprtbuffer-function"></a>D3DXCreatePRTBuffer fonction)

Crée une mémoire tampon de transfert luminance (PRT) précalculée qui peut être compressée ou remplie par un simulateur. Cette fonction doit être utilisée pour créer des mémoires tampons par vertex ou de volume.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Échantillons* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex (ou de texels) échantillonnés.

</dd> <dt>

*NumCoeffs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de coefficients par emplacement d’échantillon. Lors de l’utilisation de l’harmonique sphérique (SH) PRT, le nombre de coefficients doit être Order ², où Order est l’ordre de l’évaluation SH. La commande doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. Le degré de l’évaluation est Order-1.

</dd> <dt>

*NumChannels* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de canaux de couleur à définir dans le maillage. Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Lorsque la mémoire tampon est créée, toutes les valeurs sont initialisées à zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
