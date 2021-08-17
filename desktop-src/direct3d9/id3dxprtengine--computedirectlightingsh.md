---
description: Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'ID3DXPRTEngine :: ComputeDirectLightingSH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51eb3121501cee7c56385a9083fc689cd8a06759443250f64bae16901779a3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729711"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a>ID3DXPRTEngine :: ComputeDirectLightingSH, méthode

Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise la contribution de l’éclairage direct avec l’approximation sh. Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

La sortie n’inclut pas Albedo, et seule la lumière entrante est intégrée dans le simulateur. En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.

Appelez [**ID3DXPRTEngine :: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur de transfert de luminance (PRT) précalculé par le Albedo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
