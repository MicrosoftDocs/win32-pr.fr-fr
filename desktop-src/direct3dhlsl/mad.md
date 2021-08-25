---
title: mad (fonction)
description: Effectue une opération de multiplication/ajout arithmétique sur trois valeurs.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- fonction Mad (HLSL)
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52e0e4819e4c78f092ee99c78403ace5d0205037db3096dfe45865c2216d486d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788819"
---
# <a name="mad-function"></a>mad (fonction)

Effectue une opération de multiplication/ajout arithmétique sur trois valeurs.

## <a name="syntax"></a>Syntaxe

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*mvalue* \[ dans\]
</dt> <dd>

Type : **numérique**

Valeur de multiplication.

</dd> <dt>

*une valeurqui* \[ dans\]
</dt> <dd>

Type : **numérique**

Première valeur d’addition.

</dd> <dt>

*bValue* \[ dans\]
</dt> <dd>

Type : **numérique**

Deuxième valeur d’addition.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **numérique**

Résultat de *mvalue* \* *une valeurqui*  +  *bValue*.

## <a name="remarks"></a>Remarques

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Les auteurs de nuanceur peuvent utiliser le intrinsèques **Mad** pour cibler explicitement l’instruction matérielle **Mad** dans la sortie de nuanceur compilé, ce qui est particulièrement utile avec les nuanceurs qui marquent les résultats avec le mot clé [precise](dx-graphics-hlsl-appendix-keywords.md) . L’instruction **Mad** peut être implémentée dans le matériel en tant que « fusible », ce qui offre une plus grande précision que l’implémentation d’une instruction **mul** suivie d’une instruction **Add** ou d’un ajout de **mul**  +  .

Si les auteurs de nuanceur utilisent le intrinsèques **Mad** pour calculer un résultat marqué comme précis par le nuanceur, ils indiquent au matériel d’utiliser toute implémentation valide de l’instruction **Mad** (à fusible ou non) tant que l’implémentation est cohérente pour toutes les utilisations de cet intrinsèque **Mad** dans tout nuanceur sur ce matériel. Les nuanceurs peuvent ensuite tirer parti des améliorations potentielles en matière de performances à l’aide d’une instruction **Mad** native (par opposition à l’ajout d' **mul**  +  ) sur un matériel. Le résultat de l’exécution d’une instruction matérielle **Mad** Native peut être différent de l’exécution d’un **mul** suivi d’un **Ajout**. Toutefois, quel que soit le résultat, le résultat doit être cohérent pour que la même opération se produise dans plusieurs nuanceurs ou différentes parties d’un nuanceur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




