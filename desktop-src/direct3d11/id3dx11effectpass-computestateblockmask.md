---
title: Méthode ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect. h)
description: Générez un masque pour autoriser ou empêcher les modifications d’État.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Méthode ComputeStateBlockMask Direct3D 11
- Méthode ComputeStateBlockMask Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17198c076d200631142207189059ada425e9ec1ddf6e3c8a8d40499e40aa21a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535055"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>ID3DX11EffectPass :: ComputeStateBlockMask, méthode

Générez un masque pour autoriser ou empêcher les modifications d’État.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStateBlockMask* 
</dt> <dd>

Type : **[ **\_ masque de \_ bloc \_ d’État D3DX11**](d3dx11-state-block-mask.md)\***

Pointeur vers un masque de bloc d’État (voir [**\_ masque de \_ bloc \_ d’État D3DX11**](d3dx11-state-block-mask.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





