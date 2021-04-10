---
description: Microsoft Windows Search utilise des gestionnaires de propriétés pour extraire les valeurs des propriétés des éléments et utilise le schéma de système de propriétés pour déterminer comment une propriété spécifique doit être indexée.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Développement de gestionnaires de propriétés pour Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201303"
---
# <a name="developing-property-handlers-for-windows-search"></a><span data-ttu-id="0a576-103">Développement de gestionnaires de propriétés pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="0a576-103">Developing Property Handlers for Windows Search</span></span>

<span data-ttu-id="0a576-104">Microsoft Windows Search utilise des gestionnaires de propriétés pour extraire les valeurs des propriétés des éléments et utilise le schéma de système de propriétés pour déterminer comment une propriété spécifique doit être indexée.</span><span class="sxs-lookup"><span data-stu-id="0a576-104">Microsoft Windows Search uses property handlers to extract the values of properties from items and uses the property system schema to determine how a specific property should be indexed.</span></span> <span data-ttu-id="0a576-105">Pour lire et indexer des valeurs de propriété, les gestionnaires de propriétés sont appelés out-of-process par Windows Search pour améliorer la sécurité et la robustesse.</span><span class="sxs-lookup"><span data-stu-id="0a576-105">To read and index property values, property handlers are invoked out-of-process by Windows Search to improve security and robustness.</span></span> <span data-ttu-id="0a576-106">En revanche, les gestionnaires de propriétés sont appelés dans le processus par l’Explorateur Windows pour lire et écrire des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="0a576-106">In contrast, property handlers are invoked in-process by Windows Explorer to read and write property values.</span></span>

<span data-ttu-id="0a576-107">Cette rubrique complète la rubrique du [système de propriétés](../properties/building-property-handlers.md) avec des informations spécifiques à Windows Search et contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a576-107">This topic supplements the [Property System](../properties/building-property-handlers.md) topic with information specific to Windows Search and contains the following sections:</span></span>

