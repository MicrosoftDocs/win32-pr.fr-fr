---
description: Le prédicat LIKE effectue une comparaison de critères spéciaux sur la colonne spécifiée.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Prédicat LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516426"
---
# <a name="like-predicate"></a>Prédicat LIKE

Le prédicat LIKE effectue une comparaison de critères spéciaux sur la colonne spécifiée. Il utilise la syntaxe suivante :


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<column>Peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité. La colonne est limitée aux propriétés dans la Banque de propriétés.

Le <littéral de caractère générique \_> est un littéral de chaîne. Elle est placée entre guillemets et peut éventuellement contenir des caractères génériques. La chaîne de correspondance peut contenir plusieurs caractères génériques si nécessaire. Le tableau suivant décrit les caractères génériques reconnus par le prédicat LIKE.



| Caractère générique                | Description                                                                                                                                                                                     | Exemple                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| % (pourcentage)             | Représente zéro, un ou plusieurs caractères.                                                                                                                                                         | « COMP% r » correspond à « COMP » suivi de zéro, un ou plusieurs caractères, se terminant par r.                                                                                                                                  |
| \_ (trait de soulignement)         | Représente n'importe quel caractère unique.                                                                                                                                                                   | « COMP \_ RET » correspond à « COMP » suivi de exactement un caractère quelconque, suivi de « ter ».                                                                                                                              |
| \[\](crochets) | Correspond à n’importe quel caractère unique dans la plage ou l’ensemble spécifié. Par exemple, \[ a-z \] spécifie une plage ; \[ AEIOU \] spécifie le jeu de voyelles.                                                  | « COMP \[ a-z \] re » correspond à « COMP » suivi d’un caractère unique dans la plage de a à z, suivi de « is ». « COMP \[ AO \] » correspond à « COMP » suivi d’un caractère unique qui doit être un ou un o.<br/> |
| \[^ \] signe insertion          | Correspond à n’importe quel caractère unique qui ne se trouve pas dans la plage ou l’ensemble spécifié. Par exemple, \[ ^ a-z \] spécifie une plage qui exclut de a à z ; \[ ^ AEIOU \] spécifie un jeu qui exclut les voyelles. | « COMP \[ ^ u \] » correspond à « COMP » suivi d’un caractère unique qui n’est pas un u.                                                                                                                                        |



 

Si vous créez des prédicats avec plusieurs plages, les plages doivent être dans l’ordre.

> [!Note]  
> Pour mettre en correspondance les caractères génériques comme des caractères littéraux pour la correspondance et non comme des caractères génériques, placez le caractère entre crochets. Par exemple, pour faire correspondre le signe de pourcentage, utilisez' \[ % \] '

 

## <a name="examples"></a>Exemples


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Comparaison de valeurs littérales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Prédicat NULL](-search-sql-null.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




