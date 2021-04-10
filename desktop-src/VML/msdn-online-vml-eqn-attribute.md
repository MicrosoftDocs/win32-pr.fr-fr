---
title: Eqn VML (attribut)
description: Eqn VML (attribut)
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da00084a825147c6f8a05f503e5ee2679f40e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316415"
---
# <a name="vml-eqn-attribute"></a>Eqn VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit l’équation utilisée par une formule. En lecture/écriture. **Chaîne**.

**S’applique à**

[F](msdn-online-vml-f-element.md) (sous-élément de [formules](msdn-online-vml-formulas-element.md))

**Syntaxe de balise**

<v : *Element* eqn = " *expression* " >

**Syntaxe du script**

*Element* . eqn = "*expression*"

*expression* = *élément*. eqn

**Remarques**

Les équations sont définies par l’évaluation d’une expression de texte qui présente la forme générale d’une opération suivie de jusqu’à trois arguments. Chaque argument peut être de l’un des types suivants :

-   ajustement (par exemple, \# 2)
-   une autre formule (par exemple, @2 )
-   nombres fixes (par exemple, 2)
-   valeurs prédéfinies

Le tableau ci-dessous définit les formules qui peuvent être utilisées avec les arguments facultatifs en fonction des noms *v*, *P1* et *P2*. Le modèle de formule est le suivant :

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Opération | Paramètres | Exact  | Résultats                    | Description                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| multiples       | 1      | Oui    | v                         | Définit une valeur de repère à partir d’une autre valeur.                                   |
| Sum       | 3      | Oui    | v + P1-P2               | Utilisé pour l’addition et la soustraction.                                             |
| product   | 3      | arrondit | v \* P1/P2              | Utilisé pour la multiplication et la Division.                                          |
| mid       | 2      | secteur    | (v + P1)/2               | Moyenne.                                                                       |
| abs       | 1      | Oui    | ABS (v)                    | Valeur absolue.                                                                |
| minute(s)       | 2      | Oui    | min (v, P1)                 | Valeur inférieure de v et P1.                                                  |
| max       | 2      | Oui    | Max (v, P1)                 | Valeur supérieure de v et P1.                                                 |
| if        | 3      | Oui    | v > 0 ? P1 : P2        | Test conditionnel.                                                           |
| mod       | 3      | non     | sqrt (v ^ 2 + P1 ^ 2 + P2 ^ 2)   | Valeur de modulo.                                                                 |
| atan2     | 2      | non     | atan2 (P1, v)               | Valeur polaire en degrés \* 2 ^ 16 (unités FD).                                     |
| sin       | 2      | non     | \*Sin (P1)              | Sin, argument dans les degrés \* 2 ^ 16 (FD [Units](msdn-online-vml-units.md) ).     |
| cos       | 2      | non     | v \* Co (P1)              | COS, argument en degrés \* 2 ^ 16 ( [unités](msdn-online-vml-units.md) FD).     |
| cosatan2  | 3      | non     | v \* Co (atan2 (P2, P1))    | Préserve la précision complète dans le calcul intermédiaire.                           |
| sinatan2  | 3      | non     | v \* Sin (atan2 (P2, P1))    | Préserve la précision complète dans le calcul intermédiaire.                           |
| sqrt      | 1      | non     | sqrt (v)                   | Le résultat est positif et arrondit à la valeur inférieure.                                            |
| sumangle  | 3      | Oui    | v + P1 \* 2 ^ 16 + P2 \* 2 ^ 16 | v mis à l’échelle de 2 ^ 16 ; P1 et P2 sont des degrés.<br/>                            |
| ellipse   | 3      | non     | \*racine P2 (1-(v/P1) ^ 2)    | Es.                                                                       |
| tan       | 2      | non     | v \* brun (P1)              | Tangente, argument dans les degrés \* 2 ^ 16 (FD [Units](msdn-online-vml-units.md) ). |



 

Notez que l’équation se compose uniquement d’opérations et de nombres. les symboles mathématiques sont omis. Par exemple, l’équation

eqn = "Sum 5 9 3"

produit l’équivalent de

5 + 9-3

pour la valeur retournée 11. Si des opérandes sont manquants, la valeur n’est pas utilisée. Par exemple,

eqn = "Sum 5 9"

produit l’équivalent de

5 + 9

et ignorerait l’opérande manquant.

*Attribut standard VML*

**Exemple**

La formule suivante produit le résultat 6 (la somme des deux chiffres divisée par 2), qui, s’il s’agissait de la première formule, peut être récupérée par le symbole « @0 ».


```HTML
    <v:f eqn="mid 5 7"/>
```



 

