---
description: 'L’application implémente cette méthode. Cette méthode est appelée quand un rappel se produit pour une animation définie dans l’une des pistes pendant un appel à ID3DXAnimationController :: AdvanceTime.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'ID3DXAnimationCallbackHandler :: HandleCallback, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525299"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>ID3DXAnimationCallbackHandler :: HandleCallback, méthode

L’application implémente cette méthode. Cette méthode est appelée quand un rappel se produit pour une animation définie dans l’une des pistes pendant un appel à [**ID3DXAnimationController :: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de la piste sur laquelle le rappel se produit.

</dd> <dt>

*pCallbackData* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers des données de rappel appartenant à l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
