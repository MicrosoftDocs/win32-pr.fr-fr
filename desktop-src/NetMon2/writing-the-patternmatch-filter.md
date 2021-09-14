---
description: Le filtre de correspondance de modèle indique au pilote d’accepter des frames ayant un modèle spécifique à un décalage spécifique.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Écriture du filtre PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194488"
---
# <a name="writing-the-patternmatch-filter"></a>Écriture du filtre PATTERNMATCH

Le filtre de correspondance de modèle indique au pilote d’accepter des frames ayant un modèle spécifique à un décalage spécifique. Vous pouvez spécifier au maximum quatre correspondances de modèle détaillées, qui peuvent être combinées dans des instructions AND logiques ou ou pour l’évaluation d’un pilote Moniteur réseau.

Pour implémenter des correspondances de modèle, utilisez les structures de Moniteur réseau suivantes :

-   [**FORMULE**](expression.md)
-   [**ANDEXP**](andexp.md)
-   [**PATTERNMATCH**](patternmatch.md)

Pour évaluer une instruction **ou** , combinez deux à quatre modèles correspondant à une structure [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3). Pour évaluer une instruction AND, associez-en une à quatre structures **ANDEXP** et une structure d' [**EXPRESSION**](expression.md) (AndExp1 && AndExp2).

## <a name="pattern-match-definitions"></a>Définitions de correspondance de modèle

Une correspondance de modèle unique est définie par la structure [**PATTERNMATCH**](patternmatch.md) . Une correspondance individuelle peut fonctionner de l’une des deux façons suivantes.

Normalement, le pilote prend le décalage (qui peut être \_ basé sur le décalage \_ par rapport \_ au frame, à la base du \_ décalage \_ \_ par rapport \_ au \_ protocole effectif, à la \_ \_ base du décalage par rapport à \_ \_ \_ IPX ou à la base du décalage \_ par rapport à l' \_ \_ \_ adresse IP) et commence à compter à cet endroit. Le pilote compte le décalage d’octets à partir de là, puis correspond aux données qu’il trouve avec les octets de la première longueur dans **PatternToMatch**. S’ils sont identiques et si les indicateurs de \_ correspondance de modèle \_ \_ ne sont pas définis, alors ce modèle réussit. S’ils sont différents et que les \_ indicateurs de correspondance de modèle \_ \_ n’ont pas été définis, le modèle est réussi. Dans le cas contraire, ce modèle échoue.

Ou :

Si l' \_ indicateur de port indicateurs de correspondance de modèle \_ \_ \_ spécifié est défini et que la base est définie sur la base du décalage \_ \_ par rapport \_ au \_ protocole IPX ou à la base du décalage \_ \_ par rapport \_ à l' \_ adresse IP, la comparaison est plus complexe. Tout d’abord, le pilote s’assure que le protocole de base de décalage est présent, puis le pilote vérifie que le port spécifié correspond au port dans le frame. Enfin, le pilote s’assure que le membre **PatternToMatch** correspond à avant, à l’exception près que le décalage est à partir de la fin de l’adresse IP ou IPX. Notez que si la base n’est pas l’une de ces deux, l' \_ indicateur de port indicateurs de correspondance de modèle \_ spécifié est \_ \_ ignoré et le modèle est évalué comme indiqué ci-dessus.

Pour évaluer une correspondance de modèle unique, une structure d' [**expression**](expression.md) doit avoir un membre **AndExp** contenant une correspondance de modèle unique.

La création du filtre de correspondance de modèle implique la création de structures [**PATTERNMATCH**](patternmatch.md) et leur combinaison logique avec les structures [**expression**](expression.md) et [**ANDEXP**](andexp.md) .

**Pour écrire un filtre PATTERNMATCH**

1.  Dans la structure [**ANDEXP**](andexp.md) , remplissez le tableau avec des correspondances de modèle.
2.  Remplissez la structure de l' [**expression**](expression.md) avec un tableau de membres **AndExp** .
3.  Ne dépassez pas un total de quatre correspondances de modèle pour le filtre de capture.
4.  Dans la structure [**PATTERNMATCH**](patternmatch.md) , sélectionnez un type d’indicateur.
5.  Sélectionnez une base de décalage.
6.  Énumérer une valeur de port.
7.  Définissez la valeur de décalage.
8.  Définissez la longueur du modèle.
9.  Énumérez la valeur du modèle.

## <a name="patternmatch-examples"></a>Exemples PATTERNMATCH

Ce frame représente un décalage standard.

![frame de décalage standard](images/offs-pat.png)

Le fragment de code est implémenté comme suit :

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

Ce frame représente un décalage spécifié par le port (par rapport à IPX).

![trame de décalage spécifiée par le port](images/stan-pat.png)

L’exemple de code est implémenté comme suit :

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



