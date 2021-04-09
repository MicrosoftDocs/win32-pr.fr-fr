---
description: Définit des constantes qui décrivent le type de mémoire tampon d’arrière-plan.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: Énumération D3DBACKBUFFER_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953817"
---
# <a name="d3dbackbuffer_type-enumeration"></a>\_Énumération de type D3DBACKBUFFER

Définit des constantes qui décrivent le type de mémoire tampon d’arrière-plan.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**TYPE de D3DBACKBUFFER \_ \_ mono**
</dt> <dd>

Spécifie une chaîne d’échange stéréo.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER \_ type \_ gauche**
</dt> <dd>

Spécifie le côté gauche d’une paire stéréo dans une chaîne de permutation.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER \_ type \_ droit**
</dt> <dd>

Spécifie le côté droit d’une paire stéréo dans une chaîne de permutation.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ type \_ force \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Direct3D 9 ne prend pas en charge la vue stéréo, donc Direct3D n’utilise pas les \_ \_ valeurs de type D3DBACKBUFFER Left et D3DBACKBUFFER \_ type \_ Right de ce type énuméré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
