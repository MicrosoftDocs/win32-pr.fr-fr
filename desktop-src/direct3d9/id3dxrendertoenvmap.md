---
description: L’interface ID3DXRenderToEnvMap est utilisée pour généraliser le processus de rendu des mappages d’environnement.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interface ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106540932"
---
# <a name="id3dxrendertoenvmap-interface"></a>Interface ID3DXRenderToEnvMap

L’interface ID3DXRenderToEnvMap est utilisée pour généraliser le processus de rendu des mappages d’environnement.

## <a name="members"></a>Membres

L’interface **ID3DXRenderToEnvMap** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToEnvMap** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXRenderToEnvMap** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginCube**](id3dxrendertoenvmap--begincube.md)             | Lancer le rendu d’une carte d’environnement cubique.<br/>                                                                                                                                    |
| [**BeginHemisphere**](id3dxrendertoenvmap--beginhemisphere.md) | Lancer le rendu d’un mappage d’environnement hémisphérique.<br/>                                                                                                                              |
| [**BeginParabolic**](id3dxrendertoenvmap--beginparabolic.md)   | Lancer le rendu d’un mappage d’environnement parabolique.<br/>                                                                                                                                |
| [**BeginSphere**](id3dxrendertoenvmap--beginsphere.md)         | Lancer le rendu d’une carte d’environnement sphérique.<br/>                                                                                                                                |
| [**Effet**](id3dxrendertoenvmap--end.md)                         | Restaurez toutes les cibles de rendu et, si nécessaire, composez toutes les faces rendues dans la surface de la carte de l’environnement.<br/>                                                                           |
| [**Visage**](id3dxrendertoenvmap--face.md)                       | Initiez le dessin de chaque face d’une carte d’environnement.<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | Récupère la description de la surface de rendu.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | Récupère le périphérique Direct3D associé à la carte d’environnement.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertoenvmap--onlostdevice.md)       | Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.<br/> |
| [**OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)     | Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Notes

Une carte d’environnement est utilisée pour la géométrie de la scène de texture pour fournir une scène plus sophistiquée sans utiliser de géométrie complexe. Cette interface prend en charge la création de surfaces pour les genres suivants de géométrie : cube, demi-sphère ou hémisphérique, parabolique ou sphère.

L’interface **ID3DXRenderToEnvMap** est obtenue en appelant la fonction [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .

Le type LPD3DXRenderToEnvMap est défini comme un pointeur vers l’interface **ID3DXRenderToEnvMap** .


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
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

 

 
