---
description: Le terme proche est utilisé pour spécifier que deux termes de recherche de contenu doivent être relativement proches les uns des autres pour être reconnus comme correspondant au prédicat CONTAINs.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: À court terme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318158"
---
# <a name="near-term"></a>À court terme

Le terme proche est utilisé pour spécifier que deux termes de recherche de contenu doivent être relativement proches les uns des autres pour être reconnus comme correspondant au prédicat [Contains](-search-sql-contains.md) .

La syntaxe du terme proche est la suivante :


```
<content_search_term> NEAR | ~ <content_search_term>
```



Le terme proche peut être représenté par le mot clé « NEAR » ou par un tilde (~).

Lorsque les mots joints à proximité dans la requête se trouvent dans environ 50 mots l’un de l’autre à l’intérieur de la colonne dans laquelle la recherche est effectuée, le terme proche retourne une correspondance. Plus les deux mots sont proches, plus le classement calculé est élevé pour le terme proche. Plus les deux mots sont éloignés, plus le rang est bas.

> [!Note]  
> Le nombre de mots entre les termes de recherche trouvés est approximatif et dépend de l’apparence des mots parasites, tels que « a » ou « The », et de la manière dont séparateurs le texte. Il peut être inférieur à 50.

 


Le tableau suivant décrit les types de terme de recherche de contenu qui peuvent être utilisés avec un terme proche dans un prédicat CONTAINs.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Type</th>
<th>Description</th>
<th>Exemples</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Mot unique sans espaces ni autres signes de ponctuation. Les guillemets doubles ne sont pas nécessaires.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Expression</td>
<td>Plusieurs mots ou espaces inclus.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Caractère générique</td>
<td>Mots ou expressions avec l’astérisque (*) ajouté à la fin. Pour plus d’informations, consultez <a href="-search-sql-wildcards.md">utilisation de caractères génériques dans le PRÉDICAT Contains</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> Si les mots de correspondance spécifiés avec le terme proche se trouvent tous deux dans la colonne recherchée, mais qu’ils sont plus éloignés de 50 mots, le résultat est toujours retourné, mais a un [rang](-search-sql-understandingrelevancevalues.md) égal à 0.

 

### <a name="example"></a>Exemple

L’exemple suivant illustre le chaînage de près des termes, à l’aide des formes courtes et longues du terme :


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Utilisation de caractères génériques dans le prédicat CONTAINs](-search-sql-wildcards.md)
</dt> </dl>

 

 



