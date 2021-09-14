---
description: Multiplie chaque valeur de la mémoire tampon par une valeur de constante.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'ID3DXPRTBuffer :: ScaleBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007996"
---
# <a name="id3dxprtbufferscalebuffer-method"></a>ID3DXPRTBuffer :: ScaleBuffer, méthode

Multiplie chaque valeur de la mémoire tampon par une valeur de constante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

Mise à l' *échelle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur constante utilisée pour mettre à l’échelle la mémoire tampon. Chaque valeur de la mémoire tampon est remplacée par le produit de cette valeur et par la valeur de la mémoire tampon d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
