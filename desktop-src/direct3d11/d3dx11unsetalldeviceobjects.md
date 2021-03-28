---
title: D3DX11UnsetAllDeviceObjects, fonction (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la méthode ID3D11DeviceContext ClearState.'
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Fonction D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323113"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a>D3DX11UnsetAllDeviceObjects fonction)

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la méthode [**ID3D11DeviceContext :: ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .

 

Supprime toutes les ressources de l’appareil en affectant à leurs pointeurs la **valeur null**. Cela doit être appelé lors de l’arrêt de votre application. Cela permet de s’assurer que, lorsque l’un d’eux libère toutes ses ressources, aucune d’entre elles n’est liée à l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* \[ dans\]
</dt> <dd>

Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





