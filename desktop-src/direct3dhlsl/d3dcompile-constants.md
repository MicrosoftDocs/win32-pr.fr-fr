---
title: Constantes D3DCOMPILE (D3DCompiler. h)
description: Les constantes D3DCOMPILE spécifient la façon dont le compilateur compile le code HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211701"
---
# <a name="d3dcompile-constants"></a>Constantes D3DCOMPILE

Les constantes D3DCOMPILE spécifient la façon dont le compilateur compile le code HLSL.

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**Débogage D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Indique au compilateur d’insérer les informations de fichier de débogage/ligne/type/symbole dans le code de sortie.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ ignorer la \_ validation**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Indique au compilateur de ne pas valider le code généré par rapport aux capacités et contraintes connues. Nous vous recommandons d’utiliser cette constante uniquement avec les nuanceurs qui ont été compilés avec succès par le passé. DirectX valide toujours les nuanceurs avant de les définir sur un appareil.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ ignorer l' \_ optimisation**
</dt> <dd> <dl> <dt>

(1 << 2)
</dt> <dt>



Indique au compilateur d’ignorer les étapes d’optimisation pendant la génération de code. Nous vous recommandons de définir cette constante uniquement à des fins de débogage.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ \_ Colonne \_ principale de la matrice D3DCOMPILE Pack**
</dt> <dd> <dl> <dt>

(1 << 3)
</dt> <dt>



Indique au compilateur d’empaqueter les matrices dans l’ordre ligne-principal de l’entrée et de la sortie du nuanceur.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_ \_ \_ Colonne \_ principale de la matrice D3DCOMPILE Pack**
</dt> <dd> <dl> <dt>

(1 << 4)
</dt> <dt>



Indique au compilateur d’empaqueter les matrices dans l’ordre des colonnes-major sur l’entrée et la sortie du nuanceur. Ce type de compression est généralement plus efficace, car une série de produits scalaires peut ensuite effectuer une multiplication de matrice vectorielle.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Précision partielle \_ D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 5)
</dt> <dt>



Indique au compilateur d’effectuer tous les calculs avec une précision partielle. Si vous définissez cette constante, le code compilé peut s’exécuter plus rapidement sur du matériel.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ force \_ / \_ logiciel \_ non \_ opt**
</dt> <dd> <dl> <dt>

(1 << 6)
</dt> <dt>



Indique au compilateur de compiler un nuanceur de sommets pour le profil de nuanceur le plus élevé suivant. Cette constante désactive le débogage et les optimisations.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ forcer \_ le \_ logiciel PS \_ non \_ opt**
</dt> <dd> <dl> <dt>

(1 << 7)
</dt> <dt>



Indique au compilateur de compiler un nuanceur de pixels pour le profil de nuanceur suivant le plus élevé. Cette constante désactive également le débogage et les optimisations.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ aucun \_ prénuanceur**
</dt> <dd> <dl> <dt>

(1 << 8)
</dt> <dt>



Indique au compilateur de désactiver les prénuanceurs. Si vous définissez cette constante, le compilateur n’extrait pas l’expression statique à des fins d’évaluation.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ éviter \_ \_ le contrôle de workflow**
</dt> <dd> <dl> <dt>

(1 << 9)
</dt> <dt>



Indique au compilateur de ne pas utiliser les constructions de contrôle de Flow dans la mesure du possible.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ préférer \_ \_ le contrôle de Flow**
</dt> <dd> <dl> <dt>

(1 << 10)
</dt> <dt>



Indique au compilateur d’utiliser des constructions de contrôle de Flow dans la mesure du possible.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ activer la \_ rigueur**
</dt> <dd> <dl> <dt>

(1 << 11)
</dt> <dt>



Force la compilation stricte, qui peut ne pas autoriser la syntaxe héritée.

Par défaut, le compilateur désactive la rigueur sur la syntaxe déconseillée.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ activer la \_ compatibilité descendante \_**
</dt> <dd> <dl> <dt>

(1 << 12)
</dt> <dt>



Indique au compilateur d’activer les nuanceurs plus anciens pour compiler sur des cibles de 5 \_ 0.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ strict**
</dt> <dd> <dl> <dt>

(1 << 13)
</dt> <dt>



Force la compilation stricte de la norme IEEE.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**\_Niveau0 d’optimisation D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 14)
</dt> <dt>



Indique au compilateur d’utiliser le niveau d’optimisation le plus bas. Si vous définissez cette constante, le compilateur peut générer du code plus lent, mais produit le code plus rapidement. Définissez cette constante lorsque vous développez le nuanceur de manière itérative.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ optimisation du \_ niveau1**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Indique au compilateur d’utiliser le deuxième niveau d’optimisation le plus bas.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE d' \_ optimisation du \_ d’isolement2**
</dt> <dd> <dl> <dt>

((1 << 14) \| (1 << 15))
</dt> <dt>



Indique au compilateur d’utiliser le deuxième niveau d’optimisation le plus élevé.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**\_Niveau3 d’optimisation D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 15)
</dt> <dt>



Indique au compilateur d’utiliser le niveau d’optimisation le plus élevé. Si vous définissez cette constante, le compilateur produit le meilleur code possible, mais peut prendre beaucoup plus de temps. Définissez cette constante pour les versions finales d’une application lorsque les performances sont le facteur le plus important.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**\_Les avertissements D3DCOMPILE \_ sont des \_ Erreurs**
</dt> <dd> <dl> <dt>

(1 << 18)
</dt> <dt>



Indique au compilateur de traiter tous les avertissements comme des erreurs lors de la compilation du code du nuanceur. Nous vous recommandons d’utiliser cette constante pour le nouveau code de nuanceur, afin de pouvoir résoudre tous les avertissements et réduire le nombre de défauts de code difficiles à trouver.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**Les \_ ressources D3DCOMPILE \_ peuvent avoir un \_ alias**
</dt> <dd> <dl> <dt>

(1 << 19)
</dt> <dt>



Indique au compilateur de supposer que les vues d’accès non ordonnées (UAVs) et les vues des ressources de nuanceur (SRVs) peuvent avoir un alias pour CS \_ 5 \_ 0.

> [!Note]  
> Cette constante de compilateur est nouvelle à partir de la \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ activer les \_ tables de \_ descripteurs non liées \_**
</dt> <dd> <dl> <dt>

(1 << 20)
</dt> <dt>



Indique au compilateur d’activer les tables de descripteurs non liées.

> [!Note]  
> Cette constante de compilateur est nouvelle à partir de la \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ toutes les \_ ressources \_ liées**
</dt> <dd> <dl> <dt>

(1 << 21)
</dt> <dt>



Indique au compilateur de s’assurer que toutes les ressources sont liées.

> [!Note]  
> Cette constante de compilateur est nouvelle à partir de la \_47.dll D3dcompiler.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





