---
description: 'ID3DXRenderToSurface :: OnLostDevice, méthode : utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.'
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: 'ID3DXRenderToSurface :: OnLostDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 772b678dc4260954c2e03c13d7259565cd896bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093111"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a>ID3DXRenderToSurface :: OnLostDevice, méthode

Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes 

Cette méthode doit être appelée chaque fois que l’appareil est perdu ou avant que l’utilisateur n’appelle [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset). Même si l’appareil n’a pas été réellement perdu, ID3DXRenderToSurface :: OnLostDevice est responsable de la libération de stateblocks et d’autres ressources qui doivent être libérées avant la réinitialisation de l’appareil. Par conséquent, l’objet font ne peut pas être réutilisé avant d’appeler **IDirect3DDevice9 :: Reset** , puis ID3DXRenderToSurface :: OnResetDevice.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
