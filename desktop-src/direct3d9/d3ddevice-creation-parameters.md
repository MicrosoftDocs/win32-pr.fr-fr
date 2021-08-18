---
description: Décrit les paramètres de création d’un appareil.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Structure D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 64b3e13300d6c305d06b6b13db246134cb889cbfc407e4a99c6ae45adbf916e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805018"
---
# <a name="d3ddevice_creation_parameters-structure"></a>Structure des paramètres de \_ création de D3DDEVICE \_

Décrit les paramètres de création d’un appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a>Membres

<dl> <dt>

**AdapterOrdinal**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre ordinal qui désigne l’adaptateur d’affichage. \_La valeur par défaut de D3DADAPTER est toujours la carte d’affichage principale. Utilisez cet ordinal comme paramètre d’adaptateur pour l’une des méthodes [**IDirect3D9**](/windows/desktop/api) . Notez que les différentes instances d’objets Direct3D 9,0 peuvent utiliser des ordinaux différents. Les adaptateurs peuvent entrer ou sortir un système lorsque les utilisateurs ajoutent ou suppriment des analyses d’un système à plusieurs écrans ou lorsqu’ils échangent à chaud un ordinateur portable. Par conséquent, utilisez cet ordinal uniquement dans une instance Direct3D 9,0 connue comme valide, c’est-à-dire, soit le Direct3D 9,0 qui a créé cette interface [**IDirect3DDevice9**](/windows/desktop/api) , soit le Direct3D 9,0 retourné par [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), comme il a été appelé via cette interface **IDirect3DDevice9** .

</dd> <dt>

**DeviceType**
</dt> <dd>

Type : **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Membre du type énuméré [**D3DDEVTYPE**](./d3ddevtype.md) . Indique la quantité de fonctionnalités émulées pour cet appareil. La valeur de ce paramètre reflète la valeur passée à l’appel [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) qui a créé cet appareil.

</dd> <dt>

**hFocusWindow**
</dt> <dd>

Type : **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle de fenêtre auquel le focus appartient pour cet appareil Direct3D. La valeur de ce paramètre reflète la valeur passée à l’appel [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) qui a créé cet appareil.

</dd> <dt>

**BehaviorFlags**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinaison d’une ou de plusieurs constantes [D3DCREATE](d3dcreate.md) qui contrôlent le comportement global de l’appareil. Ces constantes reflètent les constantes transmises à [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) lorsque l’appareil a été créé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetCreationParameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
