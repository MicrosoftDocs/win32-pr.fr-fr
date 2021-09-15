---
title: Structure des attributs d’intersection
description: Structure déclarée en HLSL pour représenter des attributs d’accès pour l’intersection de triangle de fonction fixe ou le cadre englobant aligné sur l’axe pour l’intersection de la primitive procédurale.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518844"
---
# <a name="intersection-attributes-structure"></a>Structure des attributs d’intersection 

Structure déclarée en HLSL pour représenter des attributs d’accès pour l’intersection de triangle de fonction fixe ou le cadre englobant aligné sur l’axe pour l’intersection de la primitive procédurale.

## <a name="fixed-function-triangle-intersection"></a>Intersection de triangle de fonction fixe

La structure suivante est déclarée en HLSL pour représenter des attributs d’accès pour l’intersection de triangle de fonction fixe :


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Les](any-hit-shader.md) nuanceurs atteints et les nuanceurs [atteints les plus proches](closest-hit-shader.md) , appelés à l’aide d’une intersection de triangle à fonction fixe, doivent utiliser cette structure pour les attributs d’accès. Les attributs donnés a0, a1 et a2 pour les 3 vertex d’un triangle, barycentrics. x est le poids de a1 et barycentrics. y est le poids de a2.  Par exemple, l’application peut interpoler en procédant comme suit : a = a0 + barycentrics. x * (a1-a0) + barycentrics. y * (a2 – a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Cadre englobant aligné sur l’axe pour l’intersection de la primitive procédurale

Lorsque les zones englobantes alignées sur l’axe sont utilisées pour l’intersection avec les primitives procédurales, un nuanceur d’intersection est déclenché.  Ce nuanceur fournit une structure d’attribut d’intersection définie par l’utilisateur à l’appel [**ReportHit**](reporthit-function.md) .  Les nuanceurs d’atteinte et les nuanceurs atteints les plus proches dans le même groupe d’accès avec ce nuanceur d’intersection doivent utiliser la même structure pour les attributs de positionnement, même si les attributs ne sont pas référencés.  La taille maximale de la structure des attributs est de 32 octets, définie comme **\_ \_ \_ taille d’attribut D3D12 RAYTRACING Max \_ \_ en \_ octets**.


