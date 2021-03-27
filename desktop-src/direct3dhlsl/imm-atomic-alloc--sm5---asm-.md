---
title: imm_atomic_alloc (SM5-ASM)
description: Incrémentez atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajoutez la vue d’accès non ordonné (UAV), en retournant la valeur d’origine.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679150"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>IMM \_ Atomic \_ Alloc (SM5-ASM)

Incrémentez atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajoutez la vue d’accès non ordonné (UAV), en retournant la valeur d’origine.



| IMM \_ Atomic \_ Alloc dst0 \[ . \_ \_ masque de composant unique \] , dstUAV |
|-------------------------------------------------------------|



 



| Élément                                                                                           | Description                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[dans \] contient la valeur de compteur retournée.<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[dans \] une mémoire tampon structurée UAV avec l’indicateur Count ou Append. <br/> |



 

## <a name="remarks"></a>Notes

Il existe une valeur de compteur entière non signée 32 bits associée à chaque vue de la mémoire tampon Count ou Append qui est initialisée lorsque la vue est liée au pipeline, y compris l’option permettant de conserver la valeur précédente.

Cette instruction effectue un incrément atomique de la valeur de compteur, en retournant l’original à *dst0*.

Pour un UAV Append, la valeur retournée est valide uniquement pendant la durée de l’appel du nuanceur. Après cela, l’implémentation peut réorganiser la disposition de la mémoire. Tout adressage mémoire basé sur la valeur retournée doit être limité à l’appel du nuanceur.

Pour un UAV Append, dans l’appel du nuanceur, le compilateur HLSL peut utiliser la valeur retournée comme index de struct à utiliser pour accéder à la mémoire tampon structurée. L’accès à n’importe quel index de struct autre que ceux qui sont retournés par les appels à **IMM \_ Atomic \_ Alloc** ou [ \_ consomment](imm-atomic-consume--sm5---asm-.md) des résultats indéfinis dans le sens où l’emplacement de la mémoire au sein du UAV fait l’objet d’un accès aléatoire est aléatoire et fixe uniquement pendant la durée de vie de l’appel du nuanceur.

Pour un UAV Count, la valeur retournée peut être enregistrée par l’application en tant que référence à un emplacement fixe dans le UAV qui est explicite une fois l’appel du nuanceur terminé. Tout emplacement dans un UAV Count peut toujours être accessible indépendamment de la valeur de Count.

Il n’y a pas de fixation du nombre. il est donc encapsulé en cas de dépassement de capacité.

Le même nuanceur ne peut pas tenter à la fois l' **\_ \_ allocation atomique de IMM** et le **IMM \_ Atomic \_ consommer** sur le même UAV. En outre, le GPU ne peut pas autoriser plusieurs appels de nuanceur à mélanger **\_ Atomic Atomic \_ Alloc** et **IMM \_ Atomic \_ consommer** sur le même UAV.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





