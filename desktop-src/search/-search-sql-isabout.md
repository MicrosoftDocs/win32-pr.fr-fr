---
description: Le terme ISABOUT fait correspondre les colonnes à un groupe d’un ou plusieurs termes de recherche.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: Terme ISABOUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5665e7bf62da4858cf2e7d68e65d0f42771903d55e3189db12f19cdd5414530d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969608"
---
# <a name="isabout-term"></a>Terme ISABOUT

**Déconseillé**

Cette fonctionnalité a été supprimée à partir de Windows 8. Si vous écrivez de nouvelles applications, évitez d’utiliser cette fonctionnalité déconseillée. Si vous modifiez des applications existantes, il est vivement recommandé de supprimer toute dépendance sur cette fonctionnalité.

Le terme ISABOUT fait correspondre les colonnes à un groupe d’un ou plusieurs termes de recherche. Sa syntaxe est la suivante :


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



Le terme RANKMETHOD facultatif spécifie la méthode de calcul utilisée pour classer les documents qui correspondent à un ou plusieurs composants. Si aucun RANKMETHOD n’est spécifié, la méthode de classement du coefficient Jaccard par défaut est utilisée.

Le terme ISABOUT peut avoir un ou plusieurs composants. Les colonnes spécifiées dans le prédicat [Contains](-search-sql-contains.md) sont testées par rapport à chaque composant. Le document est inclus dans les résultats si au moins l’un des composants correspond. Les virgules séparent plusieurs composants.

La partie composant a la syntaxe suivante :


```
<match_term> [<weight_term>]
```



Vous pouvez utiliser le terme de pondération facultative pour modifier l’importance relative de chaque terme au sein du terme ISABOUT. Si aucun terme de poids n’est appliqué, le poids par défaut de 1,0 est implicite.

Le tableau suivant décrit les types de termes de correspondance possibles.



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
<td>Mot unique sans espaces ni autres signes de ponctuation.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Phrase</td>
<td>Plusieurs mots ou espaces inclus.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a>Pondération de colonne ISABOUT

Le terme ISABOUT classe les documents correspondants en fonction de la précision de chaque document par rapport à l’ensemble de termes de correspondance dans la requête. Vous pouvez utiliser la pondération de colonne pour mettre plus d’importance sur la correspondance de termes de correspondance que d’autres. Chaque terme de correspondance du terme ISABOUT peut avoir une valeur de poids appliquée. Le poids est appliqué à un terme de correspondance unique et est indiqué par le mot clé « WEIGHT ». Le terme poids a deux syntaxes alternatives :


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



La valeur de poids doit être comprise entre 0 et 1,0, sans plus de trois décimales. Si vous spécifiez une valeur de pondération en dehors de cette plage, un message d’erreur est générée. La valeur de classement non pondérée pour un terme est multipliée par la valeur de poids du terme.

Si aucun poids n’est spécifié pour un terme de correspondance, la valeur par défaut, 1,0, est implicite.

### <a name="example"></a>Exemple

L’exemple suivant applique des pondérations aux deux termes de correspondance ISABOUT, à l’aide de la syntaxe longue et abrégée des valeurs de poids.


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Prédicat FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> </dl>

 

 