-   [<span data-ttu-id="0a576-108">Décisions de conception pour les gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-108">Design Decisions for Property Handlers</span></span>](#design-decisions-for-property-handlers)
    -   [<span data-ttu-id="0a576-109">Décisions de propriété</span><span class="sxs-lookup"><span data-stu-id="0a576-109">Property Decisions</span></span>](#property-decisions)
    -   [<span data-ttu-id="0a576-110">Prise en charge du texte intégral</span><span class="sxs-lookup"><span data-stu-id="0a576-110">Full-Text Support</span></span>](#full-text-support)
    -   [<span data-ttu-id="0a576-111">Considérations sur le Implementatation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="0a576-111">Operating System Implementatation Considerations</span></span>](#operating-system-implementatation-considerations)
-   [<span data-ttu-id="0a576-112">Écriture de fichiers de description de propriété</span><span class="sxs-lookup"><span data-stu-id="0a576-112">Writing Property Description Files</span></span>](#writing-property-description-files)
-   [<span data-ttu-id="0a576-113">Implémentation de gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-113">Implementing Property Handlers</span></span>](#implementing-property-handlers)
    -   [<span data-ttu-id="0a576-114">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="0a576-114">IInitializeWithStream</span></span>](#iinitializewithstream)
    -   [<span data-ttu-id="0a576-115">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="0a576-115">IPropertyStore</span></span>](#ipropertystore)
    -   [<span data-ttu-id="0a576-116">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="0a576-116">IPropertyStoreCapabilities</span></span>](#ipropertystorecapabilities)
-   [<span data-ttu-id="0a576-117">Vérifier que vos éléments sont indexés</span><span class="sxs-lookup"><span data-stu-id="0a576-117">Ensuring Your Items Get Indexed</span></span>](#ensuring-your-items-get-indexed)
-   [<span data-ttu-id="0a576-118">Installation et inscription de gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-118">Installing and Registering Property Handlers</span></span>](#installing-and-registering-property-handlers)
-   [<span data-ttu-id="0a576-119">Test et dépannage des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-119">Testing and Troubleshooting Property Handlers</span></span>](#testing-and-troubleshooting-property-handlers)
    -   [<span data-ttu-id="0a576-120">Tests d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="0a576-120">Installation and Setup Tests</span></span>](#installation-and-setup-tests)
    -   [<span data-ttu-id="0a576-121">Dépannage des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-121">Troubleshooting Property Handlers</span></span>](#troubleshooting-property-handlers)
-   [<span data-ttu-id="0a576-122">Utilisation de gestionnaires de propriétés System-Supplied</span><span class="sxs-lookup"><span data-stu-id="0a576-122">Using System-Supplied Property Handlers</span></span>](#using-system-supplied-property-handlers)
-   [<span data-ttu-id="0a576-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a576-123">Related topics</span></span>](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a><span data-ttu-id="0a576-124">Décisions de conception pour les gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-124">Design Decisions for Property Handlers</span></span>

<span data-ttu-id="0a576-125">L’implémentation de gestionnaires de propriétés implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a576-125">Implementing property handlers involves the following steps:</span></span>

1.  <span data-ttu-id="0a576-126">Prendre des décisions de conception concernant les propriétés que vous souhaitez prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="0a576-126">Making design decisions regarding the properties you want to support.</span></span>
2.  <span data-ttu-id="0a576-127">Création d’un fichier de description de propriété (. propDesc) pour les propriétés qui ne sont pas déjà dans le système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-127">Creating a Property Description (.propdesc) file for properties not already in the property system.</span></span>
3.  <span data-ttu-id="0a576-128">Implémentation et test du gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-128">Implementing and testing the property handler.</span></span>
4.  <span data-ttu-id="0a576-129">Installation et enregistrement du gestionnaire de propriétés et des fichiers de description de propriété.</span><span class="sxs-lookup"><span data-stu-id="0a576-129">Installing and registering the property handler and property description files.</span></span>
5.  <span data-ttu-id="0a576-130">Test de l’installation et de l’inscription du gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-130">Testing property handler installation and registration.</span></span>

<span data-ttu-id="0a576-131">Avant de commencer, vous devez prendre en compte les questions de conception suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a576-131">Before you begin, you need to consider the following design questions:</span></span>

-   <span data-ttu-id="0a576-132">Quelles sont les propriétés prises en charge par le format de fichier ?</span><span class="sxs-lookup"><span data-stu-id="0a576-132">What properties does/should the file format support?</span></span>
-   <span data-ttu-id="0a576-133">Ces propriétés sont-elles déjà dans le schéma système ?</span><span class="sxs-lookup"><span data-stu-id="0a576-133">Are these properties already in the System schema?</span></span>
-   <span data-ttu-id="0a576-134">Puis-je utiliser un gestionnaire de propriétés fourni par le système existant ?</span><span class="sxs-lookup"><span data-stu-id="0a576-134">Can I use an existing system-supplied property handler?</span></span>
-   <span data-ttu-id="0a576-135">Quelles propriétés peuvent être affichées aux utilisateurs finaux ?</span><span class="sxs-lookup"><span data-stu-id="0a576-135">Which properties can be displayed to end users?</span></span>
-   <span data-ttu-id="0a576-136">Quelles sont les propriétés modifiables par les utilisateurs ?</span><span class="sxs-lookup"><span data-stu-id="0a576-136">Which properties can users edit?</span></span>
-   <span data-ttu-id="0a576-137">La prise en charge de la recherche en texte intégral provient-elle d’un gestionnaire de propriétés ou d’un filtre ?</span><span class="sxs-lookup"><span data-stu-id="0a576-137">Should support for full-text search come from a property handler or a filter?</span></span>
-   <span data-ttu-id="0a576-138">Dois-je prendre en charge les applications héritées ?</span><span class="sxs-lookup"><span data-stu-id="0a576-138">Do I need to support legacy applications?</span></span> <span data-ttu-id="0a576-139">Si c’est le cas, que dois-je implémenter ?</span><span class="sxs-lookup"><span data-stu-id="0a576-139">If so, what do I implement?</span></span>

> [!Note]  
> <span data-ttu-id="0a576-140">Avant de continuer, consultez [utilisation de System-Supplied gestionnaires de propriétés](#using-system-supplied-property-handlers) pour déterminer si vous pouvez utiliser un gestionnaire de propriétés fourni par le système, ce qui vous permet de gagner du temps et des ressources de développement.</span><span class="sxs-lookup"><span data-stu-id="0a576-140">Before continuing, see [Using System-Supplied Property Handlers](#using-system-supplied-property-handlers) to see if you can use a system-supplied property handler, saving you both time and development resources.</span></span>

 

<span data-ttu-id="0a576-141">Une fois ces décisions prises, vous pouvez écrire des descriptions formelles de vos propriétés personnalisées afin que le moteur de recherche Windows puisse commencer à indexer vos fichiers et propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-141">After you have made these decisions, you can write formal descriptions of your custom properties so that the Windows Search engine can begin indexing your files and properties.</span></span> <span data-ttu-id="0a576-142">Ces descriptions formelles sont des fichiers XML, décrits dans schéma de la [propriété Description](/previous-versions//cc144127(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a576-142">These formal descriptions are XML files, described in [Property Description Schema](/previous-versions//cc144127(v=vs.85)).</span></span>

### <a name="property-decisions"></a><span data-ttu-id="0a576-143">Décisions de propriété</span><span class="sxs-lookup"><span data-stu-id="0a576-143">Property Decisions</span></span>

<span data-ttu-id="0a576-144">Lorsque vous envisagez les propriétés à prendre en charge, vous devez identifier les besoins en matière d’indexation et de recherche des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0a576-144">When considering which properties to support, you should identify your users' indexing and searching needs.</span></span> <span data-ttu-id="0a576-145">Par exemple, vous pouvez identifier les propriétés potentiellement utiles 100 pour votre type de fichier, mais les utilisateurs peuvent être intéressés par la recherche sur une seule poignée.</span><span class="sxs-lookup"><span data-stu-id="0a576-145">For example, you may be able to identify one hundred potentially useful properties for your file type, but users may be interested in searching on only a handful.</span></span> <span data-ttu-id="0a576-146">En outre, vous souhaiterez peut-être afficher un groupe différent, plus grand ou plus petit de ces propriétés pour les utilisateurs dans l’Explorateur Windows, et autoriser les utilisateurs à modifier uniquement un sous-ensemble de ces propriétés affichées.</span><span class="sxs-lookup"><span data-stu-id="0a576-146">Furthermore, you may want to display a different, larger or smaller, group of those properties to users in Windows Explorer, and allow users to edit only a subset of those properties displayed.</span></span>

<span data-ttu-id="0a576-147">Votre type de fichier peut prendre en charge toutes les propriétés personnalisées que vous définissez, ainsi qu’un ensemble de propriétés définies par le système.</span><span class="sxs-lookup"><span data-stu-id="0a576-147">Your file type can support any custom properties you define, as well as a set of system-defined properties.</span></span> <span data-ttu-id="0a576-148">Avant de créer une propriété personnalisée, consultez les [Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) pour voir si la propriété que vous souhaitez prendre en charge est déjà définie par une propriété système.</span><span class="sxs-lookup"><span data-stu-id="0a576-148">Before you create a custom property, please review [System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) to see if the property you want to support is already defined by a system property.</span></span> <span data-ttu-id="0a576-149">Veillez à toujours prendre en charge les propriétés définies par le système les plus importantes.</span><span class="sxs-lookup"><span data-stu-id="0a576-149">Always be sure you support the most important system-defined properties.</span></span>

<span data-ttu-id="0a576-150">Nous vous recommandons d’utiliser une matrice pour vous aider à concevoir vos propriétés :</span><span class="sxs-lookup"><span data-stu-id="0a576-150">We recommend using a matrix to help you design your properties:</span></span>



| <span data-ttu-id="0a576-151">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="0a576-151">Property name</span></span> | <span data-ttu-id="0a576-152">Est indexable ?</span><span class="sxs-lookup"><span data-stu-id="0a576-152">Is indexable?</span></span> | <span data-ttu-id="0a576-153">Est affichable ?</span><span class="sxs-lookup"><span data-stu-id="0a576-153">Is displayable?</span></span> | <span data-ttu-id="0a576-154">Est modifiable ?</span><span class="sxs-lookup"><span data-stu-id="0a576-154">Is editable?</span></span> |
|---------------|---------------|-----------------|--------------|
| <span data-ttu-id="0a576-155">property1</span><span class="sxs-lookup"><span data-stu-id="0a576-155">property1</span></span>     | <span data-ttu-id="0a576-156">O</span><span class="sxs-lookup"><span data-stu-id="0a576-156">Y</span></span>             | <span data-ttu-id="0a576-157">O</span><span class="sxs-lookup"><span data-stu-id="0a576-157">Y</span></span>               | <span data-ttu-id="0a576-158">N</span><span class="sxs-lookup"><span data-stu-id="0a576-158">N</span></span>            |
| <span data-ttu-id="0a576-159">propriété...</span><span class="sxs-lookup"><span data-stu-id="0a576-159">property...</span></span>   | <span data-ttu-id="0a576-160">O</span><span class="sxs-lookup"><span data-stu-id="0a576-160">Y</span></span>             | <span data-ttu-id="0a576-161">O</span><span class="sxs-lookup"><span data-stu-id="0a576-161">Y</span></span>               | <span data-ttu-id="0a576-162">N</span><span class="sxs-lookup"><span data-stu-id="0a576-162">N</span></span>            |
| <span data-ttu-id="0a576-163">propriétéN</span><span class="sxs-lookup"><span data-stu-id="0a576-163">propertyn</span></span>     | <span data-ttu-id="0a576-164">N</span><span class="sxs-lookup"><span data-stu-id="0a576-164">N</span></span>             | <span data-ttu-id="0a576-165">N</span><span class="sxs-lookup"><span data-stu-id="0a576-165">N</span></span>               | <span data-ttu-id="0a576-166">N</span><span class="sxs-lookup"><span data-stu-id="0a576-166">N</span></span>            |



 

<span data-ttu-id="0a576-167">Pour chacune de ces propriétés, vous devez déterminer les attributs à utiliser, puis les décrire formellement dans les fichiers XML de description de propriété (. propDesc).</span><span class="sxs-lookup"><span data-stu-id="0a576-167">For each of these properties, you need to determine what attributes it should have and then describe them formally in Property Description XML files (.propdesc).</span></span> <span data-ttu-id="0a576-168">Les attributs incluent le type de données, l’étiquette, la chaîne d’aide de la propriété, etc.</span><span class="sxs-lookup"><span data-stu-id="0a576-168">Attributes include the property's data type, label, help string and more.</span></span> <span data-ttu-id="0a576-169">Pour les propriétés indexables, vous devez prêter une attention particulière aux attributs de propriété suivants qui se trouvent dans l’élément XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   du fichier de description de propriété.</span><span class="sxs-lookup"><span data-stu-id="0a576-169">For indexable properties, you should pay particular attention to the following property attributes found in the [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML element of the Property Description file.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a576-170">Attribut</span><span class="sxs-lookup"><span data-stu-id="0a576-170">Attribute</span></span></th>
<th><span data-ttu-id="0a576-171">Description</span><span class="sxs-lookup"><span data-stu-id="0a576-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a576-172">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="0a576-172">inInvertedIndex</span></span></td>
<td><span data-ttu-id="0a576-173">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0a576-173">Optional.</span></span> <span data-ttu-id="0a576-174">Indique si une valeur de propriété de chaîne doit être décomposée en mots et chaque mot stocké dans l’index inversé.</span><span class="sxs-lookup"><span data-stu-id="0a576-174">Indicates whether a string property value should be broken into words and each word stored in the inverted index.</span></span> <span data-ttu-id="0a576-175">L’index inversé permet une recherche efficace de mots et d’expressions sur la valeur de propriété à l’aide de CONTAINs ou FREETEXT (par exemple, SELECT... OÙ contient &quot; someText &quot; ).</span><span class="sxs-lookup"><span data-stu-id="0a576-175">The inverted index enables efficient searching for words and phrases over the property value using CONTAINS or FREETEXT (for example, SELECT ... WHERE CONTAINS &quot;sometext&quot;).</span></span> <span data-ttu-id="0a576-176">Si la valeur est <strong>false</strong>, les recherches sont effectuées par rapport à la chaîne entière.</span><span class="sxs-lookup"><span data-stu-id="0a576-176">If set to <strong>FALSE</strong>, searches are done against the whole string.</span></span> <span data-ttu-id="0a576-177">La plupart des propriétés de chaîne doivent avoir la valeur <strong>true</strong>; les propriétés qui ne sont pas des chaînes doivent avoir la valeur <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-177">Most string properties should have this set to <strong>TRUE</strong>; non-string properties should have this set to <strong>FALSE</strong>.</span></span> <span data-ttu-id="0a576-178">La valeur par défaut est <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-178">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a576-179">isColumn</span><span class="sxs-lookup"><span data-stu-id="0a576-179">isColumn</span></span></td>
<td><span data-ttu-id="0a576-180">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0a576-180">Optional.</span></span> <span data-ttu-id="0a576-181">Indique si la propriété doit être stockée dans la base de données de recherche Windows en tant que colonne.</span><span class="sxs-lookup"><span data-stu-id="0a576-181">Indicates whether the property should be stored in the Windows Search database as a column.</span></span> <span data-ttu-id="0a576-182">Le stockage de la propriété en tant que colonne permet la récupération, le tri, le regroupement et le filtrage (autrement dit, à l’aide d’un prédicat à l’exception de CONTAINs ou FREETEXT) sur l’ensemble de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="0a576-182">Storing the property as a column enables retrieving, sorting, grouping, and filtering (that is, using any predicate except CONTAINS or FREETEXT) on the whole column value.</span></span> <span data-ttu-id="0a576-183">Les propriétés affichées pour l’utilisateur doivent avoir la valeur <strong>true</strong> , sauf s’il s’agit d’une propriété textuelle très volumineuse (telle que le corps d’un document) qui serait recherchée dans l’index inversé.</span><span class="sxs-lookup"><span data-stu-id="0a576-183">Properties displayed to the user should have this set to <strong>TRUE</strong> unless it is a very large textual property (like the body of a document) that would be searched in the inverted index.</span></span> <span data-ttu-id="0a576-184">La valeur par défaut est <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-184">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a576-185">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="0a576-185">isColumnSparse</span></span></td>
<td><span data-ttu-id="0a576-186">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0a576-186">Optional.</span></span> <span data-ttu-id="0a576-187">Indique si une propriété ne prend pas d’espace si la valeur est <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-187">Indicates whether a property takes no space if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="0a576-188">Une propriété non allouée prend de l’espace pour chaque élément, même si la valeur est <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-188">A non-sparse property takes space for every item, even if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="0a576-189">Si la propriété est à valeurs multiples, cet attribut a toujours la <strong>valeur true</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-189">If the property is multi-valued, this attribute is always <strong>TRUE</strong>.</span></span> <span data-ttu-id="0a576-190">Cet attribut doit avoir la valeur <strong>false</strong> uniquement si une valeur est présente pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="0a576-190">This attribute should be <strong>FALSE</strong> only if a value is present for every item.</span></span> <span data-ttu-id="0a576-191">La valeur par défaut est <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-191">The default is <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a576-192">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="0a576-192">columnIndexType</span></span></td>
<td><span data-ttu-id="0a576-193">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0a576-193">Optional.</span></span> <span data-ttu-id="0a576-194">Pour optimiser les requêtes, le moteur de recherche Windows peut créer des index secondaires pour les propriétés qui ont isColumn =<strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a576-194">To optimize querying, the Windows Search engine can create secondary indices for properties that have isColumn=<strong>TRUE</strong>.</span></span> <span data-ttu-id="0a576-195">Cela nécessite plus d’espace disque et de traitement pendant l’indexation, mais améliore les performances lors de l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="0a576-195">This requires more processing and disk space during indexing, but improves performance during querying.</span></span> <span data-ttu-id="0a576-196">Si la propriété tend à être triée, regroupée ou filtrée (c’est-à-dire en utilisant =, ! =, <, >, comme, MATCHES) fréquemment par les utilisateurs, cet attribut doit être défini sur &quot; OnDisk &quot; .</span><span class="sxs-lookup"><span data-stu-id="0a576-196">If the property tends to be sorted, grouped, or filtered (that is, using =, !=, <, >, LIKE, MATCHES) frequently by users, this attribute should be set to &quot;OnDisk&quot;.</span></span> <span data-ttu-id="0a576-197">La valeur par défaut est &quot; NotIndexed &quot; .</span><span class="sxs-lookup"><span data-stu-id="0a576-197">The default is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="0a576-198">Les valeurs suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="0a576-198">The following values are valid:</span></span>
<ul>
<li><span data-ttu-id="0a576-199">NotIndexed : aucun index secondaire n’est créé.</span><span class="sxs-lookup"><span data-stu-id="0a576-199">NotIndexed: No secondary index is created.</span></span></li>
<li><span data-ttu-id="0a576-200">OnDisk : créez et stockez un index secondaire sur le disque.</span><span class="sxs-lookup"><span data-stu-id="0a576-200">OnDisk: Create and store a secondary index on disk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a576-201">maxSize</span><span class="sxs-lookup"><span data-stu-id="0a576-201">maxSize</span></span></td>
<td><span data-ttu-id="0a576-202">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0a576-202">Optional.</span></span> <span data-ttu-id="0a576-203">Indique la taille maximale autorisée pour la valeur de propriété stockée dans la base de données de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="0a576-203">Indicates the maximum size allowed for the property value stored in the Windows search database.</span></span> <span data-ttu-id="0a576-204">Cette limite s’applique aux éléments indvidual d’un vecteur, et non au vecteur dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="0a576-204">This limit applies to the indvidual elements of a vector, not the vector as a whole.</span></span> <span data-ttu-id="0a576-205">Les valeurs au-delà de cette taille sont tronquées.</span><span class="sxs-lookup"><span data-stu-id="0a576-205">Values beyond this size are truncated.</span></span> <span data-ttu-id="0a576-206">La valeur par défaut est &quot; 128 &quot; (octets).</span><span class="sxs-lookup"><span data-stu-id="0a576-206">The default is &quot;128&quot; (bytes).</span></span><br/> <span data-ttu-id="0a576-207">Actuellement, Windows Search n’utilise pas le maxSize lors du calcul de la quantité de données qu’il accepte à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-207">Currently, Windows Search does not use the maxSize when calculating the amount of data it accepts from a file.</span></span> <span data-ttu-id="0a576-208">Au lieu de cela, la limite d’utilisation de la recherche Windows est le produit de la taille du fichier et le MaxGrowFactor (taille de fichier N \* MaxGrowFactor) lu à partir du Registre dans HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span><span class="sxs-lookup"><span data-stu-id="0a576-208">Instead, the limit Windows Search uses is the product of the size of the file and the MaxGrowFactor (file size N \* MaxGrowFactor) read from the registry at HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span></span> <span data-ttu-id="0a576-209">La valeur par défaut de MaxGrowFactor est quatre (4).</span><span class="sxs-lookup"><span data-stu-id="0a576-209">The default MaxGrowFactor is four (4).</span></span> <span data-ttu-id="0a576-210">Par conséquent, si la taille totale de votre type de fichier est faible, mais que les propriétés sont plus volumineuses, la recherche Windows peut ne pas accepter toutes les données de propriété que vous souhaitez émettre.</span><span class="sxs-lookup"><span data-stu-id="0a576-210">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="0a576-211">Toutefois, vous pouvez augmenter le MaxGrowFactor en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0a576-211">However, you can increase the MaxGrowFactor to suit your needs.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="0a576-212">Pour l’attribut columnIndexType, l’avantage des requêtes plus rapides doit être pesé par rapport à l’augmentation du temps d’indexation et des coûts d’espace que les indices secondaires peuvent engendrer.</span><span class="sxs-lookup"><span data-stu-id="0a576-212">For the columnIndexType attribute, the benefit of faster queries needs to be weighed against the greater indexing time and space costs that the secondary indices can incur.</span></span> <span data-ttu-id="0a576-213">Toutefois, ce coût est uniquement payé pour les éléments qui ont une valeur non **null** . par conséquent, pour la plupart des propriétés, cet attribut peut avoir la valeur « OnDisk ».</span><span class="sxs-lookup"><span data-stu-id="0a576-213">However, this cost is only paid for items that have a non-**null** value, so for most properties can have this attribute set to "OnDisk".</span></span>

 

### <a name="full-text-support"></a><span data-ttu-id="0a576-214">Prise en charge du texte intégral</span><span class="sxs-lookup"><span data-stu-id="0a576-214">Full-Text Support</span></span>

<span data-ttu-id="0a576-215">En règle générale, la recherche en texte intégral est prise en charge par les composants appelés [filtres](-search-3x-wds-extidx-filters.md). Toutefois, pour les types de fichiers texte avec des formats de fichiers non compliqués, les gestionnaires de propriétés peuvent être en mesure de fournir cette fonctionnalité avec moins d’efforts de développement.</span><span class="sxs-lookup"><span data-stu-id="0a576-215">Generally speaking, full-text search is supported by components called [filters](-search-3x-wds-extidx-filters.md); however, for text-based file types with uncomplicated file formats, property handlers may be able to provide this functionality with less development effort.</span></span> <span data-ttu-id="0a576-216">Vous devez consulter la section [contenu de texte intégral](../properties/building-property-handlers-property-handlers.md) pour obtenir une comparaison des fonctionnalités de filtre et de gestionnaire de propriétés pour vous aider à déterminer ce qui convient le mieux à votre type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-216">You should review the [Full-Text Contents](../properties/building-property-handlers-property-handlers.md) section for a comparison of filter and property handler functionality to help you decide what is best for your file type.</span></span> <span data-ttu-id="0a576-217">Il est particulièrement important que les filtres puissent gérer plusieurs identificateurs de code de langue (LCID) par fichier alors que les gestionnaires de propriétés ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="0a576-217">Of particular importance is the fact that filters can handle multiple language code identifiers (LCIDs) per file while property handlers cannot.</span></span>

> [!Note]  
> <span data-ttu-id="0a576-218">Étant donné que les gestionnaires de propriétés ne peuvent pas segmenter le contenu de la même façon que les filtres, les fichiers volumineux (même s’il s’agit de formats de fichiers non compliqués) doivent être complètement chargés en mémoire.</span><span class="sxs-lookup"><span data-stu-id="0a576-218">Because property handlers cannot chunk content the way filters can, large files (even if they are uncomplicated file formats) must be completely loaded into memory.</span></span>

 

### <a name="operating-system-implementatation-considerations"></a><span data-ttu-id="0a576-219">Considérations sur le Implementatation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="0a576-219">Operating System Implementatation Considerations</span></span>

### <a name="implementation-information-for-windows-7"></a><span data-ttu-id="0a576-220">Informations d’implémentation pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="0a576-220">Implementation Information for Windows 7</span></span>

<span data-ttu-id="0a576-221">Dans Windows 7 et versions ultérieures, il existe un nouveau comportement lors de l’inscription d’un gestionnaire de propriétés, d’un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)ou d’une nouvelle extension.</span><span class="sxs-lookup"><span data-stu-id="0a576-221">In Windows 7 and later, there is new behavior when registering a property handler, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), or new extension.</span></span> <span data-ttu-id="0a576-222">Lorsqu’un nouveau gestionnaire de propriétés et/ou **IFilter** est installé, les fichiers avec les extensions correspondantes sont automatiquement réindexés.</span><span class="sxs-lookup"><span data-stu-id="0a576-222">When a new property handler and/or **IFilter** is installed, files with the corresponding extensions are automatically reindexed.</span></span>

<span data-ttu-id="0a576-223">Dans Windows 7, il est recommandé d’installer un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) conjointement avec les gestionnaires de propriétés correspondants, et d’inscrire le **IFilter** avant le gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-223">In Windows 7 it is recommended that an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed in conjunction with its corresponding property handlers, and that the **IFilter** is registered before the property handler.</span></span> <span data-ttu-id="0a576-224">L’inscription du gestionnaire de propriétés lance la réindexation immédiate des fichiers précédemment indexés sans nécessiter un redémarrage, et tire parti des IFilter précédemment inscrits à des fins d’indexation du contenu.</span><span class="sxs-lookup"><span data-stu-id="0a576-224">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a reboot, and takes advantage of any previously registered IFilter(s) for the purpose of content indexing.</span></span>

<span data-ttu-id="0a576-225">Si seul un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est installé, sans gestionnaire de propriétés correspondant, la réindexation automatique se produit soit après un redémarrage du service d’indexation, soit par un redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="0a576-225">If only an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed, without a corresponding property handler, then automatic reindexing occurs either after a restart of the indexing service, or a reboot of the system.</span></span>

<span data-ttu-id="0a576-226">Pour plus d’informations sur les indicateurs de description de propriété spécifiques à Windows 7, consultez les rubriques de référence suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a576-226">For property description flags specific to Windows 7, see the following reference topics:</span></span>

-   [<span data-ttu-id="0a576-227">GETPROPERTYSTOREFLAGS</span><span class="sxs-lookup"><span data-stu-id="0a576-227">GETPROPERTYSTOREFLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [<span data-ttu-id="0a576-228">TYPE de PROPDESC \_ COLUMNINDEX \_</span><span class="sxs-lookup"><span data-stu-id="0a576-228">PROPDESC\_COLUMNINDEX\_TYPE</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [<span data-ttu-id="0a576-229">PROPDESC \_ SEARCHINFO, \_ indicateurs</span><span class="sxs-lookup"><span data-stu-id="0a576-229">PROPDESC\_SEARCHINFO\_FLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a><span data-ttu-id="0a576-230">Informations d’implémentation pour Windows Vista et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="0a576-230">Implementation Information for Windows Vista and Earlier</span></span>

<span data-ttu-id="0a576-231">Avant Windows Vista, les filtres fournissaient la prise en charge de l’analyse et de l’énumération du contenu et des propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="0a576-231">Prior to Windows Vista, filters provided support for parsing and enumerating file content and properties.</span></span> <span data-ttu-id="0a576-232">Avec l’introduction du système de propriétés, les gestionnaires de propriétés gèrent les propriétés de fichier, tandis que les filtres gèrent le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-232">With the introduction of the property system, property handlers handle file properties while filters handle file content.</span></span> <span data-ttu-id="0a576-233">Pour Windows Vista, vous devez développer uniquement une implémentation partielle de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)en coordination avec un gestionnaire de propriétés, comme décrit dans [meilleures pratiques pour la création de gestionnaires de filtres dans la recherche Windows](-search-3x-wds-extidx-filters.md).</span><span class="sxs-lookup"><span data-stu-id="0a576-233">For Windows Vista, you need develop only a partial implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)interface in coordination with a property handler, as described in [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).</span></span>

<span data-ttu-id="0a576-234">Alors que le système de propriétés est également inclus dans l’installation de Windows Search pour Windows XP, les applications tierces et héritées peuvent exiger que les filtres gèrent le contenu et les propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-234">While the property system is also included with the Windows Search installation for Windows XP, third-party and legacy applications may require that filters handle both content and properties.</span></span> <span data-ttu-id="0a576-235">Par conséquent, si vous développez sur la plateforme Windows XP, vous devez fournir une implémentation de filtre complète, ainsi qu’un gestionnaire de propriétés pour votre type de fichier ou propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0a576-235">Therefore, if you are developing on the Windows XP platform, you should provide a full filter implementation as well as a property handler for your file type or custom property.</span></span>

 

## <a name="writing-property-description-files"></a><span data-ttu-id="0a576-236">Écriture de fichiers de description de propriété</span><span class="sxs-lookup"><span data-stu-id="0a576-236">Writing Property Description Files</span></span>

<span data-ttu-id="0a576-237">La structure des fichiers XML de description de propriété (. propDesc) est décrite dans la rubrique [PropertyDescription](../properties/propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="0a576-237">The structure of property description XML files (.propdesc) is described in the [propertyDescription](../properties/propdesc-schema-propertydescription.md) topic.</span></span> <span data-ttu-id="0a576-238">Les attributs de l’élément [searchInfo](../properties/propdesc-schema-searchinfo.md) présentent un intérêt particulier pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="0a576-238">Of particular interest for search are the attributes of the [searchInfo](../properties/propdesc-schema-searchinfo.md) element.</span></span> <span data-ttu-id="0a576-239">Une fois que vous avez choisi les propriétés à prendre en charge, vous devez créer et inscrire des fichiers de description de propriété pour chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="0a576-239">Once you've decided which properties to support, you need to create and register property description files for each properties.</span></span> <span data-ttu-id="0a576-240">Lorsque vous inscrivez vos fichiers. propDesc, ils sont inclus dans la liste de description de la propriété du schéma et deviennent des noms de colonnes dans la Banque de propriétés du moteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="0a576-240">When you register your .propdesc files, they are included in the schema's property description list and become column names within the Search engine's property store.</span></span>

<span data-ttu-id="0a576-241">Vous pouvez enregistrer vos descriptions de propriété personnalisées à l’aide de la fonction [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , une API wrapper qui appelle le IPropertySystem :: RegisterPropertySchema du sous-système de schéma.</span><span class="sxs-lookup"><span data-stu-id="0a576-241">You can register your custom property descriptions using the [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) function, a wrapper API that calls the schema subsystem's IPropertySystem::RegisterPropertySchema.</span></span> <span data-ttu-id="0a576-242">Cette fonction informe le sous-système de schéma de l’ajout de fichiers de schéma de description de propriété (. propDesc), en utilisant des chemins d’accès de fichier au (x) fichier (s). propDesc sur l’ordinateur local, généralement le répertoire d’installation de l’application sous « Program Files ».</span><span class="sxs-lookup"><span data-stu-id="0a576-242">This function informs the schema subsystem of the addition of property description schema (.propdesc) files, using file path(s) to the .propdesc file(s) on the local machine, usually the application's install directory under "Program Files".</span></span> <span data-ttu-id="0a576-243">En règle générale, une installation ou une application (par exemple, votre programme d’installation de gestionnaire de propriétés) appellera cette méthode après l’installation du ou des fichiers. propDesc.</span><span class="sxs-lookup"><span data-stu-id="0a576-243">Typically, a setup or application (for example, your property handler installer) will call this method after installing the .propdesc file(s).</span></span>

 

## <a name="implementing-property-handlers"></a><span data-ttu-id="0a576-244">Implémentation de gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-244">Implementing Property Handlers</span></span>

<span data-ttu-id="0a576-245">Le développement d’un gestionnaire de propriétés implique l’implémentation des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a576-245">Developing a property handler involves implementing the following interfaces:</span></span>

-   <span data-ttu-id="0a576-246">IInitialzeWithStream : fournit l’initialisation basée sur le flux de votre gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-246">IInitialzeWithStream: Provides stream-based initialization of your property handler.</span></span>
-   <span data-ttu-id="0a576-247">IPropertyStore : énumère, obtient et définit les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="0a576-247">IPropertyStore: Enumerates, gets, and sets property values.</span></span>
-   <span data-ttu-id="0a576-248">IPropertyStoreCapabilities : facultatif.</span><span class="sxs-lookup"><span data-stu-id="0a576-248">IPropertyStoreCapabilities: Optional.</span></span> <span data-ttu-id="0a576-249">Indique si les utilisateurs peuvent modifier une propriété à partir d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a576-249">Identifies whether users can edit a property from a user interface.</span></span>

### <a name="iinitializewithstream"></a><span data-ttu-id="0a576-250">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="0a576-250">IInitializeWithStream</span></span>

<span data-ttu-id="0a576-251">Comme décrit dans la rubrique [système de propriétés](../properties/building-property-handlers.md) , nous vous recommandons vivement d’implémenter des gestionnaires de propriétés avec **IInitializeWithStream** pour effectuer une initialisation basée sur le flux.</span><span class="sxs-lookup"><span data-stu-id="0a576-251">As described in the [Property System](../properties/building-property-handlers.md) topic, we strongly recommend implementing property handlers with **IInitializeWithStream** to do stream-based initialization.</span></span> <span data-ttu-id="0a576-252">Si vous avez choisi de ne pas implémenter IInitializeWithStream, le gestionnaire de propriétés doit refuser de s’exécuter dans le processus d’isolation en définissant l’indicateur DisableProcessIsolation sur la clé de Registre du gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-252">If you chose not to implement IInitializeWithStream, the property handler must opt out of running in the isolation process by setting the DisableProcessIsolation flag on the property handler's registry key.</span></span> <span data-ttu-id="0a576-253">La désactivation de l’isolation de processus est généralement prévue uniquement pour les gestionnaires de propriétés hérités et doit être évitée de manière ardue par tout nouveau code.</span><span class="sxs-lookup"><span data-stu-id="0a576-253">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

### <a name="ipropertystore"></a><span data-ttu-id="0a576-254">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="0a576-254">IPropertyStore</span></span>

<span data-ttu-id="0a576-255">Pour créer un gestionnaire de propriétés, vous devez implémenter l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) avec les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a576-255">To create a property handler, you must implement the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface with the following methods.</span></span>



| <span data-ttu-id="0a576-256">Méthode</span><span class="sxs-lookup"><span data-stu-id="0a576-256">Method</span></span>   | <span data-ttu-id="0a576-257">Description</span><span class="sxs-lookup"><span data-stu-id="0a576-257">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="0a576-258">Commit</span><span class="sxs-lookup"><span data-stu-id="0a576-258">Commit</span></span>   | <span data-ttu-id="0a576-259">Enregistre une modification de propriété dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-259">Saves a property change to the file.</span></span>                                |
| <span data-ttu-id="0a576-260">GetAt</span><span class="sxs-lookup"><span data-stu-id="0a576-260">GetAt</span></span>    | <span data-ttu-id="0a576-261">Récupère une clé de propriété à partir du tableau de propriétés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="0a576-261">Retrieves a property key from an item's array of properties.</span></span>        |
| <span data-ttu-id="0a576-262">GetCount</span><span class="sxs-lookup"><span data-stu-id="0a576-262">GetCount</span></span> | <span data-ttu-id="0a576-263">Obtient le nombre de propriétés jointes au fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-263">Gets the number of properties attached to the file.</span></span>                 |
| <span data-ttu-id="0a576-264">GetValue</span><span class="sxs-lookup"><span data-stu-id="0a576-264">GetValue</span></span> | <span data-ttu-id="0a576-265">Récupère des données pour une propriété spécifique.</span><span class="sxs-lookup"><span data-stu-id="0a576-265">Retrieves data for a specific property.</span></span>                             |
| <span data-ttu-id="0a576-266">SetValue</span><span class="sxs-lookup"><span data-stu-id="0a576-266">SetValue</span></span> | <span data-ttu-id="0a576-267">Définit une nouvelle valeur de propriété ou remplace ou supprime une valeur existante.</span><span class="sxs-lookup"><span data-stu-id="0a576-267">Sets a new property value or replaces or removes an existing value.</span></span> |



 

 

 

<span data-ttu-id="0a576-268">Les considérations importantes relatives à l’implémentation de cette interface sont incluses dans la documentation [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="0a576-268">Important considerations for implementing this interface are included in the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) documentation.</span></span>

> [!Note]  
> <span data-ttu-id="0a576-269">Si votre gestionnaire de propriétés émet plusieurs valeurs pour la même propriété pour un élément donné, seule la dernière valeur émise est stockée dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="0a576-269">If your property handler emits multiple values for the same property for a given item, only the last value emitted is stored in the catalog.</span></span>

 

 

### <a name="ipropertystorecapabilities"></a><span data-ttu-id="0a576-270">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="0a576-270">IPropertyStoreCapabilities</span></span>

<span data-ttu-id="0a576-271">Les gestionnaires de propriétés peuvent éventuellement implémenter cette interface pour désactiver la possibilité pour un utilisateur de modifier des propriétés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0a576-271">Property handlers can optionally implement this interface to disable a user's ability to edit specific properties.</span></span> <span data-ttu-id="0a576-272">Ces propriétés sont généralement modifiables dans la page de détails et le volet, mais leur modification n’est pas autorisée sous le gestionnaire d’implémentation de propriété.</span><span class="sxs-lookup"><span data-stu-id="0a576-272">These properties are normally editable in the Details page and pane but editing them is not allowed under the implementing property handler.</span></span> <span data-ttu-id="0a576-273">L’implémentation de cette interface offre une meilleure expérience utilisateur que l’alternative, une simple erreur d’exécution à partir de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="0a576-273">Implementing this interface correctly provides a better user experience than the alternative—a simple run-time error from the Shell.</span></span>

 

## <a name="ensuring-your-items-get-indexed"></a><span data-ttu-id="0a576-274">Vérifier que vos éléments sont indexés</span><span class="sxs-lookup"><span data-stu-id="0a576-274">Ensuring Your Items Get Indexed</span></span>

<span data-ttu-id="0a576-275">Maintenant que vous avez implémenté votre gestionnaire de propriétés, vous devez vous assurer que les éléments que votre gestionnaire est inscrit pour être indexés.</span><span class="sxs-lookup"><span data-stu-id="0a576-275">Now that you've implemented your property handler, you want to make sure the items your handler is registered for get indexed.</span></span> <span data-ttu-id="0a576-276">Vous pouvez utiliser le [Gestionnaire de catalogue](-search-3x-wds-mngidx-catalog-manager.md) pour lancer la réindexation, et vous pouvez également utiliser le [Gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md) pour configurer des règles par défaut indiquant les URL que l’indexeur doit analyser.</span><span class="sxs-lookup"><span data-stu-id="0a576-276">You can use the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to initiate re-indexing, and you can also use the [Crawl Scope Manager](-search-3x-wds-extidx-csm.md) to set up default rules indicating the URLs you want the Indexer to crawl.</span></span> <span data-ttu-id="0a576-277">Une autre option consiste à suivre l’exemple de code de réindexation dans les [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="0a576-277">Another option is to follow the ReIndex code sample in the [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="0a576-278">Pour plus d’informations, reportez-vous à [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [à l’utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="0a576-278">For further information, refer to [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

 

## <a name="installing-and-registering-property-handlers"></a><span data-ttu-id="0a576-279">Installation et inscription de gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-279">Installing and Registering Property Handlers</span></span>

<span data-ttu-id="0a576-280">Avec le gestionnaire de propriétés implémenté, il doit être enregistré et son extension de nom de fichier associée au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="0a576-280">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="0a576-281">L’exemple suivant montre les clés de Registre et les valeurs requises pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="0a576-281">The following example shows the registry keys and values required to do this.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a><span data-ttu-id="0a576-282">Test et dépannage des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-282">Testing and Troubleshooting Property Handlers</span></span>

<span data-ttu-id="0a576-283">La liste suivante fournit des conseils sur les types de tests que vous devez effectuer :</span><span class="sxs-lookup"><span data-stu-id="0a576-283">The following list provides advice on the kinds of tests you should perform:</span></span>

-   <span data-ttu-id="0a576-284">Testez l’obtention de la sortie de chaque propriété unique prise en charge par le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-284">Test getting output from every single property supported by the file type.</span></span>
-   <span data-ttu-id="0a576-285">Utilisez des valeurs de propriété volumineuses, par exemple, utilisez une large balise Meta dans des documents HTML.</span><span class="sxs-lookup"><span data-stu-id="0a576-285">Use big property values, for example, use a large metatag in HTML documents.</span></span>
-   <span data-ttu-id="0a576-286">Vérifiez que le gestionnaire de propriétés ne perd pas les handles de fichiers en les modifiant après avoir obtenu la sortie du gestionnaire de propriétés, ou à l’aide d’un outil comme oh.exe avant et après l’énumération des propriétés de fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-286">Check that the property handler does not leak file handles by editing it after getting output from the property handler, or by using a tool like oh.exe before and after enumerating file properties.</span></span>
-   <span data-ttu-id="0a576-287">Testez tous les types de fichiers associés au gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-287">Test all file types associated with the property handler.</span></span> <span data-ttu-id="0a576-288">Par exemple, vérifiez que le filtre HTML fonctionne avec les types de fichiers. htm et. html.</span><span class="sxs-lookup"><span data-stu-id="0a576-288">For example, check that the HTML filter works with .htm and .html file types.</span></span>
-   <span data-ttu-id="0a576-289">Testez les fichiers endommagés.</span><span class="sxs-lookup"><span data-stu-id="0a576-289">Test with corrupted files.</span></span> <span data-ttu-id="0a576-290">Le gestionnaire de propriétés doit échouer correctement.</span><span class="sxs-lookup"><span data-stu-id="0a576-290">Property handler should fail gracefully.</span></span>
-   <span data-ttu-id="0a576-291">Si une application prend en charge le chiffrement, vérifiez que le gestionnaire de propriétés ne génère pas de texte chiffré.</span><span class="sxs-lookup"><span data-stu-id="0a576-291">If an application supports encryption, test that the property handler does not output encrypted text.</span></span>
-   <span data-ttu-id="0a576-292">Si votre gestionnaire de propriétés prend en charge la recherche en texte intégral :</span><span class="sxs-lookup"><span data-stu-id="0a576-292">If your property handler supports full-text search:</span></span>
    -   <span data-ttu-id="0a576-293">Utilisez plusieurs caractères Unicode spéciaux dans le contenu du fichier et testez leur sortie.</span><span class="sxs-lookup"><span data-stu-id="0a576-293">Use multiple special Unicode characters in the file contents and test for their output.</span></span>
    -   <span data-ttu-id="0a576-294">Testez la gestion des documents de très grande taille pour vous assurer que le gestionnaire de propriétés fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="0a576-294">Test the handling of very large documents to ensure the property handler works as expected.</span></span>

### <a name="installation-and-setup-tests"></a><span data-ttu-id="0a576-295">Tests d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="0a576-295">Installation and Setup Tests</span></span>

<span data-ttu-id="0a576-296">Enfin, vous devez tester vos routines d’installation et de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="0a576-296">Lastly, you need to test your install and uninstall routines.</span></span>

-   <span data-ttu-id="0a576-297">L’installation doit récupérer après l’échec des installations (par exemple, en annulant, puis en redémarrant le programme d’installation).</span><span class="sxs-lookup"><span data-stu-id="0a576-297">Installation must recover from failed installations (for example, from canceling and then restarting setup).</span></span>
-   <span data-ttu-id="0a576-298">La désinstallation doit supprimer tous les fichiers associés au gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-298">Uninstall must delete all files associated with the property handler.</span></span>
-   <span data-ttu-id="0a576-299">La désinstallation ne doit pas supprimer les fichiers autres que ceux associés à l’installation du gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-299">Uninstall must not delete files other than the ones associated with the property handler installation.</span></span>
-   <span data-ttu-id="0a576-300">Les clés de Registre associées au gestionnaire de propriétés doivent être supprimées lors de la désinstallation de.</span><span class="sxs-lookup"><span data-stu-id="0a576-300">Registry keys associated with the property handler must be removed when uninstalled.</span></span>
-   <span data-ttu-id="0a576-301">La désinstallation doit fonctionner même si les fichiers sont supprimés du répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="0a576-301">Uninstall must work even if files are deleted from the installation directory.</span></span>

### <a name="troubleshooting-property-handlers"></a><span data-ttu-id="0a576-302">Dépannage des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-302">Troubleshooting Property Handlers</span></span>

<span data-ttu-id="0a576-303">Voici quelques erreurs courantes lors du développement de gestionnaires de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0a576-303">The following are some common errors made while developing property handlers:</span></span>

-   <span data-ttu-id="0a576-304">Installation des fichiers. propDesc ou des dll dans un répertoire utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a576-304">Installing .propdesc files or DLLs under a user directory.</span></span>
-   <span data-ttu-id="0a576-305">Inscription de composants à l’aide de chemins d’accès relatifs.</span><span class="sxs-lookup"><span data-stu-id="0a576-305">Registering components using relative paths.</span></span>
-   <span data-ttu-id="0a576-306">Inscription des composants sous HKEY \_ Current \_ User au lieu de HKEY \_ local \_ machine.</span><span class="sxs-lookup"><span data-stu-id="0a576-306">Registering components under HKEY\_CURRENT\_USER instead of HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="0a576-307">Oubli de définir DisableProcessIsolation pour les gestionnaires qui ne sont pas des flux.</span><span class="sxs-lookup"><span data-stu-id="0a576-307">Forgetting to set DisableProcessIsolation for non-stream handlers.</span></span>
-   <span data-ttu-id="0a576-308">Placement du fichier de test dans un emplacement non indexé.</span><span class="sxs-lookup"><span data-stu-id="0a576-308">Placing the test file in an unindexed location.</span></span>

<span data-ttu-id="0a576-309">Si vous avez des difficultés à faire fonctionner votre gestionnaire de propriétés avec l’indexeur, voici quelques conseils pour vous aider à résoudre les problèmes :</span><span class="sxs-lookup"><span data-stu-id="0a576-309">If you're having trouble getting your property handler working with the indexer, here are some tips to help you troubleshoot:</span></span>

-   <span data-ttu-id="0a576-310">Vérifiez que vos descriptions de propriété (fichiers. propDesc) sont marquées isColumn = "**true**", isViewable = "**true**" et isQueryable = "**true**" selon le cas.</span><span class="sxs-lookup"><span data-stu-id="0a576-310">Verify that your property descriptions (.propdesc files) are marked isColumn="**true**", isViewable="**true**", and isQueryable="**true**" as appropriate.</span></span>
-   <span data-ttu-id="0a576-311">Vérifiez que vos fichiers. propDesc se trouvent dans un emplacement global.</span><span class="sxs-lookup"><span data-stu-id="0a576-311">Verify that your .propdesc files are in a global location.</span></span>
-   <span data-ttu-id="0a576-312">Vérifiez que vous avez enregistré vos fichiers. propDesc à l’aide de chemins absolus.</span><span class="sxs-lookup"><span data-stu-id="0a576-312">Verify that you registered your .propdesc files using absolute paths.</span></span>
-   <span data-ttu-id="0a576-313">Vérifiez que le journal des événements n’a pas enregistré d’erreurs lors de l’inscription de votre fichier. propDesc.</span><span class="sxs-lookup"><span data-stu-id="0a576-313">Verify that the event log did not record any failures from registering your .propdesc file.</span></span>
-   <span data-ttu-id="0a576-314">Vérifiez que vos dll se trouvent dans un emplacement global (et non sous votre profil utilisateur).</span><span class="sxs-lookup"><span data-stu-id="0a576-314">Verify that your DLLs is in a global location (and not under your user profile).</span></span>
-   <span data-ttu-id="0a576-315">Vérifiez que vos dll sont inscrites sous HKEY \_ local \_ machine \\ Software \\ classes.</span><span class="sxs-lookup"><span data-stu-id="0a576-315">Verify that your DLLs is registered under HKEY\_LOCAL\_MACHINE\\Software\\Classes.</span></span>
-   <span data-ttu-id="0a576-316">Vérifiez que vos dll sont inscrites à l’aide de chemins d’accès complets (ou de chaînes SZ de l’extension REG \_ \_ qui se développent en chemins absolus à l’aide de variables d’environnement connues par le compte système).</span><span class="sxs-lookup"><span data-stu-id="0a576-316">Verify that your DLLs is registered using full paths (or REG\_EXPAND\_SZ strings that expand to absolute paths using environment variables known by the System account).</span></span>
-   <span data-ttu-id="0a576-317">Vérifiez que votre gestionnaire de propriétés fonctionne sous l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="0a576-317">Verify that your property handler works under Windows Explorer.</span></span>
-   <span data-ttu-id="0a576-318">Bien que nous vous recommandons d’utiliser IInitializeWithStream, si vous devez utiliser IInitializeWithFile ou IInitializeWithItem, vérifiez que vous spécifiez DisableProcessIsolation.</span><span class="sxs-lookup"><span data-stu-id="0a576-318">While we recommend using IInitializeWithStream, if you must use IInitializeWithFile or IInitializeWithItem, verify that you specify DisableProcessIsolation.</span></span>
-   <span data-ttu-id="0a576-319">Vérifiez que le panneau de configuration options d’indexation répertorie votre type de fichier en tant que type de fichier indexé.</span><span class="sxs-lookup"><span data-stu-id="0a576-319">Verify that the Indexing Options Control Panel lists your file type as an indexed file type.</span></span>
-   <span data-ttu-id="0a576-320">Vérifiez que le fichier de test se trouve dans un emplacement indexé.</span><span class="sxs-lookup"><span data-stu-id="0a576-320">Verify that the test file is in an indexed location.</span></span>
-   <span data-ttu-id="0a576-321">Vérifiez que le fichier de test a été modifié depuis que vous avez installé votre gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a576-321">Verify that the test file has been modified since you installed your property handler.</span></span>

<span data-ttu-id="0a576-322">Si votre fichier de test se trouve dans un emplacement indexé et que l’indexeur a déjà analysé cet emplacement, vous devez modifier le fichier d’une façon pour déclencher la réindexation du fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-322">If your test file is in an indexed location and the indexer has already crawled that location, you need to modify the file in some way in order to trigger a reindexing of the file.</span></span>

 

## <a name="using-system-supplied-property-handlers"></a><span data-ttu-id="0a576-323">Utilisation de gestionnaires de propriétés System-Supplied</span><span class="sxs-lookup"><span data-stu-id="0a576-323">Using System-Supplied Property Handlers</span></span>

<span data-ttu-id="0a576-324">Windows comprend un certain nombre de gestionnaires de propriétés fournis par le système que vous pouvez utiliser si le format de votre type de fichier est compatible.</span><span class="sxs-lookup"><span data-stu-id="0a576-324">Windows includes a number of system-supplied property handlers that you can use if the format of your file type is compatible.</span></span> <span data-ttu-id="0a576-325">Si vous définissez une nouvelle extension de fichier qui utilise l’un de ces formats, vous pouvez utiliser les gestionnaires fournis par le système en inscrivant l’identificateur de classe du gestionnaire (CLSID) pour votre extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-325">If you define a new file extension that uses one of these formats you can use the system-provided handlers by registering the handler class identifier (CLSID) for your file extension.</span></span>

<span data-ttu-id="0a576-326">Vous pouvez utiliser le CLSID indiqué dans le tableau suivant pour inscrire les gestionnaires de propriétés fournis par le système pour votre type de format de fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-326">You can use the CLSID listed in the following table to register the system-supplied property handlers for your file format type.</span></span>



| <span data-ttu-id="0a576-327">Format</span><span class="sxs-lookup"><span data-stu-id="0a576-327">Format</span></span>          | <span data-ttu-id="0a576-328">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a576-328">CLSID</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="0a576-329">Doc OLE</span><span class="sxs-lookup"><span data-stu-id="0a576-329">OLE DocFile</span></span>     | <span data-ttu-id="0a576-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span><span class="sxs-lookup"><span data-stu-id="0a576-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span></span> |
| <span data-ttu-id="0a576-331">Enregistrer le fichier XML de jeu</span><span class="sxs-lookup"><span data-stu-id="0a576-331">Save Game XML</span></span>   | <span data-ttu-id="0a576-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span><span class="sxs-lookup"><span data-stu-id="0a576-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span></span> |
| <span data-ttu-id="0a576-333">Gestionnaire XPS/OPC</span><span class="sxs-lookup"><span data-stu-id="0a576-333">XPS/OPC handler</span></span> | <span data-ttu-id="0a576-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span><span class="sxs-lookup"><span data-stu-id="0a576-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span></span> |
| <span data-ttu-id="0a576-335">XML</span><span class="sxs-lookup"><span data-stu-id="0a576-335">XML</span></span>             | <span data-ttu-id="0a576-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span><span class="sxs-lookup"><span data-stu-id="0a576-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span></span> |



 

<span data-ttu-id="0a576-337">Avant de créer une propriété personnalisée, vous devez vous assurer qu’il n’existe pas de propriété définie par le système que vous pouvez utiliser à la place.</span><span class="sxs-lookup"><span data-stu-id="0a576-337">Before creating a custom property, you should be sure there isn't a system-defined property you can use instead.</span></span> <span data-ttu-id="0a576-338">Vous pouvez énumérer les propriétés définies par le système en appelant [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) ou à l’aide de l’outil en ligne de commande prop.exe.</span><span class="sxs-lookup"><span data-stu-id="0a576-338">You can enumerate the system-defined properties by calling [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) or using the prop.exe command line tool.</span></span>

<span data-ttu-id="0a576-339">Le schéma système définit la façon dont ces propriétés interagissent avec l’indexeur, et vous ne pouvez pas le modifier.</span><span class="sxs-lookup"><span data-stu-id="0a576-339">The system schema defines how these properties interact with the indexer, and you cannot change that.</span></span> <span data-ttu-id="0a576-340">En outre, l’application que vous utilisez pour créer, modifier et enregistrer votre type de fichier doit également se conformer à certains comportements.</span><span class="sxs-lookup"><span data-stu-id="0a576-340">Furthermore, the application you use to create, edit and save your file type needs to conform to certain behavior as well.</span></span> <span data-ttu-id="0a576-341">Par exemple, si l’application implémente l’enregistrement sécurisé (où un fichier temporaire est créé lors de la modification, puis ReplaceFile () est utilisé pour échanger la nouvelle version de l’ancien), elle doit transférer toutes les propriétés du fichier d’origine vers le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="0a576-341">For example, if the application implements safe save (whereby a temporary file is created during editing, and then ReplaceFile() is used to swap the new version for the old), it must transfer all of the properties from the original file to the new file.</span></span> <span data-ttu-id="0a576-342">Dans le cas contraire, le fichier perd les propriétés ajoutées par les utilisateurs ou d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="0a576-342">Failure to do means the file loses properties added by users or other applications.</span></span>

 

<span data-ttu-id="0a576-343">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="0a576-343">**Example**</span></span>

<span data-ttu-id="0a576-344">L’exemple suivant montre l’inscription du gestionnaire OLE DocFile fourni par le système pour un type de fichier avec un. Extension OLEDocFile.</span><span class="sxs-lookup"><span data-stu-id="0a576-344">The following shows the registration of the system-supplied OLE DocFile handler for a file type with a .OLEDocFile extension.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

<span data-ttu-id="0a576-345">L’exemple suivant montre l’inscription des informations de la liste de propriétés pour les propriétés de. Les fichiers OLEDocFile s’affichent sous l’onglet Détails et le volet.</span><span class="sxs-lookup"><span data-stu-id="0a576-345">The following shows the registration of the property list information so properties of .OLEDocFile files are displayed on the Details tab and pane.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a><span data-ttu-id="0a576-346">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a576-346">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0a576-347">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="0a576-347">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a576-348">Mappages de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-348">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)
</dt> <dt>

<span data-ttu-id="0a576-349">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0a576-349">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0a576-350">Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="0a576-350">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[<span data-ttu-id="0a576-351">Processus d’indexation</span><span class="sxs-lookup"><span data-stu-id="0a576-351">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="0a576-352">Développement de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="0a576-352">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="0a576-353">Propriétés définies par le système pour les formats de fichiers personnalisés</span><span class="sxs-lookup"><span data-stu-id="0a576-353">System-Defined Properties for Custom File Formats</span></span>](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

<span data-ttu-id="0a576-354">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="0a576-354">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0a576-355">Système de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a576-355">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="0a576-356">[Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0a576-356">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> <dt>

[<span data-ttu-id="0a576-357">Exemples du kit de développement logiciel Windows Search</span><span class="sxs-lookup"><span data-stu-id="0a576-357">Windows Search SDK Samples</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
