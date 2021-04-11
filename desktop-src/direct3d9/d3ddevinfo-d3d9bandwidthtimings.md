---
description: Les métriques de débit pour vous aider à comprendre les performances d’une application.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Structure D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211721"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS, structure

Les métriques de débit pour vous aider à comprendre les performances d’une application.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a>Membres

<dl> <dt>

**MaxBandwidthUtilized**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

La bande passante ou le taux de transfert de données maximal du processeur de l’ordinateur hôte vers le GPU. Il s’agit généralement de la bande passante du bus PCI ou AGP qui connecte l’UC et le GPU.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage d’utilisation de la mémoire lors du chargement des données du processeur de l’ordinateur hôte vers le GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage du débit du vertex. Il s’agit du nombre de vertex traités par rapport au taux de traitement de vertex maximal théorique.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de débit de paramétrage des triangles. Il s’agit du nombre de triangles qui sont configurés pour la pixellisation par rapport au taux maximal de paramétrage du triangle théorique.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage du débit de remplissage des pixels. Il s’agit du nombre de pixels qui sont remplis par rapport au remplissage de pixel théorique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
