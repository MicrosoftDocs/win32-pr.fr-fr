---
description: Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interface ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998573"
---
# <a name="id3dxkeyframedanimationset-interface"></a>Interface ID3DXKeyframedAnimationSet

Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé.

## <a name="members"></a>Membres

L’interface **ID3DXKeyframedAnimationSet** hérite de [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXKeyframedAnimationSet** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXKeyframedAnimationSet** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dens**](id3dxkeyframedanimationset--compress.md)                                 | Transforme les animations dans une animation définie dans un format compressé et retourne un pointeur vers la mémoire tampon qui stocke les données compressées.<br/> |
| [**GetCallbackKey**](id3dxkeyframedanimationset--getcallbackkey.md)                     | Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.<br/>                                                                        |
| [**GetCallbackKeys**](id3dxkeyframedanimationset--getcallbackkeys.md)                   | Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.<br/>                                                                     |
| [**GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | Obtient le nombre de clés de rappel dans l’ensemble d’animations.<br/>                                                                                  |
| [**GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)             | Obtient le nombre de clés de rotation dans l’animation d’image clé spécifiée.<br/>                                                                  |
| [**GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)                   | Obtient le nombre de clés de mise à l’échelle dans l’animation d’image clé spécifiée.<br/>                                                                     |
| [**GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | Obtient le nombre de clés de traduction dans l’animation d’image clé spécifiée.<br/>                                                               |
| [**GetPlaybackType**](id3dxkeyframedanimationset--getplaybacktype.md)                   | Obtient le type de la boucle de lecture du jeu d’animations.<br/>                                                                                       |
| [**GetRotationKey**](id3dxkeyframedanimationset--getrotationkey.md)                     | Obtient des informations de rotation pour une image clé spécifique dans l’ensemble d’animations.<br/>                                                                 |
| [**GetRotationKeys**](id3dxkeyframedanimationset--getrotationkeys.md)                   | Remplit un tableau avec les données de clé de rotation utilisées pour l’animation d’image clé.<br/>                                                                   |
| [**GetScaleKey**](id3dxkeyframedanimationset--getscalekey.md)                           | Obtenir des informations de mise à l’échelle pour une image clé spécifique dans l’ensemble d’animations.<br/>                                                                    |
| [**GetScaleKeys**](id3dxkeyframedanimationset--getscalekeys.md)                         | Remplit un tableau avec les données de la clé de mise à l’échelle utilisées pour l’animation d’image clé.<br/>                                                                        |
| [**GetSourceTicksPerSecond**](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | Obtient le nombre de graduations d’image clé d’animation qui se produisent par seconde.<br/>                                                                     |
| [**GetTranslationKey**](id3dxkeyframedanimationset--gettranslationkey.md)               | Obtenir des informations de traduction pour une image clé spécifique dans l’ensemble d’animations.<br/>                                                              |
| [**GetTranslationKeys**](id3dxkeyframedanimationset--gettranslationkeys.md)             | Remplit un tableau avec les données de clé de traduction utilisées pour l’animation d’image clé.<br/>                                                                |
| [**RegisterAnimationSRTKeys**](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | Enregistre les données de l’image clé de l’échelle, de rotation et de translation (SRT) pour une animation.<br/>                                                        |
| [**SetCallbackKey**](id3dxkeyframedanimationset--setcallbackkey.md)                     | Définit des informations sur un rappel spécifique dans l’ensemble d’animations.<br/>                                                                        |
| [**SetRotationKey**](id3dxkeyframedanimationset--setrotationkey.md)                     | Définissez les informations de rotation pour une image clé spécifique dans l’ensemble d’animations.<br/>                                                                 |
| [**SetScaleKey**](id3dxkeyframedanimationset--setscalekey.md)                           | Définir les informations de mise à l’échelle d’une image clé spécifique dans l’ensemble d’animations.<br/>                                                                    |
| [**SetTranslationKey**](id3dxkeyframedanimationset--settranslationkey.md)               | Définissez les informations de traduction pour une image clé spécifique dans l’ensemble d’animations.<br/>                                                              |
| [**UnregisterAnimation**](id3dxkeyframedanimationset--unregisteranimation.md)           | Supprimez les données d’animation du jeu d’animations.<br/>                                                                                       |
| [**UnregisterRotationKey**](id3dxkeyframedanimationset--unregisterrotationkey.md)       | Supprime les données de rotation au niveau de l’image clé spécifiée.<br/>                                                                                   |
| [**UnregisterScaleKey**](id3dxkeyframedanimationset--unregisterscalekey.md)             | Supprime les données de mise à l’échelle au niveau de l’image clé spécifiée.<br/>                                                                                      |
| [**UnregisterTranslationKey**](id3dxkeyframedanimationset--unregistertranslationkey.md) | Supprime les données de traduction au niveau de l’image clé spécifiée.<br/>                                                                                |



 

## <a name="remarks"></a>Notes

Créer une animation avec image clé définie avec [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).

Le type LPD3DXKEYFRAMEDANIMATIONSET est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




