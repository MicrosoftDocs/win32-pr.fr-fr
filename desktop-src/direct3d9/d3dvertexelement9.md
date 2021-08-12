---
description: Définit la disposition des données de vertex. Chaque vertex peut contenir un ou plusieurs types de données, et chaque type de données est décrit par un élément vertex.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: D3DVERTEXELEMENT9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cda5b92170ef21f7bb66233f0748afe0c780837bbcb0eee9ef3c970880070422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527293"
---
# <a name="d3dvertexelement9-structure"></a>D3DVERTEXELEMENT9, structure

Définit la disposition des données de vertex. Chaque vertex peut contenir un ou plusieurs types de données, et chaque type de données est décrit par un élément vertex.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a>Membres

<dl> <dt>

**Train**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Numéro de flux.

</dd> <dt>

**Offset**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Décalage entre le début des données de vertex et les données associées au type de données particulier.

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Type de données spécifié en tant que [**D3DDECLTYPE**](./d3ddecltype.md). Un des nombreux types prédéfinis qui définissent la taille des données. Certaines méthodes ont un type implicite.

</dd> <dt>

**Méthode**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

La méthode spécifie le traitement du paveur, qui détermine comment le du paveur interprète (ou fonctionne) les données de vertex. Pour plus d’informations, consultez [**D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Définit ce à quoi les données seront utilisées ; autrement dit, l’interopérabilité entre la disposition des données de vertex et les nuanceurs de sommets. Chaque utilisation agit pour lier une déclaration de vertex à un nuanceur de sommets. Dans certains cas, ils ont une interprétation spéciale. Par exemple, un élément qui spécifie D3DDECLUSAGE \_ normal ou \_ la position D3DDECLUSAGE est utilisé par le du paveur de patch N pour configurer le pavage. Pour obtenir la liste des sémantiques disponibles, consultez [**D3DDECLUSAGE**](./d3ddeclusage.md) . D3DDECLUSAGE \_ texcoord peut être utilisé pour les champs définis par l’utilisateur (qui n’ont pas d’utilisation existante définie).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Modifie les données d’utilisation pour permettre à l’utilisateur de spécifier plusieurs types d’utilisation.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les données de vertex sont définies à l’aide d’un tableau de structures **D3DVERTEXELEMENT9** . Utilisez [**D3DDECL \_ end**](d3ddecl-end.md) pour déclarer le dernier élément de la déclaration.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Déclaration de vertex (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
