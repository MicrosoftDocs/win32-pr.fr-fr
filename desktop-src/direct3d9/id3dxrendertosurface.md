---
description: L’interface ID3DXRenderToSurface est utilisée pour généraliser le processus de rendu des surfaces.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interface ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 238e1870fd5bf1832ffbb3b5c3a5a49533ef122277a4000bafdbaa10112b4528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729505"
---
# <a name="id3dxrendertosurface-interface"></a>Interface ID3DXRenderToSurface

L’interface ID3DXRenderToSurface est utilisée pour généraliser le processus de rendu des surfaces.

## <a name="members"></a>Membres

L’interface **ID3DXRenderToSurface** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToSurface** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXRenderToSurface** possède ces méthodes.



| Méthode                                                       | Description                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | Commence une scène.<br/>                                                                                                                                                                      |
| [**EndScene**](id3dxrendertosurface--endscene.md)           | Termine une scène.<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | Récupère les paramètres de la surface de rendu.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Récupère le périphérique Direct3D associé à la surface de rendu.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Remarques

Les surfaces peuvent être utilisées de différentes façons, notamment les cibles de rendu, le rendu hors écran ou le rendu des textures.

Une surface peut être configurée à l’aide d’un Viewport distinct à l’aide de la méthode [**ID3DXRenderToSurface :: BeginScene**](id3dxrendertosurface--beginscene.md) pour fournir une vue Render personnalisée. Si la surface n’est pas une cible de rendu, une cible de rendu compatible est utilisée et le résultat est copié vers la surface à la fin de la scène.

L’interface **ID3DXRenderToSurface** est obtenue en appelant la fonction [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .

Le type LPD3DXRENDERTOSURFACE est défini comme un pointeur vers l’interface **ID3DXRenderToSurface** .


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
