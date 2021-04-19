---
description: Envoie un rayon dans une recherche de correspondances dans une structure d’accélération.
ms.assetid: ''
title: Fonction TraceRay
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106532366"
---
# <a name="traceray-function"></a>Fonction TraceRay

Envoie un rayon dans une recherche de correspondances dans une structure d’accélération.

## <a name="syntax"></a>Syntaxe
Cette définition de fonction intrinsèque est équivalente au modèle de fonction suivant :

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a>Paramètres

`AccelerationStructure`

Structure d’accélération de niveau supérieur à utiliser. La spécification d’une structure d’accélération NULL force un échec.

`RayFlags`

Combinaison valide de valeurs de [ray_flag](ray_flag.md) . Seuls les indicateurs de rayon définis sont propagés par le système, c’est-à-dire qu’ils sont visibles par l’intrinsèque du nuanceur [RayFlags](rayflags.md) .

`InstanceInclusionMask`

Entier non signé, dont les 8 derniers bits sont utilisés pour inclure ou rejeter des instances geometry en fonction du InstanceMask dans chaque instance. Par exemple :
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Entier non signé spécifiant le décalage à ajouter aux calculs d’adressage dans les tables de nuanceur pour l’indexation de groupe d’accès.  Seuls les 4 derniers bits de cette valeur sont utilisés.

`MultiplierForGeometryContributionToHitGroupIndex`

Entier non signé spécifiant le STRIDE à multiplier par *GeometryContributionToHitGroupIndex*, qui est simplement l’index de base 0 dans lequel la géométrie a été fournie par l’application dans sa structure d’accélération de niveau inférieur. Seuls les 16 bits inférieurs de cette valeur de multiplicateur sont utilisés.

`MissShaderIndex`

Entier non signé spécifiant l’index du nuanceur d’absence dans une table de nuanceur.

`Ray`

[**RayDesc**](raydesc.md) représentant le rayon à tracer.

`Payload`

Une charge utile de rayon définie par l’utilisateur, accessible à la fois pour l’entrée et la sortie par les nuanceurs appelés pendant Raytracing.  Une fois [**TraceRay**](traceray-function.md) terminé, l’appelant peut également accéder à la charge utile.

## <a name="return-value"></a>Valeur renvoyée

**void**

## <a name="remarks"></a>Notes

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur manque**](miss-shader.md)
* [**Nuanceur de création de rayon**](ray-generation-shader.md)



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




