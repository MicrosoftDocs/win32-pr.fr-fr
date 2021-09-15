---
description: Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'ID3DXPRTCompBuffer :: ExtractPCA, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516709"
---
# <a name="id3dxprtcompbufferextractpca-method"></a>ID3DXPRTCompBuffer :: ExtractPCA, méthode

Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartPCA* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de départ pour les coefficients de projection PCA à extraire de la mémoire tampon.

</dd> <dt>

*NumExtract* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de coefficients de projection PCA à extraire de la mémoire tampon.

</dd> <dt>

*pPCACoefficients* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers l’emplacement où les coefficients d’analyse des composants principaux en cluster (CPCA) sont écrits. La taille des données écrites est (nombre d’échantillons) \* (nombre de coefficients de l’APC).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
