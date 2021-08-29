---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Activer l’instanciation de nuanceur Geometry.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d0ec89be2d75b591315bd4b38ff495426d98e5ce941b2eb6bc9028ba647620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950629"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a>\_vGSInstanceID d’entrée DCL (SM5-ASM)

Activer l’instanciation de nuanceur Geometry.



| \_vGSInstanceID d’entrée DCL, instanceCount |
|-----------------------------------------|



 



| Élément                                                                                                                       | Description                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*<br/> | \[dans \] l’ID d’instance.<br/>    |
| <span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*<br/> | \[dans \] le nombre d’instances.<br/> |



 

## <a name="remarks"></a>Remarques

Le paramètre *instanceCount* de la déclaration spécifie le nombre d’instances que le nuanceur Geometry doit exécuter pour chaque primitive d’entrée. La valeur maximale pour *instanceCount* est 32.

Le nombre maximal de vertex déclarés pour la sortie, via [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), s’applique individuellement à chaque instance.

Le nombre d’instances dans cette déclaration, multiplié par le nombre maximal de vertex par instance via la [**\_ maxOutputVertexCount DCL**](dcl-maxoutputvertexcount.md), doit être <= 1024.

La quantité de données qu’une instance de nuanceur Geometry donnée peut émettre est 1024 scalaires maximum, validée en comptant toutes les valeurs scalaires déclarées pour l’entrée et en la multipliant par le nombre de vertex de sortie déclaré.

L’utilisation de l’instanciation de nuanceur Geometry augmente efficacement la quantité totale de données qui peuvent être émises par primitive d’entrée. 1024 Scalar pour une instance unique produit jusqu’à 1024 \* 32 scalaires de données de sortie sur toutes les instances de nuanceur Geometry pour une seule primitive d’entrée. Toutefois, plus le nombre d’instances est élevé, plus le nombre de vertex de chaque instance peut être émis. Une seule instance (sans instanciation) peut émettre 1024 sommets. Si vous déclarez \* 32 instances, cela signifie que chaque instance peut uniquement produire des sommets 1024/32 = 32.

La déclaration d’instanciation du nuanceur Geometry met à la disposition du programme un registre d’entrée d’entier 32 bits autonome, *vGSInstanceID*. Chaque instance de nuanceur Geometry est identifiée par la valeur contenue dans *vGSInstanceID* \[ 0, 1, 2... \] .

*vGSInstanceID* ne fait pas partie du tableau de vertex d’entrée du nuanceur de géométrie (par exemple, 3 sommets lors de l’entrée d’un triangle). Le Registre *vGSInstanceID* est autonome, comme vPrimitiveID.

Lorsque chaque instance de nuanceur Geometry se termine, il existe une coupe implicite de la topologie de sortie, de sorte que les instances consécutives ne dépendent pas les unes des autres.

Bien que le matériel puisse exécuter chaque instance de nuanceur Geometry en parallèle, la sortie de toutes les instances à la fin est sérialisée comme si tous les appels de nuanceur Geometry d’instance aient été exécutés de manière séquentielle dans une boucle qui itère *vGSInstanceID* de 0 à *instanceCount*-1, avec des coupes de topologie de sortie implicites à la fin de chaque instance.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





