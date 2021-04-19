---
description: Définit les types d’appareils.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Énumération D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529603"
---
# <a name="d3ddevtype-enumeration"></a>Énumération D3DDEVTYPE

Définit les types d’appareils.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_HAL D3DDEVTYPE**
</dt> <dd>

Pixellisation matérielle. L’ombrage est effectué avec des logiciels, du matériel ou des transformations et éclairages mixtes.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**
</dt> <dd>

Initialisez Direct3D sur un ordinateur sur lequel aucune pixellisation matérielle ou de référence n’est disponible, et activez les ressources pour la création de contenu 3D. Consultez la section Notes.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ Ref**
</dt> <dd>

Les fonctionnalités Direct3D sont implémentées dans le logiciel ; Toutefois, le rastériseur de référence utilise des instructions d’UC spéciales à chaque fois que cela est possible.

L’appareil de référence est installé par le SDK Windows 8,0 ou une version ultérieure et est conçu comme une aide au débogage uniquement pour le développement.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Un périphérique logiciel enfichable inscrit auprès de [**IDirect3D9 :: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Toutes les méthodes de l’interface [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) qui prennent un type d’appareil **D3DDEVTYPE** échouent si D3DDEVTYPE \_ NULLREF est spécifié. Pour utiliser ces méthodes, remplacez D3DDEVTYPE \_ ref dans l’appel de méthode.

Un \_ appareil Ref D3DDEVTYPE doit être créé dans la \_ mémoire de travail D3DPOOL, sauf si des mémoires tampons de vertex et d’index sont requises. Pour prendre en charge les mémoires tampons de vertex et d’index, créez l’appareil dans la \_ mémoire D3DPOOL SYSTEMMEM.

Si D3dref9.dll est installé, Direct3D utilise le rastériseur de référence pour créer un type d' \_ appareil Ref D3DDEVTYPE, même si D3DDEVTYPE \_ NULLREF est spécifié. Si D3dref9.dll n’est pas disponible et que D3DDEVTYPE \_ NULLREF est spécifié, Direct3D ne rend ni ne présente la scène.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**\_Paramètres de création de D3DDEVICE \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
