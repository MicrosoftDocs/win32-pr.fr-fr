---
description: 'Une application implémente cette interface pour gérer les rappels dans les jeux d’animations générés par les appels à ID3DXAnimationController :: AdvanceTime.'
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: Interface ID3DXAnimationCallbackHandler (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2eeec6fa26504d30588c5e148c07c6c628cc3ce752a2964d2dbefb3059040236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987979"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>Interface ID3DXAnimationCallbackHandler

Une application implémente cette interface pour gérer les rappels dans les jeux d’animations générés par les appels à [**ID3DXAnimationController :: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="members"></a>Membres

L’interface **ID3DXAnimationCallbackHandler** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationCallbackHandler** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXAnimationCallbackHandler** possède ces méthodes.



| Méthode                                                                  | Description                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HandleCallback**](id3dxanimationcallbackhandler--handlecallback.md) | L’application implémente cette méthode. Cette méthode est appelée quand un rappel se produit pour une animation définie dans l’une des pistes pendant un appel à [**ID3DXAnimationController :: AdvanceTime**](id3dxanimationcontroller--advancetime.md).<br/> |



 

## <a name="remarks"></a>Remarques

Le type LPD3DXANIMATIONCALLBACKHANDLER est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
