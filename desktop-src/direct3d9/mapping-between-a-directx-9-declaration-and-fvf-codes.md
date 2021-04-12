---
description: Ce tableau mappe les membres d’une déclaration D3DVERTEXELEMENT9 à un code de la Commission.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Mappage entre une déclaration Direct3D et les codes de la Commission de la Commission (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109154"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a>Mappage entre une déclaration Direct3D et les codes de la Commission de la Commission (Direct3D 9)

Ce tableau mappe les membres d’une déclaration [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) à un code de la Commission.



| Type de données             | Utilisation                      | Index d’utilisation | CLOS                       |
|-----------------------|----------------------------|-------------|---------------------------|
| D3DDECLTYPE \_ FLOAT3   | \_Position D3DDECLUSAGE     | 0           | D3DFVF \_ xyz               |
| D3DDECLTYPE \_ float4   | \_Position D3DDECLUSAGE    | 0           | D3DFVF \_ XYZRHW            |
| D3DDECLTYPE \_ floatn   | D3DDECLUSAGE \_ BLENDWEIGHT  | 0           | D3DFVF \_ XYZBn             |
| D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ BLENDINDICES | 0           | D3DFVF \_ XYZB (nWeights + 1) |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ normal       | 0           | D3DFVF \_ normal            |
| D3DDECLTYPE \_ FLOAT1   | D3DDECLUSAGE \_ psize        | 0           | D3DFVF \_ psize             |
| D3DDECLTYPE \_ D3DCOLOR | \_Couleur D3DDECLUSAGE        | 0           | \_Diffusion D3DFVF           |
| D3DDECLTYPE \_ D3DCOLOR | \_Couleur D3DDECLUSAGE        | 1           | D3DFVF \_ spéculaire          |
| D3DDECLTYPE \_ Floater   | D3DDECLUSAGE \_ texcoord     | n           | D3DFVF \_ TEXCOORDSIZEm (n)  |
| D3DDECLTYPE \_ FLOAT3   | \_Position D3DDECLUSAGE     | 1           | N/A                       |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ normal       | 1           | N/A                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration de vertex](vertex-declaration.md)
</dt> </dl>

 

 



