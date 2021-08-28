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
ms.openlocfilehash: 6b172682883c5e5272ece103879aefbbdfb79193b0576e9be04432b5d48b1bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856139"
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

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
