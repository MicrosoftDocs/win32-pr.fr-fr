---
description: Un littéral est une chaîne de caractères qui représente une valeur dans une instruction de requête. Vous utilisez des littéraux pour comparer des valeurs de colonne ou pour spécifier des termes de recherche. La recherche Windows prend en charge les types de littéraux suivants.
ms.assetid: cc526174-3c91-402d-b7d0-69fc9a61c3f9
title: Littéraux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e066f62a39bc46ec2ff7bf44c187d33f3832ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536964"
---
# <a name="literals"></a>Littéraux

Un littéral est une chaîne de caractères qui représente une valeur dans une instruction de requête. Vous utilisez des littéraux pour comparer des valeurs de colonne ou pour spécifier des termes de recherche. La recherche Windows prend en charge les types de littéraux suivants.


-   Les **littéraux de chaîne** peuvent avoir n’importe quelle longueur et peuvent contenir des caractères ANSI ou Unicode. Vous devez placer des littéraux de chaîne entre guillemets simples ('). Pour inclure un guillemet simple à l’intérieur d’un littéral de chaîne, utilisez deux guillemets simples (' '). Représente une chaîne vide sous la forme de deux guillemets simples consécutifs (' ').
-   Les **littéraux numériques** peuvent contenir les chiffres 0-9, un point et la lettre e (ou e). Les littéraux numériques représentent des nombres, y compris des entiers positifs et négatifs, des nombres décimaux et des valeurs monétaires. Les littéraux numériques peuvent être définis à l’aide de la notation scientifique (par exemple, 2.3 E-05). Ne placez pas un littéral numérique entre guillemets simples, ou il sera interprété comme un littéral de chaîne et comparé à l’aide des techniques de comparaison de chaînes. Les valeurs monétaires ne peuvent pas contenir de symboles monétaires.
-   Les **littéraux hexadécimaux** peuvent contenir les chiffres 0-9 et les lettres a-f et a-f. Un littéral hexadécimal représente un entier non signé spécifié en notation hexadécimale. Les littéraux hexadécimaux doivent commencer par 0x.
    > [!Note]  
    > La norme SQL-92 requiert que les littéraux hexadécimaux soient placés entre guillemets simples ; Toutefois, Windows Search ne prend pas en charge cette notation.

     

-   Les **littéraux booléens** représentent des valeurs logiques, et peuvent avoir la **valeur true** ou **false**. Ne placez pas un littéral booléen entre des guillemets simples, ou il est interprété comme un littéral de chaîne.
-   Les **littéraux de date** représentent des dates spécifiques, des horodatages ou des heures relatives, et sont placés entre guillemets simples. Vous devez placer les dates au format année/mois/jour heures : minutes : secondes ou année-mois-jour heures : minutes : secondes, où le mois, le jour et l’année sont des nombres. Spécifiez l’année avec une valeur à quatre chiffres, par exemple 2004. Les valeurs d’heure doivent être au format heures : minutes : secondes. La syntaxe temporelle relative est basée sur la [fonction DATEADD](-search-sql-dateadd.md).

 

 



