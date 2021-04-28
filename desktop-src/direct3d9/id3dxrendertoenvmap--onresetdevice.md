---
description: 'ID3DXRenderToEnvMap :: OnResetDevice, méthode : utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.'
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: 'ID3DXRenderToEnvMap :: OnResetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78b9e6e1081abed40d1eaf09f6540ed11ed119a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093127"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a>ID3DXRenderToEnvMap :: OnResetDevice, méthode

Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes 

**ID3DXRenderToEnvMap :: OnResetDevice** doit être appelé chaque fois que l’appareil est réinitialisé (à l’aide de [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), avant d’appeler d’autres méthodes. Il s’agit d’un bon emplacement pour acquérir à nouveau des ressources de mémoire vidéo et capturer des blocs d’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
