---
description: 'Fonction D3DX10ComputeNormalMap : convertit une carte de hauteur en une carte normale. Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: D3DX10ComputeNormalMap, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105317"
---
# <a name="d3dx10computenormalmap-function"></a>D3DX10ComputeNormalMap fonction)

Convertit une carte de hauteur en une carte normale. Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrcTexture* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Pointeur vers une interface ID3D10Texture2D représentant la texture de la carte de hauteur source.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Un ou plusieurs \_ indicateurs D3DX NORMALMAP qui contrôlent la génération de mappages normaux.

</dd> <dt>

*Chaîne* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Un \_ indicateur de canal D3DX spécifiant la source des informations de hauteur.

</dd> <dt>

*Amplitude* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Multiplicateur de valeur constante qui augmente (ou diminue) les valeurs dans la carte normale. Les valeurs plus élevées rendent généralement les bosses plus visibles, les valeurs basses rendent généralement les rugosités moins visibles.

</dd> <dt>

*pDestTexture* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Pointeur vers une interface ID3D10Texture2D représentant la texture de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la valeur suivante : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes 

Cette méthode calcule le normal à l’aide de la différence centrale avec une taille de noyau de 3 x 3. Les canaux RVB dans la destination contiennent des composants (x, y, z) biaisés de la normale. Le dénominateur de différenciation central est codé en dur sur 2,0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
