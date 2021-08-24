---
title: Format d’effet (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: En savoir plus sur le format d’effet (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7644e433f6c19df20cb2417659cf575e0613f93b0d53f6494ad6ee1422a55b9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792069"
---
# <a name="effect-format-direct3d-11"></a>Format d’effet (Direct3D 11)

Un effet (qui est souvent stocké dans un fichier avec une extension de fichier. FX) déclare l’état du pipeline défini par un effet. L’état de l’effet peut être divisé en trois catégories :

-   [Variables](d3d11-effect-variable-syntax.md), qui sont généralement déclarées en haut d’un effet.
-   Les [fonctions](d3d11-effect-function-syntax.md), qui implémentent le code du nuanceur, ou sont utilisées comme fonctions d’assistance par d’autres fonctions.
-   [Techniques](d3d11-effect-technique-syntax.md), qui peuvent être organisées en groupes d’effets, et implémenter des séquences de rendu à l’aide d’une ou de plusieurs passes d’effet. Chaque passe définit un ou plusieurs [groupes d’États](d3d11-effect-states.md) et appelle des fonctions de nuanceur.

![diagramme des catégories de déclarations pour les effets, y compris les variables en haut, les fonctions en milieu et les techniques en bas](images/d3d10-effect-intro.png)

Le diagramme précédent montre les catégories d’état d’effet.

La définition du format binaire de l’effet se trouve dans le fichier binaire \\ EffectBinaryFormat. h dans le code source Effects.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                   | Description                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Syntaxe de la variable Effect](d3d11-effect-variable-syntax.md)<br/>   | Une variable Effect est déclarée avec la syntaxe décrite dans cette section.<br/>                                 |
| [Syntaxe d’annotation](d3d11-effect-annotation-syntax.md)<br/>      | Une annotation est une information définie par l’utilisateur, déclarée avec la syntaxe décrite dans cette section.<br/> |
| [Syntaxe des fonctions Effect](d3d11-effect-function-syntax.md)<br/>   | Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe décrite dans cette section.<br/>          |
| [Syntaxe de la technique Effect](d3d11-effect-technique-syntax.md)<br/> | Une technique d’effet est déclarée avec la syntaxe décrite dans cette section.<br/>                                |
| [Groupes d’États d’effet](d3d11-effect-states.md)<br/>               | Les États d’effet sont des paires nom-valeur sous la forme d’une expression.<br/>                                          |
| [Syntaxe de groupe d’effets](d3d11-effect-group-syntax.md)<br/>         | Un groupe d’effets est déclaré avec la syntaxe décrite dans cette section.<br/>                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur Effects 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





