---
description: Le terme ISABOUT fait correspondre les colonnes à un groupe d’un ou plusieurs termes de recherche.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: Terme ISABOUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750381"
---
# <a name="isabout-term"></a><span data-ttu-id="10dfa-103">Terme ISABOUT</span><span class="sxs-lookup"><span data-stu-id="10dfa-103">ISABOUT Term</span></span>

<span data-ttu-id="10dfa-104">**Déconseillé**</span><span class="sxs-lookup"><span data-stu-id="10dfa-104">**Deprecated**</span></span>

<span data-ttu-id="10dfa-105">Cette fonctionnalité a été supprimée depuis Windows 8.</span><span class="sxs-lookup"><span data-stu-id="10dfa-105">This feature has been removed as of Windows 8.</span></span> <span data-ttu-id="10dfa-106">Si vous écrivez de nouvelles applications, évitez d’utiliser cette fonctionnalité déconseillée.</span><span class="sxs-lookup"><span data-stu-id="10dfa-106">If you write new applications, avoid using this deprecated feature.</span></span> <span data-ttu-id="10dfa-107">Si vous modifiez des applications existantes, il est vivement recommandé de supprimer toute dépendance sur cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="10dfa-107">If you modify existing applications, you are strongly encouraged to remove any dependency on this feature.</span></span>

<span data-ttu-id="10dfa-108">Le terme ISABOUT fait correspondre les colonnes à un groupe d’un ou plusieurs termes de recherche.</span><span class="sxs-lookup"><span data-stu-id="10dfa-108">The ISABOUT term matches columns against a group of one or more search terms.</span></span> <span data-ttu-id="10dfa-109">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="10dfa-109">It has the following syntax:</span></span>


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



<span data-ttu-id="10dfa-110">Le terme RANKMETHOD facultatif spécifie la méthode de calcul utilisée pour classer les documents qui correspondent à un ou plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="10dfa-110">The optional RANKMETHOD term specifies the calculation method used to rank the documents that match one or more of the components.</span></span> <span data-ttu-id="10dfa-111">Si aucun RANKMETHOD n’est spécifié, la méthode de classement du coefficient Jaccard par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="10dfa-111">If no RANKMETHOD is specified, the default Jaccard Coefficient ranking method is used.</span></span>

<span data-ttu-id="10dfa-112">Le terme ISABOUT peut avoir un ou plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="10dfa-112">The ISABOUT term can have one or more components.</span></span> <span data-ttu-id="10dfa-113">Les colonnes spécifiées dans le prédicat [Contains](-search-sql-contains.md) sont testées par rapport à chaque composant.</span><span class="sxs-lookup"><span data-stu-id="10dfa-113">The columns specified in the [CONTAINS](-search-sql-contains.md) predicate are tested against each component.</span></span> <span data-ttu-id="10dfa-114">Le document est inclus dans les résultats si au moins l’un des composants correspond.</span><span class="sxs-lookup"><span data-stu-id="10dfa-114">The document is included in the results if at least one of the components matches.</span></span> <span data-ttu-id="10dfa-115">Les virgules séparent plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="10dfa-115">Commas separate multiple components.</span></span>

<span data-ttu-id="10dfa-116">La partie composant a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="10dfa-116">The component part has the following syntax:</span></span>


```
<match_term> [<weight_term>]
```



<span data-ttu-id="10dfa-117">Vous pouvez utiliser le terme de pondération facultative pour modifier l’importance relative de chaque terme au sein du terme ISABOUT.</span><span class="sxs-lookup"><span data-stu-id="10dfa-117">You can use the optional WEIGHT term to change the relative importance of each term within the ISABOUT term.</span></span> <span data-ttu-id="10dfa-118">Si aucun terme de poids n’est appliqué, le poids par défaut de 1,0 est implicite.</span><span class="sxs-lookup"><span data-stu-id="10dfa-118">If no weight term is applied, the default 1.0 weight is implied.</span></span>

