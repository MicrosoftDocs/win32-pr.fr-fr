---
description: Le prédicat CONTAINs prend en charge l’utilisation de l’astérisque ( \* ) comme caractère générique pour représenter des mots et des expressions. Vous pouvez ajouter l’astérisque uniquement à la fin du mot ou de l’expression. La présence de l’astérisque active le mode de correspondance de préfixe.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Utilisation de caractères génériques dans le prédicat CONTAINs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760a9b4b8dae1392bf5590639775ba1b4fe534c99120322c05cc16432c1fa5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944559"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a>Utilisation de caractères génériques dans le prédicat CONTAINs

Le prédicat CONTAINs prend en charge l’utilisation de l’astérisque ( \* ) comme caractère générique pour représenter des mots et des expressions. Vous pouvez ajouter l’astérisque uniquement à la fin du mot ou de l’expression. La présence de l’astérisque active le mode de correspondance de préfixe. Dans ce mode, les correspondances sont retournées si la colonne contient le mot de recherche spécifié, suivi de zéro, un ou plusieurs autres caractères. Si une expression est fournie, les correspondances sont détectées si la colonne contient tous les mots spécifiés avec zéro, un ou plusieurs autres caractères après le mot final.

## <a name="examples"></a>Exemples

Le premier exemple correspond à des documents dont la colonne de nom de fichier contient des mots commençant par « serv ». Exemples de mots correspondants : « Server », « Servers » et « service ».


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



Le deuxième exemple correspond à des documents avec une expression dans la colonne nom de fichier qui commence par « COMP » et dans laquelle le mot suivant commence par « serv ». Exemples de mots correspondants : « COMP Server », « COMP Servers » et « COMP service ».


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



L’astérisque ne fonctionne que pour la correspondance de préfixe et ne peut être placé qu’à la fin du mot ou de l’expression. il ne fonctionne pas pour la correspondance des suffixes. La syntaxe suivante n’est pas valide et ne correspond pas aux documents avec un mot de la colonne de nom de fichier se terminant par « servi ».


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Prédicat FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> </dl>

 

 



