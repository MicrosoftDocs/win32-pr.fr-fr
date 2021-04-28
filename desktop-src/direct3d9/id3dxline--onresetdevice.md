---
description: 'ID3DXLine :: OnResetDevice, méthode : utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.'
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: 'ID3DXLine :: OnResetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7e1275e7a7ec894601dc67503e25e1fa82545f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093657"
---
# <a name="id3dxlineonresetdevice-method"></a>ID3DXLine :: OnResetDevice, méthode

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

**ID3DXLine :: OnResetDevice** doit être appelé chaque fois que l’appareil est réinitialisé (à l’aide de [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), avant d’appeler d’autres méthodes. Il s’agit d’un bon emplacement pour acquérir à nouveau des ressources de mémoire vidéo et capturer des blocs d’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
