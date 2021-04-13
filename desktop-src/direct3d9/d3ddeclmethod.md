---
description: Définit la méthode de déclaration de vertex qui est une opération prédéfinie effectuée par le du paveur (ou toute routine de géométrie procédurale sur les données de vertex pendant le pavage).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Énumération D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322730"
---
# <a name="d3ddeclmethod-enumeration"></a>Énumération D3DDECLMETHOD

Définit la méthode de déclaration de vertex qui est une opération prédéfinie effectuée par le du paveur (ou toute routine de géométrie procédurale sur les données de vertex pendant le pavage).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ par défaut**
</dt> <dd>

Valeur par défaut. Le du paveur copie les données de vertex (données de spline pour les correctifs) telles quelles, sans calculs supplémentaires. Lorsque le du paveur est utilisé, cet élément est interpolé. Sinon, les données de vertex sont copiées dans le registre d’entrée. Le type d’entrée et de sortie peut être n’importe quelle valeur, mais sont toujours du même type.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ partiel**
</dt> <dd>

Calcule la tangente à un point du rectangle ou du carreau de triangle dans la direction U. Le type d’entrée peut être l’un des suivants :

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Le type de sortie est toujours D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**
</dt> <dd>

Calcule la tangente à un point du rectangle ou du carreau de triangle dans la direction V. Le type d’entrée peut être l’un des suivants :

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Le type de sortie est toujours D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**
</dt> <dd>

Calcule le normal à un point sur le rectangle ou le triangle en utilisant le produit croisé de deux tangentes. Le type d’entrée peut être l’un des suivants :

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Le type de sortie est toujours D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**\_UV D3DDECLMETHOD**
</dt> <dd>

Copiez les valeurs U, V à un point sur le rectangle ou le correctif à triangle. Cela aboutit à un float 2D. Le type d’entrée doit être défini sur D3DDECLTYPE \_ inutilisé. Le type de données de sortie est toujours D3DDECLTYPE \_ FLOAT2. Le flux d’entrée et le décalage sont également inutilisés (mais doivent avoir la valeur 0).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**\_Recherche D3DDECLMETHOD**
</dt> <dd>

Recherche d’une carte de déplacement. Le type d’entrée peut être l’un des suivants :

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4

Seuls les composants. x et. y sont utilisés pour la recherche de la carte de texture. Le type de sortie est toujours D3DDECLTYPE \_ FLOAT1. L’appareil doit prendre en charge le mappage de déplacement. Pour plus d’informations sur le mappage de déplacement, consultez [mappage de déplacement (Direct3D 9)](displacement-mapping.md). Cette constante est prise en charge uniquement par le pipeline programmable sur les données N-patch, si les N-patchs sont activés.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**
</dt> <dd>

Recherche d’une carte de décalage prééchantillonnée. Le type d’entrée doit être défini sur D3DDECLTYPE \_ inutilisé ; l’index de flux et le décalage de flux doivent avoir la valeur 0. Le type de sortie de cette opération est toujours D3DDECLTYPE \_ FLOAT1. L’appareil doit prendre en charge le mappage de déplacement. Pour plus d’informations sur le mappage de déplacement, consultez [mappage de déplacement (Direct3D 9)](displacement-mapping.md). Cette constante est prise en charge uniquement par le pipeline programmable sur les données N-patch, si les N-patchs sont activés. Cette méthode peut être utilisée uniquement avec l' \_ exemple D3DDECLUSAGE.

</dd> </dl>

## <a name="remarks"></a>Notes

Le du paveur examine la méthode pour déterminer les données à calculer à partir des données de vertex pendant le pavage. Les données de maillage doivent utiliser la valeur par défaut. Les correctifs peuvent utiliser n’importe quel autre type implémenté.

Les données de vertex sont déclarées avec un tableau de structures [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Chaque élément du tableau contient une méthode de déclaration de vertex.

En plus de l’utilisation de D3DDECLMETHOD \_ par défaut, un maillage normal peut utiliser \_ des méthodes D3DDECLMETHOD Lookup et D3DDECLMETHOD \_ LOOKUPPRESAMPLED lorsque N-patchs sont activés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




