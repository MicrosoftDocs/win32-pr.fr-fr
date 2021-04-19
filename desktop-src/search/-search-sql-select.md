---
description: 'L’exemple suivant illustre la syntaxe de base de l’instruction SELECT pour une requête locale :'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instruction SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544622"
---
# <a name="select-statement"></a><span data-ttu-id="ee2f3-103">Instruction SELECT</span><span class="sxs-lookup"><span data-stu-id="ee2f3-103">SELECT Statement</span></span>

<span data-ttu-id="ee2f3-104">L’exemple suivant illustre la syntaxe de base de l’instruction SELECT pour une requête locale :</span><span class="sxs-lookup"><span data-stu-id="ee2f3-104">The following shows the basic syntax of the SELECT statement for a local query:</span></span>


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



<span data-ttu-id="ee2f3-105">L’exemple suivant illustre la partie colonne de la syntaxe de l’instruction SELECT :</span><span class="sxs-lookup"><span data-stu-id="ee2f3-105">The following shows the column portion of the SELECT statement syntax:</span></span>


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



<span data-ttu-id="ee2f3-106">Le ou les spécificateurs de colonne doivent être des colonnes de noms de propriété valides, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-106">The column specifier(s) must be valid property name columns, separated by commas.</span></span> <span data-ttu-id="ee2f3-107">Les noms de colonnes valides sont des descriptions de propriété inscrites ou sont définis par le schéma de système de propriétés de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-107">Valid column names are registered property descriptions or are defined by the Shell's Property System Schema.</span></span> <span data-ttu-id="ee2f3-108">Vous pouvez sélectionner uniquement les colonnes qui sont marquées comme récupérables dans le schéma du système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-108">You can select only those columns that are marked as retrievable in the Property System Schema.</span></span> <span data-ttu-id="ee2f3-109">Si vous utilisez la casse mixte pour identifier les propriétés qui ne sont pas des propriétés définies par le système, vous devez placer le spécificateur de colonne entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-109">If you use mixed case to identify properties that are not system-defined properties, you must enclose the column specifier in double quotation marks.</span></span> <span data-ttu-id="ee2f3-110">Les noms de propriété définis par le système incluent toutes les propriétés commençant par « System » (par exemple, System. contact. FirstName) et ne requièrent pas de guillemets.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-110">System-defined property names include all properties beginning with "System" (for example, System.Contact.FirstName) and do not require quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="ee2f3-111">Vous pouvez également placer les noms des propriétés définies par le système entre guillemets doubles pour une meilleure lisibilité.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-111">You can also enclose system-defined property names in double quotation marks for readability.</span></span> <span data-ttu-id="ee2f3-112">Cela n’affecte pas la compatibilité.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-112">This does not affect compatibility.</span></span>

 

<span data-ttu-id="ee2f3-113">Lorsque la requête retourne un document qui n’a pas la colonne demandée, la valeur de cette colonne pour le document est **null**.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-113">When the query returns a document that does not have the requested column, the value of that column for the document is **NULL**.</span></span>

<span data-ttu-id="ee2f3-114">Vous devez fournir au moins un nom de colonne dans une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-114">You must provide at least one column name in a SELECT statement.</span></span> <span data-ttu-id="ee2f3-115">Dans la requête langage SQL (SQL), vous êtes autorisé à utiliser l’astérisque ( \* ) pour spécifier que toutes les colonnes d’une table doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-115">In the Structured Query Language (SQL) query, you are allowed to use the asterisk (\*) to specify that all columns in a table are to be returned.</span></span> <span data-ttu-id="ee2f3-116">Toutefois, aucun ensemble de propriétés défini et fixe ne s’applique à tous les documents.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-116">However, no defined and fixed set of properties applies to all documents.</span></span> <span data-ttu-id="ee2f3-117">C’est la raison pour laquelle l’astérisque SQL n’est pas autorisé dans le <columns> spécificateur de l’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-117">For this reason, the SQL asterisk is not permitted in the <columns> specifier of the SELECT statement.</span></span>

## <a name="getting-the-top-n-results"></a><span data-ttu-id="ee2f3-118">Obtention des n premiers résultats</span><span class="sxs-lookup"><span data-stu-id="ee2f3-118">Getting the Top n Results</span></span>

<span data-ttu-id="ee2f3-119">Vous pouvez spécifier le nombre maximal de résultats à renvoyer à l’aide de la syntaxe TOP :</span><span class="sxs-lookup"><span data-stu-id="ee2f3-119">You can specify a maximum number of results to return by using the TOP syntax:</span></span>


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a><span data-ttu-id="ee2f3-120">Conversion de types de données de colonne</span><span class="sxs-lookup"><span data-stu-id="ee2f3-120">Casting Column Data Types</span></span>

<span data-ttu-id="ee2f3-121">Parfois, vous devrez peut-être convertir des données de type chaîne extraites de documents en un autre type de données afin qu’une comparaison appropriée puisse être effectuée.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-121">At times, you might need to cast string data extracted from documents as another data type so that an appropriate comparison can be made.</span></span> <span data-ttu-id="ee2f3-122">Pour plus d’informations, consultez [cast du type de données d’une colonne](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="ee2f3-122">For more information, refer to [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ee2f3-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="ee2f3-123">Examples</span></span>

<span data-ttu-id="ee2f3-124">Les exemples suivants retournent le nom et l’URL des documents correspondants.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-124">The following examples return the name and URL of matching documents.</span></span>


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a><span data-ttu-id="ee2f3-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee2f3-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ee2f3-126">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ee2f3-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee2f3-127">Conversion du type de données d’une colonne</span><span class="sxs-lookup"><span data-stu-id="ee2f3-127">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)
</dt> <dt>

<span data-ttu-id="ee2f3-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="ee2f3-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ee2f3-129">[Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="ee2f3-129">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 



