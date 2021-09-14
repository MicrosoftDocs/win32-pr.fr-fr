---
description: Cette section décrit la syntaxe des instructions conditionnelles utilisées par la fonction MsiEvaluateCondition et les tables de séquences d’actions. Pour plus d’informations, consultez Exemples de syntaxe d’instruction conditionnelle.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Syntaxe d’instruction conditionnelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131cf9513d4bf19bb84c5777d1fed1411a682ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092054"
---
# <a name="conditional-statement-syntax"></a>Syntaxe d’instruction conditionnelle

Cette section décrit la syntaxe des instructions conditionnelles utilisées par la fonction [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) et les [tables de séquences](using-a-sequence-table.md)d’actions. Pour plus d’informations, consultez [exemples de syntaxe d’instruction conditionnelle](examples-of-conditional-statement-syntax.md).

## <a name="summary-of-conditional-statement-syntax"></a>Résumé de la syntaxe des instructions conditionnelles

Ce tableau et la liste suivante résument la syntaxe à utiliser dans les expressions conditionnelles.



| Élément                | Syntaxe                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| value               | \|entier littéral de symbole \|                                                                                    |
| opérateur de comparaison | < \| > \| <= \| >= \| = \| <>                                                                 |
| terme                | \|Comparaison de valeurs de valeur-valeur d’opérateur \| (expression)\|                                                    |
| Facteur booléen      | terme \| **non** terme                                                                                            |
| Terme booléen        | Facteur booléen de facteur booléen \| **et** terme                                                                   |
| expression          | \|Expression **ou** expression booléenne à terme booléen                                                                  |
| symbole              | propriété \| % environment-variable \| $Component-action \| ? composant-State \| &Feature-action \| ! Feature-State |



 

-   Les noms et les valeurs de symboles respectent la casse.
-   Les noms des variables d’environnement ne respectent pas la casse.
-   Le texte littéral doit être placé entre guillemets ("texte").
    > [!Note]  
    > Le texte littéral qui contient des guillemets ne peut pas être utilisé dans des instructions conditionnelles, car il n’y a pas de caractère d’échappement pour les guillemets au sein du texte littéral. Pour effectuer une comparaison avec un texte littéral contenant des guillemets, le texte littéral doit être placé dans une propriété. Par exemple, pour vérifier que la propriété SERVERNAME ne contient pas de guillemets, définissez une propriété nommée QUOTes dans la [table Property](property-table.md) avec la valeur «et remplacez la condition par ServerName><quotes.

     

-   Les valeurs de propriété inexistantes sont traitées comme des chaînes vides.
-   Les valeurs numériques à virgule flottante ne sont pas prises en charge.
-   les opérateurs et la priorité sont les mêmes que dans les langages de base et SQL.
-   Les opérateurs arithmétiques ne sont pas pris en charge.
-   Les parenthèses peuvent être utilisées pour substituer la priorité des opérateurs.
-   Les opérateurs ne respectent pas la casse.
-   Pour les comparaisons de chaînes, un tilde « ~ » préfixé à l’opérateur effectue une comparaison qui ne respecte pas la casse.
-   La comparaison d’un entier avec une valeur de chaîne ou de propriété qui ne peut pas être convertie en entier est toujours **msiEvaluateConditionFalse**, à l’exception de l’opérateur de comparaison « <> », qui retourne **msiEvaluateConditionTrue**.

## <a name="access-prefixes"></a>Préfixes d’accès

Le tableau suivant présente les préfixes à utiliser pour accéder aux différentes informations du système et du programme d’installation à utiliser dans les expressions conditionnelles.



| Type de symbole          | Préfixe | Valeur                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Installer (propriété)   | (aucun) | Valeur de la table de propriétés ([propriété](property-table.md)). |
| Variable d’environnement | %      | Valeur de la variable d’environnement.                            |
| Clé de la table des composants  | $      | État d’action du composant.                            |
| Clé de la table des composants  | ?      | État installé du composant.                         |
| Clé de la table de fonctionnalités    | &      | État d’action de la fonctionnalité.                              |
| Clé de la table de fonctionnalités    | !      | État installé de la fonctionnalité.                           |



 

## <a name="logical-operators"></a>Opérateurs logiques

Le tableau suivant montre les opérateurs logiques dans les expressions conditionnelles, dans l’ordre de priorité de haut en bas.



| Opérateur | Signification                                                 |
|----------|---------------------------------------------------------|
| Not      | Prefix, opérateur unaire ; inverse l’état du terme suivant. |
| And      | TRUE si les deux termes sont vrais.                            |
| ou       | TRUE si l’un des termes ou les deux sont vrais.                  |
| Xor      | TRUE si les deux termes, mais pas les deux, ont la valeur TRUE.             |
| Eqv      | TRUE si les deux termes sont TRUE ou si les deux termes ont la valeur FALSe.    |
| IMP      | TRUE si le terme de gauche a la valeur FALSe ou si le terme à droite a la valeur TRUE.       |



 

