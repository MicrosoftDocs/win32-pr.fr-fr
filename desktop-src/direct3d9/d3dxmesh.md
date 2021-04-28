---
description: 'Énumération D3DXMESH : indicateurs utilisés pour spécifier les options de création d’une maille.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Énumération D3DXMESH (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098097"
---
# <a name="d3dxmesh-enumeration"></a>Énumération D3DXMESH

Indicateurs utilisés pour spécifier les options de création d’une maille.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**\_32 bits D3DXMESH**
</dt> <dd>

Le maillage a des index 32 bits plutôt que des index 16 bits. Consultez la section Notes.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ DONOTCLIP**](d3dusage.md) pour les mémoires tampons de vertex et d’index.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**POINTS de D3DXMESH \_**
</dt> <dd>

Utilisez l’indicateur d’utilisation de [**\_ points D3DUSAGE**](d3dusage.md) pour les mémoires tampons de vertex et d’index.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ RTPATCHES**](d3dusage.md) pour les mémoires tampons de vertex et d’index.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**
</dt> <dd>

Si cet indicateur est spécifié, la mémoire tampon de vertex et d’index du maillage est créée avec l’indicateur [**D3DUSAGE \_ NPATCHES**](d3dusage.md) . Cela est obligatoire si l’objet Mesh doit être rendu à l’aide de l’amélioration N-patch à l’aide de Direct3D.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) pour les mémoires tampons de vertex.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ managé**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**\_ managée D3DPOOL**](./d3dpool.md) pour les mémoires tampons de vertex.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) pour les mémoires tampons de vertex.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ dynamique**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**\_ dynamique D3DUSAGE**](d3dusage.md) pour les mémoires tampons de vertex.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) pour les mémoires tampons de vertex.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) pour les mémoires tampons d’index.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ géré**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**\_ managé D3DPOOL**](./d3dpool.md) pour les mémoires tampons d’index.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) pour les mémoires tampons d’index.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ dynamique**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**\_ dynamique D3DUSAGE**](d3dusage.md) pour les mémoires tampons d’index.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**
</dt> <dd>

Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) pour les mémoires tampons d’index.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_Partage VB \_ D3DXMESH**
</dt> <dd>

Force les maillages clonés à partager des mémoires tampons de vertex.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**
</dt> <dd>

Utilisez uniquement le traitement matériel. Pour les appareils en mode mixte, cet indicateur oblige le système à utiliser le matériel (s’il est pris en charge dans le matériel) ou à traiter par défaut le logiciel.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**
</dt> <dd>

Équivaut à spécifier à la fois D3DXMESH \_ VB \_ SYSTEMMEM et D3DXMESH \_ IB \_ SYSTEMMEM.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**Géré par D3DXMESH \_**
</dt> <dd>

Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Managed et D3DXMESH \_ IB \_ Managed.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**
</dt> <dd>

Équivaut à spécifier à la fois D3DXMESH \_ VB \_ WRITEONLY et D3DXMESH \_ IB \_ WriteOnly.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dynamique**
</dt> <dd>

Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Dynamic et D3DXMESH \_ IB \_ Dynamic.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**
</dt> <dd>

Équivaut à spécifier à la fois D3DXMESH \_ VB \_ SOFTWAREPROCESSING et D3DXMESH \_ IB \_ SOFTWAREPROCESSING.

</dd> </dl>

## <a name="remarks"></a>Notes 

Une maille 32 bits (D3DXMESH \_ 32 bits) peut théoriquement prendre en charge (2 ^ 32)-1 face et vertex. Toutefois, l’allocation de mémoire pour une maille qui est importante sur un système d’exploitation 32 bits n’est pas pratique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
