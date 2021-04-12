---
description: Le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble des American National Standards Institute langage SQL (ANSI SQL) &\# 8212 ; avec des modifications sémantiques mineures. Le tableau suivant répertorie les mots clés WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL for WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202276"
---
# <a name="wql-sql-for-wmi"></a><span data-ttu-id="8b27a-104">WQL (SQL for WMI)</span><span class="sxs-lookup"><span data-stu-id="8b27a-104">WQL (SQL for WMI)</span></span>

<span data-ttu-id="8b27a-105">Le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble des American National Standards Institute langage SQL (ANSI SQL) avec des modifications sémantiques mineures.</span><span class="sxs-lookup"><span data-stu-id="8b27a-105">The WMI Query Language (WQL) is a subset of the American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes.</span></span> <span data-ttu-id="8b27a-106">Le tableau suivant répertorie les mots clés WQL.</span><span class="sxs-lookup"><span data-stu-id="8b27a-106">The following table lists the WQL keywords.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b27a-107">Mot clé WQL</span><span class="sxs-lookup"><span data-stu-id="8b27a-107">WQL keyword</span></span></th>
<th><span data-ttu-id="8b27a-108">Signification</span><span class="sxs-lookup"><span data-stu-id="8b27a-108">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b27a-109">AND</span><span class="sxs-lookup"><span data-stu-id="8b27a-109">AND</span></span><br/></td>
<td><span data-ttu-id="8b27a-110">Combine deux expressions booléennes et retourne la <strong>valeur true</strong> lorsque les deux expressions ont la <strong>valeur true</strong>.</span><span class="sxs-lookup"><span data-stu-id="8b27a-110">Combines two Boolean expressions, and returns <strong>TRUE</strong> when both expressions are <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-111"><a href="associators-of-statement.md">ASSOCIATEURS DE</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span></span></td>
<td><span data-ttu-id="8b27a-112">Récupère toutes les instances associées à une instance source.</span><span class="sxs-lookup"><span data-stu-id="8b27a-112">Retrieves all instances that are associated with a source instance.</span></span><br/> <span data-ttu-id="8b27a-113">Utilisez cette instruction avec les requêtes de schéma et les requêtes de données.</span><span class="sxs-lookup"><span data-stu-id="8b27a-113">Use this statement with schema queries and data queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-114"><a href="--class-identifier.md">__CLASS</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-114"><a href="--class-identifier.md">__CLASS</a></span></span></td>
<td><span data-ttu-id="8b27a-115">Fait référence à la classe de l’objet dans une requête.</span><span class="sxs-lookup"><span data-stu-id="8b27a-115">References the class of the object in a query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-116">FROM</span><span class="sxs-lookup"><span data-stu-id="8b27a-116">FROM</span></span><br/></td>
<td><span data-ttu-id="8b27a-117">Spécifie la classe qui contient les propriétés listées dans une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="8b27a-117">Specifies the class that contains the properties listed in a SELECT statement.</span></span> <span data-ttu-id="8b27a-118">Windows Management Instrumentation (WMI) prend en charge les requêtes de données d’une seule classe à la fois.</span><span class="sxs-lookup"><span data-stu-id="8b27a-118">Windows Management Instrumentation (WMI) supports data queries from only one class at a time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-119"><a href="group-clause.md">GROUP, clause</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-119"><a href="group-clause.md">GROUP Clause</a></span></span></td>
<td><span data-ttu-id="8b27a-120">Permet à WMI de générer une notification pour représenter un groupe d’événements.</span><span class="sxs-lookup"><span data-stu-id="8b27a-120">Causes WMI to generate one notification to represent a group of events.</span></span><br/> <span data-ttu-id="8b27a-121">Utilisez cette clause avec des requêtes d’événements.</span><span class="sxs-lookup"><span data-stu-id="8b27a-121">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-122"><a href="having-clause.md">HAVING</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-122"><a href="having-clause.md">HAVING</a></span></span></td>
<td><span data-ttu-id="8b27a-123">Filtre les événements reçus pendant l’intervalle de regroupement spécifié dans la <a href="within-clause.md">clause within</a>.</span><span class="sxs-lookup"><span data-stu-id="8b27a-123">Filters the events that are received during the grouping interval that is specified in the <a href="within-clause.md">WITHIN clause</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-124"><a href="wql-operators.md">IS</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-124"><a href="wql-operators.md">IS</a></span></span></td>
<td><span data-ttu-id="8b27a-125">Opérateur de comparaison utilisé avec NOT et <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="8b27a-125">Comparison operator used with NOT and <strong>NULL</strong>.</span></span> <span data-ttu-id="8b27a-126">La syntaxe de cette instruction est la suivante :</span><span class="sxs-lookup"><span data-stu-id="8b27a-126">The syntax for this statement is the following:</span></span><br/> <span data-ttu-id="8b27a-127">IS [NOT] <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="8b27a-127">IS [NOT] <strong>NULL</strong></span></span><br/> <span data-ttu-id="8b27a-128">(où NOT est facultatif)</span><span class="sxs-lookup"><span data-stu-id="8b27a-128">(where NOT is optional)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-129"><a href="wql-operators.md">ISA</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-129"><a href="wql-operators.md">ISA</a></span></span></td>
<td><span data-ttu-id="8b27a-130">Opérateur qui applique une requête aux sous-classes d’une classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8b27a-130">Operator that applies a query to the subclasses of a specified class.</span></span> <span data-ttu-id="8b27a-131">Pour plus d’informations, consultez <a href="isa-operator-for-event-queries.md">opérateur ISA pour les requêtes d’événements</a>, <a href="isa-operator-for-data-queries.md">opérateur ISA pour les requêtes de données</a>et <a href="isa-operator-for-schema-queries.md">opérateur ISA pour les requêtes de schéma</a>.</span><span class="sxs-lookup"><span data-stu-id="8b27a-131">For more information, see <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>, and <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-132">KEYSONLY</span><span class="sxs-lookup"><span data-stu-id="8b27a-132">KEYSONLY</span></span><br/></td>
<td><span data-ttu-id="8b27a-133">Utilisé dans les <a href="references-of-statement.md">références</a> et les <a href="associators-of-statement.md">associateurs de</a> requêtes pour s’assurer que les instances résultantes sont remplies uniquement avec les clés des instances, ce qui réduit la surcharge de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8b27a-133">Used in <a href="references-of-statement.md">REFERENCES OF</a> and <a href="associators-of-statement.md">ASSOCIATORS OF</a> queries to ensure that the resulting instances are only populated with the keys of the instances, which reduces the overhead of the call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-134"><a href="wql-operators.md">LIKE</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-134"><a href="wql-operators.md">LIKE</a></span></span></td>
<td><span data-ttu-id="8b27a-135">Opérateur qui détermine si une chaîne de caractères donnée correspond à un modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="8b27a-135">Operator that determines whether or not a given character string matches a specified pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-136">NOT</span><span class="sxs-lookup"><span data-stu-id="8b27a-136">NOT</span></span><br/></td>
<td><span data-ttu-id="8b27a-137">Opérateur de comparaison qui utilise dans une requête WQL SELECT, par exemple :</span><span class="sxs-lookup"><span data-stu-id="8b27a-137">Comparison operator that use in a WQL SELECT query, for example:</span></span><br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-138"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="8b27a-138"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="8b27a-139">Indique qu’un objet n’a pas de valeur assignée explicitement.</span><span class="sxs-lookup"><span data-stu-id="8b27a-139">Indicates an object does not have an explicitly assigned value.</span></span> <span data-ttu-id="8b27a-140"><strong>Null</strong> n’est pas équivalent à zéro (0) ou vide.</span><span class="sxs-lookup"><span data-stu-id="8b27a-140"><strong>NULL</strong> is not equivalent to zero (0) or blank.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-141">OR</span><span class="sxs-lookup"><span data-stu-id="8b27a-141">OR</span></span><br/></td>
<td><span data-ttu-id="8b27a-142">Combine deux conditions.</span><span class="sxs-lookup"><span data-stu-id="8b27a-142">Combines two conditions.</span></span><br/> <span data-ttu-id="8b27a-143">Lorsque plusieurs opérateurs logiques sont utilisés dans une instruction, les opérateurs ou sont évalués après les opérateurs et.</span><span class="sxs-lookup"><span data-stu-id="8b27a-143">When more than one logical operator is used in a statement, the OR operators are evaluated after the AND operators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-144"><a href="references-of-statement.md">RÉFÉRENCES DE</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-144"><a href="references-of-statement.md">REFERENCES OF</a></span></span></td>
<td><span data-ttu-id="8b27a-145">Récupère toutes les instances d’association qui font référence à une instance source spécifique.</span><span class="sxs-lookup"><span data-stu-id="8b27a-145">Retrieves all association instances that refer to a specific source instance.</span></span> <span data-ttu-id="8b27a-146">Utilisez cette instruction avec les requêtes de schéma et de données.</span><span class="sxs-lookup"><span data-stu-id="8b27a-146">Use this statement with schema and data queries.</span></span> <span data-ttu-id="8b27a-147">Les <a href="references-of-statement.md">références de</a> l’instruction sont similaires aux <a href="associators-of-statement.md">ASSOCIATORS de</a> l’instruction.</span><span class="sxs-lookup"><span data-stu-id="8b27a-147">The <a href="references-of-statement.md">REFERENCES OF</a> statement is similar to the <a href="associators-of-statement.md">ASSOCIATORS OF</a> statement.</span></span> <span data-ttu-id="8b27a-148">Toutefois, il ne récupère pas les instances de point de terminaison ; Il récupère les instances d’association.</span><span class="sxs-lookup"><span data-stu-id="8b27a-148">However, it does not retrieve endpoint instances; it retrieves the association instances.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-149">SELECT</span><span class="sxs-lookup"><span data-stu-id="8b27a-149">SELECT</span></span><br/></td>
<td><span data-ttu-id="8b27a-150">Spécifie les propriétés utilisées dans une requête.</span><span class="sxs-lookup"><span data-stu-id="8b27a-150">Specifies the properties that are used in a query.</span></span><br/> <span data-ttu-id="8b27a-151">Pour plus d’informations, consultez <a href="select-statement-for-data-queries.md">instruction SELECT pour les requêtes de données</a>, <a href="select-statement-for-event-queries.md">instruction SELECT pour les requêtes d’événement</a>ou <a href="select-statement-for-schema-queries.md">instruction SELECT pour les requêtes de schéma</a>.</span><span class="sxs-lookup"><span data-stu-id="8b27a-151">For more information, see <a href="select-statement-for-data-queries.md">SELECT Statement for Data Queries</a>, <a href="select-statement-for-event-queries.md">SELECT Statement for Event Queries</a>, or <a href="select-statement-for-schema-queries.md">SELECT Statement for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-152"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="8b27a-152"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="8b27a-153">Opérateur booléen qui prend la valeur-1 (moins un).</span><span class="sxs-lookup"><span data-stu-id="8b27a-153">Boolean operator that evaluates to -1 (minus one).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-154"><a href="where-clause.md">WHERE</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-154"><a href="where-clause.md">WHERE</a></span></span></td>
<td><span data-ttu-id="8b27a-155">Réduit l’étendue d’une requête de données, d’événement ou de schéma.</span><span class="sxs-lookup"><span data-stu-id="8b27a-155">Narrows the scope of a data, event, or schema query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b27a-156"><a href="within-clause.md">WITHIN</a></span><span class="sxs-lookup"><span data-stu-id="8b27a-156"><a href="within-clause.md">WITHIN</a></span></span></td>
<td><span data-ttu-id="8b27a-157">Spécifie un intervalle d’interrogation ou de regroupement.</span><span class="sxs-lookup"><span data-stu-id="8b27a-157">Specifies a polling or grouping interval.</span></span><br/> <span data-ttu-id="8b27a-158">Utilisez cette clause avec des requêtes d’événements.</span><span class="sxs-lookup"><span data-stu-id="8b27a-158">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b27a-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="8b27a-159">FALSE</span></span><br/></td>
<td><span data-ttu-id="8b27a-160">Opérateur booléen qui prend la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="8b27a-160">Boolean operator that evaluates to 0 (zero).</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="8b27a-161">L’utilisation d’un mot clé WQL comme nom d’objet peut entraîner une requête qui ne peut pas être analysée même lorsque la requête est compilée sans erreur.</span><span class="sxs-lookup"><span data-stu-id="8b27a-161">Using a WQL key word as an object name can result in a query that cannot be parsed even when the query compiles without error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8b27a-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b27a-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b27a-163">Opérateurs WQL</span><span class="sxs-lookup"><span data-stu-id="8b27a-163">WQL Operators</span></span>](wql-operators.md)
</dt> <dt>

[<span data-ttu-id="8b27a-164">Formats de date pris en charge par WQL</span><span class="sxs-lookup"><span data-stu-id="8b27a-164">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
</dt> <dt>

[<span data-ttu-id="8b27a-165">Formats d’heure pris en charge par WQL</span><span class="sxs-lookup"><span data-stu-id="8b27a-165">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)
</dt> </dl>

 

 




