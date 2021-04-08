---
description: Les alias de groupes de colonnes permettent d’utiliser des noms plus courts à la place du nom d’une colonne ou d’un groupe de colonnes. Le prédicat facultatif alias de groupe fait partie de la clause WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: Prédicat WITH--AS Group alias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750365"
---
# <a name="with----as-group-alias-predicate"></a><span data-ttu-id="101e2-104">Prédicat WITH--AS Group alias</span><span class="sxs-lookup"><span data-stu-id="101e2-104">WITH -- AS Group Alias Predicate</span></span>

<span data-ttu-id="101e2-105">Les alias de groupes de colonnes permettent d’utiliser des noms plus courts à la place du nom d’une colonne ou d’un groupe de colonnes.</span><span class="sxs-lookup"><span data-stu-id="101e2-105">Column group aliases provide a way to use shorter names in place of the name of a column or a group of columns.</span></span> <span data-ttu-id="101e2-106">Le prédicat facultatif alias de groupe fait partie de la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="101e2-106">The optional group alias predicate is part of the WHERE clause.</span></span> <span data-ttu-id="101e2-107">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="101e2-107">Its syntax follows:</span></span>


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



<span data-ttu-id="101e2-108">Vous pouvez spécifier plusieurs alias de groupe, en séparant les avec... En tant que prédicats par des virgules.</span><span class="sxs-lookup"><span data-stu-id="101e2-108">You can specify more than one group alias, separating the WITH...AS predicates by commas.</span></span>

<span data-ttu-id="101e2-109">Quand un alias de groupe est référencé dans un prédicat de clause WHERE, la condition est appliquée à chaque colonne du groupe.</span><span class="sxs-lookup"><span data-stu-id="101e2-109">When a group alias is referred to in a WHERE clause predicate, the condition is applied to each column in the group.</span></span> <span data-ttu-id="101e2-110">Les valeurs logiques résultant de la correspondance de chaque colonne sont combinées à l’aide de l’opérateur logique **or** .</span><span class="sxs-lookup"><span data-stu-id="101e2-110">The logical values resulting from matching each column are combined by using the logical **OR** operator.</span></span>

<span data-ttu-id="101e2-111">Un alias doit être défini avant de pouvoir être utilisé, et il peut être utilisé uniquement dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="101e2-111">An alias must be defined before it can be used, and it can be used only within the WHERE clause.</span></span> <span data-ttu-id="101e2-112">Le nom d’alias doit être un identificateur régulier précédé d’un signe dièse () requis \# .</span><span class="sxs-lookup"><span data-stu-id="101e2-112">The alias name must be a regular identifier preceded by a required pound sign (\#).</span></span>

<span data-ttu-id="101e2-113">Le spécificateur de colonne peut contenir un ou plusieurs spécificateurs de colonne, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="101e2-113">The column specifier can contain one or more column specifiers, separated by commas.</span></span> <span data-ttu-id="101e2-114">La liste de colonnes doit être placée entre parenthèses et la pondération peut être assignée à chacune.</span><span class="sxs-lookup"><span data-stu-id="101e2-114">The list of columns must be enclosed in parentheses and weighting can be assigned to each.</span></span> <span data-ttu-id="101e2-115">Chaque colonne a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="101e2-115">Each column has the following syntax:</span></span>


```
<column_identifier> [<weight_assignment>]
```



<span data-ttu-id="101e2-116">Pour plus d’informations sur la spécification des pondérations de colonnes, consultez [prédicat FREETEXT](-search-sql-freetext.md) et [Contains Predicate](-search-sql-contains.md).</span><span class="sxs-lookup"><span data-stu-id="101e2-116">For information on specifying column weights, see [FREETEXT Predicate](-search-sql-freetext.md) and [CONTAINS Predicate](-search-sql-contains.md).</span></span>

<span data-ttu-id="101e2-117">L’identificateur de colonne peut être normal ou délimité.</span><span class="sxs-lookup"><span data-stu-id="101e2-117">The column identifier can be regular or delimited.</span></span>

## <a name="examples"></a><span data-ttu-id="101e2-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="101e2-118">Examples</span></span>

<span data-ttu-id="101e2-119">Les exemples de clause WHERE suivants montrent quand et comment vous pouvez utiliser le prédicat d’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="101e2-119">The following WHERE clause examples demonstrate when and how you can use the group alias predicate.</span></span> <span data-ttu-id="101e2-120">Le premier exemple montre une clause WHERE plus répétitive qui n’utilise pas l’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="101e2-120">The first example shows a more repetitive WHERE clause that does not use group aliasing.</span></span>


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



<span data-ttu-id="101e2-121">L’exemple précédent peut être simplifié à l’aide d’un alias de groupe, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="101e2-121">The preceding example can be simplified by using a group alias, as shown in the following example.</span></span>


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="101e2-122">Voici un exemple de pondération positive dans laquelle la propriété **title** reçoit davantage de poids en déterminant le rang relatif.</span><span class="sxs-lookup"><span data-stu-id="101e2-122">The following is an example of positive weighting where the **Title** property is given more weight in determining the relative rank.</span></span>


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="101e2-123">Voici un exemple de pondération négative dans laquelle la propriété de **titre** avec un poids de 0 n’est pas prise en compte.</span><span class="sxs-lookup"><span data-stu-id="101e2-123">The following is an example of negative weighting where the **Title** property with weight of 0 is not considered.</span></span>


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a><span data-ttu-id="101e2-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="101e2-124">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="101e2-125">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="101e2-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="101e2-126">Prédicat FREETEXT</span><span class="sxs-lookup"><span data-stu-id="101e2-126">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

<span data-ttu-id="101e2-127">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="101e2-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="101e2-128">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="101e2-128">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="101e2-129">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="101e2-129">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



