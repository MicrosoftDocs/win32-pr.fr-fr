---
title: Type struct
description: Type struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Type struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990676"
---
# <a name="struct-type"></a>Type struct

Utilisez la syntaxe suivante pour déclarer une structure à l’aide du langage HLSL.



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| *nom* du struct { \[ *InterpolationModifier* \] *type* \[ *R* x *C* \] *MemberName*;     ... }; |



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*
</dt> <dd>

Chaîne ASCII qui identifie de façon unique le nom de la structure.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]
</dt> <dd>

Modificateur facultatif qui spécifie un type d’interpolation. Pour plus d’informations, consultez [Remarques](#remarks).

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type* \[ *R* x *C*\]
</dt> <dd>

Type de membre avec une taille de tableau de colonne (C) x de *ligne (**C*) facultative. Une structure contient au moins un élément ; s’il contient plus d’un élément, les éléments sont tous du même type. Le nombre de lignes et de colonnes est un entier non signé compris entre 1 et 4 inclus.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*
</dt> <dd>

Chaîne ASCII qui identifie de façon unique le nom du membre.

</dd> </dl>

## <a name="remarks"></a>Notes

Un modificateur d’interpolation peut être spécifié sur n’importe quel membre de structure ou sur un argument d’une fonction de nuanceur de pixels. Si un modificateur apparaît aux deux emplacements, le modificateur outside (modificateur d’argument de nuanceur de pixels) est en cours de la même façon que le modificateur interne (modificateur de structure).

Lors de la compilation d’un nuanceur ou d’un effet, le compilateur de nuanceur compresse les membres de structure conformément aux [règles de compression HLSL](dx-graphics-hlsl-packing-rules.md).

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Modificateurs d’interpolation introduits dans le Shader Model 4

Les sorties de nuanceur de sommets utilisées pour les entrées de nuanceur de pixels sont interpolées de manière linéaire pour obtenir des valeurs par pixel pendant la pixellisation. Pour définir la méthode d’interpolation, utilisez l’une des valeurs suivantes, qui sont prises en charge dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) ou version ultérieure. Le modificateur est ignoré sur toute sortie de nuanceur de vertex qui n’est pas utilisée comme entrée de nuanceur de pixels.



| Modificateur d’interpolation | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **proportionnelle**             | Interpoler entre les entrées de nuanceur ; **linéaire** est la valeur par défaut si aucun modificateur d’interpolation n’est spécifié.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **centroïde**           | Interpoler entre des échantillons situés quelque part dans la zone couverte du pixel (cela peut nécessiter l’extrapolation des points de terminaison à partir d’un centre de pixels). L’échantillonnage de centre de gravité peut améliorer l’anticrénelage si un pixel est partiellement couvert (même si le centre de pixels n’est pas couvert). Le modificateur de centre de **gravité** doit être combiné avec le modificateur **Linear** ou **noperspective** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **nointerpolation**    | Ne pas interpoler.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | N’effectuez pas de correction de perspective pendant l’interpolation. Le modificateur **noperspective** peut être combiné avec le modificateur de centre de **gravité** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **exemple**             | **Disponible dans le modèle de nuanceur 4,1 et versions ultérieures** Interpoler à l’emplacement de l’échantillon plutôt qu’au centre de pixels. Le nuanceur de pixels s’exécute par exemple plutôt que par pixel. Une autre façon d’effectuer une exécution par exemple consiste à avoir une entrée avec la valeur [sémantique SV \_ SampleIndex](dx-graphics-hlsl-semantics.md), qui indique l’exemple actuel. Seules les entrées avec l' **échantillon** spécifié (ou l’entrée de SV \_ SampleIndex) diffèrent entre les appels de nuanceur du pixel, alors que d’autres entrées qui ne spécifient pas de modificateurs (par exemple, si vous mélangez des modificateurs sur des entrées différentes) sont toujours interpolées au centre de pixels. L’appel de nuanceur de pixels et le test de profondeur/stencil se produisent pour chaque échantillon couvert dans le pixel. Cela est parfois appelé *superéchantillonnage*. En revanche, en l’absence d’un exemple d’appel de fréquence, connu sous le nom d' *échantillonnage multiple*, le nuanceur de pixels est appelé une fois par pixel, quel que soit le nombre d’échantillons couverts, tandis que le test de profondeur/stencil se produit à la fréquence d’échantillonnage. Les deux modes offrent un anticrénelage de bord équivalent. Toutefois, le superéchantillonnage offre une meilleure qualité d’ombrage en invoquant le nuanceur de pixels plus fréquemment.<br/> |



 

<dl> 1. En cas d’utilisation d’un type int/uint, la seule option valide est **nointerpolation**.  
</dl>

Les modificateurs d’interpolation peuvent être appliqués à des membres de structure ou à des [arguments de fonction](dx-graphics-hlsl-function-parameters.md), ou les deux.

## <a name="examples"></a>Exemples

Voici quelques exemples de déclarations de structure.


```
struct struct1
{
  int    a;
}
```



Cette déclaration comprend un tableau.


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



Cette déclaration comprend un modificateur d’interpolation.


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





