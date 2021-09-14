---
description: Limitez le nombre d’os pouvant influencer un vertex et/ou limitez la quantité d’influence qu’un segment peut avoir sur un sommet.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'ID3DX10SkinInfo :: compact, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855274"
---
# <a name="id3dx10skininfocompact-method"></a>ID3DX10SkinInfo :: compact, méthode

Limitez le nombre d’os pouvant influencer un vertex et/ou limitez la quantité d’influence qu’un segment peut avoir sur un sommet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MaxPerVertexInfluences* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre maximal d’os pouvant influencer un vertex donné. Cette valeur est ignorée si elle est supérieure à la valeur retournée par [**ID3DX10SkinInfo :: GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Indicateur décrivant comment mettre à l’échelle les poids restants sur un vertex donné après un certain nombre de découpés par MinWeight. Si D3DX10 \_ SKININFO \_ aucune \_ mise à l’échelle n’est spécifiée, les poids ne sont pas mis à l’échelle du tout. Si D3DX10 \_ SKININFO \_ Scale \_ to \_ 1 est spécifié, les pondérations supérieures à MinWeight seront mises à l’échelle afin d’augmenter jusqu’à 1,0. Si D3DX10 \_ SKININFO \_ Scale \_ to \_ total est spécifié, les pondérations supérieures à MinWeight seront mises à l’échelle pour s’ajouter au total d’origine.

</dd> <dt>

*MinWeight* \[ dans\]
</dt> <dd>

Type : **float**

Pourcentage minimal d’influence, ou poids, que tout segment peut avoir sur n’importe quel vertex. Cette valeur doit être comprise entre 0 et 1.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être : E \_ OUTOFMEMORY ou e \_ INVALIDARG.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