<span data-ttu-id="10dfa-119">Le tableau suivant décrit les types de termes de correspondance possibles.</span><span class="sxs-lookup"><span data-stu-id="10dfa-119">The following table describes possible match term types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10dfa-120">Type</span><span class="sxs-lookup"><span data-stu-id="10dfa-120">Type</span></span></th>
<th><span data-ttu-id="10dfa-121">Description</span><span class="sxs-lookup"><span data-stu-id="10dfa-121">Description</span></span></th>
<th><span data-ttu-id="10dfa-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="10dfa-122">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10dfa-123">Word</span><span class="sxs-lookup"><span data-stu-id="10dfa-123">Word</span></span></td>
<td><span data-ttu-id="10dfa-124">Mot unique sans espaces ni autres signes de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="10dfa-124">A single word without spaces or other punctuation.</span></span></td>
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
<td><span data-ttu-id="10dfa-125">Expression</span><span class="sxs-lookup"><span data-stu-id="10dfa-125">Phrase</span></span></td>
<td><span data-ttu-id="10dfa-126">Plusieurs mots ou espaces inclus.</span><span class="sxs-lookup"><span data-stu-id="10dfa-126">Multiple words or included spaces.</span></span></td>
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
<td><span data-ttu-id="10dfa-127">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="10dfa-127">Wildcard</span></span></td>
<td><span data-ttu-id="10dfa-128">Mots ou expressions avec l’astérisque (\*) ajouté à la fin.</span><span class="sxs-lookup"><span data-stu-id="10dfa-128">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="10dfa-129">Pour plus d’informations, consultez <a href="-search-sql-wildcards.md">utilisation de caractères génériques dans le PRÉDICAT Contains</a>.</span><span class="sxs-lookup"><span data-stu-id="10dfa-129">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
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



 

## <a name="isabout-column-weighting"></a><span data-ttu-id="10dfa-130">Pondération de colonne ISABOUT</span><span class="sxs-lookup"><span data-stu-id="10dfa-130">ISABOUT Column Weighting</span></span>

<span data-ttu-id="10dfa-131">Le terme ISABOUT classe les documents correspondants en fonction de la précision de chaque document par rapport à l’ensemble de termes de correspondance dans la requête.</span><span class="sxs-lookup"><span data-stu-id="10dfa-131">The ISABOUT term ranks matching documents based on how closely each document matches the set of match terms in the query.</span></span> <span data-ttu-id="10dfa-132">Vous pouvez utiliser la pondération de colonne pour mettre plus d’importance sur la correspondance de termes de correspondance que d’autres.</span><span class="sxs-lookup"><span data-stu-id="10dfa-132">You can use column weighting to place more importance on matching some match terms than others.</span></span> <span data-ttu-id="10dfa-133">Chaque terme de correspondance du terme ISABOUT peut avoir une valeur de poids appliquée.</span><span class="sxs-lookup"><span data-stu-id="10dfa-133">Each match term in the ISABOUT term can have a weight value applied.</span></span> <span data-ttu-id="10dfa-134">Le poids est appliqué à un terme de correspondance unique et est indiqué par le mot clé « WEIGHT ».</span><span class="sxs-lookup"><span data-stu-id="10dfa-134">The weight is applied to a single match term and is indicated by the keyword "WEIGHT".</span></span> <span data-ttu-id="10dfa-135">Le terme poids a deux syntaxes alternatives :</span><span class="sxs-lookup"><span data-stu-id="10dfa-135">The WEIGHT term has two alternative syntaxes:</span></span>


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



<span data-ttu-id="10dfa-136">La valeur de poids doit être comprise entre 0 et 1,0, sans plus de trois décimales.</span><span class="sxs-lookup"><span data-stu-id="10dfa-136">The weight value must be between 0 and 1.0, with no more than three decimal places.</span></span> <span data-ttu-id="10dfa-137">Si vous spécifiez une valeur de pondération en dehors de cette plage, un message d’erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="10dfa-137">Specifying a weight value outside this range results in an error message.</span></span> <span data-ttu-id="10dfa-138">La valeur de classement non pondérée pour un terme est multipliée par la valeur de poids du terme.</span><span class="sxs-lookup"><span data-stu-id="10dfa-138">The unweighted ranking value for a term is multiplied by the weight value for the term.</span></span>

<span data-ttu-id="10dfa-139">Si aucun poids n’est spécifié pour un terme de correspondance, la valeur par défaut, 1,0, est implicite.</span><span class="sxs-lookup"><span data-stu-id="10dfa-139">If no weight is specified for a match term, the default value, 1.0, is implied.</span></span>

### <a name="example"></a><span data-ttu-id="10dfa-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="10dfa-140">Example</span></span>

<span data-ttu-id="10dfa-141">L’exemple suivant applique des pondérations aux deux termes de correspondance ISABOUT, à l’aide de la syntaxe longue et abrégée des valeurs de poids.</span><span class="sxs-lookup"><span data-stu-id="10dfa-141">The following example applies weights to the two ISABOUT match terms, using both the long and short syntax for weight values.</span></span>


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a><span data-ttu-id="10dfa-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10dfa-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="10dfa-143">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="10dfa-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10dfa-144">Prédicat FREETEXT</span><span class="sxs-lookup"><span data-stu-id="10dfa-144">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="10dfa-145">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="10dfa-145">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



