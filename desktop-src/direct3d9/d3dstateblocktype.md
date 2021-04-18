---
description: Ensembles prédéfinis d’état de pipeline utilisés par les blocs d’État (consultez États de l’enregistrement et de la restauration des blocs d’État (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Énumération D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104550616"
---
# <a name="d3dstateblocktype-enumeration"></a>Énumération D3DSTATEBLOCKTYPE

Ensembles prédéfinis d’état de pipeline utilisés par les blocs d’État (consultez États de l' [enregistrement et de la restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ tout**
</dt> <dd>

Capturer l’état actuel de l' [appareil](saving-all-device-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**
</dt> <dd>

Capturer l’état actuel du [Pixel](saving-pixel-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**
</dt> <dd>

Capture l’état actuel du [vertex](saving-vertex-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. N’utilisez pas cette valeur.

</dd> </dl>

## <a name="remarks"></a>Notes

Comme le montre le diagramme suivant, l’état des vertex et des pixels est à la fois des sous-ensembles de l’état de l’appareil.

![diagramme de l’état de l’appareil, avec un état de vertex et un état de pixel comme sous-ensembles](images/statesets.png)

Il n’y a que quelques États qui sont considérés comme l’état des vertex et des pixels. Ces états sont :

-   État du rendu : D3DRS \_ FOGDENSITY
-   État du rendu : D3DRS \_ FOGSTART
-   État du rendu : D3DRS \_ FOGEND
-   État de la texture : D3DTSS \_ TEXCOORDINDEX
-   État de la texture : D3DTSS \_ TEXTURETRANSFORMFLAGS

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9::CreateStateBlock**
</dt> </dl>

 

 
