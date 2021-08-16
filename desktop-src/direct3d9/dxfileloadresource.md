---
description: Identifie les données de ressource. Action déconseillée.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: DXFILELOADRESOURCE, structure (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 54d0072d7c87f6d26483faf8c591ea7651eff29b411643eb9848de11ff50d899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803036"
---
# <a name="dxfileloadresource-structure"></a>DXFILELOADRESOURCE, structure

Identifie les données de ressource. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
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

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers une chaîne spécifiant le nom de la ressource à charger. Par exemple, si la ressource est un maillage, ce membre doit spécifier le nom du fichier de maillage.

</dd> <dt>

**lpType**
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers une chaîne qui spécifie le type défini par l’utilisateur qui identifie la ressource.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure identifie une ressource à charger lorsqu’une application utilise la méthode [**CreateEnumObject**](idirectxfile--createenumobject.md) et spécifie DXFILELOAD \_ FROMRESOURCE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de fichiers X](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[Constantes DXFILE](dxfile.md)
</dt> </dl>

 

 