## <a name="comparative-operators"></a>Opérateurs de comparaison

Le tableau suivant présente les opérateurs de comparaison utilisés dans les expressions conditionnelles. Ces opérateurs de comparaison peuvent uniquement se produire entre deux valeurs.



| Opérateur | Signification                                                     |
|----------|-------------------------------------------------------------|
| =        | TRUE si la valeur de gauche est égale à la valeur de droite.                 |
| <> | TRUE si la valeur de gauche n’est pas égale à la valeur de droite.             |
| >     | TRUE si la valeur de gauche est supérieure à la valeur de droite.             |
| >=    | TRUE si la valeur de gauche est supérieure ou égale à la valeur droite. |
| <     | TRUE si la valeur de gauche est inférieure à la valeur de droite.                |
| <=    | TRUE si la valeur de gauche est inférieure ou égale à la valeur droite.    |



 

## <a name="substring-operators"></a>Opérateurs de sous-chaîne

Le tableau suivant montre les opérateurs de sous-chaîne utilisés dans les expressions conditionnelles. Les opérateurs de sous-chaîne peuvent se produire entre deux valeurs de chaîne.



| Opérateur | Signification                                           |
|----------|---------------------------------------------------|
| >< | TRUE si la chaîne de gauche contient la chaîne de droite.    |
| << | TRUE si la chaîne de gauche commence par la chaîne de droite. |
| >> | TRUE si la chaîne de gauche se termine par la chaîne de droite.   |



 

## <a name="bitwise-numeric-operators"></a>Opérateurs numériques au niveau du bit

Le tableau suivant montre les opérateurs numériques au niveau du bit dans les expressions conditionnelles. Ces opérateurs peuvent se produire entre deux valeurs entières.



| Opérateur | Signification                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | And au niveau du bit, TRUE si les entiers de gauche et de droite ont des bits en commun.    |
| << | True si les 16 bits de poids fort de l’entier gauche sont égaux à l’entier droit. |
| >> | True si les 16 bits de poids faible de l’entier gauche sont égaux à l’entier droit.  |



 

## <a name="feature-and-component-state-values"></a>Valeurs d’état des fonctionnalités et des composants

Le tableau suivant indique où il est possible d’utiliser les symboles d’opérateur de composant et de fonctionnalité.



| État de l’opérateur &lt;&gt; | Où cette syntaxe est valide                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| action $component      | Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) . |
| &fonctionnalité-action        | Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) . |
| ! fonctionnalité-État         | Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) . |
| ? État du composant       | Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) . |



 

Le tableau suivant indique les valeurs d’état des fonctionnalités et des composants utilisées dans les expressions conditionnelles. Ces États ne sont pas définis tant que [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) n’est pas appelé, soit directement, soit par l’action [CostFinalize](costfinalize-action.md) .



| État                    | Valeur | Signification                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLSTATE \_ inconnu    | -1    | Aucune action à effectuer sur la fonctionnalité ou le composant.              |
| INSTALLSTATE \_ publié | 1     | Fonctionnalité publiée. Cet État n’est pas disponible pour les composants. |
| INSTALLSTATE \_ absent     | 2     | La fonctionnalité ou le composant n’est pas présent.                            |
| INSTALLSTATE \_ local      | 3     | Fonctionnalité ou composant sur l’ordinateur local.                     |
| \_source INSTALLSTATE     | 4     | La fonctionnalité ou le composant s’exécutent à partir de la source.                       |



 

Par exemple, l’expression conditionnelle « &MyFeature = 3 » prend la valeur true uniquement si MyFeature change de son état actuel à l’état d’installation sur l’ordinateur local, INSTALLSTATE \_ local.

Notez que vous ne devez pas dépendre de la condition $Component 1 = 3 pour vérifier si Composant1 est installé localement sur l’ordinateur. Cela peut échouer si Composant1 est installé par plusieurs produits. Une fois Composant1 installé localement par product1, le programme d’installation évalue la condition $Component 1 = 3 comme false pendant l’installation de Product2. Cela est dû au fait que le programme d’installation détermine la version du composant à l’aide du chemin d’accès de clé du composant et marque le composant pour l’installation si sa version est supérieure ou égale au composant installé.

Notez que le programme d’installation n’effectuera pas de comparaisons directes du type de données [version](version.md) dans les instructions conditionnelles. Par exemple, vous ne pouvez pas utiliser des opérateurs comparatifs pour comparer des versions telles que « 01,10 » et « 1,010 » dans une instruction conditionnelle. Au lieu de cela, utilisez une méthode valide pour rechercher une version, comme décrit dans [recherche d’applications, de fichiers, d’entrées de registre ou de .ini entrées de Registre existantes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), puis définir une propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



