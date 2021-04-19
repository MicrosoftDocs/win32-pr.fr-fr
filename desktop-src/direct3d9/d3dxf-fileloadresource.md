---
description: Identifie les données de ressource.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Structure D3DXF_FILELOADRESOURCE (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531540"
---
# <a name="d3dxf_fileloadresource-structure"></a>D3DXF \_ FILELOADRESOURCE, structure

Identifie les données de ressource.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a>Membres

<dl> <dt>

**hModule**
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle du module contenant la ressource à charger. Si ce membre a la **valeur null**, la ressource doit être attachée au fichier exécutable qui l’utilisera.

</dd> <dt>

**lpName**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers une chaîne spécifiant le nom de la ressource à charger. Par exemple, si la ressource est un maillage, ce membre doit spécifier le nom du fichier de maillage.

</dd> <dt>

**lpType**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers une chaîne qui spécifie le type défini par l’utilisateur qui identifie la ressource.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure identifie une ressource à charger lorsqu’une application utilise la méthode [**CreateEnumObject**](id3dxfile--createenumobject.md) et spécifie l’indicateur [D3DXF \_ FILELOAD \_ FROMRESOURCE](d3dxf.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de fichiers D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
