---
description: Un nuanceur qui est appelé quand les intersections de rayon ne sont pas opaques.
ms.assetid: ''
title: Tout nuanceur de correspondance
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519285"
---
# <a name="any-hit-shader"></a>Tout nuanceur de correspondance

Un nuanceur qui est appelé quand les intersections de rayon ne sont pas opaques. 

Les nuanceurs d’accès doivent déclarer un paramètre de charge utile suivi d’un paramètre d’attributs. Chacun de ces paramètres doit être un type de structure défini par l’utilisateur correspondant aux types utilisés pour [**TraceRay**](traceray-function.md) et [**ReportHit**](reporthit-function.md) respectivement, ou la [**structure d’attributs d’intersection**](intersection-attributes.md) quand l’intersection de triangle de fonction fixe est utilisée.

Les nuanceurs d’accès peuvent effectuer les types d’opérations suivants :

*   Lire et modifier la charge utile Ray : (INOUT payload_t rayPayload)
*   Lire les attributs d’intersection : (dans attr_t attributs)
*   Appelez [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), qui accepte l’accès actuel, met fin au [nuanceur de correspondance](any-hit-shader.md), termine le [nuanceur d’intersection](intersection-shader.md) s’il y en a un, puis exécute le [nuanceur de correspondance](closest-hit-shader.md) le plus proche sur le point le plus proche, jusqu’à présent, s’il est actif.
*   Appelez [**IgnoreHit**](ignorehit-function.md), qui met fin au nuanceur de correspondance et indique au système de continuer à rechercher les résultats, y compris le renvoi du contrôle à un nuanceur d’intersection, s’il est en cours d’exécution, en renvoyant false à partir du site d’appel [**ReportHit**](reporthit-function.md)*. 
*   Retourne sans appeler l’une de ces fonctions intrinsèques, qui accepte l’accès actuel et indique au système de continuer à rechercher les correspondances, y compris le retour du contrôle au nuanceur d’intersection le cas échéant, en retournant la valeur true sur le site d’appel [**ReportHit**](reporthit-function.md) pour indiquer que l’accès a été accepté.

Même si un appel de nuanceur atteint se termine par [**IgnoreHit**](ignorehit-function.md) ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), toutes les modifications apportées à la charge utile de rayon jusqu’à présent doivent toujours être conservées.

## <a name="shader-type-attribute"></a>Attribut de type Shader

```
[shader("anyhit")]
```

## <a name="example"></a>Exemple

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
