---
description: Spécifie la manière dont l’analyse utilisée pour afficher une application en plein écran est pivotée.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: Énumération D3DDISPLAYROTATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8defdc206e88750125d88c50e86484428c0dedbd7c18575e26504d7445cd3f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804934"
---
# <a name="d3ddisplayrotation-enumeration"></a>Énumération D3DDISPLAYROTATION

Spécifie la manière dont l’analyse utilisée pour afficher une application en plein écran est pivotée.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**\_Identité D3DDISPLAYROTATION**
</dt> <dd>

L’affichage n’est pas pivoté.

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

L’affichage est pivoté de 90 degrés.

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

L’affichage est pivoté de 180 degrés.

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

L’affichage est pivoté de 270 degrés.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée dans [**IDirect3D9Ex :: GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex :: GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)et [**IDirect3DSwapChain9Ex :: GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).

Les applications peuvent choisir de gérer la rotation des analyses elles-mêmes à l’aide du [ \_ NOAUTOROTATE D3DPRESENTFLAG](d3dpresentflag.md). dans ce cas, l’application doit savoir comment l’analyse est pivotée pour qu’elle puisse ajuster son rendu en conséquence.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




