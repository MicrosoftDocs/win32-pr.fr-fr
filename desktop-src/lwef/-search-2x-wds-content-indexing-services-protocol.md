---
title: Protocole des services d’indexation de contenu
description: Ce document est une spécification du protocole de service d’indexation de contenu.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5265d9d8c802b278b4349ef4b8248b068dc7edc4
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492291"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="2babc-103">Protocole des services d’indexation de contenu</span><span class="sxs-lookup"><span data-stu-id="2babc-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="2babc-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2babc-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2babc-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="2babc-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="2babc-106">Spécification de protocole, version 0,12</span><span class="sxs-lookup"><span data-stu-id="2babc-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="2babc-107">1 Introduction</span><span class="sxs-lookup"><span data-stu-id="2babc-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="2babc-108">1.1 Glossaire</span><span class="sxs-lookup"><span data-stu-id="2babc-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="2babc-109">1.2 Références</span><span class="sxs-lookup"><span data-stu-id="2babc-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="2babc-110">Vue d’ensemble du protocole 1,3 (synopsis)</span><span class="sxs-lookup"><span data-stu-id="2babc-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="2babc-111">1.4 Relation aux autres protocoles</span><span class="sxs-lookup"><span data-stu-id="2babc-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="2babc-112">1,5 conditions préalables et conditions préalables</span><span class="sxs-lookup"><span data-stu-id="2babc-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="2babc-113">1.6 Instruction d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="2babc-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="2babc-114">1.7 Contrôle de version et négociation de capacité</span><span class="sxs-lookup"><span data-stu-id="2babc-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="2babc-115">1.8 Champs extensibles de fournisseur</span><span class="sxs-lookup"><span data-stu-id="2babc-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="2babc-116">1.9 Affectations de normes</span><span class="sxs-lookup"><span data-stu-id="2babc-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="2babc-117">2 Messages</span><span class="sxs-lookup"><span data-stu-id="2babc-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="2babc-118">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="2babc-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="2babc-119">2.2 Syntaxe de message</span><span class="sxs-lookup"><span data-stu-id="2babc-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="2babc-120">3 Détails du protocole</span><span class="sxs-lookup"><span data-stu-id="2babc-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="2babc-121">Détails du serveur 3,1</span><span class="sxs-lookup"><span data-stu-id="2babc-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="2babc-122">Détails du client 3,2</span><span class="sxs-lookup"><span data-stu-id="2babc-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="2babc-123">4 Exemples de protocoles</span><span class="sxs-lookup"><span data-stu-id="2babc-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="2babc-124">4,1 exemple 1</span><span class="sxs-lookup"><span data-stu-id="2babc-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="2babc-125">4,2 exemple 2</span><span class="sxs-lookup"><span data-stu-id="2babc-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="2babc-126">5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="2babc-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="2babc-127">5.1 Considérations relatives à la sécurité pour les implémenteurs</span><span class="sxs-lookup"><span data-stu-id="2babc-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="2babc-128">5.2 Index de paramètres de sécurité</span><span class="sxs-lookup"><span data-stu-id="2babc-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="2babc-129">6 index du comportement spécifique à la version</span><span class="sxs-lookup"><span data-stu-id="2babc-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="2babc-130">Ce document est une spécification du protocole de service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="2babc-131">La documentation du programme de protocole du serveur de groupe de travail (WSPP) est destinée à être utilisée conjointement avec la documentation sur les normes publiques, la conception de la programmation réseau et les concepts des systèmes distribués de groupe de travail Windows, et suppose que le lecteur est familiarisé avec le matériel mentionné ci-dessus ou qu’il y accède immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2babc-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="2babc-132">Une spécification de protocole WSPP ne nécessite pas l’utilisation d’outils de programmation ou d’environnements de programmation Microsoft pour permettre à un licencié de développer une implémentation.</span><span class="sxs-lookup"><span data-stu-id="2babc-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="2babc-133">Les titulaires de licences qui ont accès aux outils et aux environnements de programmation de Microsoft sont gratuits pour en tirer parti.</span><span class="sxs-lookup"><span data-stu-id="2babc-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="2babc-134">1 Introduction</span><span class="sxs-lookup"><span data-stu-id="2babc-134">1 Introduction</span></span>

-   [<span data-ttu-id="2babc-135">1.1 Glossaire</span><span class="sxs-lookup"><span data-stu-id="2babc-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="2babc-136">1.2 Références</span><span class="sxs-lookup"><span data-stu-id="2babc-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="2babc-137">Vue d’ensemble du protocole 1,3 (synopsis)</span><span class="sxs-lookup"><span data-stu-id="2babc-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="2babc-138">1.4 Relation aux autres protocoles</span><span class="sxs-lookup"><span data-stu-id="2babc-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="2babc-139">1,5 conditions préalables et conditions préalables</span><span class="sxs-lookup"><span data-stu-id="2babc-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="2babc-140">1.6 Instruction d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="2babc-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="2babc-141">1.7 Contrôle de version et négociation de capacité</span><span class="sxs-lookup"><span data-stu-id="2babc-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="2babc-142">1.8 Champs extensibles de fournisseur</span><span class="sxs-lookup"><span data-stu-id="2babc-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="2babc-143">1.9 Affectations de normes</span><span class="sxs-lookup"><span data-stu-id="2babc-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="2babc-144">1.1 Glossaire</span><span class="sxs-lookup"><span data-stu-id="2babc-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="2babc-145">Les termes suivants sont définis dans la section Glossaire de \[ ms-sys \] :</span><span class="sxs-lookup"><span data-stu-id="2babc-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="2babc-146">GUID</span><span class="sxs-lookup"><span data-stu-id="2babc-146">GUID</span></span>
> -   <span data-ttu-id="2babc-147">Little endian</span><span class="sxs-lookup"><span data-stu-id="2babc-147">Little Endian</span></span>
> -   <span data-ttu-id="2babc-148">Canal nommé</span><span class="sxs-lookup"><span data-stu-id="2babc-148">Named Pipe</span></span>
> -   <span data-ttu-id="2babc-149">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2babc-149">Path</span></span>

 

<span data-ttu-id="2babc-150">**Binding**: demande d’inclusion d’une **colonne** particulière dans un **ensemble de lignes** retourné.</span><span class="sxs-lookup"><span data-stu-id="2babc-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="2babc-151">La **liaison** spécifie une propriété à inclure dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="2babc-152">**Bookmark**: marqueur qui identifie de façon unique une ligne dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="2babc-153">**Catalogue**: unité de niveau le plus élevé de l’organisation dans le service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="2babc-154">Il représente un ensemble de documents indexés par rapport auxquels les requêtes peuvent être exécutées à l’aide du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="2babc-155">**Category**: regroupement hiérarchique de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="2babc-156">Par exemple, un résultat de requête contenant les colonnes auteur et titre peut être classé en fonction de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="2babc-157">Chaque groupe de lignes contenant la même valeur pour l’auteur constitue une catégorie.</span><span class="sxs-lookup"><span data-stu-id="2babc-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="2babc-158">**Chapitre** : plage de **lignes** au sein d’un ensemble de **lignes** .</span><span class="sxs-lookup"><span data-stu-id="2babc-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="2babc-159">**Column**: conteneur pour un seul type d’informations dans une **ligne** .</span><span class="sxs-lookup"><span data-stu-id="2babc-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="2babc-160">Les colonnes sont mappées à des noms de propriété et spécifient les propriétés qui sont utilisées pour les éléments de l' **arborescence** de **commandes** de la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="2babc-161">**Arborescence de commandes**: combinaison des **restrictions** , **catégories** et **ordres de tri** spécifiés pour la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="2babc-162">**Cursor**: entité utilisée comme mécanisme pour travailler avec une **ligne** ou un petit bloc de **lignes** à la fois dans un jeu de données retourné dans un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="2babc-163">Un **curseur** est positionné sur une seule **ligne** dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="2babc-164">Une fois que le **curseur** est positionné sur une ligne, les opérations peuvent être effectuées sur cette **ligne** ou sur un bloc de **lignes** commençant à cette position.</span><span class="sxs-lookup"><span data-stu-id="2babc-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="2babc-165">**Handle**: jeton qui peut être utilisé pour identifier les **curseurs** , les **chapitres** et les **signets** et y accéder.</span><span class="sxs-lookup"><span data-stu-id="2babc-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="2babc-166">**Index**: structure persistante qui contient le texte extrait des fichiers par un service d' **indexation** .</span><span class="sxs-lookup"><span data-stu-id="2babc-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="2babc-167">Cela comprend la liste des mots, qui sont stockés avec le nom de fichier, l’emplacement de mot et les **paramètres régionaux** qui le contiennent.</span><span class="sxs-lookup"><span data-stu-id="2babc-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="2babc-168">**Indexation**: processus d’extraction de texte et de propriétés de fichiers et de stockage des valeurs extraites dans les **index** (pour le texte) et dans le **cache de propriétés** (pour les propriétés).</span><span class="sxs-lookup"><span data-stu-id="2babc-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="2babc-169">**Service d’indexation**: service qui crée des **catalogues** indexés pour le contenu et les propriétés des systèmes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2babc-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="2babc-170">Les applications peuvent rechercher des informations dans les catalogues à partir des fichiers du système de fichiers indexé.</span><span class="sxs-lookup"><span data-stu-id="2babc-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="2babc-171">**Paramètres régionaux**: identificateur, tel que spécifié dans \[ MS-GPSI \] annexe A, qui spécifie les préférences relatives à la langue.</span><span class="sxs-lookup"><span data-stu-id="2babc-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="2babc-172">Ces préférences indiquent comment les dates et les heures doivent être mises en forme, les éléments doivent être triés par ordre alphabétique, les chaînes doivent être comparées, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="2babc-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="2babc-173">**Requête en langage naturel**: requête construite à l’aide de la langue humaine au lieu de la syntaxe de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="2babc-174">**Mot parasite**: mot ignoré par le service d’indexation lorsqu’il est présent dans les **restrictions** spécifiées pour la requête de recherche, car il a peu de valeur discriminatoire.</span><span class="sxs-lookup"><span data-stu-id="2babc-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="2babc-175">Les exemples en anglais incluent « a », « and » et « The ».</span><span class="sxs-lookup"><span data-stu-id="2babc-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="2babc-176">**Cache de propriété**: cache des propriétés de fichier extraites par un **service d’indexation** .</span><span class="sxs-lookup"><span data-stu-id="2babc-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="2babc-177">**Indexation** des propriétés : processus de création d’un **index** de **Propriétés de type valeur** d’un document, notamment l’auteur, l’objet, le type, le nombre de mots, le nombre de pages imprimées et toutes les autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="2babc-178">**Restriction**: ensemble de conditions qu’un fichier doit remplir pour être inclus dans les résultats de recherche retournés par le **service d’indexation** en réponse à une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="2babc-179">Une **restriction** réduit le focus d’une requête de recherche, limitant ainsi les fichiers que le **service d’indexation** inclura dans les résultats de la recherche à ceux qui répondent aux conditions.</span><span class="sxs-lookup"><span data-stu-id="2babc-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="2babc-180">**Row**: collection de **colonnes** contenant les valeurs de propriété qui décrivent un fichier unique à partir de l’ensemble de fichiers correspondant aux **restrictions** spécifiées dans la requête de recherche envoyée au **service d’indexation** .</span><span class="sxs-lookup"><span data-stu-id="2babc-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="2babc-181">**Rowset**: ensemble de **lignes** renvoyées dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="2babc-182">**Ordre de tri**: ensemble de règles dans une requête de recherche qui définit l’ordre des lignes dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="2babc-183">Chaque règle se compose d’une propriété (nom, taille, etc.) et d’une direction pour le tri (croissant ou décroissant).</span><span class="sxs-lookup"><span data-stu-id="2babc-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="2babc-184">Plusieurs règles sont appliquées séquentiellement</span><span class="sxs-lookup"><span data-stu-id="2babc-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="2babc-185">**Propriété Text-type**: propriété qui décrit le contenu d’un document et dont le texte n’est pas mis en forme et qui est associé à son nom.</span><span class="sxs-lookup"><span data-stu-id="2babc-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="2babc-186">**Propriété de type valeur**: propriété qui décrit un attribut unique d’un document entier.</span><span class="sxs-lookup"><span data-stu-id="2babc-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="2babc-187">Une propriété de type valeur a un ID de type de données et une valeur de ce type de données associé à son nom.</span><span class="sxs-lookup"><span data-stu-id="2babc-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="2babc-188">**Racine virtuelle**: autre chemin d’accès à un dossier.</span><span class="sxs-lookup"><span data-stu-id="2babc-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="2babc-189">Un dossier physique peut avoir zéro ou plusieurs racines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="2babc-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="2babc-190">Les chemins d’accès commençant par une racine virtuelle sont appelés chemins d’accès virtuels.</span><span class="sxs-lookup"><span data-stu-id="2babc-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="2babc-191">Par exemple,/Server/vanityroot peut être une racine virtuelle de C : \\ IIS \\ Web \\ dossier1.</span><span class="sxs-lookup"><span data-stu-id="2babc-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="2babc-192">Ensuite, le fichier C : \\ IIS \\ web \\ dossier1 \\default.htm présenterait le chemin d’accès virtuel/Server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="2babc-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="2babc-193">**Peut**, doit, ne doit pas, ne doit pas : ces termes (en majuscules) sont utilisés comme décrit dans \[ rfc2119 \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="2babc-194">Toutes les instructions de comportement facultatif utilisent PEUT, DOIT ou NE DOIT PAS.</span><span class="sxs-lookup"><span data-stu-id="2babc-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="2babc-195">1.2 Références</span><span class="sxs-lookup"><span data-stu-id="2babc-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="2babc-196">1.2.1 Références normatives</span><span class="sxs-lookup"><span data-stu-id="2babc-196">1.2.1 Normative References</span></span>

<span data-ttu-id="2babc-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, « Standard for Binary Floating-Point arithmétique », IEEE 754-1985, octobre 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="2babc-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="2babc-198">\[MS-DCOM \] Microsoft Corporation, « protocoles distants de modèle objet de composant distribué », juin 2006.</span><span class="sxs-lookup"><span data-stu-id="2babc-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="2babc-199">\[MS-GPSI \] Microsoft Corporation, « Extension installation des logiciels de la stratégie de groupe », juin 2006.</span><span class="sxs-lookup"><span data-stu-id="2babc-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="2babc-200">\[MS-SMB \] Microsoft Corporation, « protocole et extensions Microsoft Server Message Block (SMB) », mai 2006.</span><span class="sxs-lookup"><span data-stu-id="2babc-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="2babc-201">\[MS-SYS \] Microsoft Corporation, « System Overview v4 », juillet 2006.</span><span class="sxs-lookup"><span data-stu-id="2babc-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="2babc-202">\[SALTON \] Salton, G., "traitement automatique du texte : analyse de la transformation et récupération des informations par l’ordinateur", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="2babc-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="2babc-203">\[UNICODE \] consortium Unicode, « la norme Unicode, Version 2,0 », 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="2babc-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="2babc-204">1.2.2 Références informatives</span><span class="sxs-lookup"><span data-stu-id="2babc-204">1.2.2 Informative References</span></span>

<span data-ttu-id="2babc-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="2babc-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="2babc-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valeurs, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="2babc-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="2babc-207">Vue d’ensemble du protocole 1,3 (synopsis)</span><span class="sxs-lookup"><span data-stu-id="2babc-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="2babc-208">Un **service d’indexation** de contenu permet d’organiser efficacement les fonctionnalités extraites d’une collection de documents.</span><span class="sxs-lookup"><span data-stu-id="2babc-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="2babc-209">Le protocole CISP (Content Indexing Service Protocol) permet à un client de communiquer avec un serveur hébergeant un service d’indexation pour émettre des requêtes et permettre à un administrateur de gérer le serveur d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="2babc-210">Lors du traitement de fichiers, un service d’indexation analyse un ensemble de documents et réorganise leur contenu de telle sorte que les **Propriétés** de ces documents peuvent être retournées efficacement en réponse aux requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="2babc-211">Une collection de documents qui peuvent être interrogés comprend un **catalogue** .</span><span class="sxs-lookup"><span data-stu-id="2babc-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="2babc-212">Un catalogue peut contenir un **index** (pour une référence rapide à du texte) et un **cache de propriétés** (pour une récupération rapide des valeurs de propriété).</span><span class="sxs-lookup"><span data-stu-id="2babc-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="2babc-213">Conceptuellement, un catalogue se compose d’une « table » logique de propriétés avec le texte ou la valeur et les paramètres régionaux correspondants stockés dans les **colonnes** de la table.</span><span class="sxs-lookup"><span data-stu-id="2babc-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="2babc-214">Chaque « ligne » de la table correspond à un document distinct dans l’étendue du catalogue et chaque « colonne » de la table correspond à une propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="2babc-215">Les tâches spécifiques effectuées par CISP sont regroupées en deux zones fonctionnelles :</span><span class="sxs-lookup"><span data-stu-id="2babc-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="2babc-216">Administration à distance des catalogues de service d’indexation,</span><span class="sxs-lookup"><span data-stu-id="2babc-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="2babc-217">Interrogation à distance des catalogues de service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="2babc-218">1.3.1 tâches d’administration à distance</span><span class="sxs-lookup"><span data-stu-id="2babc-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="2babc-219">CISP active les tâches de gestion du catalogue du service d’indexation suivantes à partir d’un client :</span><span class="sxs-lookup"><span data-stu-id="2babc-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="2babc-220">Interrogez l’état actuel d’un catalogue du service d’indexation sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="2babc-221">Mettre à jour l’état d’un catalogue de services d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="2babc-222">Lancez le processus d’indexation pour un ensemble de fichiers particulier.</span><span class="sxs-lookup"><span data-stu-id="2babc-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="2babc-223">Initiez l’optimisation d’un index afin d’améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="2babc-224">Toutes les tâches d’administration à distance suivent un modèle de requête/réponse simple.</span><span class="sxs-lookup"><span data-stu-id="2babc-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="2babc-225">Aucun État n’est conservé sur le client pour tout appel d’administration et les appels administratifs peuvent être effectués dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="2babc-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="2babc-226">1.3.2 interrogation à distance</span><span class="sxs-lookup"><span data-stu-id="2babc-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="2babc-227">CISP permet aux clients d’effectuer des requêtes de recherche sur un serveur distant qui héberge un service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="2babc-228">L’envoi d’une requête de recherche est un processus à plusieurs étapes initié par le client.</span><span class="sxs-lookup"><span data-stu-id="2babc-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="2babc-229">La procédure comporte trois étapes :</span><span class="sxs-lookup"><span data-stu-id="2babc-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="2babc-230">Le client demande une connexion à un serveur qui héberge un service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="2babc-231">Le client envoie les paramètres pour la requête de recherche, notamment :</span><span class="sxs-lookup"><span data-stu-id="2babc-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="2babc-232">**Restrictions** permettant de spécifier les documents à inclure et/ou à exclure des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="2babc-233">Ordre dans lequel les résultats de la recherche doivent être retournés.</span><span class="sxs-lookup"><span data-stu-id="2babc-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="2babc-234">Colonnes à retourner dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="2babc-235">Nombre maximal de **lignes** qui doivent être retournées pour la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="2babc-236">Durée maximale d’exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="2babc-237">Une fois que le serveur a accepté la demande de lancement de la requête du client, le client peut demander des informations d’État sur la requête, mais cette étape n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2babc-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="2babc-238">Le client spécifie ensuite les propriétés que le serveur doit inclure dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="2babc-239">Le client demande un jeu de résultats sur le serveur, et le serveur répond en envoyant au client les valeurs de propriété des fichiers qui ont été inclus dans les résultats pour la requête de recherche du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="2babc-240">Si la valeur d’une propriété est trop grande pour tenir dans une seule mémoire tampon de réponse, le serveur n’envoie pas la propriété, mais définit plutôt l’état de la propriété sur différé.</span><span class="sxs-lookup"><span data-stu-id="2babc-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="2babc-241">Le client demande ensuite la valeur de propriété séparément à l’aide d’une série de demandes pour les segments successifs de la valeur, puis reprend la demande d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="2babc-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="2babc-242">Une fois que le client a terminé la requête de recherche et n’a plus besoin de résultats supplémentaires, le client contacte le serveur pour libérer la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="2babc-243">Une fois la requête lancée par le serveur, le client peut envoyer une demande de déconnexion du serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="2babc-244">La connexion est ensuite fermée.</span><span class="sxs-lookup"><span data-stu-id="2babc-244">The connection is then closed.</span></span> <span data-ttu-id="2babc-245">Le client peut également émettre une autre requête et répéter la séquence à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="2babc-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="2babc-246">Comportement de Windows : ce protocole est implémenté sur Windows 2000, Windows XP, Windows Server 2003 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2babc-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="2babc-247">1.4 Relation aux autres protocoles</span><span class="sxs-lookup"><span data-stu-id="2babc-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="2babc-248">Le CISP s’appuie sur le \[ protocole SMB MS-SMB \] pour le transport des messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="2babc-249">Aucun autre protocole ne dépend directement du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="2babc-250">*Comportement de Windows : les applications interagissent généralement avec un wrapper d’interface OLE DB \[ MSDN-OLEDB \] (par exemple, un client de protocole) et pas directement avec le protocole.*</span><span class="sxs-lookup"><span data-stu-id="2babc-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="2babc-251">1,5 conditions préalables et conditions préalables</span><span class="sxs-lookup"><span data-stu-id="2babc-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="2babc-252">Il est supposé que le client a obtenu le nom du serveur et un nom de catalogue avant l’appel de ce protocole.</span><span class="sxs-lookup"><span data-stu-id="2babc-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="2babc-253">Le mode de fonctionnement d’un client est en dehors de la portée de cette spécification.</span><span class="sxs-lookup"><span data-stu-id="2babc-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="2babc-254">Il est également supposé que le client et le serveur ont une association de sécurité utilisable avec les canaux nommés \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="2babc-255">1.6 Instruction d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="2babc-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="2babc-256">CISP est conçu pour l’interrogation et la gestion des catalogues sur un serveur distant à partir d’un client.</span><span class="sxs-lookup"><span data-stu-id="2babc-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="2babc-257">CISP est déconseillé sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2babc-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="2babc-258">1.7 Contrôle de version et négociation de capacité</span><span class="sxs-lookup"><span data-stu-id="2babc-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="2babc-259">Ce protocole n’a pas de mécanisme de contrôle de version ou de négociation de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2babc-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="2babc-260">1.8 Champs extensibles de fournisseur</span><span class="sxs-lookup"><span data-stu-id="2babc-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="2babc-261">Ce protocole utilise des HRESULT qui sont extensibles par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2babc-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="2babc-262">Les fournisseurs sont libres de choisir leurs propres valeurs pour ce champ, tant que le bit C (0x20000000) est défini comme indiqué dans la section 4.1.1 de \[ ms-sys \] , indiquant qu’il s’agit d’un code client.</span><span class="sxs-lookup"><span data-stu-id="2babc-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="2babc-263">Ce protocole utilise également les valeurs NTSTATUS extraites de l’espace de nombre NTSTATUS défini dans \[ ms-sys \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="2babc-264">Les fournisseurs doivent réutiliser ces valeurs avec leur signification indiquée.</span><span class="sxs-lookup"><span data-stu-id="2babc-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="2babc-265">Le choix d’une autre valeur exécute le risque d’une collision dans le futur.</span><span class="sxs-lookup"><span data-stu-id="2babc-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="2babc-266">*Comportement de Windows : Windows utilise uniquement les valeurs spécifiées dans la section 4.1.3 de \[ ms-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="2babc-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="2babc-267">ID de propriété 1.8.1</span><span class="sxs-lookup"><span data-stu-id="2babc-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="2babc-268">Les propriétés sont représentées par des ID connus sous le nom d’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="2babc-269">Chaque propriété doit avoir un identificateur global unique.</span><span class="sxs-lookup"><span data-stu-id="2babc-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="2babc-270">Cet identificateur se compose d’un **GUID** qui représente une collection de propriétés appelée un jeu de propriétés, plus une chaîne ou un entier 32 bits pour identifier la propriété dans le jeu.</span><span class="sxs-lookup"><span data-stu-id="2babc-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="2babc-271">Si la forme entière de ID est utilisée, les valeurs 0x00000000, 0xFFFFFFFF et 0xFFFFFFFE sont considérées comme non valides.</span><span class="sxs-lookup"><span data-stu-id="2babc-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="2babc-272">Les fournisseurs peuvent garantir que leurs propriétés sont définies de manière unique en les plaçant dans un jeu de propriétés défini par leur propre GUID.</span><span class="sxs-lookup"><span data-stu-id="2babc-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="2babc-273">1.9 Affectations de normes</span><span class="sxs-lookup"><span data-stu-id="2babc-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="2babc-274">Ce protocole n’a aucune attribution de normes, mais uniquement les affectations privées effectuées par Microsoft à l’aide de procédures d’allocation spécifiées dans d’autres protocoles.</span><span class="sxs-lookup"><span data-stu-id="2babc-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="2babc-275">Microsoft a alloué ce protocole à un canal nommé comme spécifié dans \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="2babc-276">L’attribution est :</span><span class="sxs-lookup"><span data-stu-id="2babc-276">The assignment is:</span></span>



| <span data-ttu-id="2babc-277">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2babc-277">Parameter</span></span> | <span data-ttu-id="2babc-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-278">Value</span></span>             | <span data-ttu-id="2babc-279">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2babc-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="2babc-280">Nom du canal</span><span class="sxs-lookup"><span data-stu-id="2babc-280">Pipe name</span></span> | <span data-ttu-id="2babc-281">\\canal d' \\ intégration de \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="2babc-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="2babc-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="2babc-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="2babc-283">2 Messages</span><span class="sxs-lookup"><span data-stu-id="2babc-283">2 Messages</span></span>

-   [<span data-ttu-id="2babc-284">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="2babc-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="2babc-285">2.2 Syntaxe de message</span><span class="sxs-lookup"><span data-stu-id="2babc-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="2babc-286">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="2babc-286">2.1 Transport</span></span>

<span data-ttu-id="2babc-287">Tous les messages doivent être transportés à l’aide d’un canal nommé, tel que spécifié dans \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="2babc-288">Le nom de canal suivant est utilisé :</span><span class="sxs-lookup"><span data-stu-id="2babc-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="2babc-289">\\canal d' \\ intégration de \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="2babc-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="2babc-290">Ce protocole utilise le protocole de canal nommé SMB sous-jacent pour récupérer l’identité de l’appelant qui a établi la connexion comme indiqué dans la section 2.2.8 de \[ MS-SMB \] ; le client doit définir l’identification de sécurité \_ en tant que ImpersonationLevel dans la demande pour ouvrir le canal nommé.</span><span class="sxs-lookup"><span data-stu-id="2babc-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="2babc-291">2.2 Syntaxe de message</span><span class="sxs-lookup"><span data-stu-id="2babc-291">2.2 Message Syntax</span></span>

<span data-ttu-id="2babc-292">Plusieurs structures et messages dans les sections suivantes font référence aux descripteurs de chapitres ou de signets.</span><span class="sxs-lookup"><span data-stu-id="2babc-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="2babc-293">Un descripteur est une structure opaque de 32 bits qui identifie de façon unique un chapitre ou un signet.</span><span class="sxs-lookup"><span data-stu-id="2babc-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="2babc-294">En règle générale, les applications clientes reçoivent des valeurs de handle via des appels de méthode ; Toutefois, il existe plusieurs valeurs connues qui n’ont pas besoin d’être obtenues à partir d’un serveur, ce qui signifie qu’elles sont spécifiées dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="2babc-295">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-295">Value</span></span>                         | <span data-ttu-id="2babc-296">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-297">DB \_ null \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="2babc-298">Descripteur de chapitre de l’ensemble de lignes non chapitre, contenant tous les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="2babc-299">DBBMK \_ premier 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="2babc-300">Handle de signet vers un signet qui identifie la première ligne dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="2babc-301">DBBMK \_ dernier 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="2babc-302">Handle de signet vers un signet qui identifie la dernière ligne de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="2babc-303">2.2.1 structures</span><span class="sxs-lookup"><span data-stu-id="2babc-303">2.2.1 Structures</span></span>

<span data-ttu-id="2babc-304">Cette section détaille les structures de données qui sont définies et utilisées par CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="2babc-305">Tous les entiers signés à 2, 4 et 8 octets et non signés dans les structures suivantes doivent être transférés dans l’ordre d’octet avec primauté des octets de poids faible (Little-endian).</span><span class="sxs-lookup"><span data-stu-id="2babc-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="2babc-306">Le tableau suivant récapitule les structures de données définies dans cette section.</span><span class="sxs-lookup"><span data-stu-id="2babc-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="2babc-307">Structure</span><span class="sxs-lookup"><span data-stu-id="2babc-307">Structure</span></span>                    | <span data-ttu-id="2babc-308">Description</span><span class="sxs-lookup"><span data-stu-id="2babc-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="2babc-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="2babc-310">Contient la valeur sur laquelle effectuer une opération de correspondance pour une propriété spécifiée dans une structure CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="2babc-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="2babc-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="2babc-312">Contient un tableau multidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="2babc-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="2babc-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="2babc-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="2babc-314">Représente les limites d’une dimension d’un tableau spécifié dans une structure SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="2babc-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="2babc-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-315">CFullPropSpec</span></span>                | <span data-ttu-id="2babc-316">Contient une spécification de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="2babc-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-317">CContentRestriction</span></span>          | <span data-ttu-id="2babc-318">Contient une chaîne à faire correspondre pour une valeur de propriété dans le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="2babc-319">CKey</span><span class="sxs-lookup"><span data-stu-id="2babc-319">CKey</span></span>                         | <span data-ttu-id="2babc-320">Contient une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="2babc-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="2babc-322">Contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="2babc-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="2babc-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="2babc-324">Contient une correspondance de requête en langage naturel pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="2babc-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-325">CNodeRestriction</span></span>             | <span data-ttu-id="2babc-326">Contient un tableau de nœuds d’arborescence de commandes spécifiant les restrictions pour une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="2babc-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-327">COccRestriction</span></span>              | <span data-ttu-id="2babc-328">Contient l’emplacement d’un mot dans une expression.</span><span class="sxs-lookup"><span data-stu-id="2babc-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="2babc-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-329">CPropertyRestriction</span></span>         | <span data-ttu-id="2babc-330">Contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="2babc-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="2babc-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-331">CRangeRestriction</span></span>            | <span data-ttu-id="2babc-332">Contient une restriction sur une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="2babc-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="2babc-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-333">CScopeRestriction</span></span>            | <span data-ttu-id="2babc-334">Contient une restriction sur les fichiers à rechercher.</span><span class="sxs-lookup"><span data-stu-id="2babc-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="2babc-335">CSort</span><span class="sxs-lookup"><span data-stu-id="2babc-335">CSort</span></span>                        | <span data-ttu-id="2babc-336">Identifie une colonne à trier.</span><span class="sxs-lookup"><span data-stu-id="2babc-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="2babc-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-337">CSynRestriction</span></span>              | <span data-ttu-id="2babc-338">Contient un mot ou ses synonymes pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="2babc-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-339">CVectorRestriction</span></span>           | <span data-ttu-id="2babc-340">Contient une opération pondérée sur un nœud d’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="2babc-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="2babc-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-341">CWordRestriction</span></span>             | <span data-ttu-id="2babc-342">Contient un mot pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="2babc-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-343">CRestriction</span></span>                 | <span data-ttu-id="2babc-344">Contient un nœud d’une arborescence de commandes de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="2babc-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="2babc-345">CColumnSet</span></span>                   | <span data-ttu-id="2babc-346">Indique le nombre de colonnes à retourner.</span><span class="sxs-lookup"><span data-stu-id="2babc-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="2babc-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="2babc-347">CCategorizationSet</span></span>           | <span data-ttu-id="2babc-348">Contient des informations sur le regroupement d’un ensemble de résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="2babc-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-349">CCategorizationSpec</span></span>          | <span data-ttu-id="2babc-350">Contient une définition des catégories dans lesquelles les résultats de la requête seront catégorisés.</span><span class="sxs-lookup"><span data-stu-id="2babc-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="2babc-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="2babc-351">CDbColId</span></span>                     | <span data-ttu-id="2babc-352">Contient une colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="2babc-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="2babc-353">CDbProp</span></span>                      | <span data-ttu-id="2babc-354">Contient une propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="2babc-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="2babc-355">CDbPropSet</span></span>                   | <span data-ttu-id="2babc-356">Contient un ensemble de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="2babc-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="2babc-357">CPidMapper</span></span>                   | <span data-ttu-id="2babc-358">Contient un tableau d’ID de propriété spécifiant les propriétés à retourner dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="2babc-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="2babc-359">CRowSeekAt</span></span>                   | <span data-ttu-id="2babc-360">Contient le décalage à partir duquel récupérer des lignes dans un message CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="2babc-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="2babc-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="2babc-362">Identifie le point à partir duquel commencer la récupération d’un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="2babc-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="2babc-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="2babc-364">Identifie les signets à partir desquels récupérer des lignes pour un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="2babc-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="2babc-365">CRowSeekNext</span></span>                 | <span data-ttu-id="2babc-366">Contient le nombre de lignes à ignorer dans un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="2babc-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="2babc-367">CRowsetProperties</span></span>            | <span data-ttu-id="2babc-368">Contient les informations de configuration d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="2babc-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="2babc-369">CSortSet</span></span>                     | <span data-ttu-id="2babc-370">Contient l’ordre de tri d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="2babc-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="2babc-371">CTableColumn</span></span>                 | <span data-ttu-id="2babc-372">Contient une colonne pour le message CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="2babc-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="2babc-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="2babc-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="2babc-374">Contient une valeur sérialisée.</span><span class="sxs-lookup"><span data-stu-id="2babc-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="2babc-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="2babc-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="2babc-376">La structure CBaseStorageVariant contient la valeur sur laquelle effectuer une opération de correspondance pour une propriété spécifiée dans la structure CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="2babc-377">0</span><span class="sxs-lookup"><span data-stu-id="2babc-377">0</span></span>

<span data-ttu-id="2babc-378">1</span><span class="sxs-lookup"><span data-stu-id="2babc-378">1</span></span>

<span data-ttu-id="2babc-379">2</span><span class="sxs-lookup"><span data-stu-id="2babc-379">2</span></span>

<span data-ttu-id="2babc-380">3</span><span class="sxs-lookup"><span data-stu-id="2babc-380">3</span></span>

<span data-ttu-id="2babc-381">4</span><span class="sxs-lookup"><span data-stu-id="2babc-381">4</span></span>

<span data-ttu-id="2babc-382">5</span><span class="sxs-lookup"><span data-stu-id="2babc-382">5</span></span>

<span data-ttu-id="2babc-383">6</span><span class="sxs-lookup"><span data-stu-id="2babc-383">6</span></span>

<span data-ttu-id="2babc-384">7</span><span class="sxs-lookup"><span data-stu-id="2babc-384">7</span></span>

<span data-ttu-id="2babc-385">8</span><span class="sxs-lookup"><span data-stu-id="2babc-385">8</span></span>

<span data-ttu-id="2babc-386">9</span><span class="sxs-lookup"><span data-stu-id="2babc-386">9</span></span>

<span data-ttu-id="2babc-387">1</span><span class="sxs-lookup"><span data-stu-id="2babc-387">1</span></span><br/> <span data-ttu-id="2babc-388">0</span><span class="sxs-lookup"><span data-stu-id="2babc-388">0</span></span><br/>

<span data-ttu-id="2babc-389">1</span><span class="sxs-lookup"><span data-stu-id="2babc-389">1</span></span>

<span data-ttu-id="2babc-390">2</span><span class="sxs-lookup"><span data-stu-id="2babc-390">2</span></span>

<span data-ttu-id="2babc-391">3</span><span class="sxs-lookup"><span data-stu-id="2babc-391">3</span></span>

<span data-ttu-id="2babc-392">4</span><span class="sxs-lookup"><span data-stu-id="2babc-392">4</span></span>

<span data-ttu-id="2babc-393">5</span><span class="sxs-lookup"><span data-stu-id="2babc-393">5</span></span>

<span data-ttu-id="2babc-394">6</span><span class="sxs-lookup"><span data-stu-id="2babc-394">6</span></span>

<span data-ttu-id="2babc-395">7</span><span class="sxs-lookup"><span data-stu-id="2babc-395">7</span></span>

<span data-ttu-id="2babc-396">8</span><span class="sxs-lookup"><span data-stu-id="2babc-396">8</span></span>

<span data-ttu-id="2babc-397">9</span><span class="sxs-lookup"><span data-stu-id="2babc-397">9</span></span>

<span data-ttu-id="2babc-398">2</span><span class="sxs-lookup"><span data-stu-id="2babc-398">2</span></span><br/> <span data-ttu-id="2babc-399">0</span><span class="sxs-lookup"><span data-stu-id="2babc-399">0</span></span><br/>

<span data-ttu-id="2babc-400">1</span><span class="sxs-lookup"><span data-stu-id="2babc-400">1</span></span>

<span data-ttu-id="2babc-401">2</span><span class="sxs-lookup"><span data-stu-id="2babc-401">2</span></span>

<span data-ttu-id="2babc-402">3</span><span class="sxs-lookup"><span data-stu-id="2babc-402">3</span></span>

<span data-ttu-id="2babc-403">4</span><span class="sxs-lookup"><span data-stu-id="2babc-403">4</span></span>

<span data-ttu-id="2babc-404">5</span><span class="sxs-lookup"><span data-stu-id="2babc-404">5</span></span>

<span data-ttu-id="2babc-405">6</span><span class="sxs-lookup"><span data-stu-id="2babc-405">6</span></span>

<span data-ttu-id="2babc-406">7</span><span class="sxs-lookup"><span data-stu-id="2babc-406">7</span></span>

<span data-ttu-id="2babc-407">8</span><span class="sxs-lookup"><span data-stu-id="2babc-407">8</span></span>

<span data-ttu-id="2babc-408">9</span><span class="sxs-lookup"><span data-stu-id="2babc-408">9</span></span>

<span data-ttu-id="2babc-409">3</span><span class="sxs-lookup"><span data-stu-id="2babc-409">3</span></span><br/> <span data-ttu-id="2babc-410">0</span><span class="sxs-lookup"><span data-stu-id="2babc-410">0</span></span><br/>

<span data-ttu-id="2babc-411">1</span><span class="sxs-lookup"><span data-stu-id="2babc-411">1</span></span>

<span data-ttu-id="2babc-412">vType</span><span class="sxs-lookup"><span data-stu-id="2babc-412">vType</span></span>

<span data-ttu-id="2babc-413">vData1</span><span class="sxs-lookup"><span data-stu-id="2babc-413">vData1</span></span>

<span data-ttu-id="2babc-414">vData2</span><span class="sxs-lookup"><span data-stu-id="2babc-414">vData2</span></span>

<span data-ttu-id="2babc-415">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-415">vValue (variable)</span></span>



 

<span data-ttu-id="2babc-416">**vType**: indicateur de type indiquant le type de vValue.</span><span class="sxs-lookup"><span data-stu-id="2babc-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="2babc-417">Il doit s’agir de l’une des valeurs VARENUM spécifiées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2babc-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="2babc-418">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-418">Value</span></span>                 | <span data-ttu-id="2babc-419">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-420">VT \_ vide (0x0000)</span><span class="sxs-lookup"><span data-stu-id="2babc-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="2babc-421">vValue n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="2babc-422">VT \_ null (0x0001)</span><span class="sxs-lookup"><span data-stu-id="2babc-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="2babc-423">vValue n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="2babc-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="2babc-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="2babc-425">Entier signé sur 1 octet.</span><span class="sxs-lookup"><span data-stu-id="2babc-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="2babc-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="2babc-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="2babc-427">Entier non signé sur 1 octet.</span><span class="sxs-lookup"><span data-stu-id="2babc-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="2babc-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="2babc-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="2babc-429">Entier signé sur 2 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="2babc-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="2babc-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="2babc-431">Entier non signé sur 2 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="2babc-432">VT \_ bool (0x000B)</span><span class="sxs-lookup"><span data-stu-id="2babc-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="2babc-433">Valeur booléenne ; entier sur 2 octets qui contient 0x0000 (FALSe) ou 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="2babc-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="2babc-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="2babc-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="2babc-435">Entier signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="2babc-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="2babc-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="2babc-437">Entier non signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="2babc-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="2babc-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="2babc-439">Nombre à virgule flottante IEEE 32 bits, tel que défini dans \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="2babc-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="2babc-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="2babc-441">Entier signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="2babc-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="2babc-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="2babc-443">Entier non signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="2babc-444">\_Erreur VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="2babc-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="2babc-445">Entier non signé de 4 octets contenant un HRESULT, tel que spécifié dans \[ ms-sys \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="2babc-446">0x0014 VT (en anglais \_ )</span><span class="sxs-lookup"><span data-stu-id="2babc-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="2babc-447">Entier signé de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="2babc-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="2babc-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="2babc-449">Entier non signé sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="2babc-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="2babc-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="2babc-451">Nombre à virgule flottante IEEE 64 bits tel que défini dans \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="2babc-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="2babc-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="2babc-453">Entier de complément à deux octets (mis à l’échelle par 10 000).</span><span class="sxs-lookup"><span data-stu-id="2babc-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="2babc-454">\_Date VT (0x0007)</span><span class="sxs-lookup"><span data-stu-id="2babc-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="2babc-455">Nombre à virgule flottante 64 bits représentant le nombre de jours écoulés depuis 00:00:00 le 31 décembre 1899 (temps universel coordonné).</span><span class="sxs-lookup"><span data-stu-id="2babc-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="2babc-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="2babc-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="2babc-457">Entier 64 bits représentant le nombre d’intervalles de 100 nanosecondes depuis 00:00:00 le 1er janvier 1601 (heure universelle coordonnée).</span><span class="sxs-lookup"><span data-stu-id="2babc-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="2babc-458">VT \_ décimale (0x000E)</span><span class="sxs-lookup"><span data-stu-id="2babc-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="2babc-459">Structure DÉCIMALe telle que spécifiée dans la section 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="2babc-460">\_CLSID VT (0x0048)</span><span class="sxs-lookup"><span data-stu-id="2babc-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="2babc-461">Valeur binaire de 16 octets contenant un GUID.</span><span class="sxs-lookup"><span data-stu-id="2babc-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="2babc-462">\_Objet BLOB VT (0x0041)</span><span class="sxs-lookup"><span data-stu-id="2babc-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="2babc-463">Nombre entier non signé de 4 octets d’octets dans l’objet BLOB, suivi de beaucoup d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="2babc-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="2babc-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="2babc-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="2babc-465">Nombre entier d’octets non signés sur 4 octets dans la chaîne, suivi d’une chaîne, comme indiqué ci-dessous sous vValue.</span><span class="sxs-lookup"><span data-stu-id="2babc-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="2babc-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="2babc-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="2babc-467">Chaîne ANSI terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="2babc-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="2babc-468">VT \_ LPWStr (0x001F)</span><span class="sxs-lookup"><span data-stu-id="2babc-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="2babc-469">Chaîne Unicode Unicode terminée par le caractère null \[ \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="2babc-470">\_Variante VT (0x000c)</span><span class="sxs-lookup"><span data-stu-id="2babc-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="2babc-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="2babc-471">CBaseStorageVariant.</span></span> <span data-ttu-id="2babc-472">DOIT être combiné avec un modificateur de type de \_ tableau VT ou de \_ vecteur VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="2babc-473">Le tableau suivant spécifie les modificateurs de type pour vType.</span><span class="sxs-lookup"><span data-stu-id="2babc-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="2babc-474">Les modificateurs de type peuvent être binaires avec vType, pour modifier la signification de vValue afin d’indiquer qu’il s’agit de l’un des deux types de tableau possibles.</span><span class="sxs-lookup"><span data-stu-id="2babc-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="2babc-475">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-475">Value</span></span>               | <span data-ttu-id="2babc-476">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-477">\_Vecteur VT (0x1000)</span><span class="sxs-lookup"><span data-stu-id="2babc-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="2babc-478">Si l’indicateur de type est combiné avec \_ un vecteur VT à l’aide d’un opérateur or, vValue est un tableau compté des valeurs du type indiqué.</span><span class="sxs-lookup"><span data-stu-id="2babc-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="2babc-479">Pour plus d’informations, consultez la section 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="2babc-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="2babc-480">Ce modificateur de type ne doit pas être combiné avec les types suivants : VT \_ int, VT \_ uint, VT \_ Decimal, VT \_ BLOB \_ , \_ objet BLOB VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="2babc-481">\_Tableau VT (0x2000)</span><span class="sxs-lookup"><span data-stu-id="2babc-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="2babc-482">Si l’indicateur de type est combiné avec \_ un tableau VT par un opérateur or, la valeur est un SafeArray (comme spécifié dans la section 2.2.1.1.1.3) qui contient les valeurs du type indiqué.</span><span class="sxs-lookup"><span data-stu-id="2babc-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="2babc-483">Ce modificateur de type ne doit pas être combiné avec les types suivants : VT \_ I8, VT \_ UI8, VT \_ fileTime, VT \_ CLSID, \_ objet BLOB VT, \_ objet BLOB VT \_ , VT \_ LPSTR, VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="2babc-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="2babc-484">**vData1**: lorsque vType est de type VT \_ Decimal, la valeur de ce champ est spécifiée en tant que champ Scale dans la section 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="2babc-485">Pour tous les autres vTypes, la valeur doit être égale à 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="2babc-486">**vData2**: lorsque vType est de type VT \_ Decimal, la valeur de ce champ est spécifiée comme champ de signe dans la section 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="2babc-487">Pour tous les autres vTypes, la valeur doit être égale à 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="2babc-488">**vValue**: valeur de l’opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="2babc-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="2babc-489">La syntaxe doit être indiquée dans le champ vType.</span><span class="sxs-lookup"><span data-stu-id="2babc-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="2babc-490">Le tableau suivant récapitule les tailles du champ vValue, selon le champ vType pour les types de données de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="2babc-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="2babc-491">La taille est en octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-491">The size is in bytes.</span></span>



| <span data-ttu-id="2babc-492">vType</span><span class="sxs-lookup"><span data-stu-id="2babc-492">vType</span></span>                                                   | <span data-ttu-id="2babc-493">Taille</span><span class="sxs-lookup"><span data-stu-id="2babc-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="2babc-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="2babc-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="2babc-495">1</span><span class="sxs-lookup"><span data-stu-id="2babc-495">1</span></span>    |
| <span data-ttu-id="2babc-496">VT \_ I2, VT \_ UI2, VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="2babc-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="2babc-497">2</span><span class="sxs-lookup"><span data-stu-id="2babc-497">2</span></span>    |
| <span data-ttu-id="2babc-498">VT \_ i4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, \_ erreur VT</span><span class="sxs-lookup"><span data-stu-id="2babc-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="2babc-499">4</span><span class="sxs-lookup"><span data-stu-id="2babc-499">4</span></span>    |
| <span data-ttu-id="2babc-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ ca, VT \_ date, VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="2babc-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="2babc-501">8</span><span class="sxs-lookup"><span data-stu-id="2babc-501">8</span></span>    |
| <span data-ttu-id="2babc-502">VT \_ décimal, \_ CLSID VT</span><span class="sxs-lookup"><span data-stu-id="2babc-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="2babc-503">16</span><span class="sxs-lookup"><span data-stu-id="2babc-503">16</span></span>   |



 

<span data-ttu-id="2babc-504">Si vType a \_ la valeur BLOB VT, VT \_ BSTR ou VT \_ LPSTR, la structure de vValue est spécifiée dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="2babc-505">0</span><span class="sxs-lookup"><span data-stu-id="2babc-505">0</span></span>

<span data-ttu-id="2babc-506">1</span><span class="sxs-lookup"><span data-stu-id="2babc-506">1</span></span>

<span data-ttu-id="2babc-507">2</span><span class="sxs-lookup"><span data-stu-id="2babc-507">2</span></span>

<span data-ttu-id="2babc-508">3</span><span class="sxs-lookup"><span data-stu-id="2babc-508">3</span></span>

<span data-ttu-id="2babc-509">4</span><span class="sxs-lookup"><span data-stu-id="2babc-509">4</span></span>

<span data-ttu-id="2babc-510">5</span><span class="sxs-lookup"><span data-stu-id="2babc-510">5</span></span>

<span data-ttu-id="2babc-511">6</span><span class="sxs-lookup"><span data-stu-id="2babc-511">6</span></span>

<span data-ttu-id="2babc-512">7</span><span class="sxs-lookup"><span data-stu-id="2babc-512">7</span></span>

<span data-ttu-id="2babc-513">8</span><span class="sxs-lookup"><span data-stu-id="2babc-513">8</span></span>

<span data-ttu-id="2babc-514">9</span><span class="sxs-lookup"><span data-stu-id="2babc-514">9</span></span>

<span data-ttu-id="2babc-515">1</span><span class="sxs-lookup"><span data-stu-id="2babc-515">1</span></span><br/> <span data-ttu-id="2babc-516">0</span><span class="sxs-lookup"><span data-stu-id="2babc-516">0</span></span><br/>

<span data-ttu-id="2babc-517">1</span><span class="sxs-lookup"><span data-stu-id="2babc-517">1</span></span>

<span data-ttu-id="2babc-518">2</span><span class="sxs-lookup"><span data-stu-id="2babc-518">2</span></span>

<span data-ttu-id="2babc-519">3</span><span class="sxs-lookup"><span data-stu-id="2babc-519">3</span></span>

<span data-ttu-id="2babc-520">4</span><span class="sxs-lookup"><span data-stu-id="2babc-520">4</span></span>

<span data-ttu-id="2babc-521">5</span><span class="sxs-lookup"><span data-stu-id="2babc-521">5</span></span>

<span data-ttu-id="2babc-522">6</span><span class="sxs-lookup"><span data-stu-id="2babc-522">6</span></span>

<span data-ttu-id="2babc-523">7</span><span class="sxs-lookup"><span data-stu-id="2babc-523">7</span></span>

<span data-ttu-id="2babc-524">8</span><span class="sxs-lookup"><span data-stu-id="2babc-524">8</span></span>

<span data-ttu-id="2babc-525">9</span><span class="sxs-lookup"><span data-stu-id="2babc-525">9</span></span>

<span data-ttu-id="2babc-526">2</span><span class="sxs-lookup"><span data-stu-id="2babc-526">2</span></span><br/> <span data-ttu-id="2babc-527">0</span><span class="sxs-lookup"><span data-stu-id="2babc-527">0</span></span><br/>

<span data-ttu-id="2babc-528">1</span><span class="sxs-lookup"><span data-stu-id="2babc-528">1</span></span>

<span data-ttu-id="2babc-529">2</span><span class="sxs-lookup"><span data-stu-id="2babc-529">2</span></span>

<span data-ttu-id="2babc-530">3</span><span class="sxs-lookup"><span data-stu-id="2babc-530">3</span></span>

<span data-ttu-id="2babc-531">4</span><span class="sxs-lookup"><span data-stu-id="2babc-531">4</span></span>

<span data-ttu-id="2babc-532">5</span><span class="sxs-lookup"><span data-stu-id="2babc-532">5</span></span>

<span data-ttu-id="2babc-533">6</span><span class="sxs-lookup"><span data-stu-id="2babc-533">6</span></span>

<span data-ttu-id="2babc-534">7</span><span class="sxs-lookup"><span data-stu-id="2babc-534">7</span></span>

<span data-ttu-id="2babc-535">8</span><span class="sxs-lookup"><span data-stu-id="2babc-535">8</span></span>

<span data-ttu-id="2babc-536">9</span><span class="sxs-lookup"><span data-stu-id="2babc-536">9</span></span>

<span data-ttu-id="2babc-537">3</span><span class="sxs-lookup"><span data-stu-id="2babc-537">3</span></span><br/> <span data-ttu-id="2babc-538">0</span><span class="sxs-lookup"><span data-stu-id="2babc-538">0</span></span><br/>

<span data-ttu-id="2babc-539">1</span><span class="sxs-lookup"><span data-stu-id="2babc-539">1</span></span>

<span data-ttu-id="2babc-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="2babc-540">cbSize</span></span>

<span data-ttu-id="2babc-541">blobData (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="2babc-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="2babc-542">**cbSize**: entier 32 bits non signé, indiquant la taille du champ blobData en octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="2babc-543">Si vType est défini sur VT \_ BSTR ou VT \_ LPSTR, cbSize doit avoir la valeur 0x00000000 lorsque la chaîne représentée est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="2babc-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="2babc-544">**blobData**: doit avoir une longueur de cbSize en octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="2babc-545">Pour vType ayant la valeur d' \_ objet BLOB VT, ce champ est opaque Binary BLOB Data.</span><span class="sxs-lookup"><span data-stu-id="2babc-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="2babc-546">Pour vType défini sur VT \_ BSTR, ce champ est un jeu de caractères dans un jeu de caractères OEM sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2babc-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="2babc-547">Le client et le serveur doivent être configurés pour avoir des jeux de caractères interopérables (hors bande du protocole).</span><span class="sxs-lookup"><span data-stu-id="2babc-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="2babc-548">Il n’est pas nécessaire qu’elle se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="2babc-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="2babc-549">Pour vType défini sur VT \_ LPSTR, ce champ est une chaîne de caractères se terminant par un caractère NULL dans un jeu de caractères OEM sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2babc-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="2babc-550">Le client et le serveur doivent être configurés pour avoir des jeux de caractères interopérables (hors bande du protocole).</span><span class="sxs-lookup"><span data-stu-id="2babc-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="2babc-551">Si vType est défini sur VT \_ LPWStr, la structure de vValue est spécifiée dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="2babc-552">0</span><span class="sxs-lookup"><span data-stu-id="2babc-552">0</span></span>

<span data-ttu-id="2babc-553">1</span><span class="sxs-lookup"><span data-stu-id="2babc-553">1</span></span>

<span data-ttu-id="2babc-554">2</span><span class="sxs-lookup"><span data-stu-id="2babc-554">2</span></span>

<span data-ttu-id="2babc-555">3</span><span class="sxs-lookup"><span data-stu-id="2babc-555">3</span></span>

<span data-ttu-id="2babc-556">4</span><span class="sxs-lookup"><span data-stu-id="2babc-556">4</span></span>

<span data-ttu-id="2babc-557">5</span><span class="sxs-lookup"><span data-stu-id="2babc-557">5</span></span>

<span data-ttu-id="2babc-558">6</span><span class="sxs-lookup"><span data-stu-id="2babc-558">6</span></span>

<span data-ttu-id="2babc-559">7</span><span class="sxs-lookup"><span data-stu-id="2babc-559">7</span></span>

<span data-ttu-id="2babc-560">8</span><span class="sxs-lookup"><span data-stu-id="2babc-560">8</span></span>

<span data-ttu-id="2babc-561">9</span><span class="sxs-lookup"><span data-stu-id="2babc-561">9</span></span>

<span data-ttu-id="2babc-562">1</span><span class="sxs-lookup"><span data-stu-id="2babc-562">1</span></span><br/> <span data-ttu-id="2babc-563">0</span><span class="sxs-lookup"><span data-stu-id="2babc-563">0</span></span><br/>

<span data-ttu-id="2babc-564">1</span><span class="sxs-lookup"><span data-stu-id="2babc-564">1</span></span>

<span data-ttu-id="2babc-565">2</span><span class="sxs-lookup"><span data-stu-id="2babc-565">2</span></span>

<span data-ttu-id="2babc-566">3</span><span class="sxs-lookup"><span data-stu-id="2babc-566">3</span></span>

<span data-ttu-id="2babc-567">4</span><span class="sxs-lookup"><span data-stu-id="2babc-567">4</span></span>

<span data-ttu-id="2babc-568">5</span><span class="sxs-lookup"><span data-stu-id="2babc-568">5</span></span>

<span data-ttu-id="2babc-569">6</span><span class="sxs-lookup"><span data-stu-id="2babc-569">6</span></span>

<span data-ttu-id="2babc-570">7</span><span class="sxs-lookup"><span data-stu-id="2babc-570">7</span></span>

<span data-ttu-id="2babc-571">8</span><span class="sxs-lookup"><span data-stu-id="2babc-571">8</span></span>

<span data-ttu-id="2babc-572">9</span><span class="sxs-lookup"><span data-stu-id="2babc-572">9</span></span>

<span data-ttu-id="2babc-573">2</span><span class="sxs-lookup"><span data-stu-id="2babc-573">2</span></span><br/> <span data-ttu-id="2babc-574">0</span><span class="sxs-lookup"><span data-stu-id="2babc-574">0</span></span><br/>

<span data-ttu-id="2babc-575">1</span><span class="sxs-lookup"><span data-stu-id="2babc-575">1</span></span>

<span data-ttu-id="2babc-576">2</span><span class="sxs-lookup"><span data-stu-id="2babc-576">2</span></span>

<span data-ttu-id="2babc-577">3</span><span class="sxs-lookup"><span data-stu-id="2babc-577">3</span></span>

<span data-ttu-id="2babc-578">4</span><span class="sxs-lookup"><span data-stu-id="2babc-578">4</span></span>

<span data-ttu-id="2babc-579">5</span><span class="sxs-lookup"><span data-stu-id="2babc-579">5</span></span>

<span data-ttu-id="2babc-580">6</span><span class="sxs-lookup"><span data-stu-id="2babc-580">6</span></span>

<span data-ttu-id="2babc-581">7</span><span class="sxs-lookup"><span data-stu-id="2babc-581">7</span></span>

<span data-ttu-id="2babc-582">8</span><span class="sxs-lookup"><span data-stu-id="2babc-582">8</span></span>

<span data-ttu-id="2babc-583">9</span><span class="sxs-lookup"><span data-stu-id="2babc-583">9</span></span>

<span data-ttu-id="2babc-584">3</span><span class="sxs-lookup"><span data-stu-id="2babc-584">3</span></span><br/> <span data-ttu-id="2babc-585">0</span><span class="sxs-lookup"><span data-stu-id="2babc-585">0</span></span><br/>

<span data-ttu-id="2babc-586">1</span><span class="sxs-lookup"><span data-stu-id="2babc-586">1</span></span>

<span data-ttu-id="2babc-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="2babc-587">ccLen</span></span>

<span data-ttu-id="2babc-588">String (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="2babc-588">string (variable, optional)</span></span>



 

<span data-ttu-id="2babc-589">**ccLen**: entier non signé 32 bits, indiquant la taille du champ de chaîne en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="2babc-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="2babc-590">DOIT être défini sur 0x00000000 pour une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="2babc-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="2babc-591">**chaîne**: chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="2babc-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="2babc-592">Structures 2.2.1.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="2babc-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="2babc-593">Les structures suivantes sont utilisées dans la structure CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="2babc-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="2babc-594">2.2.1.1.1.1 DÉCIMAL</span><span class="sxs-lookup"><span data-stu-id="2babc-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="2babc-595">Le nombre décimal est utilisé pour représenter une valeur numérique exacte avec une précision fixe et une échelle fixe.</span><span class="sxs-lookup"><span data-stu-id="2babc-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="2babc-596">Quand vType est défini sur VT \_ Decimal (0x0000E), les champs vData1 et vData2 de CBASESTORAGEVARIANT doivent être interprétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="2babc-597">**vData1**: nombre de chiffres à droite de la virgule décimale.</span><span class="sxs-lookup"><span data-stu-id="2babc-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="2babc-598">DOIT être compris entre 0 et 28.</span><span class="sxs-lookup"><span data-stu-id="2babc-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="2babc-599">**vData2**: signe de la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="2babc-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="2babc-600">Défini sur 0x00 si positif, 0x80 si négatif.</span><span class="sxs-lookup"><span data-stu-id="2babc-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="2babc-601">Le format du champ vValue est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-601">The format of the vValue field is:</span></span>



<span data-ttu-id="2babc-602">0</span><span class="sxs-lookup"><span data-stu-id="2babc-602">0</span></span>

<span data-ttu-id="2babc-603">1</span><span class="sxs-lookup"><span data-stu-id="2babc-603">1</span></span>

<span data-ttu-id="2babc-604">2</span><span class="sxs-lookup"><span data-stu-id="2babc-604">2</span></span>

<span data-ttu-id="2babc-605">3</span><span class="sxs-lookup"><span data-stu-id="2babc-605">3</span></span>

<span data-ttu-id="2babc-606">4</span><span class="sxs-lookup"><span data-stu-id="2babc-606">4</span></span>

<span data-ttu-id="2babc-607">5</span><span class="sxs-lookup"><span data-stu-id="2babc-607">5</span></span>

<span data-ttu-id="2babc-608">6</span><span class="sxs-lookup"><span data-stu-id="2babc-608">6</span></span>

<span data-ttu-id="2babc-609">7</span><span class="sxs-lookup"><span data-stu-id="2babc-609">7</span></span>

<span data-ttu-id="2babc-610">8</span><span class="sxs-lookup"><span data-stu-id="2babc-610">8</span></span>

<span data-ttu-id="2babc-611">9</span><span class="sxs-lookup"><span data-stu-id="2babc-611">9</span></span>

<span data-ttu-id="2babc-612">1</span><span class="sxs-lookup"><span data-stu-id="2babc-612">1</span></span><br/> <span data-ttu-id="2babc-613">0</span><span class="sxs-lookup"><span data-stu-id="2babc-613">0</span></span><br/>

<span data-ttu-id="2babc-614">1</span><span class="sxs-lookup"><span data-stu-id="2babc-614">1</span></span>

<span data-ttu-id="2babc-615">2</span><span class="sxs-lookup"><span data-stu-id="2babc-615">2</span></span>

<span data-ttu-id="2babc-616">3</span><span class="sxs-lookup"><span data-stu-id="2babc-616">3</span></span>

<span data-ttu-id="2babc-617">4</span><span class="sxs-lookup"><span data-stu-id="2babc-617">4</span></span>

<span data-ttu-id="2babc-618">5</span><span class="sxs-lookup"><span data-stu-id="2babc-618">5</span></span>

<span data-ttu-id="2babc-619">6</span><span class="sxs-lookup"><span data-stu-id="2babc-619">6</span></span>

<span data-ttu-id="2babc-620">7</span><span class="sxs-lookup"><span data-stu-id="2babc-620">7</span></span>

<span data-ttu-id="2babc-621">8</span><span class="sxs-lookup"><span data-stu-id="2babc-621">8</span></span>

<span data-ttu-id="2babc-622">9</span><span class="sxs-lookup"><span data-stu-id="2babc-622">9</span></span>

<span data-ttu-id="2babc-623">2</span><span class="sxs-lookup"><span data-stu-id="2babc-623">2</span></span><br/> <span data-ttu-id="2babc-624">0</span><span class="sxs-lookup"><span data-stu-id="2babc-624">0</span></span><br/>

<span data-ttu-id="2babc-625">1</span><span class="sxs-lookup"><span data-stu-id="2babc-625">1</span></span>

<span data-ttu-id="2babc-626">2</span><span class="sxs-lookup"><span data-stu-id="2babc-626">2</span></span>

<span data-ttu-id="2babc-627">3</span><span class="sxs-lookup"><span data-stu-id="2babc-627">3</span></span>

<span data-ttu-id="2babc-628">4</span><span class="sxs-lookup"><span data-stu-id="2babc-628">4</span></span>

<span data-ttu-id="2babc-629">5</span><span class="sxs-lookup"><span data-stu-id="2babc-629">5</span></span>

<span data-ttu-id="2babc-630">6</span><span class="sxs-lookup"><span data-stu-id="2babc-630">6</span></span>

<span data-ttu-id="2babc-631">7</span><span class="sxs-lookup"><span data-stu-id="2babc-631">7</span></span>

<span data-ttu-id="2babc-632">8</span><span class="sxs-lookup"><span data-stu-id="2babc-632">8</span></span>

<span data-ttu-id="2babc-633">9</span><span class="sxs-lookup"><span data-stu-id="2babc-633">9</span></span>

<span data-ttu-id="2babc-634">3</span><span class="sxs-lookup"><span data-stu-id="2babc-634">3</span></span><br/> <span data-ttu-id="2babc-635">0</span><span class="sxs-lookup"><span data-stu-id="2babc-635">0</span></span><br/>

<span data-ttu-id="2babc-636">1</span><span class="sxs-lookup"><span data-stu-id="2babc-636">1</span></span>

<span data-ttu-id="2babc-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="2babc-637">Hi32</span></span>

<span data-ttu-id="2babc-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="2babc-638">Lo32</span></span>

<span data-ttu-id="2babc-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="2babc-639">Mid32</span></span>



 

<span data-ttu-id="2babc-640">**Hi32**: 32 bits les plus élevés de l’entier 96 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="2babc-641">**Lo32**: 32 bits de poids faible de l’entier 96 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="2babc-642">**Mid32**: bits 32 au milieu de l’entier 96 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="2babc-643">vecteur VT 2.2.1.1.1.2 \_</span><span class="sxs-lookup"><span data-stu-id="2babc-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="2babc-644">Le \_ vecteur VT est utilisé pour passer des tableaux unidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="2babc-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="2babc-645">0</span><span class="sxs-lookup"><span data-stu-id="2babc-645">0</span></span>

<span data-ttu-id="2babc-646">1</span><span class="sxs-lookup"><span data-stu-id="2babc-646">1</span></span>

<span data-ttu-id="2babc-647">2</span><span class="sxs-lookup"><span data-stu-id="2babc-647">2</span></span>

<span data-ttu-id="2babc-648">3</span><span class="sxs-lookup"><span data-stu-id="2babc-648">3</span></span>

<span data-ttu-id="2babc-649">4</span><span class="sxs-lookup"><span data-stu-id="2babc-649">4</span></span>

<span data-ttu-id="2babc-650">5</span><span class="sxs-lookup"><span data-stu-id="2babc-650">5</span></span>

<span data-ttu-id="2babc-651">6</span><span class="sxs-lookup"><span data-stu-id="2babc-651">6</span></span>

<span data-ttu-id="2babc-652">7</span><span class="sxs-lookup"><span data-stu-id="2babc-652">7</span></span>

<span data-ttu-id="2babc-653">8</span><span class="sxs-lookup"><span data-stu-id="2babc-653">8</span></span>

<span data-ttu-id="2babc-654">9</span><span class="sxs-lookup"><span data-stu-id="2babc-654">9</span></span>

<span data-ttu-id="2babc-655">1</span><span class="sxs-lookup"><span data-stu-id="2babc-655">1</span></span><br/> <span data-ttu-id="2babc-656">0</span><span class="sxs-lookup"><span data-stu-id="2babc-656">0</span></span><br/>

<span data-ttu-id="2babc-657">1</span><span class="sxs-lookup"><span data-stu-id="2babc-657">1</span></span>

<span data-ttu-id="2babc-658">2</span><span class="sxs-lookup"><span data-stu-id="2babc-658">2</span></span>

<span data-ttu-id="2babc-659">3</span><span class="sxs-lookup"><span data-stu-id="2babc-659">3</span></span>

<span data-ttu-id="2babc-660">4</span><span class="sxs-lookup"><span data-stu-id="2babc-660">4</span></span>

<span data-ttu-id="2babc-661">5</span><span class="sxs-lookup"><span data-stu-id="2babc-661">5</span></span>

<span data-ttu-id="2babc-662">6</span><span class="sxs-lookup"><span data-stu-id="2babc-662">6</span></span>

<span data-ttu-id="2babc-663">7</span><span class="sxs-lookup"><span data-stu-id="2babc-663">7</span></span>

<span data-ttu-id="2babc-664">8</span><span class="sxs-lookup"><span data-stu-id="2babc-664">8</span></span>

<span data-ttu-id="2babc-665">9</span><span class="sxs-lookup"><span data-stu-id="2babc-665">9</span></span>

<span data-ttu-id="2babc-666">2</span><span class="sxs-lookup"><span data-stu-id="2babc-666">2</span></span><br/> <span data-ttu-id="2babc-667">0</span><span class="sxs-lookup"><span data-stu-id="2babc-667">0</span></span><br/>

<span data-ttu-id="2babc-668">1</span><span class="sxs-lookup"><span data-stu-id="2babc-668">1</span></span>

<span data-ttu-id="2babc-669">2</span><span class="sxs-lookup"><span data-stu-id="2babc-669">2</span></span>

<span data-ttu-id="2babc-670">3</span><span class="sxs-lookup"><span data-stu-id="2babc-670">3</span></span>

<span data-ttu-id="2babc-671">4</span><span class="sxs-lookup"><span data-stu-id="2babc-671">4</span></span>

<span data-ttu-id="2babc-672">5</span><span class="sxs-lookup"><span data-stu-id="2babc-672">5</span></span>

<span data-ttu-id="2babc-673">6</span><span class="sxs-lookup"><span data-stu-id="2babc-673">6</span></span>

<span data-ttu-id="2babc-674">7</span><span class="sxs-lookup"><span data-stu-id="2babc-674">7</span></span>

<span data-ttu-id="2babc-675">8</span><span class="sxs-lookup"><span data-stu-id="2babc-675">8</span></span>

<span data-ttu-id="2babc-676">9</span><span class="sxs-lookup"><span data-stu-id="2babc-676">9</span></span>

<span data-ttu-id="2babc-677">3</span><span class="sxs-lookup"><span data-stu-id="2babc-677">3</span></span><br/> <span data-ttu-id="2babc-678">0</span><span class="sxs-lookup"><span data-stu-id="2babc-678">0</span></span><br/>

<span data-ttu-id="2babc-679">1</span><span class="sxs-lookup"><span data-stu-id="2babc-679">1</span></span>

<span data-ttu-id="2babc-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="2babc-680">vVectorElements</span></span>

<span data-ttu-id="2babc-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="2babc-681">vVectorData</span></span>



 

<span data-ttu-id="2babc-682">**vVectorElements**: entier non signé 32 bits, indiquant le nombre d’éléments contenus dans le champ vVectorData.</span><span class="sxs-lookup"><span data-stu-id="2babc-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="2babc-683">**vVectorData**: tableau d’éléments qui ont un type indiqué par vType avec le bit 0x1000 effacé.</span><span class="sxs-lookup"><span data-stu-id="2babc-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="2babc-684">La taille d’un élément de longueur fixe individuel peut être obtenue à partir de la table de type de données de longueur fixe, comme indiqué dans la section 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="2babc-685">La longueur de ce champ, en octets, peut être calculée en multipliant vVectorElements par la taille d’un élément individuel.</span><span class="sxs-lookup"><span data-stu-id="2babc-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="2babc-686">Pour les types de données de longueur variable, vVectorData contient une séquence de types simples marshalés consécutivement, où le type est indiqué par vType avec le bit 0x1000 effacé.</span><span class="sxs-lookup"><span data-stu-id="2babc-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="2babc-687">Cela comprend un cas spécial indiqué par la \_ variante VT du tableau VTYPE VT \| \_ (c’est-à-dire, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="2babc-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="2babc-688">Les éléments du champ vVectorData doivent être séparés par 0 à 3 octets de remplissage, de sorte que chaque élément commence à un offset qui est un multiple de 4 octets à partir du début du message qui contient ce tableau.</span><span class="sxs-lookup"><span data-stu-id="2babc-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="2babc-689">Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="2babc-690">Le contenu des octets de remplissage doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-691">Pour un vType défini sur une \_ variante VT du tableau VT \| \_ , le type des éléments de cette séquence est CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="2babc-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="2babc-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="2babc-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="2babc-693">SAFEARRAY est utilisé pour passer des tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="2babc-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="2babc-694">La structure contient des informations sur la taille du tableau ainsi que les données du tableau.</span><span class="sxs-lookup"><span data-stu-id="2babc-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="2babc-695">0</span><span class="sxs-lookup"><span data-stu-id="2babc-695">0</span></span>

<span data-ttu-id="2babc-696">1</span><span class="sxs-lookup"><span data-stu-id="2babc-696">1</span></span>

<span data-ttu-id="2babc-697">2</span><span class="sxs-lookup"><span data-stu-id="2babc-697">2</span></span>

<span data-ttu-id="2babc-698">3</span><span class="sxs-lookup"><span data-stu-id="2babc-698">3</span></span>

<span data-ttu-id="2babc-699">4</span><span class="sxs-lookup"><span data-stu-id="2babc-699">4</span></span>

<span data-ttu-id="2babc-700">5</span><span class="sxs-lookup"><span data-stu-id="2babc-700">5</span></span>

<span data-ttu-id="2babc-701">6</span><span class="sxs-lookup"><span data-stu-id="2babc-701">6</span></span>

<span data-ttu-id="2babc-702">7</span><span class="sxs-lookup"><span data-stu-id="2babc-702">7</span></span>

<span data-ttu-id="2babc-703">8</span><span class="sxs-lookup"><span data-stu-id="2babc-703">8</span></span>

<span data-ttu-id="2babc-704">9</span><span class="sxs-lookup"><span data-stu-id="2babc-704">9</span></span>

<span data-ttu-id="2babc-705">1</span><span class="sxs-lookup"><span data-stu-id="2babc-705">1</span></span><br/> <span data-ttu-id="2babc-706">0</span><span class="sxs-lookup"><span data-stu-id="2babc-706">0</span></span><br/>

<span data-ttu-id="2babc-707">1</span><span class="sxs-lookup"><span data-stu-id="2babc-707">1</span></span>

<span data-ttu-id="2babc-708">2</span><span class="sxs-lookup"><span data-stu-id="2babc-708">2</span></span>

<span data-ttu-id="2babc-709">3</span><span class="sxs-lookup"><span data-stu-id="2babc-709">3</span></span>

<span data-ttu-id="2babc-710">4</span><span class="sxs-lookup"><span data-stu-id="2babc-710">4</span></span>

<span data-ttu-id="2babc-711">5</span><span class="sxs-lookup"><span data-stu-id="2babc-711">5</span></span>

<span data-ttu-id="2babc-712">6</span><span class="sxs-lookup"><span data-stu-id="2babc-712">6</span></span>

<span data-ttu-id="2babc-713">7</span><span class="sxs-lookup"><span data-stu-id="2babc-713">7</span></span>

<span data-ttu-id="2babc-714">8</span><span class="sxs-lookup"><span data-stu-id="2babc-714">8</span></span>

<span data-ttu-id="2babc-715">9</span><span class="sxs-lookup"><span data-stu-id="2babc-715">9</span></span>

<span data-ttu-id="2babc-716">2</span><span class="sxs-lookup"><span data-stu-id="2babc-716">2</span></span><br/> <span data-ttu-id="2babc-717">0</span><span class="sxs-lookup"><span data-stu-id="2babc-717">0</span></span><br/>

<span data-ttu-id="2babc-718">1</span><span class="sxs-lookup"><span data-stu-id="2babc-718">1</span></span>

<span data-ttu-id="2babc-719">2</span><span class="sxs-lookup"><span data-stu-id="2babc-719">2</span></span>

<span data-ttu-id="2babc-720">3</span><span class="sxs-lookup"><span data-stu-id="2babc-720">3</span></span>

<span data-ttu-id="2babc-721">4</span><span class="sxs-lookup"><span data-stu-id="2babc-721">4</span></span>

<span data-ttu-id="2babc-722">5</span><span class="sxs-lookup"><span data-stu-id="2babc-722">5</span></span>

<span data-ttu-id="2babc-723">6</span><span class="sxs-lookup"><span data-stu-id="2babc-723">6</span></span>

<span data-ttu-id="2babc-724">7</span><span class="sxs-lookup"><span data-stu-id="2babc-724">7</span></span>

<span data-ttu-id="2babc-725">8</span><span class="sxs-lookup"><span data-stu-id="2babc-725">8</span></span>

<span data-ttu-id="2babc-726">9</span><span class="sxs-lookup"><span data-stu-id="2babc-726">9</span></span>

<span data-ttu-id="2babc-727">3</span><span class="sxs-lookup"><span data-stu-id="2babc-727">3</span></span><br/> <span data-ttu-id="2babc-728">0</span><span class="sxs-lookup"><span data-stu-id="2babc-728">0</span></span><br/>

<span data-ttu-id="2babc-729">1</span><span class="sxs-lookup"><span data-stu-id="2babc-729">1</span></span>

<span data-ttu-id="2babc-730">cDims</span><span class="sxs-lookup"><span data-stu-id="2babc-730">cDims</span></span>

<span data-ttu-id="2babc-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="2babc-731">fFeatures</span></span>

<span data-ttu-id="2babc-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="2babc-732">cbElements</span></span>

<span data-ttu-id="2babc-733">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-733">Rgsabound (variable)</span></span>

<span data-ttu-id="2babc-734">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-734">vData (variable)</span></span>



 

<span data-ttu-id="2babc-735">**cDims**: entier 16 bits non signé indiquant le nombre de dimensions du tableau multidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="2babc-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="2babc-736">**fFeatures**: un champ de bits de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="2babc-737">Les valeurs représentent les fonctionnalités définies par les applications de couche supérieure et doivent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="2babc-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="2babc-738">**cbElements**: entier non signé 32 bits spécifiant la taille de chaque élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="2babc-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="2babc-739">**Rgsabound**: tableau qui contient une structure SAFEARRAYBOUND, comme spécifié dans la section 2.2.1.1.1.4, par dimension dans le SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="2babc-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="2babc-740">Ce tableau a la dimension la plus à gauche et la dimension la plus à droite en dernier.</span><span class="sxs-lookup"><span data-stu-id="2babc-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="2babc-741">**vdata**: vecteur d’éléments marshalés d’un type particulier, indiqué par le VType du CBaseStorageVariant conteneur, avec le bit 0x2000 effacé.</span><span class="sxs-lookup"><span data-stu-id="2babc-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="2babc-742">vData est marshalé de la même façon \_ que le vecteur VT, comme spécifié dans la section 2.2.1.1.1.2, avec la différence selon laquelle le nombre d’éléments n’est pas stocké devant le vecteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="2babc-743">Au lieu de cela, le nombre d’éléments est calculé en multipliant la valeur cElements par toutes les limites de tableau sécurisées indiquées dans le champ Rgsabound.</span><span class="sxs-lookup"><span data-stu-id="2babc-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="2babc-744">Les éléments sont stockés dans un vecteur dans l’ordre des dimensions, en commençant par la dimension la plus à droite.</span><span class="sxs-lookup"><span data-stu-id="2babc-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="2babc-745">Le diagramme suivant représente visuellement un exemple de tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="2babc-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="2babc-746">La première dimension a un cElements égal à 4 (représenté horizontalement) et lLbound égal à 0, et la deuxième dimension a cElements égal à 2 (représenté verticalement) et lLbound égal à 0.</span><span class="sxs-lookup"><span data-stu-id="2babc-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="2babc-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-747">0x00000001</span></span> | <span data-ttu-id="2babc-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-748">0x00000002</span></span> | <span data-ttu-id="2babc-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-749">0x00000003</span></span> | <span data-ttu-id="2babc-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="2babc-750">0x00000005</span></span> |
| <span data-ttu-id="2babc-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-751">0x00000007</span></span> | <span data-ttu-id="2babc-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2babc-752">0x00000011</span></span> | <span data-ttu-id="2babc-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2babc-753">0x00000013</span></span> | <span data-ttu-id="2babc-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="2babc-754">0x00000017</span></span> |



 

<span data-ttu-id="2babc-755">À l’aide du diagramme ci-dessus, vData contient la séquence suivante : 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (en commençant par parcourir la dimension la plus à droite, puis en incrémentant la dimension suivante).</span><span class="sxs-lookup"><span data-stu-id="2babc-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="2babc-756">Le Rgsabound précédent (qui enregistre cElements et LBound) est : 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="2babc-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="2babc-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="2babc-758">La structure SAFEARRAYBOUND représente les limites d’une dimension d’un SAFEARRAY ou d’un SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="2babc-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="2babc-759">Son format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-759">Its format is:</span></span>



<span data-ttu-id="2babc-760">0</span><span class="sxs-lookup"><span data-stu-id="2babc-760">0</span></span>

<span data-ttu-id="2babc-761">1</span><span class="sxs-lookup"><span data-stu-id="2babc-761">1</span></span>

<span data-ttu-id="2babc-762">2</span><span class="sxs-lookup"><span data-stu-id="2babc-762">2</span></span>

<span data-ttu-id="2babc-763">3</span><span class="sxs-lookup"><span data-stu-id="2babc-763">3</span></span>

<span data-ttu-id="2babc-764">4</span><span class="sxs-lookup"><span data-stu-id="2babc-764">4</span></span>

<span data-ttu-id="2babc-765">5</span><span class="sxs-lookup"><span data-stu-id="2babc-765">5</span></span>

<span data-ttu-id="2babc-766">6</span><span class="sxs-lookup"><span data-stu-id="2babc-766">6</span></span>

<span data-ttu-id="2babc-767">7</span><span class="sxs-lookup"><span data-stu-id="2babc-767">7</span></span>

<span data-ttu-id="2babc-768">8</span><span class="sxs-lookup"><span data-stu-id="2babc-768">8</span></span>

<span data-ttu-id="2babc-769">9</span><span class="sxs-lookup"><span data-stu-id="2babc-769">9</span></span>

<span data-ttu-id="2babc-770">1</span><span class="sxs-lookup"><span data-stu-id="2babc-770">1</span></span><br/> <span data-ttu-id="2babc-771">0</span><span class="sxs-lookup"><span data-stu-id="2babc-771">0</span></span><br/>

<span data-ttu-id="2babc-772">1</span><span class="sxs-lookup"><span data-stu-id="2babc-772">1</span></span>

<span data-ttu-id="2babc-773">2</span><span class="sxs-lookup"><span data-stu-id="2babc-773">2</span></span>

<span data-ttu-id="2babc-774">3</span><span class="sxs-lookup"><span data-stu-id="2babc-774">3</span></span>

<span data-ttu-id="2babc-775">4</span><span class="sxs-lookup"><span data-stu-id="2babc-775">4</span></span>

<span data-ttu-id="2babc-776">5</span><span class="sxs-lookup"><span data-stu-id="2babc-776">5</span></span>

<span data-ttu-id="2babc-777">6</span><span class="sxs-lookup"><span data-stu-id="2babc-777">6</span></span>

<span data-ttu-id="2babc-778">7</span><span class="sxs-lookup"><span data-stu-id="2babc-778">7</span></span>

<span data-ttu-id="2babc-779">8</span><span class="sxs-lookup"><span data-stu-id="2babc-779">8</span></span>

<span data-ttu-id="2babc-780">9</span><span class="sxs-lookup"><span data-stu-id="2babc-780">9</span></span>

<span data-ttu-id="2babc-781">2</span><span class="sxs-lookup"><span data-stu-id="2babc-781">2</span></span><br/> <span data-ttu-id="2babc-782">0</span><span class="sxs-lookup"><span data-stu-id="2babc-782">0</span></span><br/>

<span data-ttu-id="2babc-783">1</span><span class="sxs-lookup"><span data-stu-id="2babc-783">1</span></span>

<span data-ttu-id="2babc-784">2</span><span class="sxs-lookup"><span data-stu-id="2babc-784">2</span></span>

<span data-ttu-id="2babc-785">3</span><span class="sxs-lookup"><span data-stu-id="2babc-785">3</span></span>

<span data-ttu-id="2babc-786">4</span><span class="sxs-lookup"><span data-stu-id="2babc-786">4</span></span>

<span data-ttu-id="2babc-787">5</span><span class="sxs-lookup"><span data-stu-id="2babc-787">5</span></span>

<span data-ttu-id="2babc-788">6</span><span class="sxs-lookup"><span data-stu-id="2babc-788">6</span></span>

<span data-ttu-id="2babc-789">7</span><span class="sxs-lookup"><span data-stu-id="2babc-789">7</span></span>

<span data-ttu-id="2babc-790">8</span><span class="sxs-lookup"><span data-stu-id="2babc-790">8</span></span>

<span data-ttu-id="2babc-791">9</span><span class="sxs-lookup"><span data-stu-id="2babc-791">9</span></span>

<span data-ttu-id="2babc-792">3</span><span class="sxs-lookup"><span data-stu-id="2babc-792">3</span></span><br/> <span data-ttu-id="2babc-793">0</span><span class="sxs-lookup"><span data-stu-id="2babc-793">0</span></span><br/>

<span data-ttu-id="2babc-794">1</span><span class="sxs-lookup"><span data-stu-id="2babc-794">1</span></span>

<span data-ttu-id="2babc-795">cElements</span><span class="sxs-lookup"><span data-stu-id="2babc-795">cElements</span></span>

<span data-ttu-id="2babc-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="2babc-796">lLbound</span></span>



 

<span data-ttu-id="2babc-797">**cElements**: entier non signé 32 bits spécifiant le nombre d’éléments dans la dimension.</span><span class="sxs-lookup"><span data-stu-id="2babc-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="2babc-798">**lLbound**: entier non signé 32 bits spécifiant la limite inférieure de la dimension.</span><span class="sxs-lookup"><span data-stu-id="2babc-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="2babc-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="2babc-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="2babc-800">SAFEARRAY2 est utilisé pour passer des tableaux multidimensionnels dans SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="2babc-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="2babc-801">La structure contient des informations sur les limites ainsi que les données.</span><span class="sxs-lookup"><span data-stu-id="2babc-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="2babc-802">0</span><span class="sxs-lookup"><span data-stu-id="2babc-802">0</span></span>

<span data-ttu-id="2babc-803">1</span><span class="sxs-lookup"><span data-stu-id="2babc-803">1</span></span>

<span data-ttu-id="2babc-804">2</span><span class="sxs-lookup"><span data-stu-id="2babc-804">2</span></span>

<span data-ttu-id="2babc-805">3</span><span class="sxs-lookup"><span data-stu-id="2babc-805">3</span></span>

<span data-ttu-id="2babc-806">4</span><span class="sxs-lookup"><span data-stu-id="2babc-806">4</span></span>

<span data-ttu-id="2babc-807">5</span><span class="sxs-lookup"><span data-stu-id="2babc-807">5</span></span>

<span data-ttu-id="2babc-808">6</span><span class="sxs-lookup"><span data-stu-id="2babc-808">6</span></span>

<span data-ttu-id="2babc-809">7</span><span class="sxs-lookup"><span data-stu-id="2babc-809">7</span></span>

<span data-ttu-id="2babc-810">8</span><span class="sxs-lookup"><span data-stu-id="2babc-810">8</span></span>

<span data-ttu-id="2babc-811">9</span><span class="sxs-lookup"><span data-stu-id="2babc-811">9</span></span>

<span data-ttu-id="2babc-812">1</span><span class="sxs-lookup"><span data-stu-id="2babc-812">1</span></span><br/> <span data-ttu-id="2babc-813">0</span><span class="sxs-lookup"><span data-stu-id="2babc-813">0</span></span><br/>

<span data-ttu-id="2babc-814">1</span><span class="sxs-lookup"><span data-stu-id="2babc-814">1</span></span>

<span data-ttu-id="2babc-815">2</span><span class="sxs-lookup"><span data-stu-id="2babc-815">2</span></span>

<span data-ttu-id="2babc-816">3</span><span class="sxs-lookup"><span data-stu-id="2babc-816">3</span></span>

<span data-ttu-id="2babc-817">4</span><span class="sxs-lookup"><span data-stu-id="2babc-817">4</span></span>

<span data-ttu-id="2babc-818">5</span><span class="sxs-lookup"><span data-stu-id="2babc-818">5</span></span>

<span data-ttu-id="2babc-819">6</span><span class="sxs-lookup"><span data-stu-id="2babc-819">6</span></span>

<span data-ttu-id="2babc-820">7</span><span class="sxs-lookup"><span data-stu-id="2babc-820">7</span></span>

<span data-ttu-id="2babc-821">8</span><span class="sxs-lookup"><span data-stu-id="2babc-821">8</span></span>

<span data-ttu-id="2babc-822">9</span><span class="sxs-lookup"><span data-stu-id="2babc-822">9</span></span>

<span data-ttu-id="2babc-823">2</span><span class="sxs-lookup"><span data-stu-id="2babc-823">2</span></span><br/> <span data-ttu-id="2babc-824">0</span><span class="sxs-lookup"><span data-stu-id="2babc-824">0</span></span><br/>

<span data-ttu-id="2babc-825">1</span><span class="sxs-lookup"><span data-stu-id="2babc-825">1</span></span>

<span data-ttu-id="2babc-826">2</span><span class="sxs-lookup"><span data-stu-id="2babc-826">2</span></span>

<span data-ttu-id="2babc-827">3</span><span class="sxs-lookup"><span data-stu-id="2babc-827">3</span></span>

<span data-ttu-id="2babc-828">4</span><span class="sxs-lookup"><span data-stu-id="2babc-828">4</span></span>

<span data-ttu-id="2babc-829">5</span><span class="sxs-lookup"><span data-stu-id="2babc-829">5</span></span>

<span data-ttu-id="2babc-830">6</span><span class="sxs-lookup"><span data-stu-id="2babc-830">6</span></span>

<span data-ttu-id="2babc-831">7</span><span class="sxs-lookup"><span data-stu-id="2babc-831">7</span></span>

<span data-ttu-id="2babc-832">8</span><span class="sxs-lookup"><span data-stu-id="2babc-832">8</span></span>

<span data-ttu-id="2babc-833">9</span><span class="sxs-lookup"><span data-stu-id="2babc-833">9</span></span>

<span data-ttu-id="2babc-834">3</span><span class="sxs-lookup"><span data-stu-id="2babc-834">3</span></span><br/> <span data-ttu-id="2babc-835">0</span><span class="sxs-lookup"><span data-stu-id="2babc-835">0</span></span><br/>

<span data-ttu-id="2babc-836">1</span><span class="sxs-lookup"><span data-stu-id="2babc-836">1</span></span>

<span data-ttu-id="2babc-837">cDims</span><span class="sxs-lookup"><span data-stu-id="2babc-837">cDims</span></span>

<span data-ttu-id="2babc-838">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-838">Rgsabound (variable)</span></span>

<span data-ttu-id="2babc-839">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-839">vData (variable)</span></span>



 

<span data-ttu-id="2babc-840">**cDims**: entier non signé 32 bits, indiquant le nombre de dimensions du SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="2babc-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="2babc-841">**Rgsabound**: tableau qui contient une structure SAFEARRAYBOUND, comme spécifié dans la section 2.2.1.1.1.4 par dimension dans le SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="2babc-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="2babc-842">Ce tableau a la dimension la plus à gauche et la dimension la plus à droite en dernier.</span><span class="sxs-lookup"><span data-stu-id="2babc-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="2babc-843">**vdata**: vecteur d’éléments marshalés d’un type particulier, indiqué par le DWTYPE du SERIALIZEDPROPERTYVALUE conteneur, avec le bit 0x2000 effacé.</span><span class="sxs-lookup"><span data-stu-id="2babc-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="2babc-844">Le format de vData est le même que celui spécifié pour le champ vData de SAFEARRAY dans la section 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="2babc-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="2babc-845">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="2babc-846">La structure CFullPropSpec contient un GUID de jeu de propriétés et un identificateur de propriété pour identifier la propriété de manière unique.</span><span class="sxs-lookup"><span data-stu-id="2babc-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="2babc-847">0</span><span class="sxs-lookup"><span data-stu-id="2babc-847">0</span></span>

<span data-ttu-id="2babc-848">1</span><span class="sxs-lookup"><span data-stu-id="2babc-848">1</span></span>

<span data-ttu-id="2babc-849">2</span><span class="sxs-lookup"><span data-stu-id="2babc-849">2</span></span>

<span data-ttu-id="2babc-850">3</span><span class="sxs-lookup"><span data-stu-id="2babc-850">3</span></span>

<span data-ttu-id="2babc-851">4</span><span class="sxs-lookup"><span data-stu-id="2babc-851">4</span></span>

<span data-ttu-id="2babc-852">5</span><span class="sxs-lookup"><span data-stu-id="2babc-852">5</span></span>

<span data-ttu-id="2babc-853">6</span><span class="sxs-lookup"><span data-stu-id="2babc-853">6</span></span>

<span data-ttu-id="2babc-854">7</span><span class="sxs-lookup"><span data-stu-id="2babc-854">7</span></span>

<span data-ttu-id="2babc-855">8</span><span class="sxs-lookup"><span data-stu-id="2babc-855">8</span></span>

<span data-ttu-id="2babc-856">9</span><span class="sxs-lookup"><span data-stu-id="2babc-856">9</span></span>

<span data-ttu-id="2babc-857">1</span><span class="sxs-lookup"><span data-stu-id="2babc-857">1</span></span><br/> <span data-ttu-id="2babc-858">0</span><span class="sxs-lookup"><span data-stu-id="2babc-858">0</span></span><br/>

<span data-ttu-id="2babc-859">1</span><span class="sxs-lookup"><span data-stu-id="2babc-859">1</span></span>

<span data-ttu-id="2babc-860">2</span><span class="sxs-lookup"><span data-stu-id="2babc-860">2</span></span>

<span data-ttu-id="2babc-861">3</span><span class="sxs-lookup"><span data-stu-id="2babc-861">3</span></span>

<span data-ttu-id="2babc-862">4</span><span class="sxs-lookup"><span data-stu-id="2babc-862">4</span></span>

<span data-ttu-id="2babc-863">5</span><span class="sxs-lookup"><span data-stu-id="2babc-863">5</span></span>

<span data-ttu-id="2babc-864">6</span><span class="sxs-lookup"><span data-stu-id="2babc-864">6</span></span>

<span data-ttu-id="2babc-865">7</span><span class="sxs-lookup"><span data-stu-id="2babc-865">7</span></span>

<span data-ttu-id="2babc-866">8</span><span class="sxs-lookup"><span data-stu-id="2babc-866">8</span></span>

<span data-ttu-id="2babc-867">9</span><span class="sxs-lookup"><span data-stu-id="2babc-867">9</span></span>

<span data-ttu-id="2babc-868">2</span><span class="sxs-lookup"><span data-stu-id="2babc-868">2</span></span><br/> <span data-ttu-id="2babc-869">0</span><span class="sxs-lookup"><span data-stu-id="2babc-869">0</span></span><br/>

<span data-ttu-id="2babc-870">1</span><span class="sxs-lookup"><span data-stu-id="2babc-870">1</span></span>

<span data-ttu-id="2babc-871">2</span><span class="sxs-lookup"><span data-stu-id="2babc-871">2</span></span>

<span data-ttu-id="2babc-872">3</span><span class="sxs-lookup"><span data-stu-id="2babc-872">3</span></span>

<span data-ttu-id="2babc-873">4</span><span class="sxs-lookup"><span data-stu-id="2babc-873">4</span></span>

<span data-ttu-id="2babc-874">5</span><span class="sxs-lookup"><span data-stu-id="2babc-874">5</span></span>

<span data-ttu-id="2babc-875">6</span><span class="sxs-lookup"><span data-stu-id="2babc-875">6</span></span>

<span data-ttu-id="2babc-876">7</span><span class="sxs-lookup"><span data-stu-id="2babc-876">7</span></span>

<span data-ttu-id="2babc-877">8</span><span class="sxs-lookup"><span data-stu-id="2babc-877">8</span></span>

<span data-ttu-id="2babc-878">9</span><span class="sxs-lookup"><span data-stu-id="2babc-878">9</span></span>

<span data-ttu-id="2babc-879">3</span><span class="sxs-lookup"><span data-stu-id="2babc-879">3</span></span><br/> <span data-ttu-id="2babc-880">0</span><span class="sxs-lookup"><span data-stu-id="2babc-880">0</span></span><br/>

<span data-ttu-id="2babc-881">1</span><span class="sxs-lookup"><span data-stu-id="2babc-881">1</span></span>

<span data-ttu-id="2babc-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="2babc-882">\_guidPropSet</span></span>

<span data-ttu-id="2babc-883">...</span><span class="sxs-lookup"><span data-stu-id="2babc-883">...</span></span>

<span data-ttu-id="2babc-884">...</span><span class="sxs-lookup"><span data-stu-id="2babc-884">...</span></span>

<span data-ttu-id="2babc-885">...</span><span class="sxs-lookup"><span data-stu-id="2babc-885">...</span></span>

<span data-ttu-id="2babc-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="2babc-886">ulKind</span></span>

<span data-ttu-id="2babc-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-887">PrSpec</span></span>

<span data-ttu-id="2babc-888">Nom de la propriété (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-888">Property name (variable)</span></span>



 

<span data-ttu-id="2babc-889">**\_ GUIDPROPSET**: GUID du jeu de propriétés auquel appartient la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="2babc-890">**ulKind**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-891">L’une des valeurs suivantes, qui indique le contenu de PrSpec.</span><span class="sxs-lookup"><span data-stu-id="2babc-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="2babc-892">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-892">Value</span></span>                                            | <span data-ttu-id="2babc-893">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-894">PRSPEC \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="2babc-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="2babc-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-895">0x00000000</span></span><br/> | <span data-ttu-id="2babc-896">Le champ PrSpec spécifie le nombre de caractères non NULL dans le champ nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="2babc-897">PRSPEC \_ propid</span><span class="sxs-lookup"><span data-stu-id="2babc-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="2babc-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-898">0x00000001</span></span><br/>  | <span data-ttu-id="2babc-899">Le champ PrSpec spécifie l’ID de propriété (PROPID).</span><span class="sxs-lookup"><span data-stu-id="2babc-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="2babc-900">**PrSpec**: entier non signé 32 bits avec une signification comme indiqué par le champ ulKind.</span><span class="sxs-lookup"><span data-stu-id="2babc-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="2babc-901">**Nom** de la propriété : si ulKind a la valeur PRSPEC \_ propId, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="2babc-902">Si ulKind a la valeur PRSPEC \_ LPWStr, ce champ doit contenir un tableau ne respectant pas la casse des caractères Unicode non null PRSPEC, contenant le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="2babc-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="2babc-904">La structure CContentRestriction contient une chaîne à faire correspondre pour une propriété dans le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="2babc-905">0</span><span class="sxs-lookup"><span data-stu-id="2babc-905">0</span></span>

<span data-ttu-id="2babc-906">1</span><span class="sxs-lookup"><span data-stu-id="2babc-906">1</span></span>

<span data-ttu-id="2babc-907">2</span><span class="sxs-lookup"><span data-stu-id="2babc-907">2</span></span>

<span data-ttu-id="2babc-908">3</span><span class="sxs-lookup"><span data-stu-id="2babc-908">3</span></span>

<span data-ttu-id="2babc-909">4</span><span class="sxs-lookup"><span data-stu-id="2babc-909">4</span></span>

<span data-ttu-id="2babc-910">5</span><span class="sxs-lookup"><span data-stu-id="2babc-910">5</span></span>

<span data-ttu-id="2babc-911">6</span><span class="sxs-lookup"><span data-stu-id="2babc-911">6</span></span>

<span data-ttu-id="2babc-912">7</span><span class="sxs-lookup"><span data-stu-id="2babc-912">7</span></span>

<span data-ttu-id="2babc-913">8</span><span class="sxs-lookup"><span data-stu-id="2babc-913">8</span></span>

<span data-ttu-id="2babc-914">9</span><span class="sxs-lookup"><span data-stu-id="2babc-914">9</span></span>

<span data-ttu-id="2babc-915">1</span><span class="sxs-lookup"><span data-stu-id="2babc-915">1</span></span><br/> <span data-ttu-id="2babc-916">0</span><span class="sxs-lookup"><span data-stu-id="2babc-916">0</span></span><br/>

<span data-ttu-id="2babc-917">1</span><span class="sxs-lookup"><span data-stu-id="2babc-917">1</span></span>

<span data-ttu-id="2babc-918">2</span><span class="sxs-lookup"><span data-stu-id="2babc-918">2</span></span>

<span data-ttu-id="2babc-919">3</span><span class="sxs-lookup"><span data-stu-id="2babc-919">3</span></span>

<span data-ttu-id="2babc-920">4</span><span class="sxs-lookup"><span data-stu-id="2babc-920">4</span></span>

<span data-ttu-id="2babc-921">5</span><span class="sxs-lookup"><span data-stu-id="2babc-921">5</span></span>

<span data-ttu-id="2babc-922">6</span><span class="sxs-lookup"><span data-stu-id="2babc-922">6</span></span>

<span data-ttu-id="2babc-923">7</span><span class="sxs-lookup"><span data-stu-id="2babc-923">7</span></span>

<span data-ttu-id="2babc-924">8</span><span class="sxs-lookup"><span data-stu-id="2babc-924">8</span></span>

<span data-ttu-id="2babc-925">9</span><span class="sxs-lookup"><span data-stu-id="2babc-925">9</span></span>

<span data-ttu-id="2babc-926">2</span><span class="sxs-lookup"><span data-stu-id="2babc-926">2</span></span><br/> <span data-ttu-id="2babc-927">0</span><span class="sxs-lookup"><span data-stu-id="2babc-927">0</span></span><br/>

<span data-ttu-id="2babc-928">1</span><span class="sxs-lookup"><span data-stu-id="2babc-928">1</span></span>

<span data-ttu-id="2babc-929">2</span><span class="sxs-lookup"><span data-stu-id="2babc-929">2</span></span>

<span data-ttu-id="2babc-930">3</span><span class="sxs-lookup"><span data-stu-id="2babc-930">3</span></span>

<span data-ttu-id="2babc-931">4</span><span class="sxs-lookup"><span data-stu-id="2babc-931">4</span></span>

<span data-ttu-id="2babc-932">5</span><span class="sxs-lookup"><span data-stu-id="2babc-932">5</span></span>

<span data-ttu-id="2babc-933">6</span><span class="sxs-lookup"><span data-stu-id="2babc-933">6</span></span>

<span data-ttu-id="2babc-934">7</span><span class="sxs-lookup"><span data-stu-id="2babc-934">7</span></span>

<span data-ttu-id="2babc-935">8</span><span class="sxs-lookup"><span data-stu-id="2babc-935">8</span></span>

<span data-ttu-id="2babc-936">9</span><span class="sxs-lookup"><span data-stu-id="2babc-936">9</span></span>

<span data-ttu-id="2babc-937">3</span><span class="sxs-lookup"><span data-stu-id="2babc-937">3</span></span><br/> <span data-ttu-id="2babc-938">0</span><span class="sxs-lookup"><span data-stu-id="2babc-938">0</span></span><br/>

<span data-ttu-id="2babc-939">1</span><span class="sxs-lookup"><span data-stu-id="2babc-939">1</span></span>

<span data-ttu-id="2babc-940">\_Property (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-940">\_Property (variable)</span></span>

<span data-ttu-id="2babc-941">...</span><span class="sxs-lookup"><span data-stu-id="2babc-941">...</span></span>

<span data-ttu-id="2babc-942">Padding1 (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-942">Padding1 (variable)</span></span>

<span data-ttu-id="2babc-943">Cc</span><span class="sxs-lookup"><span data-stu-id="2babc-943">Cc</span></span>

<span data-ttu-id="2babc-944">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="2babc-945">...</span><span class="sxs-lookup"><span data-stu-id="2babc-945">...</span></span>

<span data-ttu-id="2babc-946">Padding2 (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-946">Padding2 (variable)</span></span>

<span data-ttu-id="2babc-947">lcid</span><span class="sxs-lookup"><span data-stu-id="2babc-947">lcid</span></span>

<span data-ttu-id="2babc-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="2babc-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="2babc-949">**\_ Property**: une structure CFullPropSpec, comme indiqué dans la section 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="2babc-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="2babc-950">Ce champ indique la propriété sur laquelle effectuer une opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="2babc-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="2babc-951">**Padding1**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="2babc-952">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="2babc-953">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="2babc-954">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-955">**CC**: entier non signé 32 bits, spécifiant le nombre de caractères dans le \_ champ pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="2babc-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="2babc-956">**\_ pwcsPhrase**: chaîne Unicode qui se termine par un caractère non null représentant le mot ou l’expression à mettre en correspondance pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="2babc-957">Ce champ ne doit pas être vide.</span><span class="sxs-lookup"><span data-stu-id="2babc-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="2babc-958">Le champ CC contient la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2babc-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="2babc-959">**Padding2**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="2babc-960">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="2babc-961">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="2babc-962">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-963">**LCID**: entier non signé 32 bits indiquant les paramètres régionaux de \_ pwcsPhrase, comme indiqué dans \[ MS-GPSI \] annexe A.</span><span class="sxs-lookup"><span data-stu-id="2babc-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="2babc-964">**\_ ulGenerateMethod**: entier non signé 32 bits, spécifiant la méthode à utiliser lors de la génération de formes de mots secondaires</span><span class="sxs-lookup"><span data-stu-id="2babc-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="2babc-965">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-965">Value</span></span>                                                       | <span data-ttu-id="2babc-966">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-967">GÉNÉRATION \_ exacte de la méthode \_</span><span class="sxs-lookup"><span data-stu-id="2babc-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="2babc-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-968">0x00000000</span></span><br/>    | <span data-ttu-id="2babc-969">Correspondance exacte.</span><span class="sxs-lookup"><span data-stu-id="2babc-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2babc-970">GÉNÉRER \_ le \_ préfixe de méthode</span><span class="sxs-lookup"><span data-stu-id="2babc-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="2babc-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-971">0x00000001</span></span> <br/>  | <span data-ttu-id="2babc-972">Correspondance du préfixe.</span><span class="sxs-lookup"><span data-stu-id="2babc-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="2babc-973">GENERATE, \_ méthode \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="2babc-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="2babc-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-974">0x00000002</span></span><br/> | <span data-ttu-id="2babc-975">Correspond aux fléchies d’un mot.</span><span class="sxs-lookup"><span data-stu-id="2babc-975">Matches inflections of a word.</span></span> <span data-ttu-id="2babc-976">Une inflexion d’un mot est une variante du mot racine dans la même partie de la parole qui a été modifiée selon les règles linguistiques d’une langue donnée.</span><span class="sxs-lookup"><span data-stu-id="2babc-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="2babc-977">Par exemple, les formes fléchies du verbe « natation » en anglais incluent « natation », « natation », « natation » et « SWAM ».</span><span class="sxs-lookup"><span data-stu-id="2babc-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="2babc-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="2babc-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="2babc-979">La structure CKey contient une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="2babc-980">0</span><span class="sxs-lookup"><span data-stu-id="2babc-980">0</span></span>

<span data-ttu-id="2babc-981">1</span><span class="sxs-lookup"><span data-stu-id="2babc-981">1</span></span>

<span data-ttu-id="2babc-982">2</span><span class="sxs-lookup"><span data-stu-id="2babc-982">2</span></span>

<span data-ttu-id="2babc-983">3</span><span class="sxs-lookup"><span data-stu-id="2babc-983">3</span></span>

<span data-ttu-id="2babc-984">4</span><span class="sxs-lookup"><span data-stu-id="2babc-984">4</span></span>

<span data-ttu-id="2babc-985">5</span><span class="sxs-lookup"><span data-stu-id="2babc-985">5</span></span>

<span data-ttu-id="2babc-986">6</span><span class="sxs-lookup"><span data-stu-id="2babc-986">6</span></span>

<span data-ttu-id="2babc-987">7</span><span class="sxs-lookup"><span data-stu-id="2babc-987">7</span></span>

<span data-ttu-id="2babc-988">8</span><span class="sxs-lookup"><span data-stu-id="2babc-988">8</span></span>

<span data-ttu-id="2babc-989">9</span><span class="sxs-lookup"><span data-stu-id="2babc-989">9</span></span>

<span data-ttu-id="2babc-990">1</span><span class="sxs-lookup"><span data-stu-id="2babc-990">1</span></span><br/> <span data-ttu-id="2babc-991">0</span><span class="sxs-lookup"><span data-stu-id="2babc-991">0</span></span><br/>

<span data-ttu-id="2babc-992">1</span><span class="sxs-lookup"><span data-stu-id="2babc-992">1</span></span>

<span data-ttu-id="2babc-993">2</span><span class="sxs-lookup"><span data-stu-id="2babc-993">2</span></span>

<span data-ttu-id="2babc-994">3</span><span class="sxs-lookup"><span data-stu-id="2babc-994">3</span></span>

<span data-ttu-id="2babc-995">4</span><span class="sxs-lookup"><span data-stu-id="2babc-995">4</span></span>

<span data-ttu-id="2babc-996">5</span><span class="sxs-lookup"><span data-stu-id="2babc-996">5</span></span>

<span data-ttu-id="2babc-997">6</span><span class="sxs-lookup"><span data-stu-id="2babc-997">6</span></span>

<span data-ttu-id="2babc-998">7</span><span class="sxs-lookup"><span data-stu-id="2babc-998">7</span></span>

<span data-ttu-id="2babc-999">8</span><span class="sxs-lookup"><span data-stu-id="2babc-999">8</span></span>

<span data-ttu-id="2babc-1000">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1000">9</span></span>

<span data-ttu-id="2babc-1001">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1001">2</span></span><br/> <span data-ttu-id="2babc-1002">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1002">0</span></span><br/>

<span data-ttu-id="2babc-1003">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1003">1</span></span>

<span data-ttu-id="2babc-1004">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1004">2</span></span>

<span data-ttu-id="2babc-1005">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1005">3</span></span>

<span data-ttu-id="2babc-1006">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1006">4</span></span>

<span data-ttu-id="2babc-1007">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1007">5</span></span>

<span data-ttu-id="2babc-1008">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1008">6</span></span>

<span data-ttu-id="2babc-1009">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1009">7</span></span>

<span data-ttu-id="2babc-1010">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1010">8</span></span>

<span data-ttu-id="2babc-1011">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1011">9</span></span>

<span data-ttu-id="2babc-1012">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1012">3</span></span><br/> <span data-ttu-id="2babc-1013">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1013">0</span></span><br/>

<span data-ttu-id="2babc-1014">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1014">1</span></span>

<span data-ttu-id="2babc-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="2babc-1015">PROPID</span></span>

<span data-ttu-id="2babc-1016">Libéré</span><span class="sxs-lookup"><span data-stu-id="2babc-1016">Cb</span></span>

<span data-ttu-id="2babc-1017">buf (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1017">buf (variable)</span></span>



 

<span data-ttu-id="2babc-1018">**Propid**: entier non signé 32 bits représentant l’ID de propriété comme indiqué dans la section 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="2babc-1019">Les valeurs connues sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-1019">Well-known values are:</span></span>



| <span data-ttu-id="2babc-1020">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1020">Value</span></span>      | <span data-ttu-id="2babc-1021">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="2babc-1022">Égale</span><span class="sxs-lookup"><span data-stu-id="2babc-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="2babc-1023">Représente un ID de propriété non valide et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2babc-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="2babc-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="2babc-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="2babc-1025">Représente un ID de propriété non valide et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2babc-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="2babc-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-1026">0x00000000</span></span> | <span data-ttu-id="2babc-1027">Représente un ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="2babc-1028">**CB**: entier non signé 32 bits contenant la longueur de buf, en octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="2babc-1029">**buf**: séquence d’octets représentant la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="2babc-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="2babc-1031">La structure CInternalPropertyRestriction contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="2babc-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="2babc-1032">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1032">0</span></span>

<span data-ttu-id="2babc-1033">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1033">1</span></span>

<span data-ttu-id="2babc-1034">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1034">2</span></span>

<span data-ttu-id="2babc-1035">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1035">3</span></span>

<span data-ttu-id="2babc-1036">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1036">4</span></span>

<span data-ttu-id="2babc-1037">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1037">5</span></span>

<span data-ttu-id="2babc-1038">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1038">6</span></span>

<span data-ttu-id="2babc-1039">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1039">7</span></span>

<span data-ttu-id="2babc-1040">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1040">8</span></span>

<span data-ttu-id="2babc-1041">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1041">9</span></span>

<span data-ttu-id="2babc-1042">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1042">1</span></span><br/> <span data-ttu-id="2babc-1043">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1043">0</span></span><br/>

<span data-ttu-id="2babc-1044">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1044">1</span></span>

<span data-ttu-id="2babc-1045">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1045">2</span></span>

<span data-ttu-id="2babc-1046">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1046">3</span></span>

<span data-ttu-id="2babc-1047">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1047">4</span></span>

<span data-ttu-id="2babc-1048">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1048">5</span></span>

<span data-ttu-id="2babc-1049">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1049">6</span></span>

<span data-ttu-id="2babc-1050">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1050">7</span></span>

<span data-ttu-id="2babc-1051">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1051">8</span></span>

<span data-ttu-id="2babc-1052">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1052">9</span></span>

<span data-ttu-id="2babc-1053">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1053">2</span></span><br/> <span data-ttu-id="2babc-1054">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1054">0</span></span><br/>

<span data-ttu-id="2babc-1055">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1055">1</span></span>

<span data-ttu-id="2babc-1056">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1056">2</span></span>

<span data-ttu-id="2babc-1057">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1057">3</span></span>

<span data-ttu-id="2babc-1058">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1058">4</span></span>

<span data-ttu-id="2babc-1059">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1059">5</span></span>

<span data-ttu-id="2babc-1060">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1060">6</span></span>

<span data-ttu-id="2babc-1061">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1061">7</span></span>

<span data-ttu-id="2babc-1062">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1062">8</span></span>

<span data-ttu-id="2babc-1063">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1063">9</span></span>

<span data-ttu-id="2babc-1064">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1064">3</span></span><br/> <span data-ttu-id="2babc-1065">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1065">0</span></span><br/>

<span data-ttu-id="2babc-1066">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1066">1</span></span>

<span data-ttu-id="2babc-1067">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="2babc-1067">\_relop</span></span>

<span data-ttu-id="2babc-1068">\_ELECTRIQUE</span><span class="sxs-lookup"><span data-stu-id="2babc-1068">\_pid</span></span>

<span data-ttu-id="2babc-1069">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1069">\_prval (variable)</span></span>

<span data-ttu-id="2babc-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="2babc-1070">restrictionPresent</span></span>

<span data-ttu-id="2babc-1071">nextRestriction (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="2babc-1072">**\_ RelOp**: entier 32 bits spécifiant la relation à exécuter sur la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="2babc-1073">Il doit s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="2babc-1074">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1074">Value</span></span>                 | <span data-ttu-id="2babc-1075">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1076">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="2babc-1077">Comparaison d’infériorité.</span><span class="sxs-lookup"><span data-stu-id="2babc-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="2babc-1078">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="2babc-1079">Comparaison d’infériorité ou d’égalité.</span><span class="sxs-lookup"><span data-stu-id="2babc-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="2babc-1080">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="2babc-1081">Comparaison plus grande que.</span><span class="sxs-lookup"><span data-stu-id="2babc-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="2babc-1082">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="2babc-1083">Comparaison supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="2babc-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="2babc-1084">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="2babc-1085">Comparaison d’égalité.</span><span class="sxs-lookup"><span data-stu-id="2babc-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="2babc-1086">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="2babc-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="2babc-1087">Comparaison inégale.</span><span class="sxs-lookup"><span data-stu-id="2babc-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="2babc-1088">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="2babc-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="2babc-1089">Comparaison d’expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="2babc-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="2babc-1090">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="2babc-1091">Opérateur de bits AND qui retourne l’opérande de droite.</span><span class="sxs-lookup"><span data-stu-id="2babc-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="2babc-1092">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="2babc-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="2babc-1093">Opérateur de bits AND qui retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2babc-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="2babc-1094">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="2babc-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="2babc-1095">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et n’a la valeur true que si l’opération a la valeur true pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="2babc-1096">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="2babc-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="2babc-1097">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et a la valeur true si l’opération a la valeur true pour une ligne quelconque.</span><span class="sxs-lookup"><span data-stu-id="2babc-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="2babc-1098">**\_ PID**: entier non signé 32 bits représentant l’ID de propriété (consultez PROPID dans la section 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="2babc-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="2babc-1099">**\_ Prval**: CBaseStorageVariant contenant la valeur à associer à la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="2babc-1100">**restrictionPresent**: valeur d’octet indiquant si le champ nextRestriction est présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="2babc-1101">DOIT être défini sur 0x00 ou 0x01.</span><span class="sxs-lookup"><span data-stu-id="2babc-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="2babc-1102">Si cette valeur est définie sur 0x01, restrictionPresent indique que le champ nextRestriction est présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="2babc-1103">Si la valeur est 0x00, restrictionPresent indique que le champ nextRestriction n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="2babc-1104">**nextRestriction**: structure CRestriction, comme spécifié dans la section 2.2.1.16, en spécifiant une restriction supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="2babc-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="2babc-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="2babc-1106">La structure CNatLanguageRestriction contient une correspondance de **requête en langage naturel** pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="2babc-1107">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1107">0</span></span>

<span data-ttu-id="2babc-1108">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1108">1</span></span>

<span data-ttu-id="2babc-1109">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1109">2</span></span>

<span data-ttu-id="2babc-1110">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1110">3</span></span>

<span data-ttu-id="2babc-1111">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1111">4</span></span>

<span data-ttu-id="2babc-1112">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1112">5</span></span>

<span data-ttu-id="2babc-1113">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1113">6</span></span>

<span data-ttu-id="2babc-1114">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1114">7</span></span>

<span data-ttu-id="2babc-1115">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1115">8</span></span>

<span data-ttu-id="2babc-1116">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1116">9</span></span>

<span data-ttu-id="2babc-1117">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1117">1</span></span><br/> <span data-ttu-id="2babc-1118">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1118">0</span></span><br/>

<span data-ttu-id="2babc-1119">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1119">1</span></span>

<span data-ttu-id="2babc-1120">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1120">2</span></span>

<span data-ttu-id="2babc-1121">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1121">3</span></span>

<span data-ttu-id="2babc-1122">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1122">4</span></span>

<span data-ttu-id="2babc-1123">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1123">5</span></span>

<span data-ttu-id="2babc-1124">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1124">6</span></span>

<span data-ttu-id="2babc-1125">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1125">7</span></span>

<span data-ttu-id="2babc-1126">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1126">8</span></span>

<span data-ttu-id="2babc-1127">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1127">9</span></span>

<span data-ttu-id="2babc-1128">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1128">2</span></span><br/> <span data-ttu-id="2babc-1129">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1129">0</span></span><br/>

<span data-ttu-id="2babc-1130">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1130">1</span></span>

<span data-ttu-id="2babc-1131">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1131">2</span></span>

<span data-ttu-id="2babc-1132">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1132">3</span></span>

<span data-ttu-id="2babc-1133">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1133">4</span></span>

<span data-ttu-id="2babc-1134">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1134">5</span></span>

<span data-ttu-id="2babc-1135">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1135">6</span></span>

<span data-ttu-id="2babc-1136">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1136">7</span></span>

<span data-ttu-id="2babc-1137">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1137">8</span></span>

<span data-ttu-id="2babc-1138">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1138">9</span></span>

<span data-ttu-id="2babc-1139">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1139">3</span></span><br/> <span data-ttu-id="2babc-1140">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1140">0</span></span><br/>

<span data-ttu-id="2babc-1141">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1141">1</span></span>

<span data-ttu-id="2babc-1142">\_Property (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1142">\_Property (variable)</span></span>

<span data-ttu-id="2babc-1143">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1143">...</span></span>

<span data-ttu-id="2babc-1144">\_remplissage \_ de CC (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="2babc-1145">Cc</span><span class="sxs-lookup"><span data-stu-id="2babc-1145">Cc</span></span>

<span data-ttu-id="2babc-1146">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="2babc-1147">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1147">...</span></span>

<span data-ttu-id="2babc-1148">\_\_LCID de remplissage (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="2babc-1149">Lcid</span><span class="sxs-lookup"><span data-stu-id="2babc-1149">Lcid</span></span>



 

<span data-ttu-id="2babc-1150">**\_ Property**: une structure CFullPropSpec, comme indiqué dans la section 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="2babc-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="2babc-1151">Ce champ indique la propriété sur laquelle effectuer l’opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="2babc-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="2babc-1152">**\_ remplissage de \_ CC**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="2babc-1153">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="2babc-1154">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="2babc-1155">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-1156">**CC**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-1157">Nombre de caractères dans le \_ champ pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="2babc-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="2babc-1158">**\_ pwcsPhrase**: chaîne Unicode qui se termine par un caractère non null représentant le mot ou l’expression à mettre en correspondance pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="2babc-1159">NE doit pas être vide.</span><span class="sxs-lookup"><span data-stu-id="2babc-1159">MUST NOT be empty.</span></span> <span data-ttu-id="2babc-1160">Le champ CC contient la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2babc-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="2babc-1161">**\_ \_ LCID de remplissage**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="2babc-1162">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="2babc-1163">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="2babc-1164">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-1165">**LCID**: entier non signé 32 bits indiquant les paramètres régionaux de \_ pwcsPhrase, comme spécifié dans \[ MS-GPSI \] annexe A.</span><span class="sxs-lookup"><span data-stu-id="2babc-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="2babc-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="2babc-1167">La structure CNodeRestriction contient un tableau de nœuds d' **arborescence de commandes** qui spécifient les restrictions pour la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="2babc-1168">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1168">0</span></span>

<span data-ttu-id="2babc-1169">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1169">1</span></span>

<span data-ttu-id="2babc-1170">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1170">2</span></span>

<span data-ttu-id="2babc-1171">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1171">3</span></span>

<span data-ttu-id="2babc-1172">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1172">4</span></span>

<span data-ttu-id="2babc-1173">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1173">5</span></span>

<span data-ttu-id="2babc-1174">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1174">6</span></span>

<span data-ttu-id="2babc-1175">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1175">7</span></span>

<span data-ttu-id="2babc-1176">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1176">8</span></span>

<span data-ttu-id="2babc-1177">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1177">9</span></span>

<span data-ttu-id="2babc-1178">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1178">1</span></span><br/> <span data-ttu-id="2babc-1179">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1179">0</span></span><br/>

<span data-ttu-id="2babc-1180">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1180">1</span></span>

<span data-ttu-id="2babc-1181">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1181">2</span></span>

<span data-ttu-id="2babc-1182">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1182">3</span></span>

<span data-ttu-id="2babc-1183">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1183">4</span></span>

<span data-ttu-id="2babc-1184">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1184">5</span></span>

<span data-ttu-id="2babc-1185">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1185">6</span></span>

<span data-ttu-id="2babc-1186">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1186">7</span></span>

<span data-ttu-id="2babc-1187">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1187">8</span></span>

<span data-ttu-id="2babc-1188">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1188">9</span></span>

<span data-ttu-id="2babc-1189">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1189">2</span></span><br/> <span data-ttu-id="2babc-1190">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1190">0</span></span><br/>

<span data-ttu-id="2babc-1191">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1191">1</span></span>

<span data-ttu-id="2babc-1192">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1192">2</span></span>

<span data-ttu-id="2babc-1193">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1193">3</span></span>

<span data-ttu-id="2babc-1194">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1194">4</span></span>

<span data-ttu-id="2babc-1195">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1195">5</span></span>

<span data-ttu-id="2babc-1196">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1196">6</span></span>

<span data-ttu-id="2babc-1197">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1197">7</span></span>

<span data-ttu-id="2babc-1198">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1198">8</span></span>

<span data-ttu-id="2babc-1199">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1199">9</span></span>

<span data-ttu-id="2babc-1200">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1200">3</span></span><br/> <span data-ttu-id="2babc-1201">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1201">0</span></span><br/>

<span data-ttu-id="2babc-1202">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1202">1</span></span>

<span data-ttu-id="2babc-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="2babc-1203">\_cNode</span></span>

<span data-ttu-id="2babc-1204">\_paNode (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="2babc-1205">**\_ CNode**: entier non signé 32 bits spécifiant le nombre de structures CRestriction contenues dans le \_ champ paNode.</span><span class="sxs-lookup"><span data-stu-id="2babc-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="2babc-1206">**\_ paNode**: tableau de structures CRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="2babc-1207">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient ce tableau.</span><span class="sxs-lookup"><span data-stu-id="2babc-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="2babc-1208">Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="2babc-1209">Le contenu des octets de remplissage doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="2babc-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="2babc-1211">La structure COccRestriction contient l’emplacement d’un mot dans une expression.</span><span class="sxs-lookup"><span data-stu-id="2babc-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="2babc-1212">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1212">0</span></span>

<span data-ttu-id="2babc-1213">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1213">1</span></span>

<span data-ttu-id="2babc-1214">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1214">2</span></span>

<span data-ttu-id="2babc-1215">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1215">3</span></span>

<span data-ttu-id="2babc-1216">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1216">4</span></span>

<span data-ttu-id="2babc-1217">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1217">5</span></span>

<span data-ttu-id="2babc-1218">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1218">6</span></span>

<span data-ttu-id="2babc-1219">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1219">7</span></span>

<span data-ttu-id="2babc-1220">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1220">8</span></span>

<span data-ttu-id="2babc-1221">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1221">9</span></span>

<span data-ttu-id="2babc-1222">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1222">1</span></span><br/> <span data-ttu-id="2babc-1223">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1223">0</span></span><br/>

<span data-ttu-id="2babc-1224">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1224">1</span></span>

<span data-ttu-id="2babc-1225">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1225">2</span></span>

<span data-ttu-id="2babc-1226">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1226">3</span></span>

<span data-ttu-id="2babc-1227">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1227">4</span></span>

<span data-ttu-id="2babc-1228">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1228">5</span></span>

<span data-ttu-id="2babc-1229">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1229">6</span></span>

<span data-ttu-id="2babc-1230">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1230">7</span></span>

<span data-ttu-id="2babc-1231">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1231">8</span></span>

<span data-ttu-id="2babc-1232">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1232">9</span></span>

<span data-ttu-id="2babc-1233">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1233">2</span></span><br/> <span data-ttu-id="2babc-1234">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1234">0</span></span><br/>

<span data-ttu-id="2babc-1235">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1235">1</span></span>

<span data-ttu-id="2babc-1236">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1236">2</span></span>

<span data-ttu-id="2babc-1237">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1237">3</span></span>

<span data-ttu-id="2babc-1238">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1238">4</span></span>

<span data-ttu-id="2babc-1239">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1239">5</span></span>

<span data-ttu-id="2babc-1240">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1240">6</span></span>

<span data-ttu-id="2babc-1241">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1241">7</span></span>

<span data-ttu-id="2babc-1242">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1242">8</span></span>

<span data-ttu-id="2babc-1243">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1243">9</span></span>

<span data-ttu-id="2babc-1244">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1244">3</span></span><br/> <span data-ttu-id="2babc-1245">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1245">0</span></span><br/>

<span data-ttu-id="2babc-1246">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1246">1</span></span>

<span data-ttu-id="2babc-1247">\_ETag</span><span class="sxs-lookup"><span data-stu-id="2babc-1247">\_occ</span></span>

<span data-ttu-id="2babc-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="2babc-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="2babc-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="2babc-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="2babc-1250">**\_ ETag**: entier non signé 32 bits spécifiant le décalage du mot dans une chaîne de requête, en unités de mots.</span><span class="sxs-lookup"><span data-stu-id="2babc-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="2babc-1251">Un mot, tel qu’il est utilisé dans cette spécification, est une unité de langue dans tous les paramètres régionaux qui impliquent la signification.</span><span class="sxs-lookup"><span data-stu-id="2babc-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="2babc-1252">**\_ cPrevNoiseWords**: entier non signé 32 bits contenant le nombre de **mots parasites** qui se produisent entre ce mot et le mot précédent dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="2babc-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="2babc-1253">**\_ cNextNoiseWords**: entier non signé 32 bits contenant le nombre de mots parasites qui se produisent entre ce mot et le mot suivant dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="2babc-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="2babc-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="2babc-1255">La structure CPropertyRestriction contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="2babc-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="2babc-1256">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1256">0</span></span>

<span data-ttu-id="2babc-1257">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1257">1</span></span>

<span data-ttu-id="2babc-1258">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1258">2</span></span>

<span data-ttu-id="2babc-1259">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1259">3</span></span>

<span data-ttu-id="2babc-1260">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1260">4</span></span>

<span data-ttu-id="2babc-1261">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1261">5</span></span>

<span data-ttu-id="2babc-1262">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1262">6</span></span>

<span data-ttu-id="2babc-1263">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1263">7</span></span>

<span data-ttu-id="2babc-1264">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1264">8</span></span>

<span data-ttu-id="2babc-1265">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1265">9</span></span>

<span data-ttu-id="2babc-1266">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1266">1</span></span><br/> <span data-ttu-id="2babc-1267">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1267">0</span></span><br/>

<span data-ttu-id="2babc-1268">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1268">1</span></span>

<span data-ttu-id="2babc-1269">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1269">2</span></span>

<span data-ttu-id="2babc-1270">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1270">3</span></span>

<span data-ttu-id="2babc-1271">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1271">4</span></span>

<span data-ttu-id="2babc-1272">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1272">5</span></span>

<span data-ttu-id="2babc-1273">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1273">6</span></span>

<span data-ttu-id="2babc-1274">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1274">7</span></span>

<span data-ttu-id="2babc-1275">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1275">8</span></span>

<span data-ttu-id="2babc-1276">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1276">9</span></span>

<span data-ttu-id="2babc-1277">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1277">2</span></span><br/> <span data-ttu-id="2babc-1278">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1278">0</span></span><br/>

<span data-ttu-id="2babc-1279">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1279">1</span></span>

<span data-ttu-id="2babc-1280">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1280">2</span></span>

<span data-ttu-id="2babc-1281">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1281">3</span></span>

<span data-ttu-id="2babc-1282">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1282">4</span></span>

<span data-ttu-id="2babc-1283">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1283">5</span></span>

<span data-ttu-id="2babc-1284">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1284">6</span></span>

<span data-ttu-id="2babc-1285">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1285">7</span></span>

<span data-ttu-id="2babc-1286">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1286">8</span></span>

<span data-ttu-id="2babc-1287">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1287">9</span></span>

<span data-ttu-id="2babc-1288">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1288">3</span></span><br/> <span data-ttu-id="2babc-1289">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1289">0</span></span><br/>

<span data-ttu-id="2babc-1290">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1290">1</span></span>

<span data-ttu-id="2babc-1291">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="2babc-1291">\_relop</span></span>

<span data-ttu-id="2babc-1292">\_Property (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1292">\_Property (variable)</span></span>

<span data-ttu-id="2babc-1293">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="2babc-1294">**\_ RelOp**: entier non signé 32 bits spécifiant la relation à exécuter sur la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="2babc-1295">DOIT avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="2babc-1296">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1296">Value</span></span>                 | <span data-ttu-id="2babc-1297">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1298">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="2babc-1299">Comparaison d’infériorité.</span><span class="sxs-lookup"><span data-stu-id="2babc-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="2babc-1300">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="2babc-1301">Comparaison d’infériorité ou d’égalité.</span><span class="sxs-lookup"><span data-stu-id="2babc-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="2babc-1302">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="2babc-1303">Comparaison plus grande que.</span><span class="sxs-lookup"><span data-stu-id="2babc-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="2babc-1304">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="2babc-1305">Comparaison supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="2babc-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="2babc-1306">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="2babc-1307">Comparaison d’égalité.</span><span class="sxs-lookup"><span data-stu-id="2babc-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="2babc-1308">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="2babc-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="2babc-1309">Comparaison inégale.</span><span class="sxs-lookup"><span data-stu-id="2babc-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="2babc-1310">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="2babc-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="2babc-1311">Comparaison d’expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="2babc-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="2babc-1312">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="2babc-1313">Opérateur de bits AND qui retourne l’opérande de droite.</span><span class="sxs-lookup"><span data-stu-id="2babc-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="2babc-1314">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="2babc-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="2babc-1315">Opérateur de bits AND qui retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2babc-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="2babc-1316">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="2babc-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="2babc-1317">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et n’a la valeur true que si l’opération a la valeur true pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="2babc-1318">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="2babc-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="2babc-1319">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et a la valeur true si l’opération a la valeur true pour une ligne quelconque.</span><span class="sxs-lookup"><span data-stu-id="2babc-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="2babc-1320">**\_ Propriété**: une structure CFullPropSpec, comme spécifié dans la section 2.2.1.2, indiquant la propriété sur laquelle effectuer une opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="2babc-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="2babc-1321">**\_ prval**: structure CBaseStorageVariant, comme indiqué dans la section 2.2.1.1, contenant la valeur à associer à la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="2babc-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="2babc-1323">La structure CRangeRestriction contient une restriction sur une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="2babc-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="2babc-1324">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1324">0</span></span>

<span data-ttu-id="2babc-1325">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1325">1</span></span>

<span data-ttu-id="2babc-1326">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1326">2</span></span>

<span data-ttu-id="2babc-1327">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1327">3</span></span>

<span data-ttu-id="2babc-1328">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1328">4</span></span>

<span data-ttu-id="2babc-1329">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1329">5</span></span>

<span data-ttu-id="2babc-1330">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1330">6</span></span>

<span data-ttu-id="2babc-1331">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1331">7</span></span>

<span data-ttu-id="2babc-1332">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1332">8</span></span>

<span data-ttu-id="2babc-1333">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1333">9</span></span>

<span data-ttu-id="2babc-1334">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1334">1</span></span><br/> <span data-ttu-id="2babc-1335">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1335">0</span></span><br/>

<span data-ttu-id="2babc-1336">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1336">1</span></span>

<span data-ttu-id="2babc-1337">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1337">2</span></span>

<span data-ttu-id="2babc-1338">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1338">3</span></span>

<span data-ttu-id="2babc-1339">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1339">4</span></span>

<span data-ttu-id="2babc-1340">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1340">5</span></span>

<span data-ttu-id="2babc-1341">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1341">6</span></span>

<span data-ttu-id="2babc-1342">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1342">7</span></span>

<span data-ttu-id="2babc-1343">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1343">8</span></span>

<span data-ttu-id="2babc-1344">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1344">9</span></span>

<span data-ttu-id="2babc-1345">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1345">2</span></span><br/> <span data-ttu-id="2babc-1346">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1346">0</span></span><br/>

<span data-ttu-id="2babc-1347">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1347">1</span></span>

<span data-ttu-id="2babc-1348">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1348">2</span></span>

<span data-ttu-id="2babc-1349">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1349">3</span></span>

<span data-ttu-id="2babc-1350">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1350">4</span></span>

<span data-ttu-id="2babc-1351">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1351">5</span></span>

<span data-ttu-id="2babc-1352">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1352">6</span></span>

<span data-ttu-id="2babc-1353">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1353">7</span></span>

<span data-ttu-id="2babc-1354">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1354">8</span></span>

<span data-ttu-id="2babc-1355">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1355">9</span></span>

<span data-ttu-id="2babc-1356">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1356">3</span></span><br/> <span data-ttu-id="2babc-1357">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1357">0</span></span><br/>

<span data-ttu-id="2babc-1358">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1358">1</span></span>

<span data-ttu-id="2babc-1359">\_keystart (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="2babc-1360">\_keyEnd (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="2babc-1361">**\_ keystart**: une structure CKey, comme spécifié dans la section 2.2.1.4, contenant le début de la plage.</span><span class="sxs-lookup"><span data-stu-id="2babc-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="2babc-1362">**\_ keyEnd**: structure CKey contenant la fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="2babc-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="2babc-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="2babc-1364">La structure CScopeRestriction contient une restriction sur les fichiers à rechercher.</span><span class="sxs-lookup"><span data-stu-id="2babc-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="2babc-1365">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1365">0</span></span>

<span data-ttu-id="2babc-1366">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1366">1</span></span>

<span data-ttu-id="2babc-1367">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1367">2</span></span>

<span data-ttu-id="2babc-1368">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1368">3</span></span>

<span data-ttu-id="2babc-1369">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1369">4</span></span>

<span data-ttu-id="2babc-1370">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1370">5</span></span>

<span data-ttu-id="2babc-1371">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1371">6</span></span>

<span data-ttu-id="2babc-1372">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1372">7</span></span>

<span data-ttu-id="2babc-1373">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1373">8</span></span>

<span data-ttu-id="2babc-1374">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1374">9</span></span>

<span data-ttu-id="2babc-1375">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1375">1</span></span><br/> <span data-ttu-id="2babc-1376">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1376">0</span></span><br/>

<span data-ttu-id="2babc-1377">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1377">1</span></span>

<span data-ttu-id="2babc-1378">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1378">2</span></span>

<span data-ttu-id="2babc-1379">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1379">3</span></span>

<span data-ttu-id="2babc-1380">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1380">4</span></span>

<span data-ttu-id="2babc-1381">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1381">5</span></span>

<span data-ttu-id="2babc-1382">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1382">6</span></span>

<span data-ttu-id="2babc-1383">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1383">7</span></span>

<span data-ttu-id="2babc-1384">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1384">8</span></span>

<span data-ttu-id="2babc-1385">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1385">9</span></span>

<span data-ttu-id="2babc-1386">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1386">2</span></span><br/> <span data-ttu-id="2babc-1387">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1387">0</span></span><br/>

<span data-ttu-id="2babc-1388">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1388">1</span></span>

<span data-ttu-id="2babc-1389">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1389">2</span></span>

<span data-ttu-id="2babc-1390">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1390">3</span></span>

<span data-ttu-id="2babc-1391">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1391">4</span></span>

<span data-ttu-id="2babc-1392">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1392">5</span></span>

<span data-ttu-id="2babc-1393">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1393">6</span></span>

<span data-ttu-id="2babc-1394">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1394">7</span></span>

<span data-ttu-id="2babc-1395">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1395">8</span></span>

<span data-ttu-id="2babc-1396">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1396">9</span></span>

<span data-ttu-id="2babc-1397">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1397">3</span></span><br/> <span data-ttu-id="2babc-1398">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1398">0</span></span><br/>

<span data-ttu-id="2babc-1399">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1399">1</span></span>

<span data-ttu-id="2babc-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="2babc-1400">CcLowerPath</span></span>

<span data-ttu-id="2babc-1401">\_lowerPath (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="2babc-1402">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1402">...</span></span>

<span data-ttu-id="2babc-1403">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1403">\_padding ( variable)</span></span>

<span data-ttu-id="2babc-1404">\_base</span><span class="sxs-lookup"><span data-stu-id="2babc-1404">\_length</span></span>

<span data-ttu-id="2babc-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="2babc-1405">\_fRecursive</span></span>

<span data-ttu-id="2babc-1406">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="2babc-1406">\_fVirtual</span></span>



 

<span data-ttu-id="2babc-1407">**CcLowerPath**: entier non signé 32 bits contenant le nombre de caractères Unicode dans le \_ champ lowerPath.</span><span class="sxs-lookup"><span data-stu-id="2babc-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="2babc-1408">**\_ lowerPath**: chaîne Unicode qui se termine par un caractère non null qui représente le **chemin d’accès** auquel la requête doit être restreinte.</span><span class="sxs-lookup"><span data-stu-id="2babc-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="2babc-1409">Le champ CcLowerPath contient la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2babc-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="2babc-1410">**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="2babc-1411">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="2babc-1412">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="2babc-1413">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-1414">**\_ Length**: entier non signé 32 bits contenant la longueur de \_ LowerPath, en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="2babc-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="2babc-1415">Il doit s’agir de la même valeur que CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="2babc-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="2babc-1416">**\_ fRecursive**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-1417">DOIT être défini sur 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="2babc-1418">Si la valeur est définie sur 0x00000001, le serveur doit examiner de manière récursive tous les sous-répertoires du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="2babc-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="2babc-1419">Si la valeur est 0x00000000, le serveur n’examine pas les sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="2babc-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="2babc-1420">**\_ fVirtual**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-1421">DOIT être défini sur 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="2babc-1422">Si la valeur est 0x00000001, \_ lowerPath est un chemin d’accès virtuel (le Uniform Resource Locator (URL) associé à un répertoire physique sur le système de fichiers) pour un site Web.</span><span class="sxs-lookup"><span data-stu-id="2babc-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="2babc-1423">Si la valeur est 0x00000000, \_ lowerPath est un chemin d’accès au système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2babc-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="2babc-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="2babc-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="2babc-1425">La structure CSort identifie une colonne à trier.</span><span class="sxs-lookup"><span data-stu-id="2babc-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="2babc-1426">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1426">0</span></span>

<span data-ttu-id="2babc-1427">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1427">1</span></span>

<span data-ttu-id="2babc-1428">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1428">2</span></span>

<span data-ttu-id="2babc-1429">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1429">3</span></span>

<span data-ttu-id="2babc-1430">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1430">4</span></span>

<span data-ttu-id="2babc-1431">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1431">5</span></span>

<span data-ttu-id="2babc-1432">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1432">6</span></span>

<span data-ttu-id="2babc-1433">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1433">7</span></span>

<span data-ttu-id="2babc-1434">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1434">8</span></span>

<span data-ttu-id="2babc-1435">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1435">9</span></span>

<span data-ttu-id="2babc-1436">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1436">1</span></span><br/> <span data-ttu-id="2babc-1437">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1437">0</span></span><br/>

<span data-ttu-id="2babc-1438">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1438">1</span></span>

<span data-ttu-id="2babc-1439">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1439">2</span></span>

<span data-ttu-id="2babc-1440">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1440">3</span></span>

<span data-ttu-id="2babc-1441">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1441">4</span></span>

<span data-ttu-id="2babc-1442">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1442">5</span></span>

<span data-ttu-id="2babc-1443">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1443">6</span></span>

<span data-ttu-id="2babc-1444">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1444">7</span></span>

<span data-ttu-id="2babc-1445">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1445">8</span></span>

<span data-ttu-id="2babc-1446">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1446">9</span></span>

<span data-ttu-id="2babc-1447">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1447">2</span></span><br/> <span data-ttu-id="2babc-1448">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1448">0</span></span><br/>

<span data-ttu-id="2babc-1449">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1449">1</span></span>

<span data-ttu-id="2babc-1450">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1450">2</span></span>

<span data-ttu-id="2babc-1451">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1451">3</span></span>

<span data-ttu-id="2babc-1452">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1452">4</span></span>

<span data-ttu-id="2babc-1453">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1453">5</span></span>

<span data-ttu-id="2babc-1454">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1454">6</span></span>

<span data-ttu-id="2babc-1455">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1455">7</span></span>

<span data-ttu-id="2babc-1456">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1456">8</span></span>

<span data-ttu-id="2babc-1457">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1457">9</span></span>

<span data-ttu-id="2babc-1458">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1458">3</span></span><br/> <span data-ttu-id="2babc-1459">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1459">0</span></span><br/>

<span data-ttu-id="2babc-1460">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1460">1</span></span>

<span data-ttu-id="2babc-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="2babc-1461">pidColumn</span></span>

<span data-ttu-id="2babc-1462">Valeur dwOrd</span><span class="sxs-lookup"><span data-stu-id="2babc-1462">dwOrder</span></span>

<span data-ttu-id="2babc-1463">locale</span><span class="sxs-lookup"><span data-stu-id="2babc-1463">locale</span></span>



 

<span data-ttu-id="2babc-1464">**pidColumn**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-1465">Numéro de la colonne par laquelle Trier.</span><span class="sxs-lookup"><span data-stu-id="2babc-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="2babc-1466">**DWORD**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-1467">DOIT avoir l’une des valeurs suivantes, en spécifiant comment trier en fonction de la colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="2babc-1468">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1468">Value</span></span>                        | <span data-ttu-id="2babc-1469">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1470">REQUÊTE \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="2babc-1471">Les lignes doivent être triées dans l’ordre croissant en fonction des valeurs de la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2babc-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="2babc-1472">REQUÊTE \_ descendante 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="2babc-1473">Les lignes doivent être triées dans l’ordre décroissant en fonction des valeurs de la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2babc-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="2babc-1474">**paramètres régionaux**: entier non signé 32 bits indiquant les paramètres régionaux, tels que spécifiés dans \[ MS-GPSI \] annexe A, de la colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="2babc-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="2babc-1476">La structure CSynRestriction contient un mot ou ses synonymes pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="2babc-1477">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1477">0</span></span>

<span data-ttu-id="2babc-1478">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1478">1</span></span>

<span data-ttu-id="2babc-1479">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1479">2</span></span>

<span data-ttu-id="2babc-1480">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1480">3</span></span>

<span data-ttu-id="2babc-1481">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1481">4</span></span>

<span data-ttu-id="2babc-1482">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1482">5</span></span>

<span data-ttu-id="2babc-1483">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1483">6</span></span>

<span data-ttu-id="2babc-1484">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1484">7</span></span>

<span data-ttu-id="2babc-1485">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1485">8</span></span>

<span data-ttu-id="2babc-1486">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1486">9</span></span>

<span data-ttu-id="2babc-1487">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1487">1</span></span><br/> <span data-ttu-id="2babc-1488">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1488">0</span></span><br/>

<span data-ttu-id="2babc-1489">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1489">1</span></span>

<span data-ttu-id="2babc-1490">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1490">2</span></span>

<span data-ttu-id="2babc-1491">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1491">3</span></span>

<span data-ttu-id="2babc-1492">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1492">4</span></span>

<span data-ttu-id="2babc-1493">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1493">5</span></span>

<span data-ttu-id="2babc-1494">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1494">6</span></span>

<span data-ttu-id="2babc-1495">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1495">7</span></span>

<span data-ttu-id="2babc-1496">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1496">8</span></span>

<span data-ttu-id="2babc-1497">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1497">9</span></span>

<span data-ttu-id="2babc-1498">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1498">2</span></span><br/> <span data-ttu-id="2babc-1499">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1499">0</span></span><br/>

<span data-ttu-id="2babc-1500">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1500">1</span></span>

<span data-ttu-id="2babc-1501">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1501">2</span></span>

<span data-ttu-id="2babc-1502">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1502">3</span></span>

<span data-ttu-id="2babc-1503">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1503">4</span></span>

<span data-ttu-id="2babc-1504">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1504">5</span></span>

<span data-ttu-id="2babc-1505">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1505">6</span></span>

<span data-ttu-id="2babc-1506">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1506">7</span></span>

<span data-ttu-id="2babc-1507">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1507">8</span></span>

<span data-ttu-id="2babc-1508">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1508">9</span></span>

<span data-ttu-id="2babc-1509">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1509">3</span></span><br/> <span data-ttu-id="2babc-1510">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1510">0</span></span><br/>

<span data-ttu-id="2babc-1511">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1511">1</span></span>

<span data-ttu-id="2babc-1512">Restriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1512">Restriction</span></span>

<span data-ttu-id="2babc-1513">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1513">...</span></span>

<span data-ttu-id="2babc-1514">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1514">...</span></span>

<span data-ttu-id="2babc-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="2babc-1515">cKey</span></span>

<span data-ttu-id="2babc-1516">\_keyarray (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="2babc-1517">\_isRange</span><span class="sxs-lookup"><span data-stu-id="2babc-1517">\_isRange</span></span>



 

<span data-ttu-id="2babc-1518">**Restriction**: structure COccRestriction spécifiant l’emplacement du mot.</span><span class="sxs-lookup"><span data-stu-id="2babc-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="2babc-1519">**CKEY**: entier non signé 32 bits spécifiant le nombre d’éléments dans le tableau de \_ tableaux de la matrice.</span><span class="sxs-lookup"><span data-stu-id="2babc-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="2babc-1520">**\_ keyarray**: tableau de structures CKey spécifiant un mot et ses synonymes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="2babc-1521">**\_ isRange**: si la valeur est 0x01, les clés sont des préfixes à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="2babc-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="2babc-1522">Si la valeur est 0x00, les clés sont des valeurs exactes à mettre en correspondance.</span><span class="sxs-lookup"><span data-stu-id="2babc-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="2babc-1523">\_isRange ne doit avoir aucune autre valeur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="2babc-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="2babc-1525">La structure CVectorRestriction contient une opération pondérée sur un nœud d’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="2babc-1526">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1526">0</span></span>

<span data-ttu-id="2babc-1527">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1527">1</span></span>

<span data-ttu-id="2babc-1528">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1528">2</span></span>

<span data-ttu-id="2babc-1529">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1529">3</span></span>

<span data-ttu-id="2babc-1530">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1530">4</span></span>

<span data-ttu-id="2babc-1531">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1531">5</span></span>

<span data-ttu-id="2babc-1532">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1532">6</span></span>

<span data-ttu-id="2babc-1533">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1533">7</span></span>

<span data-ttu-id="2babc-1534">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1534">8</span></span>

<span data-ttu-id="2babc-1535">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1535">9</span></span>

<span data-ttu-id="2babc-1536">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1536">1</span></span><br/> <span data-ttu-id="2babc-1537">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1537">0</span></span><br/>

<span data-ttu-id="2babc-1538">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1538">1</span></span>

<span data-ttu-id="2babc-1539">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1539">2</span></span>

<span data-ttu-id="2babc-1540">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1540">3</span></span>

<span data-ttu-id="2babc-1541">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1541">4</span></span>

<span data-ttu-id="2babc-1542">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1542">5</span></span>

<span data-ttu-id="2babc-1543">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1543">6</span></span>

<span data-ttu-id="2babc-1544">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1544">7</span></span>

<span data-ttu-id="2babc-1545">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1545">8</span></span>

<span data-ttu-id="2babc-1546">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1546">9</span></span>

<span data-ttu-id="2babc-1547">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1547">2</span></span><br/> <span data-ttu-id="2babc-1548">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1548">0</span></span><br/>

<span data-ttu-id="2babc-1549">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1549">1</span></span>

<span data-ttu-id="2babc-1550">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1550">2</span></span>

<span data-ttu-id="2babc-1551">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1551">3</span></span>

<span data-ttu-id="2babc-1552">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1552">4</span></span>

<span data-ttu-id="2babc-1553">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1553">5</span></span>

<span data-ttu-id="2babc-1554">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1554">6</span></span>

<span data-ttu-id="2babc-1555">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1555">7</span></span>

<span data-ttu-id="2babc-1556">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1556">8</span></span>

<span data-ttu-id="2babc-1557">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1557">9</span></span>

<span data-ttu-id="2babc-1558">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1558">3</span></span><br/> <span data-ttu-id="2babc-1559">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1559">0</span></span><br/>

<span data-ttu-id="2babc-1560">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1560">1</span></span>

<span data-ttu-id="2babc-1561">\_PRES (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1561">\_pres (variable)</span></span>

<span data-ttu-id="2babc-1562">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1562">...</span></span>

<span data-ttu-id="2babc-1563">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1563">\_padding (variable)</span></span>

<span data-ttu-id="2babc-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="2babc-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="2babc-1565">**\_ pres**: arborescence de commandes CNodeRestriction sur laquelle un classement ou une opération doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="2babc-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="2babc-1566">**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="2babc-1567">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="2babc-1568">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="2babc-1569">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-1570">**\_ ulRankMethod**: entier non signé 32 bits spécifiant un algorithme de classement.</span><span class="sxs-lookup"><span data-stu-id="2babc-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="2babc-1571">DOIT être défini sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="2babc-1572">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1572">Value</span></span>                            | <span data-ttu-id="2babc-1573">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="2babc-1574">Rang de vecteur \_ \_ min 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="2babc-1575">Utilisez l’algorithme minimal \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="2babc-1576">Nombre maximal de VECTEURs \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="2babc-1577">Utilisez le nombre maximal d’algorithmes \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="2babc-1578">VECTOR de \_ classement \_ interne 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="2babc-1579">Utilisez l’algorithme de produit interne \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="2babc-1580">\_0x00000003 de rang de vecteurs \_</span><span class="sxs-lookup"><span data-stu-id="2babc-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="2babc-1581">Utiliser l’algorithme de coefficient \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="2babc-1582">Classement de vecteur \_ \_ Jaccard 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="2babc-1583">Utilisez l’algorithme de coefficient Jaccard \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="2babc-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="2babc-1585">La structure CWordRestriction contient un mot pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="2babc-1586">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1586">0</span></span>

<span data-ttu-id="2babc-1587">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1587">1</span></span>

<span data-ttu-id="2babc-1588">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1588">2</span></span>

<span data-ttu-id="2babc-1589">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1589">3</span></span>

<span data-ttu-id="2babc-1590">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1590">4</span></span>

<span data-ttu-id="2babc-1591">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1591">5</span></span>

<span data-ttu-id="2babc-1592">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1592">6</span></span>

<span data-ttu-id="2babc-1593">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1593">7</span></span>

<span data-ttu-id="2babc-1594">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1594">8</span></span>

<span data-ttu-id="2babc-1595">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1595">9</span></span>

<span data-ttu-id="2babc-1596">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1596">1</span></span><br/> <span data-ttu-id="2babc-1597">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1597">0</span></span><br/>

<span data-ttu-id="2babc-1598">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1598">1</span></span>

<span data-ttu-id="2babc-1599">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1599">2</span></span>

<span data-ttu-id="2babc-1600">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1600">3</span></span>

<span data-ttu-id="2babc-1601">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1601">4</span></span>

<span data-ttu-id="2babc-1602">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1602">5</span></span>

<span data-ttu-id="2babc-1603">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1603">6</span></span>

<span data-ttu-id="2babc-1604">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1604">7</span></span>

<span data-ttu-id="2babc-1605">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1605">8</span></span>

<span data-ttu-id="2babc-1606">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1606">9</span></span>

<span data-ttu-id="2babc-1607">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1607">2</span></span><br/> <span data-ttu-id="2babc-1608">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1608">0</span></span><br/>

<span data-ttu-id="2babc-1609">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1609">1</span></span>

<span data-ttu-id="2babc-1610">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1610">2</span></span>

<span data-ttu-id="2babc-1611">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1611">3</span></span>

<span data-ttu-id="2babc-1612">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1612">4</span></span>

<span data-ttu-id="2babc-1613">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1613">5</span></span>

<span data-ttu-id="2babc-1614">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1614">6</span></span>

<span data-ttu-id="2babc-1615">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1615">7</span></span>

<span data-ttu-id="2babc-1616">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1616">8</span></span>

<span data-ttu-id="2babc-1617">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1617">9</span></span>

<span data-ttu-id="2babc-1618">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1618">3</span></span><br/> <span data-ttu-id="2babc-1619">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1619">0</span></span><br/>

<span data-ttu-id="2babc-1620">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1620">1</span></span>

<span data-ttu-id="2babc-1621">restriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1621">restriction</span></span>

<span data-ttu-id="2babc-1622">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1622">...</span></span>

<span data-ttu-id="2babc-1623">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1623">...</span></span>

<span data-ttu-id="2babc-1624">\_clé (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1624">\_key (variable)</span></span>

<span data-ttu-id="2babc-1625">\_isRange</span><span class="sxs-lookup"><span data-stu-id="2babc-1625">\_isRange</span></span>



 

<span data-ttu-id="2babc-1626">**restriction**: structure COccRestriction spécifiant l’emplacement du mot.</span><span class="sxs-lookup"><span data-stu-id="2babc-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="2babc-1627">**\_ clé**: une structure CKey spécifiant un mot.</span><span class="sxs-lookup"><span data-stu-id="2babc-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="2babc-1628">**\_ isRange**: si la valeur est 0x01, la clé est un préfixe à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="2babc-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="2babc-1629">Si la valeur est 0x00, la clé est une valeur exacte à mettre en correspondance.</span><span class="sxs-lookup"><span data-stu-id="2babc-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="2babc-1630">\_isRange ne doit pas être défini sur une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="2babc-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="2babc-1632">La structure CRestriction contient un nœud d’une arborescence de commandes de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="2babc-1633">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1633">0</span></span>

<span data-ttu-id="2babc-1634">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1634">1</span></span>

<span data-ttu-id="2babc-1635">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1635">2</span></span>

<span data-ttu-id="2babc-1636">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1636">3</span></span>

<span data-ttu-id="2babc-1637">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1637">4</span></span>

<span data-ttu-id="2babc-1638">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1638">5</span></span>

<span data-ttu-id="2babc-1639">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1639">6</span></span>

<span data-ttu-id="2babc-1640">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1640">7</span></span>

<span data-ttu-id="2babc-1641">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1641">8</span></span>

<span data-ttu-id="2babc-1642">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1642">9</span></span>

<span data-ttu-id="2babc-1643">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1643">1</span></span><br/> <span data-ttu-id="2babc-1644">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1644">0</span></span><br/>

<span data-ttu-id="2babc-1645">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1645">1</span></span>

<span data-ttu-id="2babc-1646">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1646">2</span></span>

<span data-ttu-id="2babc-1647">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1647">3</span></span>

<span data-ttu-id="2babc-1648">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1648">4</span></span>

<span data-ttu-id="2babc-1649">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1649">5</span></span>

<span data-ttu-id="2babc-1650">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1650">6</span></span>

<span data-ttu-id="2babc-1651">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1651">7</span></span>

<span data-ttu-id="2babc-1652">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1652">8</span></span>

<span data-ttu-id="2babc-1653">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1653">9</span></span>

<span data-ttu-id="2babc-1654">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1654">2</span></span><br/> <span data-ttu-id="2babc-1655">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1655">0</span></span><br/>

<span data-ttu-id="2babc-1656">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1656">1</span></span>

<span data-ttu-id="2babc-1657">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1657">2</span></span>

<span data-ttu-id="2babc-1658">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1658">3</span></span>

<span data-ttu-id="2babc-1659">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1659">4</span></span>

<span data-ttu-id="2babc-1660">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1660">5</span></span>

<span data-ttu-id="2babc-1661">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1661">6</span></span>

<span data-ttu-id="2babc-1662">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1662">7</span></span>

<span data-ttu-id="2babc-1663">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1663">8</span></span>

<span data-ttu-id="2babc-1664">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1664">9</span></span>

<span data-ttu-id="2babc-1665">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1665">3</span></span><br/> <span data-ttu-id="2babc-1666">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1666">0</span></span><br/>

<span data-ttu-id="2babc-1667">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1667">1</span></span>

<span data-ttu-id="2babc-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="2babc-1668">\_ulType</span></span>

<span data-ttu-id="2babc-1669">Poids</span><span class="sxs-lookup"><span data-stu-id="2babc-1669">Weight</span></span>

<span data-ttu-id="2babc-1670">Restriction</span><span class="sxs-lookup"><span data-stu-id="2babc-1670">Restriction</span></span>



 

<span data-ttu-id="2babc-1671">**\_ ulType**: entier non signé 32 bits indiquant le type de restriction utilisé pour le nœud de l’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="2babc-1672">DOIT être défini sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="2babc-1673">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1673">Value</span></span>                    | <span data-ttu-id="2babc-1674">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1675">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="2babc-1676">Le nœud représente un mot parasite dans une requête de vecteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="2babc-1677">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="2babc-1678">Le nœud contient un CNodeRestriction sur lequel une opération logique AND doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="2babc-1679">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="2babc-1680">Le nœud contient un CNodeRestriction sur lequel une opération OR logique doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="2babc-1681">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="2babc-1682">Le nœud contient un CRestriction sur lequel une opération NOT doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="2babc-1683">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="2babc-1684">Le nœud contient un CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="2babc-1685">RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="2babc-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="2babc-1686">Le nœud contient un CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="2babc-1687">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="2babc-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="2babc-1688">Le nœud contient un CNodeRestriction sur lequel un classement de proximité doit être effectué,</span><span class="sxs-lookup"><span data-stu-id="2babc-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="2babc-1689">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="2babc-1690">Le nœud contient un CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="2babc-1691">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="2babc-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="2babc-1692">Le nœud contient un CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="2babc-1693">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="2babc-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="2babc-1694">Le nœud contient un CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="2babc-1695">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="2babc-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="2babc-1696">Le nœud contient un CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="2babc-1697">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="2babc-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="2babc-1698">Le nœud contient un CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="2babc-1699">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="2babc-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="2babc-1700">Le nœud contient un CNodeRestriction sur lequel une expression de correspondance doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="2babc-1701">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="2babc-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="2babc-1702">Le nœud contient un CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="2babc-1703">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="2babc-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="2babc-1704">Le nœud contient un CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="2babc-1705">**Weight**: entier non signé 32 bits représentant le poids du nœud.</span><span class="sxs-lookup"><span data-stu-id="2babc-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="2babc-1706">Weight indique l’importance du nœud par rapport aux autres nœuds de l’arborescence de commandes de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="2babc-1707">Les valeurs de pondération supérieure sont plus importantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="2babc-1708">**Restriction**: type de restriction pour le nœud de l’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="2babc-1709">La syntaxe doit être la même que celle indiquée par le \_ champ ulType.</span><span class="sxs-lookup"><span data-stu-id="2babc-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="2babc-1710">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="2babc-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="2babc-1711">La structure CColumnSet spécifie les numéros de colonne à retourner.</span><span class="sxs-lookup"><span data-stu-id="2babc-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="2babc-1712">Cette structure est toujours utilisée en référence à une structure CPidMapper spécifique (section 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="2babc-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="2babc-1713">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1713">0</span></span>

<span data-ttu-id="2babc-1714">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1714">1</span></span>

<span data-ttu-id="2babc-1715">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1715">2</span></span>

<span data-ttu-id="2babc-1716">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1716">3</span></span>

<span data-ttu-id="2babc-1717">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1717">4</span></span>

<span data-ttu-id="2babc-1718">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1718">5</span></span>

<span data-ttu-id="2babc-1719">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1719">6</span></span>

<span data-ttu-id="2babc-1720">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1720">7</span></span>

<span data-ttu-id="2babc-1721">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1721">8</span></span>

<span data-ttu-id="2babc-1722">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1722">9</span></span>

<span data-ttu-id="2babc-1723">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1723">1</span></span><br/> <span data-ttu-id="2babc-1724">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1724">0</span></span><br/>

<span data-ttu-id="2babc-1725">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1725">1</span></span>

<span data-ttu-id="2babc-1726">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1726">2</span></span>

<span data-ttu-id="2babc-1727">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1727">3</span></span>

<span data-ttu-id="2babc-1728">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1728">4</span></span>

<span data-ttu-id="2babc-1729">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1729">5</span></span>

<span data-ttu-id="2babc-1730">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1730">6</span></span>

<span data-ttu-id="2babc-1731">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1731">7</span></span>

<span data-ttu-id="2babc-1732">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1732">8</span></span>

<span data-ttu-id="2babc-1733">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1733">9</span></span>

<span data-ttu-id="2babc-1734">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1734">2</span></span><br/> <span data-ttu-id="2babc-1735">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1735">0</span></span><br/>

<span data-ttu-id="2babc-1736">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1736">1</span></span>

<span data-ttu-id="2babc-1737">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1737">2</span></span>

<span data-ttu-id="2babc-1738">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1738">3</span></span>

<span data-ttu-id="2babc-1739">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1739">4</span></span>

<span data-ttu-id="2babc-1740">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1740">5</span></span>

<span data-ttu-id="2babc-1741">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1741">6</span></span>

<span data-ttu-id="2babc-1742">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1742">7</span></span>

<span data-ttu-id="2babc-1743">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1743">8</span></span>

<span data-ttu-id="2babc-1744">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1744">9</span></span>

<span data-ttu-id="2babc-1745">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1745">3</span></span><br/> <span data-ttu-id="2babc-1746">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1746">0</span></span><br/>

<span data-ttu-id="2babc-1747">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1747">1</span></span>

<span data-ttu-id="2babc-1748">count</span><span class="sxs-lookup"><span data-stu-id="2babc-1748">count</span></span>

<span data-ttu-id="2babc-1749">index (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1749">indexes (variable)</span></span>



 

<span data-ttu-id="2babc-1750">**Count**: entier non signé 32 bits spécifiant le nombre d’éléments dans le tableau d’index.</span><span class="sxs-lookup"><span data-stu-id="2babc-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="2babc-1751">**index**: tableau d’entiers non signés de 4 octets représentant les index de base zéro dans le tableau aPropSpec de la structure CPidMapper correspondante.</span><span class="sxs-lookup"><span data-stu-id="2babc-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="2babc-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="2babc-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="2babc-1753">La structure CCategorizationSet contient des informations sur le regroupement d’un jeu de résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="2babc-1754">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1754">0</span></span>

<span data-ttu-id="2babc-1755">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1755">1</span></span>

<span data-ttu-id="2babc-1756">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1756">2</span></span>

<span data-ttu-id="2babc-1757">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1757">3</span></span>

<span data-ttu-id="2babc-1758">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1758">4</span></span>

<span data-ttu-id="2babc-1759">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1759">5</span></span>

<span data-ttu-id="2babc-1760">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1760">6</span></span>

<span data-ttu-id="2babc-1761">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1761">7</span></span>

<span data-ttu-id="2babc-1762">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1762">8</span></span>

<span data-ttu-id="2babc-1763">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1763">9</span></span>

<span data-ttu-id="2babc-1764">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1764">1</span></span><br/> <span data-ttu-id="2babc-1765">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1765">0</span></span><br/>

<span data-ttu-id="2babc-1766">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1766">1</span></span>

<span data-ttu-id="2babc-1767">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1767">2</span></span>

<span data-ttu-id="2babc-1768">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1768">3</span></span>

<span data-ttu-id="2babc-1769">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1769">4</span></span>

<span data-ttu-id="2babc-1770">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1770">5</span></span>

<span data-ttu-id="2babc-1771">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1771">6</span></span>

<span data-ttu-id="2babc-1772">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1772">7</span></span>

<span data-ttu-id="2babc-1773">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1773">8</span></span>

<span data-ttu-id="2babc-1774">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1774">9</span></span>

<span data-ttu-id="2babc-1775">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1775">2</span></span><br/> <span data-ttu-id="2babc-1776">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1776">0</span></span><br/>

<span data-ttu-id="2babc-1777">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1777">1</span></span>

<span data-ttu-id="2babc-1778">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1778">2</span></span>

<span data-ttu-id="2babc-1779">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1779">3</span></span>

<span data-ttu-id="2babc-1780">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1780">4</span></span>

<span data-ttu-id="2babc-1781">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1781">5</span></span>

<span data-ttu-id="2babc-1782">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1782">6</span></span>

<span data-ttu-id="2babc-1783">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1783">7</span></span>

<span data-ttu-id="2babc-1784">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1784">8</span></span>

<span data-ttu-id="2babc-1785">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1785">9</span></span>

<span data-ttu-id="2babc-1786">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1786">3</span></span><br/> <span data-ttu-id="2babc-1787">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1787">0</span></span><br/>

<span data-ttu-id="2babc-1788">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1788">1</span></span>

<span data-ttu-id="2babc-1789">count</span><span class="sxs-lookup"><span data-stu-id="2babc-1789">count</span></span>

<span data-ttu-id="2babc-1790">catégories (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1790">categories (variable)</span></span>



 

<span data-ttu-id="2babc-1791">**Count**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau des catégories.</span><span class="sxs-lookup"><span data-stu-id="2babc-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="2babc-1792">**categories**: tableau de structures CCategorizationSpec spécifiant le regroupement de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="2babc-1793">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="2babc-1794">La structure CCategorizationSpec contient un regroupement pour un jeu de résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="2babc-1795">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1795">0</span></span>

<span data-ttu-id="2babc-1796">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1796">1</span></span>

<span data-ttu-id="2babc-1797">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1797">2</span></span>

<span data-ttu-id="2babc-1798">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1798">3</span></span>

<span data-ttu-id="2babc-1799">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1799">4</span></span>

<span data-ttu-id="2babc-1800">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1800">5</span></span>

<span data-ttu-id="2babc-1801">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1801">6</span></span>

<span data-ttu-id="2babc-1802">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1802">7</span></span>

<span data-ttu-id="2babc-1803">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1803">8</span></span>

<span data-ttu-id="2babc-1804">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1804">9</span></span>

<span data-ttu-id="2babc-1805">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1805">1</span></span><br/> <span data-ttu-id="2babc-1806">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1806">0</span></span><br/>

<span data-ttu-id="2babc-1807">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1807">1</span></span>

<span data-ttu-id="2babc-1808">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1808">2</span></span>

<span data-ttu-id="2babc-1809">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1809">3</span></span>

<span data-ttu-id="2babc-1810">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1810">4</span></span>

<span data-ttu-id="2babc-1811">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1811">5</span></span>

<span data-ttu-id="2babc-1812">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1812">6</span></span>

<span data-ttu-id="2babc-1813">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1813">7</span></span>

<span data-ttu-id="2babc-1814">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1814">8</span></span>

<span data-ttu-id="2babc-1815">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1815">9</span></span>

<span data-ttu-id="2babc-1816">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1816">2</span></span><br/> <span data-ttu-id="2babc-1817">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1817">0</span></span><br/>

<span data-ttu-id="2babc-1818">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1818">1</span></span>

<span data-ttu-id="2babc-1819">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1819">2</span></span>

<span data-ttu-id="2babc-1820">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1820">3</span></span>

<span data-ttu-id="2babc-1821">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1821">4</span></span>

<span data-ttu-id="2babc-1822">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1822">5</span></span>

<span data-ttu-id="2babc-1823">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1823">6</span></span>

<span data-ttu-id="2babc-1824">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1824">7</span></span>

<span data-ttu-id="2babc-1825">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1825">8</span></span>

<span data-ttu-id="2babc-1826">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1826">9</span></span>

<span data-ttu-id="2babc-1827">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1827">3</span></span><br/> <span data-ttu-id="2babc-1828">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1828">0</span></span><br/>

<span data-ttu-id="2babc-1829">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1829">1</span></span>

<span data-ttu-id="2babc-1830">\_csColumns (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="2babc-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="2babc-1831">\_ulCategType</span></span>



 

<span data-ttu-id="2babc-1832">**\_ csColumns**: structure CColumnSet indiquant les colonnes selon lesquelles regrouper la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="2babc-1833">**\_ ulCategType**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-1834">DOIT être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="2babc-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="2babc-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="2babc-1836">La structure CDbColId contient une colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="2babc-1837">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1837">0</span></span>

<span data-ttu-id="2babc-1838">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1838">1</span></span>

<span data-ttu-id="2babc-1839">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1839">2</span></span>

<span data-ttu-id="2babc-1840">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1840">3</span></span>

<span data-ttu-id="2babc-1841">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1841">4</span></span>

<span data-ttu-id="2babc-1842">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1842">5</span></span>

<span data-ttu-id="2babc-1843">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1843">6</span></span>

<span data-ttu-id="2babc-1844">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1844">7</span></span>

<span data-ttu-id="2babc-1845">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1845">8</span></span>

<span data-ttu-id="2babc-1846">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1846">9</span></span>

<span data-ttu-id="2babc-1847">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1847">1</span></span><br/> <span data-ttu-id="2babc-1848">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1848">0</span></span><br/>

<span data-ttu-id="2babc-1849">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1849">1</span></span>

<span data-ttu-id="2babc-1850">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1850">2</span></span>

<span data-ttu-id="2babc-1851">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1851">3</span></span>

<span data-ttu-id="2babc-1852">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1852">4</span></span>

<span data-ttu-id="2babc-1853">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1853">5</span></span>

<span data-ttu-id="2babc-1854">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1854">6</span></span>

<span data-ttu-id="2babc-1855">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1855">7</span></span>

<span data-ttu-id="2babc-1856">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1856">8</span></span>

<span data-ttu-id="2babc-1857">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1857">9</span></span>

<span data-ttu-id="2babc-1858">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1858">2</span></span><br/> <span data-ttu-id="2babc-1859">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1859">0</span></span><br/>

<span data-ttu-id="2babc-1860">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1860">1</span></span>

<span data-ttu-id="2babc-1861">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1861">2</span></span>

<span data-ttu-id="2babc-1862">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1862">3</span></span>

<span data-ttu-id="2babc-1863">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1863">4</span></span>

<span data-ttu-id="2babc-1864">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1864">5</span></span>

<span data-ttu-id="2babc-1865">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1865">6</span></span>

<span data-ttu-id="2babc-1866">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1866">7</span></span>

<span data-ttu-id="2babc-1867">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1867">8</span></span>

<span data-ttu-id="2babc-1868">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1868">9</span></span>

<span data-ttu-id="2babc-1869">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1869">3</span></span><br/> <span data-ttu-id="2babc-1870">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1870">0</span></span><br/>

<span data-ttu-id="2babc-1871">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1871">1</span></span>

<span data-ttu-id="2babc-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="2babc-1872">eKind</span></span>

<span data-ttu-id="2babc-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="2babc-1873">GUID</span></span>

<span data-ttu-id="2babc-1874">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1874">...</span></span>

<span data-ttu-id="2babc-1875">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1875">...</span></span>

<span data-ttu-id="2babc-1876">...</span><span class="sxs-lookup"><span data-stu-id="2babc-1876">...</span></span>

<span data-ttu-id="2babc-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="2babc-1877">ulId</span></span>

<span data-ttu-id="2babc-1878">vString (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1878">vString (variable)</span></span>



 

<span data-ttu-id="2babc-1879">**eKind**: doit être défini sur l’une des valeurs ci-dessous qui indique le contenu de GUID et vValue.</span><span class="sxs-lookup"><span data-stu-id="2babc-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="2babc-1880">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1880">Value</span></span>                            | <span data-ttu-id="2babc-1881">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1882">\_Nom GUID \_ 0x00000000 DBKIND</span><span class="sxs-lookup"><span data-stu-id="2babc-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="2babc-1883">vString contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="2babc-1884">\_GUID DBKIND \_ propid 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="2babc-1885">ulId contient un entier de 4 octets indiquant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="2babc-1886">Nom de DBKIND \_ PGUID \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="2babc-1887">vString contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1887">vString contains a property name.</span></span> <span data-ttu-id="2babc-1888">Cette valeur doit être traitée de la même façon que le \_ nom GUID DBKIND \_ .</span><span class="sxs-lookup"><span data-stu-id="2babc-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="2babc-1889">DBKIND \_ PGUID \_ propid 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="2babc-1890">ulId contient un entier de 4 octets indiquant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="2babc-1891">Cette valeur doit être identique à DBKIND \_ GUID \_ propid.</span><span class="sxs-lookup"><span data-stu-id="2babc-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="2babc-1892">**GUID**: le GUID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="2babc-1893">**ulId**: si EKIND est DBKIND \_ GUID \_ propid ou DBKIND \_ PGUID \_ propId, ce champ contient un entier non signé, en spécifiant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="2babc-1894">Si eKind est \_ \_ un nom GUID DBKIND ou \_ \_ un nom DBKIND PGUID, ce champ contient un entier non signé spécifiant le nombre de caractères Unicode contenus dans le champ vString.</span><span class="sxs-lookup"><span data-stu-id="2babc-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="2babc-1895">**vString**: chaîne Unicode qui se termine par un caractère non null représentant le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="2babc-1896">Elle doit être omise sauf si le champ eKind est défini sur DBKIND \_ GUID \_ Name ou DBKIND \_ PGUID \_ Name.</span><span class="sxs-lookup"><span data-stu-id="2babc-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="2babc-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="2babc-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="2babc-1898">La structure CDbProp contient une propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="2babc-1899">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1899">0</span></span>

<span data-ttu-id="2babc-1900">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1900">1</span></span>

<span data-ttu-id="2babc-1901">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1901">2</span></span>

<span data-ttu-id="2babc-1902">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1902">3</span></span>

<span data-ttu-id="2babc-1903">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1903">4</span></span>

<span data-ttu-id="2babc-1904">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1904">5</span></span>

<span data-ttu-id="2babc-1905">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1905">6</span></span>

<span data-ttu-id="2babc-1906">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1906">7</span></span>

<span data-ttu-id="2babc-1907">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1907">8</span></span>

<span data-ttu-id="2babc-1908">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1908">9</span></span>

<span data-ttu-id="2babc-1909">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1909">1</span></span><br/> <span data-ttu-id="2babc-1910">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1910">0</span></span><br/>

<span data-ttu-id="2babc-1911">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1911">1</span></span>

<span data-ttu-id="2babc-1912">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1912">2</span></span>

<span data-ttu-id="2babc-1913">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1913">3</span></span>

<span data-ttu-id="2babc-1914">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1914">4</span></span>

<span data-ttu-id="2babc-1915">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1915">5</span></span>

<span data-ttu-id="2babc-1916">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1916">6</span></span>

<span data-ttu-id="2babc-1917">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1917">7</span></span>

<span data-ttu-id="2babc-1918">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1918">8</span></span>

<span data-ttu-id="2babc-1919">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1919">9</span></span>

<span data-ttu-id="2babc-1920">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1920">2</span></span><br/> <span data-ttu-id="2babc-1921">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1921">0</span></span><br/>

<span data-ttu-id="2babc-1922">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1922">1</span></span>

<span data-ttu-id="2babc-1923">2</span><span class="sxs-lookup"><span data-stu-id="2babc-1923">2</span></span>

<span data-ttu-id="2babc-1924">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1924">3</span></span>

<span data-ttu-id="2babc-1925">4</span><span class="sxs-lookup"><span data-stu-id="2babc-1925">4</span></span>

<span data-ttu-id="2babc-1926">5</span><span class="sxs-lookup"><span data-stu-id="2babc-1926">5</span></span>

<span data-ttu-id="2babc-1927">6</span><span class="sxs-lookup"><span data-stu-id="2babc-1927">6</span></span>

<span data-ttu-id="2babc-1928">7</span><span class="sxs-lookup"><span data-stu-id="2babc-1928">7</span></span>

<span data-ttu-id="2babc-1929">8</span><span class="sxs-lookup"><span data-stu-id="2babc-1929">8</span></span>

<span data-ttu-id="2babc-1930">9</span><span class="sxs-lookup"><span data-stu-id="2babc-1930">9</span></span>

<span data-ttu-id="2babc-1931">3</span><span class="sxs-lookup"><span data-stu-id="2babc-1931">3</span></span><br/> <span data-ttu-id="2babc-1932">0</span><span class="sxs-lookup"><span data-stu-id="2babc-1932">0</span></span><br/>

<span data-ttu-id="2babc-1933">1</span><span class="sxs-lookup"><span data-stu-id="2babc-1933">1</span></span>

<span data-ttu-id="2babc-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="2babc-1934">DBPROPID</span></span>

<span data-ttu-id="2babc-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="2babc-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="2babc-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="2babc-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="2babc-1937">colid (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1937">colid (variable)</span></span>

<span data-ttu-id="2babc-1938">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-1938">vValue (variable)</span></span>



 

<span data-ttu-id="2babc-1939">**DBPROPID**: entier non signé 32 bits indiquant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="2babc-1940">**DBPROPOPTIONS** : doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="2babc-1941">**DBPROPSTATUS**: doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="2babc-1942">**colid**: une structure CDbColId, comme indiqué dans la section 2.2.1.20, indiquant la colonne à laquelle la propriété s’applique.</span><span class="sxs-lookup"><span data-stu-id="2babc-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="2babc-1943">**vValue**: CBaseStorageVariant contenant la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="2babc-1944">Propriétés 2.2.1.21.1</span><span class="sxs-lookup"><span data-stu-id="2babc-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="2babc-1945">Cette section détaille les propriétés utilisées par CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="2babc-1946">Ces propriétés sont regroupées en trois jeux de propriétés, ident 2.2.1.21.1 ified dans le champ guidPropertySet de la structure CDbPropSet (section 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="2babc-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="2babc-1947">Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés DBPROPSET FSCIFRMWRK \_ ext.</span><span class="sxs-lookup"><span data-stu-id="2babc-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="2babc-1948">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1948">Value</span></span>                                  | <span data-ttu-id="2babc-1949">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1950">\_Nom de \_ catalogue ci DBPROP \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="2babc-1951">Spécifie le nom du catalogue ou des catalogues à interroger.</span><span class="sxs-lookup"><span data-stu-id="2babc-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="2babc-1952">La valeur doit être un \_ LPWStr VT ou un \_ LPWStr VT Vector \| VT \_</span><span class="sxs-lookup"><span data-stu-id="2babc-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="2babc-1953">DBPROP \_ ci \_ inclut des \_ étendues 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="2babc-1954">Spécifie un ou plusieurs chemins d’accès à inclure dans la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="2babc-1955">La valeur doit être un \_ LPWStr VT ou un \_ LPWStr VT Vector \| VT \_ .</span><span class="sxs-lookup"><span data-stu-id="2babc-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="2babc-1956">Indicateurs d’étendue de l’élément de configuration DBPROP \_ \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="2babc-1957">Spécifie comment les chemins d’accès spécifiés par la \_ propriété DBPROP ci \_ include \_ scope doivent être traités.</span><span class="sxs-lookup"><span data-stu-id="2babc-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="2babc-1958">La valeur doit être un \_ I4 VT ou un \_ vecteur VT VT \| \_ I4.</span><span class="sxs-lookup"><span data-stu-id="2babc-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="2babc-1959">DBPROP \_ \_ type de requête ci \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="2babc-1960">Spécifie le type de requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-1960">Specifies the type of query.</span></span> <span data-ttu-id="2babc-1961">CDbColId doit être défini sur DB \_ NULLID.</span><span class="sxs-lookup"><span data-stu-id="2babc-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="2babc-1962">Le tableau suivant répertorie les indicateurs pour la \_ propriété indicateurs d’étendue d’DBPROP ci \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="2babc-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="2babc-1963">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1963">Value</span></span>                     | <span data-ttu-id="2babc-1964">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1965">REQUÊTE \_ complète 0x01</span><span class="sxs-lookup"><span data-stu-id="2babc-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="2babc-1966">Si cette valeur est définie, cela indique que les fichiers dans le répertoire d’étendue et tous les sous-répertoires sont inclus dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="2babc-1967">Si cette case est désactivée, seuls les fichiers du répertoire d’étendue sont inclus dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="2babc-1968">NE doit pas être combiné avec une requête \_ profonde.</span><span class="sxs-lookup"><span data-stu-id="2babc-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="2babc-1969">\_ \_ Chemin d’accès virtuel de requête 0x02</span><span class="sxs-lookup"><span data-stu-id="2babc-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="2babc-1970">S’il est défini, indique que l’étendue est un chemin d’accès virtuel.</span><span class="sxs-lookup"><span data-stu-id="2babc-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="2babc-1971">Si cette case est désactivée, cela indique que l’étendue est un répertoire physique.</span><span class="sxs-lookup"><span data-stu-id="2babc-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="2babc-1972">Le tableau suivant répertorie les types de requêtes pour \_ la \_ propriété type de requête DBPROP ci \_ :</span><span class="sxs-lookup"><span data-stu-id="2babc-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="2babc-1973">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1973">Value</span></span>                     | <span data-ttu-id="2babc-1974">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1975">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="2babc-1976">Requête normale.</span><span class="sxs-lookup"><span data-stu-id="2babc-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="2babc-1977">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="2babc-1978">La requête demande une liste des racines virtuelles du catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="2babc-1979">Cette valeur requiert des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="2babc-1980">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="2babc-1981">La requête demande une liste de toutes les propriétés prises en charge par le service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="2babc-1982">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="2babc-1983">La requête est une opération d’administration.</span><span class="sxs-lookup"><span data-stu-id="2babc-1983">The query is an administrative operation.</span></span> <span data-ttu-id="2babc-1984">Cette valeur requiert des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2babc-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="2babc-1985">Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés QUERYEXT DBPROPSET.</span><span class="sxs-lookup"><span data-stu-id="2babc-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="2babc-1986">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-1986">Value</span></span>                                      | <span data-ttu-id="2babc-1987">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-1988">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="2babc-1989">Spécifie la manière dont le service d’indexation gère les requêtes lentes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="2babc-1990">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="2babc-1991">Si la valeur est TRUE, le serveur est autorisé à faire échouer ces requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="2babc-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="2babc-1993">Indique si le service d’indexation doit effectuer la suppression des résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="2babc-1994">Si la valeur est TRUE, le serveur doit envisager d’effectuer une suppression des résultats de manière à optimiser le temps de réponse pour le client.</span><span class="sxs-lookup"><span data-stu-id="2babc-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="2babc-1995">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="2babc-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="2babc-1997">Indique si le client prend en charge les \_ types de données vectorielles VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="2babc-1998">Si la valeur est TRUE, le client prend en charge VT \_ Vector ; si la valeur est false, le serveur doit convertir les \_ types de données de Vector VT en \_ types de données de tableau VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="2babc-1999">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="2babc-2000">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="2babc-2001">Indique que les lignes correspondent à retourner.</span><span class="sxs-lookup"><span data-stu-id="2babc-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="2babc-2002">Si la valeur est TRUE, le serveur doit retourner le premier ensemble de lignes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="2babc-2003">Si la valeur est FALSe, les lignes les plus pertinentes doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="2babc-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="2babc-2004">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="2babc-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="2babc-2005">Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés DBPROPSET CIFRMWRKCORE \_ ext.</span><span class="sxs-lookup"><span data-stu-id="2babc-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="2babc-2006">Valeur/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="2babc-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="2babc-2007">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-2008">\_Ordinateur DBPROP 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="2babc-2009">Spécifie le nom du ou des ordinateurs sur lesquels une requête doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="2babc-2010">La valeur doit être VT \_ BSTR ou VT \_ array \| VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="2babc-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="2babc-2011">DBPROP \_ client \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="2babc-2012">Spécifie une constante de connexion pour le service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="2babc-2013">La valeur doit être un \_ CLSID VT contenant 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="2babc-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="2babc-2014">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="2babc-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="2babc-2015">La structure CDbPropSet contient un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="2babc-2016">Notez que le premier champ est de taille fixe, mais peut ne pas être aligné sur un décalage qui est un multiple de 4 octets à partir du début du message contenant cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="2babc-2017">Toutefois, le champ cProperties est aligné en tant que tel, et le format est donc représenté comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="2babc-2018">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2018">0</span></span>

<span data-ttu-id="2babc-2019">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2019">1</span></span>

<span data-ttu-id="2babc-2020">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2020">2</span></span>

<span data-ttu-id="2babc-2021">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2021">3</span></span>

<span data-ttu-id="2babc-2022">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2022">4</span></span>

<span data-ttu-id="2babc-2023">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2023">5</span></span>

<span data-ttu-id="2babc-2024">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2024">6</span></span>

<span data-ttu-id="2babc-2025">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2025">7</span></span>

<span data-ttu-id="2babc-2026">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2026">8</span></span>

<span data-ttu-id="2babc-2027">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2027">9</span></span>

<span data-ttu-id="2babc-2028">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2028">1</span></span><br/> <span data-ttu-id="2babc-2029">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2029">0</span></span><br/>

<span data-ttu-id="2babc-2030">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2030">1</span></span>

<span data-ttu-id="2babc-2031">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2031">2</span></span>

<span data-ttu-id="2babc-2032">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2032">3</span></span>

<span data-ttu-id="2babc-2033">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2033">4</span></span>

<span data-ttu-id="2babc-2034">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2034">5</span></span>

<span data-ttu-id="2babc-2035">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2035">6</span></span>

<span data-ttu-id="2babc-2036">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2036">7</span></span>

<span data-ttu-id="2babc-2037">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2037">8</span></span>

<span data-ttu-id="2babc-2038">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2038">9</span></span>

<span data-ttu-id="2babc-2039">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2039">2</span></span><br/> <span data-ttu-id="2babc-2040">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2040">0</span></span><br/>

<span data-ttu-id="2babc-2041">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2041">1</span></span>

<span data-ttu-id="2babc-2042">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2042">2</span></span>

<span data-ttu-id="2babc-2043">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2043">3</span></span>

<span data-ttu-id="2babc-2044">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2044">4</span></span>

<span data-ttu-id="2babc-2045">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2045">5</span></span>

<span data-ttu-id="2babc-2046">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2046">6</span></span>

<span data-ttu-id="2babc-2047">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2047">7</span></span>

<span data-ttu-id="2babc-2048">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2048">8</span></span>

<span data-ttu-id="2babc-2049">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2049">9</span></span>

<span data-ttu-id="2babc-2050">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2050">3</span></span><br/> <span data-ttu-id="2babc-2051">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2051">0</span></span><br/>

<span data-ttu-id="2babc-2052">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2052">1</span></span>

<span data-ttu-id="2babc-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="2babc-2053">guidPropertySet</span></span>

<span data-ttu-id="2babc-2054">...</span><span class="sxs-lookup"><span data-stu-id="2babc-2054">...</span></span>

<span data-ttu-id="2babc-2055">...</span><span class="sxs-lookup"><span data-stu-id="2babc-2055">...</span></span>

<span data-ttu-id="2babc-2056">...</span><span class="sxs-lookup"><span data-stu-id="2babc-2056">...</span></span>

<span data-ttu-id="2babc-2057">...</span><span class="sxs-lookup"><span data-stu-id="2babc-2057">...</span></span>

<span data-ttu-id="2babc-2058">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-2058">\_padding (variable)</span></span>

<span data-ttu-id="2babc-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="2babc-2059">cProperties</span></span>

<span data-ttu-id="2babc-2060">aProps (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-2060">aProps (variable)</span></span>



 

<span data-ttu-id="2babc-2061">**guidPropertySet**: GUID identifiant le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="2babc-2062">DOIT être défini sur la forme binaire correspondant à l’une des valeurs suivantes (affichées sous forme de représentation sous forme de chaîne), identifiant le jeu de propriétés des propriétés contenues dans le champ aProps.</span><span class="sxs-lookup"><span data-stu-id="2babc-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="2babc-2063">Valeur/GUID</span><span class="sxs-lookup"><span data-stu-id="2babc-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="2babc-2064">Name</span><span class="sxs-lookup"><span data-stu-id="2babc-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="2babc-2065">DBPROPSET \_ FSCIFRMWRK \_ ext</span><span class="sxs-lookup"><span data-stu-id="2babc-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="2babc-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="2babc-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="2babc-2067">Jeu de propriétés de l’infrastructure d’index de contenu du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="2babc-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="2babc-2068">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="2babc-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="2babc-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="2babc-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="2babc-2070">Jeu de propriétés d’extension de requête</span><span class="sxs-lookup"><span data-stu-id="2babc-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="2babc-2071">DBPROPSET \_ CIFRMWRKCORE \_ ext</span><span class="sxs-lookup"><span data-stu-id="2babc-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="2babc-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="2babc-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="2babc-2073">Jeu de propriétés principales de l’infrastructure d’index de contenu</span><span class="sxs-lookup"><span data-stu-id="2babc-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="2babc-2074">**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="2babc-2075">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="2babc-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="2babc-2076">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="2babc-2077">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-2078">**cProperties**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau aProps.</span><span class="sxs-lookup"><span data-stu-id="2babc-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="2babc-2079">**aProps**: tableau de structures CDbProp, tel que spécifié dans la section 0, contenant les propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="2babc-2080">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient ce tableau.</span><span class="sxs-lookup"><span data-stu-id="2babc-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="2babc-2081">Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="2babc-2082">Le contenu des octets de remplissage doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="2babc-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="2babc-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="2babc-2084">La structure CPidMapper contient un tableau d’ID de propriété spécifiant les propriétés à retourner dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="2babc-2085">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2085">0</span></span>

<span data-ttu-id="2babc-2086">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2086">1</span></span>

<span data-ttu-id="2babc-2087">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2087">2</span></span>

<span data-ttu-id="2babc-2088">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2088">3</span></span>

<span data-ttu-id="2babc-2089">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2089">4</span></span>

<span data-ttu-id="2babc-2090">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2090">5</span></span>

<span data-ttu-id="2babc-2091">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2091">6</span></span>

<span data-ttu-id="2babc-2092">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2092">7</span></span>

<span data-ttu-id="2babc-2093">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2093">8</span></span>

<span data-ttu-id="2babc-2094">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2094">9</span></span>

<span data-ttu-id="2babc-2095">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2095">1</span></span><br/> <span data-ttu-id="2babc-2096">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2096">0</span></span><br/>

<span data-ttu-id="2babc-2097">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2097">1</span></span>

<span data-ttu-id="2babc-2098">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2098">2</span></span>

<span data-ttu-id="2babc-2099">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2099">3</span></span>

<span data-ttu-id="2babc-2100">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2100">4</span></span>

<span data-ttu-id="2babc-2101">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2101">5</span></span>

<span data-ttu-id="2babc-2102">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2102">6</span></span>

<span data-ttu-id="2babc-2103">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2103">7</span></span>

<span data-ttu-id="2babc-2104">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2104">8</span></span>

<span data-ttu-id="2babc-2105">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2105">9</span></span>

<span data-ttu-id="2babc-2106">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2106">2</span></span><br/> <span data-ttu-id="2babc-2107">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2107">0</span></span><br/>

<span data-ttu-id="2babc-2108">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2108">1</span></span>

<span data-ttu-id="2babc-2109">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2109">2</span></span>

<span data-ttu-id="2babc-2110">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2110">3</span></span>

<span data-ttu-id="2babc-2111">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2111">4</span></span>

<span data-ttu-id="2babc-2112">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2112">5</span></span>

<span data-ttu-id="2babc-2113">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2113">6</span></span>

<span data-ttu-id="2babc-2114">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2114">7</span></span>

<span data-ttu-id="2babc-2115">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2115">8</span></span>

<span data-ttu-id="2babc-2116">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2116">9</span></span>

<span data-ttu-id="2babc-2117">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2117">3</span></span><br/> <span data-ttu-id="2babc-2118">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2118">0</span></span><br/>

<span data-ttu-id="2babc-2119">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2119">1</span></span>

<span data-ttu-id="2babc-2120">count</span><span class="sxs-lookup"><span data-stu-id="2babc-2120">count</span></span>

<span data-ttu-id="2babc-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-2121">aPropSpec</span></span>

<span data-ttu-id="2babc-2122">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-2122">... (variable)</span></span>



 

<span data-ttu-id="2babc-2123">**Count**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="2babc-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="2babc-2124">**aPropSpec**: tableau de structures CFullPropSpec indiquant les propriétés à retourner.</span><span class="sxs-lookup"><span data-stu-id="2babc-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="2babc-2125">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="2babc-2126">Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.</span><span class="sxs-lookup"><span data-stu-id="2babc-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="2babc-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="2babc-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="2babc-2128">La structure CRowSeekAt contient le décalage à partir duquel récupérer des lignes dans un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="2babc-2129">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2129">0</span></span>

<span data-ttu-id="2babc-2130">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2130">1</span></span>

<span data-ttu-id="2babc-2131">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2131">2</span></span>

<span data-ttu-id="2babc-2132">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2132">3</span></span>

<span data-ttu-id="2babc-2133">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2133">4</span></span>

<span data-ttu-id="2babc-2134">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2134">5</span></span>

<span data-ttu-id="2babc-2135">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2135">6</span></span>

<span data-ttu-id="2babc-2136">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2136">7</span></span>

<span data-ttu-id="2babc-2137">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2137">8</span></span>

<span data-ttu-id="2babc-2138">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2138">9</span></span>

<span data-ttu-id="2babc-2139">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2139">1</span></span><br/> <span data-ttu-id="2babc-2140">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2140">0</span></span><br/>

<span data-ttu-id="2babc-2141">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2141">1</span></span>

<span data-ttu-id="2babc-2142">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2142">2</span></span>

<span data-ttu-id="2babc-2143">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2143">3</span></span>

<span data-ttu-id="2babc-2144">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2144">4</span></span>

<span data-ttu-id="2babc-2145">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2145">5</span></span>

<span data-ttu-id="2babc-2146">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2146">6</span></span>

<span data-ttu-id="2babc-2147">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2147">7</span></span>

<span data-ttu-id="2babc-2148">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2148">8</span></span>

<span data-ttu-id="2babc-2149">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2149">9</span></span>

<span data-ttu-id="2babc-2150">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2150">2</span></span><br/> <span data-ttu-id="2babc-2151">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2151">0</span></span><br/>

<span data-ttu-id="2babc-2152">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2152">1</span></span>

<span data-ttu-id="2babc-2153">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2153">2</span></span>

<span data-ttu-id="2babc-2154">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2154">3</span></span>

<span data-ttu-id="2babc-2155">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2155">4</span></span>

<span data-ttu-id="2babc-2156">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2156">5</span></span>

<span data-ttu-id="2babc-2157">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2157">6</span></span>

<span data-ttu-id="2babc-2158">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2158">7</span></span>

<span data-ttu-id="2babc-2159">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2159">8</span></span>

<span data-ttu-id="2babc-2160">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2160">9</span></span>

<span data-ttu-id="2babc-2161">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2161">3</span></span><br/> <span data-ttu-id="2babc-2162">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2162">0</span></span><br/>

<span data-ttu-id="2babc-2163">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2163">1</span></span>

<span data-ttu-id="2babc-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="2babc-2164">\_hRegion</span></span>

<span data-ttu-id="2babc-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="2babc-2165">\_cskip</span></span>

<span data-ttu-id="2babc-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="2babc-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="2babc-2167">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2babc-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="2babc-2168">**\_ cskip**: entier non signé 32 bits contenant le nombre de lignes à ignorer dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="2babc-2169">**\_ bmkOffset**: valeur 32 bits représentant le handle du **signet** indiquant la position de départ à partir de laquelle ignorer le nombre de lignes spécifié dans \_ cskip, avant de commencer la récupération.</span><span class="sxs-lookup"><span data-stu-id="2babc-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="2babc-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="2babc-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="2babc-2171">La structure CRowSeekAtRatio identifie le point à partir duquel commencer la récupération d’un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="2babc-2172">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2172">0</span></span>

<span data-ttu-id="2babc-2173">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2173">1</span></span>

<span data-ttu-id="2babc-2174">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2174">2</span></span>

<span data-ttu-id="2babc-2175">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2175">3</span></span>

<span data-ttu-id="2babc-2176">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2176">4</span></span>

<span data-ttu-id="2babc-2177">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2177">5</span></span>

<span data-ttu-id="2babc-2178">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2178">6</span></span>

<span data-ttu-id="2babc-2179">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2179">7</span></span>

<span data-ttu-id="2babc-2180">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2180">8</span></span>

<span data-ttu-id="2babc-2181">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2181">9</span></span>

<span data-ttu-id="2babc-2182">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2182">1</span></span><br/> <span data-ttu-id="2babc-2183">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2183">0</span></span><br/>

<span data-ttu-id="2babc-2184">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2184">1</span></span>

<span data-ttu-id="2babc-2185">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2185">2</span></span>

<span data-ttu-id="2babc-2186">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2186">3</span></span>

<span data-ttu-id="2babc-2187">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2187">4</span></span>

<span data-ttu-id="2babc-2188">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2188">5</span></span>

<span data-ttu-id="2babc-2189">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2189">6</span></span>

<span data-ttu-id="2babc-2190">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2190">7</span></span>

<span data-ttu-id="2babc-2191">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2191">8</span></span>

<span data-ttu-id="2babc-2192">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2192">9</span></span>

<span data-ttu-id="2babc-2193">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2193">2</span></span><br/> <span data-ttu-id="2babc-2194">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2194">0</span></span><br/>

<span data-ttu-id="2babc-2195">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2195">1</span></span>

<span data-ttu-id="2babc-2196">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2196">2</span></span>

<span data-ttu-id="2babc-2197">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2197">3</span></span>

<span data-ttu-id="2babc-2198">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2198">4</span></span>

<span data-ttu-id="2babc-2199">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2199">5</span></span>

<span data-ttu-id="2babc-2200">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2200">6</span></span>

<span data-ttu-id="2babc-2201">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2201">7</span></span>

<span data-ttu-id="2babc-2202">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2202">8</span></span>

<span data-ttu-id="2babc-2203">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2203">9</span></span>

<span data-ttu-id="2babc-2204">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2204">3</span></span><br/> <span data-ttu-id="2babc-2205">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2205">0</span></span><br/>

<span data-ttu-id="2babc-2206">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2206">1</span></span>

<span data-ttu-id="2babc-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="2babc-2207">CiTblChapt</span></span>

<span data-ttu-id="2babc-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="2babc-2208">\_hRegion</span></span>

<span data-ttu-id="2babc-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="2babc-2209">\_ulNumerator</span></span>

<span data-ttu-id="2babc-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="2babc-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="2babc-2211">**CiTblChapt**: entier non signé 32 bits indiquant le chapitre de l’ensemble de lignes à partir duquel récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="2babc-2212">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2babc-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="2babc-2213">**\_ ulNumerator**: entier 32 bits non signé représentant le numérateur du rapport entre les lignes du chapitre et le début de la récupération.</span><span class="sxs-lookup"><span data-stu-id="2babc-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="2babc-2214">**\_ ulDenominator**: entier 32 bits non signé représentant le dénominateur du rapport entre les lignes du chapitre et le début de la récupération.</span><span class="sxs-lookup"><span data-stu-id="2babc-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="2babc-2215">DOIT être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="2babc-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="2babc-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="2babc-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="2babc-2217">La structure CRowSeekByBookmark identifie les signets à partir desquels commencer la récupération de lignes pour un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="2babc-2218">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2218">0</span></span>

<span data-ttu-id="2babc-2219">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2219">1</span></span>

<span data-ttu-id="2babc-2220">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2220">2</span></span>

<span data-ttu-id="2babc-2221">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2221">3</span></span>

<span data-ttu-id="2babc-2222">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2222">4</span></span>

<span data-ttu-id="2babc-2223">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2223">5</span></span>

<span data-ttu-id="2babc-2224">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2224">6</span></span>

<span data-ttu-id="2babc-2225">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2225">7</span></span>

<span data-ttu-id="2babc-2226">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2226">8</span></span>

<span data-ttu-id="2babc-2227">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2227">9</span></span>

<span data-ttu-id="2babc-2228">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2228">1</span></span><br/> <span data-ttu-id="2babc-2229">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2229">0</span></span><br/>

<span data-ttu-id="2babc-2230">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2230">1</span></span>

<span data-ttu-id="2babc-2231">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2231">2</span></span>

<span data-ttu-id="2babc-2232">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2232">3</span></span>

<span data-ttu-id="2babc-2233">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2233">4</span></span>

<span data-ttu-id="2babc-2234">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2234">5</span></span>

<span data-ttu-id="2babc-2235">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2235">6</span></span>

<span data-ttu-id="2babc-2236">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2236">7</span></span>

<span data-ttu-id="2babc-2237">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2237">8</span></span>

<span data-ttu-id="2babc-2238">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2238">9</span></span>

<span data-ttu-id="2babc-2239">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2239">2</span></span><br/> <span data-ttu-id="2babc-2240">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2240">0</span></span><br/>

<span data-ttu-id="2babc-2241">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2241">1</span></span>

<span data-ttu-id="2babc-2242">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2242">2</span></span>

<span data-ttu-id="2babc-2243">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2243">3</span></span>

<span data-ttu-id="2babc-2244">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2244">4</span></span>

<span data-ttu-id="2babc-2245">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2245">5</span></span>

<span data-ttu-id="2babc-2246">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2246">6</span></span>

<span data-ttu-id="2babc-2247">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2247">7</span></span>

<span data-ttu-id="2babc-2248">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2248">8</span></span>

<span data-ttu-id="2babc-2249">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2249">9</span></span>

<span data-ttu-id="2babc-2250">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2250">3</span></span><br/> <span data-ttu-id="2babc-2251">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2251">0</span></span><br/>

<span data-ttu-id="2babc-2252">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2252">1</span></span>

<span data-ttu-id="2babc-2253">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="2babc-2253">\_hRegion</span></span>

<span data-ttu-id="2babc-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="2babc-2254">\_cBookmarks</span></span>

<span data-ttu-id="2babc-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="2babc-2255">\_maxRet</span></span>

<span data-ttu-id="2babc-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="2babc-2256">\_cValidRet</span></span>

<span data-ttu-id="2babc-2257">\_aBookmarks (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="2babc-2258">\_ascRet (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="2babc-2259">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2babc-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="2babc-2260">**\_ cBookmarks**: entier 32 bits non signé représentant le nombre d’éléments dans le \_ tableau aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="2babc-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="2babc-2261">**\_ maxRet**: entier 32 bits non signé représentant le nombre d’éléments dans le \_ tableau ascRet.</span><span class="sxs-lookup"><span data-stu-id="2babc-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="2babc-2262">**\_ cValidRet**: entier non signé 32 bits représentant le nombre d’éléments dans le \_ tableau ascRet qui sont valides.</span><span class="sxs-lookup"><span data-stu-id="2babc-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="2babc-2263">Des éléments valides ont été définis dans le tableau, alors que les éléments non valides ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="2babc-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="2babc-2264">**\_ aBookmarks**: tableau de handles de signet (chacun représenté par 4 octets), obtenu à partir d’un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="2babc-2265">**\_ ascRet**: tableau de valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2babc-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="2babc-2266">Lorsque le CRowSeekByBookMark est envoyé dans le cadre de la demande CPMGetRowsIn, le nombre d’entrées dans le tableau doit être égal à \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="2babc-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="2babc-2267">Lorsqu’il est envoyé par le client, les valeurs doivent être égales à zéro, et le serveur doit ignorer le contenu du tableau.</span><span class="sxs-lookup"><span data-stu-id="2babc-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="2babc-2268">Lorsqu’il est envoyé par le serveur (dans le cadre du message CPMGetRowsOut), les valeurs du tableau indiquent l’état du résultat pour chaque extraction de ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="2babc-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="2babc-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="2babc-2270">La structure CRowSeekNext contient le nombre de lignes à ignorer dans un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="2babc-2271">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2271">0</span></span>

<span data-ttu-id="2babc-2272">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2272">1</span></span>

<span data-ttu-id="2babc-2273">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2273">2</span></span>

<span data-ttu-id="2babc-2274">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2274">3</span></span>

<span data-ttu-id="2babc-2275">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2275">4</span></span>

<span data-ttu-id="2babc-2276">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2276">5</span></span>

<span data-ttu-id="2babc-2277">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2277">6</span></span>

<span data-ttu-id="2babc-2278">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2278">7</span></span>

<span data-ttu-id="2babc-2279">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2279">8</span></span>

<span data-ttu-id="2babc-2280">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2280">9</span></span>

<span data-ttu-id="2babc-2281">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2281">1</span></span><br/> <span data-ttu-id="2babc-2282">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2282">0</span></span><br/>

<span data-ttu-id="2babc-2283">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2283">1</span></span>

<span data-ttu-id="2babc-2284">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2284">2</span></span>

<span data-ttu-id="2babc-2285">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2285">3</span></span>

<span data-ttu-id="2babc-2286">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2286">4</span></span>

<span data-ttu-id="2babc-2287">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2287">5</span></span>

<span data-ttu-id="2babc-2288">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2288">6</span></span>

<span data-ttu-id="2babc-2289">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2289">7</span></span>

<span data-ttu-id="2babc-2290">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2290">8</span></span>

<span data-ttu-id="2babc-2291">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2291">9</span></span>

<span data-ttu-id="2babc-2292">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2292">2</span></span><br/> <span data-ttu-id="2babc-2293">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2293">0</span></span><br/>

<span data-ttu-id="2babc-2294">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2294">1</span></span>

<span data-ttu-id="2babc-2295">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2295">2</span></span>

<span data-ttu-id="2babc-2296">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2296">3</span></span>

<span data-ttu-id="2babc-2297">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2297">4</span></span>

<span data-ttu-id="2babc-2298">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2298">5</span></span>

<span data-ttu-id="2babc-2299">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2299">6</span></span>

<span data-ttu-id="2babc-2300">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2300">7</span></span>

<span data-ttu-id="2babc-2301">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2301">8</span></span>

<span data-ttu-id="2babc-2302">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2302">9</span></span>

<span data-ttu-id="2babc-2303">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2303">3</span></span><br/> <span data-ttu-id="2babc-2304">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2304">0</span></span><br/>

<span data-ttu-id="2babc-2305">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2305">1</span></span>

<span data-ttu-id="2babc-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="2babc-2306">CiTblChapt</span></span>

<span data-ttu-id="2babc-2307">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="2babc-2307">\_hRegion</span></span>

<span data-ttu-id="2babc-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="2babc-2308">\_cskip</span></span>



 

<span data-ttu-id="2babc-2309">**CiTblChapt**: entier 32 bits non signé spécifiant le chapitre de l’ensemble de lignes à partir duquel récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="2babc-2310">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2babc-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="2babc-2311">**\_ cskip**: entier 32 bits non signé représentant le nombre de lignes à ignorer dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="2babc-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="2babc-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="2babc-2313">La structure CRowsetProperties contient des informations de configuration pour une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="2babc-2314">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2314">0</span></span>

<span data-ttu-id="2babc-2315">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2315">1</span></span>

<span data-ttu-id="2babc-2316">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2316">2</span></span>

<span data-ttu-id="2babc-2317">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2317">3</span></span>

<span data-ttu-id="2babc-2318">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2318">4</span></span>

<span data-ttu-id="2babc-2319">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2319">5</span></span>

<span data-ttu-id="2babc-2320">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2320">6</span></span>

<span data-ttu-id="2babc-2321">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2321">7</span></span>

<span data-ttu-id="2babc-2322">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2322">8</span></span>

<span data-ttu-id="2babc-2323">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2323">9</span></span>

<span data-ttu-id="2babc-2324">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2324">1</span></span><br/> <span data-ttu-id="2babc-2325">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2325">0</span></span><br/>

<span data-ttu-id="2babc-2326">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2326">1</span></span>

<span data-ttu-id="2babc-2327">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2327">2</span></span>

<span data-ttu-id="2babc-2328">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2328">3</span></span>

<span data-ttu-id="2babc-2329">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2329">4</span></span>

<span data-ttu-id="2babc-2330">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2330">5</span></span>

<span data-ttu-id="2babc-2331">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2331">6</span></span>

<span data-ttu-id="2babc-2332">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2332">7</span></span>

<span data-ttu-id="2babc-2333">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2333">8</span></span>

<span data-ttu-id="2babc-2334">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2334">9</span></span>

<span data-ttu-id="2babc-2335">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2335">2</span></span><br/> <span data-ttu-id="2babc-2336">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2336">0</span></span><br/>

<span data-ttu-id="2babc-2337">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2337">1</span></span>

<span data-ttu-id="2babc-2338">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2338">2</span></span>

<span data-ttu-id="2babc-2339">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2339">3</span></span>

<span data-ttu-id="2babc-2340">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2340">4</span></span>

<span data-ttu-id="2babc-2341">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2341">5</span></span>

<span data-ttu-id="2babc-2342">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2342">6</span></span>

<span data-ttu-id="2babc-2343">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2343">7</span></span>

<span data-ttu-id="2babc-2344">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2344">8</span></span>

<span data-ttu-id="2babc-2345">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2345">9</span></span>

<span data-ttu-id="2babc-2346">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2346">3</span></span><br/> <span data-ttu-id="2babc-2347">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2347">0</span></span><br/>

<span data-ttu-id="2babc-2348">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2348">1</span></span>

<span data-ttu-id="2babc-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="2babc-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="2babc-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="2babc-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="2babc-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="2babc-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="2babc-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="2babc-2352">\_cMaxResults</span></span>

<span data-ttu-id="2babc-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="2babc-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="2babc-2354">**\_ uBooleanOptions**: les 3 bits les moins significatifs de ce champ doivent contenir l’une des trois valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="2babc-2355">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-2355">Value</span></span>                  | <span data-ttu-id="2babc-2356">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2babc-2357">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="2babc-2358">Le curseur peut être déplacé uniquement vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="2babc-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="2babc-2359">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="2babc-2360">Le curseur peut être déplacé vers n’importe quelle position.</span><span class="sxs-lookup"><span data-stu-id="2babc-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="2babc-2361">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="2babc-2362">Le curseur peut être déplacé vers n’importe quelle position et extraction dans n’importe quelle direction.</span><span class="sxs-lookup"><span data-stu-id="2babc-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="2babc-2363">Les bits restants peuvent être clairs ou définis sur une combinaison des valeurs suivantes logiquement ou ensemble :</span><span class="sxs-lookup"><span data-stu-id="2babc-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="2babc-2364">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-2364">Value</span></span>                     | <span data-ttu-id="2babc-2365">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-2366">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="2babc-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="2babc-2367">Le client n’attend pas la fin de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2babc-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="2babc-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="2babc-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="2babc-2369">Retourne les premières lignes rencontrées, pas les meilleures correspondances.</span><span class="sxs-lookup"><span data-stu-id="2babc-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="2babc-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="2babc-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="2babc-2371">Le serveur ne doit pas ignorer les lignes tant que le client n’est pas terminé par une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="2babc-2372">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="2babc-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="2babc-2373">L’ensemble de lignes prend en charge les chapitres.</span><span class="sxs-lookup"><span data-stu-id="2babc-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="2babc-2374">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="2babc-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="2babc-2375">Répondez uniquement à la requête à partir de l’index, et non du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2babc-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="2babc-2376">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="2babc-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="2babc-2377">Le service d’indexation doit envisager d’optimiser le temps de réponse du client lors de la suppression des résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="2babc-2378">**\_ ulMaxOpenRows**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="2babc-2379">Doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="2babc-2380">Non utilisé et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2babc-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="2babc-2381">**\_ ulMemoryUsage**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="2babc-2382">Doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="2babc-2383">Non utilisé et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2babc-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="2babc-2384">**\_ cMaxResults**: entier non signé 32 bits spécifiant le nombre maximal de lignes à retourner pour la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="2babc-2385">**\_ cCmdTimeout**: entier non signé 32 bits, qui spécifie le nombre de secondes au terme duquel une requête expire et se termine automatiquement, en comptant à partir du moment où la requête commence à s’exécuter sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="2babc-2386">La valeur 0x00000000 signifie que la requête n’expire pas.</span><span class="sxs-lookup"><span data-stu-id="2babc-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="2babc-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="2babc-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="2babc-2388">La structure CRowVariant contient la partie de taille fixe d’un type de données de longueur variable stockée dans le message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="2babc-2389">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2389">0</span></span>

<span data-ttu-id="2babc-2390">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2390">1</span></span>

<span data-ttu-id="2babc-2391">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2391">2</span></span>

<span data-ttu-id="2babc-2392">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2392">3</span></span>

<span data-ttu-id="2babc-2393">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2393">4</span></span>

<span data-ttu-id="2babc-2394">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2394">5</span></span>

<span data-ttu-id="2babc-2395">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2395">6</span></span>

<span data-ttu-id="2babc-2396">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2396">7</span></span>

<span data-ttu-id="2babc-2397">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2397">8</span></span>

<span data-ttu-id="2babc-2398">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2398">9</span></span>

<span data-ttu-id="2babc-2399">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2399">1</span></span><br/> <span data-ttu-id="2babc-2400">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2400">0</span></span><br/>

<span data-ttu-id="2babc-2401">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2401">1</span></span>

<span data-ttu-id="2babc-2402">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2402">2</span></span>

<span data-ttu-id="2babc-2403">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2403">3</span></span>

<span data-ttu-id="2babc-2404">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2404">4</span></span>

<span data-ttu-id="2babc-2405">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2405">5</span></span>

<span data-ttu-id="2babc-2406">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2406">6</span></span>

<span data-ttu-id="2babc-2407">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2407">7</span></span>

<span data-ttu-id="2babc-2408">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2408">8</span></span>

<span data-ttu-id="2babc-2409">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2409">9</span></span>

<span data-ttu-id="2babc-2410">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2410">2</span></span><br/> <span data-ttu-id="2babc-2411">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2411">0</span></span><br/>

<span data-ttu-id="2babc-2412">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2412">1</span></span>

<span data-ttu-id="2babc-2413">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2413">2</span></span>

<span data-ttu-id="2babc-2414">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2414">3</span></span>

<span data-ttu-id="2babc-2415">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2415">4</span></span>

<span data-ttu-id="2babc-2416">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2416">5</span></span>

<span data-ttu-id="2babc-2417">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2417">6</span></span>

<span data-ttu-id="2babc-2418">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2418">7</span></span>

<span data-ttu-id="2babc-2419">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2419">8</span></span>

<span data-ttu-id="2babc-2420">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2420">9</span></span>

<span data-ttu-id="2babc-2421">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2421">3</span></span><br/> <span data-ttu-id="2babc-2422">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2422">0</span></span><br/>

<span data-ttu-id="2babc-2423">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2423">1</span></span>

<span data-ttu-id="2babc-2424">vType</span><span class="sxs-lookup"><span data-stu-id="2babc-2424">vType</span></span>

<span data-ttu-id="2babc-2425">Reserved1</span><span class="sxs-lookup"><span data-stu-id="2babc-2425">reserved1</span></span>

<span data-ttu-id="2babc-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="2babc-2426">reserved2</span></span>

<span data-ttu-id="2babc-2427">Offset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2427">Offset (optional)</span></span>



 

<span data-ttu-id="2babc-2428">**vType**: indicateur de type indiquant le type de vValue.</span><span class="sxs-lookup"><span data-stu-id="2babc-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="2babc-2429">Il doit s’agir de l’une des valeurs VARENUM spécifiées dans la section 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="2babc-2430">**Reserved1**: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2babc-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="2babc-2431">La valeur peut être définie sur n’importe quelle valeur arbitraire et doit être ignorée lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="2babc-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="2babc-2432">**Reserved2**: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2babc-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="2babc-2433">La valeur peut être définie sur n’importe quelle valeur arbitraire et doit être ignorée lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="2babc-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="2babc-2434">**Offset**: décalage des données de longueur variable (par exemple, une chaîne).</span><span class="sxs-lookup"><span data-stu-id="2babc-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="2babc-2435">Il doit s’agir d’une valeur 32 bits (4 octets de long) si les décalages 32 bits sont utilisés (conformément aux règles de la section 2.2.3.16) ou d’une valeur de 64 octets (8 octets de long) si les décalages de 64 bits sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="2babc-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="2babc-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="2babc-2437">La structure CSortSet contient l’ordre de tri de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="2babc-2438">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2438">0</span></span>

<span data-ttu-id="2babc-2439">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2439">1</span></span>

<span data-ttu-id="2babc-2440">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2440">2</span></span>

<span data-ttu-id="2babc-2441">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2441">3</span></span>

<span data-ttu-id="2babc-2442">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2442">4</span></span>

<span data-ttu-id="2babc-2443">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2443">5</span></span>

<span data-ttu-id="2babc-2444">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2444">6</span></span>

<span data-ttu-id="2babc-2445">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2445">7</span></span>

<span data-ttu-id="2babc-2446">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2446">8</span></span>

<span data-ttu-id="2babc-2447">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2447">9</span></span>

<span data-ttu-id="2babc-2448">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2448">1</span></span><br/> <span data-ttu-id="2babc-2449">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2449">0</span></span><br/>

<span data-ttu-id="2babc-2450">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2450">1</span></span>

<span data-ttu-id="2babc-2451">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2451">2</span></span>

<span data-ttu-id="2babc-2452">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2452">3</span></span>

<span data-ttu-id="2babc-2453">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2453">4</span></span>

<span data-ttu-id="2babc-2454">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2454">5</span></span>

<span data-ttu-id="2babc-2455">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2455">6</span></span>

<span data-ttu-id="2babc-2456">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2456">7</span></span>

<span data-ttu-id="2babc-2457">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2457">8</span></span>

<span data-ttu-id="2babc-2458">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2458">9</span></span>

<span data-ttu-id="2babc-2459">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2459">2</span></span><br/> <span data-ttu-id="2babc-2460">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2460">0</span></span><br/>

<span data-ttu-id="2babc-2461">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2461">1</span></span>

<span data-ttu-id="2babc-2462">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2462">2</span></span>

<span data-ttu-id="2babc-2463">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2463">3</span></span>

<span data-ttu-id="2babc-2464">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2464">4</span></span>

<span data-ttu-id="2babc-2465">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2465">5</span></span>

<span data-ttu-id="2babc-2466">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2466">6</span></span>

<span data-ttu-id="2babc-2467">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2467">7</span></span>

<span data-ttu-id="2babc-2468">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2468">8</span></span>

<span data-ttu-id="2babc-2469">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2469">9</span></span>

<span data-ttu-id="2babc-2470">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2470">3</span></span><br/> <span data-ttu-id="2babc-2471">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2471">0</span></span><br/>

<span data-ttu-id="2babc-2472">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2472">1</span></span>

<span data-ttu-id="2babc-2473">Count</span><span class="sxs-lookup"><span data-stu-id="2babc-2473">Count</span></span>

<span data-ttu-id="2babc-2474">sortArray (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="2babc-2475">**Count**: entier non signé 32 bits spécifiant le nombre d’éléments dans sortArray.</span><span class="sxs-lookup"><span data-stu-id="2babc-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="2babc-2476">**sortArray**: tableau de structures CSort décrivant l’ordre dans lequel trier les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="2babc-2477">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="2babc-2478">Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.</span><span class="sxs-lookup"><span data-stu-id="2babc-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="2babc-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="2babc-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="2babc-2480">La structure CTableColumn contient une colonne d’un message CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="2babc-2481">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2481">0</span></span>

<span data-ttu-id="2babc-2482">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2482">1</span></span>

<span data-ttu-id="2babc-2483">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2483">2</span></span>

<span data-ttu-id="2babc-2484">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2484">3</span></span>

<span data-ttu-id="2babc-2485">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2485">4</span></span>

<span data-ttu-id="2babc-2486">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2486">5</span></span>

<span data-ttu-id="2babc-2487">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2487">6</span></span>

<span data-ttu-id="2babc-2488">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2488">7</span></span>

<span data-ttu-id="2babc-2489">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2489">8</span></span>

<span data-ttu-id="2babc-2490">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2490">9</span></span>

<span data-ttu-id="2babc-2491">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2491">1</span></span><br/> <span data-ttu-id="2babc-2492">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2492">0</span></span><br/>

<span data-ttu-id="2babc-2493">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2493">1</span></span>

<span data-ttu-id="2babc-2494">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2494">2</span></span>

<span data-ttu-id="2babc-2495">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2495">3</span></span>

<span data-ttu-id="2babc-2496">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2496">4</span></span>

<span data-ttu-id="2babc-2497">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2497">5</span></span>

<span data-ttu-id="2babc-2498">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2498">6</span></span>

<span data-ttu-id="2babc-2499">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2499">7</span></span>

<span data-ttu-id="2babc-2500">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2500">8</span></span>

<span data-ttu-id="2babc-2501">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2501">9</span></span>

<span data-ttu-id="2babc-2502">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2502">2</span></span><br/> <span data-ttu-id="2babc-2503">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2503">0</span></span><br/>

<span data-ttu-id="2babc-2504">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2504">1</span></span>

<span data-ttu-id="2babc-2505">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2505">2</span></span>

<span data-ttu-id="2babc-2506">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2506">3</span></span>

<span data-ttu-id="2babc-2507">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2507">4</span></span>

<span data-ttu-id="2babc-2508">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2508">5</span></span>

<span data-ttu-id="2babc-2509">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2509">6</span></span>

<span data-ttu-id="2babc-2510">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2510">7</span></span>

<span data-ttu-id="2babc-2511">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2511">8</span></span>

<span data-ttu-id="2babc-2512">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2512">9</span></span>

<span data-ttu-id="2babc-2513">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2513">3</span></span><br/> <span data-ttu-id="2babc-2514">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2514">0</span></span><br/>

<span data-ttu-id="2babc-2515">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2515">1</span></span>

<span data-ttu-id="2babc-2516">PropSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-2516">PropSpec</span></span>

<span data-ttu-id="2babc-2517">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-2517">...(variable)</span></span>

<span data-ttu-id="2babc-2518">vType</span><span class="sxs-lookup"><span data-stu-id="2babc-2518">vType</span></span>

<span data-ttu-id="2babc-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="2babc-2519">ValueUsed</span></span>

<span data-ttu-id="2babc-2520">\_padding1 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="2babc-2521">ValueOffset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="2babc-2522">Value (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2522">ValueSize (optional)</span></span>

<span data-ttu-id="2babc-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="2babc-2523">StatusUsed</span></span>

<span data-ttu-id="2babc-2524">\_padding2 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="2babc-2525">StatusOffset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="2babc-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="2babc-2526">LengthUsed</span></span>

<span data-ttu-id="2babc-2527">\_padding3 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="2babc-2528">LengthOffset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="2babc-2529">**PropSpec**: structure CFullPropSpec telle que spécifiée dans la section 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="2babc-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="2babc-2530">**vType**: spécifie le type de valeur de données contenu dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="2babc-2531">Consultez le champ vType de la section 2.2.1.1 pour obtenir la liste des valeurs de ce champ.</span><span class="sxs-lookup"><span data-stu-id="2babc-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="2babc-2532">**ValueUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="2babc-2533">Si la valeur est 0x01, la colonne est transférée dans la ligne de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="2babc-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="2babc-2534">Si la valeur est 0x00, la valeur de la colonne est transférée dans la section de longueur variable à la fin de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2babc-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="2babc-2535">**\_ padding1**: un champ d’un octet qui doit être inséré avant ValueOffset si, sans lui, ValueOffset ne commence pas à un décalage pair à partir du début du message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="2babc-2536">La valeur de cet octet est arbitraire et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="2babc-2537">Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="2babc-2538">**ValueOffset**: entier non signé de 2 octets spécifiant le décalage de la valeur de colonne dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="2babc-2539">Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="2babc-2540">**Value**: entier non signé de 2 octets spécifiant la taille de la colonne en octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="2babc-2541">Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="2babc-2542">**StatusUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="2babc-2543">Si la valeur est 0x01, l’état de la colonne est transféré dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="2babc-2544">Si 0x00, l’état de la colonne n’est pas transféré dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="2babc-2545">**\_ padding2**: un champ d’un octet qui doit être inséré avant StatusOffset si, sans lui, le champ StatusOffset ne commence pas à un décalage pair à partir du début du message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="2babc-2546">La valeur de cet octet est arbitraire et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="2babc-2547">Si StatusUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="2babc-2548">**StatusOffset**: entier non signé de 2 octets spécifiant le décalage de l’état de la colonne dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="2babc-2549">Si StatusUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="2babc-2550">**LengthUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="2babc-2551">Si la valeur est 0x01, la longueur de la colonne est transférée dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="2babc-2552">Si 0x00, la longueur de la colonne ne doit pas être transférée dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="2babc-2553">**\_ padding3**: un champ d’un octet qui doit être inséré avant LengthOffset si, sans lui, LengthOffset ne commence pas à un décalage pair à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="2babc-2554">La valeur de cet octet est arbitraire et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="2babc-2555">Si LengthUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="2babc-2556">**LengthOffset**: entier non signé de 2 octets spécifiant le décalage de la longueur de colonne dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="2babc-2557">Si LengthUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="2babc-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="2babc-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="2babc-2559">La structure SERIALIZEDPROPERTYVALUE contient une valeur sérialisée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="2babc-2560">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2560">0</span></span>

<span data-ttu-id="2babc-2561">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2561">1</span></span>

<span data-ttu-id="2babc-2562">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2562">2</span></span>

<span data-ttu-id="2babc-2563">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2563">3</span></span>

<span data-ttu-id="2babc-2564">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2564">4</span></span>

<span data-ttu-id="2babc-2565">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2565">5</span></span>

<span data-ttu-id="2babc-2566">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2566">6</span></span>

<span data-ttu-id="2babc-2567">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2567">7</span></span>

<span data-ttu-id="2babc-2568">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2568">8</span></span>

<span data-ttu-id="2babc-2569">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2569">9</span></span>

<span data-ttu-id="2babc-2570">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2570">1</span></span><br/> <span data-ttu-id="2babc-2571">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2571">0</span></span><br/>

<span data-ttu-id="2babc-2572">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2572">1</span></span>

<span data-ttu-id="2babc-2573">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2573">2</span></span>

<span data-ttu-id="2babc-2574">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2574">3</span></span>

<span data-ttu-id="2babc-2575">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2575">4</span></span>

<span data-ttu-id="2babc-2576">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2576">5</span></span>

<span data-ttu-id="2babc-2577">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2577">6</span></span>

<span data-ttu-id="2babc-2578">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2578">7</span></span>

<span data-ttu-id="2babc-2579">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2579">8</span></span>

<span data-ttu-id="2babc-2580">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2580">9</span></span>

<span data-ttu-id="2babc-2581">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2581">2</span></span><br/> <span data-ttu-id="2babc-2582">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2582">0</span></span><br/>

<span data-ttu-id="2babc-2583">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2583">1</span></span>

<span data-ttu-id="2babc-2584">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2584">2</span></span>

<span data-ttu-id="2babc-2585">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2585">3</span></span>

<span data-ttu-id="2babc-2586">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2586">4</span></span>

<span data-ttu-id="2babc-2587">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2587">5</span></span>

<span data-ttu-id="2babc-2588">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2588">6</span></span>

<span data-ttu-id="2babc-2589">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2589">7</span></span>

<span data-ttu-id="2babc-2590">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2590">8</span></span>

<span data-ttu-id="2babc-2591">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2591">9</span></span>

<span data-ttu-id="2babc-2592">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2592">3</span></span><br/> <span data-ttu-id="2babc-2593">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2593">0</span></span><br/>

<span data-ttu-id="2babc-2594">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2594">1</span></span>

<span data-ttu-id="2babc-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="2babc-2595">dwType</span></span>

<span data-ttu-id="2babc-2596">RGB (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-2596">rgb (variable)</span></span>



 

<span data-ttu-id="2babc-2597">**dwType**: l’un des types variant, défini dans la section 2.2.1.1, qui peut être combiné avec des modificateurs de type Variant.</span><span class="sxs-lookup"><span data-stu-id="2babc-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="2babc-2598">Pour tous les types variant, à l’exception de ceux associés à VT \_ Array, SERIALIZEDPROPERTYVALUE a la même disposition que CBaseStorageVariant, comme indiqué dans la section 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="2babc-2599">Si le type Variant est combiné avec le \_ modificateur de type tableau VT, SAFEARRAY2, spécifié dans la section 2.2.1.2.1.1, est utilisé à la place de SAFEARRAY dans le champ vValue de CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="2babc-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="2babc-2600">**RGB**: valeur sérialisée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="2babc-2601">Consultez les détails de la sérialisation pour vValue dans 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="2babc-2602">2.2.2 en-têtes de message</span><span class="sxs-lookup"><span data-stu-id="2babc-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="2babc-2603">Tous les messages du protocole de service d’indexation de contenu ont un en-tête de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="2babc-2604">Vous trouverez ci-dessous un diagramme montrant le format d’en-tête de message du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="2babc-2605">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2605">0</span></span>

<span data-ttu-id="2babc-2606">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2606">1</span></span>

<span data-ttu-id="2babc-2607">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2607">2</span></span>

<span data-ttu-id="2babc-2608">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2608">3</span></span>

<span data-ttu-id="2babc-2609">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2609">4</span></span>

<span data-ttu-id="2babc-2610">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2610">5</span></span>

<span data-ttu-id="2babc-2611">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2611">6</span></span>

<span data-ttu-id="2babc-2612">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2612">7</span></span>

<span data-ttu-id="2babc-2613">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2613">8</span></span>

<span data-ttu-id="2babc-2614">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2614">9</span></span>

<span data-ttu-id="2babc-2615">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2615">1</span></span><br/> <span data-ttu-id="2babc-2616">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2616">0</span></span><br/>

<span data-ttu-id="2babc-2617">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2617">1</span></span>

<span data-ttu-id="2babc-2618">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2618">2</span></span>

<span data-ttu-id="2babc-2619">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2619">3</span></span>

<span data-ttu-id="2babc-2620">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2620">4</span></span>

<span data-ttu-id="2babc-2621">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2621">5</span></span>

<span data-ttu-id="2babc-2622">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2622">6</span></span>

<span data-ttu-id="2babc-2623">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2623">7</span></span>

<span data-ttu-id="2babc-2624">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2624">8</span></span>

<span data-ttu-id="2babc-2625">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2625">9</span></span>

<span data-ttu-id="2babc-2626">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2626">2</span></span><br/> <span data-ttu-id="2babc-2627">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2627">0</span></span><br/>

<span data-ttu-id="2babc-2628">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2628">1</span></span>

<span data-ttu-id="2babc-2629">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2629">2</span></span>

<span data-ttu-id="2babc-2630">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2630">3</span></span>

<span data-ttu-id="2babc-2631">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2631">4</span></span>

<span data-ttu-id="2babc-2632">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2632">5</span></span>

<span data-ttu-id="2babc-2633">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2633">6</span></span>

<span data-ttu-id="2babc-2634">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2634">7</span></span>

<span data-ttu-id="2babc-2635">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2635">8</span></span>

<span data-ttu-id="2babc-2636">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2636">9</span></span>

<span data-ttu-id="2babc-2637">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2637">3</span></span><br/> <span data-ttu-id="2babc-2638">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2638">0</span></span><br/>

<span data-ttu-id="2babc-2639">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2639">1</span></span>

<span data-ttu-id="2babc-2640">\_fragment</span><span class="sxs-lookup"><span data-stu-id="2babc-2640">\_msg</span></span>

<span data-ttu-id="2babc-2641">\_statu</span><span class="sxs-lookup"><span data-stu-id="2babc-2641">\_status</span></span>

<span data-ttu-id="2babc-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="2babc-2642">\_ulChecksum</span></span>

<span data-ttu-id="2babc-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="2babc-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="2babc-2644">\_**MSG**: entier 32 bits qui identifie le type de message suivant l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="2babc-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="2babc-2645">Le tableau suivant répertorie les messages du protocole du service d’indexation de contenu et les valeurs entières spécifiées pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="2babc-2646">Comme indiqué dans le tableau, certaines valeurs identifient 2 messages dans la table.</span><span class="sxs-lookup"><span data-stu-id="2babc-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="2babc-2647">Dans ces instances, le message qui suit l’en-tête peut être identifié par la direction du message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="2babc-2648">Si la direction est client à serveur, le message avec « in » ajouté au nom du message est indiqué.</span><span class="sxs-lookup"><span data-stu-id="2babc-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="2babc-2649">Si la direction est de serveur à client, le message « out » ajouté au nom du message est indiqué.</span><span class="sxs-lookup"><span data-stu-id="2babc-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="2babc-2650">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-2650">Value</span></span>      | <span data-ttu-id="2babc-2651">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="2babc-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="2babc-2652">0x000000C8</span></span> | <span data-ttu-id="2babc-2653">CPMConnectIn ou CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="2babc-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="2babc-2654">0x000000C9</span></span> | <span data-ttu-id="2babc-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="2babc-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="2babc-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="2babc-2656">0x000000CA</span></span> | <span data-ttu-id="2babc-2657">CPMCreateQueryIn ou CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="2babc-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="2babc-2658">0x000000CB</span></span> | <span data-ttu-id="2babc-2659">CPMFreeCursorIn ou CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="2babc-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="2babc-2660">0x000000CC</span></span> | <span data-ttu-id="2babc-2661">CPMGetRowsIn ou CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="2babc-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="2babc-2662">0x000000CD</span></span> | <span data-ttu-id="2babc-2663">CPMRatioFinishedIn ou CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="2babc-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="2babc-2664">0x000000CE</span></span> | <span data-ttu-id="2babc-2665">CPMCompareBmkIn ou CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="2babc-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="2babc-2666">0x000000CF</span></span> | <span data-ttu-id="2babc-2667">CPMGetApproximatePositionIn ou CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="2babc-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="2babc-2668">0x000000D0</span></span> | <span data-ttu-id="2babc-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="2babc-2670">Stop</span><span class="sxs-lookup"><span data-stu-id="2babc-2670">0x000000D1</span></span> | <span data-ttu-id="2babc-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="2babc-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="2babc-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="2babc-2672">0x000000D2</span></span> | <span data-ttu-id="2babc-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="2babc-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="2babc-2674">0x000000D7</span></span> | <span data-ttu-id="2babc-2675">CPMGetQueryStatusIn ou CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="2babc-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="2babc-2676">0x000000D9</span></span> | <span data-ttu-id="2babc-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="2babc-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="2babc-2678">0x000000E1</span></span> | <span data-ttu-id="2babc-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="2babc-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="2babc-2680">0x000000E4</span></span> | <span data-ttu-id="2babc-2681">CPMFetchValueIn ou CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="2babc-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="2babc-2682">0x000000E6</span></span> | <span data-ttu-id="2babc-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="2babc-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="2babc-2684">0x000000E7</span></span> | <span data-ttu-id="2babc-2685">CPMGetQueryStatusExIn ou PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="2babc-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="2babc-2686">0x000000E8</span></span> | <span data-ttu-id="2babc-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="2babc-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="2babc-2688">0x000000E9</span></span> | <span data-ttu-id="2babc-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="2babc-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="2babc-2690">0x000000EC</span></span> | <span data-ttu-id="2babc-2691">CPMSetCatStateIn ou CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="2babc-2692">\_**État**: HRESULT \[ ms-sys \] , indiquant l’état de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="2babc-2693">*Comportement de Windows : le client définit toujours le \_ champ d’État sur 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="2babc-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="2babc-2694">**\_ ulChecksum**: le \_ ulChecksum doit être calculé comme indiqué dans la section 3.2.4 pour les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="2babc-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="2babc-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="2babc-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="2babc-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="2babc-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="2babc-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="2babc-2700">Pour tous les autres messages, \_ ULCHECKSUM doit avoir la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="2babc-2701">Un client doit ignorer le \_ champ ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="2babc-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="2babc-2702">**\_ ulReserved2**: doit être défini sur 0 et ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="2babc-2703">2.2.3 messages</span><span class="sxs-lookup"><span data-stu-id="2babc-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="2babc-2704">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="2babc-2705">Le message CPMCiStateInOut contient des informations sur l’état du service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="2babc-2706">Le format du message CPMCiStateInOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-2707">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2707">0</span></span>

<span data-ttu-id="2babc-2708">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2708">1</span></span>

<span data-ttu-id="2babc-2709">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2709">2</span></span>

<span data-ttu-id="2babc-2710">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2710">3</span></span>

<span data-ttu-id="2babc-2711">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2711">4</span></span>

<span data-ttu-id="2babc-2712">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2712">5</span></span>

<span data-ttu-id="2babc-2713">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2713">6</span></span>

<span data-ttu-id="2babc-2714">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2714">7</span></span>

<span data-ttu-id="2babc-2715">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2715">8</span></span>

<span data-ttu-id="2babc-2716">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2716">9</span></span>

<span data-ttu-id="2babc-2717">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2717">1</span></span><br/> <span data-ttu-id="2babc-2718">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2718">0</span></span><br/>

<span data-ttu-id="2babc-2719">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2719">1</span></span>

<span data-ttu-id="2babc-2720">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2720">2</span></span>

<span data-ttu-id="2babc-2721">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2721">3</span></span>

<span data-ttu-id="2babc-2722">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2722">4</span></span>

<span data-ttu-id="2babc-2723">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2723">5</span></span>

<span data-ttu-id="2babc-2724">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2724">6</span></span>

<span data-ttu-id="2babc-2725">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2725">7</span></span>

<span data-ttu-id="2babc-2726">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2726">8</span></span>

<span data-ttu-id="2babc-2727">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2727">9</span></span>

<span data-ttu-id="2babc-2728">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2728">2</span></span><br/> <span data-ttu-id="2babc-2729">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2729">0</span></span><br/>

<span data-ttu-id="2babc-2730">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2730">1</span></span>

<span data-ttu-id="2babc-2731">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2731">2</span></span>

<span data-ttu-id="2babc-2732">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2732">3</span></span>

<span data-ttu-id="2babc-2733">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2733">4</span></span>

<span data-ttu-id="2babc-2734">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2734">5</span></span>

<span data-ttu-id="2babc-2735">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2735">6</span></span>

<span data-ttu-id="2babc-2736">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2736">7</span></span>

<span data-ttu-id="2babc-2737">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2737">8</span></span>

<span data-ttu-id="2babc-2738">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2738">9</span></span>

<span data-ttu-id="2babc-2739">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2739">3</span></span><br/> <span data-ttu-id="2babc-2740">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2740">0</span></span><br/>

<span data-ttu-id="2babc-2741">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2741">1</span></span>

<span data-ttu-id="2babc-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="2babc-2742">cbStruct</span></span>

<span data-ttu-id="2babc-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="2babc-2743">cWordList</span></span>

<span data-ttu-id="2babc-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="2babc-2744">cPersistentIndex</span></span>

<span data-ttu-id="2babc-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="2babc-2745">cQueries</span></span>

<span data-ttu-id="2babc-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="2babc-2746">cDocuments</span></span>

<span data-ttu-id="2babc-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="2babc-2747">cFreshTest</span></span>

<span data-ttu-id="2babc-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="2babc-2748">dwMergeProgress</span></span>

<span data-ttu-id="2babc-2749">Immobilier</span><span class="sxs-lookup"><span data-stu-id="2babc-2749">eState</span></span>

<span data-ttu-id="2babc-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="2babc-2750">cFilteredDocuments</span></span>

<span data-ttu-id="2babc-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="2babc-2751">cTotalDocuments</span></span>

<span data-ttu-id="2babc-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="2babc-2752">cPendingScans</span></span>

<span data-ttu-id="2babc-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="2babc-2753">dwIndexSize</span></span>

<span data-ttu-id="2babc-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="2babc-2754">cUniqueKeys</span></span>

<span data-ttu-id="2babc-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="2babc-2755">cSecQDocuments</span></span>

<span data-ttu-id="2babc-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="2babc-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="2babc-2757">**cbStruct**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="2babc-2758">Taille en octets de ce message (à l’exception de l’en-tête commun).</span><span class="sxs-lookup"><span data-stu-id="2babc-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="2babc-2759">DOIT être défini sur 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="2babc-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="2babc-2760">**cWordList**: entier non signé 32 bits indiquant le nombre d’index initiaux créés pour les documents récemment indexés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="2babc-2761">**cPersistentIndex**: entier non signé 32 bits indiquant le nombre d’index persistants.</span><span class="sxs-lookup"><span data-stu-id="2babc-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="2babc-2762">**cQueries**: entier non signé 32 bits indiquant un certain nombre de requêtes en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2babc-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="2babc-2763">**cDocuments**: entier non signé 32 bits indiquant le nombre total de documents en attente d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="2babc-2764">**cFreshTest**: entier non signé 32 bits indiquant le nombre de documents uniques avec les informations des index qui ne sont pas entièrement optimisés pour les performances.</span><span class="sxs-lookup"><span data-stu-id="2babc-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="2babc-2765">**dwMergeProgress**: entier 32 bits non signé spécifiant le pourcentage d’achèvement de l’optimisation complète actuelle des index, si l’optimisation est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="2babc-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="2babc-2766">DOIT être inférieur ou égal à 100.</span><span class="sxs-lookup"><span data-stu-id="2babc-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="2babc-2767">**patrimoine**: état de l’indexation du contenu comme indiqué par une ou plusieurs des \_ constantes d’état ci \_ \* définies dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2babc-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="2babc-2768">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-2768">Value</span></span>                                         | <span data-ttu-id="2babc-2769">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-2770">État de l’instantané de l' \_ état ci \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="2babc-2771">Le service d’indexation est en train d’optimiser certains des index afin de réduire l’utilisation de la mémoire et d’améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="2babc-2772">\_Fusion du maître d’état ci \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="2babc-2773">Le service d’indexation est en cours d’optimisation complète pour tous les index.</span><span class="sxs-lookup"><span data-stu-id="2babc-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2babc-2774">Analyse du contenu de l' \_ état ci \_ \_ \_ requise 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="2babc-2775">Certains documents de l’index ont changé et le service d’indexation doit déterminer ceux qui ont été ajoutés, modifiés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2babc-2776">État de l' \_ \_ opération de fusion recuite d’état ci \_</span><span class="sxs-lookup"><span data-stu-id="2babc-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="2babc-2777">Le service d’indexation est en train d’optimiser les index afin de réduire l’utilisation de la mémoire et d’améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="2babc-2778">Ce processus est plus complet que celui identifié par la valeur de \_ fusion de cliché instantané d’état ci \_ \_ , mais il n’est pas aussi complet que spécifié par la \_ valeur de fusion du maître d’état ci \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2babc-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="2babc-2779">Ces optimisations sont spécifiques à l’implémentation, car elles dépendent de la façon dont les données sont stockées en interne. les optimisations n’affectent pas le protocole de la même façon que le temps de réponse.</span><span class="sxs-lookup"><span data-stu-id="2babc-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="2babc-2780">\_Analyse d’état ci \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="2babc-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="2babc-2781">Le service d’indexation examine un répertoire ou un ensemble de répertoires pour déterminer si des fichiers ont été ajoutés, supprimés ou mis à jour depuis la dernière indexation du répertoire.</span><span class="sxs-lookup"><span data-stu-id="2babc-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2babc-2782">RÉCUPÉRATION de l’état de l’élément de configuration \_ \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="2babc-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="2babc-2783">Le service démarre à partir du dernier état enregistré et est en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="2babc-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2babc-2784">\_ \_ Mémoire insuffisante de l’état ci \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="2babc-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="2babc-2785">La majeure partie de la mémoire virtuelle du serveur est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2babc-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2babc-2786">\_ \_ \_ 0x00000100 e/s haute d’état de l’élément de configuration</span><span class="sxs-lookup"><span data-stu-id="2babc-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="2babc-2787">Le niveau d’activité d’entrée/sortie (e/s) sur le serveur est relativement élevé.</span><span class="sxs-lookup"><span data-stu-id="2babc-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2babc-2788">0x00000200 de la \_ fusion principale de l’état ci \_ \_ \_ suspendu</span><span class="sxs-lookup"><span data-stu-id="2babc-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="2babc-2789">Le processus d’optimisation complète de tous les index en cours a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="2babc-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="2babc-2790">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2babc-2791">État de l’élément de configuration \_ \_ en lecture \_ seule 0x00000400</span><span class="sxs-lookup"><span data-stu-id="2babc-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="2babc-2792">La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="2babc-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="2babc-2793">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2babc-2794">\_0x00000800 de \_ batterie \_ d’état de l’élément de configuration</span><span class="sxs-lookup"><span data-stu-id="2babc-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="2babc-2795">La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue pour économiser la durée de vie de la batterie, tout en répondant aux requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="2babc-2796">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2babc-2797">État de l' \_ \_ utilisateur \_ actif 0x00001000</span><span class="sxs-lookup"><span data-stu-id="2babc-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="2babc-2798">La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue en raison d’une activité élevée par l’utilisateur (clavier ou souris), mais elle répond toujours aux requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="2babc-2799">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="2babc-2800">État de l’élément de configuration à \_ \_ partir de 0x00002000</span><span class="sxs-lookup"><span data-stu-id="2babc-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="2babc-2801">Le service est en cours de démarrage.</span><span class="sxs-lookup"><span data-stu-id="2babc-2801">The service is starting.</span></span> <span data-ttu-id="2babc-2802">Les requêtes peuvent être exécutées, mais l’analyse et la notification n’ont pas encore été activées.</span><span class="sxs-lookup"><span data-stu-id="2babc-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="2babc-2803">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2babc-2804">État de l’élément de configuration \_ \_ \_ USN lecture USN 0x00004000</span><span class="sxs-lookup"><span data-stu-id="2babc-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="2babc-2805">Le service n’a pas lu le journal conservé par le système de fichiers pour effectuer le suivi des modifications apportées aux fichiers ou aux répertoires d’un volume, de sorte que l’index ne soit peut-être pas à jour.</span><span class="sxs-lookup"><span data-stu-id="2babc-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="2babc-2806">**cFilteredDocuments**: entier non signé 32 bits indiquant le nombre de documents indexés depuis le début de l’indexation du contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="2babc-2807">**cTotalDocuments**: entier non signé 32 bits indiquant le nombre total de documents dans le système.</span><span class="sxs-lookup"><span data-stu-id="2babc-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="2babc-2808">**cPendingScans**: entier non signé 32 bits indiquant le nombre d’opérations d’indexation de haut niveau en attente.</span><span class="sxs-lookup"><span data-stu-id="2babc-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="2babc-2809">La signification de cette valeur est spécifique au fournisseur, mais des nombres plus élevés sont supposés indiquer qu’un plus grand nombre d’index est conservé.</span><span class="sxs-lookup"><span data-stu-id="2babc-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="2babc-2810">*Comportement de Windows*: cette valeur est généralement égale à zéro, sauf immédiatement après le démarrage de l’indexation ou après un dépassement de la file d’attente de notification.</span><span class="sxs-lookup"><span data-stu-id="2babc-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="2babc-2811">**dwIndexSize**: entier non signé 32 bits indiquant la taille, en mégaoctets, de l’index (à l’exception du cache de propriété).</span><span class="sxs-lookup"><span data-stu-id="2babc-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="2babc-2812">**cUniqueKeys**: entier non signé 32 bits indiquant le nombre approximatif de clés uniques dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="2babc-2813">**cSecQDocuments**: entier non signé 32 bits indiquant le nombre de documents que le service d’indexation réessaiera d’indexer en raison d’un échec lors de la tentative d’indexation initiale.</span><span class="sxs-lookup"><span data-stu-id="2babc-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="2babc-2814">**dwPropCacheSize**: entier non signé 32 bits indiquant la taille, en mégaoctets, du cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="2babc-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="2babc-2816">Le message CPMSetCatStateIn définit l’état d’un catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="2babc-2817">Le format du message CPMSetCatStateIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-2818">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2818">0</span></span>

<span data-ttu-id="2babc-2819">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2819">1</span></span>

<span data-ttu-id="2babc-2820">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2820">2</span></span>

<span data-ttu-id="2babc-2821">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2821">3</span></span>

<span data-ttu-id="2babc-2822">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2822">4</span></span>

<span data-ttu-id="2babc-2823">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2823">5</span></span>

<span data-ttu-id="2babc-2824">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2824">6</span></span>

<span data-ttu-id="2babc-2825">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2825">7</span></span>

<span data-ttu-id="2babc-2826">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2826">8</span></span>

<span data-ttu-id="2babc-2827">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2827">9</span></span>

<span data-ttu-id="2babc-2828">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2828">1</span></span><br/> <span data-ttu-id="2babc-2829">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2829">0</span></span><br/>

<span data-ttu-id="2babc-2830">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2830">1</span></span>

<span data-ttu-id="2babc-2831">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2831">2</span></span>

<span data-ttu-id="2babc-2832">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2832">3</span></span>

<span data-ttu-id="2babc-2833">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2833">4</span></span>

<span data-ttu-id="2babc-2834">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2834">5</span></span>

<span data-ttu-id="2babc-2835">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2835">6</span></span>

<span data-ttu-id="2babc-2836">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2836">7</span></span>

<span data-ttu-id="2babc-2837">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2837">8</span></span>

<span data-ttu-id="2babc-2838">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2838">9</span></span>

<span data-ttu-id="2babc-2839">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2839">2</span></span><br/> <span data-ttu-id="2babc-2840">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2840">0</span></span><br/>

<span data-ttu-id="2babc-2841">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2841">1</span></span>

<span data-ttu-id="2babc-2842">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2842">2</span></span>

<span data-ttu-id="2babc-2843">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2843">3</span></span>

<span data-ttu-id="2babc-2844">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2844">4</span></span>

<span data-ttu-id="2babc-2845">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2845">5</span></span>

<span data-ttu-id="2babc-2846">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2846">6</span></span>

<span data-ttu-id="2babc-2847">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2847">7</span></span>

<span data-ttu-id="2babc-2848">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2848">8</span></span>

<span data-ttu-id="2babc-2849">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2849">9</span></span>

<span data-ttu-id="2babc-2850">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2850">3</span></span><br/> <span data-ttu-id="2babc-2851">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2851">0</span></span><br/>

<span data-ttu-id="2babc-2852">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2852">1</span></span>

<span data-ttu-id="2babc-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="2babc-2853">\_partID</span></span>

<span data-ttu-id="2babc-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="2babc-2854">\_dwNewState</span></span>

<span data-ttu-id="2babc-2855">\_CatName (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="2babc-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="2babc-2856">**\_ partid**: doit avoir la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="2babc-2857">**\_ dwNewState**: doit être défini sur l’une des valeurs suivantes, indiquant le nouvel État du catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="2babc-2858">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-2858">Value</span></span>                         | <span data-ttu-id="2babc-2859">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-2860">CICAT \_ arrêté 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="2babc-2861">Le catalogue est arrêté.</span><span class="sxs-lookup"><span data-stu-id="2babc-2861">The catalog is stopped.</span></span> <span data-ttu-id="2babc-2862">Cet État signifie qu’aucun nouveau fichier ne doit être indexé et qu’aucune requête de recherche ne doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="2babc-2863">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="2babc-2864">Le catalogue est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2babc-2864">The catalog is read-only.</span></span> <span data-ttu-id="2babc-2865">Aucun nouveau fichier ne doit être indexé.</span><span class="sxs-lookup"><span data-stu-id="2babc-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="2babc-2866">CICAT, en \_ écriture, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="2babc-2867">Le catalogue est accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="2babc-2867">The catalog is writable.</span></span> <span data-ttu-id="2babc-2868">Les nouveaux fichiers peuvent être indexés et les requêtes de recherche doivent être traitées.</span><span class="sxs-lookup"><span data-stu-id="2babc-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="2babc-2869">CICAT \_ pas de \_ requête 0x00000008</span><span class="sxs-lookup"><span data-stu-id="2babc-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="2babc-2870">Le catalogue n’est pas disponible pour l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="2babc-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="2babc-2871">CICAT \_ obtient l' \_ État 0x00000010</span><span class="sxs-lookup"><span data-stu-id="2babc-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="2babc-2872">L’état du catalogue ne doit pas être modifié, récupéré uniquement.</span><span class="sxs-lookup"><span data-stu-id="2babc-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="2babc-2873">CICAT \_ tous les \_ 0x00000020 ouverts</span><span class="sxs-lookup"><span data-stu-id="2babc-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="2babc-2874">Une vérification pour voir si tous les catalogues ont été démarrés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="2babc-2875">Si c’est le cas, le \_ champ dwOldState envoyé dans le CPMSetCatStateOut répondre à ce message est signalé comme étant différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="2babc-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="2babc-2876">**\_ CatName**: nom du catalogue dont l’État doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="2babc-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="2babc-2877">Le nom doit être une chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="2babc-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="2babc-2878">Ce champ doit être omis si \_ dwNewState a la valeur CICAT \_ All \_ Opened.</span><span class="sxs-lookup"><span data-stu-id="2babc-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="2babc-2879">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="2babc-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="2babc-2880">Le message CPMSetCatStateOut est une réponse à un message CPMSetCatStateIn avec l’ancien état du catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="2babc-2881">Le format du message CPMSetCatStateOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-2882">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2882">0</span></span>

<span data-ttu-id="2babc-2883">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2883">1</span></span>

<span data-ttu-id="2babc-2884">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2884">2</span></span>

<span data-ttu-id="2babc-2885">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2885">3</span></span>

<span data-ttu-id="2babc-2886">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2886">4</span></span>

<span data-ttu-id="2babc-2887">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2887">5</span></span>

<span data-ttu-id="2babc-2888">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2888">6</span></span>

<span data-ttu-id="2babc-2889">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2889">7</span></span>

<span data-ttu-id="2babc-2890">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2890">8</span></span>

<span data-ttu-id="2babc-2891">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2891">9</span></span>

<span data-ttu-id="2babc-2892">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2892">1</span></span><br/> <span data-ttu-id="2babc-2893">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2893">0</span></span><br/>

<span data-ttu-id="2babc-2894">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2894">1</span></span>

<span data-ttu-id="2babc-2895">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2895">2</span></span>

<span data-ttu-id="2babc-2896">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2896">3</span></span>

<span data-ttu-id="2babc-2897">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2897">4</span></span>

<span data-ttu-id="2babc-2898">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2898">5</span></span>

<span data-ttu-id="2babc-2899">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2899">6</span></span>

<span data-ttu-id="2babc-2900">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2900">7</span></span>

<span data-ttu-id="2babc-2901">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2901">8</span></span>

<span data-ttu-id="2babc-2902">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2902">9</span></span>

<span data-ttu-id="2babc-2903">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2903">2</span></span><br/> <span data-ttu-id="2babc-2904">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2904">0</span></span><br/>

<span data-ttu-id="2babc-2905">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2905">1</span></span>

<span data-ttu-id="2babc-2906">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2906">2</span></span>

<span data-ttu-id="2babc-2907">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2907">3</span></span>

<span data-ttu-id="2babc-2908">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2908">4</span></span>

<span data-ttu-id="2babc-2909">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2909">5</span></span>

<span data-ttu-id="2babc-2910">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2910">6</span></span>

<span data-ttu-id="2babc-2911">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2911">7</span></span>

<span data-ttu-id="2babc-2912">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2912">8</span></span>

<span data-ttu-id="2babc-2913">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2913">9</span></span>

<span data-ttu-id="2babc-2914">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2914">3</span></span><br/> <span data-ttu-id="2babc-2915">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2915">0</span></span><br/>

<span data-ttu-id="2babc-2916">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2916">1</span></span>

<span data-ttu-id="2babc-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="2babc-2917">\_dwOldState</span></span>



 

<span data-ttu-id="2babc-2918">**\_ dwOldState**: l’une des valeurs suivantes, indiquant l’ancien état du catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="2babc-2919">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-2919">Value</span></span>                       | <span data-ttu-id="2babc-2920">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="2babc-2921">CICAT \_ arrêté 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="2babc-2922">Le catalogue est arrêté.</span><span class="sxs-lookup"><span data-stu-id="2babc-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="2babc-2923">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="2babc-2924">Le catalogue est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2babc-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="2babc-2925">CICAT, en \_ écriture, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="2babc-2926">Le catalogue est accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="2babc-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="2babc-2927">CICAT \_ pas de \_ requête 0x00000008</span><span class="sxs-lookup"><span data-stu-id="2babc-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="2babc-2928">Le catalogue n’est pas disponible pour l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="2babc-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="2babc-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="2babc-2930">Le message CPMUpdateDocumentsIn indique au serveur d’indexer le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="2babc-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="2babc-2931">Le serveur répondra avec l’en-tête de message du message CPMUpdateDocumentsOut, avec les résultats de la requête contenus dans le \_ champ État de l’en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="2babc-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="2babc-2932">Le format du message CPMUpdateDocumentsIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-2933">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2933">0</span></span>

<span data-ttu-id="2babc-2934">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2934">1</span></span>

<span data-ttu-id="2babc-2935">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2935">2</span></span>

<span data-ttu-id="2babc-2936">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2936">3</span></span>

<span data-ttu-id="2babc-2937">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2937">4</span></span>

<span data-ttu-id="2babc-2938">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2938">5</span></span>

<span data-ttu-id="2babc-2939">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2939">6</span></span>

<span data-ttu-id="2babc-2940">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2940">7</span></span>

<span data-ttu-id="2babc-2941">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2941">8</span></span>

<span data-ttu-id="2babc-2942">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2942">9</span></span>

<span data-ttu-id="2babc-2943">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2943">1</span></span><br/> <span data-ttu-id="2babc-2944">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2944">0</span></span><br/>

<span data-ttu-id="2babc-2945">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2945">1</span></span>

<span data-ttu-id="2babc-2946">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2946">2</span></span>

<span data-ttu-id="2babc-2947">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2947">3</span></span>

<span data-ttu-id="2babc-2948">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2948">4</span></span>

<span data-ttu-id="2babc-2949">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2949">5</span></span>

<span data-ttu-id="2babc-2950">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2950">6</span></span>

<span data-ttu-id="2babc-2951">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2951">7</span></span>

<span data-ttu-id="2babc-2952">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2952">8</span></span>

<span data-ttu-id="2babc-2953">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2953">9</span></span>

<span data-ttu-id="2babc-2954">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2954">2</span></span><br/> <span data-ttu-id="2babc-2955">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2955">0</span></span><br/>

<span data-ttu-id="2babc-2956">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2956">1</span></span>

<span data-ttu-id="2babc-2957">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2957">2</span></span>

<span data-ttu-id="2babc-2958">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2958">3</span></span>

<span data-ttu-id="2babc-2959">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2959">4</span></span>

<span data-ttu-id="2babc-2960">5</span><span class="sxs-lookup"><span data-stu-id="2babc-2960">5</span></span>

<span data-ttu-id="2babc-2961">6</span><span class="sxs-lookup"><span data-stu-id="2babc-2961">6</span></span>

<span data-ttu-id="2babc-2962">7</span><span class="sxs-lookup"><span data-stu-id="2babc-2962">7</span></span>

<span data-ttu-id="2babc-2963">8</span><span class="sxs-lookup"><span data-stu-id="2babc-2963">8</span></span>

<span data-ttu-id="2babc-2964">9</span><span class="sxs-lookup"><span data-stu-id="2babc-2964">9</span></span>

<span data-ttu-id="2babc-2965">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2965">3</span></span><br/> <span data-ttu-id="2babc-2966">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2966">0</span></span><br/>

<span data-ttu-id="2babc-2967">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2967">1</span></span>

<span data-ttu-id="2babc-2968">\_indicateur (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2968">\_flag (optional)</span></span>

<span data-ttu-id="2babc-2969">\_fRootPath (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="2babc-2970">RootPath (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="2babc-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="2babc-2971">**\_ indicateur**: type de mise à jour à effectuer.</span><span class="sxs-lookup"><span data-stu-id="2babc-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="2babc-2972">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="2babc-2973">Ce champ doit être défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="2babc-2974">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-2974">Value</span></span>                  | <span data-ttu-id="2babc-2975">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="2babc-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="2babc-2977">Une mise à jour incrémentielle doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="2babc-2978">UPD \_ complet 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="2babc-2979">Une mise à jour complète doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="2babc-2980">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="2babc-2981">Une nouvelle initialisation doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="2babc-2982">**\_ fRootPath**: valeur booléenne indiquant si le champ RootPath spécifie un chemin d’accès sur lequel effectuer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2babc-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="2babc-2983">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="2babc-2984">Ce champ doit avoir la valeur 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="2babc-2985">Si la valeur est définie sur 0x00000001, un chemin d’accès sur lequel effectuer la mise à jour est inclus dans RootPath.</span><span class="sxs-lookup"><span data-stu-id="2babc-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="2babc-2986">Si la valeur est 0x00000000, la mise à jour doit être effectuée sur tous les chemins d’accès indexés.</span><span class="sxs-lookup"><span data-stu-id="2babc-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="2babc-2987">**RootPath**: nom du chemin d’accès à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="2babc-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="2babc-2988">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="2babc-2989">Le nom doit être une chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="2babc-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="2babc-2990">Ce champ doit être omis si \_ fRootPath a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="2babc-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="2babc-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="2babc-2992">Le message CPMForceMergeIn demande à un serveur d’effectuer les opérations de maintenance nécessaires pour améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="2babc-2993">Le serveur répondra avec l’en-tête du message CPMForceMergeIn, avec les résultats de la requête contenus dans le \_ champ État.</span><span class="sxs-lookup"><span data-stu-id="2babc-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="2babc-2994">Le format du message CPMForceMergeIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-2995">0</span><span class="sxs-lookup"><span data-stu-id="2babc-2995">0</span></span>

<span data-ttu-id="2babc-2996">1</span><span class="sxs-lookup"><span data-stu-id="2babc-2996">1</span></span>

<span data-ttu-id="2babc-2997">2</span><span class="sxs-lookup"><span data-stu-id="2babc-2997">2</span></span>

<span data-ttu-id="2babc-2998">3</span><span class="sxs-lookup"><span data-stu-id="2babc-2998">3</span></span>

<span data-ttu-id="2babc-2999">4</span><span class="sxs-lookup"><span data-stu-id="2babc-2999">4</span></span>

<span data-ttu-id="2babc-3000">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3000">5</span></span>

<span data-ttu-id="2babc-3001">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3001">6</span></span>

<span data-ttu-id="2babc-3002">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3002">7</span></span>

<span data-ttu-id="2babc-3003">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3003">8</span></span>

<span data-ttu-id="2babc-3004">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3004">9</span></span>

<span data-ttu-id="2babc-3005">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3005">1</span></span><br/> <span data-ttu-id="2babc-3006">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3006">0</span></span><br/>

<span data-ttu-id="2babc-3007">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3007">1</span></span>

<span data-ttu-id="2babc-3008">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3008">2</span></span>

<span data-ttu-id="2babc-3009">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3009">3</span></span>

<span data-ttu-id="2babc-3010">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3010">4</span></span>

<span data-ttu-id="2babc-3011">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3011">5</span></span>

<span data-ttu-id="2babc-3012">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3012">6</span></span>

<span data-ttu-id="2babc-3013">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3013">7</span></span>

<span data-ttu-id="2babc-3014">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3014">8</span></span>

<span data-ttu-id="2babc-3015">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3015">9</span></span>

<span data-ttu-id="2babc-3016">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3016">2</span></span><br/> <span data-ttu-id="2babc-3017">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3017">0</span></span><br/>

<span data-ttu-id="2babc-3018">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3018">1</span></span>

<span data-ttu-id="2babc-3019">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3019">2</span></span>

<span data-ttu-id="2babc-3020">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3020">3</span></span>

<span data-ttu-id="2babc-3021">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3021">4</span></span>

<span data-ttu-id="2babc-3022">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3022">5</span></span>

<span data-ttu-id="2babc-3023">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3023">6</span></span>

<span data-ttu-id="2babc-3024">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3024">7</span></span>

<span data-ttu-id="2babc-3025">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3025">8</span></span>

<span data-ttu-id="2babc-3026">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3026">9</span></span>

<span data-ttu-id="2babc-3027">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3027">3</span></span><br/> <span data-ttu-id="2babc-3028">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3028">0</span></span><br/>

<span data-ttu-id="2babc-3029">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3029">1</span></span>

<span data-ttu-id="2babc-3030">\_partId (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="2babc-3031">**\_ partid**: ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="2babc-3032">Quand ce champ est présent, il doit avoir la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="2babc-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="2babc-3034">Le message CPMConnectIn commence une session entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="2babc-3035">Le format du message CPMConnectIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3036">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3036">0</span></span>

<span data-ttu-id="2babc-3037">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3037">1</span></span>

<span data-ttu-id="2babc-3038">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3038">2</span></span>

<span data-ttu-id="2babc-3039">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3039">3</span></span>

<span data-ttu-id="2babc-3040">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3040">4</span></span>

<span data-ttu-id="2babc-3041">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3041">5</span></span>

<span data-ttu-id="2babc-3042">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3042">6</span></span>

<span data-ttu-id="2babc-3043">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3043">7</span></span>

<span data-ttu-id="2babc-3044">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3044">8</span></span>

<span data-ttu-id="2babc-3045">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3045">9</span></span>

<span data-ttu-id="2babc-3046">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3046">1</span></span><br/> <span data-ttu-id="2babc-3047">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3047">0</span></span><br/>

<span data-ttu-id="2babc-3048">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3048">1</span></span>

<span data-ttu-id="2babc-3049">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3049">2</span></span>

<span data-ttu-id="2babc-3050">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3050">3</span></span>

<span data-ttu-id="2babc-3051">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3051">4</span></span>

<span data-ttu-id="2babc-3052">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3052">5</span></span>

<span data-ttu-id="2babc-3053">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3053">6</span></span>

<span data-ttu-id="2babc-3054">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3054">7</span></span>

<span data-ttu-id="2babc-3055">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3055">8</span></span>

<span data-ttu-id="2babc-3056">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3056">9</span></span>

<span data-ttu-id="2babc-3057">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3057">2</span></span><br/> <span data-ttu-id="2babc-3058">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3058">0</span></span><br/>

<span data-ttu-id="2babc-3059">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3059">1</span></span>

<span data-ttu-id="2babc-3060">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3060">2</span></span>

<span data-ttu-id="2babc-3061">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3061">3</span></span>

<span data-ttu-id="2babc-3062">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3062">4</span></span>

<span data-ttu-id="2babc-3063">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3063">5</span></span>

<span data-ttu-id="2babc-3064">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3064">6</span></span>

<span data-ttu-id="2babc-3065">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3065">7</span></span>

<span data-ttu-id="2babc-3066">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3066">8</span></span>

<span data-ttu-id="2babc-3067">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3067">9</span></span>

<span data-ttu-id="2babc-3068">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3068">3</span></span><br/> <span data-ttu-id="2babc-3069">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3069">0</span></span><br/>

<span data-ttu-id="2babc-3070">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3070">1</span></span>

<span data-ttu-id="2babc-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="2babc-3071">\_iClientVersion</span></span>

<span data-ttu-id="2babc-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="2babc-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="2babc-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="2babc-3073">\_cbBlob1</span></span>

<span data-ttu-id="2babc-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="2babc-3074">\_cbBlob2</span></span>

<span data-ttu-id="2babc-3075">\_remplissage</span><span class="sxs-lookup"><span data-stu-id="2babc-3075">\_padding</span></span>

<span data-ttu-id="2babc-3076">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3076">...</span></span>

<span data-ttu-id="2babc-3077">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3077">...</span></span>

<span data-ttu-id="2babc-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="2babc-3078">MachineName</span></span>

<span data-ttu-id="2babc-3079">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-3079">... (variable)</span></span>

<span data-ttu-id="2babc-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="2babc-3080">UserName</span></span>

<span data-ttu-id="2babc-3081">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-3081">... (variable)</span></span>

<span data-ttu-id="2babc-3082">\_paddingcPropSets (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="2babc-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="2babc-3083">cPropSets</span></span>

<span data-ttu-id="2babc-3084">PropertySet1 (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="2babc-3085">PropertySet2 (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="2babc-3086">\_paddingExtPropset (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="2babc-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="2babc-3087">cExtPropSet</span></span>

<span data-ttu-id="2babc-3088">aPropertySets (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="2babc-3089">**\_ iClientVersion**: entier 32 bits qui indique si le serveur doit valider la valeur de somme de contrôle spécifiée dans le \_ champ ulChecksum des en-têtes de message pour les messages envoyés par le client.</span><span class="sxs-lookup"><span data-stu-id="2babc-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="2babc-3090">Si le \_ champ iClientVersion est défini sur 0x00000008 ou une version ultérieure, le serveur doit valider la \_ valeur du champ ulChecksum pour les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="2babc-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="2babc-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="2babc-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="2babc-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="2babc-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="2babc-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="2babc-3096">Pour plus d’informations sur la façon dont le serveur valide la valeur spécifiée par le client dans le champ ulChecksum pour les messages listés ci-dessus, consultez la section 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="2babc-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="2babc-3097">Si la valeur est supérieure à 0x00000008, le client est supposé être en charge de la gestion des décalages 64 bits dans les messages CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="2babc-3098">Pour plus d’informations, consultez la section 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="2babc-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="2babc-3099">*Comportement de Windows : sur les clients Windows, iClientVersion est défini comme suit*:</span><span class="sxs-lookup"><span data-stu-id="2babc-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="2babc-3100">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-3100">Value</span></span>      | <span data-ttu-id="2babc-3101">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="2babc-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="2babc-3102">0x00000005</span></span> | <span data-ttu-id="2babc-3103">Le système d’exploitation client est Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2babc-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="2babc-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2babc-3104">0x00000008</span></span> | <span data-ttu-id="2babc-3105">Le système d’exploitation client est soit 32 bits Windows XP, soit 32 bits Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2babc-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="2babc-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="2babc-3106">0x00010008</span></span> | <span data-ttu-id="2babc-3107">Le système d’exploitation client est soit 64 bits Windows XP, soit 64 bits Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2babc-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="2babc-3108">\_**fClientIsRemote**: valeur booléenne indiquant si le client s’exécute sur un ordinateur différent du serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="2babc-3109">DOIT être défini sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="2babc-3110">\_**cbBlob1**: entier non signé 32 bits indiquant la taille en octets des champs CPropSet, PropertySet1 et PropertySet2, combinée.</span><span class="sxs-lookup"><span data-stu-id="2babc-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="2babc-3111">\_**cbBlob2**: entier non signé 32 bits indiquant la taille en octets des champs CExPropSet et aPropertySet, combinée.</span><span class="sxs-lookup"><span data-stu-id="2babc-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="2babc-3112">\_**remplissage**: 12 octets de remplissage qui peuvent contenir des valeurs arbitraires et doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="2babc-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="2babc-3113">**MachineName**: nom de l’ordinateur du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="2babc-3114">La chaîne de nom doit être un tableau de moins de 512 caractères Unicode se terminant par un caractère null, y compris la marque de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="2babc-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="2babc-3115">**Username**: chaîne qui représente le nom d’utilisateur de la personne qui exécute l’application qui a appelé ce protocole.</span><span class="sxs-lookup"><span data-stu-id="2babc-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="2babc-3116">La chaîne de nom doit être un tableau de moins de 512 caractères Unicode se terminant par un caractère null en cas de concaténation avec MachineName.</span><span class="sxs-lookup"><span data-stu-id="2babc-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="2babc-3117">**\_ paddingcPropSets**: ce champ doit avoir une longueur de 0 à 7 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="2babc-3118">Le nombre d’octets doit être le nombre requis pour que l’offset d’octet du champ cPropSets à partir du début du message qui contient cette structure soit un multiple de 8.</span><span class="sxs-lookup"><span data-stu-id="2babc-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="2babc-3119">La valeur des octets peut être n’importe quelle valeur arbitraire et doit être ignorée par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-3120">**cPropSets**: entier non signé 32 bits indiquant le nombre de structures CDbPropSet qui suivent ce champ.</span><span class="sxs-lookup"><span data-stu-id="2babc-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="2babc-3121">Cette valeur doit être définie sur 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="2babc-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="2babc-3122">**PropertySet1**: structure CDbPropSet avec GUIDPROPERTYSET contenant DBPROPSET \_ FSCIFRMWRK \_ ext (voir la section 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="2babc-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="2babc-3123">**PropertySet2**: structure CDbPropSet avec GUIDPROPERTYSET contenant DBPROPSET \_ CIFRMWRKCORE \_ ext (voir la section 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="2babc-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="2babc-3124">\_**PaddingExtPropset**: ce champ doit avoir une longueur de 0 à 7 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="2babc-3125">Le nombre d’octets doit être le nombre requis pour que l’offset d’octet du champ cExtPropSets à partir du début du message qui contient cette structure soit un multiple de 8.</span><span class="sxs-lookup"><span data-stu-id="2babc-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="2babc-3126">La valeur des octets peut être n’importe quelle valeur arbitraire et doit être ignorée par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-3127">**cExtPropSet**: entier non signé 32 bits indiquant le nombre de structures CDbPropSet qui suivent ce champ.</span><span class="sxs-lookup"><span data-stu-id="2babc-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="2babc-3128">**aPropertySets**: tableau de structures CDbPropSet spécifiant d’autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="2babc-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="2babc-3129">Le nombre d’éléments de ce tableau doit être égal à cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="2babc-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="2babc-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="2babc-3131">Le message CPMConnectOut contient une réponse à un message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="2babc-3132">Le format du message CPMConnectOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3133">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3133">0</span></span>

<span data-ttu-id="2babc-3134">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3134">1</span></span>

<span data-ttu-id="2babc-3135">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3135">2</span></span>

<span data-ttu-id="2babc-3136">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3136">3</span></span>

<span data-ttu-id="2babc-3137">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3137">4</span></span>

<span data-ttu-id="2babc-3138">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3138">5</span></span>

<span data-ttu-id="2babc-3139">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3139">6</span></span>

<span data-ttu-id="2babc-3140">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3140">7</span></span>

<span data-ttu-id="2babc-3141">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3141">8</span></span>

<span data-ttu-id="2babc-3142">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3142">9</span></span>

<span data-ttu-id="2babc-3143">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3143">1</span></span><br/> <span data-ttu-id="2babc-3144">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3144">0</span></span><br/>

<span data-ttu-id="2babc-3145">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3145">1</span></span>

<span data-ttu-id="2babc-3146">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3146">2</span></span>

<span data-ttu-id="2babc-3147">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3147">3</span></span>

<span data-ttu-id="2babc-3148">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3148">4</span></span>

<span data-ttu-id="2babc-3149">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3149">5</span></span>

<span data-ttu-id="2babc-3150">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3150">6</span></span>

<span data-ttu-id="2babc-3151">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3151">7</span></span>

<span data-ttu-id="2babc-3152">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3152">8</span></span>

<span data-ttu-id="2babc-3153">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3153">9</span></span>

<span data-ttu-id="2babc-3154">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3154">2</span></span><br/> <span data-ttu-id="2babc-3155">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3155">0</span></span><br/>

<span data-ttu-id="2babc-3156">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3156">1</span></span>

<span data-ttu-id="2babc-3157">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3157">2</span></span>

<span data-ttu-id="2babc-3158">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3158">3</span></span>

<span data-ttu-id="2babc-3159">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3159">4</span></span>

<span data-ttu-id="2babc-3160">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3160">5</span></span>

<span data-ttu-id="2babc-3161">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3161">6</span></span>

<span data-ttu-id="2babc-3162">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3162">7</span></span>

<span data-ttu-id="2babc-3163">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3163">8</span></span>

<span data-ttu-id="2babc-3164">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3164">9</span></span>

<span data-ttu-id="2babc-3165">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3165">3</span></span><br/> <span data-ttu-id="2babc-3166">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3166">0</span></span><br/>

<span data-ttu-id="2babc-3167">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3167">1</span></span>

<span data-ttu-id="2babc-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="2babc-3168">\_serverVersion</span></span>

<span data-ttu-id="2babc-3169">\_réservé (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="2babc-3170">**\_ ServerVersion**:</span><span class="sxs-lookup"><span data-stu-id="2babc-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="2babc-3171">Entier 32 bits, indiquant si le serveur peut prendre en charge les décalages 64 bits *.*</span><span class="sxs-lookup"><span data-stu-id="2babc-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="2babc-3172">Pour plus d’informations, consultez la section 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="2babc-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="2babc-3173">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-3173">Value</span></span>      | <span data-ttu-id="2babc-3174">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="2babc-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="2babc-3175">0x00000007</span></span> | <span data-ttu-id="2babc-3176">Le serveur peut uniquement envoyer des décalages 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="2babc-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="2babc-3177">0x00010007</span></span> | <span data-ttu-id="2babc-3178">Le serveur peut envoyer des décalages 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="2babc-3179">**\_ réservé**: réservé.</span><span class="sxs-lookup"><span data-stu-id="2babc-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="2babc-3180">Le serveur peut envoyer un nombre arbitraire de valeurs arbitraires et le client doit ignorer ces valeurs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2babc-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="2babc-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="2babc-3182">Le message CPMCreateQueryIn crée une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="2babc-3183">Le format du message CPMCreateQueryIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3184">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3184">0</span></span>

<span data-ttu-id="2babc-3185">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3185">1</span></span>

<span data-ttu-id="2babc-3186">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3186">2</span></span>

<span data-ttu-id="2babc-3187">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3187">3</span></span>

<span data-ttu-id="2babc-3188">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3188">4</span></span>

<span data-ttu-id="2babc-3189">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3189">5</span></span>

<span data-ttu-id="2babc-3190">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3190">6</span></span>

<span data-ttu-id="2babc-3191">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3191">7</span></span>

<span data-ttu-id="2babc-3192">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3192">8</span></span>

<span data-ttu-id="2babc-3193">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3193">9</span></span>

<span data-ttu-id="2babc-3194">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3194">1</span></span><br/> <span data-ttu-id="2babc-3195">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3195">0</span></span><br/>

<span data-ttu-id="2babc-3196">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3196">1</span></span>

<span data-ttu-id="2babc-3197">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3197">2</span></span>

<span data-ttu-id="2babc-3198">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3198">3</span></span>

<span data-ttu-id="2babc-3199">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3199">4</span></span>

<span data-ttu-id="2babc-3200">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3200">5</span></span>

<span data-ttu-id="2babc-3201">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3201">6</span></span>

<span data-ttu-id="2babc-3202">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3202">7</span></span>

<span data-ttu-id="2babc-3203">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3203">8</span></span>

<span data-ttu-id="2babc-3204">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3204">9</span></span>

<span data-ttu-id="2babc-3205">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3205">2</span></span><br/> <span data-ttu-id="2babc-3206">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3206">0</span></span><br/>

<span data-ttu-id="2babc-3207">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3207">1</span></span>

<span data-ttu-id="2babc-3208">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3208">2</span></span>

<span data-ttu-id="2babc-3209">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3209">3</span></span>

<span data-ttu-id="2babc-3210">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3210">4</span></span>

<span data-ttu-id="2babc-3211">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3211">5</span></span>

<span data-ttu-id="2babc-3212">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3212">6</span></span>

<span data-ttu-id="2babc-3213">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3213">7</span></span>

<span data-ttu-id="2babc-3214">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3214">8</span></span>

<span data-ttu-id="2babc-3215">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3215">9</span></span>

<span data-ttu-id="2babc-3216">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3216">3</span></span><br/> <span data-ttu-id="2babc-3217">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3217">0</span></span><br/>

<span data-ttu-id="2babc-3218">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3218">1</span></span>

<span data-ttu-id="2babc-3219">Taille</span><span class="sxs-lookup"><span data-stu-id="2babc-3219">Size</span></span>

<span data-ttu-id="2babc-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="2babc-3220">CColumnSetPresent</span></span>

<span data-ttu-id="2babc-3221">ColumnSet (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="2babc-3222">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-3222">... (variable)</span></span>

<span data-ttu-id="2babc-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="2babc-3224">Restriction (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3224">Restriction (optional)</span></span>

<span data-ttu-id="2babc-3225">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-3225">... (variable)</span></span>

<span data-ttu-id="2babc-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="2babc-3226">CSortSetPresent</span></span>

<span data-ttu-id="2babc-3227">SortSet (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3227">SortSet (optional)</span></span>

<span data-ttu-id="2babc-3228">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-3228">... (variable)</span></span>

<span data-ttu-id="2babc-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="2babc-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="2babc-3230">CategorizationSet (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="2babc-3231">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-3231">... (variable)</span></span>

<span data-ttu-id="2babc-3232">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="2babc-3232">RowSetProperties</span></span>

<span data-ttu-id="2babc-3233">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3233">...</span></span>

<span data-ttu-id="2babc-3234">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3234">...</span></span>

<span data-ttu-id="2babc-3235">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3235">...</span></span>

<span data-ttu-id="2babc-3236">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3236">...</span></span>

<span data-ttu-id="2babc-3237">PidMapper (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="2babc-3238">**Size**: entier non signé 32 bits indiquant le nombre d’octets entre le début de ce champ et la fin du message.</span><span class="sxs-lookup"><span data-stu-id="2babc-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="2babc-3239">**CColumnSetPresent**: champ d’octets indiquant si le champ ColumnSet est présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="2babc-3240">Ce champ doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="2babc-3241">Si la valeur est définie sur 0x01, le champ CColumnSet doit être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="2babc-3242">Si la valeur est 0x00, elle doit être absente.</span><span class="sxs-lookup"><span data-stu-id="2babc-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="2babc-3243">**ColumnSet**: structure CColumnSet contenant les numéros de colonne dans lesquels les propriétés de CPidMapper doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="2babc-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="2babc-3244">**CRestrictionPresent**: champ d’octets indiquant si le champ de restriction est présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="2babc-3245">Si vous définissez une valeur différente de zéro, le champ de restriction doit être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="2babc-3246">Si la valeur est 0x00, la restriction doit être absente.</span><span class="sxs-lookup"><span data-stu-id="2babc-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="2babc-3247">**Restriction**: structure CRestriction contenant l’arborescence de commandes de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="2babc-3248">**CSortSetPresent**: champ d’octets indiquant si le champ SortSet est présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="2babc-3249">Si vous définissez une valeur différente de zéro, le champ SortSet doit être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="2babc-3250">Si la valeur est 0x00, SortSet doit être absent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="2babc-3251">**SortSet**: structure CSortSet indiquant l’ordre de tri de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="2babc-3252">**CCategorizationSetPresent**: champ d’octets indiquant si le champ CCategorizationSet est présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="2babc-3253">Si vous définissez une valeur différente de zéro, le champ CCategorizationSet doit être présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="2babc-3254">Si la valeur est 0x00, CCategorizationSet doit être absent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="2babc-3255">**CCategorizationSet**: structure CCategorizationSet qui contient les groupes de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="2babc-3256">**RowSetProperties**: structure CRowsetProperties fournissant des informations de configuration pour la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="2babc-3257">**PidMapper**: structure CPidMapper contenant les propriétés à retourner dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="2babc-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="2babc-3259">Le message CPMCreateQueryOut contient une réponse à un message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="2babc-3260">Le format du message CPMCreateQueryOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3261">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3261">0</span></span>

<span data-ttu-id="2babc-3262">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3262">1</span></span>

<span data-ttu-id="2babc-3263">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3263">2</span></span>

<span data-ttu-id="2babc-3264">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3264">3</span></span>

<span data-ttu-id="2babc-3265">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3265">4</span></span>

<span data-ttu-id="2babc-3266">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3266">5</span></span>

<span data-ttu-id="2babc-3267">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3267">6</span></span>

<span data-ttu-id="2babc-3268">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3268">7</span></span>

<span data-ttu-id="2babc-3269">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3269">8</span></span>

<span data-ttu-id="2babc-3270">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3270">9</span></span>

<span data-ttu-id="2babc-3271">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3271">1</span></span><br/> <span data-ttu-id="2babc-3272">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3272">0</span></span><br/>

<span data-ttu-id="2babc-3273">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3273">1</span></span>

<span data-ttu-id="2babc-3274">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3274">2</span></span>

<span data-ttu-id="2babc-3275">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3275">3</span></span>

<span data-ttu-id="2babc-3276">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3276">4</span></span>

<span data-ttu-id="2babc-3277">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3277">5</span></span>

<span data-ttu-id="2babc-3278">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3278">6</span></span>

<span data-ttu-id="2babc-3279">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3279">7</span></span>

<span data-ttu-id="2babc-3280">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3280">8</span></span>

<span data-ttu-id="2babc-3281">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3281">9</span></span>

<span data-ttu-id="2babc-3282">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3282">2</span></span><br/> <span data-ttu-id="2babc-3283">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3283">0</span></span><br/>

<span data-ttu-id="2babc-3284">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3284">1</span></span>

<span data-ttu-id="2babc-3285">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3285">2</span></span>

<span data-ttu-id="2babc-3286">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3286">3</span></span>

<span data-ttu-id="2babc-3287">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3287">4</span></span>

<span data-ttu-id="2babc-3288">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3288">5</span></span>

<span data-ttu-id="2babc-3289">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3289">6</span></span>

<span data-ttu-id="2babc-3290">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3290">7</span></span>

<span data-ttu-id="2babc-3291">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3291">8</span></span>

<span data-ttu-id="2babc-3292">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3292">9</span></span>

<span data-ttu-id="2babc-3293">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3293">3</span></span><br/> <span data-ttu-id="2babc-3294">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3294">0</span></span><br/>

<span data-ttu-id="2babc-3295">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3295">1</span></span>

<span data-ttu-id="2babc-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="2babc-3296">\_fTrueSequential</span></span>

<span data-ttu-id="2babc-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="2babc-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="2babc-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="2babc-3298">aCursors</span></span>



 

<span data-ttu-id="2babc-3299">**\_ fTrueSequential**: valeur booléenne informatif indiquant si la requête peut être supposée fournir des résultats plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="2babc-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="2babc-3300">Lorsqu’il est défini sur 0x00000001 pour la requête fournie dans CPMCreateQueryIn, le serveur peut utiliser l’index de telle sorte que les résultats de la requête seront probablement remis plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="2babc-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="2babc-3301">Lorsque la valeur est 0x00000000, il y a une latence plus importante dans la transmission des résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="2babc-3302">Ne doit pas être défini sur une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="2babc-3303">**\_ fWorkIdUnique**: valeur booléenne indiquant si les identificateurs de document pointés par les curseurs sont uniques dans tous les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="2babc-3304">Si la valeur est 0x00000001, les identificateurs sont uniques.</span><span class="sxs-lookup"><span data-stu-id="2babc-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="2babc-3305">Si la valeur est 0x00000000, elles sont uniques uniquement dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="2babc-3306">**aCursors**: tableau d’entiers non signés 32 bits représentant les handles des curseurs, avec le nombre d’éléments égal au nombre de catégories dans le champ CategorizationSet du message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="2babc-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="2babc-3308">Le message CPMGetQueryStatusIn demande l’état d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="2babc-3309">Le format du message CPMGetQueryStatusIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3310">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3310">0</span></span>

<span data-ttu-id="2babc-3311">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3311">1</span></span>

<span data-ttu-id="2babc-3312">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3312">2</span></span>

<span data-ttu-id="2babc-3313">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3313">3</span></span>

<span data-ttu-id="2babc-3314">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3314">4</span></span>

<span data-ttu-id="2babc-3315">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3315">5</span></span>

<span data-ttu-id="2babc-3316">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3316">6</span></span>

<span data-ttu-id="2babc-3317">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3317">7</span></span>

<span data-ttu-id="2babc-3318">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3318">8</span></span>

<span data-ttu-id="2babc-3319">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3319">9</span></span>

<span data-ttu-id="2babc-3320">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3320">1</span></span><br/> <span data-ttu-id="2babc-3321">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3321">0</span></span><br/>

<span data-ttu-id="2babc-3322">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3322">1</span></span>

<span data-ttu-id="2babc-3323">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3323">2</span></span>

<span data-ttu-id="2babc-3324">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3324">3</span></span>

<span data-ttu-id="2babc-3325">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3325">4</span></span>

<span data-ttu-id="2babc-3326">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3326">5</span></span>

<span data-ttu-id="2babc-3327">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3327">6</span></span>

<span data-ttu-id="2babc-3328">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3328">7</span></span>

<span data-ttu-id="2babc-3329">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3329">8</span></span>

<span data-ttu-id="2babc-3330">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3330">9</span></span>

<span data-ttu-id="2babc-3331">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3331">2</span></span><br/> <span data-ttu-id="2babc-3332">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3332">0</span></span><br/>

<span data-ttu-id="2babc-3333">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3333">1</span></span>

<span data-ttu-id="2babc-3334">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3334">2</span></span>

<span data-ttu-id="2babc-3335">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3335">3</span></span>

<span data-ttu-id="2babc-3336">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3336">4</span></span>

<span data-ttu-id="2babc-3337">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3337">5</span></span>

<span data-ttu-id="2babc-3338">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3338">6</span></span>

<span data-ttu-id="2babc-3339">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3339">7</span></span>

<span data-ttu-id="2babc-3340">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3340">8</span></span>

<span data-ttu-id="2babc-3341">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3341">9</span></span>

<span data-ttu-id="2babc-3342">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3342">3</span></span><br/> <span data-ttu-id="2babc-3343">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3343">0</span></span><br/>

<span data-ttu-id="2babc-3344">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3344">1</span></span>

<span data-ttu-id="2babc-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="2babc-3345">\_hCursor</span></span>



 

<span data-ttu-id="2babc-3346">**\_ hCursor**: entier non signé 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les informations d’État doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="2babc-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="2babc-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="2babc-3348">Le message CPMGetQueryStatusOut répond à un message CPMGetQueryStatusIn avec l’état de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="2babc-3349">Le format du message CPMGetQueryStatusOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3350">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3350">0</span></span>

<span data-ttu-id="2babc-3351">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3351">1</span></span>

<span data-ttu-id="2babc-3352">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3352">2</span></span>

<span data-ttu-id="2babc-3353">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3353">3</span></span>

<span data-ttu-id="2babc-3354">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3354">4</span></span>

<span data-ttu-id="2babc-3355">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3355">5</span></span>

<span data-ttu-id="2babc-3356">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3356">6</span></span>

<span data-ttu-id="2babc-3357">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3357">7</span></span>

<span data-ttu-id="2babc-3358">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3358">8</span></span>

<span data-ttu-id="2babc-3359">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3359">9</span></span>

<span data-ttu-id="2babc-3360">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3360">1</span></span><br/> <span data-ttu-id="2babc-3361">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3361">0</span></span><br/>

<span data-ttu-id="2babc-3362">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3362">1</span></span>

<span data-ttu-id="2babc-3363">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3363">2</span></span>

<span data-ttu-id="2babc-3364">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3364">3</span></span>

<span data-ttu-id="2babc-3365">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3365">4</span></span>

<span data-ttu-id="2babc-3366">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3366">5</span></span>

<span data-ttu-id="2babc-3367">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3367">6</span></span>

<span data-ttu-id="2babc-3368">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3368">7</span></span>

<span data-ttu-id="2babc-3369">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3369">8</span></span>

<span data-ttu-id="2babc-3370">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3370">9</span></span>

<span data-ttu-id="2babc-3371">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3371">2</span></span><br/> <span data-ttu-id="2babc-3372">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3372">0</span></span><br/>

<span data-ttu-id="2babc-3373">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3373">1</span></span>

<span data-ttu-id="2babc-3374">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3374">2</span></span>

<span data-ttu-id="2babc-3375">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3375">3</span></span>

<span data-ttu-id="2babc-3376">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3376">4</span></span>

<span data-ttu-id="2babc-3377">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3377">5</span></span>

<span data-ttu-id="2babc-3378">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3378">6</span></span>

<span data-ttu-id="2babc-3379">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3379">7</span></span>

<span data-ttu-id="2babc-3380">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3380">8</span></span>

<span data-ttu-id="2babc-3381">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3381">9</span></span>

<span data-ttu-id="2babc-3382">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3382">3</span></span><br/> <span data-ttu-id="2babc-3383">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3383">0</span></span><br/>

<span data-ttu-id="2babc-3384">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3384">1</span></span>

<span data-ttu-id="2babc-3385">\_Statut</span><span class="sxs-lookup"><span data-stu-id="2babc-3385">\_Status</span></span>



 

<span data-ttu-id="2babc-3386">**\_ État**: masque de sous-masque des valeurs définies dans les tableaux ci-dessous, qui décrit la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="2babc-3387">Le tableau suivant répertorie les \_ \* valeurs stat obtenues en effectuant une opération and au niveau du bit sur \_ Status avec 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="2babc-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="2babc-3388">Le résultat doit être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="2babc-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="2babc-3389">Constante</span><span class="sxs-lookup"><span data-stu-id="2babc-3389">Constant</span></span>                 | <span data-ttu-id="2babc-3390">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-3391">STAT \_ occupées 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="2babc-3392">La requête asynchrone est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2babc-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="2babc-3393">\_Erreur stat 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="2babc-3394">La requête est dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="2babc-3395">STATISTIQUES \_ terminées 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="2babc-3396">La requête est terminée.</span><span class="sxs-lookup"><span data-stu-id="2babc-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="2babc-3397">STATISTIQUES d' \_ actualisation 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="2babc-3398">La requête est terminée, mais les mises à jour entraînent des calculs de requête supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2babc-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="2babc-3399">Le tableau suivant répertorie les bits STAT supplémentaires \_ \* qui peuvent être définis indépendamment.</span><span class="sxs-lookup"><span data-stu-id="2babc-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="2babc-3400">Constante</span><span class="sxs-lookup"><span data-stu-id="2babc-3400">Constant</span></span>                                    | <span data-ttu-id="2babc-3401">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2babc-3402">\_Mots parasites statistiques \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="2babc-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="2babc-3403">Les mots parasites ont été remplacés par des caractères génériques dans la requête de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="2babc-3404">\_Contenu stat \_ obsolète \_ \_</span><span class="sxs-lookup"><span data-stu-id="2babc-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="2babc-3405">Les résultats de la requête sont peut-être incorrects, car la requête impliquait des fichiers modifiés, mais non indexés.</span><span class="sxs-lookup"><span data-stu-id="2babc-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="2babc-3406">Actualisation des statistiques \_ \_ 0x00000040 incomplète</span><span class="sxs-lookup"><span data-stu-id="2babc-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="2babc-3407">Les résultats de la requête sont peut-être incorrects, car la requête impliquait la modification et la réindexation des fichiers dont le contenu n’était pas inclus.</span><span class="sxs-lookup"><span data-stu-id="2babc-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="2babc-3408">\_Requête de contenu stat \_ \_ incomplète 0x00000080</span><span class="sxs-lookup"><span data-stu-id="2babc-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="2babc-3409">La requête de contenu était trop complexe pour être exécutée ou une énumération requise au lieu d’utiliser l’index de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="2babc-3410">Limite de durée des statistiques \_ \_ \_ dépassée 0x00000100</span><span class="sxs-lookup"><span data-stu-id="2babc-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="2babc-3411">Les résultats de la requête sont peut-être incorrects, car la durée d’exécution de la requête a atteint le délai maximal autorisé.</span><span class="sxs-lookup"><span data-stu-id="2babc-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="2babc-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="2babc-3413">Le message CPMGetQueryStatusExIn demande l’état d’une requête et des informations supplémentaires, telles que le nombre de documents qui ont été indexés, le nombre de documents restant à indexer, etc.</span><span class="sxs-lookup"><span data-stu-id="2babc-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="2babc-3414">Le format du message CPMGetQueryStatusExIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3415">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3415">0</span></span>

<span data-ttu-id="2babc-3416">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3416">1</span></span>

<span data-ttu-id="2babc-3417">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3417">2</span></span>

<span data-ttu-id="2babc-3418">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3418">3</span></span>

<span data-ttu-id="2babc-3419">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3419">4</span></span>

<span data-ttu-id="2babc-3420">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3420">5</span></span>

<span data-ttu-id="2babc-3421">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3421">6</span></span>

<span data-ttu-id="2babc-3422">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3422">7</span></span>

<span data-ttu-id="2babc-3423">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3423">8</span></span>

<span data-ttu-id="2babc-3424">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3424">9</span></span>

<span data-ttu-id="2babc-3425">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3425">1</span></span><br/> <span data-ttu-id="2babc-3426">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3426">0</span></span><br/>

<span data-ttu-id="2babc-3427">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3427">1</span></span>

<span data-ttu-id="2babc-3428">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3428">2</span></span>

<span data-ttu-id="2babc-3429">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3429">3</span></span>

<span data-ttu-id="2babc-3430">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3430">4</span></span>

<span data-ttu-id="2babc-3431">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3431">5</span></span>

<span data-ttu-id="2babc-3432">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3432">6</span></span>

<span data-ttu-id="2babc-3433">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3433">7</span></span>

<span data-ttu-id="2babc-3434">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3434">8</span></span>

<span data-ttu-id="2babc-3435">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3435">9</span></span>

<span data-ttu-id="2babc-3436">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3436">2</span></span><br/> <span data-ttu-id="2babc-3437">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3437">0</span></span><br/>

<span data-ttu-id="2babc-3438">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3438">1</span></span>

<span data-ttu-id="2babc-3439">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3439">2</span></span>

<span data-ttu-id="2babc-3440">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3440">3</span></span>

<span data-ttu-id="2babc-3441">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3441">4</span></span>

<span data-ttu-id="2babc-3442">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3442">5</span></span>

<span data-ttu-id="2babc-3443">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3443">6</span></span>

<span data-ttu-id="2babc-3444">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3444">7</span></span>

<span data-ttu-id="2babc-3445">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3445">8</span></span>

<span data-ttu-id="2babc-3446">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3446">9</span></span>

<span data-ttu-id="2babc-3447">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3447">3</span></span><br/> <span data-ttu-id="2babc-3448">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3448">0</span></span><br/>

<span data-ttu-id="2babc-3449">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3449">1</span></span>

<span data-ttu-id="2babc-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="2babc-3450">\_hCursor</span></span>

<span data-ttu-id="2babc-3451">\_bmk</span><span class="sxs-lookup"><span data-stu-id="2babc-3451">\_bmk</span></span>



 

<span data-ttu-id="2babc-3452">**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les informations d’État doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="2babc-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="2babc-3453">**\_ BMK**: valeur 32 bits indiquant le descripteur d’un signet dont la position doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="2babc-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="2babc-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="2babc-3455">Le message CPMGetQueryStatusExOut répond à un message CPMGetQueryStatusExIn avec l’état de la requête et d’autres informations d’État, comme indiqué dans le diagramme ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2babc-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="2babc-3456">Le format du message CPMGetQueryStatusExOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3457">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3457">0</span></span>

<span data-ttu-id="2babc-3458">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3458">1</span></span>

<span data-ttu-id="2babc-3459">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3459">2</span></span>

<span data-ttu-id="2babc-3460">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3460">3</span></span>

<span data-ttu-id="2babc-3461">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3461">4</span></span>

<span data-ttu-id="2babc-3462">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3462">5</span></span>

<span data-ttu-id="2babc-3463">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3463">6</span></span>

<span data-ttu-id="2babc-3464">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3464">7</span></span>

<span data-ttu-id="2babc-3465">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3465">8</span></span>

<span data-ttu-id="2babc-3466">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3466">9</span></span>

<span data-ttu-id="2babc-3467">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3467">1</span></span><br/> <span data-ttu-id="2babc-3468">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3468">0</span></span><br/>

<span data-ttu-id="2babc-3469">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3469">1</span></span>

<span data-ttu-id="2babc-3470">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3470">2</span></span>

<span data-ttu-id="2babc-3471">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3471">3</span></span>

<span data-ttu-id="2babc-3472">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3472">4</span></span>

<span data-ttu-id="2babc-3473">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3473">5</span></span>

<span data-ttu-id="2babc-3474">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3474">6</span></span>

<span data-ttu-id="2babc-3475">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3475">7</span></span>

<span data-ttu-id="2babc-3476">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3476">8</span></span>

<span data-ttu-id="2babc-3477">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3477">9</span></span>

<span data-ttu-id="2babc-3478">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3478">2</span></span><br/> <span data-ttu-id="2babc-3479">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3479">0</span></span><br/>

<span data-ttu-id="2babc-3480">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3480">1</span></span>

<span data-ttu-id="2babc-3481">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3481">2</span></span>

<span data-ttu-id="2babc-3482">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3482">3</span></span>

<span data-ttu-id="2babc-3483">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3483">4</span></span>

<span data-ttu-id="2babc-3484">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3484">5</span></span>

<span data-ttu-id="2babc-3485">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3485">6</span></span>

<span data-ttu-id="2babc-3486">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3486">7</span></span>

<span data-ttu-id="2babc-3487">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3487">8</span></span>

<span data-ttu-id="2babc-3488">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3488">9</span></span>

<span data-ttu-id="2babc-3489">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3489">3</span></span><br/> <span data-ttu-id="2babc-3490">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3490">0</span></span><br/>

<span data-ttu-id="2babc-3491">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3491">1</span></span>

<span data-ttu-id="2babc-3492">\_Statut</span><span class="sxs-lookup"><span data-stu-id="2babc-3492">\_Status</span></span>

<span data-ttu-id="2babc-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="2babc-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="2babc-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="2babc-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="2babc-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="2babc-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="2babc-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="2babc-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="2babc-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="2babc-3497">\_iRowBmk</span></span>

<span data-ttu-id="2babc-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="2babc-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="2babc-3499">**\_ État**: l’une des statistiques \_ \* valeurs spécifiées dans la section 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="2babc-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="2babc-3500">**\_ cFilteredDocuments**: entier non signé 32 bits indiquant le nombre de documents qui ont été indexés</span><span class="sxs-lookup"><span data-stu-id="2babc-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="2babc-3501">**\_ cDocumentsToFilter**: entier non signé 32 bits indiquant le nombre de documents restant à indexer.</span><span class="sxs-lookup"><span data-stu-id="2babc-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="2babc-3502">**\_ dwRatioFinishedDenominator**: entier non signé 32 bits indiquant le dénominateur du rapport de documents dont la requête a terminé le traitement.</span><span class="sxs-lookup"><span data-stu-id="2babc-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="2babc-3503">**\_ dwRatioFinishedNumerator**: entier non signé 32 bits indiquant le numérateur du rapport de documents dont la requête a terminé le traitement.</span><span class="sxs-lookup"><span data-stu-id="2babc-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="2babc-3504">**\_ iRowBmk**: entier non signé 32 bits indiquant la position approximative du signet dans l’ensemble de lignes en termes de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="2babc-3505">**\_ cRowsTotal**: entier non signé 32 bits spécifiant le nombre total de lignes dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="2babc-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="2babc-3507">Le message CPMSetBindingsIn demande la liaison de colonnes à un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="2babc-3508">Le serveur répond au message de requête CPMSetBindingsIn à l’aide de la section d’en-tête du message CPMBindingsIn avec les résultats de la requête contenue dans le \_ champ État.</span><span class="sxs-lookup"><span data-stu-id="2babc-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="2babc-3509">Le format du message CPMSetBindingsIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3510">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3510">0</span></span>

<span data-ttu-id="2babc-3511">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3511">1</span></span>

<span data-ttu-id="2babc-3512">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3512">2</span></span>

<span data-ttu-id="2babc-3513">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3513">3</span></span>

<span data-ttu-id="2babc-3514">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3514">4</span></span>

<span data-ttu-id="2babc-3515">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3515">5</span></span>

<span data-ttu-id="2babc-3516">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3516">6</span></span>

<span data-ttu-id="2babc-3517">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3517">7</span></span>

<span data-ttu-id="2babc-3518">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3518">8</span></span>

<span data-ttu-id="2babc-3519">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3519">9</span></span>

<span data-ttu-id="2babc-3520">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3520">1</span></span><br/> <span data-ttu-id="2babc-3521">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3521">0</span></span><br/>

<span data-ttu-id="2babc-3522">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3522">1</span></span>

<span data-ttu-id="2babc-3523">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3523">2</span></span>

<span data-ttu-id="2babc-3524">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3524">3</span></span>

<span data-ttu-id="2babc-3525">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3525">4</span></span>

<span data-ttu-id="2babc-3526">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3526">5</span></span>

<span data-ttu-id="2babc-3527">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3527">6</span></span>

<span data-ttu-id="2babc-3528">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3528">7</span></span>

<span data-ttu-id="2babc-3529">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3529">8</span></span>

<span data-ttu-id="2babc-3530">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3530">9</span></span>

<span data-ttu-id="2babc-3531">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3531">2</span></span><br/> <span data-ttu-id="2babc-3532">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3532">0</span></span><br/>

<span data-ttu-id="2babc-3533">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3533">1</span></span>

<span data-ttu-id="2babc-3534">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3534">2</span></span>

<span data-ttu-id="2babc-3535">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3535">3</span></span>

<span data-ttu-id="2babc-3536">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3536">4</span></span>

<span data-ttu-id="2babc-3537">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3537">5</span></span>

<span data-ttu-id="2babc-3538">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3538">6</span></span>

<span data-ttu-id="2babc-3539">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3539">7</span></span>

<span data-ttu-id="2babc-3540">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3540">8</span></span>

<span data-ttu-id="2babc-3541">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3541">9</span></span>

<span data-ttu-id="2babc-3542">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3542">3</span></span><br/> <span data-ttu-id="2babc-3543">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3543">0</span></span><br/>

<span data-ttu-id="2babc-3544">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3544">1</span></span>

<span data-ttu-id="2babc-3545">\_hCursor (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="2babc-3546">\_cbRow (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="2babc-3547">\_cbBindingDesc (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="2babc-3548">\_factice (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3548">\_dummy (optional)</span></span>

<span data-ttu-id="2babc-3549">cColumns (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-3549">cColumns (optional)</span></span>

<span data-ttu-id="2babc-3550">aColumns (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="2babc-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="2babc-3551">**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut qui identifie la ligne pour laquelle définir des liaisons.</span><span class="sxs-lookup"><span data-stu-id="2babc-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="2babc-3552">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="2babc-3553">**\_ cbRow**: entier non signé 32 bits indiquant la taille, en octets, d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="2babc-3554">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="2babc-3555">**\_ cbBindingDesc**: entier non signé 32 bits indiquant la longueur, en octets, des champs qui suivent le \_ champ factice.</span><span class="sxs-lookup"><span data-stu-id="2babc-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="2babc-3556">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="2babc-3557">**\_ factice**: ce champ n’est pas utilisé et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2babc-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="2babc-3558">Il peut être défini sur n’importe quelle valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="2babc-3559">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="2babc-3560">**CColumns**: entier non signé 32 bits indiquant le nombre d’éléments dans le tableau aColumns.</span><span class="sxs-lookup"><span data-stu-id="2babc-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="2babc-3561">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="2babc-3562">**aColumns**: tableau des structures CTableColumn décrivant les colonnes d’une ligne dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="2babc-3563">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="2babc-3564">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="2babc-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="2babc-3565">Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.</span><span class="sxs-lookup"><span data-stu-id="2babc-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="2babc-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="2babc-3567">Le message CPMGetRowsIn demande des lignes d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="2babc-3568">Le format du message CPMGetRowsIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3569">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3569">0</span></span>

<span data-ttu-id="2babc-3570">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3570">1</span></span>

<span data-ttu-id="2babc-3571">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3571">2</span></span>

<span data-ttu-id="2babc-3572">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3572">3</span></span>

<span data-ttu-id="2babc-3573">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3573">4</span></span>

<span data-ttu-id="2babc-3574">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3574">5</span></span>

<span data-ttu-id="2babc-3575">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3575">6</span></span>

<span data-ttu-id="2babc-3576">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3576">7</span></span>

<span data-ttu-id="2babc-3577">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3577">8</span></span>

<span data-ttu-id="2babc-3578">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3578">9</span></span>

<span data-ttu-id="2babc-3579">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3579">1</span></span><br/> <span data-ttu-id="2babc-3580">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3580">0</span></span><br/>

<span data-ttu-id="2babc-3581">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3581">1</span></span>

<span data-ttu-id="2babc-3582">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3582">2</span></span>

<span data-ttu-id="2babc-3583">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3583">3</span></span>

<span data-ttu-id="2babc-3584">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3584">4</span></span>

<span data-ttu-id="2babc-3585">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3585">5</span></span>

<span data-ttu-id="2babc-3586">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3586">6</span></span>

<span data-ttu-id="2babc-3587">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3587">7</span></span>

<span data-ttu-id="2babc-3588">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3588">8</span></span>

<span data-ttu-id="2babc-3589">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3589">9</span></span>

<span data-ttu-id="2babc-3590">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3590">2</span></span><br/> <span data-ttu-id="2babc-3591">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3591">0</span></span><br/>

<span data-ttu-id="2babc-3592">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3592">1</span></span>

<span data-ttu-id="2babc-3593">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3593">2</span></span>

<span data-ttu-id="2babc-3594">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3594">3</span></span>

<span data-ttu-id="2babc-3595">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3595">4</span></span>

<span data-ttu-id="2babc-3596">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3596">5</span></span>

<span data-ttu-id="2babc-3597">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3597">6</span></span>

<span data-ttu-id="2babc-3598">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3598">7</span></span>

<span data-ttu-id="2babc-3599">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3599">8</span></span>

<span data-ttu-id="2babc-3600">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3600">9</span></span>

<span data-ttu-id="2babc-3601">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3601">3</span></span><br/> <span data-ttu-id="2babc-3602">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3602">0</span></span><br/>

<span data-ttu-id="2babc-3603">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3603">1</span></span>

<span data-ttu-id="2babc-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="2babc-3604">\_hCursor</span></span>

<span data-ttu-id="2babc-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="2babc-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="2babc-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="2babc-3606">\_cbRowWidth</span></span>

<span data-ttu-id="2babc-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="2babc-3607">\_cbSeek</span></span>

<span data-ttu-id="2babc-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="2babc-3608">\_cbReserved</span></span>

<span data-ttu-id="2babc-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="2babc-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="2babc-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="2babc-3610">\_ulClientBase</span></span>

<span data-ttu-id="2babc-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="2babc-3611">\_fBwdFetch</span></span>

<span data-ttu-id="2babc-3612">eType</span><span class="sxs-lookup"><span data-stu-id="2babc-3612">eType</span></span>

<span data-ttu-id="2babc-3613">\_chap</span><span class="sxs-lookup"><span data-stu-id="2babc-3613">\_chapt</span></span>

<span data-ttu-id="2babc-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="2babc-3614">SeekDescription</span></span>

<span data-ttu-id="2babc-3615">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3615">...</span></span>

<span data-ttu-id="2babc-3616">... variable</span><span class="sxs-lookup"><span data-stu-id="2babc-3616">... (variable)</span></span>



 

<span data-ttu-id="2babc-3617">**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les lignes doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="2babc-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="2babc-3618">**\_ cRowsToTransfer**: entier non signé 32 bits indiquant le nombre maximal de lignes que le client souhaite recevoir en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="2babc-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="2babc-3619">**\_ cbRowWidth**: entier non signé 32 bits indiquant la longueur d’une ligne, en octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="2babc-3620">**\_ cbSeek**: entier non signé 32 bits indiquant la taille du message commençant par ETYPE.</span><span class="sxs-lookup"><span data-stu-id="2babc-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="2babc-3621">**\_ cbReserved**: entier non signé 32 bits indiquant la taille, en octets, d’un message CPMGetRowsOut (sans les champs Rows et SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="2babc-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="2babc-3622">Cette valeur dans ce champ est ajoutée à la valeur du \_ champ cbSeek, puis doit être utilisée pour calculer le décalage du champ Rows dans le message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="2babc-3623">**\_ cbReadBuffer**: entier non signé 32 bits qui doit être défini sur la valeur maximale de la valeur de \_ cbRowWidth ou 1000 fois la valeur de \_ cRowsToTransfer, arrondie au multiple de 512 octets le plus proche.</span><span class="sxs-lookup"><span data-stu-id="2babc-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="2babc-3624">La valeur ne doit pas dépasser 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="2babc-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="2babc-3625">**\_ ulClientBase**: entier non signé 32 bits indiquant la valeur de base à utiliser pour les calculs de pointeur dans la mémoire tampon de ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="2babc-3626">Si des décalages 64 bits sont utilisés, le champ Reserved2 de l’en-tête de message est utilisé comme les 32 bits supérieurs et \_ ulClientBase en tant que 32 bits inférieur d’une valeur de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="2babc-3627">Pour plus d’informations, consultez la section 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="2babc-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="2babc-3628">**\_ fBwdFetch**: entier non signé 32 bits indiquant l’ordre dans lequel les lignes sont extraites.</span><span class="sxs-lookup"><span data-stu-id="2babc-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="2babc-3629">Si la valeur est définie sur 0x00000001, les lignes doivent être extraites dans l’ordre inverse.</span><span class="sxs-lookup"><span data-stu-id="2babc-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="2babc-3630">Si la valeur est 0x00000000, les lignes doivent être extraites dans l’ordre de transmission.</span><span class="sxs-lookup"><span data-stu-id="2babc-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="2babc-3631">NE doit avoir aucune autre valeur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="2babc-3632">**ETYPE**: entier non signé 32 bits contenant l’une des valeurs suivantes pour indiquer le type d’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="2babc-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="2babc-3633">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-3633">Value</span></span>                         | <span data-ttu-id="2babc-3634">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="2babc-3635">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="2babc-3636">SeekDescription contient une structure CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="2babc-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="2babc-3637">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="2babc-3638">SeekDescription contient une structure CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="2babc-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="2babc-3639">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="2babc-3640">SeekDescription contient une structure CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="2babc-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="2babc-3641">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="2babc-3642">SeekDescription contient une structure CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="2babc-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="2babc-3643">**\_ Chapt**: valeur 32 bits représentant le descripteur du chapitre de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="2babc-3644">**SeekDescription**: ce champ doit contenir une structure du type indiqué par la valeur ETYPE.</span><span class="sxs-lookup"><span data-stu-id="2babc-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="2babc-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="2babc-3646">Le message CPMGetRowsOut répond à un message CPMGetRowsIn avec les lignes d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="2babc-3647">Les serveurs doivent mettre en forme des décalages avec les types de données de longueur variable dans le champ Rows comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="2babc-3648">Le client a indiqué qu’il s’agissait d’un système 32 bits (0x00000008 ou moins dans le champ iClientVersion de CPMConnectIn) : les décalages sont des entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="2babc-3649">Le client a indiqué qu’il s’agissait d’un système 64 bits ( \_ iClientVersion > 0x00000008 dans CPMConnectIn) et que le serveur indiquait qu’il s’agissait d’un système 32 bits ( \_ ServerVersion défini sur 0X00000007 dans CPMConnectOut) : les décalages sont des entiers de 32 bits</span><span class="sxs-lookup"><span data-stu-id="2babc-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="2babc-3650">Le client a indiqué qu’il s’agissait d’un système 64 bits ( \_ iClientVersion > 0x00000008 dans CPMConnectIn) et que le serveur indiquait qu’il s’agissait d’un système 64 bits ( \_ ServerVersion défini sur 0X00010007 dans CPMConnectOut) : les décalages sont des entiers de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2babc-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="2babc-3651">Le format du message CPMGetRowsOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3652">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3652">0</span></span>

<span data-ttu-id="2babc-3653">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3653">1</span></span>

<span data-ttu-id="2babc-3654">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3654">2</span></span>

<span data-ttu-id="2babc-3655">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3655">3</span></span>

<span data-ttu-id="2babc-3656">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3656">4</span></span>

<span data-ttu-id="2babc-3657">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3657">5</span></span>

<span data-ttu-id="2babc-3658">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3658">6</span></span>

<span data-ttu-id="2babc-3659">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3659">7</span></span>

<span data-ttu-id="2babc-3660">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3660">8</span></span>

<span data-ttu-id="2babc-3661">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3661">9</span></span>

<span data-ttu-id="2babc-3662">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3662">1</span></span><br/> <span data-ttu-id="2babc-3663">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3663">0</span></span><br/>

<span data-ttu-id="2babc-3664">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3664">1</span></span>

<span data-ttu-id="2babc-3665">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3665">2</span></span>

<span data-ttu-id="2babc-3666">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3666">3</span></span>

<span data-ttu-id="2babc-3667">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3667">4</span></span>

<span data-ttu-id="2babc-3668">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3668">5</span></span>

<span data-ttu-id="2babc-3669">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3669">6</span></span>

<span data-ttu-id="2babc-3670">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3670">7</span></span>

<span data-ttu-id="2babc-3671">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3671">8</span></span>

<span data-ttu-id="2babc-3672">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3672">9</span></span>

<span data-ttu-id="2babc-3673">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3673">2</span></span><br/> <span data-ttu-id="2babc-3674">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3674">0</span></span><br/>

<span data-ttu-id="2babc-3675">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3675">1</span></span>

<span data-ttu-id="2babc-3676">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3676">2</span></span>

<span data-ttu-id="2babc-3677">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3677">3</span></span>

<span data-ttu-id="2babc-3678">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3678">4</span></span>

<span data-ttu-id="2babc-3679">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3679">5</span></span>

<span data-ttu-id="2babc-3680">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3680">6</span></span>

<span data-ttu-id="2babc-3681">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3681">7</span></span>

<span data-ttu-id="2babc-3682">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3682">8</span></span>

<span data-ttu-id="2babc-3683">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3683">9</span></span>

<span data-ttu-id="2babc-3684">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3684">3</span></span><br/> <span data-ttu-id="2babc-3685">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3685">0</span></span><br/>

<span data-ttu-id="2babc-3686">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3686">1</span></span>

<span data-ttu-id="2babc-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="2babc-3687">\_cRowsReturned</span></span>

<span data-ttu-id="2babc-3688">eType</span><span class="sxs-lookup"><span data-stu-id="2babc-3688">eType</span></span>

<span data-ttu-id="2babc-3689">\_chap</span><span class="sxs-lookup"><span data-stu-id="2babc-3689">\_chapt</span></span>

<span data-ttu-id="2babc-3690">SeekDescription (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="2babc-3691">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3691">...</span></span>

<span data-ttu-id="2babc-3692">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3692">...</span></span>

<span data-ttu-id="2babc-3693">paddingRows (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="2babc-3694">Lignes</span><span class="sxs-lookup"><span data-stu-id="2babc-3694">Rows</span></span>



 

<span data-ttu-id="2babc-3695">**\_ cRowsReturned**: entier non signé 32 bits indiquant le nombre de lignes retournées dans les lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="2babc-3696">**ETYPE**: entier non signé 32 bits contenant l’une des valeurs suivantes pour indiquer le type d’opération rowseek à effectuer</span><span class="sxs-lookup"><span data-stu-id="2babc-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="2babc-3697">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-3697">Value</span></span>                         | <span data-ttu-id="2babc-3698">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="2babc-3699">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="2babc-3700">Aucun SeekDescription, ignorer le champ SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="2babc-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="2babc-3701">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="2babc-3702">SeekDescription contient une structure CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="2babc-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="2babc-3703">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="2babc-3704">SeekDescription contient une structure CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="2babc-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="2babc-3705">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="2babc-3706">SeekDescription contient une structure CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="2babc-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="2babc-3707">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="2babc-3708">SeekDescription contient une structure CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="2babc-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="2babc-3709">**\_ Chapt**: valeur 32 bits représentant le descripteur du chapitre de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="2babc-3710">**SeekDescription**: ce champ doit contenir une structure du type indiqué par le champ ETYPE.</span><span class="sxs-lookup"><span data-stu-id="2babc-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="2babc-3711">**paddingRows**: ce champ doit avoir une longueur suffisante (de 0 à \_ cbReserved octets) pour remplir le champ de lignes à \_ cbReserved offset à partir du début d’un message, où \_ cbReserved est la valeur dans le message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="2babc-3712">Les octets de remplissage utilisés dans ce champ peuvent être n’importe quelle valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="2babc-3713">Ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="2babc-3714">**Lignes**: données de ligne, est mise en forme comme stipulé par les informations de colonne dans le message CPMSetBindingsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="2babc-3715">Les lignes doivent être stockées dans l’ordre de transfert (par exemple, ligne 1 avant la ligne 2).</span><span class="sxs-lookup"><span data-stu-id="2babc-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="2babc-3716">Les colonnes de taille fixe doivent être stockées aux décalages spécifiés par le message CPMSetBindingsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="2babc-3717">Les colonnes de taille variable (par exemple, les chaînes) doivent être stockées comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="2babc-3718">Les données de la variable proprement dite (par exemple, la chaîne) sont stockées vers la fin de la mémoire tampon dans l’ordre décroissant (par exemple, la collection de toutes les données de variable pour la ligne 1 est à la fin, ligne 2 la plus proche, etc.).</span><span class="sxs-lookup"><span data-stu-id="2babc-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="2babc-3719">La zone de taille fixe (au début de la mémoire tampon de ligne) doit contenir un CRowVariant pour chaque colonne, stockée au décalage spécifié dans le message CPMSetBindingsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="2babc-3720">vType doit contenir le type de données (par ex \_ ., VT LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="2babc-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="2babc-3721">Si, comme déterminé par les règles au début de la section de cette section, les décalages 32 bits sont utilisés, alors le champ offset dans CRowVariant doit contenir une valeur 32 bits qui correspond au décalage des données variables à partir du début du message CPMGetRowsOut, plus la valeur de \_ ulClientBase spécifiée dans le message CPMGetRowsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="2babc-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="2babc-3722">Si des décalages 64 bits sont utilisés, le champ de décalage dans CRowVariant doit contenir une valeur 64 bits qui correspond au décalage du début du message CPMGetRowsOut, ajouté à une valeur de 64 bits composée à l’aide de \_ ulClientBase comme 32 bits et ulReserved2 de poids \_ fort (32 bits).</span><span class="sxs-lookup"><span data-stu-id="2babc-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="2babc-3723">Par exemple, si le message CPMSetBindingsIn spécifiant deux colonnes-Size (VT \_ I4) et title (VT \_ LPWStr)-et \_ ulClientBase de CPMGetRowsIn a été 0x10000, deux lignes s’affichent comme suit.</span><span class="sxs-lookup"><span data-stu-id="2babc-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="2babc-3724">La section marquée en gris est la partie de longueur fixe de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2babc-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![exemple de message cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="2babc-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="2babc-3727">Le message CPMRatioFinishedIn demande le pourcentage d’achèvement d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="2babc-3728">Le format du message CPMRatioFinishedIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3729">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3729">0</span></span>

<span data-ttu-id="2babc-3730">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3730">1</span></span>

<span data-ttu-id="2babc-3731">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3731">2</span></span>

<span data-ttu-id="2babc-3732">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3732">3</span></span>

<span data-ttu-id="2babc-3733">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3733">4</span></span>

<span data-ttu-id="2babc-3734">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3734">5</span></span>

<span data-ttu-id="2babc-3735">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3735">6</span></span>

<span data-ttu-id="2babc-3736">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3736">7</span></span>

<span data-ttu-id="2babc-3737">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3737">8</span></span>

<span data-ttu-id="2babc-3738">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3738">9</span></span>

<span data-ttu-id="2babc-3739">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3739">1</span></span><br/> <span data-ttu-id="2babc-3740">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3740">0</span></span><br/>

<span data-ttu-id="2babc-3741">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3741">1</span></span>

<span data-ttu-id="2babc-3742">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3742">2</span></span>

<span data-ttu-id="2babc-3743">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3743">3</span></span>

<span data-ttu-id="2babc-3744">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3744">4</span></span>

<span data-ttu-id="2babc-3745">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3745">5</span></span>

<span data-ttu-id="2babc-3746">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3746">6</span></span>

<span data-ttu-id="2babc-3747">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3747">7</span></span>

<span data-ttu-id="2babc-3748">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3748">8</span></span>

<span data-ttu-id="2babc-3749">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3749">9</span></span>

<span data-ttu-id="2babc-3750">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3750">2</span></span><br/> <span data-ttu-id="2babc-3751">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3751">0</span></span><br/>

<span data-ttu-id="2babc-3752">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3752">1</span></span>

<span data-ttu-id="2babc-3753">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3753">2</span></span>

<span data-ttu-id="2babc-3754">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3754">3</span></span>

<span data-ttu-id="2babc-3755">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3755">4</span></span>

<span data-ttu-id="2babc-3756">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3756">5</span></span>

<span data-ttu-id="2babc-3757">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3757">6</span></span>

<span data-ttu-id="2babc-3758">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3758">7</span></span>

<span data-ttu-id="2babc-3759">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3759">8</span></span>

<span data-ttu-id="2babc-3760">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3760">9</span></span>

<span data-ttu-id="2babc-3761">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3761">3</span></span><br/> <span data-ttu-id="2babc-3762">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3762">0</span></span><br/>

<span data-ttu-id="2babc-3763">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3763">1</span></span>

<span data-ttu-id="2babc-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="2babc-3764">\_hCursor</span></span>

<span data-ttu-id="2babc-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="2babc-3765">\_fQuick</span></span>



 

<span data-ttu-id="2babc-3766">**\_ hCursor**: descripteur du message CPMCreateQueryOut identifiant la requête pour laquelle des informations de saisie semi-automatique doivent être demandées.</span><span class="sxs-lookup"><span data-stu-id="2babc-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="2babc-3767">**\_ fQuick**: doit être défini sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="2babc-3768">Inutilisé et doit être ignoré par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="2babc-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="2babc-3770">Le message CPMRatioFinishedOut répond à un message CPMRatioFinishedIn avec le ratio d’achèvement d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="2babc-3771">Le format du message CPMRatioFinishedOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3772">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3772">0</span></span>

<span data-ttu-id="2babc-3773">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3773">1</span></span>

<span data-ttu-id="2babc-3774">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3774">2</span></span>

<span data-ttu-id="2babc-3775">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3775">3</span></span>

<span data-ttu-id="2babc-3776">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3776">4</span></span>

<span data-ttu-id="2babc-3777">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3777">5</span></span>

<span data-ttu-id="2babc-3778">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3778">6</span></span>

<span data-ttu-id="2babc-3779">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3779">7</span></span>

<span data-ttu-id="2babc-3780">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3780">8</span></span>

<span data-ttu-id="2babc-3781">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3781">9</span></span>

<span data-ttu-id="2babc-3782">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3782">1</span></span><br/> <span data-ttu-id="2babc-3783">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3783">0</span></span><br/>

<span data-ttu-id="2babc-3784">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3784">1</span></span>

<span data-ttu-id="2babc-3785">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3785">2</span></span>

<span data-ttu-id="2babc-3786">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3786">3</span></span>

<span data-ttu-id="2babc-3787">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3787">4</span></span>

<span data-ttu-id="2babc-3788">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3788">5</span></span>

<span data-ttu-id="2babc-3789">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3789">6</span></span>

<span data-ttu-id="2babc-3790">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3790">7</span></span>

<span data-ttu-id="2babc-3791">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3791">8</span></span>

<span data-ttu-id="2babc-3792">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3792">9</span></span>

<span data-ttu-id="2babc-3793">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3793">2</span></span><br/> <span data-ttu-id="2babc-3794">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3794">0</span></span><br/>

<span data-ttu-id="2babc-3795">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3795">1</span></span>

<span data-ttu-id="2babc-3796">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3796">2</span></span>

<span data-ttu-id="2babc-3797">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3797">3</span></span>

<span data-ttu-id="2babc-3798">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3798">4</span></span>

<span data-ttu-id="2babc-3799">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3799">5</span></span>

<span data-ttu-id="2babc-3800">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3800">6</span></span>

<span data-ttu-id="2babc-3801">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3801">7</span></span>

<span data-ttu-id="2babc-3802">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3802">8</span></span>

<span data-ttu-id="2babc-3803">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3803">9</span></span>

<span data-ttu-id="2babc-3804">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3804">3</span></span><br/> <span data-ttu-id="2babc-3805">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3805">0</span></span><br/>

<span data-ttu-id="2babc-3806">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3806">1</span></span>

<span data-ttu-id="2babc-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="2babc-3807">\_ ulNumerator</span></span>

<span data-ttu-id="2babc-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="2babc-3808">\_ulDenominator</span></span>

<span data-ttu-id="2babc-3809">\_cRows</span><span class="sxs-lookup"><span data-stu-id="2babc-3809">\_cRows</span></span>

<span data-ttu-id="2babc-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="2babc-3810">\_fNewRows</span></span>



 

<span data-ttu-id="2babc-3811">**\_ ulNumerator**: entier non signé 32 bits indiquant le numérateur du rapport d’achèvement en termes de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="2babc-3812">**\_ ulDenominator**: entier non signé 32 bits indiquant le dénominateur du rapport d’achèvement en termes de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="2babc-3813">DOIT être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="2babc-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="2babc-3814">**\_ Crows**: entier non signé 32 bits indiquant le nombre total de lignes de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="2babc-3815">**\_ fNewRows**: valeur booléenne indiquant si de nouvelles lignes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="2babc-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="2babc-3816">La valeur 0x00000001 indique que les nouvelles lignes sont disponibles dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="2babc-3817">La valeur 0x00000000 indique que l’ensemble de lignes ne contient pas de nouvelles lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="2babc-3818">Ce champ ne doit avoir aucune autre valeur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="2babc-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="2babc-3820">Le message CPMFetchValueIn demande une valeur de propriété qui était trop grande pour être renvoyée dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="2babc-3821">Comme indiqué dans la section 3.2.4.2.5, ce message est envoyé à plusieurs reprises pour récupérer tous les octets de la propriété, en mettant à jour \_ cbSoFar pour chacun, jusqu’à ce que le \_ champ fMoreExists du message CPMFetchValueOut soit défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="2babc-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="2babc-3822">Le format du message CPMFetchValueIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3823">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3823">0</span></span>

<span data-ttu-id="2babc-3824">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3824">1</span></span>

<span data-ttu-id="2babc-3825">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3825">2</span></span>

<span data-ttu-id="2babc-3826">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3826">3</span></span>

<span data-ttu-id="2babc-3827">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3827">4</span></span>

<span data-ttu-id="2babc-3828">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3828">5</span></span>

<span data-ttu-id="2babc-3829">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3829">6</span></span>

<span data-ttu-id="2babc-3830">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3830">7</span></span>

<span data-ttu-id="2babc-3831">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3831">8</span></span>

<span data-ttu-id="2babc-3832">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3832">9</span></span>

<span data-ttu-id="2babc-3833">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3833">1</span></span><br/> <span data-ttu-id="2babc-3834">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3834">0</span></span><br/>

<span data-ttu-id="2babc-3835">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3835">1</span></span>

<span data-ttu-id="2babc-3836">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3836">2</span></span>

<span data-ttu-id="2babc-3837">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3837">3</span></span>

<span data-ttu-id="2babc-3838">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3838">4</span></span>

<span data-ttu-id="2babc-3839">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3839">5</span></span>

<span data-ttu-id="2babc-3840">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3840">6</span></span>

<span data-ttu-id="2babc-3841">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3841">7</span></span>

<span data-ttu-id="2babc-3842">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3842">8</span></span>

<span data-ttu-id="2babc-3843">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3843">9</span></span>

<span data-ttu-id="2babc-3844">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3844">2</span></span><br/> <span data-ttu-id="2babc-3845">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3845">0</span></span><br/>

<span data-ttu-id="2babc-3846">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3846">1</span></span>

<span data-ttu-id="2babc-3847">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3847">2</span></span>

<span data-ttu-id="2babc-3848">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3848">3</span></span>

<span data-ttu-id="2babc-3849">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3849">4</span></span>

<span data-ttu-id="2babc-3850">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3850">5</span></span>

<span data-ttu-id="2babc-3851">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3851">6</span></span>

<span data-ttu-id="2babc-3852">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3852">7</span></span>

<span data-ttu-id="2babc-3853">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3853">8</span></span>

<span data-ttu-id="2babc-3854">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3854">9</span></span>

<span data-ttu-id="2babc-3855">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3855">3</span></span><br/> <span data-ttu-id="2babc-3856">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3856">0</span></span><br/>

<span data-ttu-id="2babc-3857">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3857">1</span></span>

<span data-ttu-id="2babc-3858">\_wid</span><span class="sxs-lookup"><span data-stu-id="2babc-3858">\_wid</span></span>

<span data-ttu-id="2babc-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="2babc-3859">\_cbSoFar</span></span>

<span data-ttu-id="2babc-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="2babc-3860">\_cbPropSpec</span></span>

<span data-ttu-id="2babc-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="2babc-3861">\_cbChunk</span></span>

<span data-ttu-id="2babc-3862">PropSpec (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3862">PropSpec (variable)</span></span>

<span data-ttu-id="2babc-3863">...</span><span class="sxs-lookup"><span data-stu-id="2babc-3863">...</span></span>

<span data-ttu-id="2babc-3864">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="2babc-3865">**\_ wid**: entier non signé 32 bits contenant des informations sur l’ID de document identifiant le document pour lequel une propriété doit être extraite.</span><span class="sxs-lookup"><span data-stu-id="2babc-3865">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="2babc-3866">**\_ cbSoFar**: entier non signé 32 bits contenant le nombre d’octets transférés précédemment pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="2babc-3867">DOIT être défini sur 0x00000000 dans le premier message.</span><span class="sxs-lookup"><span data-stu-id="2babc-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="2babc-3868">**\_ cbPropSpec**: entier non signé 32 bits contenant la taille du champ PropSpec, en octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="2babc-3869">**\_ cbChunk**: entier non signé 32 bits contenant le nombre maximal d’octets que l’expéditeur peut accepter dans un message CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="2babc-3870">*Comportement de Windows : ce champ est défini sur 0x00004000 pour toutes les versions de Windows.*</span><span class="sxs-lookup"><span data-stu-id="2babc-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="2babc-3871">**PropSpec**: structure CFullPropSpec spécifiant la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2babc-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="2babc-3872">**\_ remplissage**: ce champ doit avoir la longueur nécessaire (de 0 à 3 octets) pour remplir le message sur un multiple de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="2babc-3873">La valeur des octets de remplissage peut être n’importe quelle valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="2babc-3874">Ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="2babc-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="2babc-3876">Le message CPMFetchValueOut répond à un message CPMFetchValueIn avec une valeur de propriété d’une requête précédente.</span><span class="sxs-lookup"><span data-stu-id="2babc-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="2babc-3877">Comme indiqué dans la section 3.1.5.2.8, ce message est envoyé après chaque message CPMFetchValueIn jusqu’à ce que tous les octets de la propriété soient transférés.</span><span class="sxs-lookup"><span data-stu-id="2babc-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="2babc-3878">Le format du message CPMFetchValueOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3879">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3879">0</span></span>

<span data-ttu-id="2babc-3880">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3880">1</span></span>

<span data-ttu-id="2babc-3881">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3881">2</span></span>

<span data-ttu-id="2babc-3882">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3882">3</span></span>

<span data-ttu-id="2babc-3883">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3883">4</span></span>

<span data-ttu-id="2babc-3884">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3884">5</span></span>

<span data-ttu-id="2babc-3885">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3885">6</span></span>

<span data-ttu-id="2babc-3886">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3886">7</span></span>

<span data-ttu-id="2babc-3887">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3887">8</span></span>

<span data-ttu-id="2babc-3888">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3888">9</span></span>

<span data-ttu-id="2babc-3889">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3889">1</span></span><br/> <span data-ttu-id="2babc-3890">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3890">0</span></span><br/>

<span data-ttu-id="2babc-3891">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3891">1</span></span>

<span data-ttu-id="2babc-3892">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3892">2</span></span>

<span data-ttu-id="2babc-3893">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3893">3</span></span>

<span data-ttu-id="2babc-3894">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3894">4</span></span>

<span data-ttu-id="2babc-3895">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3895">5</span></span>

<span data-ttu-id="2babc-3896">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3896">6</span></span>

<span data-ttu-id="2babc-3897">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3897">7</span></span>

<span data-ttu-id="2babc-3898">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3898">8</span></span>

<span data-ttu-id="2babc-3899">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3899">9</span></span>

<span data-ttu-id="2babc-3900">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3900">2</span></span><br/> <span data-ttu-id="2babc-3901">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3901">0</span></span><br/>

<span data-ttu-id="2babc-3902">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3902">1</span></span>

<span data-ttu-id="2babc-3903">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3903">2</span></span>

<span data-ttu-id="2babc-3904">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3904">3</span></span>

<span data-ttu-id="2babc-3905">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3905">4</span></span>

<span data-ttu-id="2babc-3906">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3906">5</span></span>

<span data-ttu-id="2babc-3907">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3907">6</span></span>

<span data-ttu-id="2babc-3908">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3908">7</span></span>

<span data-ttu-id="2babc-3909">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3909">8</span></span>

<span data-ttu-id="2babc-3910">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3910">9</span></span>

<span data-ttu-id="2babc-3911">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3911">3</span></span><br/> <span data-ttu-id="2babc-3912">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3912">0</span></span><br/>

<span data-ttu-id="2babc-3913">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3913">1</span></span>

<span data-ttu-id="2babc-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="2babc-3914">\_cbValue</span></span>

<span data-ttu-id="2babc-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="2babc-3915">\_fMoreExists</span></span>

<span data-ttu-id="2babc-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="2babc-3916">\_fValueExists</span></span>

<span data-ttu-id="2babc-3917">vType</span><span class="sxs-lookup"><span data-stu-id="2babc-3917">vType</span></span>

<span data-ttu-id="2babc-3918">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="2babc-3918">vValue (variable)</span></span>



 

<span data-ttu-id="2babc-3919">**\_ cbValue**: entier non signé 32 bits contenant la taille totale, en octets, dans vValue.</span><span class="sxs-lookup"><span data-stu-id="2babc-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="2babc-3920">**\_ fMoreExists**: valeur booléenne indiquant si des messages CPMFetchValueOut supplémentaires sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="2babc-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="2babc-3921">S’il est défini sur 0x00000001, il y a des messages CPMFetchValueOut supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2babc-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="2babc-3922">Si la valeur est 0x00000000, aucun message CPMFetchValueOut supplémentaire n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="2babc-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="2babc-3923">**\_ fValueExists**: valeur booléenne indiquant s’il existe une valeur pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="2babc-3924">Si la valeur est définie sur 0x00000001, il existe une valeur pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="2babc-3925">Si la valeur est 0x00000000, la valeur de la propriété n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="2babc-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="2babc-3926">**vType**: une valeur de l’énumération VarEnum, consultez la section 2.2.1.1 pour plus d’informations, décrivant le type de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="2babc-3927">**vValue**: partie d’un tableau d’octets contenant une structure SERIALIZEDPROPERTYVALUE telle que spécifiée dans la section 2.2.1.32, où l’offset du début de la partie est la valeur de \_ cbSoFar dans CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="2babc-3928">La longueur de la partie, indiquée par le \_ champ cbValue, doit être égale à la valeur de \_ CbChunk dans CPMFetchValueIn si \_ fMoreExists est défini sur 0x00000001 et doit être inférieur ou égal à la valeur de cbChunk dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2babc-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="2babc-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="2babc-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="2babc-3930">Le message CPMGetNotify demande que le client souhaite être averti des modifications de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="2babc-3931">Le message ne doit pas inclure un corps ; seul l’en-tête de message, tel que spécifié dans la section 2.2.2, doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="2babc-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="2babc-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="2babc-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="2babc-3933">Le message CPMSendNotifyOut avertit le client qu’une modification a été apportée aux résultats d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="2babc-3934">Ce message est envoyé uniquement lorsqu’une modification se produit.</span><span class="sxs-lookup"><span data-stu-id="2babc-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="2babc-3935">Le format du message CPMSendNotifyOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-3936">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3936">0</span></span>

<span data-ttu-id="2babc-3937">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3937">1</span></span>

<span data-ttu-id="2babc-3938">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3938">2</span></span>

<span data-ttu-id="2babc-3939">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3939">3</span></span>

<span data-ttu-id="2babc-3940">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3940">4</span></span>

<span data-ttu-id="2babc-3941">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3941">5</span></span>

<span data-ttu-id="2babc-3942">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3942">6</span></span>

<span data-ttu-id="2babc-3943">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3943">7</span></span>

<span data-ttu-id="2babc-3944">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3944">8</span></span>

<span data-ttu-id="2babc-3945">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3945">9</span></span>

<span data-ttu-id="2babc-3946">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3946">1</span></span><br/> <span data-ttu-id="2babc-3947">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3947">0</span></span><br/>

<span data-ttu-id="2babc-3948">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3948">1</span></span>

<span data-ttu-id="2babc-3949">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3949">2</span></span>

<span data-ttu-id="2babc-3950">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3950">3</span></span>

<span data-ttu-id="2babc-3951">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3951">4</span></span>

<span data-ttu-id="2babc-3952">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3952">5</span></span>

<span data-ttu-id="2babc-3953">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3953">6</span></span>

<span data-ttu-id="2babc-3954">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3954">7</span></span>

<span data-ttu-id="2babc-3955">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3955">8</span></span>

<span data-ttu-id="2babc-3956">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3956">9</span></span>

<span data-ttu-id="2babc-3957">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3957">2</span></span><br/> <span data-ttu-id="2babc-3958">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3958">0</span></span><br/>

<span data-ttu-id="2babc-3959">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3959">1</span></span>

<span data-ttu-id="2babc-3960">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3960">2</span></span>

<span data-ttu-id="2babc-3961">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3961">3</span></span>

<span data-ttu-id="2babc-3962">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3962">4</span></span>

<span data-ttu-id="2babc-3963">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3963">5</span></span>

<span data-ttu-id="2babc-3964">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3964">6</span></span>

<span data-ttu-id="2babc-3965">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3965">7</span></span>

<span data-ttu-id="2babc-3966">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3966">8</span></span>

<span data-ttu-id="2babc-3967">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3967">9</span></span>

<span data-ttu-id="2babc-3968">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3968">3</span></span><br/> <span data-ttu-id="2babc-3969">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3969">0</span></span><br/>

<span data-ttu-id="2babc-3970">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3970">1</span></span>

<span data-ttu-id="2babc-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="2babc-3971">\_watchNotify</span></span>



 

<span data-ttu-id="2babc-3972">**\_ watchNotify**: modification de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="2babc-3973">Il doit s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="2babc-3974">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-3974">Value</span></span>                                     | <span data-ttu-id="2babc-3975">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="2babc-3976">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="2babc-3977">Le nombre de lignes dans l’ensemble de lignes de requête a changé.</span><span class="sxs-lookup"><span data-stu-id="2babc-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="2babc-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="2babc-3979">La requête est terminée.</span><span class="sxs-lookup"><span data-stu-id="2babc-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="2babc-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="2babc-3981">La requête a été réexécutée.</span><span class="sxs-lookup"><span data-stu-id="2babc-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="2babc-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="2babc-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="2babc-3983">Le message CPMGetApproximatePositionIn demande la position approximative d’un signet dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="2babc-3984">Le format du message CPMGetApproximatePositionIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-3985">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3985">0</span></span>

<span data-ttu-id="2babc-3986">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3986">1</span></span>

<span data-ttu-id="2babc-3987">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3987">2</span></span>

<span data-ttu-id="2babc-3988">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3988">3</span></span>

<span data-ttu-id="2babc-3989">4</span><span class="sxs-lookup"><span data-stu-id="2babc-3989">4</span></span>

<span data-ttu-id="2babc-3990">5</span><span class="sxs-lookup"><span data-stu-id="2babc-3990">5</span></span>

<span data-ttu-id="2babc-3991">6</span><span class="sxs-lookup"><span data-stu-id="2babc-3991">6</span></span>

<span data-ttu-id="2babc-3992">7</span><span class="sxs-lookup"><span data-stu-id="2babc-3992">7</span></span>

<span data-ttu-id="2babc-3993">8</span><span class="sxs-lookup"><span data-stu-id="2babc-3993">8</span></span>

<span data-ttu-id="2babc-3994">9</span><span class="sxs-lookup"><span data-stu-id="2babc-3994">9</span></span>

<span data-ttu-id="2babc-3995">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3995">1</span></span><br/> <span data-ttu-id="2babc-3996">0</span><span class="sxs-lookup"><span data-stu-id="2babc-3996">0</span></span><br/>

<span data-ttu-id="2babc-3997">1</span><span class="sxs-lookup"><span data-stu-id="2babc-3997">1</span></span>

<span data-ttu-id="2babc-3998">2</span><span class="sxs-lookup"><span data-stu-id="2babc-3998">2</span></span>

<span data-ttu-id="2babc-3999">3</span><span class="sxs-lookup"><span data-stu-id="2babc-3999">3</span></span>

<span data-ttu-id="2babc-4000">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4000">4</span></span>

<span data-ttu-id="2babc-4001">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4001">5</span></span>

<span data-ttu-id="2babc-4002">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4002">6</span></span>

<span data-ttu-id="2babc-4003">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4003">7</span></span>

<span data-ttu-id="2babc-4004">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4004">8</span></span>

<span data-ttu-id="2babc-4005">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4005">9</span></span>

<span data-ttu-id="2babc-4006">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4006">2</span></span><br/> <span data-ttu-id="2babc-4007">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4007">0</span></span><br/>

<span data-ttu-id="2babc-4008">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4008">1</span></span>

<span data-ttu-id="2babc-4009">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4009">2</span></span>

<span data-ttu-id="2babc-4010">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4010">3</span></span>

<span data-ttu-id="2babc-4011">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4011">4</span></span>

<span data-ttu-id="2babc-4012">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4012">5</span></span>

<span data-ttu-id="2babc-4013">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4013">6</span></span>

<span data-ttu-id="2babc-4014">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4014">7</span></span>

<span data-ttu-id="2babc-4015">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4015">8</span></span>

<span data-ttu-id="2babc-4016">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4016">9</span></span>

<span data-ttu-id="2babc-4017">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4017">3</span></span><br/> <span data-ttu-id="2babc-4018">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4018">0</span></span><br/>

<span data-ttu-id="2babc-4019">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4019">1</span></span>

<span data-ttu-id="2babc-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="2babc-4020">\_hCursor</span></span>

<span data-ttu-id="2babc-4021">\_chap</span><span class="sxs-lookup"><span data-stu-id="2babc-4021">\_chapt</span></span>

<span data-ttu-id="2babc-4022">\_bmk</span><span class="sxs-lookup"><span data-stu-id="2babc-4022">\_bmk</span></span>



 

<span data-ttu-id="2babc-4023">**\_ hCursor**: valeur 32 bits représentant le curseur de requête obtenu à partir de CPMCreateQueryOut pour l’ensemble de lignes contenant le signet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="2babc-4024">**\_ Chapt**: valeur 32 bits représentant le handle du chapitre contenant le signet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="2babc-4025">**\_ BMK**: valeur 32 bits représentant le handle du signet pour lequel récupérer la position approximative.</span><span class="sxs-lookup"><span data-stu-id="2babc-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="2babc-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="2babc-4027">Le message CPMGetApproximatePositionOut répond à un message CPMGetApproximatePositionIn décrivant la position approximative du signet dans le chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="2babc-4028">Le format du message CPMGetApproximatePositionOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-4029">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4029">0</span></span>

<span data-ttu-id="2babc-4030">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4030">1</span></span>

<span data-ttu-id="2babc-4031">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4031">2</span></span>

<span data-ttu-id="2babc-4032">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4032">3</span></span>

<span data-ttu-id="2babc-4033">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4033">4</span></span>

<span data-ttu-id="2babc-4034">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4034">5</span></span>

<span data-ttu-id="2babc-4035">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4035">6</span></span>

<span data-ttu-id="2babc-4036">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4036">7</span></span>

<span data-ttu-id="2babc-4037">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4037">8</span></span>

<span data-ttu-id="2babc-4038">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4038">9</span></span>

<span data-ttu-id="2babc-4039">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4039">1</span></span><br/> <span data-ttu-id="2babc-4040">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4040">0</span></span><br/>

<span data-ttu-id="2babc-4041">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4041">1</span></span>

<span data-ttu-id="2babc-4042">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4042">2</span></span>

<span data-ttu-id="2babc-4043">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4043">3</span></span>

<span data-ttu-id="2babc-4044">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4044">4</span></span>

<span data-ttu-id="2babc-4045">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4045">5</span></span>

<span data-ttu-id="2babc-4046">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4046">6</span></span>

<span data-ttu-id="2babc-4047">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4047">7</span></span>

<span data-ttu-id="2babc-4048">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4048">8</span></span>

<span data-ttu-id="2babc-4049">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4049">9</span></span>

<span data-ttu-id="2babc-4050">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4050">2</span></span><br/> <span data-ttu-id="2babc-4051">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4051">0</span></span><br/>

<span data-ttu-id="2babc-4052">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4052">1</span></span>

<span data-ttu-id="2babc-4053">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4053">2</span></span>

<span data-ttu-id="2babc-4054">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4054">3</span></span>

<span data-ttu-id="2babc-4055">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4055">4</span></span>

<span data-ttu-id="2babc-4056">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4056">5</span></span>

<span data-ttu-id="2babc-4057">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4057">6</span></span>

<span data-ttu-id="2babc-4058">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4058">7</span></span>

<span data-ttu-id="2babc-4059">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4059">8</span></span>

<span data-ttu-id="2babc-4060">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4060">9</span></span>

<span data-ttu-id="2babc-4061">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4061">3</span></span><br/> <span data-ttu-id="2babc-4062">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4062">0</span></span><br/>

<span data-ttu-id="2babc-4063">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4063">1</span></span>

<span data-ttu-id="2babc-4064">\_numerator</span><span class="sxs-lookup"><span data-stu-id="2babc-4064">\_numerator</span></span>

<span data-ttu-id="2babc-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="2babc-4065">\_denominator</span></span>



 

<span data-ttu-id="2babc-4066">**\_ numérateur**: entier non signé 32 bits contenant le numéro de ligne du signet dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="2babc-4067">En l’absence de lignes, ce champ doit avoir la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="2babc-4068">**\_ dénominateur**: entier non signé 32 bits contenant le nombre de lignes dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="2babc-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="2babc-4070">Le message CPMCompareBmkIn demande une comparaison de deux signets dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="2babc-4071">Le format du message CPMCompareBmkIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-4072">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4072">0</span></span>

<span data-ttu-id="2babc-4073">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4073">1</span></span>

<span data-ttu-id="2babc-4074">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4074">2</span></span>

<span data-ttu-id="2babc-4075">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4075">3</span></span>

<span data-ttu-id="2babc-4076">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4076">4</span></span>

<span data-ttu-id="2babc-4077">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4077">5</span></span>

<span data-ttu-id="2babc-4078">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4078">6</span></span>

<span data-ttu-id="2babc-4079">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4079">7</span></span>

<span data-ttu-id="2babc-4080">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4080">8</span></span>

<span data-ttu-id="2babc-4081">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4081">9</span></span>

<span data-ttu-id="2babc-4082">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4082">1</span></span><br/> <span data-ttu-id="2babc-4083">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4083">0</span></span><br/>

<span data-ttu-id="2babc-4084">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4084">1</span></span>

<span data-ttu-id="2babc-4085">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4085">2</span></span>

<span data-ttu-id="2babc-4086">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4086">3</span></span>

<span data-ttu-id="2babc-4087">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4087">4</span></span>

<span data-ttu-id="2babc-4088">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4088">5</span></span>

<span data-ttu-id="2babc-4089">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4089">6</span></span>

<span data-ttu-id="2babc-4090">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4090">7</span></span>

<span data-ttu-id="2babc-4091">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4091">8</span></span>

<span data-ttu-id="2babc-4092">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4092">9</span></span>

<span data-ttu-id="2babc-4093">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4093">2</span></span><br/> <span data-ttu-id="2babc-4094">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4094">0</span></span><br/>

<span data-ttu-id="2babc-4095">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4095">1</span></span>

<span data-ttu-id="2babc-4096">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4096">2</span></span>

<span data-ttu-id="2babc-4097">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4097">3</span></span>

<span data-ttu-id="2babc-4098">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4098">4</span></span>

<span data-ttu-id="2babc-4099">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4099">5</span></span>

<span data-ttu-id="2babc-4100">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4100">6</span></span>

<span data-ttu-id="2babc-4101">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4101">7</span></span>

<span data-ttu-id="2babc-4102">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4102">8</span></span>

<span data-ttu-id="2babc-4103">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4103">9</span></span>

<span data-ttu-id="2babc-4104">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4104">3</span></span><br/> <span data-ttu-id="2babc-4105">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4105">0</span></span><br/>

<span data-ttu-id="2babc-4106">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4106">1</span></span>

<span data-ttu-id="2babc-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="2babc-4107">\_hCursor</span></span>

<span data-ttu-id="2babc-4108">\_chap</span><span class="sxs-lookup"><span data-stu-id="2babc-4108">\_chapt</span></span>

<span data-ttu-id="2babc-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="2babc-4109">\_bmkFirst</span></span>

<span data-ttu-id="2babc-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="2babc-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="2babc-4111">\_**hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut pour l’ensemble de lignes contenant les signets.</span><span class="sxs-lookup"><span data-stu-id="2babc-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="2babc-4112">\_**Chapt**: valeur de 32 bits représentant le descripteur du chapitre contenant les signets à comparer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="2babc-4113">\_**bmkFirst**: valeur 32 bits représentant le handle du premier signet à comparer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="2babc-4114">\_**bmkSecond**: valeur 32 bits représentant le handle du deuxième signet à comparer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="2babc-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="2babc-4116">Le message CPMCompareBmkOut répond à un message CPMCompareBmkIn avec la comparaison des deux signets du chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="2babc-4117">Le format du message CPMCompareBmkOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-4118">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4118">0</span></span>

<span data-ttu-id="2babc-4119">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4119">1</span></span>

<span data-ttu-id="2babc-4120">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4120">2</span></span>

<span data-ttu-id="2babc-4121">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4121">3</span></span>

<span data-ttu-id="2babc-4122">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4122">4</span></span>

<span data-ttu-id="2babc-4123">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4123">5</span></span>

<span data-ttu-id="2babc-4124">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4124">6</span></span>

<span data-ttu-id="2babc-4125">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4125">7</span></span>

<span data-ttu-id="2babc-4126">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4126">8</span></span>

<span data-ttu-id="2babc-4127">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4127">9</span></span>

<span data-ttu-id="2babc-4128">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4128">1</span></span><br/> <span data-ttu-id="2babc-4129">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4129">0</span></span><br/>

<span data-ttu-id="2babc-4130">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4130">1</span></span>

<span data-ttu-id="2babc-4131">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4131">2</span></span>

<span data-ttu-id="2babc-4132">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4132">3</span></span>

<span data-ttu-id="2babc-4133">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4133">4</span></span>

<span data-ttu-id="2babc-4134">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4134">5</span></span>

<span data-ttu-id="2babc-4135">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4135">6</span></span>

<span data-ttu-id="2babc-4136">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4136">7</span></span>

<span data-ttu-id="2babc-4137">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4137">8</span></span>

<span data-ttu-id="2babc-4138">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4138">9</span></span>

<span data-ttu-id="2babc-4139">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4139">2</span></span><br/> <span data-ttu-id="2babc-4140">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4140">0</span></span><br/>

<span data-ttu-id="2babc-4141">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4141">1</span></span>

<span data-ttu-id="2babc-4142">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4142">2</span></span>

<span data-ttu-id="2babc-4143">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4143">3</span></span>

<span data-ttu-id="2babc-4144">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4144">4</span></span>

<span data-ttu-id="2babc-4145">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4145">5</span></span>

<span data-ttu-id="2babc-4146">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4146">6</span></span>

<span data-ttu-id="2babc-4147">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4147">7</span></span>

<span data-ttu-id="2babc-4148">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4148">8</span></span>

<span data-ttu-id="2babc-4149">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4149">9</span></span>

<span data-ttu-id="2babc-4150">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4150">3</span></span><br/> <span data-ttu-id="2babc-4151">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4151">0</span></span><br/>

<span data-ttu-id="2babc-4152">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4152">1</span></span>

<span data-ttu-id="2babc-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="2babc-4153">\_dwComparison</span></span>



 

<span data-ttu-id="2babc-4154">\_**dwComparison**: l’une des valeurs suivantes, indiquant les positions relatives des deux signets dans le chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="2babc-4155">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-4155">Value</span></span>                               | <span data-ttu-id="2babc-4156">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2babc-4157">DBCOMPARE \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="2babc-4158">Le premier signet est positionné avant le deuxième.</span><span class="sxs-lookup"><span data-stu-id="2babc-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="2babc-4159">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="2babc-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="2babc-4160">Le premier signet a la même position que le second.</span><span class="sxs-lookup"><span data-stu-id="2babc-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="2babc-4161">DBCOMPARE \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="2babc-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="2babc-4162">Le premier signet est positionné après le deuxième.</span><span class="sxs-lookup"><span data-stu-id="2babc-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="2babc-4163">DBCOMPARE ne \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="2babc-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="2babc-4164">Le premier signet n’a pas la même position que le second.</span><span class="sxs-lookup"><span data-stu-id="2babc-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="2babc-4165">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="2babc-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="2babc-4166">Le premier signet n’est pas comparable au second.</span><span class="sxs-lookup"><span data-stu-id="2babc-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="2babc-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="2babc-4168">Le message CPMRestartPositionIn déplace la position d’extraction d’un curseur vers le début du chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="2babc-4169">Comme indiqué dans la section 3.1.5.2.12, le serveur répondra en utilisant le même message, avec les résultats de la requête contenus dans le \_ champ Status de l’en-tête CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="2babc-4170">Le format du message CPMRestartPositionIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-4171">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4171">0</span></span>

<span data-ttu-id="2babc-4172">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4172">1</span></span>

<span data-ttu-id="2babc-4173">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4173">2</span></span>

<span data-ttu-id="2babc-4174">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4174">3</span></span>

<span data-ttu-id="2babc-4175">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4175">4</span></span>

<span data-ttu-id="2babc-4176">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4176">5</span></span>

<span data-ttu-id="2babc-4177">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4177">6</span></span>

<span data-ttu-id="2babc-4178">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4178">7</span></span>

<span data-ttu-id="2babc-4179">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4179">8</span></span>

<span data-ttu-id="2babc-4180">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4180">9</span></span>

<span data-ttu-id="2babc-4181">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4181">1</span></span><br/> <span data-ttu-id="2babc-4182">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4182">0</span></span><br/>

<span data-ttu-id="2babc-4183">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4183">1</span></span>

<span data-ttu-id="2babc-4184">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4184">2</span></span>

<span data-ttu-id="2babc-4185">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4185">3</span></span>

<span data-ttu-id="2babc-4186">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4186">4</span></span>

<span data-ttu-id="2babc-4187">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4187">5</span></span>

<span data-ttu-id="2babc-4188">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4188">6</span></span>

<span data-ttu-id="2babc-4189">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4189">7</span></span>

<span data-ttu-id="2babc-4190">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4190">8</span></span>

<span data-ttu-id="2babc-4191">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4191">9</span></span>

<span data-ttu-id="2babc-4192">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4192">2</span></span><br/> <span data-ttu-id="2babc-4193">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4193">0</span></span><br/>

<span data-ttu-id="2babc-4194">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4194">1</span></span>

<span data-ttu-id="2babc-4195">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4195">2</span></span>

<span data-ttu-id="2babc-4196">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4196">3</span></span>

<span data-ttu-id="2babc-4197">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4197">4</span></span>

<span data-ttu-id="2babc-4198">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4198">5</span></span>

<span data-ttu-id="2babc-4199">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4199">6</span></span>

<span data-ttu-id="2babc-4200">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4200">7</span></span>

<span data-ttu-id="2babc-4201">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4201">8</span></span>

<span data-ttu-id="2babc-4202">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4202">9</span></span>

<span data-ttu-id="2babc-4203">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4203">3</span></span><br/> <span data-ttu-id="2babc-4204">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4204">0</span></span><br/>

<span data-ttu-id="2babc-4205">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4205">1</span></span>

<span data-ttu-id="2babc-4206">\_hCursor (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="2babc-4207">\_Chapt (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2babc-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="2babc-4208">**\_ hCursor**: valeur 32 bits représentant le descripteur, obtenue à partir d’un message CPMCreateQueryOut, qui identifie la requête pour laquelle la position doit être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="2babc-4209">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="2babc-4210">**\_ Chapt**: valeur 32 bits représentant le descripteur d’un chapitre à partir duquel récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="2babc-4211">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="2babc-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="2babc-4213">Le message CPMFreeCursorIn demande la libération d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="2babc-4214">Le format du message CPMFreeCursorIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="2babc-4215">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4215">0</span></span>

<span data-ttu-id="2babc-4216">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4216">1</span></span>

<span data-ttu-id="2babc-4217">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4217">2</span></span>

<span data-ttu-id="2babc-4218">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4218">3</span></span>

<span data-ttu-id="2babc-4219">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4219">4</span></span>

<span data-ttu-id="2babc-4220">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4220">5</span></span>

<span data-ttu-id="2babc-4221">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4221">6</span></span>

<span data-ttu-id="2babc-4222">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4222">7</span></span>

<span data-ttu-id="2babc-4223">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4223">8</span></span>

<span data-ttu-id="2babc-4224">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4224">9</span></span>

<span data-ttu-id="2babc-4225">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4225">1</span></span><br/> <span data-ttu-id="2babc-4226">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4226">0</span></span><br/>

<span data-ttu-id="2babc-4227">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4227">1</span></span>

<span data-ttu-id="2babc-4228">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4228">2</span></span>

<span data-ttu-id="2babc-4229">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4229">3</span></span>

<span data-ttu-id="2babc-4230">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4230">4</span></span>

<span data-ttu-id="2babc-4231">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4231">5</span></span>

<span data-ttu-id="2babc-4232">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4232">6</span></span>

<span data-ttu-id="2babc-4233">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4233">7</span></span>

<span data-ttu-id="2babc-4234">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4234">8</span></span>

<span data-ttu-id="2babc-4235">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4235">9</span></span>

<span data-ttu-id="2babc-4236">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4236">2</span></span><br/> <span data-ttu-id="2babc-4237">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4237">0</span></span><br/>

<span data-ttu-id="2babc-4238">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4238">1</span></span>

<span data-ttu-id="2babc-4239">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4239">2</span></span>

<span data-ttu-id="2babc-4240">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4240">3</span></span>

<span data-ttu-id="2babc-4241">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4241">4</span></span>

<span data-ttu-id="2babc-4242">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4242">5</span></span>

<span data-ttu-id="2babc-4243">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4243">6</span></span>

<span data-ttu-id="2babc-4244">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4244">7</span></span>

<span data-ttu-id="2babc-4245">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4245">8</span></span>

<span data-ttu-id="2babc-4246">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4246">9</span></span>

<span data-ttu-id="2babc-4247">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4247">3</span></span><br/> <span data-ttu-id="2babc-4248">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4248">0</span></span><br/>

<span data-ttu-id="2babc-4249">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4249">1</span></span>

<span data-ttu-id="2babc-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="2babc-4250">\_hCursor</span></span>



 

<span data-ttu-id="2babc-4251">**\_ hCursor**: valeur 32 bits représentant le handle du curseur du message CPMCreateQueryOut à libérer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="2babc-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="2babc-4253">Le message CPMFreeCursorOut répond à un message CPMFreeCursorIn avec les résultats de la libération d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="2babc-4254">Le format du message CPMFreeCursorOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="2babc-4255">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4255">0</span></span>

<span data-ttu-id="2babc-4256">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4256">1</span></span>

<span data-ttu-id="2babc-4257">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4257">2</span></span>

<span data-ttu-id="2babc-4258">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4258">3</span></span>

<span data-ttu-id="2babc-4259">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4259">4</span></span>

<span data-ttu-id="2babc-4260">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4260">5</span></span>

<span data-ttu-id="2babc-4261">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4261">6</span></span>

<span data-ttu-id="2babc-4262">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4262">7</span></span>

<span data-ttu-id="2babc-4263">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4263">8</span></span>

<span data-ttu-id="2babc-4264">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4264">9</span></span>

<span data-ttu-id="2babc-4265">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4265">1</span></span><br/> <span data-ttu-id="2babc-4266">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4266">0</span></span><br/>

<span data-ttu-id="2babc-4267">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4267">1</span></span>

<span data-ttu-id="2babc-4268">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4268">2</span></span>

<span data-ttu-id="2babc-4269">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4269">3</span></span>

<span data-ttu-id="2babc-4270">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4270">4</span></span>

<span data-ttu-id="2babc-4271">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4271">5</span></span>

<span data-ttu-id="2babc-4272">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4272">6</span></span>

<span data-ttu-id="2babc-4273">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4273">7</span></span>

<span data-ttu-id="2babc-4274">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4274">8</span></span>

<span data-ttu-id="2babc-4275">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4275">9</span></span>

<span data-ttu-id="2babc-4276">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4276">2</span></span><br/> <span data-ttu-id="2babc-4277">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4277">0</span></span><br/>

<span data-ttu-id="2babc-4278">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4278">1</span></span>

<span data-ttu-id="2babc-4279">2</span><span class="sxs-lookup"><span data-stu-id="2babc-4279">2</span></span>

<span data-ttu-id="2babc-4280">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4280">3</span></span>

<span data-ttu-id="2babc-4281">4</span><span class="sxs-lookup"><span data-stu-id="2babc-4281">4</span></span>

<span data-ttu-id="2babc-4282">5</span><span class="sxs-lookup"><span data-stu-id="2babc-4282">5</span></span>

<span data-ttu-id="2babc-4283">6</span><span class="sxs-lookup"><span data-stu-id="2babc-4283">6</span></span>

<span data-ttu-id="2babc-4284">7</span><span class="sxs-lookup"><span data-stu-id="2babc-4284">7</span></span>

<span data-ttu-id="2babc-4285">8</span><span class="sxs-lookup"><span data-stu-id="2babc-4285">8</span></span>

<span data-ttu-id="2babc-4286">9</span><span class="sxs-lookup"><span data-stu-id="2babc-4286">9</span></span>

<span data-ttu-id="2babc-4287">3</span><span class="sxs-lookup"><span data-stu-id="2babc-4287">3</span></span><br/> <span data-ttu-id="2babc-4288">0</span><span class="sxs-lookup"><span data-stu-id="2babc-4288">0</span></span><br/>

<span data-ttu-id="2babc-4289">1</span><span class="sxs-lookup"><span data-stu-id="2babc-4289">1</span></span>

<span data-ttu-id="2babc-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="2babc-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="2babc-4291">**\_ cCursorsRemaining**: entier non signé 32 bits indiquant le nombre de curseurs encore utilisés pour la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="2babc-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="2babc-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="2babc-4293">Le message CPMDisconnect met fin à la connexion avec le serveur</span><span class="sxs-lookup"><span data-stu-id="2babc-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="2babc-4294">Le message ne doit pas inclure un corps ; seul l’en-tête de message, tel que spécifié dans la section 2.2.2, doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="2babc-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="2babc-4295">Erreurs 2.2.4</span><span class="sxs-lookup"><span data-stu-id="2babc-4295">2.2.4 Errors</span></span>

<span data-ttu-id="2babc-4296">Tous les messages du protocole de service d’indexation de contenu doivent retourner 0x00000000 en cas de réussite ; dans le cas contraire, ils retournent un code d’erreur non nul 32 bits qui peut être un HRESULT ou une valeur NTSTATUS (voir la section 1,8).</span><span class="sxs-lookup"><span data-stu-id="2babc-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="2babc-4297">Si une mémoire tampon est trop petite pour contenir un résultat, un code d’état de \_ l’État ressources insuffisantes \_ (0XC0000009A) doit être retourné et l’opération ayant échoué doit être retentée avec une mémoire tampon plus grande.</span><span class="sxs-lookup"><span data-stu-id="2babc-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="2babc-4298">Toutes les autres valeurs d’erreur doivent être traitées de la même façon.</span><span class="sxs-lookup"><span data-stu-id="2babc-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="2babc-4299">(Notez que actuellement, les espaces de numérotation HRESULT et NTSTATUS ne se chevauchent pas, à l’exception des valeurs de signification identique, mais même s’ils étaient des conflits à l’avenir, cela ne provoque aucun problème de protocole tant que la valeur de l’état \_ Les ressources insuffisantes \_ restent uniques, car toutes les autres valeurs d’erreur sont traitées de la même façon.)</span><span class="sxs-lookup"><span data-stu-id="2babc-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="2babc-4300">3 Détails du protocole</span><span class="sxs-lookup"><span data-stu-id="2babc-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="2babc-4301">Détails du serveur 3,1</span><span class="sxs-lookup"><span data-stu-id="2babc-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="2babc-4302">Détails du client 3,2</span><span class="sxs-lookup"><span data-stu-id="2babc-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="2babc-4303">Les demandes de message CISP pour l’interrogation à distance des catalogues du service d’indexation ne nécessitent pas de séquence particulière.</span><span class="sxs-lookup"><span data-stu-id="2babc-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="2babc-4304">Il est recommandé que la couche supérieure adhère à une séquence de messages significative, comme pour les messages reçus à partir de cette séquence ou avec des données non valides, le serveur répond avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="2babc-4305">Certains messages dépendent également de la couche supérieure qui fournit des données valides qui ont été reçues dans les messages précédemment dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="2babc-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="2babc-4306">Une séquence de message standard pour une requête simple à partir d’un client vers un ordinateur distant est illustrée dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="2babc-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![séquence de message pour une requête simple](images/protocoldetails.jpg)

<span data-ttu-id="2babc-4308">Les messages représentés dans le diagramme précédent représentent un sous-ensemble de tous les messages CISP utilisés pour l’interrogation d’un catalogue du service d’indexation à distance.</span><span class="sxs-lookup"><span data-stu-id="2babc-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="2babc-4309">Détails du serveur 3,1</span><span class="sxs-lookup"><span data-stu-id="2babc-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="2babc-4310">3.1.1 Modèle de données abstraites</span><span class="sxs-lookup"><span data-stu-id="2babc-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="2babc-4311">La section suivante spécifie les données et l’état géré par le serveur CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="2babc-4312">Les données fournies ici sont pour faciliter l’explication du comportement du protocole.</span><span class="sxs-lookup"><span data-stu-id="2babc-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="2babc-4313">Cette section ne stipule pas que les implémentations adhèrent à ce modèle tant que leur comportement externe est cohérent avec celui décrit dans ce document.</span><span class="sxs-lookup"><span data-stu-id="2babc-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="2babc-4314">Un service d’indexation qui implémente CISP doit conserver les éléments de données abstraits suivants :</span><span class="sxs-lookup"><span data-stu-id="2babc-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="2babc-4315">Liste des clients connectés au serveur</span><span class="sxs-lookup"><span data-stu-id="2babc-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="2babc-4316">Informations sur chaque client, notamment :</span><span class="sxs-lookup"><span data-stu-id="2babc-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="2babc-4317">Version du client (comme indiqué dans le message CPMConnectIn spécifié dans la section 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="2babc-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="2babc-4318">Catalogue associé au client (par un message CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="2babc-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="2babc-4319">Propriétés client supplémentaires comme indiqué dans la section 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="2babc-4320">Requête de recherche du client</span><span class="sxs-lookup"><span data-stu-id="2babc-4320">Client's search query</span></span>
    -   <span data-ttu-id="2babc-4321">Liste des handles de curseur pour la requête et la position dans le jeu de résultats pour chaque descripteur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="2babc-4322">Ensemble actuel de liaisons</span><span class="sxs-lookup"><span data-stu-id="2babc-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="2babc-4323">État actuel de la requête qui comprend (pour chaque curseur) :</span><span class="sxs-lookup"><span data-stu-id="2babc-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="2babc-4324">Nombre de lignes dans le résultat de la requête</span><span class="sxs-lookup"><span data-stu-id="2babc-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="2babc-4325">Numérateur et dénominateur de la saisie semi-automatique des requêtes</span><span class="sxs-lookup"><span data-stu-id="2babc-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="2babc-4326">Nombre de lignes indiqué par le message CPMRatioFinishedOut le plus récent pour ce curseur</span><span class="sxs-lookup"><span data-stu-id="2babc-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="2babc-4327">Si la requête est analysée par le serveur pour les modifications des résultats de la requête et si elle est analysée, ce qui a changé dans les résultats de la requête depuis son dernier rapport au client par CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="2babc-4328">Liste des descripteurs de chapitres, servis par cette requête à un client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="2babc-4329">Liste de handles de signet pour chaque curseur, servie par cette requête à un client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="2babc-4330">État actuel du service d’indexation, qui peut être « non initialisé », « en cours d’exécution » ou « arrêt en cours ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="2babc-4331">Notez que la plupart du serveur de temps est dans l’État « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="2babc-4332">Voici le diagramme d’ordinateur d’État pour le serveur :</span><span class="sxs-lookup"><span data-stu-id="2babc-4332">Following is the state machine diagram for the server:</span></span>

    ![diagramme d’ordinateur d’État du serveur de service d’indexation](images/abstractdatamodel.jpg)

-   <span data-ttu-id="2babc-4334">Informations par catalogue : nombre de documents indexés, taille de l’index, nombre de clés uniques, etc. (voir la section 2.2.3.1 pour obtenir la liste complète), State (qui correspond aux valeurs de dwNewState dans la section 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="2babc-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="2babc-4335">Pour chaque langue prise en charge, une base de données de variantes Word, comme indiqué dans la section 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="2babc-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="2babc-4336">3.1.2 Minuteurs</span><span class="sxs-lookup"><span data-stu-id="2babc-4336">3.1.2 Timers</span></span>

<span data-ttu-id="2babc-4337">Aucun minuteur de protocole n’est requis.</span><span class="sxs-lookup"><span data-stu-id="2babc-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="2babc-4338">3.1.3 Initialisation</span><span class="sxs-lookup"><span data-stu-id="2babc-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="2babc-4339">Lors de l’initialisation, le serveur doit définir son état sur « non initialisé » et commencer à écouter les messages sur le canal nommé spécifié dans la section 1,9.</span><span class="sxs-lookup"><span data-stu-id="2babc-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="2babc-4340">Une fois l’initialisation interne effectuée, elle doit passer à l’État « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="2babc-4341">3.1.4 Événements déclenchés de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="2babc-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="2babc-4342">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2babc-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="2babc-4343">Règles de traitement et de séquencement des messages 3.1.5</span><span class="sxs-lookup"><span data-stu-id="2babc-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="2babc-4344">À chaque fois qu’une erreur se produit lors du traitement d’un message envoyé par un client, le serveur doit signaler une erreur au client comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="2babc-4345">Arrêter le traitement du message envoyé par le client</span><span class="sxs-lookup"><span data-stu-id="2babc-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="2babc-4346">Répondre avec l’en-tête de message (uniquement) du message envoyé par le client, en conservant le \_ champ MSG intact.</span><span class="sxs-lookup"><span data-stu-id="2babc-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="2babc-4347">Définissez le \_ champ État sur la valeur du code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="2babc-4348">Lorsqu’un message arrive, le serveur doit vérifier la \_ valeur du champ MSG pour déterminer s’il s’agit d’un type connu (voir la section 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="2babc-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="2babc-4349">Si le type n’est pas connu, il doit signaler un état d' \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="2babc-4350">Le serveur doit ensuite valider la \_ valeur du champ ulChecksum si le type de message est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2babc-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="2babc-4351">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="2babc-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="2babc-4352">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="2babc-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="2babc-4353">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="2babc-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="2babc-4354">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="2babc-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="2babc-4355">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="2babc-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="2babc-4356">Pour valider la \_ valeur du champ ulChecksum, le serveur doit vérifier la valeur spécifiée par le client dans le \_ champ iClientVersion du message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="2babc-4357">Si le \_ champ iClientVersion n’a pas la valeur 0x00000008 et que le \_ champ ulChecksum n’a pas la valeur 0x00000000, le serveur doit signaler une \_ erreur de paramètre non valide d’état \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="2babc-4358">Le serveur ne doit pas valider le \_ champ ulChecksum pour les clients \_ . le champ iClientVersion a une valeur inférieure à 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="2babc-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="2babc-4359">Si la \_ valeur du champ iClientVersionfield est 0x00000008 ou supérieure, le serveur doit vérifier que le \_ champ ulChecksum a été calculé comme indiqué dans la section 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="2babc-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="2babc-4360">Si la \_ valeur ulChecksum n’est pas valide, le serveur doit signaler une \_ erreur de paramètre non valide d’état \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="2babc-4361">Ensuite, le serveur vérifie l’État dans lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="2babc-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="2babc-4362">Si son état est « non initialisé », le serveur doit signaler une \_ erreur d’E/t \_ non \_ initialisée (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="2babc-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="2babc-4363">Si l’État est « arrêt en cours », le serveur doit signaler une \_ erreur d’arrêt de l’E/ \_ 0X80041812 (ci).</span><span class="sxs-lookup"><span data-stu-id="2babc-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="2babc-4364">Une fois qu’un en-tête a été déterminé comme étant valide et que le serveur est en état d’exécution, un traitement spécifique des messages doit être effectué comme indiqué dans les sous-sections ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2babc-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="2babc-4365">Gestion du catalogue du service d’indexation à distance 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="2babc-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="2babc-4366">3.1.5.1.1 recevant une demande CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="2babc-4367">Lorsque le serveur reçoit une demande de message CPMCIStateInOut du client, le serveur doit d’abord vérifier si le client figure dans une liste de clients connectés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="2babc-4368">Si le client ne figure pas dans la liste, le serveur doit signaler une erreur de paramètre d’état \_ non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="2babc-4369">Dans le cas contraire, il doit répondre au client avec un message CPMCIStateInOut, en le remplissant avec les informations relatives au catalogue associé du client, comme indiqué dans la section 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="2babc-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="2babc-4370">3.1.5.1.2 recevant une demande CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="2babc-4371">Lorsque le serveur reçoit une demande de message CPMSetCatStateIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4372">Vérifiez que le client dispose d’un accès administratif.</span><span class="sxs-lookup"><span data-stu-id="2babc-4372">Check that client has administrative access.</span></span> <span data-ttu-id="2babc-4373">Si le client ne dispose pas d’un accès administrateur, le serveur doit signaler une erreur d’état \_ accès \_ refusé (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="2babc-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="2babc-4374">Si \_ dwNewState n’est pas égal à CICAT \_ All \_ Opened, modifiez l’état du catalogue spécifié dans le champ CatName comme spécifié par le \_ champ dwNewState.</span><span class="sxs-lookup"><span data-stu-id="2babc-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="2babc-4375">Pour plus d’informations, consultez la section 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="2babc-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="2babc-4376">Si le serveur ne trouve pas de catalogue avec le nom spécifié dans le champ CatName, le serveur doit retourner une \_ erreur de paramètre non valide de l’état \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4377">Répondez au client avec un message CPMSetCatStateOut, où \_ DWOLDSTATE doit être défini à l’état précédent du catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="2babc-4378">Si \_ dwNewState est égal à CICAT \_ All \_ Opened, le serveur doit vérifier l’état de tous les catalogues et, s’ils sont tous démarrés, il doit définir \_ dwOldState sur 0x00000001 et, sinon, définir \_ dwOldState sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="2babc-4379">3.1.5.1.3 recevant une demande CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="2babc-4380">Lorsque le serveur reçoit une demande de message CPMUpdateDocumentsIn, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4381">Vérifiez si le client figure dans une liste de clients connectés (auxquels est associé un catalogue).</span><span class="sxs-lookup"><span data-stu-id="2babc-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="2babc-4382">Si le client ne figure pas dans la liste, le serveur doit signaler une erreur de paramètre d’état \_ non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4383">Vérifiez que le client dispose d’un accès administratif.</span><span class="sxs-lookup"><span data-stu-id="2babc-4383">Check that client has administrative access.</span></span> <span data-ttu-id="2babc-4384">Si le client ne dispose pas d’un accès administratif au serveur, le serveur doit signaler une \_ erreur d’accès \_ refusé (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="2babc-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="2babc-4385">Commencez le processus d’indexation du chemin d’accès spécifié par le client, en procédant à une analyse complète ou incrémentielle, en fonction de la valeur du \_ champ d’indicateur dans le message CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="2babc-4386">Si le chemin d’accès n’était pas déjà indexé, il doit être ajouté à la collection d’emplacements indexés et une analyse complète est effectuée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="2babc-4387">Si une valeur non conforme du \_ champ indicateur est spécifiée, le serveur doit agir comme si \_ Flag était défini sur UPD \_ Init et effectuer une analyse complète.</span><span class="sxs-lookup"><span data-stu-id="2babc-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="2babc-4388">Cette opération doit être effectuée dans le catalogue associé au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="2babc-4389">Répondez au client avec l’en-tête de message pour CPMUpdateDocumentsIn et définissez le \_ champ Status sur les résultats de la demande.</span><span class="sxs-lookup"><span data-stu-id="2babc-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="2babc-4390">3.1.5.1.4 recevant une demande CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="2babc-4391">Lorsque le serveur reçoit une demande de message CPMForceMergeIn, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4392">Vérifiez si le client figure dans une liste de clients connectés (auxquels est associé un catalogue).</span><span class="sxs-lookup"><span data-stu-id="2babc-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="2babc-4393">Si le client ne figure pas dans la liste, le serveur doit signaler un état d' \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4394">Vérifiez que le client dispose d’un accès administratif.</span><span class="sxs-lookup"><span data-stu-id="2babc-4394">Check that client has administrative access.</span></span> <span data-ttu-id="2babc-4395">Si le client ne dispose pas d’un accès administrateur, le serveur doit signaler une erreur d’état \_ accès \_ refusé (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="2babc-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="2babc-4396">Commencez tout processus de maintenance nécessaire pour améliorer les performances des requêtes sur un catalogue, associées au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="2babc-4397">Répondez au client avec un en-tête de message pour CPMForceMergeIn et définissez le \_ champ Status sur les résultats de la demande.</span><span class="sxs-lookup"><span data-stu-id="2babc-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="2babc-4398">Notez que le processus de maintenance est asynchrone et peut continuer une fois que le client a reçu le message de réponse.</span><span class="sxs-lookup"><span data-stu-id="2babc-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="2babc-4399">Ce processus n’affecte pas directement le protocole de quelque façon que ce soit (autre que le temps de réponse).</span><span class="sxs-lookup"><span data-stu-id="2babc-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="2babc-4400">interrogation du service d’indexation à distance 3.1.5.2</span><span class="sxs-lookup"><span data-stu-id="2babc-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="2babc-4401">3.1.5.2.1 recevant une demande CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="2babc-4402">Lorsque le serveur reçoit une requête CPMConnectIn à partir d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4403">Vérifiez si le client figure dans la liste des clients connectés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="2babc-4404">Si c’est le cas, le serveur doit signaler une \_ erreur de \_ paramètre non valide (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4405">Vérifie si le catalogue spécifié existe et s’il n’est pas à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="2babc-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="2babc-4406">Si ce n’est pas le cas, le serveur doit disposer d’une erreur de l’état d' \_ \_ absence du \_ catalogue (0x8004181D) du rapport ci.</span><span class="sxs-lookup"><span data-stu-id="2babc-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="2babc-4407">Ajoutez le client à la liste des clients connectés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="2babc-4408">Associez le catalogue au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="2babc-4409">Stockez les informations transmises dans le message CPMConnectIn (telles que le nom du catalogue, la version du client, etc.) dans l’état du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="2babc-4410">Répondez au client avec un message CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="2babc-4411">3.1.5.2.2 recevant une demande CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="2babc-4412">Lorsque le serveur reçoit une demande de message CPMCreateQueryIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4413">Vérifiez si le client figure dans la liste des clients connectés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="2babc-4414">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4415">Vérifiez si une requête est déjà associée au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="2babc-4416">Si c’est le cas, le serveur doit signaler une \_ erreur de \_ paramètre non valide (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4417">Vérifiez si le catalogue associé au client est dans l’État, ce qui permet le traitement de la requête (CICAT \_ ReadOnly ou CICAT \_ accessible en écriture).</span><span class="sxs-lookup"><span data-stu-id="2babc-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="2babc-4418">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur requête S \_ aucune \_ requête (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="2babc-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="2babc-4419">Analysez l’ensemble de restrictions, les ordres de tri et les regroupements spécifiés dans la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="2babc-4420">Si le serveur rencontre une erreur, il doit signaler une erreur appropriée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="2babc-4421">Si cette étape échoue pour une autre raison, le serveur doit signaler l’erreur rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="2babc-4422">Pour plus d’informations sur les erreurs de requête du service d’indexation, consultez \[ MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="2babc-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="2babc-4423">Enregistrez la requête de recherche dans l’état du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="2babc-4424">Effectuez les préparatifs nécessaires pour servir les lignes à un client et associez la requête aux handles de curseur appropriés (en fonction des informations transmises dans le message CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="2babc-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="2babc-4425">Ajoutez ces handles à la liste des handles de curseurs du client et initialisez les listes de handles de chapitre et de signets.</span><span class="sxs-lookup"><span data-stu-id="2babc-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="2babc-4426">Initialise la liste des descripteurs de chapitre pour chaque curseur de cette requête sur DB \_ null \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="2babc-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="2babc-4427">Initialisez la liste des descripteurs de signet pour chaque curseur de cette requête sur un ensemble de DBBMK \_ et de DBBMK en \_ dernier.</span><span class="sxs-lookup"><span data-stu-id="2babc-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="2babc-4428">Marquez la requête comme non surveillée pour les modifications.</span><span class="sxs-lookup"><span data-stu-id="2babc-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="2babc-4429">Initialisez le nombre de lignes sur le nombre de lignes actuellement calculé (ce qui peut être 0 si la requête n’a pas commencé à s’exécuter ou un nombre si la requête est en cours d’exécution) et initialisez le numérateur et le dénominateur de la saisie semi-automatique des requêtes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="2babc-4430">Répondez au client avec un message CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="2babc-4431">3.1.5.2.3 recevant une demande CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="2babc-4432">Lorsque le serveur reçoit une demande de message CPMGetQueryStatusIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4433">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="2babc-4434">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4435">Vérifiez si le handle de curseur se trouve dans une liste de handles de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="2babc-4436">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4437">Préparez un message CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="2babc-4438">Le serveur doit récupérer l’état actuel de la requête et le définir dans le \_ champ QStatus (consultez 2.2.3.11 pour connaître les valeurs possibles).</span><span class="sxs-lookup"><span data-stu-id="2babc-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="2babc-4439">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="2babc-4440">Répondez au client avec le message CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="2babc-4441">3.1.5.2.4 recevant une demande CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="2babc-4442">Lorsque le serveur reçoit une demande de message CPMGetQueryStatusExIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4443">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="2babc-4444">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4445">Vérifiez si le handle de curseur réussi figure dans une liste de handles de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="2babc-4446">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4447">Préparez un message CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="2babc-4448">Le serveur doit récupérer l’état de la requête actuelle et la progression de la requête et définir QStatus (consultez 2.2.3.11 pour connaître les valeurs possibles), \_ dwRatioFinishedDenominator et \_ dwRatioFinishedNumerator respectivement.</span><span class="sxs-lookup"><span data-stu-id="2babc-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="2babc-4449">Il doit ensuite définir le nombre de lignes dans les résultats de la requête sur \_ cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="2babc-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="2babc-4450">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="2babc-4451">Récupérez des informations sur le catalogue du client et remplissez \_ cFilteredDocuments et \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="2babc-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="2babc-4452">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="2babc-4453">Récupérez la position du signet indiquée par la poignée dans le \_ champ BMK, puis remplissez le \_ champ iRowBmk restant dans le message CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="2babc-4454">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="2babc-4455">Répondez au client avec le message CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="2babc-4456">3.1.5.2.5 recevant une demande CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="2babc-4457">Lorsque le serveur reçoit une demande de message CPMRatioFinishedIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4458">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="2babc-4459">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4460">Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="2babc-4461">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4462">Préparez un message CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="2babc-4463">Le serveur doit récupérer l’état de la requête du client et remplir les \_ champs ulNumerator, \_ ulDenominator et \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="2babc-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="2babc-4464">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="2babc-4465">Si \_ Crows est égal au dernier nombre de lignes signalées pour cette requête, définissez \_ fNewRows sur 0x00000000. sinon, affectez-lui la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="2babc-4466">Met à jour le dernier nombre de lignes signalées pour cette requête à la valeur de \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="2babc-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="2babc-4467">Répondez au client avec le message CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="2babc-4468">3.1.5.2.6 recevant une demande CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="2babc-4469">Lorsque le serveur reçoit une demande de message CPMSetBindingsIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4470">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="2babc-4471">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4472">Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="2babc-4473">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4474">Vérifiez que les informations de liaison sont valides (c’est-à-dire que la colonne spécifie au moins la valeur, la longueur ou l’État à renvoyer ; aucun chevauchement des liaisons pour la valeur, la longueur ou l’État ; et la valeur, la longueur et l’État s’ajustent à la taille de ligne spécifiée) et si aucune erreur de base de données \_ \_ BADBINDINFO (0x80040E08) n’est signalée</span><span class="sxs-lookup"><span data-stu-id="2babc-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="2babc-4475">Enregistrez les informations de liaison associées aux colonnes spécifiées dans le champ aColumns.</span><span class="sxs-lookup"><span data-stu-id="2babc-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="2babc-4476">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="2babc-4477">Répondez au client avec un en-tête de message (uniquement) avec \_ MSG défini sur CPMSetBindingsIn et \_ Status défini sur les résultats de la liaison spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="2babc-4478">3.1.5.2.7 recevant une demande CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="2babc-4479">Lorsque le serveur reçoit une demande de message CPMGetRowsIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4480">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="2babc-4481">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4482">Vérifiez si le handle de curseur passé est dans athelist des handles de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="2babc-4483">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4484">Vérifiez si le client dispose d’un ensemble de liaisons en cours.</span><span class="sxs-lookup"><span data-stu-id="2babc-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="2babc-4485">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4486">Préparez un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="2babc-4487">Le serveur doit positionner le curseur dans les résultats de la requête comme indiqué par la description de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="2babc-4488">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="2babc-4489">Récupérez autant de lignes que vous le configurez dans une mémoire tampon, dont la taille est indiquée par \_ cbReadBuffer, mais pas plus que ce qui est indiqué par \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="2babc-4490">Lors de l’extraction de lignes, le serveur doit comparer le type de valeur de propriété de chaque colonne sélectionnée au type spécifié dans le jeu de liaisons actuel du client (section 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="2babc-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="2babc-4491">Si le type de la liaison n’est pas de type VT \_ , le serveur doit tenter de convertir la valeur de la propriété de la colonne en ce type.</span><span class="sxs-lookup"><span data-stu-id="2babc-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="2babc-4492">Sinon, si l' \_ indicateur DBPROP USEEXTENDEDDBTYPES est défini dans le jeu de propriétés DBPROPSET QUERYEXT du client \_ , ou si la valeur de la propriété de la colonne n’est pas un \_ type de vecteur VT, la valeur de la propriété doit être retournée dans son type normal.</span><span class="sxs-lookup"><span data-stu-id="2babc-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="2babc-4493">Si aucune de ces conditions n’est respectée (c’est-à-dire que le serveur a un \_ type de vecteur VT et que le client ne prend pas en charge VT \_ Vector), le serveur doit tenter de le convertir en un \_ type de tableau VT comme suit : les \_ éléments VT I8, VT \_ UI8, VT \_ fileTime et VT \_ CLSID du tableau ne peuvent pas être convertis et échouent à la place ; \_ \_ Les éléments de tableau VT LPSTR et VT LPWStr doivent être convertis en \_ BSTR BSTR ; les éléments de tableau de tous les autres types doivent rester inchangés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="2babc-4494">Enfin, si les colonnes de ligne contiennent des handles de chapitre ou de signet, le serveur doit mettre à jour les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="2babc-4495">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="2babc-4496">Stockez le nombre réel de lignes extraites dans \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="2babc-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="2babc-4497">Copiez la description de recherche et le champ de chapitre de CPMGetRowsIn dans un message CPMGetRowsOut à envoyer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="2babc-4498">Stockez les lignes extraites dans le champ Rows (voir la remarque sur l’octet d’état ci-dessous et la section 2.2.3.16 dans la structure du champ Rows).</span><span class="sxs-lookup"><span data-stu-id="2babc-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="2babc-4499">Répondez au client avec le message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="2babc-4500">Remarque sur le champ octet d’État :</span><span class="sxs-lookup"><span data-stu-id="2babc-4500">Note on status byte field:</span></span>

<span data-ttu-id="2babc-4501">Si StatusUsed est défini sur 0x01 dans le CTableColumn du message CPMSetBindingIn pour la colonne, le serveur doit définir l’octet d’État (qui se trouve à StatusOffset à partir du début de la ligne) pour cette colonne à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="2babc-4502">Valeur</span><span class="sxs-lookup"><span data-stu-id="2babc-4502">Value</span></span> | <span data-ttu-id="2babc-4503">Signification</span><span class="sxs-lookup"><span data-stu-id="2babc-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="2babc-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="2babc-4504">0x00</span></span>  | <span data-ttu-id="2babc-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="2babc-4505">StatusOK</span></span>       |
| <span data-ttu-id="2babc-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="2babc-4506">0x01</span></span>  | <span data-ttu-id="2babc-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="2babc-4507">StatusDeferred</span></span> |
| <span data-ttu-id="2babc-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="2babc-4508">0x02</span></span>  | <span data-ttu-id="2babc-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="2babc-4509">StatusNull</span></span>     |



 

<span data-ttu-id="2babc-4510">Si la valeur de propriété est absente pour cette ligne, le serveur doit définir l’octet d’État sur StatusNull.</span><span class="sxs-lookup"><span data-stu-id="2babc-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="2babc-4511">Si la valeur est trop grande pour être transférée dans le message CPMGetRowsOut, le serveur doit définir l’octet d’État sur StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="2babc-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="2babc-4512">Dans le cas contraire, le serveur doit définir l’octet d’État sur StatusOK.</span><span class="sxs-lookup"><span data-stu-id="2babc-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="2babc-4513">3.1.5.2.8 recevant une demande CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="2babc-4514">Lorsque le serveur reçoit une demande de message CPMFetchValueIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4515">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="2babc-4516">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4517">Préparez un message CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="2babc-4518">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="2babc-4519">Recherchez le document indiqué par le \_ champ wid et vérifiez si l’ID de propriété de ce document (ultérieurement appelé « valeur de propriété ») indiqué par la structure PropSpec est disponible pour ce client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="2babc-4520">Si cette valeur n’est pas disponible, le serveur doit définir \_ fValueExists sur 0x00000000 et, sinon, définir \_ fValueExists sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="2babc-4521">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="2babc-4522">Si \_ fValueExists est égal à 0x00000001, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="2babc-4523">Sérialisez la valeur de la propriété dans une structure SERIALIZEDPROPERTYVALUE et copiez-la, en commençant par l' \_ offset cbSoFar, au maximum \_ cbChunk octets (mais sans dépasser la fin de la propriété sérialisée) dans le champ vValue.</span><span class="sxs-lookup"><span data-stu-id="2babc-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="2babc-4524">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="2babc-4525">Définissez \_ cbValue sur le nombre d’octets copiés à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="2babc-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="2babc-4526">Définissez vType sur le type de propriété de la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="2babc-4527">Si la longueur de la propriété sérialisée est supérieure à \_ cbSoFar ajoutée à \_ cbValue, affectez à fMoreExists la valeur \_ 0x00000001. sinon, affectez-lui la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="2babc-4528">Répondre au client avec le message CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="2babc-4529">3.1.5.2.9 recevant une demande CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="2babc-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="2babc-4530">Lorsque le serveur reçoit un message CPMGetNotify d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4531">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="2babc-4532">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4533">Si aucune modification n’a été apportée dans le jeu de résultats de la requête depuis le dernier message CPMSendNotifyOut pour ce client, ou si la requête n’est pas actuellement surveillée pour les modifications dans le jeu de résultats, le serveur doit répondre avec le message CPMGetNotify et commencer à analyser la requête pour rechercher les modifications dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="2babc-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="2babc-4534">Si, par la suite, une modification est apportée au jeu de résultats de la requête, le serveur doit envoyer un seul message CPMSendNotifyOut au client et doit spécifier la modification dans le \_ champ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="2babc-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="2babc-4535">Si des modifications ont été apportées au jeu de résultats de la requête depuis le dernier message CPMSendNotifyOut, le serveur doit répondre avec CPMSendNotifyOut et doit spécifier la modification dans le \_ champ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="2babc-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="2babc-4536">Notez que, dans le cas de nombreuses modifications des résultats de la requête, DBWATCHNOTIFY \_ ROWSCHANGED prend la priorité (c’est-à-dire, si la requête a été exécutée, réexécutée et que le nombre de lignes modifiées et la requête a été effectué à nouveau, l’événement signalé est DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="2babc-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="2babc-4537">3.1.5.2.10 recevant une demande CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="2babc-4538">Lorsque le serveur reçoit une demande de message CPMGetApproximatePositionIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4539">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="2babc-4540">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4541">Vérifiez si le handle de curseur, le handle de chapitre et le handle de signet passés se trouvent dans les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="2babc-4542">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4543">Recherchez une ligne qui est associée au handle de signet dans les résultats de la requête et déterminez approximativement la position de la ligne dans l’ensemble de lignes, référencée par le handle de chapitre, et déterminez le numérateur et le dénominateur de la position.</span><span class="sxs-lookup"><span data-stu-id="2babc-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="2babc-4544">Notez que lorsque le descripteur de chapitre est DB \_ null \_ HCHAPTER, le chapitre correspondant est l’ensemble de lignes principal de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="2babc-4545">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="2babc-4546">Répondez au client avec un message CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="2babc-4547">3.1.5.2.11 recevant une demande CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="2babc-4548">Lorsque le serveur reçoit une demande de message CPMCompareBmkIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4549">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="2babc-4550">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4551">Vérifiez si le handle de curseur, le handle de chapitre et les handles de signet réussis se trouvent dans les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="2babc-4552">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4553">Préparez un message CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="2babc-4554">Si les poignées de signet sont égales, \_ DWCOMPARISON doit avoir la valeur DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="2babc-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="2babc-4555">Sinon, si l’un des descripteurs de signets est DBBMK \_ First ou DBBMK \_ Last, \_ dwComparison doit être défini sur DBCOMPARE ne \_ .</span><span class="sxs-lookup"><span data-stu-id="2babc-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="2babc-4556">Dans le cas contraire, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="2babc-4557">Rechercher les lignes référencées par chaque handle de signet dans les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="2babc-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="2babc-4558">Si l’une des lignes n’est pas dans le chapitre indiqué par le descripteur de chapitre dans CPMCompareBmkIn, \_ DWCOMPARISON doit être défini sur DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="2babc-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="2babc-4559">Dans le cas contraire, lorsque les deux lignes se trouvent dans le même chapitre, le serveur doit arrondir la position de ces lignes dans l’ensemble de lignes référencé par le handle de ce chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="2babc-4560">Il doit ensuite comparer les valeurs de position et définir \_ dwComparison sur DBCOMPARE \_ lt si la position de la première ligne est inférieure à la position de la deuxième ligne ; sinon, \_ dwComparison doit être défini sur DBCOMPARE \_ gt.</span><span class="sxs-lookup"><span data-stu-id="2babc-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="2babc-4561">Répondez au client avec un message CPMCompareBmkOut rempli.</span><span class="sxs-lookup"><span data-stu-id="2babc-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="2babc-4562">3.1.5.2.12 recevant une demande CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="2babc-4563">Lorsque le serveur reçoit la demande de message CPMRestartPositionIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4564">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="2babc-4565">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4566">Vérifiez si le handle de curseur et le descripteur de chapitre sont dans les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="2babc-4567">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4568">Placez le curseur au début du chapitre, identifié par le handle de chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="2babc-4569">Notez que lorsque le descripteur de chapitre est DB \_ null \_ HCHAPTER, le chapitre correspondant est l’ensemble de lignes principal de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="2babc-4570">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="2babc-4571">Répondez au client avec un message CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="2babc-4572">3.1.5.2.13 recevant une demande CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="2babc-4573">Lorsque le serveur reçoit une demande de message CPMFreeCursorIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4574">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="2babc-4575">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="2babc-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="2babc-4576">Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="2babc-4577">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="2babc-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="2babc-4578">Libérer le curseur et les ressources associées (voir la section 3.1.1 pour obtenir la liste complète) pour ce handle de curseur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="2babc-4579">Supprimez le curseur de la liste des curseurs pour ce client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="2babc-4580">Répondez avec un message CPMFreeCursorOut, en définissant le \_ champ cCursorsRemaining avec le nombre de curseurs restants.</span><span class="sxs-lookup"><span data-stu-id="2babc-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="2babc-4581">dans la liste de ce client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4581">in this client's list.</span></span>
-   <span data-ttu-id="2babc-4582">S’il n’y a plus de curseurs pour ce client, le serveur doit libérer la requête et les ressources associées (voir la section 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="2babc-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="2babc-4583">3.1.5.2.14 recevant une demande CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="2babc-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="2babc-4584">Lorsque le serveur reçoit une demande de message CPMDisconnect du client, le serveur doit supprimer le client de la liste des clients connectés et libérer toutes les ressources associées au client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="2babc-4585">Événements de minuterie 3.1.6</span><span class="sxs-lookup"><span data-stu-id="2babc-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="2babc-4586">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2babc-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="2babc-4587">3.1.7 autres événements locaux</span><span class="sxs-lookup"><span data-stu-id="2babc-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="2babc-4588">Quand le serveur est arrêté, il doit d’abord passer à l’état « arrêt ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="2babc-4589">Il doit ensuite arrêter d’écouter le canal, effectuer d’autres tâches d’arrêt spécifiques à l’implémentation, puis passer à l’état « arrêté ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="2babc-4590">Détails du client 3,2</span><span class="sxs-lookup"><span data-stu-id="2babc-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="2babc-4591">3.2.1 modèle de données abstraites</span><span class="sxs-lookup"><span data-stu-id="2babc-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="2babc-4592">La section suivante spécifie les données et l’état géré par le client du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="2babc-4593">Les données fournies sont pour faciliter l’explication du comportement du protocole.</span><span class="sxs-lookup"><span data-stu-id="2babc-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="2babc-4594">Cette section ne stipule pas que les implémentations adhèrent à ce modèle tant que leur comportement externe est cohérent avec celui décrit dans ce document.</span><span class="sxs-lookup"><span data-stu-id="2babc-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="2babc-4595">Un client a l’État abstrait suivant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="2babc-4596">**Dernier message envoyé**: copie du dernier message envoyé au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="2babc-4597">**Valeur de propriété actuelle**: valeur partielle d’une propriété « différée », qui est en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="2babc-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="2babc-4598">**Octets actuels reçus**: nombre d’octets reçus pour la valeur de propriété actuelle jusqu’à présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="2babc-4599">**État de la connexion de canal nommé**: une connexion au serveur</span><span class="sxs-lookup"><span data-stu-id="2babc-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="2babc-4600">les minuteurs 3.2.2</span><span class="sxs-lookup"><span data-stu-id="2babc-4600">3.2.2 Timers</span></span>

<span data-ttu-id="2babc-4601">Aucun minuteur de protocole n’est requis.</span><span class="sxs-lookup"><span data-stu-id="2babc-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="2babc-4602">3.2.3 initialisation</span><span class="sxs-lookup"><span data-stu-id="2babc-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="2babc-4603">Aucune action n’est effectuée tant qu’une demande de couche supérieure n’a pas été reçue.</span><span class="sxs-lookup"><span data-stu-id="2babc-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="2babc-4604">3.2.4 Higher-Layer événements déclenchés</span><span class="sxs-lookup"><span data-stu-id="2babc-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="2babc-4605">Lorsqu’une demande est reçue à partir d’une couche supérieure, le client doit créer une connexion de canal nommé au serveur, à l’aide des détails spécifiés dans la section 2,1.</span><span class="sxs-lookup"><span data-stu-id="2babc-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="2babc-4606">Si ce n’est pas le cas, la demande de couche supérieure doit être en échec.</span><span class="sxs-lookup"><span data-stu-id="2babc-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="2babc-4607">Autrement dit, en cas de défaillance de la connexion, il incombe au niveau supérieur de réessayer si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="2babc-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="2babc-4608">Un en-tête doit être préalablement associé à des champs définis comme indiqué dans la section 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="2babc-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="2babc-4609">Pour les messages spécifiés comme nécessitant une somme de contrôle différente de zéro, la \_ valeur ULCHECKSUM doit être calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="2babc-4610">Le contenu du message après que le \_ champ ulReserved2 de l’en-tête de message doit être interprété comme une séquence d’entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="2babc-4611">Le client doit calculer la somme des valeurs numériques fournies par ces entiers.</span><span class="sxs-lookup"><span data-stu-id="2babc-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="2babc-4612">Calcule l’opération de bits XOR de cette valeur avec 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="2babc-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="2babc-4613">Soustrait la valeur donnée par \_ MSG de la valeur qui résulte de l’opération de bits XOR.</span><span class="sxs-lookup"><span data-stu-id="2babc-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="2babc-4614">Gestion du catalogue du service d’indexation à distance 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="2babc-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="2babc-4615">Chaque message est déclenché par une demande de la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="2babc-4616">Aucune séquence de message n’est appliquée par le client pour les demandes de message CISP pour la gestion à distance des catalogues, mais (à l’exception d’un message CPMSetCatStateIn) le serveur répondra uniquement avec succès si le client s’est connecté précédemment au moyen d’un message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="2babc-4617">3.2.4.1.1 envoyant une demande CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="2babc-4618">En règle générale, la couche supérieure demande au client de protocole d’envoyer un message CPMCiStateInOut lorsqu’il a besoin d’informations sur les services d’indexation sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="2babc-4619">Lorsque vous demandez à envoyer ce message, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4620">Envoyez un message CPMCiStateInOut tel que spécifié dans la section 2.2.3.1 au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="2babc-4621">Attendez de recevoir le message CPMCiStateInOut du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="2babc-4622">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, la structure d’information pour revenir à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="2babc-4623">3.2.4.1.2 envoyant une demande CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="2babc-4624">En règle générale, la couche supérieure demande au client de protocole d’envoyer un message CPMSetCatStateIn lorsqu’il a besoin d’informations sur un catalogue ou sur tous les catalogues.</span><span class="sxs-lookup"><span data-stu-id="2babc-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="2babc-4625">Pour ce message, la couche supérieure doit fournir au client de protocole une valeur pour \_ dwNewState et, si nécessaire, le nom du catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="2babc-4626">Lorsque vous demandez à envoyer ce message, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4627">Envoi d’un message CPMSetCatStateIn tel que spécifié dans 2.2.3.2 au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="2babc-4628">Attendez de recevoir un message CPMSetCatStateOut du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="2babc-4629">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, \_ redwOldState à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="2babc-4630">3.2.4.1.3 envoyant une demande CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="2babc-4631">En général, la couche supérieure demande à envoyer ce message lorsqu’il doit mettre à jour des documents dans un chemin d’accès existant ou ajouter un nouveau chemin d’accès de fichier à l’index.</span><span class="sxs-lookup"><span data-stu-id="2babc-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="2babc-4632">La couche supérieure est donc de fournir le chemin d’accès et le type d’une analyse, qui est spécifiée comme dans la section 2.2.3.4 où une mise à jour incrémentielle ou complète est destinée à des chemins d’accès existants, et l’initialisation de nouvelles est destinée aux nouveaux chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="2babc-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="2babc-4633">Pour répondre à la demande de couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4634">Envoyez un message CPMUpdateDocumentsIn tel que spécifié dans la section 2.2.3.4 au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="2babc-4635">Attendez de recevoir le message CPMUpdateDocumentsIn du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="2babc-4636">Signalez la valeur du \_ champ d’état de la réponse à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="2babc-4637">3.2.4.1.4 envoyant une demande CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="2babc-4638">En règle générale, la couche supérieure demande à envoyer ce message lorsqu’il est nécessaire d’améliorer les performances des requêtes ou qu’elle fait partie de la maintenance planifiée du service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="2babc-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="2babc-4639">Afin de servir la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4640">Envoie le message CPMForceMergeIn tel que spécifié par la section 2.2.3.5 au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="2babc-4641">Attente de réception d’un message CPMUpdateDocumentsIn à partir du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="2babc-4642">Signalez la valeur du \_ champ d’état de la réponse à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="2babc-4643">Messages de requête du catalogue du service d’indexation à distance 3.2.4.2</span><span class="sxs-lookup"><span data-stu-id="2babc-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="2babc-4644">À l’exception de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, il existe une relation un-à-un entre les messages CISP et les demandes de couche supérieures.</span><span class="sxs-lookup"><span data-stu-id="2babc-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="2babc-4645">Pour les deux exceptions mentionnées ci-dessus, il peut y avoir plusieurs messages générés par le client pour répondre aux exigences de taille, ou pour récupérer une propriété complète.</span><span class="sxs-lookup"><span data-stu-id="2babc-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="2babc-4646">La couche supérieure effectue généralement le suivi de toutes les informations spécifiques à la requête (telles que les handles de curseur ouverts, les valeurs autorisées pour les descripteurs de signet et de chapitre, les valeurs wid pour les valeurs de propriété différées, etc.) et effectue également le suivi si le client est dans un état connecté, mais cela n’est pas appliqué par le client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="2babc-4647">À des fins d’illustration, la partie cliente du diagramme de la section 3 illustre cette séquence pour une requête de service d’indexation simple.</span><span class="sxs-lookup"><span data-stu-id="2babc-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="2babc-4648">3.2.4.2.1 envoyant une demande CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="2babc-4649">Ce message est généralement la toute première requête de la couche supérieure (comme si le client n’est pas connecté, le serveur échouera la plupart des messages avec l’exception de CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="2babc-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="2babc-4650">Le niveau supérieur fournit au client de protocole les informations nécessaires pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="2babc-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="2babc-4651">Afin de servir la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4652">Renseignez le message à l’aide des informations fournies par le client de couche supérieure (voir la section 2.2.3.6) dans \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 et aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="2babc-4653">Définissez \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet et cExtPropSet comme spécifié dans 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="2babc-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="2babc-4654">Définissez la somme de contrôle dans le \_ champ ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="2babc-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="2babc-4655">Envoyez le message CPMConnectIn au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="2babc-4656">Attente de réception d’un message CPMConnectOut à partir du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="2babc-4657">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, \_ restaurez la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="2babc-4658">À des fins d’information, il est prévu que les couches supérieures effectuent généralement les actions suivantes lors de la connexion réussie, mais elles ne sont pas appliquées par le client CISP :</span><span class="sxs-lookup"><span data-stu-id="2babc-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="2babc-4659">Utiliser les messages de gestion du catalogue du service d’indexation à distance pour les tâches d’administration</span><span class="sxs-lookup"><span data-stu-id="2babc-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="2babc-4660">Utilisez une demande CPMCreateQueryIn pour créer une requête de recherche dans le but de récupérer les résultats du catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="2babc-4661">3.2.4.2.2 envoyant une demande CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="2babc-4662">La couche supérieure fournit généralement des informations pour la création de la requête une fois que le client de protocole est connecté.</span><span class="sxs-lookup"><span data-stu-id="2babc-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="2babc-4663">La couche supérieure fournit au client un ensemble de restrictions, un jeu de colonnes, des règles d’ordre de tri et un ensemble de catégorisation (chacune d’elles peut être omise), des propriétés d’ensemble de lignes et la structure du mappeur d’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="2babc-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="2babc-4664">Lorsque cette demande est reçue à partir d’une couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4665">Préparez un CPMCreateQueryOut comme suit.</span><span class="sxs-lookup"><span data-stu-id="2babc-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="2babc-4666">Si un jeu de colonnes est présent, définissez CColumnsSetPreset sur 0x01 et remplissez le champ ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="2babc-4667">Si des restrictions sont présentes, définissez CRestrictionPresent sur 0x01 et remplissez le champ restriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="2babc-4668">Si un ensemble de tris est présent, renseignez le champ SortSet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="2babc-4669">Si un ensemble de catégorisations est présent, définissez CSortSetPresent sur 0x01 et remplissez le champ CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="2babc-4670">Définir le reste des champs comme indiqué dans 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="2babc-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="2babc-4671">Calculez \_ le champ ulCheckSum dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="2babc-4672">Envoyez le message CPMCreateQueryIn au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="2babc-4673">Attendez de recevoir le message CPMCreateQueryOut (voir les détails dans la section 3.2.5.1.1), en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="2babc-4674">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, le tableau de handles de curseur et les valeurs booléennes informatifs (comme spécifié dans 2.2.3.9) à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="2babc-4675">3.2.4.2.3 envoyant une demande CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="2babc-4676">En règle générale, la couche supérieure définit des liaisons pour chaque colonne à retourner dans les lignes lorsqu’elle a déjà un handle de curseur valide (après avoir reçu avec succès CPMCreateQueryOut, consultez la section 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="2babc-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="2babc-4677">Le plus élevé est supposé fournir un tableau de structures CTableColumn, comme indiqué dans la section 2.2.4.31, pour le champ aColumns et un handle de curseur valide.</span><span class="sxs-lookup"><span data-stu-id="2babc-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="2babc-4678">Lorsque cette demande est reçue de la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4679">Calculez le nombre de structures CTableColumn dans le tableau aColumns et définissez le champ cColumns sur cette valeur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="2babc-4680">Calculez la taille totale en octets des champs cColumns et aColumns, puis affectez la \_ valeur au champ cbBindingDesc.</span><span class="sxs-lookup"><span data-stu-id="2babc-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="2babc-4681">Définissez les champs spécifiés dans le message CPMSetBindingsIn sur les valeurs fournies par la couche d’application supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="2babc-4682">Définissez le \_ champ ulChecksum sur la valeur calculée comme indiqué dans la section 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="2babc-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="2babc-4683">Envoyez le message CPMSetBindignsIn terminé au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="2babc-4684">Attendez de recevoir un message CPMSetBindingsIn du serveur, en ignorant les autres messages.</span><span class="sxs-lookup"><span data-stu-id="2babc-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="2babc-4685">Indiquez l’état du \_ champ État de la réponse à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="2babc-4686">À des fins d’information, il est prévu que les couches supérieures demandent généralement à un client d’envoyer un message CPMGetRowsIn, mais cela n’est pas appliqué par le protocole de service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="2babc-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="2babc-4687">3.2.4.2.4 envoyant une demande CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="2babc-4688">Lorsque la couche supérieure est sur le point de recevoir des informations sur les lignes, elle fournit au client de protocole un pointeur et un handle de chapitre valides et donne une description de recherche appropriée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="2babc-4689">En règle générale, une couche supérieure est censée le faire lorsqu’elle a un handle de curseur et/ou de chapitre valide et que les liaisons ont été définies avec un message CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="2babc-4690">Pour accéder à l’ensemble de lignes dans un chapitre, la couche supérieure est d’utiliser le descripteur de chapitre reçu du serveur dans un message CPMGetRowsOut précédent.</span><span class="sxs-lookup"><span data-stu-id="2babc-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="2babc-4691">Lorsque cette demande est reçue de la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4692">Déterminez la valeur de l’entier non signé à spécifier pour le \_ champ cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="2babc-4693">Pour déterminer cette valeur, le client doit prendre la valeur maximale de ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="2babc-4694">1000 fois la valeur du champ c \_ RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="2babc-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="2babc-4695">Valeur de \_ cbRowWidth, arrondie au multiple de 512 octets le plus proche.</span><span class="sxs-lookup"><span data-stu-id="2babc-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="2babc-4696">Prenez la valeur la plus élevée de ces deux valeurs, jusqu’à la limite de 16 Ko.</span><span class="sxs-lookup"><span data-stu-id="2babc-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="2babc-4697">Dans les cas où une seule ligne est supérieure à 16 Ko, le serveur ne peut pas retourner les résultats de cette requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="2babc-4698">Spécifiez une base de client pour les données de ligne de taille variable dans l’espace d’adressage du client dans le \_ champ ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="2babc-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="2babc-4699">*Comportement de Windows : pour un client 32 bits communiquant avec un serveur 32 bits, ou un client 64 bits parlant à un serveur 64 bits, cette valeur est définie sur une adresse mémoire de la mémoire tampon de réception dans le processus d’application. Cela permet aux pointeurs, qui sont reçus dans le champ de lignes de CPMGetRowsOut d’être des pointeurs de mémoire corrects dans un processus d’application cliente. Sinon, la valeur est 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="2babc-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="2babc-4700">Calculez la taille de la description de la recherche et définissez-la dans le \_ champ cbSeek.</span><span class="sxs-lookup"><span data-stu-id="2babc-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="2babc-4701">Définissez la valeur de cbReserved (qui ferait office de décalage pour les lignes de début) à la valeur de \_ cbSeek plus 0x14.</span><span class="sxs-lookup"><span data-stu-id="2babc-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="2babc-4702">Envoi d’un message CPMConnectIn tel que spécifié dans 2.2.3.15 au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="2babc-4703">3.2.4.2.5 envoyant une demande CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="2babc-4704">Si le client reçoit une réponse CPMGetRowsOut du serveur avec le champ d’état de la colonne défini sur StatusDeferred (0x01), cela signifie que la valeur de propriété n’a pas été incluse dans le champ Rows du message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="2babc-4705">Dans ce cas, la couche supérieure demande généralement au client de protocole de récupérer la valeur au moyen du message CPMFetchValueIn et fournit la valeur PropSpec et \_ wid pour une propriété différée, que le client de protocole doit utiliser dans le premier message CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="2babc-4706">S’il s’agit du premier message CPMFetchValueIn que le client a envoyé pour demander la propriété spécifiée, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4707">Définissez tous les champs d’un message comme indiqué dans la section 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="2babc-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="2babc-4708">Affectez \_ à cbSoFar la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="2babc-4709">Définir les octets actuels reçus à 0.</span><span class="sxs-lookup"><span data-stu-id="2babc-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="2babc-4710">Envoyez le message CPMFetchValueIn au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="2babc-4711">3.2.4.2.6 envoyant une demande CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="2babc-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="2babc-4712">Une fois que le niveau supérieur n’utilise plus la requête de recherche, il peut libérer les ressources sur le serveur en demandant au client d’envoyer un message CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="2babc-4713">Lorsque cette demande est reçue, le client doit envoyer un message CPMFreeCursorIn tel que spécifié dans 2.2.3.28 au serveur, contenant le descripteur spécifié par la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="2babc-4714">3.2.4.2.7 envoi d’un message CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="2babc-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="2babc-4715">Si la couche supérieure n’a plus de requêtes pour le service d’indexation, pour libérer davantage de ressources serveur, l’application peut demander que le client envoie un message CPMDisconnect au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="2babc-4716">Lorsque cette requête est reçue, le client doit simplement envoyer le message comme demandé.</span><span class="sxs-lookup"><span data-stu-id="2babc-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="2babc-4717">Il n’y a aucune réponse à ce message à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="2babc-4718">3.2.5 traitement des messages et règles de séquencement</span><span class="sxs-lookup"><span data-stu-id="2babc-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="2babc-4719">Lorsque le client reçoit une réponse de message du serveur, le client doit utiliser le dernier message envoyé pour déterminer si le message reçu du serveur est celui attendu par le client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="2babc-4720">Tous les messages dont \_ le champ MSG est différent de celui du dernier message d’envoi doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="2babc-4721">3.2.5.1 recevant une réponse CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="2babc-4722">Lorsque le client reçoit une réponse de message CPMCreateQueryOut du serveur, le client doit renvoyer l' \_ État et (si l’État est réussi) les valeurs de handle de curseur sont retournées à une couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="2babc-4723">Toutes les actions supplémentaires sont effectuées jusqu’à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="2babc-4724">Comme la couche supérieure est consciente de la structure de la requête, elle devrait toujours s’attendre à ce que le nombre de handles de curseur soit renvoyé dans le message CPMCreateOueryOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="2babc-4725">Les handles de curseur sont retournés dans l’ordre suivant : le premier descripteur est l’ensemble de lignes non chapitre, le second est le premier ensemble de lignes chapitre (qui est le regroupement de résultats en fonction de la première catégorie spécifiée dans le champ CategorizationSet du message CPMCreateQueryIn.)</span><span class="sxs-lookup"><span data-stu-id="2babc-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="2babc-4726">À des fins d’information, il est prévu que les couches supérieures puissent effectuer les actions suivantes, mais elles ne sont pas appliquées par le client CISP :</span><span class="sxs-lookup"><span data-stu-id="2babc-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="2babc-4727">Utilisez CPMSetBindingsIn pour définir des liaisons pour des colonnes individuelles et effectuer toutes les actions suivantes sur le chemin d’accès de la requête</span><span class="sxs-lookup"><span data-stu-id="2babc-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="2babc-4728">Utilisez CPMGetQueryStatusIn pour vérifier la progression de l’exécution d’une requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="2babc-4729">Utilisez CPMRatioFinishedIn pour demander le pourcentage d’achèvement de la requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="2babc-4730">3.2.5.2 recevant une réponse CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="2babc-4731">Lorsque le client reçoit une réponse de message CPMGetRowsOut du serveur, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4732">Vérifiez si le \_ champ d’État dans l’en-tête indique réussite ou échec.</span><span class="sxs-lookup"><span data-stu-id="2babc-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="2babc-4733">Si la \_ valeur d’État est mémoire tampon d’État insuffisante \_ \_ \_ (0xC0000023), le client doit vérifier l’état du dernier message envoyé.</span><span class="sxs-lookup"><span data-stu-id="2babc-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="2babc-4734">S’il ne contient pas de message CPMGetRowsIn, le message reçu doit être ignoré en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="2babc-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="2babc-4735">Dans le cas contraire, le client doit envoyer au serveur un nouveau message CPMGetRowsIn avec tous les champs identiques à ceux qui sont stockés, sauf que le \_ CBREADBUFFER doit être augmenté de 512 (mais pas supérieur à 0x4000).</span><span class="sxs-lookup"><span data-stu-id="2babc-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="2babc-4736">Si \_ l’État est \_ \_ trop \_ petit pour le tampon d’État (0xC0000023) et que le dernier message envoyé a déjà un \_ CBREADBUFFER égal au client 0x4000 doit signaler l’erreur au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="2babc-4737">Si la \_ valeur d’État est une autre valeur d’erreur, le client doit indiquer l’échec jusqu’à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="2babc-4738">Si la \_ valeur d’État indique une réussite, les résultats doivent être indiqués jusqu’à la couche supérieure demandant les informations, et d’autres actions sont effectuées sur la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="2babc-4739">À des fins d’information, il est prévu que les couches supérieures effectuent généralement les actions suivantes, mais elles ne sont pas appliquées par le client du protocole du service d’indexation de contenu :</span><span class="sxs-lookup"><span data-stu-id="2babc-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="2babc-4740">Si les valeurs des lignes représentent les ID de document, les poignées de chapitre ou de signet, la couche supérieure les stocke en général pour une utilisation dans des opérations ultérieures qui impliquent des ID de document, des handles de chapitre ou de signet valides.</span><span class="sxs-lookup"><span data-stu-id="2babc-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="2babc-4741">En général, la couche supérieure stocke ou affiche ou utilise les données des valeurs de ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="2babc-4742">Pour les valeurs qui ont été marquées comme couches supérieures différées, la valeur est extraite à l’aide de messages CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="2babc-4743">La description de la recherche est également retournée à la couche supérieure et peut être réutilisée ou examinée par la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="2babc-4744">À des fins d’information, si la couche supérieure a demandé des descripteurs aux chapitres et aux signets qui ont été reçus dans les lignes, elle peut effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="2babc-4745">Utilisez CPMGetQueryStatusExIn pour vérifier la progression de l’exécution d’une requête, ainsi que des informations d’État supplémentaires, telles que le nombre de documents filtrés, les documents restants à filtrer, le rapport entre les documents traités par la requête, le nombre total de lignes dans la requête et la position du signet dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="2babc-4746">Utilisez CPMGetNotify pour demander que le serveur informe le client des modifications de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="2babc-4747">Utilisez CPMGetApproximatePositionIn pour demander la position approximative d’un signet dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="2babc-4748">Utilisez CPMCompareBmkIn pour demander une comparaison de deux signets dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="2babc-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="2babc-4749">Utilisez CPMRestartPositionIn pour que le serveur modifie l’emplacement du curseur au début de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="2babc-4750">3.2.5.3 recevant une réponse CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="2babc-4751">Lorsque le client reçoit une réponse de message CPMGetRowsOut du serveur, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="2babc-4752">Vérifiez si le \_ champ d’État dans l’en-tête indique réussite ou échec.</span><span class="sxs-lookup"><span data-stu-id="2babc-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="2babc-4753">En cas d’échec, notifiez la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="2babc-4754">Dans le cas contraire, continuez ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2babc-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="2babc-4755">Vérifiez \_ fValueExist et, s’il a la valeur 0x00000000, informez la couche supérieure que la valeur est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2babc-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="2babc-4756">Sinon, ajoutez \_ cbValue octets de vValue à la valeur de propriété actuelle.</span><span class="sxs-lookup"><span data-stu-id="2babc-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="2babc-4757">Si \_ \_ fMoreExists a la valeur 0x00000001, incrémentez \_ les octets actuels reçus par \_ cbValue et envoyez un message CPMFetchValueIn au serveur, en définissant \_ CbSoFar sur la valeur des octets actuels reçus, \_ cbPropSpec sur zéro et \_ cbChunk sur la taille de la mémoire tampon souhaitée par la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="2babc-4758">Si \_ fMoreExists a la valeur 0x00000000, indiquez la valeur de propriété de la valeur de propriété actuelle à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="2babc-4759">3.2.5.4 recevant une réponse CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="2babc-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="2babc-4760">Lorsque le client reçoit une réponse de message CPMFreeCursorOut réussie du serveur, le client doit renvoyer la \_ valeur cCursorsRemaining à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="2babc-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="2babc-4761">Les informations suivantes sont fournies à des fins d’information uniquement et ne sont pas appliquées par le client CISP.</span><span class="sxs-lookup"><span data-stu-id="2babc-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="2babc-4762">La couche supérieure est supposée effectuer le suivi des poignées de curseur et ne pas utiliser celles qui ont déjà été libérées.</span><span class="sxs-lookup"><span data-stu-id="2babc-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="2babc-4763">Une fois que le nombre de \_ cCursorsRemaining est égal à 0x00000000, la couche supérieure peut utiliser la connexion pour spécifier une autre requête (à l’aide d’un message CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="2babc-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="2babc-4764">Événements de minuterie 3.2.6</span><span class="sxs-lookup"><span data-stu-id="2babc-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="2babc-4765">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2babc-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="2babc-4766">3.2.7 autres événements locaux</span><span class="sxs-lookup"><span data-stu-id="2babc-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="2babc-4767">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2babc-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="2babc-4768">4 Exemples de protocoles</span><span class="sxs-lookup"><span data-stu-id="2babc-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="2babc-4769">4,1 exemple 1</span><span class="sxs-lookup"><span data-stu-id="2babc-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="2babc-4770">4,2 exemple 2</span><span class="sxs-lookup"><span data-stu-id="2babc-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="2babc-4771">4,1 exemple 1</span><span class="sxs-lookup"><span data-stu-id="2babc-4771">4.1 Example 1</span></span>

<span data-ttu-id="2babc-4772">Dans l’exemple suivant, nous considérons un scénario dans lequel l’utilisateur JOHN sur l’ordinateur A souhaite obtenir la taille des fichiers qui contiennent le mot « Microsoft » à partir de l’ensemble de documents stockés sur le serveur X dans le système de catalogue.</span><span class="sxs-lookup"><span data-stu-id="2babc-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="2babc-4773">Supposons que l’ordinateur A exécute un système d’exploitation Windows XP 32 bits et que l’ordinateur X exécute un système d’exploitation Windows Server 2003 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2babc-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="2babc-4774">L’utilisateur lance une application de recherche et entre dans la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="2babc-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="2babc-4775">L’application transmet à son tour la requête de recherche au client du protocole.</span><span class="sxs-lookup"><span data-stu-id="2babc-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="2babc-4776">Le client de protocole établit une connexion avec le serveur d’indexation X. Le client de protocole utilise le \\ canal de canal nommé \\ ci \_ SKADS pour se connecter au serveur X sur SMB.</span><span class="sxs-lookup"><span data-stu-id="2babc-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="2babc-4777">Le client de protocole prépare ensuite un message CPMConnectIn avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="2babc-4778">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4779">**\_ MSG** a la valeur 0x000000C8, ce qui indique qu’il s’agit d’un message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="2babc-4780">l' **\_ État** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="2babc-4781">**\_ ulChecksum** contient la somme de contrôle, calculée comme indiqué dans la section 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="2babc-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="2babc-4782">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="2babc-4783">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4784">**\_ iClientVersion** est défini sur 0x00000008, ce qui indique que le serveur doit valider le champ de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2babc-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="2babc-4785">**\_ fClientIsRemote** a la valeur 0x00000001, ce qui indique que le serveur est un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="2babc-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="2babc-4786">**\_ cbBlob1** est défini sur la taille, en octets, des champs cPropSet, PropertySet1 et PropertySet2 combinés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="2babc-4787">**\_ cbBlob2** a la valeur 0x00000004 (ce qui signifie qu’il n’y a pas de jeux de propriétés supplémentaires).</span><span class="sxs-lookup"><span data-stu-id="2babc-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="2babc-4788">**MachineName** a pour valeur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="2babc-4789">Le **nom d’utilisateur** est défini sur John.</span><span class="sxs-lookup"><span data-stu-id="2babc-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="2babc-4790">**cPropSets** a la valeur 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="2babc-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="2babc-4791">Le champ **PropertySet1** est de type CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="2babc-4792">La structure CDbPropSet comprenant le champ PropertySet1 est remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="2babc-4793">Le champ **GuidPropSet** est défini sur A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ ext).</span><span class="sxs-lookup"><span data-stu-id="2babc-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="2babc-4794">le champ **cProperties** est défini sur 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="2babc-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="2babc-4795">le champ **aProps** est un tableau de structures CDbProp.</span><span class="sxs-lookup"><span data-stu-id="2babc-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="2babc-4796">Pour l' **élément \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="2babc-4797">**PropId** a la valeur 0X00000002 (DBPROP \_ ci \_ nom du catalogue \_ ).</span><span class="sxs-lookup"><span data-stu-id="2babc-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="2babc-4798">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="2babc-4799">**DBPROPSTATUS** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4800">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="2babc-4801">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid)</span><span class="sxs-lookup"><span data-stu-id="2babc-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="2babc-4802">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="2babc-4803">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4804">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="2babc-4805">**vType** est défini sur 0X001F (VT \_ LPWStr).</span><span class="sxs-lookup"><span data-stu-id="2babc-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="2babc-4806">**vValue** est défini sur « System », le nom du catalogue souhaité.</span><span class="sxs-lookup"><span data-stu-id="2babc-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="2babc-4807">Pour l' **élément \[ aProps \] 1** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="2babc-4808">**PropId** est défini sur 0x00000007 ( \_ type de \_ requête DBPROP ci \_ )</span><span class="sxs-lookup"><span data-stu-id="2babc-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="2babc-4809">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="2babc-4810">**DBPROPSTATUS** est défini sur to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4811">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="2babc-4812">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="2babc-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="2babc-4813">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="2babc-4814">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4815">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="2babc-4816">**vType** est défini sur 0X0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="2babc-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="2babc-4817">**vValue** a la valeur 0X00000000 (CiNormal), ce qui signifie qu’il s’agit d’une requête normale.</span><span class="sxs-lookup"><span data-stu-id="2babc-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="2babc-4818">Pour l' **élément \[ aProps \] 2** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="2babc-4819">**PropId** a la valeur 0x00000004 (indicateurs d’étendue d’DBPROP \_ ci \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="2babc-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="2babc-4820">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="2babc-4821">**DBPROPSTATUS** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4822">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="2babc-4823">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="2babc-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="2babc-4824">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="2babc-4825">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4826">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="2babc-4827">**vType**: 0X1003 (VT \_ Vector \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="2babc-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="2babc-4828">**vValue**: 0x00000001/0x00000001 (un élément avec la valeur 1), ce qui signifie que les sous-dossiers de recherche</span><span class="sxs-lookup"><span data-stu-id="2babc-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="2babc-4829">Pour l' **élément \[ aProps \] 3** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="2babc-4830">**PropId**: 0X00000003 (DBPROP \_ ci \_ include include \_ )</span><span class="sxs-lookup"><span data-stu-id="2babc-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="2babc-4831">**DBPROPOPTIONS**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="2babc-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="2babc-4832">**DBPROPSTATUS**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="2babc-4833">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="2babc-4834">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="2babc-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="2babc-4835">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="2babc-4836">**ulID** a la valeur 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="2babc-4837">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="2babc-4838">**vType** est défini sur 0X101F (VT \_ Vector \| VT \_ LPWStr).</span><span class="sxs-lookup"><span data-stu-id="2babc-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="2babc-4839">**vValue** est défini sur 0x00000001/0x00000002/" \\ " (un élément avec une chaîne de 2 caractères se terminant par un caractère null), ce qui correspond à l’étendue racine.</span><span class="sxs-lookup"><span data-stu-id="2babc-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="2babc-4840">Le champ **PropertySet2** est de type CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="2babc-4841">La structure CDbPropSet comprenant le champ PropertySet1 est remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="2babc-4842">**GuidPropSet** est défini sur AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ ext).</span><span class="sxs-lookup"><span data-stu-id="2babc-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="2babc-4843">le champ **cProperties** est défini sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="2babc-4844">Le champ **aProps** est un tableau de structures CDbProp.</span><span class="sxs-lookup"><span data-stu-id="2babc-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="2babc-4845">Pour l' **élément \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="2babc-4846">**PropId** a la valeur 0X00000002 (DBPROP \_ machine).</span><span class="sxs-lookup"><span data-stu-id="2babc-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="2babc-4847">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="2babc-4848">**DBPROPSTATUS** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4849">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="2babc-4850">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid),</span><span class="sxs-lookup"><span data-stu-id="2babc-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="2babc-4851">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="2babc-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="2babc-4852">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-4853">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="2babc-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="2babc-4854">**vType**: 0X0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="2babc-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="2babc-4855">**vValue**: 0x04/"x" (4 octets/chaîne Unicode terminée par un caractère null), signifiant "X"-nom d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="2babc-4856">le champ **cExtPropSet** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="2babc-4857">le tableau **aPropertySets** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="2babc-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="2babc-4858">Les différents champs de remplissage sont renseignés en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="2babc-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="2babc-4859">Le message est envoyé au serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="2babc-4860">Le serveur vérifie que le **\_ ulChecksum** est correct, vérifie que l’utilisateur est autorisé à effectuer cette demande et répond avec un message CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="2babc-4861">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4862">**\_ MSG** a la valeur 0x000000C8, ce qui indique qu’il s’agit d’un message CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="2babc-4863">l' **\_ État** est défini sur 0X0000000 indiquant la réussite.</span><span class="sxs-lookup"><span data-stu-id="2babc-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="2babc-4864">**\_ ulChecksum** a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="2babc-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="2babc-4865">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="2babc-4866">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4867">le champ **\_ ServerVersion** est défini sur 0x00000007 (32 bits windows XP ou 32 bits Windows Server 2003).</span><span class="sxs-lookup"><span data-stu-id="2babc-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="2babc-4868">les champs **\_ réservés** sont remplis avec des données arbitraires.</span><span class="sxs-lookup"><span data-stu-id="2babc-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="2babc-4869">Le client prépare un message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="2babc-4870">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4871">**\_ MSG** a la valeur 0x000000CA, ce qui indique qu’il s’agit d’un message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="2babc-4872">l' **\_ État** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="2babc-4873">**\_ ulChecksum** contient la somme de contrôle calculée d’après 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="2babc-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="2babc-4874">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="2babc-4875">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4876">Le champ **taille** est défini sur la taille du reste du message.</span><span class="sxs-lookup"><span data-stu-id="2babc-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="2babc-4877">Le champ **CColumnSetPresent** est défini sur 0x01.</span><span class="sxs-lookup"><span data-stu-id="2babc-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="2babc-4878">Le champ **ColumnSet** est de type CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="2babc-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="2babc-4879">La structure CColumnSet comprenant ce champ est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="2babc-4880">le champ **\_ Count** a la valeur 0x00000001, indiquant qu’une colonne est retournée.</span><span class="sxs-lookup"><span data-stu-id="2babc-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="2babc-4881">le tableau d' **index** est 0x00000000 et indique la première entrée dans \_ aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="2babc-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="2babc-4882">Le champ **CRestrictionPresent** est défini sur 0x01, ce qui indique que le champ de **restriction** est présent.</span><span class="sxs-lookup"><span data-stu-id="2babc-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="2babc-4883">Le champ de **restriction** est de type CRestriction et a la valeur :</span><span class="sxs-lookup"><span data-stu-id="2babc-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="2babc-4884">**\_ ulType** est défini sur 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="2babc-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="2babc-4885">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="2babc-4886">Le reste du champ contient une structure CContentRestriction :</span><span class="sxs-lookup"><span data-stu-id="2babc-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="2babc-4887">La **\_ propriété** est définie sur GUID B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13 qui représente le corps du document.</span><span class="sxs-lookup"><span data-stu-id="2babc-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="2babc-4888">**\_ CC** est défini sur 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="2babc-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="2babc-4889">**\_ pwcsphrase** est défini sur la chaîne « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="2babc-4890">**\_ LCID** est défini sur 0x40C (pour l’anglais).</span><span class="sxs-lookup"><span data-stu-id="2babc-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="2babc-4891">**\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).</span><span class="sxs-lookup"><span data-stu-id="2babc-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="2babc-4892">**CSortPresent** est défini sur 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="2babc-4893">**CCategorizationSetPresent** est défini sur 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="2babc-4894">**RowSetProperties** est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="2babc-4895">**\_ uBooleanOptions** a la valeur 0x00000001 (Sequential).</span><span class="sxs-lookup"><span data-stu-id="2babc-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="2babc-4896">**\_ ulMaxOpenRows** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="2babc-4897">**\_ ulMemoryUsage** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="2babc-4898">\_**cMaxResults** est défini sur 0x00000100 (retourner au maximum 256 lignes).</span><span class="sxs-lookup"><span data-stu-id="2babc-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="2babc-4899">**\_ cCmdTimeOut** a la valeur 0x00000000 (jamais timeout).</span><span class="sxs-lookup"><span data-stu-id="2babc-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="2babc-4900">**PidMapper** a la valeur :</span><span class="sxs-lookup"><span data-stu-id="2babc-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="2babc-4901">**\_ Count** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="2babc-4902">**\_ aPropSpec** est défini sur GUID B725F130-47EF-101A-a5-F1-02608C9EEBAC/0X00000001 (pour PRSPEC \_ propid)/0x0000000c qui représente la propriété de taille de fichier Windows.</span><span class="sxs-lookup"><span data-stu-id="2babc-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="2babc-4903">Le serveur le traite et répond avec un message CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="2babc-4904">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4905">**\_ MSG** a la valeur 0x000000CA, ce qui indique qu’il s’agit d’un message CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="2babc-4906">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="2babc-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="2babc-4907">**\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="2babc-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="2babc-4908">**\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="2babc-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="2babc-4909">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4910">**\_ fTrueSeqeuntial** a la valeur 0x00000000, ce qui indique que la requête peut utiliser un index.</span><span class="sxs-lookup"><span data-stu-id="2babc-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="2babc-4911">**\_ fWorkIdUnique** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="2babc-4912">Le tableau **aCursors** contient un seul élément, représentant un handle de curseur pour cette requête.</span><span class="sxs-lookup"><span data-stu-id="2babc-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="2babc-4913">La valeur dépend de l’état du serveur.</span><span class="sxs-lookup"><span data-stu-id="2babc-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="2babc-4914">Supposons que la valeur retournée est 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="2babc-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="2babc-4915">Le client émet un message de demande CPMSetBindingsIn pour définir le format d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="2babc-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="2babc-4916">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4917">**\_ MSG** a la valeur 0x000000D0, ce qui indique qu’il s’agit d’un message CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="2babc-4918">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="2babc-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="2babc-4919">**\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="2babc-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="2babc-4920">**\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="2babc-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="2babc-4921">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4922">**\_ hCursor** est défini sur 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="2babc-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="2babc-4923">**\_ cbRow** est défini sur 0x10 (suffisamment grand pour tenir les colonnes).</span><span class="sxs-lookup"><span data-stu-id="2babc-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="2babc-4924">**\_ cbBindingDesc** est défini sur la taille des champs **\_ CColumns** et **\_ aColumns** combinés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="2babc-4925">**\_ CColumns** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="2babc-4926">le tableau **\_ aColumns** est défini de façon à contenir une structure CTableColumn contenant :</span><span class="sxs-lookup"><span data-stu-id="2babc-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="2babc-4927">**\_ PropSpec** est défini sur GUID b725f130-47EF-101A-a5-F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x0000000c qui représente la propriété de taille de fichier Windows.</span><span class="sxs-lookup"><span data-stu-id="2babc-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="2babc-4928">**\_ vType** est défini sur 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="2babc-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="2babc-4929">**\_ ValueUsed** est défini sur 0x01 (colonne transférée dans la ligne).</span><span class="sxs-lookup"><span data-stu-id="2babc-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="2babc-4930">**\_ ValueOffset** est défini sur 0x0002 (au début de la ligne).</span><span class="sxs-lookup"><span data-stu-id="2babc-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="2babc-4931">**\_ Value** est défini sur 0x08 (taille d’un UI8 VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="2babc-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="2babc-4932">**\_ StatusUsed** est défini sur 0x01.</span><span class="sxs-lookup"><span data-stu-id="2babc-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="2babc-4933">**\_ StatusOffset** est défini sur 0x0A.</span><span class="sxs-lookup"><span data-stu-id="2babc-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="2babc-4934">**\_ LengthUsed** est défini sur 0x00.</span><span class="sxs-lookup"><span data-stu-id="2babc-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="2babc-4935">Le serveur le traite et répond avec un message CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="2babc-4936">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4937">**\_ MSG** est défini sur 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="2babc-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="2babc-4938">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="2babc-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="2babc-4939">**\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="2babc-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="2babc-4940">**\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="2babc-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="2babc-4941">Le client émet un message de demande CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="2babc-4942">Supposons que le client est prêt à accepter 100 lignes à ce stade et qu’il les souhaite dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="2babc-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="2babc-4943">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4944">**\_ MSG** a la valeur 0x000000CC, ce qui indique qu’il s’agit d’un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="2babc-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="2babc-4945">l' **\_ État** est défini sur 0x00000000</span><span class="sxs-lookup"><span data-stu-id="2babc-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="2babc-4946">**\_ ulChecksum** contient la somme de contrôle calculée en fonction de la section 0.</span><span class="sxs-lookup"><span data-stu-id="2babc-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="2babc-4947">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="2babc-4948">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4949">**\_ hCursor** est défini sur 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="2babc-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="2babc-4950">**\_ cRowsToTransfer** est défini sur 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="2babc-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="2babc-4951">**\_ cRowWidth** est défini sur 0x00000010 (à partir des liaisons).</span><span class="sxs-lookup"><span data-stu-id="2babc-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="2babc-4952">**\_ cbSeek** est défini sur 0x14, qui est la taille des champs ETYPE, \_ Chapt et CRowSeekNext combinés.</span><span class="sxs-lookup"><span data-stu-id="2babc-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="2babc-4953">**\_ cbReserved** a la valeur 0x18 (0x14 plus \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="2babc-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="2babc-4954">**\_ cbReadBuffer** est défini sur 0x800 (0x64 \* 0x10 est arrondi au multiple suivant de 0x200).</span><span class="sxs-lookup"><span data-stu-id="2babc-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="2babc-4955">**\_ ulClientBase** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="2babc-4956">**\_ fBwdfetch** a la valeur 0x00000000, ce qui indique que les lignes doivent être extraites dans l’ordre de transmission.</span><span class="sxs-lookup"><span data-stu-id="2babc-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="2babc-4957">**ETYPE** a la valeur 0x0000001, ce qui indique que le client souhaite les lignes suivantes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="2babc-4958">**\_ Chapt** a la valeur 0 (pas un résultat chapitre).</span><span class="sxs-lookup"><span data-stu-id="2babc-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="2babc-4959">**SeekDescription** est défini sur CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="2babc-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="2babc-4960">La structure CRowSeekNext contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2babc-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="2babc-4961">**CiTblChapt** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="2babc-4962">**\_ hRegion** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="2babc-4963">**\_ cSkip** a la valeur 0, ce qui indique que le client ne souhaite pas ignorer les lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="2babc-4964">Le serveur le traite et répond avec un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="2babc-4965">Supposons que le serveur a trouvé 100 documents qui contiennent le mot « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="2babc-4966">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4967">**\_ MSG** a la valeur 0x000000CC, ce qui indique qu’il s’agit d’un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="2babc-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="2babc-4968">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="2babc-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="2babc-4969">**\_ ulChecksum** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="2babc-4970">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="2babc-4971">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4972">**\_ CRowsReturned** est défini sur 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="2babc-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="2babc-4973">**ETYPE** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="2babc-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="2babc-4974">**\_ Chapt** a la valeur 0x00000000 (pas un résultat chapitre).</span><span class="sxs-lookup"><span data-stu-id="2babc-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="2babc-4975">**SeekDescription** contient une structure CRowSeekNext, remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="2babc-4976">**CiTblChapt** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="2babc-4977">**\_ hRegion** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="2babc-4978">**\_ cSkip** a la valeur 0, ce qui indique que le client ne souhaite pas ignorer les lignes.</span><span class="sxs-lookup"><span data-stu-id="2babc-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="2babc-4979">**Lignes** contient la taille des documents 100 qui contiennent le mot « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="2babc-4980">Étant donné qu’il s’agit de données de taille fixe, elles sont simplement structurées sous la forme d’une liste d’entiers non signés de 100 à 8 octets.</span><span class="sxs-lookup"><span data-stu-id="2babc-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="2babc-4981">Le client envoie un message CPMDisconnect pour mettre fin à la connexion.</span><span class="sxs-lookup"><span data-stu-id="2babc-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="2babc-4982">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="2babc-4983">**\_ MSG** a la valeur 0x000000C9, ce qui indique qu’il s’agit d’un message CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="2babc-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="2babc-4984">l' **\_ État** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="2babc-4985">**\_ ulChecksum** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="2babc-4986">Le serveur traite le message et supprime tous les États du client.</span><span class="sxs-lookup"><span data-stu-id="2babc-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="2babc-4987">4,2 exemple 2</span><span class="sxs-lookup"><span data-stu-id="2babc-4987">4.2 Example 2</span></span>

<span data-ttu-id="2babc-4988">Dans l’exemple précédent, la requête était assez simple.</span><span class="sxs-lookup"><span data-stu-id="2babc-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="2babc-4989">Prenons maintenant une requête légèrement plus complexe.</span><span class="sxs-lookup"><span data-stu-id="2babc-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="2babc-4990">Supposons que l’utilisateur souhaite récupérer la taille des documents qui contiennent les deux mots suivants : « Microsoft » et « Office ».</span><span class="sxs-lookup"><span data-stu-id="2babc-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="2babc-4991">Cela est spécifié en modifiant le champ de restriction contenu dans le message CPMCreateQueryIn envoyé à l’étape 5 comme suit :</span><span class="sxs-lookup"><span data-stu-id="2babc-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="2babc-4992">Le champ de **restriction** est de type CRestriction et a la valeur :</span><span class="sxs-lookup"><span data-stu-id="2babc-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="2babc-4993">**\_ ulType** est défini sur 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="2babc-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="2babc-4994">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="2babc-4995">Le reste du champ contient une structure CNodeRestriction :</span><span class="sxs-lookup"><span data-stu-id="2babc-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="2babc-4996">**\_ CNode** a la valeur 0x00000002, ce qui indique qu’il existe deux nœuds dans le tableau paNode.</span><span class="sxs-lookup"><span data-stu-id="2babc-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="2babc-4997">Le champ **\_ paNode** est un tableau de deux structures CRestriction.</span><span class="sxs-lookup"><span data-stu-id="2babc-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="2babc-4998">**\_ paNode \[ 0 \]** contient :</span><span class="sxs-lookup"><span data-stu-id="2babc-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="2babc-4999">**\_ ulType** est défini sur 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="2babc-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="2babc-5000">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-5001">Le reste du champ contient une structure CContentRestriction :</span><span class="sxs-lookup"><span data-stu-id="2babc-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="2babc-5002">La **\_ propriété** est définie sur GUID b725f130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="2babc-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="2babc-5003">**\_ CC** est défini sur 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="2babc-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="2babc-5004">**\_ pwcsphrase** est défini sur la chaîne « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="2babc-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="2babc-5005">**\_ LCID** est défini sur 0x40C (pour l’anglais).</span><span class="sxs-lookup"><span data-stu-id="2babc-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="2babc-5006">**\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).</span><span class="sxs-lookup"><span data-stu-id="2babc-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="2babc-5007">**\_ paNode \[ 1 \]** contient :</span><span class="sxs-lookup"><span data-stu-id="2babc-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="2babc-5008">**\_ ulType** est défini sur 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="2babc-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="2babc-5009">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2babc-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="2babc-5010">Le reste du champ contient une structure CContentRestriction :</span><span class="sxs-lookup"><span data-stu-id="2babc-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="2babc-5011">La **\_ propriété** est définie sur GUID b725f130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="2babc-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="2babc-5012">**\_ CC** est défini sur 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="2babc-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="2babc-5013">**\_ pwcsphrase** est défini sur la chaîne « Office ».</span><span class="sxs-lookup"><span data-stu-id="2babc-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="2babc-5014">**\_ LCID** est défini sur 0x40C (pour l’anglais).</span><span class="sxs-lookup"><span data-stu-id="2babc-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="2babc-5015">**\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).</span><span class="sxs-lookup"><span data-stu-id="2babc-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="2babc-5016">5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="2babc-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="2babc-5017">5.1 Considérations relatives à la sécurité pour les implémenteurs</span><span class="sxs-lookup"><span data-stu-id="2babc-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="2babc-5018">Les implémentations d’indexation qui permettent d’indexer du contenu sécurisé doivent envisager d’utiliser le contexte utilisateur fourni par SMB \[ MS-SMB \] pour supprimer les résultats de recherche et retourner uniquement ceux accessibles à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="2babc-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="2babc-5019">5.2 Index de paramètres de sécurité</span><span class="sxs-lookup"><span data-stu-id="2babc-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="2babc-5020">Paramètre de sécurité</span><span class="sxs-lookup"><span data-stu-id="2babc-5020">Security Parameter</span></span>  | <span data-ttu-id="2babc-5021">Section</span><span class="sxs-lookup"><span data-stu-id="2babc-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="2babc-5022">Niveau d'emprunt d'identité</span><span class="sxs-lookup"><span data-stu-id="2babc-5022">Impersonation level</span></span> | <span data-ttu-id="2babc-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="2babc-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="2babc-5024">6 index du comportement spécifique à la version</span><span class="sxs-lookup"><span data-stu-id="2babc-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="2babc-5025">Comportement spécifique à la version</span><span class="sxs-lookup"><span data-stu-id="2babc-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="2babc-5026">Section</span><span class="sxs-lookup"><span data-stu-id="2babc-5026">Section</span></span>   | <span data-ttu-id="2babc-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2babc-5027">Windows 2000</span></span> | <span data-ttu-id="2babc-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2babc-5028">Windows XP</span></span> | <span data-ttu-id="2babc-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2babc-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="2babc-5030">Ce protocole est implémenté sur Windows 2000, Windows XP, Windows Server 2003 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2babc-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="2babc-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="2babc-5031">1.3.2</span></span>     | <span data-ttu-id="2babc-5032">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5032">X</span></span>            | <span data-ttu-id="2babc-5033">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5033">X</span></span>          | <span data-ttu-id="2babc-5034">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5034">X</span></span>                   |
| <span data-ttu-id="2babc-5035">Les applications interagissent généralement avec un wrapper d’interface OLE DB</span><span class="sxs-lookup"><span data-stu-id="2babc-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="2babc-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="2babc-5036">1.4</span></span>       | <span data-ttu-id="2babc-5037">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5037">X</span></span>            | <span data-ttu-id="2babc-5038">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5038">X</span></span>          | <span data-ttu-id="2babc-5039">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5039">X</span></span>                   |
| <span data-ttu-id="2babc-5040">Valeurs NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="2babc-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="2babc-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="2babc-5041">1.8</span></span>       | <span data-ttu-id="2babc-5042">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5042">X</span></span>            | <span data-ttu-id="2babc-5043">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5043">X</span></span>          | <span data-ttu-id="2babc-5044">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5044">X</span></span>                   |
| <span data-ttu-id="2babc-5045">Le client définit le \_ champ d’État dans chaque en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="2babc-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="2babc-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="2babc-5046">2.2.2</span></span>     | <span data-ttu-id="2babc-5047">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5047">X</span></span>            | <span data-ttu-id="2babc-5048">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5048">X</span></span>          | <span data-ttu-id="2babc-5049">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5049">X</span></span>                   |
| <span data-ttu-id="2babc-5050">la valeur de cPendingScans est généralement zéro</span><span class="sxs-lookup"><span data-stu-id="2babc-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="2babc-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="2babc-5051">2.2.3.1</span></span>   | <span data-ttu-id="2babc-5052">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5052">X</span></span>            | <span data-ttu-id="2babc-5053">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5053">X</span></span>          | <span data-ttu-id="2babc-5054">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5054">X</span></span>                   |
| <span data-ttu-id="2babc-5055">valeur iClientVersion</span><span class="sxs-lookup"><span data-stu-id="2babc-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="2babc-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="2babc-5056">2.2.3.6</span></span>   | <span data-ttu-id="2babc-5057">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5057">X</span></span>            | <span data-ttu-id="2babc-5058">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5058">X</span></span>          | <span data-ttu-id="2babc-5059">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5059">X</span></span>                   |
| <span data-ttu-id="2babc-5060">\_valeur cbChunk</span><span class="sxs-lookup"><span data-stu-id="2babc-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="2babc-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="2babc-5061">2.2.3.19</span></span>  | <span data-ttu-id="2babc-5062">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5062">X</span></span>            | <span data-ttu-id="2babc-5063">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5063">X</span></span>          | <span data-ttu-id="2babc-5064">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5064">X</span></span>                   |
| <span data-ttu-id="2babc-5065">adresses mémoire 32 bits et 64 bits</span><span class="sxs-lookup"><span data-stu-id="2babc-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="2babc-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="2babc-5066">3.2.4.2.4</span></span> | <span data-ttu-id="2babc-5067">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5067">X</span></span>            | <span data-ttu-id="2babc-5068">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5068">X</span></span>          | <span data-ttu-id="2babc-5069">X</span><span class="sxs-lookup"><span data-stu-id="2babc-5069">X</span></span>                   |



 

 

 





