---
description: Transforme les animations dans une animation définie dans un format compressé et retourne un pointeur vers la mémoire tampon qui stocke les données compressées.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'ID3DXKeyframedAnimationSet :: compress, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295714"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>ID3DXKeyframedAnimationSet :: compress, méthode

Transforme les animations dans une animation définie dans un format compressé et retourne un pointeur vers la mémoire tampon qui stocke les données compressées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

L’une des valeurs d' [**\_ indicateurs D3DXCOMPRESSION**](./d3dxcompression-flags.md) qui définissent le mode de compression utilisé pour le stockage des données d’animation compressées. D3DXCOMPRESS \_ par défaut est la seule valeur actuellement prise en charge.

</dd> <dt>

*Lossiness* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Taux de perte de compression souhaité, dans la plage comprise entre 0 et 1.

</dd> <dt>

*pHierarchy* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFRAME**](d3dxframe.md)**

Pointeur désignant une hiérarchie d’images de transformation [**D3DXFRAME**](d3dxframe.md) . Peut avoir la **valeur null**.

</dd> <dt>

*ppCompressedData* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers l’ensemble d’animations compressées [**ID3DXBuffer**](id3dxbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
