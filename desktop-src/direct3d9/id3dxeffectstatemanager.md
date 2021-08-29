---
description: Il s’agit d’une interface implémentée par l’utilisateur qui permet à un utilisateur de définir l’état de l’appareil à partir d’un effet.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interface ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 38fa6affff27c77fcebc4f8417ca3fd4bd8165fb0597c09ea8d34af79ff4b7d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893579"
---
# <a name="id3dxeffectstatemanager-interface"></a>Interface ID3DXEffectStateManager

Il s’agit d’une interface implémentée par l’utilisateur qui permet à un utilisateur de définir l’état de l’appareil à partir d’un effet. Chacune des méthodes dans cette interface doit être implémentée par l’utilisateur et sera ensuite utilisée comme rappels de l’application lorsque l’une ou l’autre des conditions suivantes se présente :

-   Un effet appelle [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’état de l’effet est mis à jour de manière dynamique en appelant l’API de modification d’État appropriée. Pour plus d’informations, consultez les pages de méthode individuelles.

Quand une application utilise le gestionnaire d’État pour implémenter des rappels personnalisés, un effet n’enregistre et ne restaure plus automatiquement l’état lors de l’appel de [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) et de [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md). Étant donné que l’application a implémenté un comportement personnalisé d’enregistrement et de restauration dans les rappels, ce comportement automatique est contourné.

## <a name="members"></a>Membres

L’interface **ID3DXEffectStateManager** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXEffectStateManager** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXEffectStateManager** possède ces méthodes.



| Méthode                                                                                | Description                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Éclaircie**](id3dxeffectstatemanager--lightenable.md)                           | Fonction de rappel qui doit être implémentée par un utilisateur pour activer/désactiver une lumière.<br/>                                 |
| [**SetFVF**](id3dxeffectstatemanager--setfvf.md)                                     | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un code de Commission.<br/>                                         |
| [**SetLight**](id3dxeffectstatemanager--setlight.md)                                 | Fonction de rappel qui doit être implémentée par un utilisateur pour définir une lumière.<br/>                                            |
| [**SetMaterial**](id3dxeffectstatemanager--setmaterial.md)                           | Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état du matériau.<br/>                                     |
| [**SetNPatchMode**](id3dxeffectstatemanager--setnpatchmode.md)                       | Fonction de rappel qui doit être implémentée par un utilisateur pour définir le nombre de segments de la sous-division pour N-patchs.<br/>   |
| [**SetPixelShader**](id3dxeffectstatemanager--setpixelshader.md)                     | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de pixels.<br/>                                     |
| [**SetPixelShaderConstantB**](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.<br/>        |
| [**SetPixelShaderConstantF**](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de vertex shader.<br/> |
| [**SetPixelShaderConstantI**](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes entières de nuanceur de vertex.<br/>        |
| [**SetRenderState**](id3dxeffectstatemanager--setrenderstate.md)                     | Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de rendu.<br/>                                       |
| [**SetSamplerState**](id3dxeffectstatemanager--setsamplerstate.md)                   | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un échantillonneur.<br/>                                          |
| [**SetTexture**](id3dxeffectstatemanager--settexture.md)                             | Fonction de rappel qui doit être implémentée par un utilisateur pour définir une texture.<br/>                                          |
| [**SetTextureStageState**](id3dxeffectstatemanager--settexturestagestate.md)         | Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de l’étape de texture.<br/>                            |
| [**SetTransform**](id3dxeffectstatemanager--settransform.md)                         | Fonction de rappel qui doit être implémentée par un utilisateur pour définir une transformation.<br/>                                        |
| [**SetVertexShader**](id3dxeffectstatemanager--setvertexshader.md)                   | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de sommets.<br/>                                    |
| [**SetVertexShaderConstantB**](id3dxeffectstatemanager--setvertexshaderconstantb.md) | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.<br/>        |
| [**SetVertexShaderConstantF**](id3dxeffectstatemanager--setvertexshaderconstantf.md) | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de vertex shader.<br/> |
| [**SetVertexShaderConstantI**](id3dxeffectstatemanager--setvertexshaderconstanti.md) | Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes entières de nuanceur de vertex.<br/>        |



 

## <a name="remarks"></a>Remarques

Un utilisateur crée une interface ID3DXEffectStateManager en implémentant une classe qui dérive de cette interface et en implémentant toutes les méthodes d’interface. Une fois l’interface créée, vous pouvez récupérer ou définir le gestionnaire d’État dans un effet à l’aide de [**ID3DXEffect :: GetStateManager**](id3dxeffect--getstatemanager.md) et [**ID3DXEffect :: SetStateManager**](id3dxeffect--setstatemanager.md).

Le type LPD3DXEFFECTSTATEMANAGER est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces d’effet](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
