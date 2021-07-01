---
title: Protocole des services d’indexation de contenu
description: Ce document est une spécification du protocole de service d’indexation de contenu.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119734"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="999c8-103">Protocole des services d’indexation de contenu</span><span class="sxs-lookup"><span data-stu-id="999c8-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="999c8-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="999c8-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="999c8-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="999c8-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="999c8-106">Spécification de protocole, version 0,12</span><span class="sxs-lookup"><span data-stu-id="999c8-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="999c8-107">1 Introduction</span><span class="sxs-lookup"><span data-stu-id="999c8-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="999c8-108">1.1 Glossaire</span><span class="sxs-lookup"><span data-stu-id="999c8-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="999c8-109">1.2 Références</span><span class="sxs-lookup"><span data-stu-id="999c8-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="999c8-110">Vue d’ensemble du protocole 1,3 (synopsis)</span><span class="sxs-lookup"><span data-stu-id="999c8-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="999c8-111">1.4 Relation aux autres protocoles</span><span class="sxs-lookup"><span data-stu-id="999c8-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="999c8-112">1,5 conditions préalables et conditions préalables</span><span class="sxs-lookup"><span data-stu-id="999c8-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="999c8-113">1.6 Instruction d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="999c8-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="999c8-114">1.7 Contrôle de version et négociation de capacité</span><span class="sxs-lookup"><span data-stu-id="999c8-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="999c8-115">1.8 Champs extensibles de fournisseur</span><span class="sxs-lookup"><span data-stu-id="999c8-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="999c8-116">1.9 Affectations de normes</span><span class="sxs-lookup"><span data-stu-id="999c8-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="999c8-117">2 Messages</span><span class="sxs-lookup"><span data-stu-id="999c8-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="999c8-118">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="999c8-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="999c8-119">2.2 Syntaxe de message</span><span class="sxs-lookup"><span data-stu-id="999c8-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="999c8-120">3 Détails du protocole</span><span class="sxs-lookup"><span data-stu-id="999c8-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="999c8-121">Détails du serveur 3,1</span><span class="sxs-lookup"><span data-stu-id="999c8-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="999c8-122">Détails du client 3,2</span><span class="sxs-lookup"><span data-stu-id="999c8-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="999c8-123">4 Exemples de protocoles</span><span class="sxs-lookup"><span data-stu-id="999c8-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="999c8-124">4,1 exemple 1</span><span class="sxs-lookup"><span data-stu-id="999c8-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="999c8-125">4,2 exemple 2</span><span class="sxs-lookup"><span data-stu-id="999c8-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="999c8-126">5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="999c8-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="999c8-127">5.1 Considérations relatives à la sécurité pour les implémenteurs</span><span class="sxs-lookup"><span data-stu-id="999c8-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="999c8-128">5.2 Index de paramètres de sécurité</span><span class="sxs-lookup"><span data-stu-id="999c8-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="999c8-129">6 index du comportement spécifique à la version</span><span class="sxs-lookup"><span data-stu-id="999c8-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="999c8-130">Ce document est une spécification du protocole de service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="999c8-131">La documentation du programme de protocole du serveur de groupe de travail (WSPP) est destinée à être utilisée conjointement avec la documentation sur les normes publiques, la conception de la programmation réseau et les concepts des systèmes distribués de groupe de travail Windows, et suppose que le lecteur est familiarisé avec le matériel mentionné ci-dessus ou qu’il y accède immédiatement.</span><span class="sxs-lookup"><span data-stu-id="999c8-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="999c8-132">Une spécification de protocole WSPP ne nécessite pas l’utilisation d’outils de programmation ou d’environnements de programmation Microsoft pour permettre à un licencié de développer une implémentation.</span><span class="sxs-lookup"><span data-stu-id="999c8-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="999c8-133">Les titulaires de licences qui ont accès aux outils et aux environnements de programmation de Microsoft sont gratuits pour en tirer parti.</span><span class="sxs-lookup"><span data-stu-id="999c8-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="999c8-134">1 Introduction</span><span class="sxs-lookup"><span data-stu-id="999c8-134">1 Introduction</span></span>

-   [<span data-ttu-id="999c8-135">1.1 Glossaire</span><span class="sxs-lookup"><span data-stu-id="999c8-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="999c8-136">1.2 Références</span><span class="sxs-lookup"><span data-stu-id="999c8-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="999c8-137">Vue d’ensemble du protocole 1,3 (synopsis)</span><span class="sxs-lookup"><span data-stu-id="999c8-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="999c8-138">1.4 Relation aux autres protocoles</span><span class="sxs-lookup"><span data-stu-id="999c8-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="999c8-139">1,5 conditions préalables et conditions préalables</span><span class="sxs-lookup"><span data-stu-id="999c8-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="999c8-140">1.6 Instruction d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="999c8-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="999c8-141">1.7 Contrôle de version et négociation de capacité</span><span class="sxs-lookup"><span data-stu-id="999c8-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="999c8-142">1.8 Champs extensibles de fournisseur</span><span class="sxs-lookup"><span data-stu-id="999c8-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="999c8-143">1.9 Affectations de normes</span><span class="sxs-lookup"><span data-stu-id="999c8-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="999c8-144">1.1 Glossaire</span><span class="sxs-lookup"><span data-stu-id="999c8-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="999c8-145">Les termes suivants sont définis dans la section Glossaire de \[ ms-sys \] :</span><span class="sxs-lookup"><span data-stu-id="999c8-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="999c8-146">GUID</span><span class="sxs-lookup"><span data-stu-id="999c8-146">GUID</span></span>
> -   <span data-ttu-id="999c8-147">Little endian</span><span class="sxs-lookup"><span data-stu-id="999c8-147">Little Endian</span></span>
> -   <span data-ttu-id="999c8-148">Canal nommé</span><span class="sxs-lookup"><span data-stu-id="999c8-148">Named Pipe</span></span>
> -   <span data-ttu-id="999c8-149">Path</span><span class="sxs-lookup"><span data-stu-id="999c8-149">Path</span></span>

 

<span data-ttu-id="999c8-150">**Binding**: demande d’inclusion d’une **colonne** particulière dans un **ensemble de lignes** retourné.</span><span class="sxs-lookup"><span data-stu-id="999c8-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="999c8-151">La **liaison** spécifie une propriété à inclure dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="999c8-152">**Bookmark**: marqueur qui identifie de façon unique une ligne dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="999c8-153">**Catalogue**: unité de niveau le plus élevé de l’organisation dans le service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="999c8-154">Il représente un ensemble de documents indexés par rapport auxquels les requêtes peuvent être exécutées à l’aide du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="999c8-155">**Category**: regroupement hiérarchique de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="999c8-156">Par exemple, un résultat de requête contenant les colonnes auteur et titre peut être classé en fonction de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="999c8-157">Chaque groupe de lignes contenant la même valeur pour l’auteur constitue une catégorie.</span><span class="sxs-lookup"><span data-stu-id="999c8-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="999c8-158">**Chapitre** : plage de **lignes** au sein d’un ensemble de **lignes** .</span><span class="sxs-lookup"><span data-stu-id="999c8-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="999c8-159">**Column**: conteneur pour un seul type d’informations dans une **ligne** .</span><span class="sxs-lookup"><span data-stu-id="999c8-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="999c8-160">Les colonnes sont mappées à des noms de propriété et spécifient les propriétés qui sont utilisées pour les éléments de l' **arborescence** de **commandes** de la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="999c8-161">**Arborescence de commandes**: combinaison des **restrictions** , **catégories** et **ordres de tri** spécifiés pour la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="999c8-162">**Cursor**: entité utilisée comme mécanisme pour travailler avec une **ligne** ou un petit bloc de **lignes** à la fois dans un jeu de données retourné dans un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="999c8-163">Un **curseur** est positionné sur une seule **ligne** dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="999c8-164">Une fois que le **curseur** est positionné sur une ligne, les opérations peuvent être effectuées sur cette **ligne** ou sur un bloc de **lignes** commençant à cette position.</span><span class="sxs-lookup"><span data-stu-id="999c8-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="999c8-165">**Handle**: jeton qui peut être utilisé pour identifier les **curseurs** , les **chapitres** et les **signets** et y accéder.</span><span class="sxs-lookup"><span data-stu-id="999c8-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="999c8-166">**Index**: structure persistante qui contient le texte extrait des fichiers par un service d' **indexation** .</span><span class="sxs-lookup"><span data-stu-id="999c8-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="999c8-167">Cela comprend la liste des mots, qui sont stockés avec le nom de fichier, l’emplacement de mot et les **paramètres régionaux** qui le contiennent.</span><span class="sxs-lookup"><span data-stu-id="999c8-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="999c8-168">**Indexation**: processus d’extraction de texte et de propriétés de fichiers et de stockage des valeurs extraites dans les **index** (pour le texte) et dans le **cache de propriétés** (pour les propriétés).</span><span class="sxs-lookup"><span data-stu-id="999c8-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="999c8-169">**Service d’indexation**: service qui crée des **catalogues** indexés pour le contenu et les propriétés des systèmes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="999c8-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="999c8-170">Les applications peuvent rechercher des informations dans les catalogues à partir des fichiers du système de fichiers indexé.</span><span class="sxs-lookup"><span data-stu-id="999c8-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="999c8-171">**Paramètres régionaux**: identificateur, tel que spécifié dans \[ MS-GPSI \] annexe A, qui spécifie les préférences relatives à la langue.</span><span class="sxs-lookup"><span data-stu-id="999c8-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="999c8-172">Ces préférences indiquent comment les dates et les heures doivent être mises en forme, les éléments doivent être triés par ordre alphabétique, les chaînes doivent être comparées, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="999c8-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="999c8-173">**Requête en langage naturel**: requête construite à l’aide de la langue humaine au lieu de la syntaxe de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="999c8-174">**Mot parasite**: mot ignoré par le service d’indexation lorsqu’il est présent dans les **restrictions** spécifiées pour la requête de recherche, car il a peu de valeur discriminatoire.</span><span class="sxs-lookup"><span data-stu-id="999c8-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="999c8-175">Les exemples en anglais incluent « a », « and » et « The ».</span><span class="sxs-lookup"><span data-stu-id="999c8-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="999c8-176">**Cache de propriété**: cache des propriétés de fichier extraites par un **service d’indexation** .</span><span class="sxs-lookup"><span data-stu-id="999c8-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="999c8-177">**Indexation** des propriétés : processus de création d’un **index** de **Propriétés de type valeur** d’un document, notamment l’auteur, l’objet, le type, le nombre de mots, le nombre de pages imprimées et toutes les autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="999c8-178">**Restriction**: ensemble de conditions qu’un fichier doit remplir pour être inclus dans les résultats de recherche retournés par le **service d’indexation** en réponse à une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="999c8-179">Une **restriction** réduit le focus d’une requête de recherche, limitant ainsi les fichiers que le **service d’indexation** inclura dans les résultats de la recherche à ceux qui répondent aux conditions.</span><span class="sxs-lookup"><span data-stu-id="999c8-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="999c8-180">**Row**: collection de **colonnes** contenant les valeurs de propriété qui décrivent un fichier unique à partir de l’ensemble de fichiers correspondant aux **restrictions** spécifiées dans la requête de recherche envoyée au **service d’indexation** .</span><span class="sxs-lookup"><span data-stu-id="999c8-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="999c8-181">**Rowset**: ensemble de **lignes** renvoyées dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="999c8-182">**Ordre de tri**: ensemble de règles dans une requête de recherche qui définit l’ordre des lignes dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="999c8-183">Chaque règle se compose d’une propriété (nom, taille, etc.) et d’une direction pour le tri (croissant ou décroissant).</span><span class="sxs-lookup"><span data-stu-id="999c8-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="999c8-184">Plusieurs règles sont appliquées séquentiellement</span><span class="sxs-lookup"><span data-stu-id="999c8-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="999c8-185">**Propriété Text-type**: propriété qui décrit le contenu d’un document et dont le texte n’est pas mis en forme et qui est associé à son nom.</span><span class="sxs-lookup"><span data-stu-id="999c8-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="999c8-186">**Propriété de type valeur**: propriété qui décrit un attribut unique d’un document entier.</span><span class="sxs-lookup"><span data-stu-id="999c8-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="999c8-187">Une propriété de type valeur a un ID de type de données et une valeur de ce type de données associé à son nom.</span><span class="sxs-lookup"><span data-stu-id="999c8-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="999c8-188">**Racine virtuelle**: autre chemin d’accès à un dossier.</span><span class="sxs-lookup"><span data-stu-id="999c8-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="999c8-189">Un dossier physique peut avoir zéro ou plusieurs racines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="999c8-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="999c8-190">Les chemins d’accès commençant par une racine virtuelle sont appelés chemins d’accès virtuels.</span><span class="sxs-lookup"><span data-stu-id="999c8-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="999c8-191">Par exemple,/Server/vanityroot peut être une racine virtuelle de C : \\ IIS \\ Web \\ dossier1.</span><span class="sxs-lookup"><span data-stu-id="999c8-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="999c8-192">Ensuite, le fichier C : \\ IIS \\ web \\ dossier1 \\default.htm présenterait le chemin d’accès virtuel/Server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="999c8-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="999c8-193">**Peut**, doit, ne doit pas, ne doit pas : ces termes (en majuscules) sont utilisés comme décrit dans \[ rfc2119 \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="999c8-194">Toutes les instructions de comportement facultatif utilisent PEUT, DOIT ou NE DOIT PAS.</span><span class="sxs-lookup"><span data-stu-id="999c8-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="999c8-195">1.2 Références</span><span class="sxs-lookup"><span data-stu-id="999c8-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="999c8-196">1.2.1 Références normatives</span><span class="sxs-lookup"><span data-stu-id="999c8-196">1.2.1 Normative References</span></span>

<span data-ttu-id="999c8-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, « Standard for Binary Floating-Point arithmétique », IEEE 754-1985, octobre 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="999c8-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="999c8-198">\[MS-DCOM \] Microsoft Corporation, « protocoles distants de modèle objet de composant distribué », juin 2006.</span><span class="sxs-lookup"><span data-stu-id="999c8-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="999c8-199">\[MS-GPSI \] Microsoft Corporation, « Extension installation des logiciels de la stratégie de groupe », juin 2006.</span><span class="sxs-lookup"><span data-stu-id="999c8-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="999c8-200">\[MS-SMB \] Microsoft Corporation, « protocole et extensions Microsoft Server Message Block (SMB) », mai 2006.</span><span class="sxs-lookup"><span data-stu-id="999c8-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="999c8-201">\[MS-SYS \] Microsoft Corporation, « System Overview v4 », juillet 2006.</span><span class="sxs-lookup"><span data-stu-id="999c8-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="999c8-202">\[SALTON \] Salton, G., "traitement automatique du texte : analyse de la transformation et récupération des informations par l’ordinateur", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="999c8-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="999c8-203">\[UNICODE \] consortium Unicode, « la norme Unicode, Version 2,0 », 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="999c8-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="999c8-204">1.2.2 Références informatives</span><span class="sxs-lookup"><span data-stu-id="999c8-204">1.2.2 Informative References</span></span>

<span data-ttu-id="999c8-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="999c8-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="999c8-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valeurs, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="999c8-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="999c8-207">Vue d’ensemble du protocole 1,3 (synopsis)</span><span class="sxs-lookup"><span data-stu-id="999c8-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="999c8-208">Un **service d’indexation** de contenu permet d’organiser efficacement les fonctionnalités extraites d’une collection de documents.</span><span class="sxs-lookup"><span data-stu-id="999c8-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="999c8-209">Le protocole CISP (Content Indexing Service Protocol) permet à un client de communiquer avec un serveur hébergeant un service d’indexation pour émettre des requêtes et permettre à un administrateur de gérer le serveur d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="999c8-210">Lors du traitement de fichiers, un service d’indexation analyse un ensemble de documents et réorganise leur contenu de telle sorte que les **Propriétés** de ces documents peuvent être retournées efficacement en réponse aux requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="999c8-211">Une collection de documents qui peuvent être interrogés comprend un **catalogue** .</span><span class="sxs-lookup"><span data-stu-id="999c8-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="999c8-212">Un catalogue peut contenir un **index** (pour une référence rapide à du texte) et un **cache de propriétés** (pour une récupération rapide des valeurs de propriété).</span><span class="sxs-lookup"><span data-stu-id="999c8-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="999c8-213">Conceptuellement, un catalogue se compose d’une « table » logique de propriétés avec le texte ou la valeur et les paramètres régionaux correspondants stockés dans les **colonnes** de la table.</span><span class="sxs-lookup"><span data-stu-id="999c8-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="999c8-214">Chaque « ligne » de la table correspond à un document distinct dans l’étendue du catalogue et chaque « colonne » de la table correspond à une propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="999c8-215">Les tâches spécifiques effectuées par CISP sont regroupées en deux zones fonctionnelles :</span><span class="sxs-lookup"><span data-stu-id="999c8-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="999c8-216">Administration à distance des catalogues de service d’indexation,</span><span class="sxs-lookup"><span data-stu-id="999c8-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="999c8-217">Interrogation à distance des catalogues de service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="999c8-218">1.3.1 tâches d’administration à distance</span><span class="sxs-lookup"><span data-stu-id="999c8-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="999c8-219">CISP active les tâches de gestion du catalogue du service d’indexation suivantes à partir d’un client :</span><span class="sxs-lookup"><span data-stu-id="999c8-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="999c8-220">Interrogez l’état actuel d’un catalogue du service d’indexation sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="999c8-221">Mettre à jour l’état d’un catalogue de services d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="999c8-222">Lancez le processus d’indexation pour un ensemble de fichiers particulier.</span><span class="sxs-lookup"><span data-stu-id="999c8-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="999c8-223">Initiez l’optimisation d’un index afin d’améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="999c8-224">Toutes les tâches d’administration à distance suivent un modèle de requête/réponse simple.</span><span class="sxs-lookup"><span data-stu-id="999c8-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="999c8-225">Aucun État n’est conservé sur le client pour tout appel d’administration et les appels administratifs peuvent être effectués dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="999c8-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="999c8-226">1.3.2 interrogation à distance</span><span class="sxs-lookup"><span data-stu-id="999c8-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="999c8-227">CISP permet aux clients d’effectuer des requêtes de recherche sur un serveur distant qui héberge un service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="999c8-228">L’envoi d’une requête de recherche est un processus à plusieurs étapes initié par le client.</span><span class="sxs-lookup"><span data-stu-id="999c8-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="999c8-229">La procédure comporte trois étapes :</span><span class="sxs-lookup"><span data-stu-id="999c8-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="999c8-230">Le client demande une connexion à un serveur qui héberge un service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="999c8-231">Le client envoie les paramètres pour la requête de recherche, notamment :</span><span class="sxs-lookup"><span data-stu-id="999c8-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="999c8-232">**Restrictions** permettant de spécifier les documents à inclure et/ou à exclure des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="999c8-233">Ordre dans lequel les résultats de la recherche doivent être retournés.</span><span class="sxs-lookup"><span data-stu-id="999c8-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="999c8-234">Colonnes à retourner dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="999c8-235">Nombre maximal de **lignes** qui doivent être retournées pour la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="999c8-236">Durée maximale d’exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="999c8-237">Une fois que le serveur a accepté la demande de lancement de la requête du client, le client peut demander des informations d’État sur la requête, mais cette étape n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="999c8-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="999c8-238">Le client spécifie ensuite les propriétés que le serveur doit inclure dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="999c8-239">Le client demande un jeu de résultats sur le serveur, et le serveur répond en envoyant au client les valeurs de propriété des fichiers qui ont été inclus dans les résultats pour la requête de recherche du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="999c8-240">Si la valeur d’une propriété est trop grande pour tenir dans une seule mémoire tampon de réponse, le serveur n’envoie pas la propriété, mais définit plutôt l’état de la propriété sur différé.</span><span class="sxs-lookup"><span data-stu-id="999c8-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="999c8-241">Le client demande ensuite la valeur de propriété séparément à l’aide d’une série de demandes pour les segments successifs de la valeur, puis reprend la demande d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="999c8-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="999c8-242">Une fois que le client a terminé la requête de recherche et n’a plus besoin de résultats supplémentaires, le client contacte le serveur pour libérer la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="999c8-243">Une fois la requête lancée par le serveur, le client peut envoyer une demande de déconnexion du serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="999c8-244">La connexion est ensuite fermée.</span><span class="sxs-lookup"><span data-stu-id="999c8-244">The connection is then closed.</span></span> <span data-ttu-id="999c8-245">Le client peut également émettre une autre requête et répéter la séquence à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="999c8-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="999c8-246">Comportement de Windows : ce protocole est implémenté sur Windows 2000, Windows XP, Windows Server 2003 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="999c8-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="999c8-247">1.4 Relation aux autres protocoles</span><span class="sxs-lookup"><span data-stu-id="999c8-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="999c8-248">Le CISP s’appuie sur le \[ protocole SMB MS-SMB \] pour le transport des messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="999c8-249">Aucun autre protocole ne dépend directement du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="999c8-250">*Comportement de Windows : les applications interagissent généralement avec un wrapper d’interface OLE DB \[ MSDN-OLEDB \] (par exemple, un client de protocole) et pas directement avec le protocole.*</span><span class="sxs-lookup"><span data-stu-id="999c8-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="999c8-251">1,5 conditions préalables et conditions préalables</span><span class="sxs-lookup"><span data-stu-id="999c8-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="999c8-252">Il est supposé que le client a obtenu le nom du serveur et un nom de catalogue avant l’appel de ce protocole.</span><span class="sxs-lookup"><span data-stu-id="999c8-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="999c8-253">Le mode de fonctionnement d’un client est en dehors de la portée de cette spécification.</span><span class="sxs-lookup"><span data-stu-id="999c8-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="999c8-254">Il est également supposé que le client et le serveur ont une association de sécurité utilisable avec les canaux nommés \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="999c8-255">1.6 Instruction d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="999c8-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="999c8-256">CISP est conçu pour l’interrogation et la gestion des catalogues sur un serveur distant à partir d’un client.</span><span class="sxs-lookup"><span data-stu-id="999c8-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="999c8-257">CISP est déconseillé sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="999c8-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="999c8-258">1.7 Contrôle de version et négociation de capacité</span><span class="sxs-lookup"><span data-stu-id="999c8-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="999c8-259">Ce protocole n’a pas de mécanisme de contrôle de version ou de négociation de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="999c8-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="999c8-260">1.8 Champs extensibles de fournisseur</span><span class="sxs-lookup"><span data-stu-id="999c8-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="999c8-261">Ce protocole utilise des HRESULT qui sont extensibles par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="999c8-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="999c8-262">Les fournisseurs sont libres de choisir leurs propres valeurs pour ce champ, tant que le bit C (0x20000000) est défini comme indiqué dans la section 4.1.1 de \[ ms-sys \] , indiquant qu’il s’agit d’un code client.</span><span class="sxs-lookup"><span data-stu-id="999c8-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="999c8-263">Ce protocole utilise également les valeurs NTSTATUS extraites de l’espace de nombre NTSTATUS défini dans \[ ms-sys \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="999c8-264">Les fournisseurs doivent réutiliser ces valeurs avec leur signification indiquée.</span><span class="sxs-lookup"><span data-stu-id="999c8-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="999c8-265">Le choix d’une autre valeur exécute le risque d’une collision dans le futur.</span><span class="sxs-lookup"><span data-stu-id="999c8-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="999c8-266">*Comportement de Windows : Windows utilise uniquement les valeurs spécifiées dans la section 4.1.3 de \[ ms-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="999c8-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="999c8-267">ID de propriété 1.8.1</span><span class="sxs-lookup"><span data-stu-id="999c8-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="999c8-268">Les propriétés sont représentées par des ID connus sous le nom d’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="999c8-269">Chaque propriété doit avoir un identificateur global unique.</span><span class="sxs-lookup"><span data-stu-id="999c8-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="999c8-270">Cet identificateur se compose d’un **GUID** qui représente une collection de propriétés appelée un jeu de propriétés, plus une chaîne ou un entier 32 bits pour identifier la propriété dans le jeu.</span><span class="sxs-lookup"><span data-stu-id="999c8-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="999c8-271">Si la forme entière de ID est utilisée, les valeurs 0x00000000, 0xFFFFFFFF et 0xFFFFFFFE sont considérées comme non valides.</span><span class="sxs-lookup"><span data-stu-id="999c8-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="999c8-272">Les fournisseurs peuvent garantir que leurs propriétés sont définies de manière unique en les plaçant dans un jeu de propriétés défini par leur propre GUID.</span><span class="sxs-lookup"><span data-stu-id="999c8-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="999c8-273">1.9 Affectations de normes</span><span class="sxs-lookup"><span data-stu-id="999c8-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="999c8-274">Ce protocole n’a aucune attribution de normes, mais uniquement les affectations privées effectuées par Microsoft à l’aide de procédures d’allocation spécifiées dans d’autres protocoles.</span><span class="sxs-lookup"><span data-stu-id="999c8-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="999c8-275">Microsoft a alloué ce protocole à un canal nommé comme spécifié dans \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="999c8-276">L’attribution est :</span><span class="sxs-lookup"><span data-stu-id="999c8-276">The assignment is:</span></span>



| <span data-ttu-id="999c8-277">Paramètre</span><span class="sxs-lookup"><span data-stu-id="999c8-277">Parameter</span></span> | <span data-ttu-id="999c8-278">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-278">Value</span></span>             | <span data-ttu-id="999c8-279">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="999c8-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="999c8-280">Nom du canal</span><span class="sxs-lookup"><span data-stu-id="999c8-280">Pipe name</span></span> | <span data-ttu-id="999c8-281">\\canal d' \\ intégration de \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="999c8-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="999c8-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="999c8-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="999c8-283">2 Messages</span><span class="sxs-lookup"><span data-stu-id="999c8-283">2 Messages</span></span>

-   [<span data-ttu-id="999c8-284">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="999c8-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="999c8-285">2.2 Syntaxe de message</span><span class="sxs-lookup"><span data-stu-id="999c8-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="999c8-286">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="999c8-286">2.1 Transport</span></span>

<span data-ttu-id="999c8-287">Tous les messages doivent être transportés à l’aide d’un canal nommé, tel que spécifié dans \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="999c8-288">Le nom de canal suivant est utilisé :</span><span class="sxs-lookup"><span data-stu-id="999c8-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="999c8-289">\\canal d' \\ intégration de \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="999c8-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="999c8-290">Ce protocole utilise le protocole de canal nommé SMB sous-jacent pour récupérer l’identité de l’appelant qui a établi la connexion comme indiqué dans la section 2.2.8 de \[ MS-SMB \] ; le client doit définir l’identification de sécurité \_ en tant que ImpersonationLevel dans la demande pour ouvrir le canal nommé.</span><span class="sxs-lookup"><span data-stu-id="999c8-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="999c8-291">2.2 Syntaxe de message</span><span class="sxs-lookup"><span data-stu-id="999c8-291">2.2 Message Syntax</span></span>

<span data-ttu-id="999c8-292">Plusieurs structures et messages dans les sections suivantes font référence aux descripteurs de chapitres ou de signets.</span><span class="sxs-lookup"><span data-stu-id="999c8-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="999c8-293">Un descripteur est une structure opaque de 32 bits qui identifie de façon unique un chapitre ou un signet.</span><span class="sxs-lookup"><span data-stu-id="999c8-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="999c8-294">En règle générale, les applications clientes reçoivent des valeurs de handle via des appels de méthode ; Toutefois, il existe plusieurs valeurs connues qui n’ont pas besoin d’être obtenues à partir d’un serveur, ce qui signifie qu’elles sont spécifiées dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="999c8-295">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-295">Value</span></span>                         | <span data-ttu-id="999c8-296">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-297">DB \_ null \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="999c8-298">Descripteur de chapitre de l’ensemble de lignes non chapitre, contenant tous les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="999c8-299">DBBMK \_ premier 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="999c8-300">Handle de signet vers un signet qui identifie la première ligne dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="999c8-301">DBBMK \_ dernier 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="999c8-302">Handle de signet vers un signet qui identifie la dernière ligne de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="999c8-303">2.2.1 structures</span><span class="sxs-lookup"><span data-stu-id="999c8-303">2.2.1 Structures</span></span>

<span data-ttu-id="999c8-304">Cette section détaille les structures de données qui sont définies et utilisées par CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="999c8-305">Tous les entiers signés à 2, 4 et 8 octets et non signés dans les structures suivantes doivent être transférés dans l’ordre d’octet avec primauté des octets de poids faible (Little-endian).</span><span class="sxs-lookup"><span data-stu-id="999c8-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="999c8-306">Le tableau suivant récapitule les structures de données définies dans cette section.</span><span class="sxs-lookup"><span data-stu-id="999c8-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="999c8-307">Structure</span><span class="sxs-lookup"><span data-stu-id="999c8-307">Structure</span></span>                    | <span data-ttu-id="999c8-308">Description</span><span class="sxs-lookup"><span data-stu-id="999c8-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="999c8-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="999c8-310">Contient la valeur sur laquelle effectuer une opération de correspondance pour une propriété spécifiée dans une structure CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="999c8-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="999c8-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="999c8-312">Contient un tableau multidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="999c8-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="999c8-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="999c8-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="999c8-314">Représente les limites d’une dimension d’un tableau spécifié dans une structure SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="999c8-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="999c8-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-315">CFullPropSpec</span></span>                | <span data-ttu-id="999c8-316">Contient une spécification de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="999c8-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-317">CContentRestriction</span></span>          | <span data-ttu-id="999c8-318">Contient une chaîne à faire correspondre pour une valeur de propriété dans le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="999c8-319">CKey</span><span class="sxs-lookup"><span data-stu-id="999c8-319">CKey</span></span>                         | <span data-ttu-id="999c8-320">Contient une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="999c8-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="999c8-322">Contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="999c8-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="999c8-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="999c8-324">Contient une correspondance de requête en langage naturel pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="999c8-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-325">CNodeRestriction</span></span>             | <span data-ttu-id="999c8-326">Contient un tableau de nœuds d’arborescence de commandes spécifiant les restrictions pour une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="999c8-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-327">COccRestriction</span></span>              | <span data-ttu-id="999c8-328">Contient l’emplacement d’un mot dans une expression.</span><span class="sxs-lookup"><span data-stu-id="999c8-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="999c8-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-329">CPropertyRestriction</span></span>         | <span data-ttu-id="999c8-330">Contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="999c8-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="999c8-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-331">CRangeRestriction</span></span>            | <span data-ttu-id="999c8-332">Contient une restriction sur une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="999c8-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="999c8-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-333">CScopeRestriction</span></span>            | <span data-ttu-id="999c8-334">Contient une restriction sur les fichiers à rechercher.</span><span class="sxs-lookup"><span data-stu-id="999c8-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="999c8-335">CSort</span><span class="sxs-lookup"><span data-stu-id="999c8-335">CSort</span></span>                        | <span data-ttu-id="999c8-336">Identifie une colonne à trier.</span><span class="sxs-lookup"><span data-stu-id="999c8-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="999c8-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-337">CSynRestriction</span></span>              | <span data-ttu-id="999c8-338">Contient un mot ou ses synonymes pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="999c8-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-339">CVectorRestriction</span></span>           | <span data-ttu-id="999c8-340">Contient une opération pondérée sur un nœud d’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="999c8-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="999c8-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-341">CWordRestriction</span></span>             | <span data-ttu-id="999c8-342">Contient un mot pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="999c8-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-343">CRestriction</span></span>                 | <span data-ttu-id="999c8-344">Contient un nœud d’une arborescence de commandes de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="999c8-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="999c8-345">CColumnSet</span></span>                   | <span data-ttu-id="999c8-346">Indique le nombre de colonnes à retourner.</span><span class="sxs-lookup"><span data-stu-id="999c8-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="999c8-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="999c8-347">CCategorizationSet</span></span>           | <span data-ttu-id="999c8-348">Contient des informations sur le regroupement d’un ensemble de résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="999c8-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-349">CCategorizationSpec</span></span>          | <span data-ttu-id="999c8-350">Contient une définition des catégories dans lesquelles les résultats de la requête seront catégorisés.</span><span class="sxs-lookup"><span data-stu-id="999c8-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="999c8-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="999c8-351">CDbColId</span></span>                     | <span data-ttu-id="999c8-352">Contient une colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="999c8-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="999c8-353">CDbProp</span></span>                      | <span data-ttu-id="999c8-354">Contient une propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="999c8-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="999c8-355">CDbPropSet</span></span>                   | <span data-ttu-id="999c8-356">Contient un ensemble de propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="999c8-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="999c8-357">CPidMapper</span></span>                   | <span data-ttu-id="999c8-358">Contient un tableau d’ID de propriété spécifiant les propriétés à retourner dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="999c8-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="999c8-359">CRowSeekAt</span></span>                   | <span data-ttu-id="999c8-360">Contient le décalage à partir duquel récupérer des lignes dans un message CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="999c8-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="999c8-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="999c8-362">Identifie le point à partir duquel commencer la récupération d’un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="999c8-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="999c8-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="999c8-364">Identifie les signets à partir desquels récupérer des lignes pour un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="999c8-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="999c8-365">CRowSeekNext</span></span>                 | <span data-ttu-id="999c8-366">Contient le nombre de lignes à ignorer dans un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="999c8-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="999c8-367">CRowsetProperties</span></span>            | <span data-ttu-id="999c8-368">Contient les informations de configuration d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="999c8-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="999c8-369">CSortSet</span></span>                     | <span data-ttu-id="999c8-370">Contient l’ordre de tri d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="999c8-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="999c8-371">CTableColumn</span></span>                 | <span data-ttu-id="999c8-372">Contient une colonne pour le message CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="999c8-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="999c8-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="999c8-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="999c8-374">Contient une valeur sérialisée.</span><span class="sxs-lookup"><span data-stu-id="999c8-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="999c8-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="999c8-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="999c8-376">La structure CBaseStorageVariant contient la valeur sur laquelle effectuer une opération de correspondance pour une propriété spécifiée dans la structure CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="999c8-377">0</span><span class="sxs-lookup"><span data-stu-id="999c8-377">0</span></span>

<span data-ttu-id="999c8-378">1</span><span class="sxs-lookup"><span data-stu-id="999c8-378">1</span></span>

<span data-ttu-id="999c8-379">2</span><span class="sxs-lookup"><span data-stu-id="999c8-379">2</span></span>

<span data-ttu-id="999c8-380">3</span><span class="sxs-lookup"><span data-stu-id="999c8-380">3</span></span>

<span data-ttu-id="999c8-381">4</span><span class="sxs-lookup"><span data-stu-id="999c8-381">4</span></span>

<span data-ttu-id="999c8-382">5</span><span class="sxs-lookup"><span data-stu-id="999c8-382">5</span></span>

<span data-ttu-id="999c8-383">6</span><span class="sxs-lookup"><span data-stu-id="999c8-383">6</span></span>

<span data-ttu-id="999c8-384">7</span><span class="sxs-lookup"><span data-stu-id="999c8-384">7</span></span>

<span data-ttu-id="999c8-385">8</span><span class="sxs-lookup"><span data-stu-id="999c8-385">8</span></span>

<span data-ttu-id="999c8-386">9</span><span class="sxs-lookup"><span data-stu-id="999c8-386">9</span></span>

<span data-ttu-id="999c8-387">1</span><span class="sxs-lookup"><span data-stu-id="999c8-387">1</span></span><br/> <span data-ttu-id="999c8-388">0</span><span class="sxs-lookup"><span data-stu-id="999c8-388">0</span></span><br/>

<span data-ttu-id="999c8-389">1</span><span class="sxs-lookup"><span data-stu-id="999c8-389">1</span></span>

<span data-ttu-id="999c8-390">2</span><span class="sxs-lookup"><span data-stu-id="999c8-390">2</span></span>

<span data-ttu-id="999c8-391">3</span><span class="sxs-lookup"><span data-stu-id="999c8-391">3</span></span>

<span data-ttu-id="999c8-392">4</span><span class="sxs-lookup"><span data-stu-id="999c8-392">4</span></span>

<span data-ttu-id="999c8-393">5</span><span class="sxs-lookup"><span data-stu-id="999c8-393">5</span></span>

<span data-ttu-id="999c8-394">6</span><span class="sxs-lookup"><span data-stu-id="999c8-394">6</span></span>

<span data-ttu-id="999c8-395">7</span><span class="sxs-lookup"><span data-stu-id="999c8-395">7</span></span>

<span data-ttu-id="999c8-396">8</span><span class="sxs-lookup"><span data-stu-id="999c8-396">8</span></span>

<span data-ttu-id="999c8-397">9</span><span class="sxs-lookup"><span data-stu-id="999c8-397">9</span></span>

<span data-ttu-id="999c8-398">2</span><span class="sxs-lookup"><span data-stu-id="999c8-398">2</span></span><br/> <span data-ttu-id="999c8-399">0</span><span class="sxs-lookup"><span data-stu-id="999c8-399">0</span></span><br/>

<span data-ttu-id="999c8-400">1</span><span class="sxs-lookup"><span data-stu-id="999c8-400">1</span></span>

<span data-ttu-id="999c8-401">2</span><span class="sxs-lookup"><span data-stu-id="999c8-401">2</span></span>

<span data-ttu-id="999c8-402">3</span><span class="sxs-lookup"><span data-stu-id="999c8-402">3</span></span>

<span data-ttu-id="999c8-403">4</span><span class="sxs-lookup"><span data-stu-id="999c8-403">4</span></span>

<span data-ttu-id="999c8-404">5</span><span class="sxs-lookup"><span data-stu-id="999c8-404">5</span></span>

<span data-ttu-id="999c8-405">6</span><span class="sxs-lookup"><span data-stu-id="999c8-405">6</span></span>

<span data-ttu-id="999c8-406">7</span><span class="sxs-lookup"><span data-stu-id="999c8-406">7</span></span>

<span data-ttu-id="999c8-407">8</span><span class="sxs-lookup"><span data-stu-id="999c8-407">8</span></span>

<span data-ttu-id="999c8-408">9</span><span class="sxs-lookup"><span data-stu-id="999c8-408">9</span></span>

<span data-ttu-id="999c8-409">3</span><span class="sxs-lookup"><span data-stu-id="999c8-409">3</span></span><br/> <span data-ttu-id="999c8-410">0</span><span class="sxs-lookup"><span data-stu-id="999c8-410">0</span></span><br/>

<span data-ttu-id="999c8-411">1</span><span class="sxs-lookup"><span data-stu-id="999c8-411">1</span></span>

<span data-ttu-id="999c8-412">vType</span><span class="sxs-lookup"><span data-stu-id="999c8-412">vType</span></span>

<span data-ttu-id="999c8-413">vData1</span><span class="sxs-lookup"><span data-stu-id="999c8-413">vData1</span></span>

<span data-ttu-id="999c8-414">vData2</span><span class="sxs-lookup"><span data-stu-id="999c8-414">vData2</span></span>

<span data-ttu-id="999c8-415">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-415">vValue (variable)</span></span>



 

<span data-ttu-id="999c8-416">**vType**: indicateur de type indiquant le type de vValue.</span><span class="sxs-lookup"><span data-stu-id="999c8-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="999c8-417">Il doit s’agir de l’une des valeurs VARENUM spécifiées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="999c8-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="999c8-418">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-418">Value</span></span>                 | <span data-ttu-id="999c8-419">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-420">VT \_ vide (0x0000)</span><span class="sxs-lookup"><span data-stu-id="999c8-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="999c8-421">vValue n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="999c8-422">VT \_ null (0x0001)</span><span class="sxs-lookup"><span data-stu-id="999c8-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="999c8-423">vValue n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="999c8-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="999c8-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="999c8-425">Entier signé sur 1 octet.</span><span class="sxs-lookup"><span data-stu-id="999c8-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="999c8-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="999c8-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="999c8-427">Entier non signé sur 1 octet.</span><span class="sxs-lookup"><span data-stu-id="999c8-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="999c8-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="999c8-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="999c8-429">Entier signé sur 2 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="999c8-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="999c8-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="999c8-431">Entier non signé sur 2 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="999c8-432">VT \_ bool (0x000B)</span><span class="sxs-lookup"><span data-stu-id="999c8-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="999c8-433">Valeur booléenne ; entier sur 2 octets qui contient 0x0000 (FALSe) ou 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="999c8-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="999c8-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="999c8-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="999c8-435">Entier signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="999c8-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="999c8-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="999c8-437">Entier non signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="999c8-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="999c8-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="999c8-439">Nombre à virgule flottante IEEE 32 bits, tel que défini dans \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="999c8-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="999c8-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="999c8-441">Entier signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="999c8-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="999c8-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="999c8-443">Entier non signé sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="999c8-444">\_Erreur VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="999c8-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="999c8-445">Entier non signé de 4 octets contenant un HRESULT, tel que spécifié dans \[ ms-sys \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="999c8-446">0x0014 VT (en anglais \_ )</span><span class="sxs-lookup"><span data-stu-id="999c8-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="999c8-447">Entier signé de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="999c8-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="999c8-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="999c8-449">Entier non signé sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="999c8-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="999c8-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="999c8-451">Nombre à virgule flottante IEEE 64 bits tel que défini dans \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="999c8-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="999c8-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="999c8-453">Entier de complément à deux octets (mis à l’échelle par 10 000).</span><span class="sxs-lookup"><span data-stu-id="999c8-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="999c8-454">\_Date VT (0x0007)</span><span class="sxs-lookup"><span data-stu-id="999c8-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="999c8-455">Nombre à virgule flottante 64 bits représentant le nombre de jours écoulés depuis 00:00:00 le 31 décembre 1899 (temps universel coordonné).</span><span class="sxs-lookup"><span data-stu-id="999c8-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="999c8-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="999c8-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="999c8-457">Entier 64 bits représentant le nombre d’intervalles de 100 nanosecondes depuis 00:00:00 le 1er janvier 1601 (heure universelle coordonnée).</span><span class="sxs-lookup"><span data-stu-id="999c8-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="999c8-458">VT \_ décimale (0x000E)</span><span class="sxs-lookup"><span data-stu-id="999c8-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="999c8-459">Structure DÉCIMALe telle que spécifiée dans la section 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="999c8-460">\_CLSID VT (0x0048)</span><span class="sxs-lookup"><span data-stu-id="999c8-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="999c8-461">Valeur binaire de 16 octets contenant un GUID.</span><span class="sxs-lookup"><span data-stu-id="999c8-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="999c8-462">\_Objet BLOB VT (0x0041)</span><span class="sxs-lookup"><span data-stu-id="999c8-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="999c8-463">Nombre entier non signé de 4 octets d’octets dans l’objet BLOB, suivi de beaucoup d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="999c8-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="999c8-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="999c8-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="999c8-465">Nombre entier d’octets non signés sur 4 octets dans la chaîne, suivi d’une chaîne, comme indiqué ci-dessous sous vValue.</span><span class="sxs-lookup"><span data-stu-id="999c8-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="999c8-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="999c8-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="999c8-467">Chaîne ANSI terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="999c8-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="999c8-468">VT \_ LPWStr (0x001F)</span><span class="sxs-lookup"><span data-stu-id="999c8-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="999c8-469">Chaîne Unicode Unicode terminée par le caractère null \[ \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="999c8-470">\_Variante VT (0x000c)</span><span class="sxs-lookup"><span data-stu-id="999c8-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="999c8-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="999c8-471">CBaseStorageVariant.</span></span> <span data-ttu-id="999c8-472">DOIT être combiné avec un modificateur de type de \_ tableau VT ou de \_ vecteur VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="999c8-473">Le tableau suivant spécifie les modificateurs de type pour vType.</span><span class="sxs-lookup"><span data-stu-id="999c8-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="999c8-474">Les modificateurs de type peuvent être binaires avec vType, pour modifier la signification de vValue afin d’indiquer qu’il s’agit de l’un des deux types de tableau possibles.</span><span class="sxs-lookup"><span data-stu-id="999c8-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="999c8-475">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-475">Value</span></span>               | <span data-ttu-id="999c8-476">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-477">\_Vecteur VT (0x1000)</span><span class="sxs-lookup"><span data-stu-id="999c8-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="999c8-478">Si l’indicateur de type est combiné avec \_ un vecteur VT à l’aide d’un opérateur or, vValue est un tableau compté des valeurs du type indiqué.</span><span class="sxs-lookup"><span data-stu-id="999c8-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="999c8-479">Pour plus d’informations, consultez la section 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="999c8-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="999c8-480">Ce modificateur de type ne doit pas être combiné avec les types suivants : VT \_ int, VT \_ uint, VT \_ Decimal, VT \_ BLOB \_ , \_ objet BLOB VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="999c8-481">\_Tableau VT (0x2000)</span><span class="sxs-lookup"><span data-stu-id="999c8-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="999c8-482">Si l’indicateur de type est combiné avec \_ un tableau VT par un opérateur or, la valeur est un SafeArray (comme spécifié dans la section 2.2.1.1.1.3) qui contient les valeurs du type indiqué.</span><span class="sxs-lookup"><span data-stu-id="999c8-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="999c8-483">Ce modificateur de type ne doit pas être combiné avec les types suivants : VT \_ I8, VT \_ UI8, VT \_ fileTime, VT \_ CLSID, \_ objet BLOB VT, \_ objet BLOB VT \_ , VT \_ LPSTR, VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="999c8-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="999c8-484">**vData1**: lorsque vType est de type VT \_ Decimal, la valeur de ce champ est spécifiée en tant que champ Scale dans la section 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="999c8-485">Pour tous les autres vTypes, la valeur doit être égale à 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="999c8-486">**vData2**: lorsque vType est de type VT \_ Decimal, la valeur de ce champ est spécifiée comme champ de signe dans la section 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="999c8-487">Pour tous les autres vTypes, la valeur doit être égale à 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="999c8-488">**vValue**: valeur de l’opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="999c8-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="999c8-489">La syntaxe doit être indiquée dans le champ vType.</span><span class="sxs-lookup"><span data-stu-id="999c8-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="999c8-490">Le tableau suivant récapitule les tailles du champ vValue, selon le champ vType pour les types de données de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="999c8-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="999c8-491">La taille est en octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-491">The size is in bytes.</span></span>



| <span data-ttu-id="999c8-492">vType</span><span class="sxs-lookup"><span data-stu-id="999c8-492">vType</span></span>                                                   | <span data-ttu-id="999c8-493">Taille</span><span class="sxs-lookup"><span data-stu-id="999c8-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="999c8-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="999c8-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="999c8-495">1</span><span class="sxs-lookup"><span data-stu-id="999c8-495">1</span></span>    |
| <span data-ttu-id="999c8-496">VT \_ I2, VT \_ UI2, VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="999c8-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="999c8-497">2</span><span class="sxs-lookup"><span data-stu-id="999c8-497">2</span></span>    |
| <span data-ttu-id="999c8-498">VT \_ i4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, \_ erreur VT</span><span class="sxs-lookup"><span data-stu-id="999c8-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="999c8-499">4</span><span class="sxs-lookup"><span data-stu-id="999c8-499">4</span></span>    |
| <span data-ttu-id="999c8-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ ca, VT \_ date, VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="999c8-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="999c8-501">8</span><span class="sxs-lookup"><span data-stu-id="999c8-501">8</span></span>    |
| <span data-ttu-id="999c8-502">VT \_ décimal, \_ CLSID VT</span><span class="sxs-lookup"><span data-stu-id="999c8-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="999c8-503">16</span><span class="sxs-lookup"><span data-stu-id="999c8-503">16</span></span>   |



 

<span data-ttu-id="999c8-504">Si vType a \_ la valeur BLOB VT, VT \_ BSTR ou VT \_ LPSTR, la structure de vValue est spécifiée dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="999c8-505">0</span><span class="sxs-lookup"><span data-stu-id="999c8-505">0</span></span>

<span data-ttu-id="999c8-506">1</span><span class="sxs-lookup"><span data-stu-id="999c8-506">1</span></span>

<span data-ttu-id="999c8-507">2</span><span class="sxs-lookup"><span data-stu-id="999c8-507">2</span></span>

<span data-ttu-id="999c8-508">3</span><span class="sxs-lookup"><span data-stu-id="999c8-508">3</span></span>

<span data-ttu-id="999c8-509">4</span><span class="sxs-lookup"><span data-stu-id="999c8-509">4</span></span>

<span data-ttu-id="999c8-510">5</span><span class="sxs-lookup"><span data-stu-id="999c8-510">5</span></span>

<span data-ttu-id="999c8-511">6</span><span class="sxs-lookup"><span data-stu-id="999c8-511">6</span></span>

<span data-ttu-id="999c8-512">7</span><span class="sxs-lookup"><span data-stu-id="999c8-512">7</span></span>

<span data-ttu-id="999c8-513">8</span><span class="sxs-lookup"><span data-stu-id="999c8-513">8</span></span>

<span data-ttu-id="999c8-514">9</span><span class="sxs-lookup"><span data-stu-id="999c8-514">9</span></span>

<span data-ttu-id="999c8-515">1</span><span class="sxs-lookup"><span data-stu-id="999c8-515">1</span></span><br/> <span data-ttu-id="999c8-516">0</span><span class="sxs-lookup"><span data-stu-id="999c8-516">0</span></span><br/>

<span data-ttu-id="999c8-517">1</span><span class="sxs-lookup"><span data-stu-id="999c8-517">1</span></span>

<span data-ttu-id="999c8-518">2</span><span class="sxs-lookup"><span data-stu-id="999c8-518">2</span></span>

<span data-ttu-id="999c8-519">3</span><span class="sxs-lookup"><span data-stu-id="999c8-519">3</span></span>

<span data-ttu-id="999c8-520">4</span><span class="sxs-lookup"><span data-stu-id="999c8-520">4</span></span>

<span data-ttu-id="999c8-521">5</span><span class="sxs-lookup"><span data-stu-id="999c8-521">5</span></span>

<span data-ttu-id="999c8-522">6</span><span class="sxs-lookup"><span data-stu-id="999c8-522">6</span></span>

<span data-ttu-id="999c8-523">7</span><span class="sxs-lookup"><span data-stu-id="999c8-523">7</span></span>

<span data-ttu-id="999c8-524">8</span><span class="sxs-lookup"><span data-stu-id="999c8-524">8</span></span>

<span data-ttu-id="999c8-525">9</span><span class="sxs-lookup"><span data-stu-id="999c8-525">9</span></span>

<span data-ttu-id="999c8-526">2</span><span class="sxs-lookup"><span data-stu-id="999c8-526">2</span></span><br/> <span data-ttu-id="999c8-527">0</span><span class="sxs-lookup"><span data-stu-id="999c8-527">0</span></span><br/>

<span data-ttu-id="999c8-528">1</span><span class="sxs-lookup"><span data-stu-id="999c8-528">1</span></span>

<span data-ttu-id="999c8-529">2</span><span class="sxs-lookup"><span data-stu-id="999c8-529">2</span></span>

<span data-ttu-id="999c8-530">3</span><span class="sxs-lookup"><span data-stu-id="999c8-530">3</span></span>

<span data-ttu-id="999c8-531">4</span><span class="sxs-lookup"><span data-stu-id="999c8-531">4</span></span>

<span data-ttu-id="999c8-532">5</span><span class="sxs-lookup"><span data-stu-id="999c8-532">5</span></span>

<span data-ttu-id="999c8-533">6</span><span class="sxs-lookup"><span data-stu-id="999c8-533">6</span></span>

<span data-ttu-id="999c8-534">7</span><span class="sxs-lookup"><span data-stu-id="999c8-534">7</span></span>

<span data-ttu-id="999c8-535">8</span><span class="sxs-lookup"><span data-stu-id="999c8-535">8</span></span>

<span data-ttu-id="999c8-536">9</span><span class="sxs-lookup"><span data-stu-id="999c8-536">9</span></span>

<span data-ttu-id="999c8-537">3</span><span class="sxs-lookup"><span data-stu-id="999c8-537">3</span></span><br/> <span data-ttu-id="999c8-538">0</span><span class="sxs-lookup"><span data-stu-id="999c8-538">0</span></span><br/>

<span data-ttu-id="999c8-539">1</span><span class="sxs-lookup"><span data-stu-id="999c8-539">1</span></span>

<span data-ttu-id="999c8-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="999c8-540">cbSize</span></span>

<span data-ttu-id="999c8-541">blobData (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="999c8-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="999c8-542">**cbSize**: entier 32 bits non signé, indiquant la taille du champ blobData en octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="999c8-543">Si vType est défini sur VT \_ BSTR ou VT \_ LPSTR, cbSize doit avoir la valeur 0x00000000 lorsque la chaîne représentée est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="999c8-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="999c8-544">**blobData**: doit avoir une longueur de cbSize en octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="999c8-545">Pour vType ayant la valeur d' \_ objet BLOB VT, ce champ est opaque Binary BLOB Data.</span><span class="sxs-lookup"><span data-stu-id="999c8-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="999c8-546">Pour vType défini sur VT \_ BSTR, ce champ est un jeu de caractères dans un jeu de caractères OEM sélectionné.</span><span class="sxs-lookup"><span data-stu-id="999c8-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="999c8-547">Le client et le serveur doivent être configurés pour avoir des jeux de caractères interopérables (hors bande du protocole).</span><span class="sxs-lookup"><span data-stu-id="999c8-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="999c8-548">Il n’est pas nécessaire qu’elle se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="999c8-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="999c8-549">Pour vType défini sur VT \_ LPSTR, ce champ est une chaîne de caractères se terminant par un caractère NULL dans un jeu de caractères OEM sélectionné.</span><span class="sxs-lookup"><span data-stu-id="999c8-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="999c8-550">Le client et le serveur doivent être configurés pour avoir des jeux de caractères interopérables (hors bande du protocole).</span><span class="sxs-lookup"><span data-stu-id="999c8-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="999c8-551">Si vType est défini sur VT \_ LPWStr, la structure de vValue est spécifiée dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="999c8-552">0</span><span class="sxs-lookup"><span data-stu-id="999c8-552">0</span></span>

<span data-ttu-id="999c8-553">1</span><span class="sxs-lookup"><span data-stu-id="999c8-553">1</span></span>

<span data-ttu-id="999c8-554">2</span><span class="sxs-lookup"><span data-stu-id="999c8-554">2</span></span>

<span data-ttu-id="999c8-555">3</span><span class="sxs-lookup"><span data-stu-id="999c8-555">3</span></span>

<span data-ttu-id="999c8-556">4</span><span class="sxs-lookup"><span data-stu-id="999c8-556">4</span></span>

<span data-ttu-id="999c8-557">5</span><span class="sxs-lookup"><span data-stu-id="999c8-557">5</span></span>

<span data-ttu-id="999c8-558">6</span><span class="sxs-lookup"><span data-stu-id="999c8-558">6</span></span>

<span data-ttu-id="999c8-559">7</span><span class="sxs-lookup"><span data-stu-id="999c8-559">7</span></span>

<span data-ttu-id="999c8-560">8</span><span class="sxs-lookup"><span data-stu-id="999c8-560">8</span></span>

<span data-ttu-id="999c8-561">9</span><span class="sxs-lookup"><span data-stu-id="999c8-561">9</span></span>

<span data-ttu-id="999c8-562">1</span><span class="sxs-lookup"><span data-stu-id="999c8-562">1</span></span><br/> <span data-ttu-id="999c8-563">0</span><span class="sxs-lookup"><span data-stu-id="999c8-563">0</span></span><br/>

<span data-ttu-id="999c8-564">1</span><span class="sxs-lookup"><span data-stu-id="999c8-564">1</span></span>

<span data-ttu-id="999c8-565">2</span><span class="sxs-lookup"><span data-stu-id="999c8-565">2</span></span>

<span data-ttu-id="999c8-566">3</span><span class="sxs-lookup"><span data-stu-id="999c8-566">3</span></span>

<span data-ttu-id="999c8-567">4</span><span class="sxs-lookup"><span data-stu-id="999c8-567">4</span></span>

<span data-ttu-id="999c8-568">5</span><span class="sxs-lookup"><span data-stu-id="999c8-568">5</span></span>

<span data-ttu-id="999c8-569">6</span><span class="sxs-lookup"><span data-stu-id="999c8-569">6</span></span>

<span data-ttu-id="999c8-570">7</span><span class="sxs-lookup"><span data-stu-id="999c8-570">7</span></span>

<span data-ttu-id="999c8-571">8</span><span class="sxs-lookup"><span data-stu-id="999c8-571">8</span></span>

<span data-ttu-id="999c8-572">9</span><span class="sxs-lookup"><span data-stu-id="999c8-572">9</span></span>

<span data-ttu-id="999c8-573">2</span><span class="sxs-lookup"><span data-stu-id="999c8-573">2</span></span><br/> <span data-ttu-id="999c8-574">0</span><span class="sxs-lookup"><span data-stu-id="999c8-574">0</span></span><br/>

<span data-ttu-id="999c8-575">1</span><span class="sxs-lookup"><span data-stu-id="999c8-575">1</span></span>

<span data-ttu-id="999c8-576">2</span><span class="sxs-lookup"><span data-stu-id="999c8-576">2</span></span>

<span data-ttu-id="999c8-577">3</span><span class="sxs-lookup"><span data-stu-id="999c8-577">3</span></span>

<span data-ttu-id="999c8-578">4</span><span class="sxs-lookup"><span data-stu-id="999c8-578">4</span></span>

<span data-ttu-id="999c8-579">5</span><span class="sxs-lookup"><span data-stu-id="999c8-579">5</span></span>

<span data-ttu-id="999c8-580">6</span><span class="sxs-lookup"><span data-stu-id="999c8-580">6</span></span>

<span data-ttu-id="999c8-581">7</span><span class="sxs-lookup"><span data-stu-id="999c8-581">7</span></span>

<span data-ttu-id="999c8-582">8</span><span class="sxs-lookup"><span data-stu-id="999c8-582">8</span></span>

<span data-ttu-id="999c8-583">9</span><span class="sxs-lookup"><span data-stu-id="999c8-583">9</span></span>

<span data-ttu-id="999c8-584">3</span><span class="sxs-lookup"><span data-stu-id="999c8-584">3</span></span><br/> <span data-ttu-id="999c8-585">0</span><span class="sxs-lookup"><span data-stu-id="999c8-585">0</span></span><br/>

<span data-ttu-id="999c8-586">1</span><span class="sxs-lookup"><span data-stu-id="999c8-586">1</span></span>

<span data-ttu-id="999c8-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="999c8-587">ccLen</span></span>

<span data-ttu-id="999c8-588">String (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="999c8-588">string (variable, optional)</span></span>



 

<span data-ttu-id="999c8-589">**ccLen**: entier non signé 32 bits, indiquant la taille du champ de chaîne en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="999c8-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="999c8-590">DOIT être défini sur 0x00000000 pour une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="999c8-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="999c8-591">**chaîne**: chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="999c8-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="999c8-592">Structures 2.2.1.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="999c8-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="999c8-593">Les structures suivantes sont utilisées dans la structure CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="999c8-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="999c8-594">2.2.1.1.1.1 DÉCIMAL</span><span class="sxs-lookup"><span data-stu-id="999c8-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="999c8-595">Le nombre décimal est utilisé pour représenter une valeur numérique exacte avec une précision fixe et une échelle fixe.</span><span class="sxs-lookup"><span data-stu-id="999c8-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="999c8-596">Quand vType est défini sur VT \_ Decimal (0x0000E), les champs vData1 et vData2 de CBASESTORAGEVARIANT doivent être interprétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="999c8-597">**vData1**: nombre de chiffres à droite de la virgule décimale.</span><span class="sxs-lookup"><span data-stu-id="999c8-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="999c8-598">DOIT être compris entre 0 et 28.</span><span class="sxs-lookup"><span data-stu-id="999c8-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="999c8-599">**vData2**: signe de la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="999c8-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="999c8-600">Défini sur 0x00 si positif, 0x80 si négatif.</span><span class="sxs-lookup"><span data-stu-id="999c8-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="999c8-601">Le format du champ vValue est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-601">The format of the vValue field is:</span></span>



<span data-ttu-id="999c8-602">0</span><span class="sxs-lookup"><span data-stu-id="999c8-602">0</span></span>

<span data-ttu-id="999c8-603">1</span><span class="sxs-lookup"><span data-stu-id="999c8-603">1</span></span>

<span data-ttu-id="999c8-604">2</span><span class="sxs-lookup"><span data-stu-id="999c8-604">2</span></span>

<span data-ttu-id="999c8-605">3</span><span class="sxs-lookup"><span data-stu-id="999c8-605">3</span></span>

<span data-ttu-id="999c8-606">4</span><span class="sxs-lookup"><span data-stu-id="999c8-606">4</span></span>

<span data-ttu-id="999c8-607">5</span><span class="sxs-lookup"><span data-stu-id="999c8-607">5</span></span>

<span data-ttu-id="999c8-608">6</span><span class="sxs-lookup"><span data-stu-id="999c8-608">6</span></span>

<span data-ttu-id="999c8-609">7</span><span class="sxs-lookup"><span data-stu-id="999c8-609">7</span></span>

<span data-ttu-id="999c8-610">8</span><span class="sxs-lookup"><span data-stu-id="999c8-610">8</span></span>

<span data-ttu-id="999c8-611">9</span><span class="sxs-lookup"><span data-stu-id="999c8-611">9</span></span>

<span data-ttu-id="999c8-612">1</span><span class="sxs-lookup"><span data-stu-id="999c8-612">1</span></span><br/> <span data-ttu-id="999c8-613">0</span><span class="sxs-lookup"><span data-stu-id="999c8-613">0</span></span><br/>

<span data-ttu-id="999c8-614">1</span><span class="sxs-lookup"><span data-stu-id="999c8-614">1</span></span>

<span data-ttu-id="999c8-615">2</span><span class="sxs-lookup"><span data-stu-id="999c8-615">2</span></span>

<span data-ttu-id="999c8-616">3</span><span class="sxs-lookup"><span data-stu-id="999c8-616">3</span></span>

<span data-ttu-id="999c8-617">4</span><span class="sxs-lookup"><span data-stu-id="999c8-617">4</span></span>

<span data-ttu-id="999c8-618">5</span><span class="sxs-lookup"><span data-stu-id="999c8-618">5</span></span>

<span data-ttu-id="999c8-619">6</span><span class="sxs-lookup"><span data-stu-id="999c8-619">6</span></span>

<span data-ttu-id="999c8-620">7</span><span class="sxs-lookup"><span data-stu-id="999c8-620">7</span></span>

<span data-ttu-id="999c8-621">8</span><span class="sxs-lookup"><span data-stu-id="999c8-621">8</span></span>

<span data-ttu-id="999c8-622">9</span><span class="sxs-lookup"><span data-stu-id="999c8-622">9</span></span>

<span data-ttu-id="999c8-623">2</span><span class="sxs-lookup"><span data-stu-id="999c8-623">2</span></span><br/> <span data-ttu-id="999c8-624">0</span><span class="sxs-lookup"><span data-stu-id="999c8-624">0</span></span><br/>

<span data-ttu-id="999c8-625">1</span><span class="sxs-lookup"><span data-stu-id="999c8-625">1</span></span>

<span data-ttu-id="999c8-626">2</span><span class="sxs-lookup"><span data-stu-id="999c8-626">2</span></span>

<span data-ttu-id="999c8-627">3</span><span class="sxs-lookup"><span data-stu-id="999c8-627">3</span></span>

<span data-ttu-id="999c8-628">4</span><span class="sxs-lookup"><span data-stu-id="999c8-628">4</span></span>

<span data-ttu-id="999c8-629">5</span><span class="sxs-lookup"><span data-stu-id="999c8-629">5</span></span>

<span data-ttu-id="999c8-630">6</span><span class="sxs-lookup"><span data-stu-id="999c8-630">6</span></span>

<span data-ttu-id="999c8-631">7</span><span class="sxs-lookup"><span data-stu-id="999c8-631">7</span></span>

<span data-ttu-id="999c8-632">8</span><span class="sxs-lookup"><span data-stu-id="999c8-632">8</span></span>

<span data-ttu-id="999c8-633">9</span><span class="sxs-lookup"><span data-stu-id="999c8-633">9</span></span>

<span data-ttu-id="999c8-634">3</span><span class="sxs-lookup"><span data-stu-id="999c8-634">3</span></span><br/> <span data-ttu-id="999c8-635">0</span><span class="sxs-lookup"><span data-stu-id="999c8-635">0</span></span><br/>

<span data-ttu-id="999c8-636">1</span><span class="sxs-lookup"><span data-stu-id="999c8-636">1</span></span>

<span data-ttu-id="999c8-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="999c8-637">Hi32</span></span>

<span data-ttu-id="999c8-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="999c8-638">Lo32</span></span>

<span data-ttu-id="999c8-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="999c8-639">Mid32</span></span>



 

<span data-ttu-id="999c8-640">**Hi32**: 32 bits les plus élevés de l’entier 96 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="999c8-641">**Lo32**: 32 bits de poids faible de l’entier 96 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="999c8-642">**Mid32**: bits 32 au milieu de l’entier 96 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="999c8-643">vecteur VT 2.2.1.1.1.2 \_</span><span class="sxs-lookup"><span data-stu-id="999c8-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="999c8-644">Le \_ vecteur VT est utilisé pour passer des tableaux unidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="999c8-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="999c8-645">0</span><span class="sxs-lookup"><span data-stu-id="999c8-645">0</span></span>

<span data-ttu-id="999c8-646">1</span><span class="sxs-lookup"><span data-stu-id="999c8-646">1</span></span>

<span data-ttu-id="999c8-647">2</span><span class="sxs-lookup"><span data-stu-id="999c8-647">2</span></span>

<span data-ttu-id="999c8-648">3</span><span class="sxs-lookup"><span data-stu-id="999c8-648">3</span></span>

<span data-ttu-id="999c8-649">4</span><span class="sxs-lookup"><span data-stu-id="999c8-649">4</span></span>

<span data-ttu-id="999c8-650">5</span><span class="sxs-lookup"><span data-stu-id="999c8-650">5</span></span>

<span data-ttu-id="999c8-651">6</span><span class="sxs-lookup"><span data-stu-id="999c8-651">6</span></span>

<span data-ttu-id="999c8-652">7</span><span class="sxs-lookup"><span data-stu-id="999c8-652">7</span></span>

<span data-ttu-id="999c8-653">8</span><span class="sxs-lookup"><span data-stu-id="999c8-653">8</span></span>

<span data-ttu-id="999c8-654">9</span><span class="sxs-lookup"><span data-stu-id="999c8-654">9</span></span>

<span data-ttu-id="999c8-655">1</span><span class="sxs-lookup"><span data-stu-id="999c8-655">1</span></span><br/> <span data-ttu-id="999c8-656">0</span><span class="sxs-lookup"><span data-stu-id="999c8-656">0</span></span><br/>

<span data-ttu-id="999c8-657">1</span><span class="sxs-lookup"><span data-stu-id="999c8-657">1</span></span>

<span data-ttu-id="999c8-658">2</span><span class="sxs-lookup"><span data-stu-id="999c8-658">2</span></span>

<span data-ttu-id="999c8-659">3</span><span class="sxs-lookup"><span data-stu-id="999c8-659">3</span></span>

<span data-ttu-id="999c8-660">4</span><span class="sxs-lookup"><span data-stu-id="999c8-660">4</span></span>

<span data-ttu-id="999c8-661">5</span><span class="sxs-lookup"><span data-stu-id="999c8-661">5</span></span>

<span data-ttu-id="999c8-662">6</span><span class="sxs-lookup"><span data-stu-id="999c8-662">6</span></span>

<span data-ttu-id="999c8-663">7</span><span class="sxs-lookup"><span data-stu-id="999c8-663">7</span></span>

<span data-ttu-id="999c8-664">8</span><span class="sxs-lookup"><span data-stu-id="999c8-664">8</span></span>

<span data-ttu-id="999c8-665">9</span><span class="sxs-lookup"><span data-stu-id="999c8-665">9</span></span>

<span data-ttu-id="999c8-666">2</span><span class="sxs-lookup"><span data-stu-id="999c8-666">2</span></span><br/> <span data-ttu-id="999c8-667">0</span><span class="sxs-lookup"><span data-stu-id="999c8-667">0</span></span><br/>

<span data-ttu-id="999c8-668">1</span><span class="sxs-lookup"><span data-stu-id="999c8-668">1</span></span>

<span data-ttu-id="999c8-669">2</span><span class="sxs-lookup"><span data-stu-id="999c8-669">2</span></span>

<span data-ttu-id="999c8-670">3</span><span class="sxs-lookup"><span data-stu-id="999c8-670">3</span></span>

<span data-ttu-id="999c8-671">4</span><span class="sxs-lookup"><span data-stu-id="999c8-671">4</span></span>

<span data-ttu-id="999c8-672">5</span><span class="sxs-lookup"><span data-stu-id="999c8-672">5</span></span>

<span data-ttu-id="999c8-673">6</span><span class="sxs-lookup"><span data-stu-id="999c8-673">6</span></span>

<span data-ttu-id="999c8-674">7</span><span class="sxs-lookup"><span data-stu-id="999c8-674">7</span></span>

<span data-ttu-id="999c8-675">8</span><span class="sxs-lookup"><span data-stu-id="999c8-675">8</span></span>

<span data-ttu-id="999c8-676">9</span><span class="sxs-lookup"><span data-stu-id="999c8-676">9</span></span>

<span data-ttu-id="999c8-677">3</span><span class="sxs-lookup"><span data-stu-id="999c8-677">3</span></span><br/> <span data-ttu-id="999c8-678">0</span><span class="sxs-lookup"><span data-stu-id="999c8-678">0</span></span><br/>

<span data-ttu-id="999c8-679">1</span><span class="sxs-lookup"><span data-stu-id="999c8-679">1</span></span>

<span data-ttu-id="999c8-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="999c8-680">vVectorElements</span></span>

<span data-ttu-id="999c8-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="999c8-681">vVectorData</span></span>



 

<span data-ttu-id="999c8-682">**vVectorElements**: entier non signé 32 bits, indiquant le nombre d’éléments contenus dans le champ vVectorData.</span><span class="sxs-lookup"><span data-stu-id="999c8-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="999c8-683">**vVectorData**: tableau d’éléments qui ont un type indiqué par vType avec le bit 0x1000 effacé.</span><span class="sxs-lookup"><span data-stu-id="999c8-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="999c8-684">La taille d’un élément de longueur fixe individuel peut être obtenue à partir de la table de type de données de longueur fixe, comme indiqué dans la section 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="999c8-685">La longueur de ce champ, en octets, peut être calculée en multipliant vVectorElements par la taille d’un élément individuel.</span><span class="sxs-lookup"><span data-stu-id="999c8-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="999c8-686">Pour les types de données de longueur variable, vVectorData contient une séquence de types simples marshalés consécutivement, où le type est indiqué par vType avec le bit 0x1000 effacé.</span><span class="sxs-lookup"><span data-stu-id="999c8-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="999c8-687">Cela comprend un cas spécial indiqué par la \_ variante VT du tableau VTYPE VT \| \_ (c’est-à-dire, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="999c8-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="999c8-688">Les éléments du champ vVectorData doivent être séparés par 0 à 3 octets de remplissage, de sorte que chaque élément commence à un offset qui est un multiple de 4 octets à partir du début du message qui contient ce tableau.</span><span class="sxs-lookup"><span data-stu-id="999c8-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="999c8-689">Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="999c8-690">Le contenu des octets de remplissage doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-691">Pour un vType défini sur une \_ variante VT du tableau VT \| \_ , le type des éléments de cette séquence est CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="999c8-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="999c8-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="999c8-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="999c8-693">SAFEARRAY est utilisé pour passer des tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="999c8-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="999c8-694">La structure contient des informations sur la taille du tableau ainsi que les données du tableau.</span><span class="sxs-lookup"><span data-stu-id="999c8-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="999c8-695">0</span><span class="sxs-lookup"><span data-stu-id="999c8-695">0</span></span>

<span data-ttu-id="999c8-696">1</span><span class="sxs-lookup"><span data-stu-id="999c8-696">1</span></span>

<span data-ttu-id="999c8-697">2</span><span class="sxs-lookup"><span data-stu-id="999c8-697">2</span></span>

<span data-ttu-id="999c8-698">3</span><span class="sxs-lookup"><span data-stu-id="999c8-698">3</span></span>

<span data-ttu-id="999c8-699">4</span><span class="sxs-lookup"><span data-stu-id="999c8-699">4</span></span>

<span data-ttu-id="999c8-700">5</span><span class="sxs-lookup"><span data-stu-id="999c8-700">5</span></span>

<span data-ttu-id="999c8-701">6</span><span class="sxs-lookup"><span data-stu-id="999c8-701">6</span></span>

<span data-ttu-id="999c8-702">7</span><span class="sxs-lookup"><span data-stu-id="999c8-702">7</span></span>

<span data-ttu-id="999c8-703">8</span><span class="sxs-lookup"><span data-stu-id="999c8-703">8</span></span>

<span data-ttu-id="999c8-704">9</span><span class="sxs-lookup"><span data-stu-id="999c8-704">9</span></span>

<span data-ttu-id="999c8-705">1</span><span class="sxs-lookup"><span data-stu-id="999c8-705">1</span></span><br/> <span data-ttu-id="999c8-706">0</span><span class="sxs-lookup"><span data-stu-id="999c8-706">0</span></span><br/>

<span data-ttu-id="999c8-707">1</span><span class="sxs-lookup"><span data-stu-id="999c8-707">1</span></span>

<span data-ttu-id="999c8-708">2</span><span class="sxs-lookup"><span data-stu-id="999c8-708">2</span></span>

<span data-ttu-id="999c8-709">3</span><span class="sxs-lookup"><span data-stu-id="999c8-709">3</span></span>

<span data-ttu-id="999c8-710">4</span><span class="sxs-lookup"><span data-stu-id="999c8-710">4</span></span>

<span data-ttu-id="999c8-711">5</span><span class="sxs-lookup"><span data-stu-id="999c8-711">5</span></span>

<span data-ttu-id="999c8-712">6</span><span class="sxs-lookup"><span data-stu-id="999c8-712">6</span></span>

<span data-ttu-id="999c8-713">7</span><span class="sxs-lookup"><span data-stu-id="999c8-713">7</span></span>

<span data-ttu-id="999c8-714">8</span><span class="sxs-lookup"><span data-stu-id="999c8-714">8</span></span>

<span data-ttu-id="999c8-715">9</span><span class="sxs-lookup"><span data-stu-id="999c8-715">9</span></span>

<span data-ttu-id="999c8-716">2</span><span class="sxs-lookup"><span data-stu-id="999c8-716">2</span></span><br/> <span data-ttu-id="999c8-717">0</span><span class="sxs-lookup"><span data-stu-id="999c8-717">0</span></span><br/>

<span data-ttu-id="999c8-718">1</span><span class="sxs-lookup"><span data-stu-id="999c8-718">1</span></span>

<span data-ttu-id="999c8-719">2</span><span class="sxs-lookup"><span data-stu-id="999c8-719">2</span></span>

<span data-ttu-id="999c8-720">3</span><span class="sxs-lookup"><span data-stu-id="999c8-720">3</span></span>

<span data-ttu-id="999c8-721">4</span><span class="sxs-lookup"><span data-stu-id="999c8-721">4</span></span>

<span data-ttu-id="999c8-722">5</span><span class="sxs-lookup"><span data-stu-id="999c8-722">5</span></span>

<span data-ttu-id="999c8-723">6</span><span class="sxs-lookup"><span data-stu-id="999c8-723">6</span></span>

<span data-ttu-id="999c8-724">7</span><span class="sxs-lookup"><span data-stu-id="999c8-724">7</span></span>

<span data-ttu-id="999c8-725">8</span><span class="sxs-lookup"><span data-stu-id="999c8-725">8</span></span>

<span data-ttu-id="999c8-726">9</span><span class="sxs-lookup"><span data-stu-id="999c8-726">9</span></span>

<span data-ttu-id="999c8-727">3</span><span class="sxs-lookup"><span data-stu-id="999c8-727">3</span></span><br/> <span data-ttu-id="999c8-728">0</span><span class="sxs-lookup"><span data-stu-id="999c8-728">0</span></span><br/>

<span data-ttu-id="999c8-729">1</span><span class="sxs-lookup"><span data-stu-id="999c8-729">1</span></span>

<span data-ttu-id="999c8-730">cDims</span><span class="sxs-lookup"><span data-stu-id="999c8-730">cDims</span></span>

<span data-ttu-id="999c8-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="999c8-731">fFeatures</span></span>

<span data-ttu-id="999c8-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="999c8-732">cbElements</span></span>

<span data-ttu-id="999c8-733">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-733">Rgsabound (variable)</span></span>

<span data-ttu-id="999c8-734">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-734">vData (variable)</span></span>



 

<span data-ttu-id="999c8-735">**cDims**: entier 16 bits non signé indiquant le nombre de dimensions du tableau multidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="999c8-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="999c8-736">**fFeatures**: un champ de bits de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="999c8-737">Les valeurs représentent les fonctionnalités définies par les applications de couche supérieure et doivent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="999c8-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="999c8-738">**cbElements**: entier non signé 32 bits spécifiant la taille de chaque élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="999c8-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="999c8-739">**Rgsabound**: tableau qui contient une structure SAFEARRAYBOUND, comme spécifié dans la section 2.2.1.1.1.4, par dimension dans le SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="999c8-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="999c8-740">Ce tableau a la dimension la plus à gauche et la dimension la plus à droite en dernier.</span><span class="sxs-lookup"><span data-stu-id="999c8-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="999c8-741">**vdata**: vecteur d’éléments marshalés d’un type particulier, indiqué par le VType du CBaseStorageVariant conteneur, avec le bit 0x2000 effacé.</span><span class="sxs-lookup"><span data-stu-id="999c8-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="999c8-742">vData est marshalé de la même façon \_ que le vecteur VT, comme spécifié dans la section 2.2.1.1.1.2, avec la différence selon laquelle le nombre d’éléments n’est pas stocké devant le vecteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="999c8-743">Au lieu de cela, le nombre d’éléments est calculé en multipliant la valeur cElements par toutes les limites de tableau sécurisées indiquées dans le champ Rgsabound.</span><span class="sxs-lookup"><span data-stu-id="999c8-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="999c8-744">Les éléments sont stockés dans un vecteur dans l’ordre des dimensions, en commençant par la dimension la plus à droite.</span><span class="sxs-lookup"><span data-stu-id="999c8-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="999c8-745">Le diagramme suivant représente visuellement un exemple de tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="999c8-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="999c8-746">La première dimension a un cElements égal à 4 (représenté horizontalement) et lLbound égal à 0, et la deuxième dimension a cElements égal à 2 (représenté verticalement) et lLbound égal à 0.</span><span class="sxs-lookup"><span data-stu-id="999c8-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="999c8-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-747">0x00000001</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="999c8-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-748">0x00000002</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="999c8-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-749">0x00000003</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="999c8-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="999c8-750">0x00000005</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="999c8-751">:: Row :::</span><span class="sxs-lookup"><span data-stu-id="999c8-751">::row:::</span></span>
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

<span data-ttu-id="999c8-752">À l’aide du diagramme ci-dessus, vData contient la séquence suivante : 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (en commençant par parcourir la dimension la plus à droite, puis en incrémentant la dimension suivante).</span><span class="sxs-lookup"><span data-stu-id="999c8-752">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="999c8-753">Le Rgsabound précédent (qui enregistre cElements et LBound) est : 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-753">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="999c8-754">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="999c8-754">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="999c8-755">La structure SAFEARRAYBOUND représente les limites d’une dimension d’un SAFEARRAY ou d’un SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="999c8-755">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="999c8-756">Son format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-756">Its format is:</span></span>



<span data-ttu-id="999c8-757">0</span><span class="sxs-lookup"><span data-stu-id="999c8-757">0</span></span>

<span data-ttu-id="999c8-758">1</span><span class="sxs-lookup"><span data-stu-id="999c8-758">1</span></span>

<span data-ttu-id="999c8-759">2</span><span class="sxs-lookup"><span data-stu-id="999c8-759">2</span></span>

<span data-ttu-id="999c8-760">3</span><span class="sxs-lookup"><span data-stu-id="999c8-760">3</span></span>

<span data-ttu-id="999c8-761">4</span><span class="sxs-lookup"><span data-stu-id="999c8-761">4</span></span>

<span data-ttu-id="999c8-762">5</span><span class="sxs-lookup"><span data-stu-id="999c8-762">5</span></span>

<span data-ttu-id="999c8-763">6</span><span class="sxs-lookup"><span data-stu-id="999c8-763">6</span></span>

<span data-ttu-id="999c8-764">7</span><span class="sxs-lookup"><span data-stu-id="999c8-764">7</span></span>

<span data-ttu-id="999c8-765">8</span><span class="sxs-lookup"><span data-stu-id="999c8-765">8</span></span>

<span data-ttu-id="999c8-766">9</span><span class="sxs-lookup"><span data-stu-id="999c8-766">9</span></span>

<span data-ttu-id="999c8-767">1</span><span class="sxs-lookup"><span data-stu-id="999c8-767">1</span></span><br/> <span data-ttu-id="999c8-768">0</span><span class="sxs-lookup"><span data-stu-id="999c8-768">0</span></span><br/>

<span data-ttu-id="999c8-769">1</span><span class="sxs-lookup"><span data-stu-id="999c8-769">1</span></span>

<span data-ttu-id="999c8-770">2</span><span class="sxs-lookup"><span data-stu-id="999c8-770">2</span></span>

<span data-ttu-id="999c8-771">3</span><span class="sxs-lookup"><span data-stu-id="999c8-771">3</span></span>

<span data-ttu-id="999c8-772">4</span><span class="sxs-lookup"><span data-stu-id="999c8-772">4</span></span>

<span data-ttu-id="999c8-773">5</span><span class="sxs-lookup"><span data-stu-id="999c8-773">5</span></span>

<span data-ttu-id="999c8-774">6</span><span class="sxs-lookup"><span data-stu-id="999c8-774">6</span></span>

<span data-ttu-id="999c8-775">7</span><span class="sxs-lookup"><span data-stu-id="999c8-775">7</span></span>

<span data-ttu-id="999c8-776">8</span><span class="sxs-lookup"><span data-stu-id="999c8-776">8</span></span>

<span data-ttu-id="999c8-777">9</span><span class="sxs-lookup"><span data-stu-id="999c8-777">9</span></span>

<span data-ttu-id="999c8-778">2</span><span class="sxs-lookup"><span data-stu-id="999c8-778">2</span></span><br/> <span data-ttu-id="999c8-779">0</span><span class="sxs-lookup"><span data-stu-id="999c8-779">0</span></span><br/>

<span data-ttu-id="999c8-780">1</span><span class="sxs-lookup"><span data-stu-id="999c8-780">1</span></span>

<span data-ttu-id="999c8-781">2</span><span class="sxs-lookup"><span data-stu-id="999c8-781">2</span></span>

<span data-ttu-id="999c8-782">3</span><span class="sxs-lookup"><span data-stu-id="999c8-782">3</span></span>

<span data-ttu-id="999c8-783">4</span><span class="sxs-lookup"><span data-stu-id="999c8-783">4</span></span>

<span data-ttu-id="999c8-784">5</span><span class="sxs-lookup"><span data-stu-id="999c8-784">5</span></span>

<span data-ttu-id="999c8-785">6</span><span class="sxs-lookup"><span data-stu-id="999c8-785">6</span></span>

<span data-ttu-id="999c8-786">7</span><span class="sxs-lookup"><span data-stu-id="999c8-786">7</span></span>

<span data-ttu-id="999c8-787">8</span><span class="sxs-lookup"><span data-stu-id="999c8-787">8</span></span>

<span data-ttu-id="999c8-788">9</span><span class="sxs-lookup"><span data-stu-id="999c8-788">9</span></span>

<span data-ttu-id="999c8-789">3</span><span class="sxs-lookup"><span data-stu-id="999c8-789">3</span></span><br/> <span data-ttu-id="999c8-790">0</span><span class="sxs-lookup"><span data-stu-id="999c8-790">0</span></span><br/>

<span data-ttu-id="999c8-791">1</span><span class="sxs-lookup"><span data-stu-id="999c8-791">1</span></span>

<span data-ttu-id="999c8-792">cElements</span><span class="sxs-lookup"><span data-stu-id="999c8-792">cElements</span></span>

<span data-ttu-id="999c8-793">lLbound</span><span class="sxs-lookup"><span data-stu-id="999c8-793">lLbound</span></span>



 

<span data-ttu-id="999c8-794">**cElements**: entier non signé 32 bits spécifiant le nombre d’éléments dans la dimension.</span><span class="sxs-lookup"><span data-stu-id="999c8-794">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="999c8-795">**lLbound**: entier non signé 32 bits spécifiant la limite inférieure de la dimension.</span><span class="sxs-lookup"><span data-stu-id="999c8-795">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="999c8-796">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="999c8-796">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="999c8-797">SAFEARRAY2 est utilisé pour passer des tableaux multidimensionnels dans SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="999c8-797">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="999c8-798">La structure contient des informations sur les limites ainsi que les données.</span><span class="sxs-lookup"><span data-stu-id="999c8-798">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="999c8-799">0</span><span class="sxs-lookup"><span data-stu-id="999c8-799">0</span></span>

<span data-ttu-id="999c8-800">1</span><span class="sxs-lookup"><span data-stu-id="999c8-800">1</span></span>

<span data-ttu-id="999c8-801">2</span><span class="sxs-lookup"><span data-stu-id="999c8-801">2</span></span>

<span data-ttu-id="999c8-802">3</span><span class="sxs-lookup"><span data-stu-id="999c8-802">3</span></span>

<span data-ttu-id="999c8-803">4</span><span class="sxs-lookup"><span data-stu-id="999c8-803">4</span></span>

<span data-ttu-id="999c8-804">5</span><span class="sxs-lookup"><span data-stu-id="999c8-804">5</span></span>

<span data-ttu-id="999c8-805">6</span><span class="sxs-lookup"><span data-stu-id="999c8-805">6</span></span>

<span data-ttu-id="999c8-806">7</span><span class="sxs-lookup"><span data-stu-id="999c8-806">7</span></span>

<span data-ttu-id="999c8-807">8</span><span class="sxs-lookup"><span data-stu-id="999c8-807">8</span></span>

<span data-ttu-id="999c8-808">9</span><span class="sxs-lookup"><span data-stu-id="999c8-808">9</span></span>

<span data-ttu-id="999c8-809">1</span><span class="sxs-lookup"><span data-stu-id="999c8-809">1</span></span><br/> <span data-ttu-id="999c8-810">0</span><span class="sxs-lookup"><span data-stu-id="999c8-810">0</span></span><br/>

<span data-ttu-id="999c8-811">1</span><span class="sxs-lookup"><span data-stu-id="999c8-811">1</span></span>

<span data-ttu-id="999c8-812">2</span><span class="sxs-lookup"><span data-stu-id="999c8-812">2</span></span>

<span data-ttu-id="999c8-813">3</span><span class="sxs-lookup"><span data-stu-id="999c8-813">3</span></span>

<span data-ttu-id="999c8-814">4</span><span class="sxs-lookup"><span data-stu-id="999c8-814">4</span></span>

<span data-ttu-id="999c8-815">5</span><span class="sxs-lookup"><span data-stu-id="999c8-815">5</span></span>

<span data-ttu-id="999c8-816">6</span><span class="sxs-lookup"><span data-stu-id="999c8-816">6</span></span>

<span data-ttu-id="999c8-817">7</span><span class="sxs-lookup"><span data-stu-id="999c8-817">7</span></span>

<span data-ttu-id="999c8-818">8</span><span class="sxs-lookup"><span data-stu-id="999c8-818">8</span></span>

<span data-ttu-id="999c8-819">9</span><span class="sxs-lookup"><span data-stu-id="999c8-819">9</span></span>

<span data-ttu-id="999c8-820">2</span><span class="sxs-lookup"><span data-stu-id="999c8-820">2</span></span><br/> <span data-ttu-id="999c8-821">0</span><span class="sxs-lookup"><span data-stu-id="999c8-821">0</span></span><br/>

<span data-ttu-id="999c8-822">1</span><span class="sxs-lookup"><span data-stu-id="999c8-822">1</span></span>

<span data-ttu-id="999c8-823">2</span><span class="sxs-lookup"><span data-stu-id="999c8-823">2</span></span>

<span data-ttu-id="999c8-824">3</span><span class="sxs-lookup"><span data-stu-id="999c8-824">3</span></span>

<span data-ttu-id="999c8-825">4</span><span class="sxs-lookup"><span data-stu-id="999c8-825">4</span></span>

<span data-ttu-id="999c8-826">5</span><span class="sxs-lookup"><span data-stu-id="999c8-826">5</span></span>

<span data-ttu-id="999c8-827">6</span><span class="sxs-lookup"><span data-stu-id="999c8-827">6</span></span>

<span data-ttu-id="999c8-828">7</span><span class="sxs-lookup"><span data-stu-id="999c8-828">7</span></span>

<span data-ttu-id="999c8-829">8</span><span class="sxs-lookup"><span data-stu-id="999c8-829">8</span></span>

<span data-ttu-id="999c8-830">9</span><span class="sxs-lookup"><span data-stu-id="999c8-830">9</span></span>

<span data-ttu-id="999c8-831">3</span><span class="sxs-lookup"><span data-stu-id="999c8-831">3</span></span><br/> <span data-ttu-id="999c8-832">0</span><span class="sxs-lookup"><span data-stu-id="999c8-832">0</span></span><br/>

<span data-ttu-id="999c8-833">1</span><span class="sxs-lookup"><span data-stu-id="999c8-833">1</span></span>

<span data-ttu-id="999c8-834">cDims</span><span class="sxs-lookup"><span data-stu-id="999c8-834">cDims</span></span>

<span data-ttu-id="999c8-835">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-835">Rgsabound (variable)</span></span>

<span data-ttu-id="999c8-836">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-836">vData (variable)</span></span>



 

<span data-ttu-id="999c8-837">**cDims**: entier non signé 32 bits, indiquant le nombre de dimensions du SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="999c8-837">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="999c8-838">**Rgsabound**: tableau qui contient une structure SAFEARRAYBOUND, comme spécifié dans la section 2.2.1.1.1.4 par dimension dans le SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="999c8-838">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="999c8-839">Ce tableau a la dimension la plus à gauche et la dimension la plus à droite en dernier.</span><span class="sxs-lookup"><span data-stu-id="999c8-839">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="999c8-840">**vdata**: vecteur d’éléments marshalés d’un type particulier, indiqué par le DWTYPE du SERIALIZEDPROPERTYVALUE conteneur, avec le bit 0x2000 effacé.</span><span class="sxs-lookup"><span data-stu-id="999c8-840">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="999c8-841">Le format de vData est le même que celui spécifié pour le champ vData de SAFEARRAY dans la section 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="999c8-841">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="999c8-842">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-842">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="999c8-843">La structure CFullPropSpec contient un GUID de jeu de propriétés et un identificateur de propriété pour identifier la propriété de manière unique.</span><span class="sxs-lookup"><span data-stu-id="999c8-843">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="999c8-844">0</span><span class="sxs-lookup"><span data-stu-id="999c8-844">0</span></span>

<span data-ttu-id="999c8-845">1</span><span class="sxs-lookup"><span data-stu-id="999c8-845">1</span></span>

<span data-ttu-id="999c8-846">2</span><span class="sxs-lookup"><span data-stu-id="999c8-846">2</span></span>

<span data-ttu-id="999c8-847">3</span><span class="sxs-lookup"><span data-stu-id="999c8-847">3</span></span>

<span data-ttu-id="999c8-848">4</span><span class="sxs-lookup"><span data-stu-id="999c8-848">4</span></span>

<span data-ttu-id="999c8-849">5</span><span class="sxs-lookup"><span data-stu-id="999c8-849">5</span></span>

<span data-ttu-id="999c8-850">6</span><span class="sxs-lookup"><span data-stu-id="999c8-850">6</span></span>

<span data-ttu-id="999c8-851">7</span><span class="sxs-lookup"><span data-stu-id="999c8-851">7</span></span>

<span data-ttu-id="999c8-852">8</span><span class="sxs-lookup"><span data-stu-id="999c8-852">8</span></span>

<span data-ttu-id="999c8-853">9</span><span class="sxs-lookup"><span data-stu-id="999c8-853">9</span></span>

<span data-ttu-id="999c8-854">1</span><span class="sxs-lookup"><span data-stu-id="999c8-854">1</span></span><br/> <span data-ttu-id="999c8-855">0</span><span class="sxs-lookup"><span data-stu-id="999c8-855">0</span></span><br/>

<span data-ttu-id="999c8-856">1</span><span class="sxs-lookup"><span data-stu-id="999c8-856">1</span></span>

<span data-ttu-id="999c8-857">2</span><span class="sxs-lookup"><span data-stu-id="999c8-857">2</span></span>

<span data-ttu-id="999c8-858">3</span><span class="sxs-lookup"><span data-stu-id="999c8-858">3</span></span>

<span data-ttu-id="999c8-859">4</span><span class="sxs-lookup"><span data-stu-id="999c8-859">4</span></span>

<span data-ttu-id="999c8-860">5</span><span class="sxs-lookup"><span data-stu-id="999c8-860">5</span></span>

<span data-ttu-id="999c8-861">6</span><span class="sxs-lookup"><span data-stu-id="999c8-861">6</span></span>

<span data-ttu-id="999c8-862">7</span><span class="sxs-lookup"><span data-stu-id="999c8-862">7</span></span>

<span data-ttu-id="999c8-863">8</span><span class="sxs-lookup"><span data-stu-id="999c8-863">8</span></span>

<span data-ttu-id="999c8-864">9</span><span class="sxs-lookup"><span data-stu-id="999c8-864">9</span></span>

<span data-ttu-id="999c8-865">2</span><span class="sxs-lookup"><span data-stu-id="999c8-865">2</span></span><br/> <span data-ttu-id="999c8-866">0</span><span class="sxs-lookup"><span data-stu-id="999c8-866">0</span></span><br/>

<span data-ttu-id="999c8-867">1</span><span class="sxs-lookup"><span data-stu-id="999c8-867">1</span></span>

<span data-ttu-id="999c8-868">2</span><span class="sxs-lookup"><span data-stu-id="999c8-868">2</span></span>

<span data-ttu-id="999c8-869">3</span><span class="sxs-lookup"><span data-stu-id="999c8-869">3</span></span>

<span data-ttu-id="999c8-870">4</span><span class="sxs-lookup"><span data-stu-id="999c8-870">4</span></span>

<span data-ttu-id="999c8-871">5</span><span class="sxs-lookup"><span data-stu-id="999c8-871">5</span></span>

<span data-ttu-id="999c8-872">6</span><span class="sxs-lookup"><span data-stu-id="999c8-872">6</span></span>

<span data-ttu-id="999c8-873">7</span><span class="sxs-lookup"><span data-stu-id="999c8-873">7</span></span>

<span data-ttu-id="999c8-874">8</span><span class="sxs-lookup"><span data-stu-id="999c8-874">8</span></span>

<span data-ttu-id="999c8-875">9</span><span class="sxs-lookup"><span data-stu-id="999c8-875">9</span></span>

<span data-ttu-id="999c8-876">3</span><span class="sxs-lookup"><span data-stu-id="999c8-876">3</span></span><br/> <span data-ttu-id="999c8-877">0</span><span class="sxs-lookup"><span data-stu-id="999c8-877">0</span></span><br/>

<span data-ttu-id="999c8-878">1</span><span class="sxs-lookup"><span data-stu-id="999c8-878">1</span></span>

<span data-ttu-id="999c8-879">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="999c8-879">\_guidPropSet</span></span>

<span data-ttu-id="999c8-880">...</span><span class="sxs-lookup"><span data-stu-id="999c8-880">...</span></span>

<span data-ttu-id="999c8-881">...</span><span class="sxs-lookup"><span data-stu-id="999c8-881">...</span></span>

<span data-ttu-id="999c8-882">...</span><span class="sxs-lookup"><span data-stu-id="999c8-882">...</span></span>

<span data-ttu-id="999c8-883">ulKind</span><span class="sxs-lookup"><span data-stu-id="999c8-883">ulKind</span></span>

<span data-ttu-id="999c8-884">PrSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-884">PrSpec</span></span>

<span data-ttu-id="999c8-885">Nom de la propriété (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-885">Property name (variable)</span></span>



 

<span data-ttu-id="999c8-886">**\_ GUIDPROPSET**: GUID du jeu de propriétés auquel appartient la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-886">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="999c8-887">**ulKind**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-887">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-888">L’une des valeurs suivantes, qui indique le contenu de PrSpec.</span><span class="sxs-lookup"><span data-stu-id="999c8-888">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="999c8-889">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-889">Value</span></span>                                            | <span data-ttu-id="999c8-890">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-890">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-891">PRSPEC \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="999c8-891">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="999c8-892">0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-892">0x00000000</span></span><br/> | <span data-ttu-id="999c8-893">Le champ PrSpec spécifie le nombre de caractères non NULL dans le champ nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-893">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="999c8-894">PRSPEC \_ propid</span><span class="sxs-lookup"><span data-stu-id="999c8-894">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="999c8-895">0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-895">0x00000001</span></span><br/>  | <span data-ttu-id="999c8-896">Le champ PrSpec spécifie l’ID de propriété (PROPID).</span><span class="sxs-lookup"><span data-stu-id="999c8-896">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="999c8-897">**PrSpec**: entier non signé 32 bits avec une signification comme indiqué par le champ ulKind.</span><span class="sxs-lookup"><span data-stu-id="999c8-897">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="999c8-898">**Nom** de la propriété : si ulKind a la valeur PRSPEC \_ propId, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-898">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="999c8-899">Si ulKind a la valeur PRSPEC \_ LPWStr, ce champ doit contenir un tableau ne respectant pas la casse des caractères Unicode non null PRSPEC, contenant le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-899">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="999c8-900">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-900">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="999c8-901">La structure CContentRestriction contient une chaîne à faire correspondre pour une propriété dans le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-901">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="999c8-902">0</span><span class="sxs-lookup"><span data-stu-id="999c8-902">0</span></span>

<span data-ttu-id="999c8-903">1</span><span class="sxs-lookup"><span data-stu-id="999c8-903">1</span></span>

<span data-ttu-id="999c8-904">2</span><span class="sxs-lookup"><span data-stu-id="999c8-904">2</span></span>

<span data-ttu-id="999c8-905">3</span><span class="sxs-lookup"><span data-stu-id="999c8-905">3</span></span>

<span data-ttu-id="999c8-906">4</span><span class="sxs-lookup"><span data-stu-id="999c8-906">4</span></span>

<span data-ttu-id="999c8-907">5</span><span class="sxs-lookup"><span data-stu-id="999c8-907">5</span></span>

<span data-ttu-id="999c8-908">6</span><span class="sxs-lookup"><span data-stu-id="999c8-908">6</span></span>

<span data-ttu-id="999c8-909">7</span><span class="sxs-lookup"><span data-stu-id="999c8-909">7</span></span>

<span data-ttu-id="999c8-910">8</span><span class="sxs-lookup"><span data-stu-id="999c8-910">8</span></span>

<span data-ttu-id="999c8-911">9</span><span class="sxs-lookup"><span data-stu-id="999c8-911">9</span></span>

<span data-ttu-id="999c8-912">1</span><span class="sxs-lookup"><span data-stu-id="999c8-912">1</span></span><br/> <span data-ttu-id="999c8-913">0</span><span class="sxs-lookup"><span data-stu-id="999c8-913">0</span></span><br/>

<span data-ttu-id="999c8-914">1</span><span class="sxs-lookup"><span data-stu-id="999c8-914">1</span></span>

<span data-ttu-id="999c8-915">2</span><span class="sxs-lookup"><span data-stu-id="999c8-915">2</span></span>

<span data-ttu-id="999c8-916">3</span><span class="sxs-lookup"><span data-stu-id="999c8-916">3</span></span>

<span data-ttu-id="999c8-917">4</span><span class="sxs-lookup"><span data-stu-id="999c8-917">4</span></span>

<span data-ttu-id="999c8-918">5</span><span class="sxs-lookup"><span data-stu-id="999c8-918">5</span></span>

<span data-ttu-id="999c8-919">6</span><span class="sxs-lookup"><span data-stu-id="999c8-919">6</span></span>

<span data-ttu-id="999c8-920">7</span><span class="sxs-lookup"><span data-stu-id="999c8-920">7</span></span>

<span data-ttu-id="999c8-921">8</span><span class="sxs-lookup"><span data-stu-id="999c8-921">8</span></span>

<span data-ttu-id="999c8-922">9</span><span class="sxs-lookup"><span data-stu-id="999c8-922">9</span></span>

<span data-ttu-id="999c8-923">2</span><span class="sxs-lookup"><span data-stu-id="999c8-923">2</span></span><br/> <span data-ttu-id="999c8-924">0</span><span class="sxs-lookup"><span data-stu-id="999c8-924">0</span></span><br/>

<span data-ttu-id="999c8-925">1</span><span class="sxs-lookup"><span data-stu-id="999c8-925">1</span></span>

<span data-ttu-id="999c8-926">2</span><span class="sxs-lookup"><span data-stu-id="999c8-926">2</span></span>

<span data-ttu-id="999c8-927">3</span><span class="sxs-lookup"><span data-stu-id="999c8-927">3</span></span>

<span data-ttu-id="999c8-928">4</span><span class="sxs-lookup"><span data-stu-id="999c8-928">4</span></span>

<span data-ttu-id="999c8-929">5</span><span class="sxs-lookup"><span data-stu-id="999c8-929">5</span></span>

<span data-ttu-id="999c8-930">6</span><span class="sxs-lookup"><span data-stu-id="999c8-930">6</span></span>

<span data-ttu-id="999c8-931">7</span><span class="sxs-lookup"><span data-stu-id="999c8-931">7</span></span>

<span data-ttu-id="999c8-932">8</span><span class="sxs-lookup"><span data-stu-id="999c8-932">8</span></span>

<span data-ttu-id="999c8-933">9</span><span class="sxs-lookup"><span data-stu-id="999c8-933">9</span></span>

<span data-ttu-id="999c8-934">3</span><span class="sxs-lookup"><span data-stu-id="999c8-934">3</span></span><br/> <span data-ttu-id="999c8-935">0</span><span class="sxs-lookup"><span data-stu-id="999c8-935">0</span></span><br/>

<span data-ttu-id="999c8-936">1</span><span class="sxs-lookup"><span data-stu-id="999c8-936">1</span></span>

<span data-ttu-id="999c8-937">\_Property (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-937">\_Property (variable)</span></span>

<span data-ttu-id="999c8-938">...</span><span class="sxs-lookup"><span data-stu-id="999c8-938">...</span></span>

<span data-ttu-id="999c8-939">Padding1 (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-939">Padding1 (variable)</span></span>

<span data-ttu-id="999c8-940">Cc</span><span class="sxs-lookup"><span data-stu-id="999c8-940">Cc</span></span>

<span data-ttu-id="999c8-941">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-941">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="999c8-942">...</span><span class="sxs-lookup"><span data-stu-id="999c8-942">...</span></span>

<span data-ttu-id="999c8-943">Padding2 (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-943">Padding2 (variable)</span></span>

<span data-ttu-id="999c8-944">lcid</span><span class="sxs-lookup"><span data-stu-id="999c8-944">lcid</span></span>

<span data-ttu-id="999c8-945">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="999c8-945">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="999c8-946">**\_ Property**: une structure CFullPropSpec, comme indiqué dans la section 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="999c8-946">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="999c8-947">Ce champ indique la propriété sur laquelle effectuer une opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="999c8-947">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="999c8-948">**Padding1**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-948">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="999c8-949">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-949">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="999c8-950">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-950">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="999c8-951">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-951">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-952">**CC**: entier non signé 32 bits, spécifiant le nombre de caractères dans le \_ champ pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="999c8-952">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="999c8-953">**\_ pwcsPhrase**: chaîne Unicode qui se termine par un caractère non null représentant le mot ou l’expression à mettre en correspondance pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-953">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="999c8-954">Ce champ ne doit pas être vide.</span><span class="sxs-lookup"><span data-stu-id="999c8-954">This field MUST NOT be empty.</span></span> <span data-ttu-id="999c8-955">Le champ CC contient la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="999c8-955">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="999c8-956">**Padding2**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-956">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="999c8-957">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-957">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="999c8-958">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-958">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="999c8-959">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-959">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-960">**LCID**: entier non signé 32 bits indiquant les paramètres régionaux de \_ pwcsPhrase, comme indiqué dans \[ MS-GPSI \] annexe A.</span><span class="sxs-lookup"><span data-stu-id="999c8-960">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="999c8-961">**\_ ulGenerateMethod**: entier non signé 32 bits, spécifiant la méthode à utiliser lors de la génération de formes de mots secondaires</span><span class="sxs-lookup"><span data-stu-id="999c8-961">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="999c8-962">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-962">Value</span></span>                                                       | <span data-ttu-id="999c8-963">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-963">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-964">GÉNÉRATION \_ exacte de la méthode \_</span><span class="sxs-lookup"><span data-stu-id="999c8-964">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="999c8-965">0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-965">0x00000000</span></span><br/>    | <span data-ttu-id="999c8-966">Correspondance exacte.</span><span class="sxs-lookup"><span data-stu-id="999c8-966">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="999c8-967">GÉNÉRER \_ le \_ préfixe de méthode</span><span class="sxs-lookup"><span data-stu-id="999c8-967">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="999c8-968">0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-968">0x00000001</span></span> <br/>  | <span data-ttu-id="999c8-969">Correspondance du préfixe.</span><span class="sxs-lookup"><span data-stu-id="999c8-969">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="999c8-970">GENERATE, \_ méthode \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="999c8-970">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="999c8-971">0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-971">0x00000002</span></span><br/> | <span data-ttu-id="999c8-972">Correspond aux fléchies d’un mot.</span><span class="sxs-lookup"><span data-stu-id="999c8-972">Matches inflections of a word.</span></span> <span data-ttu-id="999c8-973">Une inflexion d’un mot est une variante du mot racine dans la même partie de la parole qui a été modifiée selon les règles linguistiques d’une langue donnée.</span><span class="sxs-lookup"><span data-stu-id="999c8-973">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="999c8-974">Par exemple, les formes fléchies du verbe « natation » en anglais incluent « natation », « natation », « natation » et « SWAM ».</span><span class="sxs-lookup"><span data-stu-id="999c8-974">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="999c8-975">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="999c8-975">2.2.1.4 CKey</span></span>

<span data-ttu-id="999c8-976">La structure CKey contient une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-976">The CKey structure contains a property value.</span></span>



<span data-ttu-id="999c8-977">0</span><span class="sxs-lookup"><span data-stu-id="999c8-977">0</span></span>

<span data-ttu-id="999c8-978">1</span><span class="sxs-lookup"><span data-stu-id="999c8-978">1</span></span>

<span data-ttu-id="999c8-979">2</span><span class="sxs-lookup"><span data-stu-id="999c8-979">2</span></span>

<span data-ttu-id="999c8-980">3</span><span class="sxs-lookup"><span data-stu-id="999c8-980">3</span></span>

<span data-ttu-id="999c8-981">4</span><span class="sxs-lookup"><span data-stu-id="999c8-981">4</span></span>

<span data-ttu-id="999c8-982">5</span><span class="sxs-lookup"><span data-stu-id="999c8-982">5</span></span>

<span data-ttu-id="999c8-983">6</span><span class="sxs-lookup"><span data-stu-id="999c8-983">6</span></span>

<span data-ttu-id="999c8-984">7</span><span class="sxs-lookup"><span data-stu-id="999c8-984">7</span></span>

<span data-ttu-id="999c8-985">8</span><span class="sxs-lookup"><span data-stu-id="999c8-985">8</span></span>

<span data-ttu-id="999c8-986">9</span><span class="sxs-lookup"><span data-stu-id="999c8-986">9</span></span>

<span data-ttu-id="999c8-987">1</span><span class="sxs-lookup"><span data-stu-id="999c8-987">1</span></span><br/> <span data-ttu-id="999c8-988">0</span><span class="sxs-lookup"><span data-stu-id="999c8-988">0</span></span><br/>

<span data-ttu-id="999c8-989">1</span><span class="sxs-lookup"><span data-stu-id="999c8-989">1</span></span>

<span data-ttu-id="999c8-990">2</span><span class="sxs-lookup"><span data-stu-id="999c8-990">2</span></span>

<span data-ttu-id="999c8-991">3</span><span class="sxs-lookup"><span data-stu-id="999c8-991">3</span></span>

<span data-ttu-id="999c8-992">4</span><span class="sxs-lookup"><span data-stu-id="999c8-992">4</span></span>

<span data-ttu-id="999c8-993">5</span><span class="sxs-lookup"><span data-stu-id="999c8-993">5</span></span>

<span data-ttu-id="999c8-994">6</span><span class="sxs-lookup"><span data-stu-id="999c8-994">6</span></span>

<span data-ttu-id="999c8-995">7</span><span class="sxs-lookup"><span data-stu-id="999c8-995">7</span></span>

<span data-ttu-id="999c8-996">8</span><span class="sxs-lookup"><span data-stu-id="999c8-996">8</span></span>

<span data-ttu-id="999c8-997">9</span><span class="sxs-lookup"><span data-stu-id="999c8-997">9</span></span>

<span data-ttu-id="999c8-998">2</span><span class="sxs-lookup"><span data-stu-id="999c8-998">2</span></span><br/> <span data-ttu-id="999c8-999">0</span><span class="sxs-lookup"><span data-stu-id="999c8-999">0</span></span><br/>

<span data-ttu-id="999c8-1000">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1000">1</span></span>

<span data-ttu-id="999c8-1001">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1001">2</span></span>

<span data-ttu-id="999c8-1002">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1002">3</span></span>

<span data-ttu-id="999c8-1003">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1003">4</span></span>

<span data-ttu-id="999c8-1004">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1004">5</span></span>

<span data-ttu-id="999c8-1005">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1005">6</span></span>

<span data-ttu-id="999c8-1006">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1006">7</span></span>

<span data-ttu-id="999c8-1007">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1007">8</span></span>

<span data-ttu-id="999c8-1008">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1008">9</span></span>

<span data-ttu-id="999c8-1009">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1009">3</span></span><br/> <span data-ttu-id="999c8-1010">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1010">0</span></span><br/>

<span data-ttu-id="999c8-1011">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1011">1</span></span>

<span data-ttu-id="999c8-1012">PROPID</span><span class="sxs-lookup"><span data-stu-id="999c8-1012">PROPID</span></span>

<span data-ttu-id="999c8-1013">Libéré</span><span class="sxs-lookup"><span data-stu-id="999c8-1013">Cb</span></span>

<span data-ttu-id="999c8-1014">buf (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1014">buf (variable)</span></span>



 

<span data-ttu-id="999c8-1015">**Propid**: entier non signé 32 bits représentant l’ID de propriété comme indiqué dans la section 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-1015">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="999c8-1016">Les valeurs connues sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-1016">Well-known values are:</span></span>



| <span data-ttu-id="999c8-1017">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1017">Value</span></span>      | <span data-ttu-id="999c8-1018">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1018">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="999c8-1019">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="999c8-1019">0xFFFFFFFF</span></span> | <span data-ttu-id="999c8-1020">Représente un ID de propriété non valide et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="999c8-1020">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="999c8-1021">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="999c8-1021">0xFFFFFFFE</span></span> | <span data-ttu-id="999c8-1022">Représente un ID de propriété non valide et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="999c8-1022">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="999c8-1023">0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-1023">0x00000000</span></span> | <span data-ttu-id="999c8-1024">Représente un ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1024">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="999c8-1025">**CB**: entier non signé 32 bits contenant la longueur de buf, en octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-1025">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="999c8-1026">**buf**: séquence d’octets représentant la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1026">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="999c8-1027">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1027">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="999c8-1028">La structure CInternalPropertyRestriction contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="999c8-1028">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="999c8-1029">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1029">0</span></span>

<span data-ttu-id="999c8-1030">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1030">1</span></span>

<span data-ttu-id="999c8-1031">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1031">2</span></span>

<span data-ttu-id="999c8-1032">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1032">3</span></span>

<span data-ttu-id="999c8-1033">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1033">4</span></span>

<span data-ttu-id="999c8-1034">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1034">5</span></span>

<span data-ttu-id="999c8-1035">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1035">6</span></span>

<span data-ttu-id="999c8-1036">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1036">7</span></span>

<span data-ttu-id="999c8-1037">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1037">8</span></span>

<span data-ttu-id="999c8-1038">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1038">9</span></span>

<span data-ttu-id="999c8-1039">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1039">1</span></span><br/> <span data-ttu-id="999c8-1040">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1040">0</span></span><br/>

<span data-ttu-id="999c8-1041">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1041">1</span></span>

<span data-ttu-id="999c8-1042">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1042">2</span></span>

<span data-ttu-id="999c8-1043">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1043">3</span></span>

<span data-ttu-id="999c8-1044">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1044">4</span></span>

<span data-ttu-id="999c8-1045">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1045">5</span></span>

<span data-ttu-id="999c8-1046">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1046">6</span></span>

<span data-ttu-id="999c8-1047">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1047">7</span></span>

<span data-ttu-id="999c8-1048">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1048">8</span></span>

<span data-ttu-id="999c8-1049">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1049">9</span></span>

<span data-ttu-id="999c8-1050">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1050">2</span></span><br/> <span data-ttu-id="999c8-1051">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1051">0</span></span><br/>

<span data-ttu-id="999c8-1052">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1052">1</span></span>

<span data-ttu-id="999c8-1053">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1053">2</span></span>

<span data-ttu-id="999c8-1054">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1054">3</span></span>

<span data-ttu-id="999c8-1055">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1055">4</span></span>

<span data-ttu-id="999c8-1056">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1056">5</span></span>

<span data-ttu-id="999c8-1057">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1057">6</span></span>

<span data-ttu-id="999c8-1058">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1058">7</span></span>

<span data-ttu-id="999c8-1059">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1059">8</span></span>

<span data-ttu-id="999c8-1060">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1060">9</span></span>

<span data-ttu-id="999c8-1061">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1061">3</span></span><br/> <span data-ttu-id="999c8-1062">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1062">0</span></span><br/>

<span data-ttu-id="999c8-1063">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1063">1</span></span>

<span data-ttu-id="999c8-1064">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="999c8-1064">\_relop</span></span>

<span data-ttu-id="999c8-1065">\_ELECTRIQUE</span><span class="sxs-lookup"><span data-stu-id="999c8-1065">\_pid</span></span>

<span data-ttu-id="999c8-1066">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1066">\_prval (variable)</span></span>

<span data-ttu-id="999c8-1067">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="999c8-1067">restrictionPresent</span></span>

<span data-ttu-id="999c8-1068">nextRestriction (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1068">nextRestriction (variable)</span></span>



 

<span data-ttu-id="999c8-1069">**\_ RelOp**: entier 32 bits spécifiant la relation à exécuter sur la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1069">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="999c8-1070">Il doit s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-1070">MUST be one of the following values:</span></span>



| <span data-ttu-id="999c8-1071">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1071">Value</span></span>                 | <span data-ttu-id="999c8-1072">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1072">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1073">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-1073">PRLT 0x00000000</span></span>       | <span data-ttu-id="999c8-1074">Comparaison d’infériorité.</span><span class="sxs-lookup"><span data-stu-id="999c8-1074">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="999c8-1075">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-1075">PRLE 0x00000001</span></span>       | <span data-ttu-id="999c8-1076">Comparaison d’infériorité ou d’égalité.</span><span class="sxs-lookup"><span data-stu-id="999c8-1076">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="999c8-1077">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-1077">PRGT 0x00000002</span></span>       | <span data-ttu-id="999c8-1078">Comparaison plus grande que.</span><span class="sxs-lookup"><span data-stu-id="999c8-1078">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="999c8-1079">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-1079">PRGE 0x00000003</span></span>       | <span data-ttu-id="999c8-1080">Comparaison supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="999c8-1080">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="999c8-1081">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1081">PREQ 0x00000004</span></span>       | <span data-ttu-id="999c8-1082">Comparaison d’égalité.</span><span class="sxs-lookup"><span data-stu-id="999c8-1082">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="999c8-1083">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="999c8-1083">PRNE 0x00000005</span></span>       | <span data-ttu-id="999c8-1084">Comparaison inégale.</span><span class="sxs-lookup"><span data-stu-id="999c8-1084">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="999c8-1085">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="999c8-1085">PRRE 0x00000006</span></span>       | <span data-ttu-id="999c8-1086">Comparaison d’expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="999c8-1086">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="999c8-1087">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="999c8-1087">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="999c8-1088">Opérateur de bits AND qui retourne l’opérande de droite.</span><span class="sxs-lookup"><span data-stu-id="999c8-1088">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="999c8-1089">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="999c8-1089">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="999c8-1090">Opérateur de bits AND qui retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="999c8-1090">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="999c8-1091">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="999c8-1091">PRAll 0x00000100</span></span>      | <span data-ttu-id="999c8-1092">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et n’a la valeur true que si l’opération a la valeur true pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1092">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="999c8-1093">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="999c8-1093">PRAny 0x00000200</span></span>      | <span data-ttu-id="999c8-1094">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et a la valeur true si l’opération a la valeur true pour une ligne quelconque.</span><span class="sxs-lookup"><span data-stu-id="999c8-1094">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="999c8-1095">**\_ PID**: entier non signé 32 bits représentant l’ID de propriété (consultez PROPID dans la section 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="999c8-1095">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="999c8-1096">**\_ Prval**: CBaseStorageVariant contenant la valeur à associer à la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1096">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="999c8-1097">**restrictionPresent**: valeur d’octet indiquant si le champ nextRestriction est présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-1097">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="999c8-1098">DOIT être défini sur 0x00 ou 0x01.</span><span class="sxs-lookup"><span data-stu-id="999c8-1098">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="999c8-1099">Si cette valeur est définie sur 0x01, restrictionPresent indique que le champ nextRestriction est présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-1099">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="999c8-1100">Si la valeur est 0x00, restrictionPresent indique que le champ nextRestriction n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-1100">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="999c8-1101">**nextRestriction**: structure CRestriction, comme spécifié dans la section 2.2.1.16, en spécifiant une restriction supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="999c8-1101">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="999c8-1102">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1102">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="999c8-1103">La structure CNatLanguageRestriction contient une correspondance de **requête en langage naturel** pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1103">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="999c8-1104">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1104">0</span></span>

<span data-ttu-id="999c8-1105">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1105">1</span></span>

<span data-ttu-id="999c8-1106">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1106">2</span></span>

<span data-ttu-id="999c8-1107">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1107">3</span></span>

<span data-ttu-id="999c8-1108">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1108">4</span></span>

<span data-ttu-id="999c8-1109">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1109">5</span></span>

<span data-ttu-id="999c8-1110">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1110">6</span></span>

<span data-ttu-id="999c8-1111">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1111">7</span></span>

<span data-ttu-id="999c8-1112">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1112">8</span></span>

<span data-ttu-id="999c8-1113">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1113">9</span></span>

<span data-ttu-id="999c8-1114">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1114">1</span></span><br/> <span data-ttu-id="999c8-1115">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1115">0</span></span><br/>

<span data-ttu-id="999c8-1116">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1116">1</span></span>

<span data-ttu-id="999c8-1117">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1117">2</span></span>

<span data-ttu-id="999c8-1118">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1118">3</span></span>

<span data-ttu-id="999c8-1119">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1119">4</span></span>

<span data-ttu-id="999c8-1120">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1120">5</span></span>

<span data-ttu-id="999c8-1121">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1121">6</span></span>

<span data-ttu-id="999c8-1122">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1122">7</span></span>

<span data-ttu-id="999c8-1123">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1123">8</span></span>

<span data-ttu-id="999c8-1124">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1124">9</span></span>

<span data-ttu-id="999c8-1125">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1125">2</span></span><br/> <span data-ttu-id="999c8-1126">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1126">0</span></span><br/>

<span data-ttu-id="999c8-1127">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1127">1</span></span>

<span data-ttu-id="999c8-1128">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1128">2</span></span>

<span data-ttu-id="999c8-1129">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1129">3</span></span>

<span data-ttu-id="999c8-1130">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1130">4</span></span>

<span data-ttu-id="999c8-1131">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1131">5</span></span>

<span data-ttu-id="999c8-1132">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1132">6</span></span>

<span data-ttu-id="999c8-1133">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1133">7</span></span>

<span data-ttu-id="999c8-1134">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1134">8</span></span>

<span data-ttu-id="999c8-1135">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1135">9</span></span>

<span data-ttu-id="999c8-1136">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1136">3</span></span><br/> <span data-ttu-id="999c8-1137">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1137">0</span></span><br/>

<span data-ttu-id="999c8-1138">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1138">1</span></span>

<span data-ttu-id="999c8-1139">\_Property (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1139">\_Property (variable)</span></span>

<span data-ttu-id="999c8-1140">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1140">...</span></span>

<span data-ttu-id="999c8-1141">\_remplissage \_ de CC (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1141">\_padding\_cc (variable)</span></span>

<span data-ttu-id="999c8-1142">Cc</span><span class="sxs-lookup"><span data-stu-id="999c8-1142">Cc</span></span>

<span data-ttu-id="999c8-1143">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1143">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="999c8-1144">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1144">...</span></span>

<span data-ttu-id="999c8-1145">\_\_LCID de remplissage (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1145">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="999c8-1146">Lcid</span><span class="sxs-lookup"><span data-stu-id="999c8-1146">Lcid</span></span>



 

<span data-ttu-id="999c8-1147">**\_ Property**: une structure CFullPropSpec, comme indiqué dans la section 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="999c8-1147">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="999c8-1148">Ce champ indique la propriété sur laquelle effectuer l’opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="999c8-1148">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="999c8-1149">**\_ remplissage de \_ CC**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-1149">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="999c8-1150">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-1150">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="999c8-1151">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-1151">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="999c8-1152">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1152">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-1153">**CC**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-1153">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-1154">Nombre de caractères dans le \_ champ pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="999c8-1154">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="999c8-1155">**\_ pwcsPhrase**: chaîne Unicode qui se termine par un caractère non null représentant le mot ou l’expression à mettre en correspondance pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1155">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="999c8-1156">NE doit pas être vide.</span><span class="sxs-lookup"><span data-stu-id="999c8-1156">MUST NOT be empty.</span></span> <span data-ttu-id="999c8-1157">Le champ CC contient la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="999c8-1157">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="999c8-1158">**\_ \_ LCID de remplissage**: ce champ doit avoir une longueur comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-1158">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="999c8-1159">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-1159">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="999c8-1160">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-1160">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="999c8-1161">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1161">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-1162">**LCID**: entier non signé 32 bits indiquant les paramètres régionaux de \_ pwcsPhrase, comme spécifié dans \[ MS-GPSI \] annexe A.</span><span class="sxs-lookup"><span data-stu-id="999c8-1162">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="999c8-1163">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1163">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="999c8-1164">La structure CNodeRestriction contient un tableau de nœuds d' **arborescence de commandes** qui spécifient les restrictions pour la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1164">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="999c8-1165">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1165">0</span></span>

<span data-ttu-id="999c8-1166">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1166">1</span></span>

<span data-ttu-id="999c8-1167">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1167">2</span></span>

<span data-ttu-id="999c8-1168">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1168">3</span></span>

<span data-ttu-id="999c8-1169">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1169">4</span></span>

<span data-ttu-id="999c8-1170">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1170">5</span></span>

<span data-ttu-id="999c8-1171">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1171">6</span></span>

<span data-ttu-id="999c8-1172">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1172">7</span></span>

<span data-ttu-id="999c8-1173">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1173">8</span></span>

<span data-ttu-id="999c8-1174">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1174">9</span></span>

<span data-ttu-id="999c8-1175">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1175">1</span></span><br/> <span data-ttu-id="999c8-1176">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1176">0</span></span><br/>

<span data-ttu-id="999c8-1177">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1177">1</span></span>

<span data-ttu-id="999c8-1178">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1178">2</span></span>

<span data-ttu-id="999c8-1179">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1179">3</span></span>

<span data-ttu-id="999c8-1180">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1180">4</span></span>

<span data-ttu-id="999c8-1181">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1181">5</span></span>

<span data-ttu-id="999c8-1182">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1182">6</span></span>

<span data-ttu-id="999c8-1183">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1183">7</span></span>

<span data-ttu-id="999c8-1184">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1184">8</span></span>

<span data-ttu-id="999c8-1185">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1185">9</span></span>

<span data-ttu-id="999c8-1186">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1186">2</span></span><br/> <span data-ttu-id="999c8-1187">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1187">0</span></span><br/>

<span data-ttu-id="999c8-1188">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1188">1</span></span>

<span data-ttu-id="999c8-1189">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1189">2</span></span>

<span data-ttu-id="999c8-1190">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1190">3</span></span>

<span data-ttu-id="999c8-1191">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1191">4</span></span>

<span data-ttu-id="999c8-1192">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1192">5</span></span>

<span data-ttu-id="999c8-1193">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1193">6</span></span>

<span data-ttu-id="999c8-1194">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1194">7</span></span>

<span data-ttu-id="999c8-1195">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1195">8</span></span>

<span data-ttu-id="999c8-1196">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1196">9</span></span>

<span data-ttu-id="999c8-1197">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1197">3</span></span><br/> <span data-ttu-id="999c8-1198">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1198">0</span></span><br/>

<span data-ttu-id="999c8-1199">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1199">1</span></span>

<span data-ttu-id="999c8-1200">\_cNode</span><span class="sxs-lookup"><span data-stu-id="999c8-1200">\_cNode</span></span>

<span data-ttu-id="999c8-1201">\_paNode (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1201">\_paNode (variable)</span></span>



 

<span data-ttu-id="999c8-1202">**\_ CNode**: entier non signé 32 bits spécifiant le nombre de structures CRestriction contenues dans le \_ champ paNode.</span><span class="sxs-lookup"><span data-stu-id="999c8-1202">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="999c8-1203">**\_ paNode**: tableau de structures CRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1203">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="999c8-1204">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient ce tableau.</span><span class="sxs-lookup"><span data-stu-id="999c8-1204">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="999c8-1205">Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-1205">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="999c8-1206">Le contenu des octets de remplissage doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1206">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="999c8-1207">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1207">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="999c8-1208">La structure COccRestriction contient l’emplacement d’un mot dans une expression.</span><span class="sxs-lookup"><span data-stu-id="999c8-1208">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="999c8-1209">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1209">0</span></span>

<span data-ttu-id="999c8-1210">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1210">1</span></span>

<span data-ttu-id="999c8-1211">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1211">2</span></span>

<span data-ttu-id="999c8-1212">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1212">3</span></span>

<span data-ttu-id="999c8-1213">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1213">4</span></span>

<span data-ttu-id="999c8-1214">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1214">5</span></span>

<span data-ttu-id="999c8-1215">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1215">6</span></span>

<span data-ttu-id="999c8-1216">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1216">7</span></span>

<span data-ttu-id="999c8-1217">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1217">8</span></span>

<span data-ttu-id="999c8-1218">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1218">9</span></span>

<span data-ttu-id="999c8-1219">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1219">1</span></span><br/> <span data-ttu-id="999c8-1220">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1220">0</span></span><br/>

<span data-ttu-id="999c8-1221">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1221">1</span></span>

<span data-ttu-id="999c8-1222">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1222">2</span></span>

<span data-ttu-id="999c8-1223">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1223">3</span></span>

<span data-ttu-id="999c8-1224">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1224">4</span></span>

<span data-ttu-id="999c8-1225">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1225">5</span></span>

<span data-ttu-id="999c8-1226">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1226">6</span></span>

<span data-ttu-id="999c8-1227">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1227">7</span></span>

<span data-ttu-id="999c8-1228">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1228">8</span></span>

<span data-ttu-id="999c8-1229">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1229">9</span></span>

<span data-ttu-id="999c8-1230">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1230">2</span></span><br/> <span data-ttu-id="999c8-1231">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1231">0</span></span><br/>

<span data-ttu-id="999c8-1232">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1232">1</span></span>

<span data-ttu-id="999c8-1233">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1233">2</span></span>

<span data-ttu-id="999c8-1234">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1234">3</span></span>

<span data-ttu-id="999c8-1235">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1235">4</span></span>

<span data-ttu-id="999c8-1236">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1236">5</span></span>

<span data-ttu-id="999c8-1237">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1237">6</span></span>

<span data-ttu-id="999c8-1238">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1238">7</span></span>

<span data-ttu-id="999c8-1239">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1239">8</span></span>

<span data-ttu-id="999c8-1240">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1240">9</span></span>

<span data-ttu-id="999c8-1241">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1241">3</span></span><br/> <span data-ttu-id="999c8-1242">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1242">0</span></span><br/>

<span data-ttu-id="999c8-1243">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1243">1</span></span>

<span data-ttu-id="999c8-1244">\_ETag</span><span class="sxs-lookup"><span data-stu-id="999c8-1244">\_occ</span></span>

<span data-ttu-id="999c8-1245">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="999c8-1245">\_cPrevNoiseWords</span></span>

<span data-ttu-id="999c8-1246">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="999c8-1246">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="999c8-1247">**\_ ETag**: entier non signé 32 bits spécifiant le décalage du mot dans une chaîne de requête, en unités de mots.</span><span class="sxs-lookup"><span data-stu-id="999c8-1247">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="999c8-1248">Un mot, tel qu’il est utilisé dans cette spécification, est une unité de langue dans tous les paramètres régionaux qui impliquent la signification.</span><span class="sxs-lookup"><span data-stu-id="999c8-1248">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="999c8-1249">**\_ cPrevNoiseWords**: entier non signé 32 bits contenant le nombre de **mots parasites** qui se produisent entre ce mot et le mot précédent dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="999c8-1249">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="999c8-1250">**\_ cNextNoiseWords**: entier non signé 32 bits contenant le nombre de mots parasites qui se produisent entre ce mot et le mot suivant dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="999c8-1250">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="999c8-1251">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1251">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="999c8-1252">La structure CPropertyRestriction contient une valeur de propriété à associer à une opération.</span><span class="sxs-lookup"><span data-stu-id="999c8-1252">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="999c8-1253">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1253">0</span></span>

<span data-ttu-id="999c8-1254">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1254">1</span></span>

<span data-ttu-id="999c8-1255">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1255">2</span></span>

<span data-ttu-id="999c8-1256">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1256">3</span></span>

<span data-ttu-id="999c8-1257">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1257">4</span></span>

<span data-ttu-id="999c8-1258">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1258">5</span></span>

<span data-ttu-id="999c8-1259">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1259">6</span></span>

<span data-ttu-id="999c8-1260">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1260">7</span></span>

<span data-ttu-id="999c8-1261">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1261">8</span></span>

<span data-ttu-id="999c8-1262">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1262">9</span></span>

<span data-ttu-id="999c8-1263">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1263">1</span></span><br/> <span data-ttu-id="999c8-1264">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1264">0</span></span><br/>

<span data-ttu-id="999c8-1265">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1265">1</span></span>

<span data-ttu-id="999c8-1266">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1266">2</span></span>

<span data-ttu-id="999c8-1267">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1267">3</span></span>

<span data-ttu-id="999c8-1268">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1268">4</span></span>

<span data-ttu-id="999c8-1269">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1269">5</span></span>

<span data-ttu-id="999c8-1270">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1270">6</span></span>

<span data-ttu-id="999c8-1271">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1271">7</span></span>

<span data-ttu-id="999c8-1272">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1272">8</span></span>

<span data-ttu-id="999c8-1273">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1273">9</span></span>

<span data-ttu-id="999c8-1274">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1274">2</span></span><br/> <span data-ttu-id="999c8-1275">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1275">0</span></span><br/>

<span data-ttu-id="999c8-1276">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1276">1</span></span>

<span data-ttu-id="999c8-1277">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1277">2</span></span>

<span data-ttu-id="999c8-1278">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1278">3</span></span>

<span data-ttu-id="999c8-1279">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1279">4</span></span>

<span data-ttu-id="999c8-1280">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1280">5</span></span>

<span data-ttu-id="999c8-1281">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1281">6</span></span>

<span data-ttu-id="999c8-1282">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1282">7</span></span>

<span data-ttu-id="999c8-1283">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1283">8</span></span>

<span data-ttu-id="999c8-1284">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1284">9</span></span>

<span data-ttu-id="999c8-1285">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1285">3</span></span><br/> <span data-ttu-id="999c8-1286">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1286">0</span></span><br/>

<span data-ttu-id="999c8-1287">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1287">1</span></span>

<span data-ttu-id="999c8-1288">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="999c8-1288">\_relop</span></span>

<span data-ttu-id="999c8-1289">\_Property (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1289">\_Property (variable)</span></span>

<span data-ttu-id="999c8-1290">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1290">\_prval (variable)</span></span>



 

<span data-ttu-id="999c8-1291">**\_ RelOp**: entier non signé 32 bits spécifiant la relation à exécuter sur la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1291">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="999c8-1292">DOIT avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1292">MUST be one of the following values.</span></span>



| <span data-ttu-id="999c8-1293">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1293">Value</span></span>                 | <span data-ttu-id="999c8-1294">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1294">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1295">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-1295">PRLT 0x00000000</span></span>       | <span data-ttu-id="999c8-1296">Comparaison d’infériorité.</span><span class="sxs-lookup"><span data-stu-id="999c8-1296">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="999c8-1297">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-1297">PRLE 0x00000001</span></span>       | <span data-ttu-id="999c8-1298">Comparaison d’infériorité ou d’égalité.</span><span class="sxs-lookup"><span data-stu-id="999c8-1298">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="999c8-1299">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-1299">PRGT 0x00000002</span></span>       | <span data-ttu-id="999c8-1300">Comparaison plus grande que.</span><span class="sxs-lookup"><span data-stu-id="999c8-1300">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="999c8-1301">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-1301">PRGE 0x00000003</span></span>       | <span data-ttu-id="999c8-1302">Comparaison supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="999c8-1302">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="999c8-1303">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1303">PREQ 0x00000004</span></span>       | <span data-ttu-id="999c8-1304">Comparaison d’égalité.</span><span class="sxs-lookup"><span data-stu-id="999c8-1304">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="999c8-1305">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="999c8-1305">PRNE 0x00000005</span></span>       | <span data-ttu-id="999c8-1306">Comparaison inégale.</span><span class="sxs-lookup"><span data-stu-id="999c8-1306">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="999c8-1307">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="999c8-1307">PRRE 0x00000006</span></span>       | <span data-ttu-id="999c8-1308">Comparaison d’expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="999c8-1308">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="999c8-1309">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="999c8-1309">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="999c8-1310">Opérateur de bits AND qui retourne l’opérande de droite.</span><span class="sxs-lookup"><span data-stu-id="999c8-1310">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="999c8-1311">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="999c8-1311">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="999c8-1312">Opérateur de bits AND qui retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="999c8-1312">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="999c8-1313">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="999c8-1313">PRAll 0x00000100</span></span>      | <span data-ttu-id="999c8-1314">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et n’a la valeur true que si l’opération a la valeur true pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1314">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="999c8-1315">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="999c8-1315">PRAny 0x00000200</span></span>      | <span data-ttu-id="999c8-1316">L’opération doit être effectuée sur une colonne d’un ensemble de lignes, et a la valeur true si l’opération a la valeur true pour une ligne quelconque.</span><span class="sxs-lookup"><span data-stu-id="999c8-1316">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="999c8-1317">**\_ Propriété**: une structure CFullPropSpec, comme spécifié dans la section 2.2.1.2, indiquant la propriété sur laquelle effectuer une opération de correspondance.</span><span class="sxs-lookup"><span data-stu-id="999c8-1317">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="999c8-1318">**\_ prval**: structure CBaseStorageVariant, comme indiqué dans la section 2.2.1.1, contenant la valeur à associer à la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1318">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="999c8-1319">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1319">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="999c8-1320">La structure CRangeRestriction contient une restriction sur une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="999c8-1320">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="999c8-1321">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1321">0</span></span>

<span data-ttu-id="999c8-1322">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1322">1</span></span>

<span data-ttu-id="999c8-1323">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1323">2</span></span>

<span data-ttu-id="999c8-1324">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1324">3</span></span>

<span data-ttu-id="999c8-1325">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1325">4</span></span>

<span data-ttu-id="999c8-1326">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1326">5</span></span>

<span data-ttu-id="999c8-1327">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1327">6</span></span>

<span data-ttu-id="999c8-1328">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1328">7</span></span>

<span data-ttu-id="999c8-1329">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1329">8</span></span>

<span data-ttu-id="999c8-1330">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1330">9</span></span>

<span data-ttu-id="999c8-1331">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1331">1</span></span><br/> <span data-ttu-id="999c8-1332">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1332">0</span></span><br/>

<span data-ttu-id="999c8-1333">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1333">1</span></span>

<span data-ttu-id="999c8-1334">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1334">2</span></span>

<span data-ttu-id="999c8-1335">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1335">3</span></span>

<span data-ttu-id="999c8-1336">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1336">4</span></span>

<span data-ttu-id="999c8-1337">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1337">5</span></span>

<span data-ttu-id="999c8-1338">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1338">6</span></span>

<span data-ttu-id="999c8-1339">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1339">7</span></span>

<span data-ttu-id="999c8-1340">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1340">8</span></span>

<span data-ttu-id="999c8-1341">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1341">9</span></span>

<span data-ttu-id="999c8-1342">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1342">2</span></span><br/> <span data-ttu-id="999c8-1343">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1343">0</span></span><br/>

<span data-ttu-id="999c8-1344">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1344">1</span></span>

<span data-ttu-id="999c8-1345">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1345">2</span></span>

<span data-ttu-id="999c8-1346">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1346">3</span></span>

<span data-ttu-id="999c8-1347">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1347">4</span></span>

<span data-ttu-id="999c8-1348">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1348">5</span></span>

<span data-ttu-id="999c8-1349">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1349">6</span></span>

<span data-ttu-id="999c8-1350">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1350">7</span></span>

<span data-ttu-id="999c8-1351">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1351">8</span></span>

<span data-ttu-id="999c8-1352">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1352">9</span></span>

<span data-ttu-id="999c8-1353">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1353">3</span></span><br/> <span data-ttu-id="999c8-1354">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1354">0</span></span><br/>

<span data-ttu-id="999c8-1355">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1355">1</span></span>

<span data-ttu-id="999c8-1356">\_keystart (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1356">\_keyStart (variable)</span></span>

<span data-ttu-id="999c8-1357">\_keyEnd (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1357">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="999c8-1358">**\_ keystart**: une structure CKey, comme spécifié dans la section 2.2.1.4, contenant le début de la plage.</span><span class="sxs-lookup"><span data-stu-id="999c8-1358">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="999c8-1359">**\_ keyEnd**: structure CKey contenant la fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="999c8-1359">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="999c8-1360">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1360">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="999c8-1361">La structure CScopeRestriction contient une restriction sur les fichiers à rechercher.</span><span class="sxs-lookup"><span data-stu-id="999c8-1361">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="999c8-1362">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1362">0</span></span>

<span data-ttu-id="999c8-1363">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1363">1</span></span>

<span data-ttu-id="999c8-1364">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1364">2</span></span>

<span data-ttu-id="999c8-1365">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1365">3</span></span>

<span data-ttu-id="999c8-1366">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1366">4</span></span>

<span data-ttu-id="999c8-1367">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1367">5</span></span>

<span data-ttu-id="999c8-1368">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1368">6</span></span>

<span data-ttu-id="999c8-1369">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1369">7</span></span>

<span data-ttu-id="999c8-1370">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1370">8</span></span>

<span data-ttu-id="999c8-1371">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1371">9</span></span>

<span data-ttu-id="999c8-1372">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1372">1</span></span><br/> <span data-ttu-id="999c8-1373">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1373">0</span></span><br/>

<span data-ttu-id="999c8-1374">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1374">1</span></span>

<span data-ttu-id="999c8-1375">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1375">2</span></span>

<span data-ttu-id="999c8-1376">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1376">3</span></span>

<span data-ttu-id="999c8-1377">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1377">4</span></span>

<span data-ttu-id="999c8-1378">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1378">5</span></span>

<span data-ttu-id="999c8-1379">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1379">6</span></span>

<span data-ttu-id="999c8-1380">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1380">7</span></span>

<span data-ttu-id="999c8-1381">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1381">8</span></span>

<span data-ttu-id="999c8-1382">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1382">9</span></span>

<span data-ttu-id="999c8-1383">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1383">2</span></span><br/> <span data-ttu-id="999c8-1384">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1384">0</span></span><br/>

<span data-ttu-id="999c8-1385">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1385">1</span></span>

<span data-ttu-id="999c8-1386">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1386">2</span></span>

<span data-ttu-id="999c8-1387">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1387">3</span></span>

<span data-ttu-id="999c8-1388">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1388">4</span></span>

<span data-ttu-id="999c8-1389">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1389">5</span></span>

<span data-ttu-id="999c8-1390">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1390">6</span></span>

<span data-ttu-id="999c8-1391">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1391">7</span></span>

<span data-ttu-id="999c8-1392">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1392">8</span></span>

<span data-ttu-id="999c8-1393">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1393">9</span></span>

<span data-ttu-id="999c8-1394">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1394">3</span></span><br/> <span data-ttu-id="999c8-1395">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1395">0</span></span><br/>

<span data-ttu-id="999c8-1396">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1396">1</span></span>

<span data-ttu-id="999c8-1397">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="999c8-1397">CcLowerPath</span></span>

<span data-ttu-id="999c8-1398">\_lowerPath (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1398">\_lowerPath (variable)</span></span>

<span data-ttu-id="999c8-1399">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1399">...</span></span>

<span data-ttu-id="999c8-1400">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1400">\_padding ( variable)</span></span>

<span data-ttu-id="999c8-1401">\_base</span><span class="sxs-lookup"><span data-stu-id="999c8-1401">\_length</span></span>

<span data-ttu-id="999c8-1402">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="999c8-1402">\_fRecursive</span></span>

<span data-ttu-id="999c8-1403">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="999c8-1403">\_fVirtual</span></span>



 

<span data-ttu-id="999c8-1404">**CcLowerPath**: entier non signé 32 bits contenant le nombre de caractères Unicode dans le \_ champ lowerPath.</span><span class="sxs-lookup"><span data-stu-id="999c8-1404">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="999c8-1405">**\_ lowerPath**: chaîne Unicode qui se termine par un caractère non null qui représente le **chemin d’accès** auquel la requête doit être restreinte.</span><span class="sxs-lookup"><span data-stu-id="999c8-1405">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="999c8-1406">Le champ CcLowerPath contient la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="999c8-1406">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="999c8-1407">**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-1407">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="999c8-1408">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-1408">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="999c8-1409">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-1409">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="999c8-1410">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1410">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-1411">**\_ Length**: entier non signé 32 bits contenant la longueur de \_ LowerPath, en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="999c8-1411">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="999c8-1412">Il doit s’agir de la même valeur que CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="999c8-1412">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="999c8-1413">**\_ fRecursive**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-1413">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-1414">DOIT être défini sur 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-1414">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="999c8-1415">Si la valeur est définie sur 0x00000001, le serveur doit examiner de manière récursive tous les sous-répertoires du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="999c8-1415">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="999c8-1416">Si la valeur est 0x00000000, le serveur n’examine pas les sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="999c8-1416">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="999c8-1417">**\_ fVirtual**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-1417">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-1418">DOIT être défini sur 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-1418">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="999c8-1419">Si la valeur est 0x00000001, \_ lowerPath est un chemin d’accès virtuel (le Uniform Resource Locator (URL) associé à un répertoire physique sur le système de fichiers) pour un site Web.</span><span class="sxs-lookup"><span data-stu-id="999c8-1419">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="999c8-1420">Si la valeur est 0x00000000, \_ lowerPath est un chemin d’accès au système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="999c8-1420">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="999c8-1421">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="999c8-1421">2.2.1.12 CSort</span></span>

<span data-ttu-id="999c8-1422">La structure CSort identifie une colonne à trier.</span><span class="sxs-lookup"><span data-stu-id="999c8-1422">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="999c8-1423">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1423">0</span></span>

<span data-ttu-id="999c8-1424">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1424">1</span></span>

<span data-ttu-id="999c8-1425">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1425">2</span></span>

<span data-ttu-id="999c8-1426">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1426">3</span></span>

<span data-ttu-id="999c8-1427">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1427">4</span></span>

<span data-ttu-id="999c8-1428">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1428">5</span></span>

<span data-ttu-id="999c8-1429">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1429">6</span></span>

<span data-ttu-id="999c8-1430">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1430">7</span></span>

<span data-ttu-id="999c8-1431">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1431">8</span></span>

<span data-ttu-id="999c8-1432">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1432">9</span></span>

<span data-ttu-id="999c8-1433">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1433">1</span></span><br/> <span data-ttu-id="999c8-1434">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1434">0</span></span><br/>

<span data-ttu-id="999c8-1435">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1435">1</span></span>

<span data-ttu-id="999c8-1436">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1436">2</span></span>

<span data-ttu-id="999c8-1437">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1437">3</span></span>

<span data-ttu-id="999c8-1438">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1438">4</span></span>

<span data-ttu-id="999c8-1439">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1439">5</span></span>

<span data-ttu-id="999c8-1440">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1440">6</span></span>

<span data-ttu-id="999c8-1441">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1441">7</span></span>

<span data-ttu-id="999c8-1442">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1442">8</span></span>

<span data-ttu-id="999c8-1443">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1443">9</span></span>

<span data-ttu-id="999c8-1444">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1444">2</span></span><br/> <span data-ttu-id="999c8-1445">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1445">0</span></span><br/>

<span data-ttu-id="999c8-1446">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1446">1</span></span>

<span data-ttu-id="999c8-1447">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1447">2</span></span>

<span data-ttu-id="999c8-1448">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1448">3</span></span>

<span data-ttu-id="999c8-1449">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1449">4</span></span>

<span data-ttu-id="999c8-1450">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1450">5</span></span>

<span data-ttu-id="999c8-1451">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1451">6</span></span>

<span data-ttu-id="999c8-1452">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1452">7</span></span>

<span data-ttu-id="999c8-1453">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1453">8</span></span>

<span data-ttu-id="999c8-1454">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1454">9</span></span>

<span data-ttu-id="999c8-1455">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1455">3</span></span><br/> <span data-ttu-id="999c8-1456">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1456">0</span></span><br/>

<span data-ttu-id="999c8-1457">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1457">1</span></span>

<span data-ttu-id="999c8-1458">pidColumn</span><span class="sxs-lookup"><span data-stu-id="999c8-1458">pidColumn</span></span>

<span data-ttu-id="999c8-1459">Valeur dwOrd</span><span class="sxs-lookup"><span data-stu-id="999c8-1459">dwOrder</span></span>

<span data-ttu-id="999c8-1460">locale</span><span class="sxs-lookup"><span data-stu-id="999c8-1460">locale</span></span>



 

<span data-ttu-id="999c8-1461">**pidColumn**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-1461">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-1462">Numéro de la colonne par laquelle Trier.</span><span class="sxs-lookup"><span data-stu-id="999c8-1462">The number of the column to sort by.</span></span>

<span data-ttu-id="999c8-1463">**DWORD**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-1463">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-1464">DOIT avoir l’une des valeurs suivantes, en spécifiant comment trier en fonction de la colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-1464">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="999c8-1465">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1465">Value</span></span>                        | <span data-ttu-id="999c8-1466">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1466">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1467">REQUÊTE \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-1467">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="999c8-1468">Les lignes doivent être triées dans l’ordre croissant en fonction des valeurs de la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="999c8-1468">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="999c8-1469">REQUÊTE \_ descendante 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-1469">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="999c8-1470">Les lignes doivent être triées dans l’ordre décroissant en fonction des valeurs de la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="999c8-1470">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="999c8-1471">**paramètres régionaux**: entier non signé 32 bits indiquant les paramètres régionaux, tels que spécifiés dans \[ MS-GPSI \] annexe A, de la colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-1471">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="999c8-1472">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1472">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="999c8-1473">La structure CSynRestriction contient un mot ou ses synonymes pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1473">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="999c8-1474">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1474">0</span></span>

<span data-ttu-id="999c8-1475">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1475">1</span></span>

<span data-ttu-id="999c8-1476">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1476">2</span></span>

<span data-ttu-id="999c8-1477">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1477">3</span></span>

<span data-ttu-id="999c8-1478">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1478">4</span></span>

<span data-ttu-id="999c8-1479">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1479">5</span></span>

<span data-ttu-id="999c8-1480">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1480">6</span></span>

<span data-ttu-id="999c8-1481">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1481">7</span></span>

<span data-ttu-id="999c8-1482">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1482">8</span></span>

<span data-ttu-id="999c8-1483">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1483">9</span></span>

<span data-ttu-id="999c8-1484">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1484">1</span></span><br/> <span data-ttu-id="999c8-1485">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1485">0</span></span><br/>

<span data-ttu-id="999c8-1486">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1486">1</span></span>

<span data-ttu-id="999c8-1487">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1487">2</span></span>

<span data-ttu-id="999c8-1488">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1488">3</span></span>

<span data-ttu-id="999c8-1489">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1489">4</span></span>

<span data-ttu-id="999c8-1490">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1490">5</span></span>

<span data-ttu-id="999c8-1491">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1491">6</span></span>

<span data-ttu-id="999c8-1492">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1492">7</span></span>

<span data-ttu-id="999c8-1493">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1493">8</span></span>

<span data-ttu-id="999c8-1494">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1494">9</span></span>

<span data-ttu-id="999c8-1495">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1495">2</span></span><br/> <span data-ttu-id="999c8-1496">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1496">0</span></span><br/>

<span data-ttu-id="999c8-1497">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1497">1</span></span>

<span data-ttu-id="999c8-1498">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1498">2</span></span>

<span data-ttu-id="999c8-1499">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1499">3</span></span>

<span data-ttu-id="999c8-1500">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1500">4</span></span>

<span data-ttu-id="999c8-1501">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1501">5</span></span>

<span data-ttu-id="999c8-1502">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1502">6</span></span>

<span data-ttu-id="999c8-1503">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1503">7</span></span>

<span data-ttu-id="999c8-1504">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1504">8</span></span>

<span data-ttu-id="999c8-1505">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1505">9</span></span>

<span data-ttu-id="999c8-1506">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1506">3</span></span><br/> <span data-ttu-id="999c8-1507">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1507">0</span></span><br/>

<span data-ttu-id="999c8-1508">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1508">1</span></span>

<span data-ttu-id="999c8-1509">Restriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1509">Restriction</span></span>

<span data-ttu-id="999c8-1510">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1510">...</span></span>

<span data-ttu-id="999c8-1511">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1511">...</span></span>

<span data-ttu-id="999c8-1512">cKey</span><span class="sxs-lookup"><span data-stu-id="999c8-1512">cKey</span></span>

<span data-ttu-id="999c8-1513">\_keyarray (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1513">\_keyArray (variable)</span></span>

<span data-ttu-id="999c8-1514">\_isRange</span><span class="sxs-lookup"><span data-stu-id="999c8-1514">\_isRange</span></span>



 

<span data-ttu-id="999c8-1515">**Restriction**: structure COccRestriction spécifiant l’emplacement du mot.</span><span class="sxs-lookup"><span data-stu-id="999c8-1515">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="999c8-1516">**CKEY**: entier non signé 32 bits spécifiant le nombre d’éléments dans le tableau de \_ tableaux de la matrice.</span><span class="sxs-lookup"><span data-stu-id="999c8-1516">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="999c8-1517">**\_ keyarray**: tableau de structures CKey spécifiant un mot et ses synonymes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1517">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="999c8-1518">**\_ isRange**: si la valeur est 0x01, les clés sont des préfixes à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="999c8-1518">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="999c8-1519">Si la valeur est 0x00, les clés sont des valeurs exactes à mettre en correspondance.</span><span class="sxs-lookup"><span data-stu-id="999c8-1519">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="999c8-1520">\_isRange ne doit avoir aucune autre valeur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1520">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="999c8-1521">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1521">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="999c8-1522">La structure CVectorRestriction contient une opération pondérée sur un nœud d’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1522">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="999c8-1523">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1523">0</span></span>

<span data-ttu-id="999c8-1524">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1524">1</span></span>

<span data-ttu-id="999c8-1525">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1525">2</span></span>

<span data-ttu-id="999c8-1526">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1526">3</span></span>

<span data-ttu-id="999c8-1527">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1527">4</span></span>

<span data-ttu-id="999c8-1528">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1528">5</span></span>

<span data-ttu-id="999c8-1529">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1529">6</span></span>

<span data-ttu-id="999c8-1530">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1530">7</span></span>

<span data-ttu-id="999c8-1531">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1531">8</span></span>

<span data-ttu-id="999c8-1532">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1532">9</span></span>

<span data-ttu-id="999c8-1533">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1533">1</span></span><br/> <span data-ttu-id="999c8-1534">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1534">0</span></span><br/>

<span data-ttu-id="999c8-1535">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1535">1</span></span>

<span data-ttu-id="999c8-1536">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1536">2</span></span>

<span data-ttu-id="999c8-1537">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1537">3</span></span>

<span data-ttu-id="999c8-1538">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1538">4</span></span>

<span data-ttu-id="999c8-1539">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1539">5</span></span>

<span data-ttu-id="999c8-1540">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1540">6</span></span>

<span data-ttu-id="999c8-1541">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1541">7</span></span>

<span data-ttu-id="999c8-1542">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1542">8</span></span>

<span data-ttu-id="999c8-1543">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1543">9</span></span>

<span data-ttu-id="999c8-1544">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1544">2</span></span><br/> <span data-ttu-id="999c8-1545">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1545">0</span></span><br/>

<span data-ttu-id="999c8-1546">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1546">1</span></span>

<span data-ttu-id="999c8-1547">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1547">2</span></span>

<span data-ttu-id="999c8-1548">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1548">3</span></span>

<span data-ttu-id="999c8-1549">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1549">4</span></span>

<span data-ttu-id="999c8-1550">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1550">5</span></span>

<span data-ttu-id="999c8-1551">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1551">6</span></span>

<span data-ttu-id="999c8-1552">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1552">7</span></span>

<span data-ttu-id="999c8-1553">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1553">8</span></span>

<span data-ttu-id="999c8-1554">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1554">9</span></span>

<span data-ttu-id="999c8-1555">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1555">3</span></span><br/> <span data-ttu-id="999c8-1556">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1556">0</span></span><br/>

<span data-ttu-id="999c8-1557">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1557">1</span></span>

<span data-ttu-id="999c8-1558">\_PRES (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1558">\_pres (variable)</span></span>

<span data-ttu-id="999c8-1559">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1559">...</span></span>

<span data-ttu-id="999c8-1560">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1560">\_padding (variable)</span></span>

<span data-ttu-id="999c8-1561">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="999c8-1561">\_ulRankMethod</span></span>



 

<span data-ttu-id="999c8-1562">**\_ pres**: arborescence de commandes CNodeRestriction sur laquelle un classement ou une opération doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="999c8-1562">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="999c8-1563">**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-1563">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="999c8-1564">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-1564">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="999c8-1565">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-1565">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="999c8-1566">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1566">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-1567">**\_ ulRankMethod**: entier non signé 32 bits spécifiant un algorithme de classement.</span><span class="sxs-lookup"><span data-stu-id="999c8-1567">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="999c8-1568">DOIT être défini sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1568">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="999c8-1569">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1569">Value</span></span>                            | <span data-ttu-id="999c8-1570">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1570">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="999c8-1571">Rang de vecteur \_ \_ min 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-1571">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="999c8-1572">Utilisez l’algorithme minimal \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-1572">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="999c8-1573">Nombre maximal de VECTEURs \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-1573">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="999c8-1574">Utilisez le nombre maximal d’algorithmes \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-1574">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="999c8-1575">VECTOR de \_ classement \_ interne 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-1575">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="999c8-1576">Utilisez l’algorithme de produit interne \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-1576">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="999c8-1577">\_0x00000003 de rang de vecteurs \_</span><span class="sxs-lookup"><span data-stu-id="999c8-1577">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="999c8-1578">Utiliser l’algorithme de coefficient \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-1578">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="999c8-1579">Classement de vecteur \_ \_ Jaccard 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1579">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="999c8-1580">Utilisez l’algorithme de coefficient Jaccard \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-1580">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="999c8-1581">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1581">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="999c8-1582">La structure CWordRestriction contient un mot pour une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1582">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="999c8-1583">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1583">0</span></span>

<span data-ttu-id="999c8-1584">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1584">1</span></span>

<span data-ttu-id="999c8-1585">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1585">2</span></span>

<span data-ttu-id="999c8-1586">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1586">3</span></span>

<span data-ttu-id="999c8-1587">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1587">4</span></span>

<span data-ttu-id="999c8-1588">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1588">5</span></span>

<span data-ttu-id="999c8-1589">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1589">6</span></span>

<span data-ttu-id="999c8-1590">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1590">7</span></span>

<span data-ttu-id="999c8-1591">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1591">8</span></span>

<span data-ttu-id="999c8-1592">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1592">9</span></span>

<span data-ttu-id="999c8-1593">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1593">1</span></span><br/> <span data-ttu-id="999c8-1594">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1594">0</span></span><br/>

<span data-ttu-id="999c8-1595">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1595">1</span></span>

<span data-ttu-id="999c8-1596">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1596">2</span></span>

<span data-ttu-id="999c8-1597">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1597">3</span></span>

<span data-ttu-id="999c8-1598">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1598">4</span></span>

<span data-ttu-id="999c8-1599">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1599">5</span></span>

<span data-ttu-id="999c8-1600">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1600">6</span></span>

<span data-ttu-id="999c8-1601">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1601">7</span></span>

<span data-ttu-id="999c8-1602">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1602">8</span></span>

<span data-ttu-id="999c8-1603">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1603">9</span></span>

<span data-ttu-id="999c8-1604">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1604">2</span></span><br/> <span data-ttu-id="999c8-1605">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1605">0</span></span><br/>

<span data-ttu-id="999c8-1606">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1606">1</span></span>

<span data-ttu-id="999c8-1607">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1607">2</span></span>

<span data-ttu-id="999c8-1608">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1608">3</span></span>

<span data-ttu-id="999c8-1609">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1609">4</span></span>

<span data-ttu-id="999c8-1610">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1610">5</span></span>

<span data-ttu-id="999c8-1611">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1611">6</span></span>

<span data-ttu-id="999c8-1612">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1612">7</span></span>

<span data-ttu-id="999c8-1613">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1613">8</span></span>

<span data-ttu-id="999c8-1614">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1614">9</span></span>

<span data-ttu-id="999c8-1615">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1615">3</span></span><br/> <span data-ttu-id="999c8-1616">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1616">0</span></span><br/>

<span data-ttu-id="999c8-1617">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1617">1</span></span>

<span data-ttu-id="999c8-1618">restriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1618">restriction</span></span>

<span data-ttu-id="999c8-1619">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1619">...</span></span>

<span data-ttu-id="999c8-1620">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1620">...</span></span>

<span data-ttu-id="999c8-1621">\_clé (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1621">\_key (variable)</span></span>

<span data-ttu-id="999c8-1622">\_isRange</span><span class="sxs-lookup"><span data-stu-id="999c8-1622">\_isRange</span></span>



 

<span data-ttu-id="999c8-1623">**restriction**: structure COccRestriction spécifiant l’emplacement du mot.</span><span class="sxs-lookup"><span data-stu-id="999c8-1623">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="999c8-1624">**\_ clé**: une structure CKey spécifiant un mot.</span><span class="sxs-lookup"><span data-stu-id="999c8-1624">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="999c8-1625">**\_ isRange**: si la valeur est 0x01, la clé est un préfixe à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="999c8-1625">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="999c8-1626">Si la valeur est 0x00, la clé est une valeur exacte à mettre en correspondance.</span><span class="sxs-lookup"><span data-stu-id="999c8-1626">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="999c8-1627">\_isRange ne doit pas être défini sur une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1627">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="999c8-1628">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1628">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="999c8-1629">La structure CRestriction contient un nœud d’une arborescence de commandes de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1629">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="999c8-1630">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1630">0</span></span>

<span data-ttu-id="999c8-1631">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1631">1</span></span>

<span data-ttu-id="999c8-1632">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1632">2</span></span>

<span data-ttu-id="999c8-1633">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1633">3</span></span>

<span data-ttu-id="999c8-1634">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1634">4</span></span>

<span data-ttu-id="999c8-1635">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1635">5</span></span>

<span data-ttu-id="999c8-1636">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1636">6</span></span>

<span data-ttu-id="999c8-1637">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1637">7</span></span>

<span data-ttu-id="999c8-1638">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1638">8</span></span>

<span data-ttu-id="999c8-1639">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1639">9</span></span>

<span data-ttu-id="999c8-1640">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1640">1</span></span><br/> <span data-ttu-id="999c8-1641">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1641">0</span></span><br/>

<span data-ttu-id="999c8-1642">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1642">1</span></span>

<span data-ttu-id="999c8-1643">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1643">2</span></span>

<span data-ttu-id="999c8-1644">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1644">3</span></span>

<span data-ttu-id="999c8-1645">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1645">4</span></span>

<span data-ttu-id="999c8-1646">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1646">5</span></span>

<span data-ttu-id="999c8-1647">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1647">6</span></span>

<span data-ttu-id="999c8-1648">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1648">7</span></span>

<span data-ttu-id="999c8-1649">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1649">8</span></span>

<span data-ttu-id="999c8-1650">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1650">9</span></span>

<span data-ttu-id="999c8-1651">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1651">2</span></span><br/> <span data-ttu-id="999c8-1652">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1652">0</span></span><br/>

<span data-ttu-id="999c8-1653">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1653">1</span></span>

<span data-ttu-id="999c8-1654">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1654">2</span></span>

<span data-ttu-id="999c8-1655">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1655">3</span></span>

<span data-ttu-id="999c8-1656">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1656">4</span></span>

<span data-ttu-id="999c8-1657">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1657">5</span></span>

<span data-ttu-id="999c8-1658">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1658">6</span></span>

<span data-ttu-id="999c8-1659">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1659">7</span></span>

<span data-ttu-id="999c8-1660">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1660">8</span></span>

<span data-ttu-id="999c8-1661">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1661">9</span></span>

<span data-ttu-id="999c8-1662">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1662">3</span></span><br/> <span data-ttu-id="999c8-1663">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1663">0</span></span><br/>

<span data-ttu-id="999c8-1664">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1664">1</span></span>

<span data-ttu-id="999c8-1665">\_ulType</span><span class="sxs-lookup"><span data-stu-id="999c8-1665">\_ulType</span></span>

<span data-ttu-id="999c8-1666">Poids</span><span class="sxs-lookup"><span data-stu-id="999c8-1666">Weight</span></span>

<span data-ttu-id="999c8-1667">Restriction</span><span class="sxs-lookup"><span data-stu-id="999c8-1667">Restriction</span></span>



 

<span data-ttu-id="999c8-1668">**\_ ulType**: entier non signé 32 bits indiquant le type de restriction utilisé pour le nœud de l’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1668">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="999c8-1669">DOIT être défini sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1669">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="999c8-1670">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1670">Value</span></span>                    | <span data-ttu-id="999c8-1671">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1671">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1672">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-1672">RTNone 0x00000000</span></span>        | <span data-ttu-id="999c8-1673">Le nœud représente un mot parasite dans une requête de vecteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1673">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="999c8-1674">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-1674">RTAnd 0x00000001</span></span>         | <span data-ttu-id="999c8-1675">Le nœud contient un CNodeRestriction sur lequel une opération logique AND doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-1675">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="999c8-1676">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-1676">RTOr 0x00000002</span></span>          | <span data-ttu-id="999c8-1677">Le nœud contient un CNodeRestriction sur lequel une opération OR logique doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-1677">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="999c8-1678">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-1678">RTNot 0x00000003</span></span>         | <span data-ttu-id="999c8-1679">Le nœud contient un CRestriction sur lequel une opération NOT doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-1679">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="999c8-1680">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1680">RTContent 0x00000004</span></span>     | <span data-ttu-id="999c8-1681">Le nœud contient un CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1681">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="999c8-1682">RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="999c8-1682">RTProperty 0x00000005</span></span>    | <span data-ttu-id="999c8-1683">Le nœud contient un CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1683">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="999c8-1684">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="999c8-1684">RTProximity 0x00000006</span></span>   | <span data-ttu-id="999c8-1685">Le nœud contient un CNodeRestriction sur lequel un classement de proximité doit être effectué,</span><span class="sxs-lookup"><span data-stu-id="999c8-1685">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="999c8-1686">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="999c8-1686">RTVector 0x00000007</span></span>      | <span data-ttu-id="999c8-1687">Le nœud contient un CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1687">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="999c8-1688">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="999c8-1688">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="999c8-1689">Le nœud contient un CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1689">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="999c8-1690">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="999c8-1690">RTScope 0x00000009</span></span>       | <span data-ttu-id="999c8-1691">Le nœud contient un CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1691">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="999c8-1692">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="999c8-1692">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="999c8-1693">Le nœud contient un CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1693">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="999c8-1694">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="999c8-1694">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="999c8-1695">Le nœud contient un CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1695">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="999c8-1696">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="999c8-1696">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="999c8-1697">Le nœud contient un CNodeRestriction sur lequel une expression de correspondance doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-1697">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="999c8-1698">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="999c8-1698">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="999c8-1699">Le nœud contient un CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1699">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="999c8-1700">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="999c8-1700">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="999c8-1701">Le nœud contient un CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-1701">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="999c8-1702">**Weight**: entier non signé 32 bits représentant le poids du nœud.</span><span class="sxs-lookup"><span data-stu-id="999c8-1702">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="999c8-1703">Weight indique l’importance du nœud par rapport aux autres nœuds de l’arborescence de commandes de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1703">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="999c8-1704">Les valeurs de pondération supérieure sont plus importantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1704">Higher weight values are more important.</span></span>

<span data-ttu-id="999c8-1705">**Restriction**: type de restriction pour le nœud de l’arborescence de commandes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1705">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="999c8-1706">La syntaxe doit être la même que celle indiquée par le \_ champ ulType.</span><span class="sxs-lookup"><span data-stu-id="999c8-1706">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="999c8-1707">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="999c8-1707">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="999c8-1708">La structure CColumnSet spécifie les numéros de colonne à retourner.</span><span class="sxs-lookup"><span data-stu-id="999c8-1708">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="999c8-1709">Cette structure est toujours utilisée en référence à une structure CPidMapper spécifique (section 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="999c8-1709">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="999c8-1710">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1710">0</span></span>

<span data-ttu-id="999c8-1711">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1711">1</span></span>

<span data-ttu-id="999c8-1712">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1712">2</span></span>

<span data-ttu-id="999c8-1713">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1713">3</span></span>

<span data-ttu-id="999c8-1714">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1714">4</span></span>

<span data-ttu-id="999c8-1715">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1715">5</span></span>

<span data-ttu-id="999c8-1716">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1716">6</span></span>

<span data-ttu-id="999c8-1717">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1717">7</span></span>

<span data-ttu-id="999c8-1718">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1718">8</span></span>

<span data-ttu-id="999c8-1719">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1719">9</span></span>

<span data-ttu-id="999c8-1720">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1720">1</span></span><br/> <span data-ttu-id="999c8-1721">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1721">0</span></span><br/>

<span data-ttu-id="999c8-1722">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1722">1</span></span>

<span data-ttu-id="999c8-1723">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1723">2</span></span>

<span data-ttu-id="999c8-1724">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1724">3</span></span>

<span data-ttu-id="999c8-1725">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1725">4</span></span>

<span data-ttu-id="999c8-1726">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1726">5</span></span>

<span data-ttu-id="999c8-1727">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1727">6</span></span>

<span data-ttu-id="999c8-1728">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1728">7</span></span>

<span data-ttu-id="999c8-1729">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1729">8</span></span>

<span data-ttu-id="999c8-1730">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1730">9</span></span>

<span data-ttu-id="999c8-1731">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1731">2</span></span><br/> <span data-ttu-id="999c8-1732">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1732">0</span></span><br/>

<span data-ttu-id="999c8-1733">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1733">1</span></span>

<span data-ttu-id="999c8-1734">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1734">2</span></span>

<span data-ttu-id="999c8-1735">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1735">3</span></span>

<span data-ttu-id="999c8-1736">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1736">4</span></span>

<span data-ttu-id="999c8-1737">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1737">5</span></span>

<span data-ttu-id="999c8-1738">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1738">6</span></span>

<span data-ttu-id="999c8-1739">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1739">7</span></span>

<span data-ttu-id="999c8-1740">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1740">8</span></span>

<span data-ttu-id="999c8-1741">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1741">9</span></span>

<span data-ttu-id="999c8-1742">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1742">3</span></span><br/> <span data-ttu-id="999c8-1743">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1743">0</span></span><br/>

<span data-ttu-id="999c8-1744">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1744">1</span></span>

<span data-ttu-id="999c8-1745">count</span><span class="sxs-lookup"><span data-stu-id="999c8-1745">count</span></span>

<span data-ttu-id="999c8-1746">index (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1746">indexes (variable)</span></span>



 

<span data-ttu-id="999c8-1747">**Count**: entier non signé 32 bits spécifiant le nombre d’éléments dans le tableau d’index.</span><span class="sxs-lookup"><span data-stu-id="999c8-1747">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="999c8-1748">**index**: tableau d’entiers non signés de 4 octets représentant les index de base zéro dans le tableau aPropSpec de la structure CPidMapper correspondante.</span><span class="sxs-lookup"><span data-stu-id="999c8-1748">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="999c8-1749">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="999c8-1749">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="999c8-1750">La structure CCategorizationSet contient des informations sur le regroupement d’un jeu de résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1750">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="999c8-1751">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1751">0</span></span>

<span data-ttu-id="999c8-1752">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1752">1</span></span>

<span data-ttu-id="999c8-1753">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1753">2</span></span>

<span data-ttu-id="999c8-1754">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1754">3</span></span>

<span data-ttu-id="999c8-1755">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1755">4</span></span>

<span data-ttu-id="999c8-1756">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1756">5</span></span>

<span data-ttu-id="999c8-1757">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1757">6</span></span>

<span data-ttu-id="999c8-1758">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1758">7</span></span>

<span data-ttu-id="999c8-1759">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1759">8</span></span>

<span data-ttu-id="999c8-1760">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1760">9</span></span>

<span data-ttu-id="999c8-1761">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1761">1</span></span><br/> <span data-ttu-id="999c8-1762">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1762">0</span></span><br/>

<span data-ttu-id="999c8-1763">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1763">1</span></span>

<span data-ttu-id="999c8-1764">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1764">2</span></span>

<span data-ttu-id="999c8-1765">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1765">3</span></span>

<span data-ttu-id="999c8-1766">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1766">4</span></span>

<span data-ttu-id="999c8-1767">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1767">5</span></span>

<span data-ttu-id="999c8-1768">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1768">6</span></span>

<span data-ttu-id="999c8-1769">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1769">7</span></span>

<span data-ttu-id="999c8-1770">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1770">8</span></span>

<span data-ttu-id="999c8-1771">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1771">9</span></span>

<span data-ttu-id="999c8-1772">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1772">2</span></span><br/> <span data-ttu-id="999c8-1773">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1773">0</span></span><br/>

<span data-ttu-id="999c8-1774">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1774">1</span></span>

<span data-ttu-id="999c8-1775">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1775">2</span></span>

<span data-ttu-id="999c8-1776">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1776">3</span></span>

<span data-ttu-id="999c8-1777">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1777">4</span></span>

<span data-ttu-id="999c8-1778">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1778">5</span></span>

<span data-ttu-id="999c8-1779">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1779">6</span></span>

<span data-ttu-id="999c8-1780">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1780">7</span></span>

<span data-ttu-id="999c8-1781">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1781">8</span></span>

<span data-ttu-id="999c8-1782">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1782">9</span></span>

<span data-ttu-id="999c8-1783">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1783">3</span></span><br/> <span data-ttu-id="999c8-1784">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1784">0</span></span><br/>

<span data-ttu-id="999c8-1785">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1785">1</span></span>

<span data-ttu-id="999c8-1786">count</span><span class="sxs-lookup"><span data-stu-id="999c8-1786">count</span></span>

<span data-ttu-id="999c8-1787">catégories (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1787">categories (variable)</span></span>



 

<span data-ttu-id="999c8-1788">**Count**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau des catégories.</span><span class="sxs-lookup"><span data-stu-id="999c8-1788">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="999c8-1789">**categories**: tableau de structures CCategorizationSpec spécifiant le regroupement de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1789">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="999c8-1790">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-1790">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="999c8-1791">La structure CCategorizationSpec contient un regroupement pour un jeu de résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1791">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="999c8-1792">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1792">0</span></span>

<span data-ttu-id="999c8-1793">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1793">1</span></span>

<span data-ttu-id="999c8-1794">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1794">2</span></span>

<span data-ttu-id="999c8-1795">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1795">3</span></span>

<span data-ttu-id="999c8-1796">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1796">4</span></span>

<span data-ttu-id="999c8-1797">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1797">5</span></span>

<span data-ttu-id="999c8-1798">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1798">6</span></span>

<span data-ttu-id="999c8-1799">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1799">7</span></span>

<span data-ttu-id="999c8-1800">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1800">8</span></span>

<span data-ttu-id="999c8-1801">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1801">9</span></span>

<span data-ttu-id="999c8-1802">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1802">1</span></span><br/> <span data-ttu-id="999c8-1803">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1803">0</span></span><br/>

<span data-ttu-id="999c8-1804">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1804">1</span></span>

<span data-ttu-id="999c8-1805">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1805">2</span></span>

<span data-ttu-id="999c8-1806">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1806">3</span></span>

<span data-ttu-id="999c8-1807">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1807">4</span></span>

<span data-ttu-id="999c8-1808">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1808">5</span></span>

<span data-ttu-id="999c8-1809">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1809">6</span></span>

<span data-ttu-id="999c8-1810">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1810">7</span></span>

<span data-ttu-id="999c8-1811">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1811">8</span></span>

<span data-ttu-id="999c8-1812">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1812">9</span></span>

<span data-ttu-id="999c8-1813">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1813">2</span></span><br/> <span data-ttu-id="999c8-1814">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1814">0</span></span><br/>

<span data-ttu-id="999c8-1815">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1815">1</span></span>

<span data-ttu-id="999c8-1816">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1816">2</span></span>

<span data-ttu-id="999c8-1817">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1817">3</span></span>

<span data-ttu-id="999c8-1818">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1818">4</span></span>

<span data-ttu-id="999c8-1819">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1819">5</span></span>

<span data-ttu-id="999c8-1820">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1820">6</span></span>

<span data-ttu-id="999c8-1821">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1821">7</span></span>

<span data-ttu-id="999c8-1822">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1822">8</span></span>

<span data-ttu-id="999c8-1823">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1823">9</span></span>

<span data-ttu-id="999c8-1824">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1824">3</span></span><br/> <span data-ttu-id="999c8-1825">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1825">0</span></span><br/>

<span data-ttu-id="999c8-1826">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1826">1</span></span>

<span data-ttu-id="999c8-1827">\_csColumns (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1827">\_csColumns (variable)</span></span>

<span data-ttu-id="999c8-1828">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="999c8-1828">\_ulCategType</span></span>



 

<span data-ttu-id="999c8-1829">**\_ csColumns**: structure CColumnSet indiquant les colonnes selon lesquelles regrouper la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1829">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="999c8-1830">**\_ ulCategType**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-1830">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-1831">DOIT être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-1831">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="999c8-1832">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="999c8-1832">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="999c8-1833">La structure CDbColId contient une colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-1833">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="999c8-1834">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1834">0</span></span>

<span data-ttu-id="999c8-1835">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1835">1</span></span>

<span data-ttu-id="999c8-1836">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1836">2</span></span>

<span data-ttu-id="999c8-1837">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1837">3</span></span>

<span data-ttu-id="999c8-1838">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1838">4</span></span>

<span data-ttu-id="999c8-1839">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1839">5</span></span>

<span data-ttu-id="999c8-1840">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1840">6</span></span>

<span data-ttu-id="999c8-1841">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1841">7</span></span>

<span data-ttu-id="999c8-1842">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1842">8</span></span>

<span data-ttu-id="999c8-1843">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1843">9</span></span>

<span data-ttu-id="999c8-1844">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1844">1</span></span><br/> <span data-ttu-id="999c8-1845">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1845">0</span></span><br/>

<span data-ttu-id="999c8-1846">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1846">1</span></span>

<span data-ttu-id="999c8-1847">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1847">2</span></span>

<span data-ttu-id="999c8-1848">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1848">3</span></span>

<span data-ttu-id="999c8-1849">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1849">4</span></span>

<span data-ttu-id="999c8-1850">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1850">5</span></span>

<span data-ttu-id="999c8-1851">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1851">6</span></span>

<span data-ttu-id="999c8-1852">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1852">7</span></span>

<span data-ttu-id="999c8-1853">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1853">8</span></span>

<span data-ttu-id="999c8-1854">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1854">9</span></span>

<span data-ttu-id="999c8-1855">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1855">2</span></span><br/> <span data-ttu-id="999c8-1856">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1856">0</span></span><br/>

<span data-ttu-id="999c8-1857">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1857">1</span></span>

<span data-ttu-id="999c8-1858">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1858">2</span></span>

<span data-ttu-id="999c8-1859">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1859">3</span></span>

<span data-ttu-id="999c8-1860">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1860">4</span></span>

<span data-ttu-id="999c8-1861">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1861">5</span></span>

<span data-ttu-id="999c8-1862">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1862">6</span></span>

<span data-ttu-id="999c8-1863">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1863">7</span></span>

<span data-ttu-id="999c8-1864">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1864">8</span></span>

<span data-ttu-id="999c8-1865">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1865">9</span></span>

<span data-ttu-id="999c8-1866">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1866">3</span></span><br/> <span data-ttu-id="999c8-1867">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1867">0</span></span><br/>

<span data-ttu-id="999c8-1868">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1868">1</span></span>

<span data-ttu-id="999c8-1869">eKind</span><span class="sxs-lookup"><span data-stu-id="999c8-1869">eKind</span></span>

<span data-ttu-id="999c8-1870">GUID</span><span class="sxs-lookup"><span data-stu-id="999c8-1870">GUID</span></span>

<span data-ttu-id="999c8-1871">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1871">...</span></span>

<span data-ttu-id="999c8-1872">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1872">...</span></span>

<span data-ttu-id="999c8-1873">...</span><span class="sxs-lookup"><span data-stu-id="999c8-1873">...</span></span>

<span data-ttu-id="999c8-1874">ulId</span><span class="sxs-lookup"><span data-stu-id="999c8-1874">ulId</span></span>

<span data-ttu-id="999c8-1875">vString (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1875">vString (variable)</span></span>



 

<span data-ttu-id="999c8-1876">**eKind**: doit être défini sur l’une des valeurs ci-dessous qui indique le contenu de GUID et vValue.</span><span class="sxs-lookup"><span data-stu-id="999c8-1876">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="999c8-1877">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1877">Value</span></span>                            | <span data-ttu-id="999c8-1878">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1878">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1879">\_Nom GUID \_ 0x00000000 DBKIND</span><span class="sxs-lookup"><span data-stu-id="999c8-1879">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="999c8-1880">vString contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1880">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="999c8-1881">\_GUID DBKIND \_ propid 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-1881">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="999c8-1882">ulId contient un entier de 4 octets indiquant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1882">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="999c8-1883">Nom de DBKIND \_ PGUID \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-1883">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="999c8-1884">vString contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1884">vString contains a property name.</span></span> <span data-ttu-id="999c8-1885">Cette valeur doit être traitée de la même façon que le \_ nom GUID DBKIND \_ .</span><span class="sxs-lookup"><span data-stu-id="999c8-1885">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="999c8-1886">DBKIND \_ PGUID \_ propid 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1886">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="999c8-1887">ulId contient un entier de 4 octets indiquant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1887">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="999c8-1888">Cette valeur doit être identique à DBKIND \_ GUID \_ propid.</span><span class="sxs-lookup"><span data-stu-id="999c8-1888">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="999c8-1889">**GUID**: le GUID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1889">**GUID**: The property GUID.</span></span>

<span data-ttu-id="999c8-1890">**ulId**: si EKIND est DBKIND \_ GUID \_ propid ou DBKIND \_ PGUID \_ propId, ce champ contient un entier non signé, en spécifiant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1890">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="999c8-1891">Si eKind est \_ \_ un nom GUID DBKIND ou \_ \_ un nom DBKIND PGUID, ce champ contient un entier non signé spécifiant le nombre de caractères Unicode contenus dans le champ vString.</span><span class="sxs-lookup"><span data-stu-id="999c8-1891">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="999c8-1892">**vString**: chaîne Unicode qui se termine par un caractère non null représentant le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1892">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="999c8-1893">Elle doit être omise sauf si le champ eKind est défini sur DBKIND \_ GUID \_ Name ou DBKIND \_ PGUID \_ Name.</span><span class="sxs-lookup"><span data-stu-id="999c8-1893">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="999c8-1894">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="999c8-1894">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="999c8-1895">La structure CDbProp contient une propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1895">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="999c8-1896">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1896">0</span></span>

<span data-ttu-id="999c8-1897">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1897">1</span></span>

<span data-ttu-id="999c8-1898">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1898">2</span></span>

<span data-ttu-id="999c8-1899">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1899">3</span></span>

<span data-ttu-id="999c8-1900">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1900">4</span></span>

<span data-ttu-id="999c8-1901">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1901">5</span></span>

<span data-ttu-id="999c8-1902">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1902">6</span></span>

<span data-ttu-id="999c8-1903">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1903">7</span></span>

<span data-ttu-id="999c8-1904">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1904">8</span></span>

<span data-ttu-id="999c8-1905">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1905">9</span></span>

<span data-ttu-id="999c8-1906">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1906">1</span></span><br/> <span data-ttu-id="999c8-1907">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1907">0</span></span><br/>

<span data-ttu-id="999c8-1908">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1908">1</span></span>

<span data-ttu-id="999c8-1909">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1909">2</span></span>

<span data-ttu-id="999c8-1910">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1910">3</span></span>

<span data-ttu-id="999c8-1911">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1911">4</span></span>

<span data-ttu-id="999c8-1912">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1912">5</span></span>

<span data-ttu-id="999c8-1913">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1913">6</span></span>

<span data-ttu-id="999c8-1914">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1914">7</span></span>

<span data-ttu-id="999c8-1915">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1915">8</span></span>

<span data-ttu-id="999c8-1916">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1916">9</span></span>

<span data-ttu-id="999c8-1917">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1917">2</span></span><br/> <span data-ttu-id="999c8-1918">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1918">0</span></span><br/>

<span data-ttu-id="999c8-1919">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1919">1</span></span>

<span data-ttu-id="999c8-1920">2</span><span class="sxs-lookup"><span data-stu-id="999c8-1920">2</span></span>

<span data-ttu-id="999c8-1921">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1921">3</span></span>

<span data-ttu-id="999c8-1922">4</span><span class="sxs-lookup"><span data-stu-id="999c8-1922">4</span></span>

<span data-ttu-id="999c8-1923">5</span><span class="sxs-lookup"><span data-stu-id="999c8-1923">5</span></span>

<span data-ttu-id="999c8-1924">6</span><span class="sxs-lookup"><span data-stu-id="999c8-1924">6</span></span>

<span data-ttu-id="999c8-1925">7</span><span class="sxs-lookup"><span data-stu-id="999c8-1925">7</span></span>

<span data-ttu-id="999c8-1926">8</span><span class="sxs-lookup"><span data-stu-id="999c8-1926">8</span></span>

<span data-ttu-id="999c8-1927">9</span><span class="sxs-lookup"><span data-stu-id="999c8-1927">9</span></span>

<span data-ttu-id="999c8-1928">3</span><span class="sxs-lookup"><span data-stu-id="999c8-1928">3</span></span><br/> <span data-ttu-id="999c8-1929">0</span><span class="sxs-lookup"><span data-stu-id="999c8-1929">0</span></span><br/>

<span data-ttu-id="999c8-1930">1</span><span class="sxs-lookup"><span data-stu-id="999c8-1930">1</span></span>

<span data-ttu-id="999c8-1931">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="999c8-1931">DBPROPID</span></span>

<span data-ttu-id="999c8-1932">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="999c8-1932">DBPROPOPTIONS</span></span>

<span data-ttu-id="999c8-1933">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="999c8-1933">DBPROPSTATUS</span></span>

<span data-ttu-id="999c8-1934">colid (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1934">colid (variable)</span></span>

<span data-ttu-id="999c8-1935">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-1935">vValue (variable)</span></span>



 

<span data-ttu-id="999c8-1936">**DBPROPID**: entier non signé 32 bits indiquant l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1936">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="999c8-1937">**DBPROPOPTIONS** : doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-1937">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="999c8-1938">**DBPROPSTATUS**: doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-1938">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="999c8-1939">**colid**: une structure CDbColId, comme indiqué dans la section 2.2.1.20, indiquant la colonne à laquelle la propriété s’applique.</span><span class="sxs-lookup"><span data-stu-id="999c8-1939">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="999c8-1940">**vValue**: CBaseStorageVariant contenant la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-1940">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="999c8-1941">Propriétés 2.2.1.21.1</span><span class="sxs-lookup"><span data-stu-id="999c8-1941">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="999c8-1942">Cette section détaille les propriétés utilisées par CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-1942">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="999c8-1943">Ces propriétés sont regroupées en trois jeux de propriétés, ident 2.2.1.21.1 ified dans le champ guidPropertySet de la structure CDbPropSet (section 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="999c8-1943">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="999c8-1944">Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés DBPROPSET FSCIFRMWRK \_ ext.</span><span class="sxs-lookup"><span data-stu-id="999c8-1944">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="999c8-1945">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1945">Value</span></span>                                  | <span data-ttu-id="999c8-1946">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1946">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1947">\_Nom de \_ catalogue ci DBPROP \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-1947">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="999c8-1948">Spécifie le nom du catalogue ou des catalogues à interroger.</span><span class="sxs-lookup"><span data-stu-id="999c8-1948">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="999c8-1949">La valeur doit être un \_ LPWStr VT ou un \_ LPWStr VT Vector \| VT \_</span><span class="sxs-lookup"><span data-stu-id="999c8-1949">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="999c8-1950">DBPROP \_ ci \_ inclut des \_ étendues 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-1950">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="999c8-1951">Spécifie un ou plusieurs chemins d’accès à inclure dans la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1951">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="999c8-1952">La valeur doit être un \_ LPWStr VT ou un \_ LPWStr VT Vector \| VT \_ .</span><span class="sxs-lookup"><span data-stu-id="999c8-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="999c8-1953">Indicateurs d’étendue de l’élément de configuration DBPROP \_ \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1953">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="999c8-1954">Spécifie comment les chemins d’accès spécifiés par la \_ propriété DBPROP ci \_ include \_ scope doivent être traités.</span><span class="sxs-lookup"><span data-stu-id="999c8-1954">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="999c8-1955">La valeur doit être un \_ I4 VT ou un \_ vecteur VT VT \| \_ I4.</span><span class="sxs-lookup"><span data-stu-id="999c8-1955">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="999c8-1956">DBPROP \_ \_ type de requête ci \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="999c8-1956">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="999c8-1957">Spécifie le type de requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-1957">Specifies the type of query.</span></span> <span data-ttu-id="999c8-1958">CDbColId doit être défini sur DB \_ NULLID.</span><span class="sxs-lookup"><span data-stu-id="999c8-1958">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="999c8-1959">Le tableau suivant répertorie les indicateurs pour la \_ propriété indicateurs d’étendue d’DBPROP ci \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="999c8-1959">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="999c8-1960">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1960">Value</span></span>                     | <span data-ttu-id="999c8-1961">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1961">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1962">REQUÊTE \_ complète 0x01</span><span class="sxs-lookup"><span data-stu-id="999c8-1962">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="999c8-1963">Si cette valeur est définie, cela indique que les fichiers dans le répertoire d’étendue et tous les sous-répertoires sont inclus dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-1963">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="999c8-1964">Si cette case est désactivée, seuls les fichiers du répertoire d’étendue sont inclus dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-1964">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="999c8-1965">NE doit pas être combiné avec une requête \_ profonde.</span><span class="sxs-lookup"><span data-stu-id="999c8-1965">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="999c8-1966">\_ \_ Chemin d’accès virtuel de requête 0x02</span><span class="sxs-lookup"><span data-stu-id="999c8-1966">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="999c8-1967">S’il est défini, indique que l’étendue est un chemin d’accès virtuel.</span><span class="sxs-lookup"><span data-stu-id="999c8-1967">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="999c8-1968">Si cette case est désactivée, cela indique que l’étendue est un répertoire physique.</span><span class="sxs-lookup"><span data-stu-id="999c8-1968">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="999c8-1969">Le tableau suivant répertorie les types de requêtes pour \_ la \_ propriété type de requête DBPROP ci \_ :</span><span class="sxs-lookup"><span data-stu-id="999c8-1969">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="999c8-1970">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1970">Value</span></span>                     | <span data-ttu-id="999c8-1971">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1971">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1972">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-1972">CiNormal 0x00000000</span></span>       | <span data-ttu-id="999c8-1973">Requête normale.</span><span class="sxs-lookup"><span data-stu-id="999c8-1973">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="999c8-1974">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-1974">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="999c8-1975">La requête demande une liste des racines virtuelles du catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-1975">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="999c8-1976">Cette valeur requiert des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1976">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="999c8-1977">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-1977">CiProperties 0x00000003</span></span>   | <span data-ttu-id="999c8-1978">La requête demande une liste de toutes les propriétés prises en charge par le service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-1978">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="999c8-1979">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1979">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="999c8-1980">La requête est une opération d’administration.</span><span class="sxs-lookup"><span data-stu-id="999c8-1980">The query is an administrative operation.</span></span> <span data-ttu-id="999c8-1981">Cette valeur requiert des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="999c8-1981">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="999c8-1982">Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés QUERYEXT DBPROPSET.</span><span class="sxs-lookup"><span data-stu-id="999c8-1982">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="999c8-1983">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-1983">Value</span></span>                                      | <span data-ttu-id="999c8-1984">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-1984">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-1985">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-1985">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="999c8-1986">Spécifie la manière dont le service d’indexation gère les requêtes lentes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1986">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="999c8-1987">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-1987">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="999c8-1988">Si la valeur est TRUE, le serveur est autorisé à faire échouer ces requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1988">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="999c8-1989">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-1989">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="999c8-1990">Indique si le service d’indexation doit effectuer la suppression des résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-1990">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="999c8-1991">Si la valeur est TRUE, le serveur doit envisager d’effectuer une suppression des résultats de manière à optimiser le temps de réponse pour le client.</span><span class="sxs-lookup"><span data-stu-id="999c8-1991">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="999c8-1992">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-1992">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="999c8-1993">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-1993">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="999c8-1994">Indique si le client prend en charge les \_ types de données vectorielles VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-1994">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="999c8-1995">Si la valeur est TRUE, le client prend en charge VT \_ Vector ; si la valeur est false, le serveur doit convertir les \_ types de données de Vector VT en \_ types de données de tableau VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-1995">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="999c8-1996">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-1996">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="999c8-1997">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="999c8-1997">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="999c8-1998">Indique que les lignes correspondent à retourner.</span><span class="sxs-lookup"><span data-stu-id="999c8-1998">Indicates the row matches to return.</span></span> <span data-ttu-id="999c8-1999">Si la valeur est TRUE, le serveur doit retourner le premier ensemble de lignes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-1999">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="999c8-2000">Si la valeur est FALSe, les lignes les plus pertinentes doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="999c8-2000">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="999c8-2001">La valeur doit être un \_ booléen VT.</span><span class="sxs-lookup"><span data-stu-id="999c8-2001">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="999c8-2002">Le tableau suivant répertorie les propriétés qui font partie du \_ jeu de propriétés DBPROPSET CIFRMWRKCORE \_ ext.</span><span class="sxs-lookup"><span data-stu-id="999c8-2002">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="999c8-2003">Valeur/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="999c8-2003">Value / DBPROPID</span></span>                 | <span data-ttu-id="999c8-2004">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2004">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-2005">\_Ordinateur DBPROP 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-2005">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="999c8-2006">Spécifie le nom du ou des ordinateurs sur lesquels une requête doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2006">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="999c8-2007">La valeur doit être VT \_ BSTR ou VT \_ array \| VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="999c8-2007">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="999c8-2008">DBPROP \_ client \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-2008">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="999c8-2009">Spécifie une constante de connexion pour le service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-2009">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="999c8-2010">La valeur doit être un \_ CLSID VT contenant 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="999c8-2010">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="999c8-2011">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="999c8-2011">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="999c8-2012">La structure CDbPropSet contient un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2012">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="999c8-2013">Notez que le premier champ est de taille fixe, mais peut ne pas être aligné sur un décalage qui est un multiple de 4 octets à partir du début du message contenant cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-2013">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="999c8-2014">Toutefois, le champ cProperties est aligné en tant que tel, et le format est donc représenté comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-2014">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="999c8-2015">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2015">0</span></span>

<span data-ttu-id="999c8-2016">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2016">1</span></span>

<span data-ttu-id="999c8-2017">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2017">2</span></span>

<span data-ttu-id="999c8-2018">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2018">3</span></span>

<span data-ttu-id="999c8-2019">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2019">4</span></span>

<span data-ttu-id="999c8-2020">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2020">5</span></span>

<span data-ttu-id="999c8-2021">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2021">6</span></span>

<span data-ttu-id="999c8-2022">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2022">7</span></span>

<span data-ttu-id="999c8-2023">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2023">8</span></span>

<span data-ttu-id="999c8-2024">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2024">9</span></span>

<span data-ttu-id="999c8-2025">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2025">1</span></span><br/> <span data-ttu-id="999c8-2026">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2026">0</span></span><br/>

<span data-ttu-id="999c8-2027">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2027">1</span></span>

<span data-ttu-id="999c8-2028">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2028">2</span></span>

<span data-ttu-id="999c8-2029">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2029">3</span></span>

<span data-ttu-id="999c8-2030">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2030">4</span></span>

<span data-ttu-id="999c8-2031">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2031">5</span></span>

<span data-ttu-id="999c8-2032">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2032">6</span></span>

<span data-ttu-id="999c8-2033">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2033">7</span></span>

<span data-ttu-id="999c8-2034">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2034">8</span></span>

<span data-ttu-id="999c8-2035">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2035">9</span></span>

<span data-ttu-id="999c8-2036">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2036">2</span></span><br/> <span data-ttu-id="999c8-2037">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2037">0</span></span><br/>

<span data-ttu-id="999c8-2038">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2038">1</span></span>

<span data-ttu-id="999c8-2039">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2039">2</span></span>

<span data-ttu-id="999c8-2040">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2040">3</span></span>

<span data-ttu-id="999c8-2041">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2041">4</span></span>

<span data-ttu-id="999c8-2042">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2042">5</span></span>

<span data-ttu-id="999c8-2043">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2043">6</span></span>

<span data-ttu-id="999c8-2044">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2044">7</span></span>

<span data-ttu-id="999c8-2045">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2045">8</span></span>

<span data-ttu-id="999c8-2046">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2046">9</span></span>

<span data-ttu-id="999c8-2047">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2047">3</span></span><br/> <span data-ttu-id="999c8-2048">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2048">0</span></span><br/>

<span data-ttu-id="999c8-2049">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2049">1</span></span>

<span data-ttu-id="999c8-2050">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="999c8-2050">guidPropertySet</span></span>

<span data-ttu-id="999c8-2051">...</span><span class="sxs-lookup"><span data-stu-id="999c8-2051">...</span></span>

<span data-ttu-id="999c8-2052">...</span><span class="sxs-lookup"><span data-stu-id="999c8-2052">...</span></span>

<span data-ttu-id="999c8-2053">...</span><span class="sxs-lookup"><span data-stu-id="999c8-2053">...</span></span>

<span data-ttu-id="999c8-2054">...</span><span class="sxs-lookup"><span data-stu-id="999c8-2054">...</span></span>

<span data-ttu-id="999c8-2055">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-2055">\_padding (variable)</span></span>

<span data-ttu-id="999c8-2056">cProperties</span><span class="sxs-lookup"><span data-stu-id="999c8-2056">cProperties</span></span>

<span data-ttu-id="999c8-2057">aProps (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-2057">aProps (variable)</span></span>



 

<span data-ttu-id="999c8-2058">**guidPropertySet**: GUID identifiant le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2058">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="999c8-2059">DOIT être défini sur la forme binaire correspondant à l’une des valeurs suivantes (affichées sous forme de représentation sous forme de chaîne), identifiant le jeu de propriétés des propriétés contenues dans le champ aProps.</span><span class="sxs-lookup"><span data-stu-id="999c8-2059">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="999c8-2060">Valeur/GUID</span><span class="sxs-lookup"><span data-stu-id="999c8-2060">Value / GUID</span></span>                                                                              | <span data-ttu-id="999c8-2061">Nom</span><span class="sxs-lookup"><span data-stu-id="999c8-2061">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="999c8-2062">DBPROPSET \_ FSCIFRMWRK \_ ext</span><span class="sxs-lookup"><span data-stu-id="999c8-2062">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="999c8-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="999c8-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="999c8-2064">Jeu de propriétés de l’infrastructure d’index de contenu du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="999c8-2064">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="999c8-2065">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="999c8-2065">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="999c8-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="999c8-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="999c8-2067">Jeu de propriétés d’extension de requête</span><span class="sxs-lookup"><span data-stu-id="999c8-2067">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="999c8-2068">DBPROPSET \_ CIFRMWRKCORE \_ ext</span><span class="sxs-lookup"><span data-stu-id="999c8-2068">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="999c8-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="999c8-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="999c8-2070">Jeu de propriétés principales de l’infrastructure d’index de contenu</span><span class="sxs-lookup"><span data-stu-id="999c8-2070">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="999c8-2071">**\_ remplissage**: la longueur de ce champ doit être comprise entre 0 et 3 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-2071">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="999c8-2072">La longueur de ce champ doit être telle que le champ suivant commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient cette structure.</span><span class="sxs-lookup"><span data-stu-id="999c8-2072">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="999c8-2073">Si ce champ est présent (c’est-à-dire une longueur différente de zéro), la valeur qu’il contient est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-2073">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="999c8-2074">Le contenu de ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-2074">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-2075">**cProperties**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau aProps.</span><span class="sxs-lookup"><span data-stu-id="999c8-2075">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="999c8-2076">**aProps**: tableau de structures CDbProp, tel que spécifié dans la section 0, contenant les propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2076">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="999c8-2077">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure commence à un décalage qui est un multiple de 4 octets à partir du début du message qui contient ce tableau.</span><span class="sxs-lookup"><span data-stu-id="999c8-2077">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="999c8-2078">Si des octets de remplissage sont présents, la valeur qu’ils contiennent est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-2078">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="999c8-2079">Le contenu des octets de remplissage doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-2079">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="999c8-2080">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="999c8-2080">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="999c8-2081">La structure CPidMapper contient un tableau d’ID de propriété spécifiant les propriétés à retourner dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2081">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="999c8-2082">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2082">0</span></span>

<span data-ttu-id="999c8-2083">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2083">1</span></span>

<span data-ttu-id="999c8-2084">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2084">2</span></span>

<span data-ttu-id="999c8-2085">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2085">3</span></span>

<span data-ttu-id="999c8-2086">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2086">4</span></span>

<span data-ttu-id="999c8-2087">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2087">5</span></span>

<span data-ttu-id="999c8-2088">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2088">6</span></span>

<span data-ttu-id="999c8-2089">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2089">7</span></span>

<span data-ttu-id="999c8-2090">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2090">8</span></span>

<span data-ttu-id="999c8-2091">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2091">9</span></span>

<span data-ttu-id="999c8-2092">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2092">1</span></span><br/> <span data-ttu-id="999c8-2093">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2093">0</span></span><br/>

<span data-ttu-id="999c8-2094">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2094">1</span></span>

<span data-ttu-id="999c8-2095">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2095">2</span></span>

<span data-ttu-id="999c8-2096">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2096">3</span></span>

<span data-ttu-id="999c8-2097">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2097">4</span></span>

<span data-ttu-id="999c8-2098">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2098">5</span></span>

<span data-ttu-id="999c8-2099">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2099">6</span></span>

<span data-ttu-id="999c8-2100">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2100">7</span></span>

<span data-ttu-id="999c8-2101">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2101">8</span></span>

<span data-ttu-id="999c8-2102">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2102">9</span></span>

<span data-ttu-id="999c8-2103">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2103">2</span></span><br/> <span data-ttu-id="999c8-2104">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2104">0</span></span><br/>

<span data-ttu-id="999c8-2105">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2105">1</span></span>

<span data-ttu-id="999c8-2106">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2106">2</span></span>

<span data-ttu-id="999c8-2107">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2107">3</span></span>

<span data-ttu-id="999c8-2108">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2108">4</span></span>

<span data-ttu-id="999c8-2109">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2109">5</span></span>

<span data-ttu-id="999c8-2110">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2110">6</span></span>

<span data-ttu-id="999c8-2111">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2111">7</span></span>

<span data-ttu-id="999c8-2112">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2112">8</span></span>

<span data-ttu-id="999c8-2113">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2113">9</span></span>

<span data-ttu-id="999c8-2114">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2114">3</span></span><br/> <span data-ttu-id="999c8-2115">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2115">0</span></span><br/>

<span data-ttu-id="999c8-2116">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2116">1</span></span>

<span data-ttu-id="999c8-2117">count</span><span class="sxs-lookup"><span data-stu-id="999c8-2117">count</span></span>

<span data-ttu-id="999c8-2118">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-2118">aPropSpec</span></span>

<span data-ttu-id="999c8-2119">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-2119">... (variable)</span></span>



 

<span data-ttu-id="999c8-2120">**Count**: entier non signé 32 bits contenant le nombre d’éléments dans le tableau aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="999c8-2120">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="999c8-2121">**aPropSpec**: tableau de structures CFullPropSpec indiquant les propriétés à retourner.</span><span class="sxs-lookup"><span data-stu-id="999c8-2121">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="999c8-2122">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2122">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="999c8-2123">Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.</span><span class="sxs-lookup"><span data-stu-id="999c8-2123">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="999c8-2124">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="999c8-2124">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="999c8-2125">La structure CRowSeekAt contient le décalage à partir duquel récupérer des lignes dans un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-2125">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="999c8-2126">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2126">0</span></span>

<span data-ttu-id="999c8-2127">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2127">1</span></span>

<span data-ttu-id="999c8-2128">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2128">2</span></span>

<span data-ttu-id="999c8-2129">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2129">3</span></span>

<span data-ttu-id="999c8-2130">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2130">4</span></span>

<span data-ttu-id="999c8-2131">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2131">5</span></span>

<span data-ttu-id="999c8-2132">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2132">6</span></span>

<span data-ttu-id="999c8-2133">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2133">7</span></span>

<span data-ttu-id="999c8-2134">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2134">8</span></span>

<span data-ttu-id="999c8-2135">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2135">9</span></span>

<span data-ttu-id="999c8-2136">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2136">1</span></span><br/> <span data-ttu-id="999c8-2137">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2137">0</span></span><br/>

<span data-ttu-id="999c8-2138">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2138">1</span></span>

<span data-ttu-id="999c8-2139">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2139">2</span></span>

<span data-ttu-id="999c8-2140">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2140">3</span></span>

<span data-ttu-id="999c8-2141">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2141">4</span></span>

<span data-ttu-id="999c8-2142">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2142">5</span></span>

<span data-ttu-id="999c8-2143">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2143">6</span></span>

<span data-ttu-id="999c8-2144">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2144">7</span></span>

<span data-ttu-id="999c8-2145">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2145">8</span></span>

<span data-ttu-id="999c8-2146">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2146">9</span></span>

<span data-ttu-id="999c8-2147">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2147">2</span></span><br/> <span data-ttu-id="999c8-2148">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2148">0</span></span><br/>

<span data-ttu-id="999c8-2149">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2149">1</span></span>

<span data-ttu-id="999c8-2150">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2150">2</span></span>

<span data-ttu-id="999c8-2151">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2151">3</span></span>

<span data-ttu-id="999c8-2152">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2152">4</span></span>

<span data-ttu-id="999c8-2153">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2153">5</span></span>

<span data-ttu-id="999c8-2154">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2154">6</span></span>

<span data-ttu-id="999c8-2155">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2155">7</span></span>

<span data-ttu-id="999c8-2156">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2156">8</span></span>

<span data-ttu-id="999c8-2157">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2157">9</span></span>

<span data-ttu-id="999c8-2158">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2158">3</span></span><br/> <span data-ttu-id="999c8-2159">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2159">0</span></span><br/>

<span data-ttu-id="999c8-2160">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2160">1</span></span>

<span data-ttu-id="999c8-2161">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="999c8-2161">\_hRegion</span></span>

<span data-ttu-id="999c8-2162">\_cskip</span><span class="sxs-lookup"><span data-stu-id="999c8-2162">\_cskip</span></span>

<span data-ttu-id="999c8-2163">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="999c8-2163">\_bmkOffset</span></span>



 

<span data-ttu-id="999c8-2164">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="999c8-2164">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="999c8-2165">**\_ cskip**: entier non signé 32 bits contenant le nombre de lignes à ignorer dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2165">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="999c8-2166">**\_ bmkOffset**: valeur 32 bits représentant le handle du **signet** indiquant la position de départ à partir de laquelle ignorer le nombre de lignes spécifié dans \_ cskip, avant de commencer la récupération.</span><span class="sxs-lookup"><span data-stu-id="999c8-2166">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="999c8-2167">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="999c8-2167">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="999c8-2168">La structure CRowSeekAtRatio identifie le point à partir duquel commencer la récupération d’un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-2168">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="999c8-2169">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2169">0</span></span>

<span data-ttu-id="999c8-2170">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2170">1</span></span>

<span data-ttu-id="999c8-2171">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2171">2</span></span>

<span data-ttu-id="999c8-2172">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2172">3</span></span>

<span data-ttu-id="999c8-2173">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2173">4</span></span>

<span data-ttu-id="999c8-2174">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2174">5</span></span>

<span data-ttu-id="999c8-2175">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2175">6</span></span>

<span data-ttu-id="999c8-2176">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2176">7</span></span>

<span data-ttu-id="999c8-2177">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2177">8</span></span>

<span data-ttu-id="999c8-2178">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2178">9</span></span>

<span data-ttu-id="999c8-2179">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2179">1</span></span><br/> <span data-ttu-id="999c8-2180">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2180">0</span></span><br/>

<span data-ttu-id="999c8-2181">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2181">1</span></span>

<span data-ttu-id="999c8-2182">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2182">2</span></span>

<span data-ttu-id="999c8-2183">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2183">3</span></span>

<span data-ttu-id="999c8-2184">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2184">4</span></span>

<span data-ttu-id="999c8-2185">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2185">5</span></span>

<span data-ttu-id="999c8-2186">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2186">6</span></span>

<span data-ttu-id="999c8-2187">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2187">7</span></span>

<span data-ttu-id="999c8-2188">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2188">8</span></span>

<span data-ttu-id="999c8-2189">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2189">9</span></span>

<span data-ttu-id="999c8-2190">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2190">2</span></span><br/> <span data-ttu-id="999c8-2191">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2191">0</span></span><br/>

<span data-ttu-id="999c8-2192">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2192">1</span></span>

<span data-ttu-id="999c8-2193">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2193">2</span></span>

<span data-ttu-id="999c8-2194">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2194">3</span></span>

<span data-ttu-id="999c8-2195">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2195">4</span></span>

<span data-ttu-id="999c8-2196">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2196">5</span></span>

<span data-ttu-id="999c8-2197">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2197">6</span></span>

<span data-ttu-id="999c8-2198">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2198">7</span></span>

<span data-ttu-id="999c8-2199">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2199">8</span></span>

<span data-ttu-id="999c8-2200">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2200">9</span></span>

<span data-ttu-id="999c8-2201">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2201">3</span></span><br/> <span data-ttu-id="999c8-2202">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2202">0</span></span><br/>

<span data-ttu-id="999c8-2203">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2203">1</span></span>

<span data-ttu-id="999c8-2204">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="999c8-2204">CiTblChapt</span></span>

<span data-ttu-id="999c8-2205">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="999c8-2205">\_hRegion</span></span>

<span data-ttu-id="999c8-2206">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="999c8-2206">\_ulNumerator</span></span>

<span data-ttu-id="999c8-2207">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="999c8-2207">\_ulDenominator</span></span>



 

<span data-ttu-id="999c8-2208">**CiTblChapt**: entier non signé 32 bits indiquant le chapitre de l’ensemble de lignes à partir duquel récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2208">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="999c8-2209">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="999c8-2209">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="999c8-2210">**\_ ulNumerator**: entier 32 bits non signé représentant le numérateur du rapport entre les lignes du chapitre et le début de la récupération.</span><span class="sxs-lookup"><span data-stu-id="999c8-2210">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="999c8-2211">**\_ ulDenominator**: entier 32 bits non signé représentant le dénominateur du rapport entre les lignes du chapitre et le début de la récupération.</span><span class="sxs-lookup"><span data-stu-id="999c8-2211">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="999c8-2212">DOIT être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="999c8-2212">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="999c8-2213">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="999c8-2213">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="999c8-2214">La structure CRowSeekByBookmark identifie les signets à partir desquels commencer la récupération de lignes pour un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-2214">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="999c8-2215">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2215">0</span></span>

<span data-ttu-id="999c8-2216">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2216">1</span></span>

<span data-ttu-id="999c8-2217">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2217">2</span></span>

<span data-ttu-id="999c8-2218">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2218">3</span></span>

<span data-ttu-id="999c8-2219">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2219">4</span></span>

<span data-ttu-id="999c8-2220">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2220">5</span></span>

<span data-ttu-id="999c8-2221">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2221">6</span></span>

<span data-ttu-id="999c8-2222">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2222">7</span></span>

<span data-ttu-id="999c8-2223">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2223">8</span></span>

<span data-ttu-id="999c8-2224">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2224">9</span></span>

<span data-ttu-id="999c8-2225">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2225">1</span></span><br/> <span data-ttu-id="999c8-2226">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2226">0</span></span><br/>

<span data-ttu-id="999c8-2227">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2227">1</span></span>

<span data-ttu-id="999c8-2228">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2228">2</span></span>

<span data-ttu-id="999c8-2229">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2229">3</span></span>

<span data-ttu-id="999c8-2230">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2230">4</span></span>

<span data-ttu-id="999c8-2231">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2231">5</span></span>

<span data-ttu-id="999c8-2232">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2232">6</span></span>

<span data-ttu-id="999c8-2233">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2233">7</span></span>

<span data-ttu-id="999c8-2234">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2234">8</span></span>

<span data-ttu-id="999c8-2235">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2235">9</span></span>

<span data-ttu-id="999c8-2236">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2236">2</span></span><br/> <span data-ttu-id="999c8-2237">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2237">0</span></span><br/>

<span data-ttu-id="999c8-2238">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2238">1</span></span>

<span data-ttu-id="999c8-2239">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2239">2</span></span>

<span data-ttu-id="999c8-2240">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2240">3</span></span>

<span data-ttu-id="999c8-2241">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2241">4</span></span>

<span data-ttu-id="999c8-2242">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2242">5</span></span>

<span data-ttu-id="999c8-2243">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2243">6</span></span>

<span data-ttu-id="999c8-2244">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2244">7</span></span>

<span data-ttu-id="999c8-2245">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2245">8</span></span>

<span data-ttu-id="999c8-2246">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2246">9</span></span>

<span data-ttu-id="999c8-2247">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2247">3</span></span><br/> <span data-ttu-id="999c8-2248">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2248">0</span></span><br/>

<span data-ttu-id="999c8-2249">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2249">1</span></span>

<span data-ttu-id="999c8-2250">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="999c8-2250">\_hRegion</span></span>

<span data-ttu-id="999c8-2251">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="999c8-2251">\_cBookmarks</span></span>

<span data-ttu-id="999c8-2252">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="999c8-2252">\_maxRet</span></span>

<span data-ttu-id="999c8-2253">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="999c8-2253">\_cValidRet</span></span>

<span data-ttu-id="999c8-2254">\_aBookmarks (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-2254">\_aBookmarks (variable)</span></span>

<span data-ttu-id="999c8-2255">\_ascRet (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-2255">\_ascRet (variable)</span></span>



 

<span data-ttu-id="999c8-2256">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="999c8-2256">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="999c8-2257">**\_ cBookmarks**: entier 32 bits non signé représentant le nombre d’éléments dans le \_ tableau aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="999c8-2257">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="999c8-2258">**\_ maxRet**: entier 32 bits non signé représentant le nombre d’éléments dans le \_ tableau ascRet.</span><span class="sxs-lookup"><span data-stu-id="999c8-2258">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="999c8-2259">**\_ cValidRet**: entier non signé 32 bits représentant le nombre d’éléments dans le \_ tableau ascRet qui sont valides.</span><span class="sxs-lookup"><span data-stu-id="999c8-2259">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="999c8-2260">Des éléments valides ont été définis dans le tableau, alors que les éléments non valides ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="999c8-2260">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="999c8-2261">**\_ aBookmarks**: tableau de handles de signet (chacun représenté par 4 octets), obtenu à partir d’un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-2261">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="999c8-2262">**\_ ascRet**: tableau de valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="999c8-2262">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="999c8-2263">Lorsque le CRowSeekByBookMark est envoyé dans le cadre de la demande CPMGetRowsIn, le nombre d’entrées dans le tableau doit être égal à \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="999c8-2263">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="999c8-2264">Lorsqu’il est envoyé par le client, les valeurs doivent être égales à zéro, et le serveur doit ignorer le contenu du tableau.</span><span class="sxs-lookup"><span data-stu-id="999c8-2264">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="999c8-2265">Lorsqu’il est envoyé par le serveur (dans le cadre du message CPMGetRowsOut), les valeurs du tableau indiquent l’état du résultat pour chaque extraction de ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2265">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="999c8-2266">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="999c8-2266">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="999c8-2267">La structure CRowSeekNext contient le nombre de lignes à ignorer dans un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-2267">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="999c8-2268">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2268">0</span></span>

<span data-ttu-id="999c8-2269">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2269">1</span></span>

<span data-ttu-id="999c8-2270">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2270">2</span></span>

<span data-ttu-id="999c8-2271">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2271">3</span></span>

<span data-ttu-id="999c8-2272">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2272">4</span></span>

<span data-ttu-id="999c8-2273">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2273">5</span></span>

<span data-ttu-id="999c8-2274">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2274">6</span></span>

<span data-ttu-id="999c8-2275">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2275">7</span></span>

<span data-ttu-id="999c8-2276">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2276">8</span></span>

<span data-ttu-id="999c8-2277">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2277">9</span></span>

<span data-ttu-id="999c8-2278">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2278">1</span></span><br/> <span data-ttu-id="999c8-2279">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2279">0</span></span><br/>

<span data-ttu-id="999c8-2280">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2280">1</span></span>

<span data-ttu-id="999c8-2281">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2281">2</span></span>

<span data-ttu-id="999c8-2282">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2282">3</span></span>

<span data-ttu-id="999c8-2283">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2283">4</span></span>

<span data-ttu-id="999c8-2284">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2284">5</span></span>

<span data-ttu-id="999c8-2285">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2285">6</span></span>

<span data-ttu-id="999c8-2286">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2286">7</span></span>

<span data-ttu-id="999c8-2287">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2287">8</span></span>

<span data-ttu-id="999c8-2288">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2288">9</span></span>

<span data-ttu-id="999c8-2289">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2289">2</span></span><br/> <span data-ttu-id="999c8-2290">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2290">0</span></span><br/>

<span data-ttu-id="999c8-2291">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2291">1</span></span>

<span data-ttu-id="999c8-2292">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2292">2</span></span>

<span data-ttu-id="999c8-2293">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2293">3</span></span>

<span data-ttu-id="999c8-2294">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2294">4</span></span>

<span data-ttu-id="999c8-2295">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2295">5</span></span>

<span data-ttu-id="999c8-2296">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2296">6</span></span>

<span data-ttu-id="999c8-2297">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2297">7</span></span>

<span data-ttu-id="999c8-2298">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2298">8</span></span>

<span data-ttu-id="999c8-2299">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2299">9</span></span>

<span data-ttu-id="999c8-2300">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2300">3</span></span><br/> <span data-ttu-id="999c8-2301">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2301">0</span></span><br/>

<span data-ttu-id="999c8-2302">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2302">1</span></span>

<span data-ttu-id="999c8-2303">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="999c8-2303">CiTblChapt</span></span>

<span data-ttu-id="999c8-2304">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="999c8-2304">\_hRegion</span></span>

<span data-ttu-id="999c8-2305">\_cskip</span><span class="sxs-lookup"><span data-stu-id="999c8-2305">\_cskip</span></span>



 

<span data-ttu-id="999c8-2306">**CiTblChapt**: entier 32 bits non signé spécifiant le chapitre de l’ensemble de lignes à partir duquel récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2306">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="999c8-2307">**\_ hRegion**: doit être défini sur 0x00000000 et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="999c8-2307">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="999c8-2308">**\_ cskip**: entier 32 bits non signé représentant le nombre de lignes à ignorer dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2308">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="999c8-2309">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="999c8-2309">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="999c8-2310">La structure CRowsetProperties contient des informations de configuration pour une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-2310">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="999c8-2311">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2311">0</span></span>

<span data-ttu-id="999c8-2312">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2312">1</span></span>

<span data-ttu-id="999c8-2313">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2313">2</span></span>

<span data-ttu-id="999c8-2314">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2314">3</span></span>

<span data-ttu-id="999c8-2315">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2315">4</span></span>

<span data-ttu-id="999c8-2316">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2316">5</span></span>

<span data-ttu-id="999c8-2317">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2317">6</span></span>

<span data-ttu-id="999c8-2318">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2318">7</span></span>

<span data-ttu-id="999c8-2319">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2319">8</span></span>

<span data-ttu-id="999c8-2320">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2320">9</span></span>

<span data-ttu-id="999c8-2321">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2321">1</span></span><br/> <span data-ttu-id="999c8-2322">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2322">0</span></span><br/>

<span data-ttu-id="999c8-2323">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2323">1</span></span>

<span data-ttu-id="999c8-2324">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2324">2</span></span>

<span data-ttu-id="999c8-2325">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2325">3</span></span>

<span data-ttu-id="999c8-2326">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2326">4</span></span>

<span data-ttu-id="999c8-2327">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2327">5</span></span>

<span data-ttu-id="999c8-2328">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2328">6</span></span>

<span data-ttu-id="999c8-2329">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2329">7</span></span>

<span data-ttu-id="999c8-2330">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2330">8</span></span>

<span data-ttu-id="999c8-2331">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2331">9</span></span>

<span data-ttu-id="999c8-2332">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2332">2</span></span><br/> <span data-ttu-id="999c8-2333">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2333">0</span></span><br/>

<span data-ttu-id="999c8-2334">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2334">1</span></span>

<span data-ttu-id="999c8-2335">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2335">2</span></span>

<span data-ttu-id="999c8-2336">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2336">3</span></span>

<span data-ttu-id="999c8-2337">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2337">4</span></span>

<span data-ttu-id="999c8-2338">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2338">5</span></span>

<span data-ttu-id="999c8-2339">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2339">6</span></span>

<span data-ttu-id="999c8-2340">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2340">7</span></span>

<span data-ttu-id="999c8-2341">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2341">8</span></span>

<span data-ttu-id="999c8-2342">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2342">9</span></span>

<span data-ttu-id="999c8-2343">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2343">3</span></span><br/> <span data-ttu-id="999c8-2344">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2344">0</span></span><br/>

<span data-ttu-id="999c8-2345">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2345">1</span></span>

<span data-ttu-id="999c8-2346">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="999c8-2346">\_uBooleanOptions</span></span>

<span data-ttu-id="999c8-2347">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="999c8-2347">\_ulMaxOpenRows</span></span>

<span data-ttu-id="999c8-2348">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="999c8-2348">\_ulMemoryUsage</span></span>

<span data-ttu-id="999c8-2349">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="999c8-2349">\_cMaxResults</span></span>

<span data-ttu-id="999c8-2350">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="999c8-2350">\_cCmdTimeout</span></span>



 

<span data-ttu-id="999c8-2351">**\_ uBooleanOptions**: les 3 bits les moins significatifs de ce champ doivent contenir l’une des trois valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-2351">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="999c8-2352">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-2352">Value</span></span>                  | <span data-ttu-id="999c8-2353">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2353">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="999c8-2354">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-2354">eSequential 0x00000001</span></span> | <span data-ttu-id="999c8-2355">Le curseur peut être déplacé uniquement vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="999c8-2355">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="999c8-2356">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-2356">eLocatable 0x00000003</span></span>  | <span data-ttu-id="999c8-2357">Le curseur peut être déplacé vers n’importe quelle position.</span><span class="sxs-lookup"><span data-stu-id="999c8-2357">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="999c8-2358">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="999c8-2358">eScrollable 0x00000007</span></span> | <span data-ttu-id="999c8-2359">Le curseur peut être déplacé vers n’importe quelle position et extraction dans n’importe quelle direction.</span><span class="sxs-lookup"><span data-stu-id="999c8-2359">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="999c8-2360">Les bits restants peuvent être clairs ou définis sur une combinaison des valeurs suivantes logiquement ou ensemble :</span><span class="sxs-lookup"><span data-stu-id="999c8-2360">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="999c8-2361">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-2361">Value</span></span>                     | <span data-ttu-id="999c8-2362">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2362">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-2363">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="999c8-2363">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="999c8-2364">Le client n’attend pas la fin de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="999c8-2364">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="999c8-2365">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="999c8-2365">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="999c8-2366">Retourne les premières lignes rencontrées, pas les meilleures correspondances.</span><span class="sxs-lookup"><span data-stu-id="999c8-2366">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="999c8-2367">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="999c8-2367">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="999c8-2368">Le serveur ne doit pas ignorer les lignes tant que le client n’est pas terminé par une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-2368">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="999c8-2369">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="999c8-2369">eChaptered 0x00000800</span></span>     | <span data-ttu-id="999c8-2370">L’ensemble de lignes prend en charge les chapitres.</span><span class="sxs-lookup"><span data-stu-id="999c8-2370">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="999c8-2371">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="999c8-2371">eUseCI 0x00001000</span></span>         | <span data-ttu-id="999c8-2372">Répondez uniquement à la requête à partir de l’index, et non du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="999c8-2372">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="999c8-2373">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="999c8-2373">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="999c8-2374">Le service d’indexation doit envisager d’optimiser le temps de réponse du client lors de la suppression des résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-2374">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="999c8-2375">**\_ ulMaxOpenRows**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-2375">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="999c8-2376">Doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-2376">Must be set to 0x00000000.</span></span> <span data-ttu-id="999c8-2377">Non utilisé et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="999c8-2377">Not used and MUST be ignored.</span></span>

<span data-ttu-id="999c8-2378">**\_ ulMemoryUsage**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-2378">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="999c8-2379">Doit être défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="999c8-2380">Non utilisé et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="999c8-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="999c8-2381">**\_ cMaxResults**: entier non signé 32 bits spécifiant le nombre maximal de lignes à retourner pour la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-2381">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="999c8-2382">**\_ cCmdTimeout**: entier non signé 32 bits, qui spécifie le nombre de secondes au terme duquel une requête expire et se termine automatiquement, en comptant à partir du moment où la requête commence à s’exécuter sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-2382">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="999c8-2383">La valeur 0x00000000 signifie que la requête n’expire pas.</span><span class="sxs-lookup"><span data-stu-id="999c8-2383">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="999c8-2384">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="999c8-2384">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="999c8-2385">La structure CRowVariant contient la partie de taille fixe d’un type de données de longueur variable stockée dans le message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-2385">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="999c8-2386">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2386">0</span></span>

<span data-ttu-id="999c8-2387">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2387">1</span></span>

<span data-ttu-id="999c8-2388">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2388">2</span></span>

<span data-ttu-id="999c8-2389">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2389">3</span></span>

<span data-ttu-id="999c8-2390">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2390">4</span></span>

<span data-ttu-id="999c8-2391">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2391">5</span></span>

<span data-ttu-id="999c8-2392">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2392">6</span></span>

<span data-ttu-id="999c8-2393">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2393">7</span></span>

<span data-ttu-id="999c8-2394">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2394">8</span></span>

<span data-ttu-id="999c8-2395">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2395">9</span></span>

<span data-ttu-id="999c8-2396">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2396">1</span></span><br/> <span data-ttu-id="999c8-2397">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2397">0</span></span><br/>

<span data-ttu-id="999c8-2398">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2398">1</span></span>

<span data-ttu-id="999c8-2399">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2399">2</span></span>

<span data-ttu-id="999c8-2400">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2400">3</span></span>

<span data-ttu-id="999c8-2401">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2401">4</span></span>

<span data-ttu-id="999c8-2402">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2402">5</span></span>

<span data-ttu-id="999c8-2403">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2403">6</span></span>

<span data-ttu-id="999c8-2404">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2404">7</span></span>

<span data-ttu-id="999c8-2405">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2405">8</span></span>

<span data-ttu-id="999c8-2406">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2406">9</span></span>

<span data-ttu-id="999c8-2407">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2407">2</span></span><br/> <span data-ttu-id="999c8-2408">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2408">0</span></span><br/>

<span data-ttu-id="999c8-2409">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2409">1</span></span>

<span data-ttu-id="999c8-2410">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2410">2</span></span>

<span data-ttu-id="999c8-2411">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2411">3</span></span>

<span data-ttu-id="999c8-2412">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2412">4</span></span>

<span data-ttu-id="999c8-2413">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2413">5</span></span>

<span data-ttu-id="999c8-2414">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2414">6</span></span>

<span data-ttu-id="999c8-2415">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2415">7</span></span>

<span data-ttu-id="999c8-2416">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2416">8</span></span>

<span data-ttu-id="999c8-2417">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2417">9</span></span>

<span data-ttu-id="999c8-2418">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2418">3</span></span><br/> <span data-ttu-id="999c8-2419">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2419">0</span></span><br/>

<span data-ttu-id="999c8-2420">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2420">1</span></span>

<span data-ttu-id="999c8-2421">vType</span><span class="sxs-lookup"><span data-stu-id="999c8-2421">vType</span></span>

<span data-ttu-id="999c8-2422">Reserved1</span><span class="sxs-lookup"><span data-stu-id="999c8-2422">reserved1</span></span>

<span data-ttu-id="999c8-2423">reserved2</span><span class="sxs-lookup"><span data-stu-id="999c8-2423">reserved2</span></span>

<span data-ttu-id="999c8-2424">Offset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2424">Offset (optional)</span></span>



 

<span data-ttu-id="999c8-2425">**vType**: indicateur de type indiquant le type de vValue.</span><span class="sxs-lookup"><span data-stu-id="999c8-2425">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="999c8-2426">Il doit s’agir de l’une des valeurs VARENUM spécifiées dans la section 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-2426">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="999c8-2427">**Reserved1**: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="999c8-2427">**reserved1**: Not used.</span></span> <span data-ttu-id="999c8-2428">La valeur peut être définie sur n’importe quelle valeur arbitraire et doit être ignorée lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="999c8-2428">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="999c8-2429">**Reserved2**: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="999c8-2429">**reserved2**: Not used.</span></span> <span data-ttu-id="999c8-2430">La valeur peut être définie sur n’importe quelle valeur arbitraire et doit être ignorée lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="999c8-2430">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="999c8-2431">**Offset**: décalage des données de longueur variable (par exemple, une chaîne).</span><span class="sxs-lookup"><span data-stu-id="999c8-2431">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="999c8-2432">Il doit s’agir d’une valeur 32 bits (4 octets de long) si les décalages 32 bits sont utilisés (conformément aux règles de la section 2.2.3.16) ou d’une valeur de 64 octets (8 octets de long) si les décalages de 64 bits sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2432">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="999c8-2433">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="999c8-2433">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="999c8-2434">La structure CSortSet contient l’ordre de tri de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-2434">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="999c8-2435">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2435">0</span></span>

<span data-ttu-id="999c8-2436">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2436">1</span></span>

<span data-ttu-id="999c8-2437">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2437">2</span></span>

<span data-ttu-id="999c8-2438">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2438">3</span></span>

<span data-ttu-id="999c8-2439">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2439">4</span></span>

<span data-ttu-id="999c8-2440">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2440">5</span></span>

<span data-ttu-id="999c8-2441">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2441">6</span></span>

<span data-ttu-id="999c8-2442">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2442">7</span></span>

<span data-ttu-id="999c8-2443">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2443">8</span></span>

<span data-ttu-id="999c8-2444">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2444">9</span></span>

<span data-ttu-id="999c8-2445">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2445">1</span></span><br/> <span data-ttu-id="999c8-2446">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2446">0</span></span><br/>

<span data-ttu-id="999c8-2447">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2447">1</span></span>

<span data-ttu-id="999c8-2448">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2448">2</span></span>

<span data-ttu-id="999c8-2449">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2449">3</span></span>

<span data-ttu-id="999c8-2450">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2450">4</span></span>

<span data-ttu-id="999c8-2451">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2451">5</span></span>

<span data-ttu-id="999c8-2452">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2452">6</span></span>

<span data-ttu-id="999c8-2453">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2453">7</span></span>

<span data-ttu-id="999c8-2454">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2454">8</span></span>

<span data-ttu-id="999c8-2455">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2455">9</span></span>

<span data-ttu-id="999c8-2456">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2456">2</span></span><br/> <span data-ttu-id="999c8-2457">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2457">0</span></span><br/>

<span data-ttu-id="999c8-2458">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2458">1</span></span>

<span data-ttu-id="999c8-2459">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2459">2</span></span>

<span data-ttu-id="999c8-2460">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2460">3</span></span>

<span data-ttu-id="999c8-2461">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2461">4</span></span>

<span data-ttu-id="999c8-2462">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2462">5</span></span>

<span data-ttu-id="999c8-2463">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2463">6</span></span>

<span data-ttu-id="999c8-2464">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2464">7</span></span>

<span data-ttu-id="999c8-2465">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2465">8</span></span>

<span data-ttu-id="999c8-2466">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2466">9</span></span>

<span data-ttu-id="999c8-2467">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2467">3</span></span><br/> <span data-ttu-id="999c8-2468">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2468">0</span></span><br/>

<span data-ttu-id="999c8-2469">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2469">1</span></span>

<span data-ttu-id="999c8-2470">Count</span><span class="sxs-lookup"><span data-stu-id="999c8-2470">Count</span></span>

<span data-ttu-id="999c8-2471">sortArray (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-2471">sortArray (variable)</span></span>



 

<span data-ttu-id="999c8-2472">**Count**: entier non signé 32 bits spécifiant le nombre d’éléments dans sortArray.</span><span class="sxs-lookup"><span data-stu-id="999c8-2472">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="999c8-2473">**sortArray**: tableau de structures CSort décrivant l’ordre dans lequel trier les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-2473">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="999c8-2474">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2474">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="999c8-2475">Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.</span><span class="sxs-lookup"><span data-stu-id="999c8-2475">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="999c8-2476">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="999c8-2476">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="999c8-2477">La structure CTableColumn contient une colonne d’un message CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2477">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="999c8-2478">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2478">0</span></span>

<span data-ttu-id="999c8-2479">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2479">1</span></span>

<span data-ttu-id="999c8-2480">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2480">2</span></span>

<span data-ttu-id="999c8-2481">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2481">3</span></span>

<span data-ttu-id="999c8-2482">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2482">4</span></span>

<span data-ttu-id="999c8-2483">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2483">5</span></span>

<span data-ttu-id="999c8-2484">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2484">6</span></span>

<span data-ttu-id="999c8-2485">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2485">7</span></span>

<span data-ttu-id="999c8-2486">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2486">8</span></span>

<span data-ttu-id="999c8-2487">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2487">9</span></span>

<span data-ttu-id="999c8-2488">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2488">1</span></span><br/> <span data-ttu-id="999c8-2489">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2489">0</span></span><br/>

<span data-ttu-id="999c8-2490">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2490">1</span></span>

<span data-ttu-id="999c8-2491">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2491">2</span></span>

<span data-ttu-id="999c8-2492">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2492">3</span></span>

<span data-ttu-id="999c8-2493">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2493">4</span></span>

<span data-ttu-id="999c8-2494">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2494">5</span></span>

<span data-ttu-id="999c8-2495">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2495">6</span></span>

<span data-ttu-id="999c8-2496">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2496">7</span></span>

<span data-ttu-id="999c8-2497">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2497">8</span></span>

<span data-ttu-id="999c8-2498">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2498">9</span></span>

<span data-ttu-id="999c8-2499">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2499">2</span></span><br/> <span data-ttu-id="999c8-2500">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2500">0</span></span><br/>

<span data-ttu-id="999c8-2501">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2501">1</span></span>

<span data-ttu-id="999c8-2502">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2502">2</span></span>

<span data-ttu-id="999c8-2503">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2503">3</span></span>

<span data-ttu-id="999c8-2504">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2504">4</span></span>

<span data-ttu-id="999c8-2505">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2505">5</span></span>

<span data-ttu-id="999c8-2506">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2506">6</span></span>

<span data-ttu-id="999c8-2507">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2507">7</span></span>

<span data-ttu-id="999c8-2508">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2508">8</span></span>

<span data-ttu-id="999c8-2509">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2509">9</span></span>

<span data-ttu-id="999c8-2510">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2510">3</span></span><br/> <span data-ttu-id="999c8-2511">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2511">0</span></span><br/>

<span data-ttu-id="999c8-2512">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2512">1</span></span>

<span data-ttu-id="999c8-2513">PropSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-2513">PropSpec</span></span>

<span data-ttu-id="999c8-2514">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-2514">...(variable)</span></span>

<span data-ttu-id="999c8-2515">vType</span><span class="sxs-lookup"><span data-stu-id="999c8-2515">vType</span></span>

<span data-ttu-id="999c8-2516">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="999c8-2516">ValueUsed</span></span>

<span data-ttu-id="999c8-2517">\_padding1 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2517">\_padding1 (optional)</span></span>

<span data-ttu-id="999c8-2518">ValueOffset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2518">ValueOffset (optional)</span></span>

<span data-ttu-id="999c8-2519">Value (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2519">ValueSize (optional)</span></span>

<span data-ttu-id="999c8-2520">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="999c8-2520">StatusUsed</span></span>

<span data-ttu-id="999c8-2521">\_padding2 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2521">\_padding2 (optional)</span></span>

<span data-ttu-id="999c8-2522">StatusOffset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2522">StatusOffset (optional)</span></span>

<span data-ttu-id="999c8-2523">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="999c8-2523">LengthUsed</span></span>

<span data-ttu-id="999c8-2524">\_padding3 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2524">\_padding3 (optional)</span></span>

<span data-ttu-id="999c8-2525">LengthOffset (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2525">LengthOffset (optional)</span></span>



 

<span data-ttu-id="999c8-2526">**PropSpec**: structure CFullPropSpec telle que spécifiée dans la section 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="999c8-2526">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="999c8-2527">**vType**: spécifie le type de valeur de données contenu dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2527">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="999c8-2528">Consultez le champ vType de la section 2.2.1.1 pour obtenir la liste des valeurs de ce champ.</span><span class="sxs-lookup"><span data-stu-id="999c8-2528">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="999c8-2529">**ValueUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-2529">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="999c8-2530">Si la valeur est 0x01, la colonne est transférée dans la ligne de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="999c8-2530">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="999c8-2531">Si la valeur est 0x00, la valeur de la colonne est transférée dans la section de longueur variable à la fin de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="999c8-2531">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="999c8-2532">**\_ padding1**: un champ d’un octet qui doit être inséré avant ValueOffset si, sans lui, ValueOffset ne commence pas à un décalage pair à partir du début du message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2532">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="999c8-2533">La valeur de cet octet est arbitraire et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2533">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="999c8-2534">Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-2534">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="999c8-2535">**ValueOffset**: entier non signé de 2 octets spécifiant le décalage de la valeur de colonne dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2535">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="999c8-2536">Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-2536">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="999c8-2537">**Value**: entier non signé de 2 octets spécifiant la taille de la colonne en octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-2537">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="999c8-2538">Si ValueUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-2538">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="999c8-2539">**StatusUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-2539">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="999c8-2540">Si la valeur est 0x01, l’état de la colonne est transféré dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2540">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="999c8-2541">Si 0x00, l’état de la colonne n’est pas transféré dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2541">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="999c8-2542">**\_ padding2**: un champ d’un octet qui doit être inséré avant StatusOffset si, sans lui, le champ StatusOffset ne commence pas à un décalage pair à partir du début du message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2542">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="999c8-2543">La valeur de cet octet est arbitraire et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2543">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="999c8-2544">Si StatusUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-2544">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="999c8-2545">**StatusOffset**: entier non signé de 2 octets spécifiant le décalage de l’état de la colonne dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2545">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="999c8-2546">Si StatusUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-2546">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="999c8-2547">**LengthUsed**: champ d’un octet qui doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-2547">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="999c8-2548">Si la valeur est 0x01, la longueur de la colonne est transférée dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2548">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="999c8-2549">Si 0x00, la longueur de la colonne ne doit pas être transférée dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2549">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="999c8-2550">**\_ padding3**: un champ d’un octet qui doit être inséré avant LengthOffset si, sans lui, LengthOffset ne commence pas à un décalage pair à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2550">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="999c8-2551">La valeur de cet octet est arbitraire et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2551">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="999c8-2552">Si LengthUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-2552">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="999c8-2553">**LengthOffset**: entier non signé de 2 octets spécifiant le décalage de la longueur de colonne dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-2553">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="999c8-2554">Si LengthUsed a la valeur 0x00, ce champ ne doit pas être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-2554">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="999c8-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="999c8-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="999c8-2556">La structure SERIALIZEDPROPERTYVALUE contient une valeur sérialisée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2556">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="999c8-2557">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2557">0</span></span>

<span data-ttu-id="999c8-2558">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2558">1</span></span>

<span data-ttu-id="999c8-2559">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2559">2</span></span>

<span data-ttu-id="999c8-2560">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2560">3</span></span>

<span data-ttu-id="999c8-2561">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2561">4</span></span>

<span data-ttu-id="999c8-2562">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2562">5</span></span>

<span data-ttu-id="999c8-2563">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2563">6</span></span>

<span data-ttu-id="999c8-2564">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2564">7</span></span>

<span data-ttu-id="999c8-2565">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2565">8</span></span>

<span data-ttu-id="999c8-2566">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2566">9</span></span>

<span data-ttu-id="999c8-2567">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2567">1</span></span><br/> <span data-ttu-id="999c8-2568">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2568">0</span></span><br/>

<span data-ttu-id="999c8-2569">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2569">1</span></span>

<span data-ttu-id="999c8-2570">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2570">2</span></span>

<span data-ttu-id="999c8-2571">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2571">3</span></span>

<span data-ttu-id="999c8-2572">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2572">4</span></span>

<span data-ttu-id="999c8-2573">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2573">5</span></span>

<span data-ttu-id="999c8-2574">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2574">6</span></span>

<span data-ttu-id="999c8-2575">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2575">7</span></span>

<span data-ttu-id="999c8-2576">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2576">8</span></span>

<span data-ttu-id="999c8-2577">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2577">9</span></span>

<span data-ttu-id="999c8-2578">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2578">2</span></span><br/> <span data-ttu-id="999c8-2579">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2579">0</span></span><br/>

<span data-ttu-id="999c8-2580">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2580">1</span></span>

<span data-ttu-id="999c8-2581">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2581">2</span></span>

<span data-ttu-id="999c8-2582">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2582">3</span></span>

<span data-ttu-id="999c8-2583">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2583">4</span></span>

<span data-ttu-id="999c8-2584">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2584">5</span></span>

<span data-ttu-id="999c8-2585">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2585">6</span></span>

<span data-ttu-id="999c8-2586">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2586">7</span></span>

<span data-ttu-id="999c8-2587">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2587">8</span></span>

<span data-ttu-id="999c8-2588">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2588">9</span></span>

<span data-ttu-id="999c8-2589">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2589">3</span></span><br/> <span data-ttu-id="999c8-2590">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2590">0</span></span><br/>

<span data-ttu-id="999c8-2591">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2591">1</span></span>

<span data-ttu-id="999c8-2592">dwType</span><span class="sxs-lookup"><span data-stu-id="999c8-2592">dwType</span></span>

<span data-ttu-id="999c8-2593">RGB (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-2593">rgb (variable)</span></span>



 

<span data-ttu-id="999c8-2594">**dwType**: l’un des types variant, défini dans la section 2.2.1.1, qui peut être combiné avec des modificateurs de type Variant.</span><span class="sxs-lookup"><span data-stu-id="999c8-2594">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="999c8-2595">Pour tous les types variant, à l’exception de ceux associés à VT \_ Array, SERIALIZEDPROPERTYVALUE a la même disposition que CBaseStorageVariant, comme indiqué dans la section 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-2595">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="999c8-2596">Si le type Variant est combiné avec le \_ modificateur de type tableau VT, SAFEARRAY2, spécifié dans la section 2.2.1.2.1.1, est utilisé à la place de SAFEARRAY dans le champ vValue de CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="999c8-2596">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="999c8-2597">**RGB**: valeur sérialisée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2597">**rgb**: Serialized value.</span></span> <span data-ttu-id="999c8-2598">Consultez les détails de la sérialisation pour vValue dans 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-2598">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="999c8-2599">2.2.2 en-têtes de message</span><span class="sxs-lookup"><span data-stu-id="999c8-2599">2.2.2 Message Headers</span></span>

<span data-ttu-id="999c8-2600">Tous les messages du protocole de service d’indexation de contenu ont un en-tête de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-2600">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="999c8-2601">Vous trouverez ci-dessous un diagramme montrant le format d’en-tête de message du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-2601">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="999c8-2602">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2602">0</span></span>

<span data-ttu-id="999c8-2603">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2603">1</span></span>

<span data-ttu-id="999c8-2604">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2604">2</span></span>

<span data-ttu-id="999c8-2605">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2605">3</span></span>

<span data-ttu-id="999c8-2606">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2606">4</span></span>

<span data-ttu-id="999c8-2607">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2607">5</span></span>

<span data-ttu-id="999c8-2608">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2608">6</span></span>

<span data-ttu-id="999c8-2609">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2609">7</span></span>

<span data-ttu-id="999c8-2610">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2610">8</span></span>

<span data-ttu-id="999c8-2611">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2611">9</span></span>

<span data-ttu-id="999c8-2612">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2612">1</span></span><br/> <span data-ttu-id="999c8-2613">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2613">0</span></span><br/>

<span data-ttu-id="999c8-2614">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2614">1</span></span>

<span data-ttu-id="999c8-2615">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2615">2</span></span>

<span data-ttu-id="999c8-2616">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2616">3</span></span>

<span data-ttu-id="999c8-2617">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2617">4</span></span>

<span data-ttu-id="999c8-2618">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2618">5</span></span>

<span data-ttu-id="999c8-2619">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2619">6</span></span>

<span data-ttu-id="999c8-2620">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2620">7</span></span>

<span data-ttu-id="999c8-2621">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2621">8</span></span>

<span data-ttu-id="999c8-2622">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2622">9</span></span>

<span data-ttu-id="999c8-2623">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2623">2</span></span><br/> <span data-ttu-id="999c8-2624">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2624">0</span></span><br/>

<span data-ttu-id="999c8-2625">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2625">1</span></span>

<span data-ttu-id="999c8-2626">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2626">2</span></span>

<span data-ttu-id="999c8-2627">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2627">3</span></span>

<span data-ttu-id="999c8-2628">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2628">4</span></span>

<span data-ttu-id="999c8-2629">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2629">5</span></span>

<span data-ttu-id="999c8-2630">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2630">6</span></span>

<span data-ttu-id="999c8-2631">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2631">7</span></span>

<span data-ttu-id="999c8-2632">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2632">8</span></span>

<span data-ttu-id="999c8-2633">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2633">9</span></span>

<span data-ttu-id="999c8-2634">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2634">3</span></span><br/> <span data-ttu-id="999c8-2635">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2635">0</span></span><br/>

<span data-ttu-id="999c8-2636">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2636">1</span></span>

<span data-ttu-id="999c8-2637">\_msg</span><span class="sxs-lookup"><span data-stu-id="999c8-2637">\_msg</span></span>

<span data-ttu-id="999c8-2638">\_statu</span><span class="sxs-lookup"><span data-stu-id="999c8-2638">\_status</span></span>

<span data-ttu-id="999c8-2639">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="999c8-2639">\_ulChecksum</span></span>

<span data-ttu-id="999c8-2640">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="999c8-2640">\_ulReserved2</span></span>



 

<span data-ttu-id="999c8-2641">\_**MSG**: entier 32 bits qui identifie le type de message suivant l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="999c8-2641">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="999c8-2642">Le tableau suivant répertorie les messages du protocole du service d’indexation de contenu et les valeurs entières spécifiées pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2642">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="999c8-2643">Comme indiqué dans le tableau, certaines valeurs identifient 2 messages dans la table.</span><span class="sxs-lookup"><span data-stu-id="999c8-2643">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="999c8-2644">Dans ces instances, le message qui suit l’en-tête peut être identifié par la direction du message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2644">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="999c8-2645">Si la direction est client à serveur, le message avec « in » ajouté au nom du message est indiqué.</span><span class="sxs-lookup"><span data-stu-id="999c8-2645">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="999c8-2646">Si la direction est de serveur à client, le message « out » ajouté au nom du message est indiqué.</span><span class="sxs-lookup"><span data-stu-id="999c8-2646">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="999c8-2647">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-2647">Value</span></span>      | <span data-ttu-id="999c8-2648">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2648">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="999c8-2649">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="999c8-2649">0x000000C8</span></span> | <span data-ttu-id="999c8-2650">CPMConnectIn ou CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2650">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="999c8-2651">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="999c8-2651">0x000000C9</span></span> | <span data-ttu-id="999c8-2652">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="999c8-2652">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="999c8-2653">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="999c8-2653">0x000000CA</span></span> | <span data-ttu-id="999c8-2654">CPMCreateQueryIn ou CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2654">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="999c8-2655">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="999c8-2655">0x000000CB</span></span> | <span data-ttu-id="999c8-2656">CPMFreeCursorIn ou CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2656">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="999c8-2657">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="999c8-2657">0x000000CC</span></span> | <span data-ttu-id="999c8-2658">CPMGetRowsIn ou CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2658">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="999c8-2659">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="999c8-2659">0x000000CD</span></span> | <span data-ttu-id="999c8-2660">CPMRatioFinishedIn ou CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2660">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="999c8-2661">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="999c8-2661">0x000000CE</span></span> | <span data-ttu-id="999c8-2662">CPMCompareBmkIn ou CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2662">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="999c8-2663">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="999c8-2663">0x000000CF</span></span> | <span data-ttu-id="999c8-2664">CPMGetApproximatePositionIn ou CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2664">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="999c8-2665">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="999c8-2665">0x000000D0</span></span> | <span data-ttu-id="999c8-2666">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2666">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="999c8-2667">Stop</span><span class="sxs-lookup"><span data-stu-id="999c8-2667">0x000000D1</span></span> | <span data-ttu-id="999c8-2668">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="999c8-2668">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="999c8-2669">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="999c8-2669">0x000000D2</span></span> | <span data-ttu-id="999c8-2670">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2670">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="999c8-2671">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="999c8-2671">0x000000D7</span></span> | <span data-ttu-id="999c8-2672">CPMGetQueryStatusIn ou CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2672">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="999c8-2673">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="999c8-2673">0x000000D9</span></span> | <span data-ttu-id="999c8-2674">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2674">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="999c8-2675">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="999c8-2675">0x000000E1</span></span> | <span data-ttu-id="999c8-2676">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2676">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="999c8-2677">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="999c8-2677">0x000000E4</span></span> | <span data-ttu-id="999c8-2678">CPMFetchValueIn ou CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2678">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="999c8-2679">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="999c8-2679">0x000000E6</span></span> | <span data-ttu-id="999c8-2680">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2680">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="999c8-2681">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="999c8-2681">0x000000E7</span></span> | <span data-ttu-id="999c8-2682">CPMGetQueryStatusExIn ou PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2682">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="999c8-2683">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="999c8-2683">0x000000E8</span></span> | <span data-ttu-id="999c8-2684">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2684">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="999c8-2685">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="999c8-2685">0x000000E9</span></span> | <span data-ttu-id="999c8-2686">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2686">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="999c8-2687">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="999c8-2687">0x000000EC</span></span> | <span data-ttu-id="999c8-2688">CPMSetCatStateIn ou CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2688">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="999c8-2689">\_**État**: HRESULT \[ ms-sys \] , indiquant l’état de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2689">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="999c8-2690">*Comportement de Windows : le client définit toujours le \_ champ d’État sur 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="999c8-2690">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="999c8-2691">**\_ ulChecksum**: le \_ ulChecksum doit être calculé comme indiqué dans la section 3.2.4 pour les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="999c8-2691">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="999c8-2692">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2692">CPMConnectIn</span></span>
-   <span data-ttu-id="999c8-2693">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2693">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="999c8-2694">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2694">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="999c8-2695">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2695">CPMGetRowsIn</span></span>
-   <span data-ttu-id="999c8-2696">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2696">CPMFetchValueIn</span></span>

<span data-ttu-id="999c8-2697">Pour tous les autres messages, \_ ULCHECKSUM doit avoir la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-2697">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="999c8-2698">Un client doit ignorer le \_ champ ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="999c8-2698">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="999c8-2699">**\_ ulReserved2**: doit être défini sur 0 et ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-2699">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="999c8-2700">2.2.3 messages</span><span class="sxs-lookup"><span data-stu-id="999c8-2700">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="999c8-2701">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2701">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="999c8-2702">Le message CPMCiStateInOut contient des informations sur l’état du service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-2702">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="999c8-2703">Le format du message CPMCiStateInOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-2703">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-2704">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2704">0</span></span>

<span data-ttu-id="999c8-2705">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2705">1</span></span>

<span data-ttu-id="999c8-2706">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2706">2</span></span>

<span data-ttu-id="999c8-2707">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2707">3</span></span>

<span data-ttu-id="999c8-2708">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2708">4</span></span>

<span data-ttu-id="999c8-2709">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2709">5</span></span>

<span data-ttu-id="999c8-2710">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2710">6</span></span>

<span data-ttu-id="999c8-2711">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2711">7</span></span>

<span data-ttu-id="999c8-2712">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2712">8</span></span>

<span data-ttu-id="999c8-2713">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2713">9</span></span>

<span data-ttu-id="999c8-2714">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2714">1</span></span><br/> <span data-ttu-id="999c8-2715">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2715">0</span></span><br/>

<span data-ttu-id="999c8-2716">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2716">1</span></span>

<span data-ttu-id="999c8-2717">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2717">2</span></span>

<span data-ttu-id="999c8-2718">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2718">3</span></span>

<span data-ttu-id="999c8-2719">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2719">4</span></span>

<span data-ttu-id="999c8-2720">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2720">5</span></span>

<span data-ttu-id="999c8-2721">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2721">6</span></span>

<span data-ttu-id="999c8-2722">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2722">7</span></span>

<span data-ttu-id="999c8-2723">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2723">8</span></span>

<span data-ttu-id="999c8-2724">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2724">9</span></span>

<span data-ttu-id="999c8-2725">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2725">2</span></span><br/> <span data-ttu-id="999c8-2726">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2726">0</span></span><br/>

<span data-ttu-id="999c8-2727">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2727">1</span></span>

<span data-ttu-id="999c8-2728">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2728">2</span></span>

<span data-ttu-id="999c8-2729">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2729">3</span></span>

<span data-ttu-id="999c8-2730">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2730">4</span></span>

<span data-ttu-id="999c8-2731">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2731">5</span></span>

<span data-ttu-id="999c8-2732">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2732">6</span></span>

<span data-ttu-id="999c8-2733">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2733">7</span></span>

<span data-ttu-id="999c8-2734">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2734">8</span></span>

<span data-ttu-id="999c8-2735">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2735">9</span></span>

<span data-ttu-id="999c8-2736">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2736">3</span></span><br/> <span data-ttu-id="999c8-2737">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2737">0</span></span><br/>

<span data-ttu-id="999c8-2738">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2738">1</span></span>

<span data-ttu-id="999c8-2739">cbStruct</span><span class="sxs-lookup"><span data-stu-id="999c8-2739">cbStruct</span></span>

<span data-ttu-id="999c8-2740">cWordList</span><span class="sxs-lookup"><span data-stu-id="999c8-2740">cWordList</span></span>

<span data-ttu-id="999c8-2741">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="999c8-2741">cPersistentIndex</span></span>

<span data-ttu-id="999c8-2742">cQueries</span><span class="sxs-lookup"><span data-stu-id="999c8-2742">cQueries</span></span>

<span data-ttu-id="999c8-2743">cDocuments</span><span class="sxs-lookup"><span data-stu-id="999c8-2743">cDocuments</span></span>

<span data-ttu-id="999c8-2744">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="999c8-2744">cFreshTest</span></span>

<span data-ttu-id="999c8-2745">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="999c8-2745">dwMergeProgress</span></span>

<span data-ttu-id="999c8-2746">Immobilier</span><span class="sxs-lookup"><span data-stu-id="999c8-2746">eState</span></span>

<span data-ttu-id="999c8-2747">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="999c8-2747">cFilteredDocuments</span></span>

<span data-ttu-id="999c8-2748">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="999c8-2748">cTotalDocuments</span></span>

<span data-ttu-id="999c8-2749">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="999c8-2749">cPendingScans</span></span>

<span data-ttu-id="999c8-2750">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="999c8-2750">dwIndexSize</span></span>

<span data-ttu-id="999c8-2751">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="999c8-2751">cUniqueKeys</span></span>

<span data-ttu-id="999c8-2752">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="999c8-2752">cSecQDocuments</span></span>

<span data-ttu-id="999c8-2753">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="999c8-2753">dwPropCacheSize</span></span>



 

<span data-ttu-id="999c8-2754">**cbStruct**: entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-2754">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="999c8-2755">Taille en octets de ce message (à l’exception de l’en-tête commun).</span><span class="sxs-lookup"><span data-stu-id="999c8-2755">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="999c8-2756">DOIT être défini sur 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="999c8-2756">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="999c8-2757">**cWordList**: entier non signé 32 bits indiquant le nombre d’index initiaux créés pour les documents récemment indexés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2757">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="999c8-2758">**cPersistentIndex**: entier non signé 32 bits indiquant le nombre d’index persistants.</span><span class="sxs-lookup"><span data-stu-id="999c8-2758">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="999c8-2759">**cQueries**: entier non signé 32 bits indiquant un certain nombre de requêtes en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="999c8-2759">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="999c8-2760">**cDocuments**: entier non signé 32 bits indiquant le nombre total de documents en attente d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-2760">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="999c8-2761">**cFreshTest**: entier non signé 32 bits indiquant le nombre de documents uniques avec les informations des index qui ne sont pas entièrement optimisés pour les performances.</span><span class="sxs-lookup"><span data-stu-id="999c8-2761">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="999c8-2762">**dwMergeProgress**: entier 32 bits non signé spécifiant le pourcentage d’achèvement de l’optimisation complète actuelle des index, si l’optimisation est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="999c8-2762">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="999c8-2763">DOIT être inférieur ou égal à 100.</span><span class="sxs-lookup"><span data-stu-id="999c8-2763">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="999c8-2764">**patrimoine**: état de l’indexation du contenu comme indiqué par une ou plusieurs des \_ constantes d’état ci \_ \* définies dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="999c8-2764">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="999c8-2765">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-2765">Value</span></span>                                         | <span data-ttu-id="999c8-2766">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2766">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-2767">État de l’instantané de l' \_ état ci \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-2767">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="999c8-2768">Le service d’indexation est en train d’optimiser certains des index afin de réduire l’utilisation de la mémoire et d’améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2768">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="999c8-2769">\_Fusion du maître d’état ci \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-2769">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="999c8-2770">Le service d’indexation est en cours d’optimisation complète pour tous les index.</span><span class="sxs-lookup"><span data-stu-id="999c8-2770">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="999c8-2771">Analyse du contenu de l' \_ état ci \_ \_ \_ requise 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-2771">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="999c8-2772">Certains documents de l’index ont changé et le service d’indexation doit déterminer ceux qui ont été ajoutés, modifiés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2772">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="999c8-2773">État de l' \_ \_ opération de fusion recuite d’état ci \_</span><span class="sxs-lookup"><span data-stu-id="999c8-2773">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="999c8-2774">Le service d’indexation est en train d’optimiser les index afin de réduire l’utilisation de la mémoire et d’améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2774">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="999c8-2775">Ce processus est plus complet que celui identifié par la valeur de \_ fusion de cliché instantané d’état ci \_ \_ , mais il n’est pas aussi complet que spécifié par la \_ valeur de fusion du maître d’état ci \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="999c8-2775">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="999c8-2776">Ces optimisations sont spécifiques à l’implémentation, car elles dépendent de la façon dont les données sont stockées en interne. les optimisations n’affectent pas le protocole de la même façon que le temps de réponse.</span><span class="sxs-lookup"><span data-stu-id="999c8-2776">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="999c8-2777">\_Analyse d’état ci \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="999c8-2777">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="999c8-2778">Le service d’indexation examine un répertoire ou un ensemble de répertoires pour déterminer si des fichiers ont été ajoutés, supprimés ou mis à jour depuis la dernière indexation du répertoire.</span><span class="sxs-lookup"><span data-stu-id="999c8-2778">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="999c8-2779">RÉCUPÉRATION de l’état de l’élément de configuration \_ \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="999c8-2779">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="999c8-2780">Le service démarre à partir du dernier état enregistré et est en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="999c8-2780">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="999c8-2781">\_ \_ Mémoire insuffisante de l’état ci \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="999c8-2781">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="999c8-2782">La majeure partie de la mémoire virtuelle du serveur est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="999c8-2782">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="999c8-2783">\_ \_ \_ 0x00000100 e/s haute d’état de l’élément de configuration</span><span class="sxs-lookup"><span data-stu-id="999c8-2783">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="999c8-2784">Le niveau d’activité d’entrée/sortie (e/s) sur le serveur est relativement élevé.</span><span class="sxs-lookup"><span data-stu-id="999c8-2784">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="999c8-2785">0x00000200 de la \_ fusion principale de l’état ci \_ \_ \_ suspendu</span><span class="sxs-lookup"><span data-stu-id="999c8-2785">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="999c8-2786">Le processus d’optimisation complète de tous les index en cours a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="999c8-2786">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="999c8-2787">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-2787">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="999c8-2788">État de l’élément de configuration \_ \_ en lecture \_ seule 0x00000400</span><span class="sxs-lookup"><span data-stu-id="999c8-2788">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="999c8-2789">La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="999c8-2789">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="999c8-2790">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="999c8-2791">\_0x00000800 de \_ batterie \_ d’état de l’élément de configuration</span><span class="sxs-lookup"><span data-stu-id="999c8-2791">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="999c8-2792">La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue pour économiser la durée de vie de la batterie, tout en répondant aux requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2792">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="999c8-2793">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="999c8-2794">État de l' \_ \_ utilisateur \_ actif 0x00001000</span><span class="sxs-lookup"><span data-stu-id="999c8-2794">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="999c8-2795">La partie du service d’indexation qui récupère les nouveaux documents à indexer a été suspendue en raison d’une activité élevée par l’utilisateur (clavier ou souris), mais elle répond toujours aux requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2795">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="999c8-2796">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="999c8-2797">État de l’élément de configuration à \_ \_ partir de 0x00002000</span><span class="sxs-lookup"><span data-stu-id="999c8-2797">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="999c8-2798">Le service est en cours de démarrage.</span><span class="sxs-lookup"><span data-stu-id="999c8-2798">The service is starting.</span></span> <span data-ttu-id="999c8-2799">Les requêtes peuvent être exécutées, mais l’analyse et la notification n’ont pas encore été activées.</span><span class="sxs-lookup"><span data-stu-id="999c8-2799">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="999c8-2800">Elle est fournie à des fins d’information uniquement et n’affecte pas les CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-2800">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="999c8-2801">État de l’élément de configuration \_ \_ \_ USN lecture USN 0x00004000</span><span class="sxs-lookup"><span data-stu-id="999c8-2801">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="999c8-2802">Le service n’a pas lu le journal conservé par le système de fichiers pour effectuer le suivi des modifications apportées aux fichiers ou aux répertoires d’un volume, de sorte que l’index ne soit peut-être pas à jour.</span><span class="sxs-lookup"><span data-stu-id="999c8-2802">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="999c8-2803">**cFilteredDocuments**: entier non signé 32 bits indiquant le nombre de documents indexés depuis le début de l’indexation du contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-2803">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="999c8-2804">**cTotalDocuments**: entier non signé 32 bits indiquant le nombre total de documents dans le système.</span><span class="sxs-lookup"><span data-stu-id="999c8-2804">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="999c8-2805">**cPendingScans**: entier non signé 32 bits indiquant le nombre d’opérations d’indexation de haut niveau en attente.</span><span class="sxs-lookup"><span data-stu-id="999c8-2805">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="999c8-2806">La signification de cette valeur est spécifique au fournisseur, mais des nombres plus élevés sont supposés indiquer qu’un plus grand nombre d’index est conservé.</span><span class="sxs-lookup"><span data-stu-id="999c8-2806">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="999c8-2807">*Comportement de Windows*: cette valeur est généralement égale à zéro, sauf immédiatement après le démarrage de l’indexation ou après un dépassement de la file d’attente de notification.</span><span class="sxs-lookup"><span data-stu-id="999c8-2807">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="999c8-2808">**dwIndexSize**: entier non signé 32 bits indiquant la taille, en mégaoctets, de l’index (à l’exception du cache de propriété).</span><span class="sxs-lookup"><span data-stu-id="999c8-2808">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="999c8-2809">**cUniqueKeys**: entier non signé 32 bits indiquant le nombre approximatif de clés uniques dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-2809">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="999c8-2810">**cSecQDocuments**: entier non signé 32 bits indiquant le nombre de documents que le service d’indexation réessaiera d’indexer en raison d’un échec lors de la tentative d’indexation initiale.</span><span class="sxs-lookup"><span data-stu-id="999c8-2810">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="999c8-2811">**dwPropCacheSize**: entier non signé 32 bits indiquant la taille, en mégaoctets, du cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2811">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="999c8-2812">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2812">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="999c8-2813">Le message CPMSetCatStateIn définit l’état d’un catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-2813">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="999c8-2814">Le format du message CPMSetCatStateIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-2814">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-2815">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2815">0</span></span>

<span data-ttu-id="999c8-2816">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2816">1</span></span>

<span data-ttu-id="999c8-2817">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2817">2</span></span>

<span data-ttu-id="999c8-2818">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2818">3</span></span>

<span data-ttu-id="999c8-2819">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2819">4</span></span>

<span data-ttu-id="999c8-2820">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2820">5</span></span>

<span data-ttu-id="999c8-2821">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2821">6</span></span>

<span data-ttu-id="999c8-2822">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2822">7</span></span>

<span data-ttu-id="999c8-2823">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2823">8</span></span>

<span data-ttu-id="999c8-2824">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2824">9</span></span>

<span data-ttu-id="999c8-2825">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2825">1</span></span><br/> <span data-ttu-id="999c8-2826">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2826">0</span></span><br/>

<span data-ttu-id="999c8-2827">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2827">1</span></span>

<span data-ttu-id="999c8-2828">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2828">2</span></span>

<span data-ttu-id="999c8-2829">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2829">3</span></span>

<span data-ttu-id="999c8-2830">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2830">4</span></span>

<span data-ttu-id="999c8-2831">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2831">5</span></span>

<span data-ttu-id="999c8-2832">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2832">6</span></span>

<span data-ttu-id="999c8-2833">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2833">7</span></span>

<span data-ttu-id="999c8-2834">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2834">8</span></span>

<span data-ttu-id="999c8-2835">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2835">9</span></span>

<span data-ttu-id="999c8-2836">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2836">2</span></span><br/> <span data-ttu-id="999c8-2837">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2837">0</span></span><br/>

<span data-ttu-id="999c8-2838">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2838">1</span></span>

<span data-ttu-id="999c8-2839">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2839">2</span></span>

<span data-ttu-id="999c8-2840">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2840">3</span></span>

<span data-ttu-id="999c8-2841">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2841">4</span></span>

<span data-ttu-id="999c8-2842">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2842">5</span></span>

<span data-ttu-id="999c8-2843">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2843">6</span></span>

<span data-ttu-id="999c8-2844">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2844">7</span></span>

<span data-ttu-id="999c8-2845">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2845">8</span></span>

<span data-ttu-id="999c8-2846">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2846">9</span></span>

<span data-ttu-id="999c8-2847">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2847">3</span></span><br/> <span data-ttu-id="999c8-2848">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2848">0</span></span><br/>

<span data-ttu-id="999c8-2849">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2849">1</span></span>

<span data-ttu-id="999c8-2850">\_partID</span><span class="sxs-lookup"><span data-stu-id="999c8-2850">\_partID</span></span>

<span data-ttu-id="999c8-2851">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="999c8-2851">\_dwNewState</span></span>

<span data-ttu-id="999c8-2852">\_CatName (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="999c8-2852">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="999c8-2853">**\_ partid**: doit avoir la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-2853">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="999c8-2854">**\_ dwNewState**: doit être défini sur l’une des valeurs suivantes, indiquant le nouvel État du catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-2854">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="999c8-2855">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-2855">Value</span></span>                         | <span data-ttu-id="999c8-2856">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2856">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-2857">CICAT \_ arrêté 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-2857">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="999c8-2858">Le catalogue est arrêté.</span><span class="sxs-lookup"><span data-stu-id="999c8-2858">The catalog is stopped.</span></span> <span data-ttu-id="999c8-2859">Cet État signifie qu’aucun nouveau fichier ne doit être indexé et qu’aucune requête de recherche ne doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2859">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="999c8-2860">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-2860">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="999c8-2861">Le catalogue est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="999c8-2861">The catalog is read-only.</span></span> <span data-ttu-id="999c8-2862">Aucun nouveau fichier ne doit être indexé.</span><span class="sxs-lookup"><span data-stu-id="999c8-2862">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="999c8-2863">CICAT, en \_ écriture, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-2863">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="999c8-2864">Le catalogue est accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="999c8-2864">The catalog is writable.</span></span> <span data-ttu-id="999c8-2865">Les nouveaux fichiers peuvent être indexés et les requêtes de recherche doivent être traitées.</span><span class="sxs-lookup"><span data-stu-id="999c8-2865">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="999c8-2866">CICAT \_ pas de \_ requête 0x00000008</span><span class="sxs-lookup"><span data-stu-id="999c8-2866">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="999c8-2867">Le catalogue n’est pas disponible pour l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="999c8-2867">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="999c8-2868">CICAT \_ obtient l' \_ État 0x00000010</span><span class="sxs-lookup"><span data-stu-id="999c8-2868">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="999c8-2869">L’état du catalogue ne doit pas être modifié, récupéré uniquement.</span><span class="sxs-lookup"><span data-stu-id="999c8-2869">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="999c8-2870">CICAT \_ tous les \_ 0x00000020 ouverts</span><span class="sxs-lookup"><span data-stu-id="999c8-2870">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="999c8-2871">Une vérification pour voir si tous les catalogues ont été démarrés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2871">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="999c8-2872">Si c’est le cas, le \_ champ dwOldState envoyé dans le CPMSetCatStateOut répondre à ce message est signalé comme étant différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="999c8-2872">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="999c8-2873">**\_ CatName**: nom du catalogue dont l’État doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="999c8-2873">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="999c8-2874">Le nom doit être une chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="999c8-2874">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="999c8-2875">Ce champ doit être omis si \_ dwNewState a la valeur CICAT \_ All \_ Opened.</span><span class="sxs-lookup"><span data-stu-id="999c8-2875">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="999c8-2876">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="999c8-2876">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="999c8-2877">Le message CPMSetCatStateOut est une réponse à un message CPMSetCatStateIn avec l’ancien état du catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-2877">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="999c8-2878">Le format du message CPMSetCatStateOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-2878">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-2879">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2879">0</span></span>

<span data-ttu-id="999c8-2880">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2880">1</span></span>

<span data-ttu-id="999c8-2881">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2881">2</span></span>

<span data-ttu-id="999c8-2882">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2882">3</span></span>

<span data-ttu-id="999c8-2883">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2883">4</span></span>

<span data-ttu-id="999c8-2884">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2884">5</span></span>

<span data-ttu-id="999c8-2885">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2885">6</span></span>

<span data-ttu-id="999c8-2886">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2886">7</span></span>

<span data-ttu-id="999c8-2887">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2887">8</span></span>

<span data-ttu-id="999c8-2888">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2888">9</span></span>

<span data-ttu-id="999c8-2889">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2889">1</span></span><br/> <span data-ttu-id="999c8-2890">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2890">0</span></span><br/>

<span data-ttu-id="999c8-2891">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2891">1</span></span>

<span data-ttu-id="999c8-2892">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2892">2</span></span>

<span data-ttu-id="999c8-2893">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2893">3</span></span>

<span data-ttu-id="999c8-2894">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2894">4</span></span>

<span data-ttu-id="999c8-2895">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2895">5</span></span>

<span data-ttu-id="999c8-2896">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2896">6</span></span>

<span data-ttu-id="999c8-2897">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2897">7</span></span>

<span data-ttu-id="999c8-2898">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2898">8</span></span>

<span data-ttu-id="999c8-2899">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2899">9</span></span>

<span data-ttu-id="999c8-2900">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2900">2</span></span><br/> <span data-ttu-id="999c8-2901">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2901">0</span></span><br/>

<span data-ttu-id="999c8-2902">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2902">1</span></span>

<span data-ttu-id="999c8-2903">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2903">2</span></span>

<span data-ttu-id="999c8-2904">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2904">3</span></span>

<span data-ttu-id="999c8-2905">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2905">4</span></span>

<span data-ttu-id="999c8-2906">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2906">5</span></span>

<span data-ttu-id="999c8-2907">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2907">6</span></span>

<span data-ttu-id="999c8-2908">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2908">7</span></span>

<span data-ttu-id="999c8-2909">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2909">8</span></span>

<span data-ttu-id="999c8-2910">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2910">9</span></span>

<span data-ttu-id="999c8-2911">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2911">3</span></span><br/> <span data-ttu-id="999c8-2912">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2912">0</span></span><br/>

<span data-ttu-id="999c8-2913">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2913">1</span></span>

<span data-ttu-id="999c8-2914">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="999c8-2914">\_dwOldState</span></span>



 

<span data-ttu-id="999c8-2915">**\_ dwOldState**: l’une des valeurs suivantes, indiquant l’ancien état du catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-2915">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="999c8-2916">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-2916">Value</span></span>                       | <span data-ttu-id="999c8-2917">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2917">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="999c8-2918">CICAT \_ arrêté 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-2918">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="999c8-2919">Le catalogue est arrêté.</span><span class="sxs-lookup"><span data-stu-id="999c8-2919">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="999c8-2920">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-2920">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="999c8-2921">Le catalogue est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="999c8-2921">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="999c8-2922">CICAT, en \_ écriture, 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-2922">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="999c8-2923">Le catalogue est accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="999c8-2923">The catalog is writable.</span></span>                   |
| <span data-ttu-id="999c8-2924">CICAT \_ pas de \_ requête 0x00000008</span><span class="sxs-lookup"><span data-stu-id="999c8-2924">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="999c8-2925">Le catalogue n’est pas disponible pour l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="999c8-2925">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="999c8-2926">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2926">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="999c8-2927">Le message CPMUpdateDocumentsIn indique au serveur d’indexer le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="999c8-2927">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="999c8-2928">Le serveur répondra avec l’en-tête de message du message CPMUpdateDocumentsOut, avec les résultats de la requête contenus dans le \_ champ État de l’en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="999c8-2928">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="999c8-2929">Le format du message CPMUpdateDocumentsIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-2929">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-2930">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2930">0</span></span>

<span data-ttu-id="999c8-2931">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2931">1</span></span>

<span data-ttu-id="999c8-2932">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2932">2</span></span>

<span data-ttu-id="999c8-2933">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2933">3</span></span>

<span data-ttu-id="999c8-2934">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2934">4</span></span>

<span data-ttu-id="999c8-2935">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2935">5</span></span>

<span data-ttu-id="999c8-2936">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2936">6</span></span>

<span data-ttu-id="999c8-2937">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2937">7</span></span>

<span data-ttu-id="999c8-2938">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2938">8</span></span>

<span data-ttu-id="999c8-2939">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2939">9</span></span>

<span data-ttu-id="999c8-2940">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2940">1</span></span><br/> <span data-ttu-id="999c8-2941">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2941">0</span></span><br/>

<span data-ttu-id="999c8-2942">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2942">1</span></span>

<span data-ttu-id="999c8-2943">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2943">2</span></span>

<span data-ttu-id="999c8-2944">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2944">3</span></span>

<span data-ttu-id="999c8-2945">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2945">4</span></span>

<span data-ttu-id="999c8-2946">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2946">5</span></span>

<span data-ttu-id="999c8-2947">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2947">6</span></span>

<span data-ttu-id="999c8-2948">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2948">7</span></span>

<span data-ttu-id="999c8-2949">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2949">8</span></span>

<span data-ttu-id="999c8-2950">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2950">9</span></span>

<span data-ttu-id="999c8-2951">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2951">2</span></span><br/> <span data-ttu-id="999c8-2952">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2952">0</span></span><br/>

<span data-ttu-id="999c8-2953">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2953">1</span></span>

<span data-ttu-id="999c8-2954">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2954">2</span></span>

<span data-ttu-id="999c8-2955">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2955">3</span></span>

<span data-ttu-id="999c8-2956">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2956">4</span></span>

<span data-ttu-id="999c8-2957">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2957">5</span></span>

<span data-ttu-id="999c8-2958">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2958">6</span></span>

<span data-ttu-id="999c8-2959">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2959">7</span></span>

<span data-ttu-id="999c8-2960">8</span><span class="sxs-lookup"><span data-stu-id="999c8-2960">8</span></span>

<span data-ttu-id="999c8-2961">9</span><span class="sxs-lookup"><span data-stu-id="999c8-2961">9</span></span>

<span data-ttu-id="999c8-2962">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2962">3</span></span><br/> <span data-ttu-id="999c8-2963">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2963">0</span></span><br/>

<span data-ttu-id="999c8-2964">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2964">1</span></span>

<span data-ttu-id="999c8-2965">\_indicateur (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2965">\_flag (optional)</span></span>

<span data-ttu-id="999c8-2966">\_fRootPath (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-2966">\_fRootPath (optional)</span></span>

<span data-ttu-id="999c8-2967">RootPath (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="999c8-2967">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="999c8-2968">**\_ indicateur**: type de mise à jour à effectuer.</span><span class="sxs-lookup"><span data-stu-id="999c8-2968">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="999c8-2969">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-2969">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="999c8-2970">Ce champ doit être défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-2970">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="999c8-2971">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-2971">Value</span></span>                  | <span data-ttu-id="999c8-2972">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-2972">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="999c8-2973">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-2973">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="999c8-2974">Une mise à jour incrémentielle doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2974">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="999c8-2975">UPD \_ complet 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-2975">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="999c8-2976">Une mise à jour complète doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2976">A full update is to be performed.</span></span>         |
| <span data-ttu-id="999c8-2977">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-2977">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="999c8-2978">Une nouvelle initialisation doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-2978">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="999c8-2979">**\_ fRootPath**: valeur booléenne indiquant si le champ RootPath spécifie un chemin d’accès sur lequel effectuer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="999c8-2979">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="999c8-2980">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-2980">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="999c8-2981">Ce champ doit avoir la valeur 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-2981">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="999c8-2982">Si la valeur est définie sur 0x00000001, un chemin d’accès sur lequel effectuer la mise à jour est inclus dans RootPath.</span><span class="sxs-lookup"><span data-stu-id="999c8-2982">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="999c8-2983">Si la valeur est 0x00000000, la mise à jour doit être effectuée sur tous les chemins d’accès indexés.</span><span class="sxs-lookup"><span data-stu-id="999c8-2983">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="999c8-2984">**RootPath**: nom du chemin d’accès à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="999c8-2984">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="999c8-2985">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-2985">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="999c8-2986">Le nom doit être une chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="999c8-2986">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="999c8-2987">Ce champ doit être omis si \_ fRootPath a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-2987">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="999c8-2988">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="999c8-2988">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="999c8-2989">Le message CPMForceMergeIn demande à un serveur d’effectuer les opérations de maintenance nécessaires pour améliorer les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-2989">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="999c8-2990">Le serveur répondra avec l’en-tête du message CPMForceMergeIn, avec les résultats de la requête contenus dans le \_ champ État.</span><span class="sxs-lookup"><span data-stu-id="999c8-2990">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="999c8-2991">Le format du message CPMForceMergeIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-2991">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-2992">0</span><span class="sxs-lookup"><span data-stu-id="999c8-2992">0</span></span>

<span data-ttu-id="999c8-2993">1</span><span class="sxs-lookup"><span data-stu-id="999c8-2993">1</span></span>

<span data-ttu-id="999c8-2994">2</span><span class="sxs-lookup"><span data-stu-id="999c8-2994">2</span></span>

<span data-ttu-id="999c8-2995">3</span><span class="sxs-lookup"><span data-stu-id="999c8-2995">3</span></span>

<span data-ttu-id="999c8-2996">4</span><span class="sxs-lookup"><span data-stu-id="999c8-2996">4</span></span>

<span data-ttu-id="999c8-2997">5</span><span class="sxs-lookup"><span data-stu-id="999c8-2997">5</span></span>

<span data-ttu-id="999c8-2998">6</span><span class="sxs-lookup"><span data-stu-id="999c8-2998">6</span></span>

<span data-ttu-id="999c8-2999">7</span><span class="sxs-lookup"><span data-stu-id="999c8-2999">7</span></span>

<span data-ttu-id="999c8-3000">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3000">8</span></span>

<span data-ttu-id="999c8-3001">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3001">9</span></span>

<span data-ttu-id="999c8-3002">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3002">1</span></span><br/> <span data-ttu-id="999c8-3003">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3003">0</span></span><br/>

<span data-ttu-id="999c8-3004">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3004">1</span></span>

<span data-ttu-id="999c8-3005">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3005">2</span></span>

<span data-ttu-id="999c8-3006">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3006">3</span></span>

<span data-ttu-id="999c8-3007">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3007">4</span></span>

<span data-ttu-id="999c8-3008">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3008">5</span></span>

<span data-ttu-id="999c8-3009">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3009">6</span></span>

<span data-ttu-id="999c8-3010">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3010">7</span></span>

<span data-ttu-id="999c8-3011">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3011">8</span></span>

<span data-ttu-id="999c8-3012">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3012">9</span></span>

<span data-ttu-id="999c8-3013">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3013">2</span></span><br/> <span data-ttu-id="999c8-3014">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3014">0</span></span><br/>

<span data-ttu-id="999c8-3015">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3015">1</span></span>

<span data-ttu-id="999c8-3016">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3016">2</span></span>

<span data-ttu-id="999c8-3017">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3017">3</span></span>

<span data-ttu-id="999c8-3018">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3018">4</span></span>

<span data-ttu-id="999c8-3019">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3019">5</span></span>

<span data-ttu-id="999c8-3020">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3020">6</span></span>

<span data-ttu-id="999c8-3021">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3021">7</span></span>

<span data-ttu-id="999c8-3022">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3022">8</span></span>

<span data-ttu-id="999c8-3023">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3023">9</span></span>

<span data-ttu-id="999c8-3024">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3024">3</span></span><br/> <span data-ttu-id="999c8-3025">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3025">0</span></span><br/>

<span data-ttu-id="999c8-3026">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3026">1</span></span>

<span data-ttu-id="999c8-3027">\_partId (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3027">\_partID (optional)</span></span>



 

<span data-ttu-id="999c8-3028">**\_ partid**: ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3028">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="999c8-3029">Quand ce champ est présent, il doit avoir la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-3029">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="999c8-3030">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3030">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="999c8-3031">Le message CPMConnectIn commence une session entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3031">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="999c8-3032">Le format du message CPMConnectIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3032">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3033">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3033">0</span></span>

<span data-ttu-id="999c8-3034">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3034">1</span></span>

<span data-ttu-id="999c8-3035">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3035">2</span></span>

<span data-ttu-id="999c8-3036">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3036">3</span></span>

<span data-ttu-id="999c8-3037">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3037">4</span></span>

<span data-ttu-id="999c8-3038">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3038">5</span></span>

<span data-ttu-id="999c8-3039">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3039">6</span></span>

<span data-ttu-id="999c8-3040">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3040">7</span></span>

<span data-ttu-id="999c8-3041">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3041">8</span></span>

<span data-ttu-id="999c8-3042">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3042">9</span></span>

<span data-ttu-id="999c8-3043">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3043">1</span></span><br/> <span data-ttu-id="999c8-3044">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3044">0</span></span><br/>

<span data-ttu-id="999c8-3045">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3045">1</span></span>

<span data-ttu-id="999c8-3046">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3046">2</span></span>

<span data-ttu-id="999c8-3047">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3047">3</span></span>

<span data-ttu-id="999c8-3048">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3048">4</span></span>

<span data-ttu-id="999c8-3049">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3049">5</span></span>

<span data-ttu-id="999c8-3050">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3050">6</span></span>

<span data-ttu-id="999c8-3051">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3051">7</span></span>

<span data-ttu-id="999c8-3052">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3052">8</span></span>

<span data-ttu-id="999c8-3053">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3053">9</span></span>

<span data-ttu-id="999c8-3054">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3054">2</span></span><br/> <span data-ttu-id="999c8-3055">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3055">0</span></span><br/>

<span data-ttu-id="999c8-3056">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3056">1</span></span>

<span data-ttu-id="999c8-3057">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3057">2</span></span>

<span data-ttu-id="999c8-3058">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3058">3</span></span>

<span data-ttu-id="999c8-3059">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3059">4</span></span>

<span data-ttu-id="999c8-3060">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3060">5</span></span>

<span data-ttu-id="999c8-3061">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3061">6</span></span>

<span data-ttu-id="999c8-3062">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3062">7</span></span>

<span data-ttu-id="999c8-3063">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3063">8</span></span>

<span data-ttu-id="999c8-3064">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3064">9</span></span>

<span data-ttu-id="999c8-3065">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3065">3</span></span><br/> <span data-ttu-id="999c8-3066">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3066">0</span></span><br/>

<span data-ttu-id="999c8-3067">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3067">1</span></span>

<span data-ttu-id="999c8-3068">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="999c8-3068">\_iClientVersion</span></span>

<span data-ttu-id="999c8-3069">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="999c8-3069">\_fClientIsRemote</span></span>

<span data-ttu-id="999c8-3070">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="999c8-3070">\_cbBlob1</span></span>

<span data-ttu-id="999c8-3071">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="999c8-3071">\_cbBlob2</span></span>

<span data-ttu-id="999c8-3072">\_remplissage</span><span class="sxs-lookup"><span data-stu-id="999c8-3072">\_padding</span></span>

<span data-ttu-id="999c8-3073">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3073">...</span></span>

<span data-ttu-id="999c8-3074">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3074">...</span></span>

<span data-ttu-id="999c8-3075">MachineName</span><span class="sxs-lookup"><span data-stu-id="999c8-3075">MachineName</span></span>

<span data-ttu-id="999c8-3076">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-3076">... (variable)</span></span>

<span data-ttu-id="999c8-3077">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="999c8-3077">UserName</span></span>

<span data-ttu-id="999c8-3078">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-3078">... (variable)</span></span>

<span data-ttu-id="999c8-3079">\_paddingcPropSets (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3079">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="999c8-3080">cPropSets</span><span class="sxs-lookup"><span data-stu-id="999c8-3080">cPropSets</span></span>

<span data-ttu-id="999c8-3081">PropertySet1 (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3081">PropertySet1 (variable)</span></span>

<span data-ttu-id="999c8-3082">PropertySet2 (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3082">PropertySet2 (variable)</span></span>

<span data-ttu-id="999c8-3083">\_paddingExtPropset (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3083">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="999c8-3084">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="999c8-3084">cExtPropSet</span></span>

<span data-ttu-id="999c8-3085">aPropertySets (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3085">aPropertySets (variable)</span></span>



 

<span data-ttu-id="999c8-3086">**\_ iClientVersion**: entier 32 bits qui indique si le serveur doit valider la valeur de somme de contrôle spécifiée dans le \_ champ ulChecksum des en-têtes de message pour les messages envoyés par le client.</span><span class="sxs-lookup"><span data-stu-id="999c8-3086">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="999c8-3087">Si le \_ champ iClientVersion est défini sur 0x00000008 ou une version ultérieure, le serveur doit valider la \_ valeur du champ ulChecksum pour les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="999c8-3087">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="999c8-3088">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3088">CPMConnectIn</span></span>
-   <span data-ttu-id="999c8-3089">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3089">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="999c8-3090">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3090">CPMFetchValueIn</span></span>
-   <span data-ttu-id="999c8-3091">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3091">CPMGetRowsIn</span></span>
-   <span data-ttu-id="999c8-3092">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3092">CPMSetBindingsIn</span></span>

<span data-ttu-id="999c8-3093">Pour plus d’informations sur la façon dont le serveur valide la valeur spécifiée par le client dans le champ ulChecksum pour les messages listés ci-dessus, consultez la section 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="999c8-3093">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="999c8-3094">Si la valeur est supérieure à 0x00000008, le client est supposé être en charge de la gestion des décalages 64 bits dans les messages CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-3094">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="999c8-3095">Pour plus d’informations, consultez la section 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="999c8-3095">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="999c8-3096">*Comportement de Windows : sur les clients Windows, iClientVersion est défini comme suit*:</span><span class="sxs-lookup"><span data-stu-id="999c8-3096">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="999c8-3097">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-3097">Value</span></span>      | <span data-ttu-id="999c8-3098">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-3098">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="999c8-3099">0x00000005</span><span class="sxs-lookup"><span data-stu-id="999c8-3099">0x00000005</span></span> | <span data-ttu-id="999c8-3100">Le système d’exploitation client est Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="999c8-3100">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="999c8-3101">0x00000008</span><span class="sxs-lookup"><span data-stu-id="999c8-3101">0x00000008</span></span> | <span data-ttu-id="999c8-3102">Le système d’exploitation client est soit 32 bits Windows XP, soit 32 bits Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="999c8-3102">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="999c8-3103">0x00010008</span><span class="sxs-lookup"><span data-stu-id="999c8-3103">0x00010008</span></span> | <span data-ttu-id="999c8-3104">Le système d’exploitation client est soit 64 bits Windows XP, soit 64 bits Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="999c8-3104">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="999c8-3105">\_**fClientIsRemote**: valeur booléenne indiquant si le client s’exécute sur un ordinateur différent du serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3105">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="999c8-3106">DOIT être défini sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-3106">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="999c8-3107">\_**cbBlob1**: entier non signé 32 bits indiquant la taille en octets des champs CPropSet, PropertySet1 et PropertySet2, combinée.</span><span class="sxs-lookup"><span data-stu-id="999c8-3107">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="999c8-3108">\_**cbBlob2**: entier non signé 32 bits indiquant la taille en octets des champs CExPropSet et aPropertySet, combinée.</span><span class="sxs-lookup"><span data-stu-id="999c8-3108">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="999c8-3109">\_**remplissage**: 12 octets de remplissage qui peuvent contenir des valeurs arbitraires et doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="999c8-3109">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="999c8-3110">**MachineName**: nom de l’ordinateur du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-3110">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="999c8-3111">La chaîne de nom doit être un tableau de moins de 512 caractères Unicode se terminant par un caractère null, y compris la marque de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="999c8-3111">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="999c8-3112">**Username**: chaîne qui représente le nom d’utilisateur de la personne qui exécute l’application qui a appelé ce protocole.</span><span class="sxs-lookup"><span data-stu-id="999c8-3112">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="999c8-3113">La chaîne de nom doit être un tableau de moins de 512 caractères Unicode se terminant par un caractère null en cas de concaténation avec MachineName.</span><span class="sxs-lookup"><span data-stu-id="999c8-3113">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="999c8-3114">**\_ paddingcPropSets**: ce champ doit avoir une longueur de 0 à 7 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-3114">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="999c8-3115">Le nombre d’octets doit être le nombre requis pour que l’offset d’octet du champ cPropSets à partir du début du message qui contient cette structure soit un multiple de 8.</span><span class="sxs-lookup"><span data-stu-id="999c8-3115">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="999c8-3116">La valeur des octets peut être n’importe quelle valeur arbitraire et doit être ignorée par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3116">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-3117">**cPropSets**: entier non signé 32 bits indiquant le nombre de structures CDbPropSet qui suivent ce champ.</span><span class="sxs-lookup"><span data-stu-id="999c8-3117">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="999c8-3118">Cette valeur doit être définie sur 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="999c8-3118">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="999c8-3119">**PropertySet1**: structure CDbPropSet avec GUIDPROPERTYSET contenant DBPROPSET \_ FSCIFRMWRK \_ ext (voir la section 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="999c8-3119">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="999c8-3120">**PropertySet2**: structure CDbPropSet avec GUIDPROPERTYSET contenant DBPROPSET \_ CIFRMWRKCORE \_ ext (voir la section 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="999c8-3120">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="999c8-3121">\_**PaddingExtPropset**: ce champ doit avoir une longueur de 0 à 7 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-3121">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="999c8-3122">Le nombre d’octets doit être le nombre requis pour que l’offset d’octet du champ cExtPropSets à partir du début du message qui contient cette structure soit un multiple de 8.</span><span class="sxs-lookup"><span data-stu-id="999c8-3122">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="999c8-3123">La valeur des octets peut être n’importe quelle valeur arbitraire et doit être ignorée par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3123">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-3124">**cExtPropSet**: entier non signé 32 bits indiquant le nombre de structures CDbPropSet qui suivent ce champ.</span><span class="sxs-lookup"><span data-stu-id="999c8-3124">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="999c8-3125">**aPropertySets**: tableau de structures CDbPropSet spécifiant d’autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="999c8-3125">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="999c8-3126">Le nombre d’éléments de ce tableau doit être égal à cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="999c8-3126">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="999c8-3127">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3127">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="999c8-3128">Le message CPMConnectOut contient une réponse à un message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-3128">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="999c8-3129">Le format du message CPMConnectOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3129">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3130">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3130">0</span></span>

<span data-ttu-id="999c8-3131">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3131">1</span></span>

<span data-ttu-id="999c8-3132">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3132">2</span></span>

<span data-ttu-id="999c8-3133">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3133">3</span></span>

<span data-ttu-id="999c8-3134">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3134">4</span></span>

<span data-ttu-id="999c8-3135">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3135">5</span></span>

<span data-ttu-id="999c8-3136">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3136">6</span></span>

<span data-ttu-id="999c8-3137">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3137">7</span></span>

<span data-ttu-id="999c8-3138">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3138">8</span></span>

<span data-ttu-id="999c8-3139">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3139">9</span></span>

<span data-ttu-id="999c8-3140">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3140">1</span></span><br/> <span data-ttu-id="999c8-3141">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3141">0</span></span><br/>

<span data-ttu-id="999c8-3142">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3142">1</span></span>

<span data-ttu-id="999c8-3143">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3143">2</span></span>

<span data-ttu-id="999c8-3144">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3144">3</span></span>

<span data-ttu-id="999c8-3145">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3145">4</span></span>

<span data-ttu-id="999c8-3146">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3146">5</span></span>

<span data-ttu-id="999c8-3147">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3147">6</span></span>

<span data-ttu-id="999c8-3148">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3148">7</span></span>

<span data-ttu-id="999c8-3149">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3149">8</span></span>

<span data-ttu-id="999c8-3150">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3150">9</span></span>

<span data-ttu-id="999c8-3151">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3151">2</span></span><br/> <span data-ttu-id="999c8-3152">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3152">0</span></span><br/>

<span data-ttu-id="999c8-3153">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3153">1</span></span>

<span data-ttu-id="999c8-3154">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3154">2</span></span>

<span data-ttu-id="999c8-3155">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3155">3</span></span>

<span data-ttu-id="999c8-3156">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3156">4</span></span>

<span data-ttu-id="999c8-3157">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3157">5</span></span>

<span data-ttu-id="999c8-3158">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3158">6</span></span>

<span data-ttu-id="999c8-3159">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3159">7</span></span>

<span data-ttu-id="999c8-3160">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3160">8</span></span>

<span data-ttu-id="999c8-3161">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3161">9</span></span>

<span data-ttu-id="999c8-3162">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3162">3</span></span><br/> <span data-ttu-id="999c8-3163">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3163">0</span></span><br/>

<span data-ttu-id="999c8-3164">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3164">1</span></span>

<span data-ttu-id="999c8-3165">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="999c8-3165">\_serverVersion</span></span>

<span data-ttu-id="999c8-3166">\_réservé (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3166">\_reserved (variable)</span></span>



 

<span data-ttu-id="999c8-3167">**\_ ServerVersion**:</span><span class="sxs-lookup"><span data-stu-id="999c8-3167">**\_serverVersion**:</span></span>

<span data-ttu-id="999c8-3168">Entier 32 bits, indiquant si le serveur peut prendre en charge les décalages 64 bits *.*</span><span class="sxs-lookup"><span data-stu-id="999c8-3168">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="999c8-3169">Pour plus d’informations, consultez la section 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="999c8-3169">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="999c8-3170">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-3170">Value</span></span>      | <span data-ttu-id="999c8-3171">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-3171">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="999c8-3172">0x00000007</span><span class="sxs-lookup"><span data-stu-id="999c8-3172">0x00000007</span></span> | <span data-ttu-id="999c8-3173">Le serveur peut uniquement envoyer des décalages 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-3173">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="999c8-3174">0x00010007</span><span class="sxs-lookup"><span data-stu-id="999c8-3174">0x00010007</span></span> | <span data-ttu-id="999c8-3175">Le serveur peut envoyer des décalages 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-3175">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="999c8-3176">**\_ réservé**: réservé.</span><span class="sxs-lookup"><span data-stu-id="999c8-3176">**\_reserved**: Reserved.</span></span> <span data-ttu-id="999c8-3177">Le serveur peut envoyer un nombre arbitraire de valeurs arbitraires et le client doit ignorer ces valeurs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="999c8-3177">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="999c8-3178">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3178">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="999c8-3179">Le message CPMCreateQueryIn crée une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3179">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="999c8-3180">Le format du message CPMCreateQueryIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3180">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3181">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3181">0</span></span>

<span data-ttu-id="999c8-3182">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3182">1</span></span>

<span data-ttu-id="999c8-3183">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3183">2</span></span>

<span data-ttu-id="999c8-3184">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3184">3</span></span>

<span data-ttu-id="999c8-3185">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3185">4</span></span>

<span data-ttu-id="999c8-3186">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3186">5</span></span>

<span data-ttu-id="999c8-3187">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3187">6</span></span>

<span data-ttu-id="999c8-3188">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3188">7</span></span>

<span data-ttu-id="999c8-3189">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3189">8</span></span>

<span data-ttu-id="999c8-3190">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3190">9</span></span>

<span data-ttu-id="999c8-3191">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3191">1</span></span><br/> <span data-ttu-id="999c8-3192">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3192">0</span></span><br/>

<span data-ttu-id="999c8-3193">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3193">1</span></span>

<span data-ttu-id="999c8-3194">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3194">2</span></span>

<span data-ttu-id="999c8-3195">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3195">3</span></span>

<span data-ttu-id="999c8-3196">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3196">4</span></span>

<span data-ttu-id="999c8-3197">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3197">5</span></span>

<span data-ttu-id="999c8-3198">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3198">6</span></span>

<span data-ttu-id="999c8-3199">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3199">7</span></span>

<span data-ttu-id="999c8-3200">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3200">8</span></span>

<span data-ttu-id="999c8-3201">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3201">9</span></span>

<span data-ttu-id="999c8-3202">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3202">2</span></span><br/> <span data-ttu-id="999c8-3203">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3203">0</span></span><br/>

<span data-ttu-id="999c8-3204">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3204">1</span></span>

<span data-ttu-id="999c8-3205">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3205">2</span></span>

<span data-ttu-id="999c8-3206">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3206">3</span></span>

<span data-ttu-id="999c8-3207">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3207">4</span></span>

<span data-ttu-id="999c8-3208">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3208">5</span></span>

<span data-ttu-id="999c8-3209">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3209">6</span></span>

<span data-ttu-id="999c8-3210">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3210">7</span></span>

<span data-ttu-id="999c8-3211">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3211">8</span></span>

<span data-ttu-id="999c8-3212">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3212">9</span></span>

<span data-ttu-id="999c8-3213">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3213">3</span></span><br/> <span data-ttu-id="999c8-3214">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3214">0</span></span><br/>

<span data-ttu-id="999c8-3215">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3215">1</span></span>

<span data-ttu-id="999c8-3216">Taille</span><span class="sxs-lookup"><span data-stu-id="999c8-3216">Size</span></span>

<span data-ttu-id="999c8-3217">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="999c8-3217">CColumnSetPresent</span></span>

<span data-ttu-id="999c8-3218">ColumnSet (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3218">ColumnSet (optional)</span></span>

<span data-ttu-id="999c8-3219">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-3219">... (variable)</span></span>

<span data-ttu-id="999c8-3220">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3220">CRestrictionPresent.</span></span>

<span data-ttu-id="999c8-3221">Restriction (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3221">Restriction (optional)</span></span>

<span data-ttu-id="999c8-3222">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-3222">... (variable)</span></span>

<span data-ttu-id="999c8-3223">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="999c8-3223">CSortSetPresent</span></span>

<span data-ttu-id="999c8-3224">SortSet (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3224">SortSet (optional)</span></span>

<span data-ttu-id="999c8-3225">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-3225">... (variable)</span></span>

<span data-ttu-id="999c8-3226">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="999c8-3226">CCategorizationSetPresent</span></span>

<span data-ttu-id="999c8-3227">CategorizationSet (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3227">CategorizationSet (optional)</span></span>

<span data-ttu-id="999c8-3228">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-3228">... (variable)</span></span>

<span data-ttu-id="999c8-3229">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="999c8-3229">RowSetProperties</span></span>

<span data-ttu-id="999c8-3230">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3230">...</span></span>

<span data-ttu-id="999c8-3231">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3231">...</span></span>

<span data-ttu-id="999c8-3232">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3232">...</span></span>

<span data-ttu-id="999c8-3233">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3233">...</span></span>

<span data-ttu-id="999c8-3234">PidMapper (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3234">PidMapper (variable)</span></span>



 

<span data-ttu-id="999c8-3235">**Size**: entier non signé 32 bits indiquant le nombre d’octets entre le début de ce champ et la fin du message.</span><span class="sxs-lookup"><span data-stu-id="999c8-3235">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="999c8-3236">**CColumnSetPresent**: champ d’octets indiquant si le champ ColumnSet est présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3236">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="999c8-3237">Ce champ doit être défini sur 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-3237">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="999c8-3238">Si la valeur est définie sur 0x01, le champ CColumnSet doit être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3238">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="999c8-3239">Si la valeur est 0x00, elle doit être absente.</span><span class="sxs-lookup"><span data-stu-id="999c8-3239">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="999c8-3240">**ColumnSet**: structure CColumnSet contenant les numéros de colonne dans lesquels les propriétés de CPidMapper doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="999c8-3240">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="999c8-3241">**CRestrictionPresent**: champ d’octets indiquant si le champ de restriction est présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3241">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="999c8-3242">Si vous définissez une valeur différente de zéro, le champ de restriction doit être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3242">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="999c8-3243">Si la valeur est 0x00, la restriction doit être absente.</span><span class="sxs-lookup"><span data-stu-id="999c8-3243">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="999c8-3244">**Restriction**: structure CRestriction contenant l’arborescence de commandes de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3244">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="999c8-3245">**CSortSetPresent**: champ d’octets indiquant si le champ SortSet est présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3245">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="999c8-3246">Si vous définissez une valeur différente de zéro, le champ SortSet doit être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3246">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="999c8-3247">Si la valeur est 0x00, SortSet doit être absent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3247">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="999c8-3248">**SortSet**: structure CSortSet indiquant l’ordre de tri de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3248">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="999c8-3249">**CCategorizationSetPresent**: champ d’octets indiquant si le champ CCategorizationSet est présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3249">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="999c8-3250">Si vous définissez une valeur différente de zéro, le champ CCategorizationSet doit être présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3250">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="999c8-3251">Si la valeur est 0x00, CCategorizationSet doit être absent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3251">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="999c8-3252">**CCategorizationSet**: structure CCategorizationSet qui contient les groupes de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3252">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="999c8-3253">**RowSetProperties**: structure CRowsetProperties fournissant des informations de configuration pour la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3253">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="999c8-3254">**PidMapper**: structure CPidMapper contenant les propriétés à retourner dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3254">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="999c8-3255">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3255">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="999c8-3256">Le message CPMCreateQueryOut contient une réponse à un message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-3256">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="999c8-3257">Le format du message CPMCreateQueryOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3257">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3258">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3258">0</span></span>

<span data-ttu-id="999c8-3259">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3259">1</span></span>

<span data-ttu-id="999c8-3260">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3260">2</span></span>

<span data-ttu-id="999c8-3261">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3261">3</span></span>

<span data-ttu-id="999c8-3262">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3262">4</span></span>

<span data-ttu-id="999c8-3263">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3263">5</span></span>

<span data-ttu-id="999c8-3264">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3264">6</span></span>

<span data-ttu-id="999c8-3265">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3265">7</span></span>

<span data-ttu-id="999c8-3266">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3266">8</span></span>

<span data-ttu-id="999c8-3267">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3267">9</span></span>

<span data-ttu-id="999c8-3268">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3268">1</span></span><br/> <span data-ttu-id="999c8-3269">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3269">0</span></span><br/>

<span data-ttu-id="999c8-3270">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3270">1</span></span>

<span data-ttu-id="999c8-3271">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3271">2</span></span>

<span data-ttu-id="999c8-3272">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3272">3</span></span>

<span data-ttu-id="999c8-3273">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3273">4</span></span>

<span data-ttu-id="999c8-3274">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3274">5</span></span>

<span data-ttu-id="999c8-3275">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3275">6</span></span>

<span data-ttu-id="999c8-3276">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3276">7</span></span>

<span data-ttu-id="999c8-3277">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3277">8</span></span>

<span data-ttu-id="999c8-3278">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3278">9</span></span>

<span data-ttu-id="999c8-3279">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3279">2</span></span><br/> <span data-ttu-id="999c8-3280">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3280">0</span></span><br/>

<span data-ttu-id="999c8-3281">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3281">1</span></span>

<span data-ttu-id="999c8-3282">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3282">2</span></span>

<span data-ttu-id="999c8-3283">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3283">3</span></span>

<span data-ttu-id="999c8-3284">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3284">4</span></span>

<span data-ttu-id="999c8-3285">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3285">5</span></span>

<span data-ttu-id="999c8-3286">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3286">6</span></span>

<span data-ttu-id="999c8-3287">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3287">7</span></span>

<span data-ttu-id="999c8-3288">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3288">8</span></span>

<span data-ttu-id="999c8-3289">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3289">9</span></span>

<span data-ttu-id="999c8-3290">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3290">3</span></span><br/> <span data-ttu-id="999c8-3291">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3291">0</span></span><br/>

<span data-ttu-id="999c8-3292">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3292">1</span></span>

<span data-ttu-id="999c8-3293">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="999c8-3293">\_fTrueSequential</span></span>

<span data-ttu-id="999c8-3294">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="999c8-3294">\_fWorkIdUnique</span></span>

<span data-ttu-id="999c8-3295">aCursors</span><span class="sxs-lookup"><span data-stu-id="999c8-3295">aCursors</span></span>



 

<span data-ttu-id="999c8-3296">**\_ fTrueSequential**: valeur booléenne informatif indiquant si la requête peut être supposée fournir des résultats plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="999c8-3296">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="999c8-3297">Lorsqu’il est défini sur 0x00000001 pour la requête fournie dans CPMCreateQueryIn, le serveur peut utiliser l’index de telle sorte que les résultats de la requête seront probablement remis plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="999c8-3297">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="999c8-3298">Lorsque la valeur est 0x00000000, il y a une latence plus importante dans la transmission des résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3298">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="999c8-3299">Ne doit pas être défini sur une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3299">MUST not be set to any other value.</span></span>

<span data-ttu-id="999c8-3300">**\_ fWorkIdUnique**: valeur booléenne indiquant si les identificateurs de document pointés par les curseurs sont uniques dans tous les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3300">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="999c8-3301">Si la valeur est 0x00000001, les identificateurs sont uniques.</span><span class="sxs-lookup"><span data-stu-id="999c8-3301">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="999c8-3302">Si la valeur est 0x00000000, elles sont uniques uniquement dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3302">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="999c8-3303">**aCursors**: tableau d’entiers non signés 32 bits représentant les handles des curseurs, avec le nombre d’éléments égal au nombre de catégories dans le champ CategorizationSet du message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-3303">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="999c8-3304">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3304">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="999c8-3305">Le message CPMGetQueryStatusIn demande l’état d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3305">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="999c8-3306">Le format du message CPMGetQueryStatusIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3306">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3307">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3307">0</span></span>

<span data-ttu-id="999c8-3308">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3308">1</span></span>

<span data-ttu-id="999c8-3309">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3309">2</span></span>

<span data-ttu-id="999c8-3310">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3310">3</span></span>

<span data-ttu-id="999c8-3311">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3311">4</span></span>

<span data-ttu-id="999c8-3312">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3312">5</span></span>

<span data-ttu-id="999c8-3313">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3313">6</span></span>

<span data-ttu-id="999c8-3314">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3314">7</span></span>

<span data-ttu-id="999c8-3315">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3315">8</span></span>

<span data-ttu-id="999c8-3316">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3316">9</span></span>

<span data-ttu-id="999c8-3317">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3317">1</span></span><br/> <span data-ttu-id="999c8-3318">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3318">0</span></span><br/>

<span data-ttu-id="999c8-3319">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3319">1</span></span>

<span data-ttu-id="999c8-3320">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3320">2</span></span>

<span data-ttu-id="999c8-3321">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3321">3</span></span>

<span data-ttu-id="999c8-3322">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3322">4</span></span>

<span data-ttu-id="999c8-3323">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3323">5</span></span>

<span data-ttu-id="999c8-3324">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3324">6</span></span>

<span data-ttu-id="999c8-3325">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3325">7</span></span>

<span data-ttu-id="999c8-3326">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3326">8</span></span>

<span data-ttu-id="999c8-3327">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3327">9</span></span>

<span data-ttu-id="999c8-3328">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3328">2</span></span><br/> <span data-ttu-id="999c8-3329">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3329">0</span></span><br/>

<span data-ttu-id="999c8-3330">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3330">1</span></span>

<span data-ttu-id="999c8-3331">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3331">2</span></span>

<span data-ttu-id="999c8-3332">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3332">3</span></span>

<span data-ttu-id="999c8-3333">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3333">4</span></span>

<span data-ttu-id="999c8-3334">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3334">5</span></span>

<span data-ttu-id="999c8-3335">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3335">6</span></span>

<span data-ttu-id="999c8-3336">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3336">7</span></span>

<span data-ttu-id="999c8-3337">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3337">8</span></span>

<span data-ttu-id="999c8-3338">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3338">9</span></span>

<span data-ttu-id="999c8-3339">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3339">3</span></span><br/> <span data-ttu-id="999c8-3340">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3340">0</span></span><br/>

<span data-ttu-id="999c8-3341">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3341">1</span></span>

<span data-ttu-id="999c8-3342">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="999c8-3342">\_hCursor</span></span>



 

<span data-ttu-id="999c8-3343">**\_ hCursor**: entier non signé 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les informations d’État doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="999c8-3343">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="999c8-3344">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3344">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="999c8-3345">Le message CPMGetQueryStatusOut répond à un message CPMGetQueryStatusIn avec l’état de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3345">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="999c8-3346">Le format du message CPMGetQueryStatusOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3346">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3347">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3347">0</span></span>

<span data-ttu-id="999c8-3348">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3348">1</span></span>

<span data-ttu-id="999c8-3349">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3349">2</span></span>

<span data-ttu-id="999c8-3350">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3350">3</span></span>

<span data-ttu-id="999c8-3351">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3351">4</span></span>

<span data-ttu-id="999c8-3352">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3352">5</span></span>

<span data-ttu-id="999c8-3353">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3353">6</span></span>

<span data-ttu-id="999c8-3354">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3354">7</span></span>

<span data-ttu-id="999c8-3355">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3355">8</span></span>

<span data-ttu-id="999c8-3356">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3356">9</span></span>

<span data-ttu-id="999c8-3357">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3357">1</span></span><br/> <span data-ttu-id="999c8-3358">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3358">0</span></span><br/>

<span data-ttu-id="999c8-3359">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3359">1</span></span>

<span data-ttu-id="999c8-3360">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3360">2</span></span>

<span data-ttu-id="999c8-3361">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3361">3</span></span>

<span data-ttu-id="999c8-3362">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3362">4</span></span>

<span data-ttu-id="999c8-3363">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3363">5</span></span>

<span data-ttu-id="999c8-3364">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3364">6</span></span>

<span data-ttu-id="999c8-3365">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3365">7</span></span>

<span data-ttu-id="999c8-3366">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3366">8</span></span>

<span data-ttu-id="999c8-3367">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3367">9</span></span>

<span data-ttu-id="999c8-3368">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3368">2</span></span><br/> <span data-ttu-id="999c8-3369">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3369">0</span></span><br/>

<span data-ttu-id="999c8-3370">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3370">1</span></span>

<span data-ttu-id="999c8-3371">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3371">2</span></span>

<span data-ttu-id="999c8-3372">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3372">3</span></span>

<span data-ttu-id="999c8-3373">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3373">4</span></span>

<span data-ttu-id="999c8-3374">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3374">5</span></span>

<span data-ttu-id="999c8-3375">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3375">6</span></span>

<span data-ttu-id="999c8-3376">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3376">7</span></span>

<span data-ttu-id="999c8-3377">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3377">8</span></span>

<span data-ttu-id="999c8-3378">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3378">9</span></span>

<span data-ttu-id="999c8-3379">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3379">3</span></span><br/> <span data-ttu-id="999c8-3380">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3380">0</span></span><br/>

<span data-ttu-id="999c8-3381">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3381">1</span></span>

<span data-ttu-id="999c8-3382">\_État</span><span class="sxs-lookup"><span data-stu-id="999c8-3382">\_Status</span></span>



 

<span data-ttu-id="999c8-3383">**\_ État**: masque de sous-masque des valeurs définies dans les tableaux ci-dessous, qui décrit la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3383">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="999c8-3384">Le tableau suivant répertorie les \_ \* valeurs stat obtenues en effectuant une opération and au niveau du bit sur \_ Status avec 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="999c8-3384">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="999c8-3385">Le résultat doit être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="999c8-3385">The result MUST be one of the following:</span></span>



| <span data-ttu-id="999c8-3386">Constante</span><span class="sxs-lookup"><span data-stu-id="999c8-3386">Constant</span></span>                 | <span data-ttu-id="999c8-3387">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-3387">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-3388">STAT \_ occupées 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-3388">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="999c8-3389">La requête asynchrone est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="999c8-3389">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="999c8-3390">\_Erreur stat 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-3390">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="999c8-3391">La requête est dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3391">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="999c8-3392">STATISTIQUES \_ terminées 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-3392">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="999c8-3393">La requête est terminée.</span><span class="sxs-lookup"><span data-stu-id="999c8-3393">The query is complete.</span></span>                                                            |
| <span data-ttu-id="999c8-3394">STATISTIQUES d' \_ actualisation 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-3394">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="999c8-3395">La requête est terminée, mais les mises à jour entraînent des calculs de requête supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="999c8-3395">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="999c8-3396">Le tableau suivant répertorie les bits STAT supplémentaires \_ \* qui peuvent être définis indépendamment.</span><span class="sxs-lookup"><span data-stu-id="999c8-3396">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="999c8-3397">Constante</span><span class="sxs-lookup"><span data-stu-id="999c8-3397">Constant</span></span>                                    | <span data-ttu-id="999c8-3398">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-3398">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c8-3399">\_Mots parasites statistiques \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="999c8-3399">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="999c8-3400">Les mots parasites ont été remplacés par des caractères génériques dans la requête de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-3400">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="999c8-3401">\_Contenu stat \_ obsolète \_ \_</span><span class="sxs-lookup"><span data-stu-id="999c8-3401">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="999c8-3402">Les résultats de la requête sont peut-être incorrects, car la requête impliquait des fichiers modifiés, mais non indexés.</span><span class="sxs-lookup"><span data-stu-id="999c8-3402">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="999c8-3403">Actualisation des statistiques \_ \_ 0x00000040 incomplète</span><span class="sxs-lookup"><span data-stu-id="999c8-3403">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="999c8-3404">Les résultats de la requête sont peut-être incorrects, car la requête impliquait la modification et la réindexation des fichiers dont le contenu n’était pas inclus.</span><span class="sxs-lookup"><span data-stu-id="999c8-3404">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="999c8-3405">\_Requête de contenu stat \_ \_ incomplète 0x00000080</span><span class="sxs-lookup"><span data-stu-id="999c8-3405">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="999c8-3406">La requête de contenu était trop complexe pour être exécutée ou une énumération requise au lieu d’utiliser l’index de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-3406">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="999c8-3407">Limite de durée des statistiques \_ \_ \_ dépassée 0x00000100</span><span class="sxs-lookup"><span data-stu-id="999c8-3407">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="999c8-3408">Les résultats de la requête sont peut-être incorrects, car la durée d’exécution de la requête a atteint le délai maximal autorisé.</span><span class="sxs-lookup"><span data-stu-id="999c8-3408">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="999c8-3409">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3409">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="999c8-3410">Le message CPMGetQueryStatusExIn demande l’état d’une requête et des informations supplémentaires, telles que le nombre de documents qui ont été indexés, le nombre de documents restant à indexer, etc.</span><span class="sxs-lookup"><span data-stu-id="999c8-3410">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="999c8-3411">Le format du message CPMGetQueryStatusExIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3411">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3412">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3412">0</span></span>

<span data-ttu-id="999c8-3413">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3413">1</span></span>

<span data-ttu-id="999c8-3414">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3414">2</span></span>

<span data-ttu-id="999c8-3415">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3415">3</span></span>

<span data-ttu-id="999c8-3416">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3416">4</span></span>

<span data-ttu-id="999c8-3417">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3417">5</span></span>

<span data-ttu-id="999c8-3418">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3418">6</span></span>

<span data-ttu-id="999c8-3419">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3419">7</span></span>

<span data-ttu-id="999c8-3420">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3420">8</span></span>

<span data-ttu-id="999c8-3421">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3421">9</span></span>

<span data-ttu-id="999c8-3422">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3422">1</span></span><br/> <span data-ttu-id="999c8-3423">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3423">0</span></span><br/>

<span data-ttu-id="999c8-3424">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3424">1</span></span>

<span data-ttu-id="999c8-3425">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3425">2</span></span>

<span data-ttu-id="999c8-3426">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3426">3</span></span>

<span data-ttu-id="999c8-3427">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3427">4</span></span>

<span data-ttu-id="999c8-3428">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3428">5</span></span>

<span data-ttu-id="999c8-3429">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3429">6</span></span>

<span data-ttu-id="999c8-3430">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3430">7</span></span>

<span data-ttu-id="999c8-3431">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3431">8</span></span>

<span data-ttu-id="999c8-3432">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3432">9</span></span>

<span data-ttu-id="999c8-3433">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3433">2</span></span><br/> <span data-ttu-id="999c8-3434">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3434">0</span></span><br/>

<span data-ttu-id="999c8-3435">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3435">1</span></span>

<span data-ttu-id="999c8-3436">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3436">2</span></span>

<span data-ttu-id="999c8-3437">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3437">3</span></span>

<span data-ttu-id="999c8-3438">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3438">4</span></span>

<span data-ttu-id="999c8-3439">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3439">5</span></span>

<span data-ttu-id="999c8-3440">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3440">6</span></span>

<span data-ttu-id="999c8-3441">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3441">7</span></span>

<span data-ttu-id="999c8-3442">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3442">8</span></span>

<span data-ttu-id="999c8-3443">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3443">9</span></span>

<span data-ttu-id="999c8-3444">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3444">3</span></span><br/> <span data-ttu-id="999c8-3445">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3445">0</span></span><br/>

<span data-ttu-id="999c8-3446">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3446">1</span></span>

<span data-ttu-id="999c8-3447">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="999c8-3447">\_hCursor</span></span>

<span data-ttu-id="999c8-3448">\_bmk</span><span class="sxs-lookup"><span data-stu-id="999c8-3448">\_bmk</span></span>



 

<span data-ttu-id="999c8-3449">**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les informations d’État doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="999c8-3449">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="999c8-3450">**\_ BMK**: valeur 32 bits indiquant le descripteur d’un signet dont la position doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="999c8-3450">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="999c8-3451">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3451">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="999c8-3452">Le message CPMGetQueryStatusExOut répond à un message CPMGetQueryStatusExIn avec l’état de la requête et d’autres informations d’État, comme indiqué dans le diagramme ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="999c8-3452">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="999c8-3453">Le format du message CPMGetQueryStatusExOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3453">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3454">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3454">0</span></span>

<span data-ttu-id="999c8-3455">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3455">1</span></span>

<span data-ttu-id="999c8-3456">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3456">2</span></span>

<span data-ttu-id="999c8-3457">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3457">3</span></span>

<span data-ttu-id="999c8-3458">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3458">4</span></span>

<span data-ttu-id="999c8-3459">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3459">5</span></span>

<span data-ttu-id="999c8-3460">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3460">6</span></span>

<span data-ttu-id="999c8-3461">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3461">7</span></span>

<span data-ttu-id="999c8-3462">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3462">8</span></span>

<span data-ttu-id="999c8-3463">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3463">9</span></span>

<span data-ttu-id="999c8-3464">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3464">1</span></span><br/> <span data-ttu-id="999c8-3465">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3465">0</span></span><br/>

<span data-ttu-id="999c8-3466">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3466">1</span></span>

<span data-ttu-id="999c8-3467">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3467">2</span></span>

<span data-ttu-id="999c8-3468">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3468">3</span></span>

<span data-ttu-id="999c8-3469">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3469">4</span></span>

<span data-ttu-id="999c8-3470">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3470">5</span></span>

<span data-ttu-id="999c8-3471">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3471">6</span></span>

<span data-ttu-id="999c8-3472">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3472">7</span></span>

<span data-ttu-id="999c8-3473">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3473">8</span></span>

<span data-ttu-id="999c8-3474">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3474">9</span></span>

<span data-ttu-id="999c8-3475">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3475">2</span></span><br/> <span data-ttu-id="999c8-3476">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3476">0</span></span><br/>

<span data-ttu-id="999c8-3477">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3477">1</span></span>

<span data-ttu-id="999c8-3478">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3478">2</span></span>

<span data-ttu-id="999c8-3479">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3479">3</span></span>

<span data-ttu-id="999c8-3480">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3480">4</span></span>

<span data-ttu-id="999c8-3481">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3481">5</span></span>

<span data-ttu-id="999c8-3482">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3482">6</span></span>

<span data-ttu-id="999c8-3483">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3483">7</span></span>

<span data-ttu-id="999c8-3484">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3484">8</span></span>

<span data-ttu-id="999c8-3485">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3485">9</span></span>

<span data-ttu-id="999c8-3486">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3486">3</span></span><br/> <span data-ttu-id="999c8-3487">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3487">0</span></span><br/>

<span data-ttu-id="999c8-3488">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3488">1</span></span>

<span data-ttu-id="999c8-3489">\_État</span><span class="sxs-lookup"><span data-stu-id="999c8-3489">\_Status</span></span>

<span data-ttu-id="999c8-3490">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="999c8-3490">\_cFilteredDocuments</span></span>

<span data-ttu-id="999c8-3491">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="999c8-3491">\_cDocumentsToFilter</span></span>

<span data-ttu-id="999c8-3492">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="999c8-3492">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="999c8-3493">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="999c8-3493">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="999c8-3494">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="999c8-3494">\_iRowBmk</span></span>

<span data-ttu-id="999c8-3495">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="999c8-3495">\_cRowsTotal</span></span>



 

<span data-ttu-id="999c8-3496">**\_ État**: l’une des statistiques \_ \* valeurs spécifiées dans la section 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="999c8-3496">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="999c8-3497">**\_ cFilteredDocuments**: entier non signé 32 bits indiquant le nombre de documents qui ont été indexés</span><span class="sxs-lookup"><span data-stu-id="999c8-3497">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="999c8-3498">**\_ cDocumentsToFilter**: entier non signé 32 bits indiquant le nombre de documents restant à indexer.</span><span class="sxs-lookup"><span data-stu-id="999c8-3498">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="999c8-3499">**\_ dwRatioFinishedDenominator**: entier non signé 32 bits indiquant le dénominateur du rapport de documents dont la requête a terminé le traitement.</span><span class="sxs-lookup"><span data-stu-id="999c8-3499">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="999c8-3500">**\_ dwRatioFinishedNumerator**: entier non signé 32 bits indiquant le numérateur du rapport de documents dont la requête a terminé le traitement.</span><span class="sxs-lookup"><span data-stu-id="999c8-3500">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="999c8-3501">**\_ iRowBmk**: entier non signé 32 bits indiquant la position approximative du signet dans l’ensemble de lignes en termes de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3501">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="999c8-3502">**\_ cRowsTotal**: entier non signé 32 bits spécifiant le nombre total de lignes dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3502">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="999c8-3503">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3503">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="999c8-3504">Le message CPMSetBindingsIn demande la liaison de colonnes à un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3504">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="999c8-3505">Le serveur répond au message de requête CPMSetBindingsIn à l’aide de la section d’en-tête du message CPMBindingsIn avec les résultats de la requête contenue dans le \_ champ État.</span><span class="sxs-lookup"><span data-stu-id="999c8-3505">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="999c8-3506">Le format du message CPMSetBindingsIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3506">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3507">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3507">0</span></span>

<span data-ttu-id="999c8-3508">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3508">1</span></span>

<span data-ttu-id="999c8-3509">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3509">2</span></span>

<span data-ttu-id="999c8-3510">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3510">3</span></span>

<span data-ttu-id="999c8-3511">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3511">4</span></span>

<span data-ttu-id="999c8-3512">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3512">5</span></span>

<span data-ttu-id="999c8-3513">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3513">6</span></span>

<span data-ttu-id="999c8-3514">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3514">7</span></span>

<span data-ttu-id="999c8-3515">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3515">8</span></span>

<span data-ttu-id="999c8-3516">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3516">9</span></span>

<span data-ttu-id="999c8-3517">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3517">1</span></span><br/> <span data-ttu-id="999c8-3518">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3518">0</span></span><br/>

<span data-ttu-id="999c8-3519">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3519">1</span></span>

<span data-ttu-id="999c8-3520">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3520">2</span></span>

<span data-ttu-id="999c8-3521">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3521">3</span></span>

<span data-ttu-id="999c8-3522">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3522">4</span></span>

<span data-ttu-id="999c8-3523">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3523">5</span></span>

<span data-ttu-id="999c8-3524">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3524">6</span></span>

<span data-ttu-id="999c8-3525">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3525">7</span></span>

<span data-ttu-id="999c8-3526">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3526">8</span></span>

<span data-ttu-id="999c8-3527">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3527">9</span></span>

<span data-ttu-id="999c8-3528">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3528">2</span></span><br/> <span data-ttu-id="999c8-3529">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3529">0</span></span><br/>

<span data-ttu-id="999c8-3530">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3530">1</span></span>

<span data-ttu-id="999c8-3531">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3531">2</span></span>

<span data-ttu-id="999c8-3532">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3532">3</span></span>

<span data-ttu-id="999c8-3533">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3533">4</span></span>

<span data-ttu-id="999c8-3534">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3534">5</span></span>

<span data-ttu-id="999c8-3535">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3535">6</span></span>

<span data-ttu-id="999c8-3536">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3536">7</span></span>

<span data-ttu-id="999c8-3537">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3537">8</span></span>

<span data-ttu-id="999c8-3538">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3538">9</span></span>

<span data-ttu-id="999c8-3539">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3539">3</span></span><br/> <span data-ttu-id="999c8-3540">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3540">0</span></span><br/>

<span data-ttu-id="999c8-3541">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3541">1</span></span>

<span data-ttu-id="999c8-3542">\_hCursor (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3542">\_hCursor (optional)</span></span>

<span data-ttu-id="999c8-3543">\_cbRow (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3543">\_cbRow (optional)</span></span>

<span data-ttu-id="999c8-3544">\_cbBindingDesc (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3544">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="999c8-3545">\_factice (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3545">\_dummy (optional)</span></span>

<span data-ttu-id="999c8-3546">cColumns (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-3546">cColumns (optional)</span></span>

<span data-ttu-id="999c8-3547">aColumns (variable, facultative)</span><span class="sxs-lookup"><span data-stu-id="999c8-3547">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="999c8-3548">**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut qui identifie la ligne pour laquelle définir des liaisons.</span><span class="sxs-lookup"><span data-stu-id="999c8-3548">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="999c8-3549">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3549">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="999c8-3550">**\_ cbRow**: entier non signé 32 bits indiquant la taille, en octets, d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-3550">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="999c8-3551">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3551">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="999c8-3552">**\_ cbBindingDesc**: entier non signé 32 bits indiquant la longueur, en octets, des champs qui suivent le \_ champ factice.</span><span class="sxs-lookup"><span data-stu-id="999c8-3552">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="999c8-3553">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3553">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="999c8-3554">**\_ factice**: ce champ n’est pas utilisé et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="999c8-3554">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="999c8-3555">Il peut être défini sur n’importe quelle valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-3555">It can be set to any arbitrary value.</span></span> <span data-ttu-id="999c8-3556">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="999c8-3557">**CColumns**: entier non signé 32 bits indiquant le nombre d’éléments dans le tableau aColumns.</span><span class="sxs-lookup"><span data-stu-id="999c8-3557">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="999c8-3558">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3558">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="999c8-3559">**aColumns**: tableau des structures CTableColumn décrivant les colonnes d’une ligne dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3559">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="999c8-3560">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3560">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="999c8-3561">Les structures dans le tableau doivent être séparées par 0 à 3 octets de remplissage, de sorte que chaque structure a un alignement sur 4 octets à partir du début d’un message.</span><span class="sxs-lookup"><span data-stu-id="999c8-3561">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="999c8-3562">Ces octets de remplissage peuvent être des valeurs arbitraires et doivent être ignorés à la réception.</span><span class="sxs-lookup"><span data-stu-id="999c8-3562">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="999c8-3563">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3563">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="999c8-3564">Le message CPMGetRowsIn demande des lignes d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3564">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="999c8-3565">Le format du message CPMGetRowsIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3565">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3566">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3566">0</span></span>

<span data-ttu-id="999c8-3567">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3567">1</span></span>

<span data-ttu-id="999c8-3568">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3568">2</span></span>

<span data-ttu-id="999c8-3569">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3569">3</span></span>

<span data-ttu-id="999c8-3570">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3570">4</span></span>

<span data-ttu-id="999c8-3571">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3571">5</span></span>

<span data-ttu-id="999c8-3572">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3572">6</span></span>

<span data-ttu-id="999c8-3573">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3573">7</span></span>

<span data-ttu-id="999c8-3574">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3574">8</span></span>

<span data-ttu-id="999c8-3575">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3575">9</span></span>

<span data-ttu-id="999c8-3576">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3576">1</span></span><br/> <span data-ttu-id="999c8-3577">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3577">0</span></span><br/>

<span data-ttu-id="999c8-3578">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3578">1</span></span>

<span data-ttu-id="999c8-3579">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3579">2</span></span>

<span data-ttu-id="999c8-3580">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3580">3</span></span>

<span data-ttu-id="999c8-3581">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3581">4</span></span>

<span data-ttu-id="999c8-3582">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3582">5</span></span>

<span data-ttu-id="999c8-3583">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3583">6</span></span>

<span data-ttu-id="999c8-3584">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3584">7</span></span>

<span data-ttu-id="999c8-3585">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3585">8</span></span>

<span data-ttu-id="999c8-3586">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3586">9</span></span>

<span data-ttu-id="999c8-3587">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3587">2</span></span><br/> <span data-ttu-id="999c8-3588">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3588">0</span></span><br/>

<span data-ttu-id="999c8-3589">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3589">1</span></span>

<span data-ttu-id="999c8-3590">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3590">2</span></span>

<span data-ttu-id="999c8-3591">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3591">3</span></span>

<span data-ttu-id="999c8-3592">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3592">4</span></span>

<span data-ttu-id="999c8-3593">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3593">5</span></span>

<span data-ttu-id="999c8-3594">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3594">6</span></span>

<span data-ttu-id="999c8-3595">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3595">7</span></span>

<span data-ttu-id="999c8-3596">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3596">8</span></span>

<span data-ttu-id="999c8-3597">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3597">9</span></span>

<span data-ttu-id="999c8-3598">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3598">3</span></span><br/> <span data-ttu-id="999c8-3599">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3599">0</span></span><br/>

<span data-ttu-id="999c8-3600">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3600">1</span></span>

<span data-ttu-id="999c8-3601">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="999c8-3601">\_hCursor</span></span>

<span data-ttu-id="999c8-3602">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="999c8-3602">\_cRowsToTransfer</span></span>

<span data-ttu-id="999c8-3603">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="999c8-3603">\_cbRowWidth</span></span>

<span data-ttu-id="999c8-3604">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="999c8-3604">\_cbSeek</span></span>

<span data-ttu-id="999c8-3605">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="999c8-3605">\_cbReserved</span></span>

<span data-ttu-id="999c8-3606">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="999c8-3606">\_cbReadBuffer</span></span>

<span data-ttu-id="999c8-3607">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="999c8-3607">\_ulClientBase</span></span>

<span data-ttu-id="999c8-3608">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="999c8-3608">\_fBwdFetch</span></span>

<span data-ttu-id="999c8-3609">eType</span><span class="sxs-lookup"><span data-stu-id="999c8-3609">eType</span></span>

<span data-ttu-id="999c8-3610">\_chap</span><span class="sxs-lookup"><span data-stu-id="999c8-3610">\_chapt</span></span>

<span data-ttu-id="999c8-3611">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="999c8-3611">SeekDescription</span></span>

<span data-ttu-id="999c8-3612">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3612">...</span></span>

<span data-ttu-id="999c8-3613">... variable</span><span class="sxs-lookup"><span data-stu-id="999c8-3613">... (variable)</span></span>



 

<span data-ttu-id="999c8-3614">**\_ hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut identifiant la requête dont les lignes doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="999c8-3614">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="999c8-3615">**\_ cRowsToTransfer**: entier non signé 32 bits indiquant le nombre maximal de lignes que le client souhaite recevoir en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="999c8-3615">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="999c8-3616">**\_ cbRowWidth**: entier non signé 32 bits indiquant la longueur d’une ligne, en octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-3616">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="999c8-3617">**\_ cbSeek**: entier non signé 32 bits indiquant la taille du message commençant par ETYPE.</span><span class="sxs-lookup"><span data-stu-id="999c8-3617">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="999c8-3618">**\_ cbReserved**: entier non signé 32 bits indiquant la taille, en octets, d’un message CPMGetRowsOut (sans les champs Rows et SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="999c8-3618">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="999c8-3619">Cette valeur dans ce champ est ajoutée à la valeur du \_ champ cbSeek, puis doit être utilisée pour calculer le décalage du champ Rows dans le message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-3619">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="999c8-3620">**\_ cbReadBuffer**: entier non signé 32 bits qui doit être défini sur la valeur maximale de la valeur de \_ cbRowWidth ou 1000 fois la valeur de \_ cRowsToTransfer, arrondie au multiple de 512 octets le plus proche.</span><span class="sxs-lookup"><span data-stu-id="999c8-3620">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="999c8-3621">La valeur ne doit pas dépasser 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="999c8-3621">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="999c8-3622">**\_ ulClientBase**: entier non signé 32 bits indiquant la valeur de base à utiliser pour les calculs de pointeur dans la mémoire tampon de ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-3622">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="999c8-3623">Si des décalages 64 bits sont utilisés, le champ Reserved2 de l’en-tête de message est utilisé comme les 32 bits supérieurs et \_ ulClientBase en tant que 32 bits inférieur d’une valeur de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-3623">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="999c8-3624">Pour plus d’informations, consultez la section 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="999c8-3624">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="999c8-3625">**\_ fBwdFetch**: entier non signé 32 bits indiquant l’ordre dans lequel les lignes sont extraites.</span><span class="sxs-lookup"><span data-stu-id="999c8-3625">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="999c8-3626">Si la valeur est définie sur 0x00000001, les lignes doivent être extraites dans l’ordre inverse.</span><span class="sxs-lookup"><span data-stu-id="999c8-3626">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="999c8-3627">Si la valeur est 0x00000000, les lignes doivent être extraites dans l’ordre de transmission.</span><span class="sxs-lookup"><span data-stu-id="999c8-3627">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="999c8-3628">NE doit avoir aucune autre valeur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3628">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="999c8-3629">**ETYPE**: entier non signé 32 bits contenant l’une des valeurs suivantes pour indiquer le type d’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="999c8-3629">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="999c8-3630">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-3630">Value</span></span>                         | <span data-ttu-id="999c8-3631">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-3631">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="999c8-3632">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-3632">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="999c8-3633">SeekDescription contient une structure CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="999c8-3633">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="999c8-3634">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-3634">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="999c8-3635">SeekDescription contient une structure CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="999c8-3635">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="999c8-3636">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-3636">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="999c8-3637">SeekDescription contient une structure CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="999c8-3637">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="999c8-3638">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-3638">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="999c8-3639">SeekDescription contient une structure CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="999c8-3639">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="999c8-3640">**\_ Chapt**: valeur 32 bits représentant le descripteur du chapitre de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3640">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="999c8-3641">**SeekDescription**: ce champ doit contenir une structure du type indiqué par la valeur ETYPE.</span><span class="sxs-lookup"><span data-stu-id="999c8-3641">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="999c8-3642">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3642">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="999c8-3643">Le message CPMGetRowsOut répond à un message CPMGetRowsIn avec les lignes d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3643">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="999c8-3644">Les serveurs doivent mettre en forme des décalages avec les types de données de longueur variable dans le champ Rows comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-3644">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="999c8-3645">Le client a indiqué qu’il s’agissait d’un système 32 bits (0x00000008 ou moins dans le champ iClientVersion de CPMConnectIn) : les décalages sont des entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-3645">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="999c8-3646">Le client a indiqué qu’il s’agissait d’un système 64 bits ( \_ iClientVersion > 0x00000008 dans CPMConnectIn) et que le serveur indiquait qu’il s’agissait d’un système 32 bits ( \_ ServerVersion défini sur 0X00000007 dans CPMConnectOut) : les décalages sont des entiers de 32 bits</span><span class="sxs-lookup"><span data-stu-id="999c8-3646">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="999c8-3647">Le client a indiqué qu’il s’agissait d’un système 64 bits ( \_ iClientVersion > 0x00000008 dans CPMConnectIn) et que le serveur indiquait qu’il s’agissait d’un système 64 bits ( \_ ServerVersion défini sur 0X00010007 dans CPMConnectOut) : les décalages sont des entiers de 64 bits</span><span class="sxs-lookup"><span data-stu-id="999c8-3647">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="999c8-3648">Le format du message CPMGetRowsOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3648">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3649">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3649">0</span></span>

<span data-ttu-id="999c8-3650">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3650">1</span></span>

<span data-ttu-id="999c8-3651">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3651">2</span></span>

<span data-ttu-id="999c8-3652">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3652">3</span></span>

<span data-ttu-id="999c8-3653">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3653">4</span></span>

<span data-ttu-id="999c8-3654">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3654">5</span></span>

<span data-ttu-id="999c8-3655">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3655">6</span></span>

<span data-ttu-id="999c8-3656">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3656">7</span></span>

<span data-ttu-id="999c8-3657">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3657">8</span></span>

<span data-ttu-id="999c8-3658">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3658">9</span></span>

<span data-ttu-id="999c8-3659">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3659">1</span></span><br/> <span data-ttu-id="999c8-3660">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3660">0</span></span><br/>

<span data-ttu-id="999c8-3661">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3661">1</span></span>

<span data-ttu-id="999c8-3662">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3662">2</span></span>

<span data-ttu-id="999c8-3663">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3663">3</span></span>

<span data-ttu-id="999c8-3664">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3664">4</span></span>

<span data-ttu-id="999c8-3665">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3665">5</span></span>

<span data-ttu-id="999c8-3666">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3666">6</span></span>

<span data-ttu-id="999c8-3667">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3667">7</span></span>

<span data-ttu-id="999c8-3668">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3668">8</span></span>

<span data-ttu-id="999c8-3669">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3669">9</span></span>

<span data-ttu-id="999c8-3670">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3670">2</span></span><br/> <span data-ttu-id="999c8-3671">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3671">0</span></span><br/>

<span data-ttu-id="999c8-3672">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3672">1</span></span>

<span data-ttu-id="999c8-3673">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3673">2</span></span>

<span data-ttu-id="999c8-3674">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3674">3</span></span>

<span data-ttu-id="999c8-3675">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3675">4</span></span>

<span data-ttu-id="999c8-3676">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3676">5</span></span>

<span data-ttu-id="999c8-3677">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3677">6</span></span>

<span data-ttu-id="999c8-3678">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3678">7</span></span>

<span data-ttu-id="999c8-3679">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3679">8</span></span>

<span data-ttu-id="999c8-3680">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3680">9</span></span>

<span data-ttu-id="999c8-3681">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3681">3</span></span><br/> <span data-ttu-id="999c8-3682">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3682">0</span></span><br/>

<span data-ttu-id="999c8-3683">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3683">1</span></span>

<span data-ttu-id="999c8-3684">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="999c8-3684">\_cRowsReturned</span></span>

<span data-ttu-id="999c8-3685">eType</span><span class="sxs-lookup"><span data-stu-id="999c8-3685">eType</span></span>

<span data-ttu-id="999c8-3686">\_chap</span><span class="sxs-lookup"><span data-stu-id="999c8-3686">\_chapt</span></span>

<span data-ttu-id="999c8-3687">SeekDescription (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3687">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="999c8-3688">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3688">...</span></span>

<span data-ttu-id="999c8-3689">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3689">...</span></span>

<span data-ttu-id="999c8-3690">paddingRows (facultatif, variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3690">paddingRows (optional, variable)</span></span>

<span data-ttu-id="999c8-3691">Lignes</span><span class="sxs-lookup"><span data-stu-id="999c8-3691">Rows</span></span>



 

<span data-ttu-id="999c8-3692">**\_ cRowsReturned**: entier non signé 32 bits indiquant le nombre de lignes retournées dans les lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3692">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="999c8-3693">**ETYPE**: entier non signé 32 bits contenant l’une des valeurs suivantes pour indiquer le type d’opération rowseek à effectuer</span><span class="sxs-lookup"><span data-stu-id="999c8-3693">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="999c8-3694">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-3694">Value</span></span>                         | <span data-ttu-id="999c8-3695">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-3695">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="999c8-3696">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-3696">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="999c8-3697">Aucun SeekDescription, ignorer le champ SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="999c8-3697">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="999c8-3698">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-3698">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="999c8-3699">SeekDescription contient une structure CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="999c8-3699">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="999c8-3700">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-3700">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="999c8-3701">SeekDescription contient une structure CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="999c8-3701">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="999c8-3702">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-3702">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="999c8-3703">SeekDescription contient une structure CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="999c8-3703">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="999c8-3704">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-3704">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="999c8-3705">SeekDescription contient une structure CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="999c8-3705">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="999c8-3706">**\_ Chapt**: valeur 32 bits représentant le descripteur du chapitre de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3706">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="999c8-3707">**SeekDescription**: ce champ doit contenir une structure du type indiqué par le champ ETYPE.</span><span class="sxs-lookup"><span data-stu-id="999c8-3707">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="999c8-3708">**paddingRows**: ce champ doit avoir une longueur suffisante (de 0 à \_ cbReserved octets) pour remplir le champ de lignes à \_ cbReserved offset à partir du début d’un message, où \_ cbReserved est la valeur dans le message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-3708">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="999c8-3709">Les octets de remplissage utilisés dans ce champ peuvent être n’importe quelle valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-3709">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="999c8-3710">Ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3710">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="999c8-3711">**Lignes**: données de ligne, est mise en forme comme stipulé par les informations de colonne dans le message CPMSetBindingsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3711">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="999c8-3712">Les lignes doivent être stockées dans l’ordre de transfert (par exemple, ligne 1 avant la ligne 2).</span><span class="sxs-lookup"><span data-stu-id="999c8-3712">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="999c8-3713">Les colonnes de taille fixe doivent être stockées aux décalages spécifiés par le message CPMSetBindingsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3713">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="999c8-3714">Les colonnes de taille variable (par exemple, les chaînes) doivent être stockées comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-3714">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="999c8-3715">Les données de la variable proprement dite (par exemple, la chaîne) sont stockées vers la fin de la mémoire tampon dans l’ordre décroissant (par exemple, la collection de toutes les données de variable pour la ligne 1 est à la fin, ligne 2 la plus proche, etc.).</span><span class="sxs-lookup"><span data-stu-id="999c8-3715">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="999c8-3716">La zone de taille fixe (au début de la mémoire tampon de ligne) doit contenir un CRowVariant pour chaque colonne, stockée au décalage spécifié dans le message CPMSetBindingsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3716">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="999c8-3717">vType doit contenir le type de données (par ex \_ ., VT LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="999c8-3717">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="999c8-3718">Si, comme déterminé par les règles au début de la section de cette section, les décalages 32 bits sont utilisés, alors le champ offset dans CRowVariant doit contenir une valeur 32 bits qui correspond au décalage des données variables à partir du début du message CPMGetRowsOut, plus la valeur de \_ ulClientBase spécifiée dans le message CPMGetRowsIn le plus récent.</span><span class="sxs-lookup"><span data-stu-id="999c8-3718">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="999c8-3719">Si des décalages 64 bits sont utilisés, le champ de décalage dans CRowVariant doit contenir une valeur 64 bits qui correspond au décalage du début du message CPMGetRowsOut, ajouté à une valeur de 64 bits composée à l’aide de \_ ulClientBase comme 32 bits et ulReserved2 de poids \_ fort (32 bits).</span><span class="sxs-lookup"><span data-stu-id="999c8-3719">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="999c8-3720">Par exemple, si le message CPMSetBindingsIn spécifiant deux colonnes-Size (VT \_ I4) et title (VT \_ LPWStr)-et \_ ulClientBase de CPMGetRowsIn a été 0x10000, deux lignes s’affichent comme suit.</span><span class="sxs-lookup"><span data-stu-id="999c8-3720">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="999c8-3721">La section marquée en gris est la partie de longueur fixe de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="999c8-3721">The section marked in grey is the fixed-length part of the buffer.</span></span>

![exemple de message cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="999c8-3723">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3723">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="999c8-3724">Le message CPMRatioFinishedIn demande le pourcentage d’achèvement d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3724">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="999c8-3725">Le format du message CPMRatioFinishedIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3725">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3726">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3726">0</span></span>

<span data-ttu-id="999c8-3727">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3727">1</span></span>

<span data-ttu-id="999c8-3728">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3728">2</span></span>

<span data-ttu-id="999c8-3729">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3729">3</span></span>

<span data-ttu-id="999c8-3730">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3730">4</span></span>

<span data-ttu-id="999c8-3731">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3731">5</span></span>

<span data-ttu-id="999c8-3732">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3732">6</span></span>

<span data-ttu-id="999c8-3733">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3733">7</span></span>

<span data-ttu-id="999c8-3734">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3734">8</span></span>

<span data-ttu-id="999c8-3735">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3735">9</span></span>

<span data-ttu-id="999c8-3736">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3736">1</span></span><br/> <span data-ttu-id="999c8-3737">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3737">0</span></span><br/>

<span data-ttu-id="999c8-3738">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3738">1</span></span>

<span data-ttu-id="999c8-3739">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3739">2</span></span>

<span data-ttu-id="999c8-3740">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3740">3</span></span>

<span data-ttu-id="999c8-3741">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3741">4</span></span>

<span data-ttu-id="999c8-3742">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3742">5</span></span>

<span data-ttu-id="999c8-3743">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3743">6</span></span>

<span data-ttu-id="999c8-3744">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3744">7</span></span>

<span data-ttu-id="999c8-3745">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3745">8</span></span>

<span data-ttu-id="999c8-3746">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3746">9</span></span>

<span data-ttu-id="999c8-3747">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3747">2</span></span><br/> <span data-ttu-id="999c8-3748">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3748">0</span></span><br/>

<span data-ttu-id="999c8-3749">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3749">1</span></span>

<span data-ttu-id="999c8-3750">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3750">2</span></span>

<span data-ttu-id="999c8-3751">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3751">3</span></span>

<span data-ttu-id="999c8-3752">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3752">4</span></span>

<span data-ttu-id="999c8-3753">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3753">5</span></span>

<span data-ttu-id="999c8-3754">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3754">6</span></span>

<span data-ttu-id="999c8-3755">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3755">7</span></span>

<span data-ttu-id="999c8-3756">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3756">8</span></span>

<span data-ttu-id="999c8-3757">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3757">9</span></span>

<span data-ttu-id="999c8-3758">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3758">3</span></span><br/> <span data-ttu-id="999c8-3759">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3759">0</span></span><br/>

<span data-ttu-id="999c8-3760">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3760">1</span></span>

<span data-ttu-id="999c8-3761">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="999c8-3761">\_hCursor</span></span>

<span data-ttu-id="999c8-3762">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="999c8-3762">\_fQuick</span></span>



 

<span data-ttu-id="999c8-3763">**\_ hCursor**: descripteur du message CPMCreateQueryOut identifiant la requête pour laquelle des informations de saisie semi-automatique doivent être demandées.</span><span class="sxs-lookup"><span data-stu-id="999c8-3763">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="999c8-3764">**\_ fQuick**: doit être défini sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-3764">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="999c8-3765">Inutilisé et doit être ignoré par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3765">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="999c8-3766">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3766">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="999c8-3767">Le message CPMRatioFinishedOut répond à un message CPMRatioFinishedIn avec le ratio d’achèvement d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3767">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="999c8-3768">Le format du message CPMRatioFinishedOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3768">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3769">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3769">0</span></span>

<span data-ttu-id="999c8-3770">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3770">1</span></span>

<span data-ttu-id="999c8-3771">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3771">2</span></span>

<span data-ttu-id="999c8-3772">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3772">3</span></span>

<span data-ttu-id="999c8-3773">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3773">4</span></span>

<span data-ttu-id="999c8-3774">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3774">5</span></span>

<span data-ttu-id="999c8-3775">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3775">6</span></span>

<span data-ttu-id="999c8-3776">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3776">7</span></span>

<span data-ttu-id="999c8-3777">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3777">8</span></span>

<span data-ttu-id="999c8-3778">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3778">9</span></span>

<span data-ttu-id="999c8-3779">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3779">1</span></span><br/> <span data-ttu-id="999c8-3780">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3780">0</span></span><br/>

<span data-ttu-id="999c8-3781">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3781">1</span></span>

<span data-ttu-id="999c8-3782">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3782">2</span></span>

<span data-ttu-id="999c8-3783">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3783">3</span></span>

<span data-ttu-id="999c8-3784">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3784">4</span></span>

<span data-ttu-id="999c8-3785">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3785">5</span></span>

<span data-ttu-id="999c8-3786">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3786">6</span></span>

<span data-ttu-id="999c8-3787">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3787">7</span></span>

<span data-ttu-id="999c8-3788">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3788">8</span></span>

<span data-ttu-id="999c8-3789">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3789">9</span></span>

<span data-ttu-id="999c8-3790">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3790">2</span></span><br/> <span data-ttu-id="999c8-3791">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3791">0</span></span><br/>

<span data-ttu-id="999c8-3792">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3792">1</span></span>

<span data-ttu-id="999c8-3793">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3793">2</span></span>

<span data-ttu-id="999c8-3794">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3794">3</span></span>

<span data-ttu-id="999c8-3795">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3795">4</span></span>

<span data-ttu-id="999c8-3796">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3796">5</span></span>

<span data-ttu-id="999c8-3797">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3797">6</span></span>

<span data-ttu-id="999c8-3798">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3798">7</span></span>

<span data-ttu-id="999c8-3799">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3799">8</span></span>

<span data-ttu-id="999c8-3800">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3800">9</span></span>

<span data-ttu-id="999c8-3801">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3801">3</span></span><br/> <span data-ttu-id="999c8-3802">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3802">0</span></span><br/>

<span data-ttu-id="999c8-3803">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3803">1</span></span>

<span data-ttu-id="999c8-3804">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="999c8-3804">\_ ulNumerator</span></span>

<span data-ttu-id="999c8-3805">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="999c8-3805">\_ulDenominator</span></span>

<span data-ttu-id="999c8-3806">\_cRows</span><span class="sxs-lookup"><span data-stu-id="999c8-3806">\_cRows</span></span>

<span data-ttu-id="999c8-3807">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="999c8-3807">\_fNewRows</span></span>



 

<span data-ttu-id="999c8-3808">**\_ ulNumerator**: entier non signé 32 bits indiquant le numérateur du rapport d’achèvement en termes de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3808">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="999c8-3809">**\_ ulDenominator**: entier non signé 32 bits indiquant le dénominateur du rapport d’achèvement en termes de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3809">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="999c8-3810">DOIT être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="999c8-3810">MUST be greater than zero.</span></span>

<span data-ttu-id="999c8-3811">**\_ Crows**: entier non signé 32 bits indiquant le nombre total de lignes de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3811">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="999c8-3812">**\_ fNewRows**: valeur booléenne indiquant si de nouvelles lignes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="999c8-3812">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="999c8-3813">La valeur 0x00000001 indique que les nouvelles lignes sont disponibles dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3813">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="999c8-3814">La valeur 0x00000000 indique que l’ensemble de lignes ne contient pas de nouvelles lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3814">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="999c8-3815">Ce champ ne doit avoir aucune autre valeur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3815">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="999c8-3816">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3816">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="999c8-3817">Le message CPMFetchValueIn demande une valeur de propriété qui était trop grande pour être renvoyée dans un ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3817">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="999c8-3818">Comme indiqué dans la section 3.2.4.2.5, ce message est envoyé à plusieurs reprises pour récupérer tous les octets de la propriété, en mettant à jour \_ cbSoFar pour chacun, jusqu’à ce que le \_ champ fMoreExists du message CPMFetchValueOut soit défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="999c8-3818">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="999c8-3819">Le format du message CPMFetchValueIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3819">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3820">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3820">0</span></span>

<span data-ttu-id="999c8-3821">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3821">1</span></span>

<span data-ttu-id="999c8-3822">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3822">2</span></span>

<span data-ttu-id="999c8-3823">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3823">3</span></span>

<span data-ttu-id="999c8-3824">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3824">4</span></span>

<span data-ttu-id="999c8-3825">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3825">5</span></span>

<span data-ttu-id="999c8-3826">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3826">6</span></span>

<span data-ttu-id="999c8-3827">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3827">7</span></span>

<span data-ttu-id="999c8-3828">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3828">8</span></span>

<span data-ttu-id="999c8-3829">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3829">9</span></span>

<span data-ttu-id="999c8-3830">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3830">1</span></span><br/> <span data-ttu-id="999c8-3831">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3831">0</span></span><br/>

<span data-ttu-id="999c8-3832">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3832">1</span></span>

<span data-ttu-id="999c8-3833">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3833">2</span></span>

<span data-ttu-id="999c8-3834">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3834">3</span></span>

<span data-ttu-id="999c8-3835">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3835">4</span></span>

<span data-ttu-id="999c8-3836">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3836">5</span></span>

<span data-ttu-id="999c8-3837">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3837">6</span></span>

<span data-ttu-id="999c8-3838">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3838">7</span></span>

<span data-ttu-id="999c8-3839">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3839">8</span></span>

<span data-ttu-id="999c8-3840">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3840">9</span></span>

<span data-ttu-id="999c8-3841">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3841">2</span></span><br/> <span data-ttu-id="999c8-3842">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3842">0</span></span><br/>

<span data-ttu-id="999c8-3843">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3843">1</span></span>

<span data-ttu-id="999c8-3844">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3844">2</span></span>

<span data-ttu-id="999c8-3845">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3845">3</span></span>

<span data-ttu-id="999c8-3846">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3846">4</span></span>

<span data-ttu-id="999c8-3847">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3847">5</span></span>

<span data-ttu-id="999c8-3848">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3848">6</span></span>

<span data-ttu-id="999c8-3849">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3849">7</span></span>

<span data-ttu-id="999c8-3850">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3850">8</span></span>

<span data-ttu-id="999c8-3851">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3851">9</span></span>

<span data-ttu-id="999c8-3852">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3852">3</span></span><br/> <span data-ttu-id="999c8-3853">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3853">0</span></span><br/>

<span data-ttu-id="999c8-3854">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3854">1</span></span>

<span data-ttu-id="999c8-3855">\_wid</span><span class="sxs-lookup"><span data-stu-id="999c8-3855">\_wid</span></span>

<span data-ttu-id="999c8-3856">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="999c8-3856">\_cbSoFar</span></span>

<span data-ttu-id="999c8-3857">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="999c8-3857">\_cbPropSpec</span></span>

<span data-ttu-id="999c8-3858">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="999c8-3858">\_cbChunk</span></span>

<span data-ttu-id="999c8-3859">PropSpec (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3859">PropSpec (variable)</span></span>

<span data-ttu-id="999c8-3860">...</span><span class="sxs-lookup"><span data-stu-id="999c8-3860">...</span></span>

<span data-ttu-id="999c8-3861">\_Padding (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3861">\_padding (variable)</span></span>



 

<span data-ttu-id="999c8-3862">**\_ wid**: entier non signé 32 bits contenant des informations sur l’ID de document identifiant le document pour lequel une propriété doit être extraite.</span><span class="sxs-lookup"><span data-stu-id="999c8-3862">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="999c8-3863">**\_ cbSoFar**: entier non signé 32 bits contenant le nombre d’octets transférés précédemment pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-3863">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="999c8-3864">DOIT être défini sur 0x00000000 dans le premier message.</span><span class="sxs-lookup"><span data-stu-id="999c8-3864">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="999c8-3865">**\_ cbPropSpec**: entier non signé 32 bits contenant la taille du champ PropSpec, en octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-3865">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="999c8-3866">**\_ cbChunk**: entier non signé 32 bits contenant le nombre maximal d’octets que l’expéditeur peut accepter dans un message CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-3866">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="999c8-3867">*Comportement de Windows : ce champ est défini sur 0x00004000 pour toutes les versions de Windows.*</span><span class="sxs-lookup"><span data-stu-id="999c8-3867">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="999c8-3868">**PropSpec**: structure CFullPropSpec spécifiant la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="999c8-3868">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="999c8-3869">**\_ remplissage**: ce champ doit avoir la longueur nécessaire (de 0 à 3 octets) pour remplir le message sur un multiple de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-3869">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="999c8-3870">La valeur des octets de remplissage peut être n’importe quelle valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-3870">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="999c8-3871">Ce champ doit être ignoré par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-3871">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="999c8-3872">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3872">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="999c8-3873">Le message CPMFetchValueOut répond à un message CPMFetchValueIn avec une valeur de propriété d’une requête précédente.</span><span class="sxs-lookup"><span data-stu-id="999c8-3873">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="999c8-3874">Comme indiqué dans la section 3.1.5.2.8, ce message est envoyé après chaque message CPMFetchValueIn jusqu’à ce que tous les octets de la propriété soient transférés.</span><span class="sxs-lookup"><span data-stu-id="999c8-3874">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="999c8-3875">Le format du message CPMFetchValueOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3875">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3876">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3876">0</span></span>

<span data-ttu-id="999c8-3877">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3877">1</span></span>

<span data-ttu-id="999c8-3878">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3878">2</span></span>

<span data-ttu-id="999c8-3879">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3879">3</span></span>

<span data-ttu-id="999c8-3880">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3880">4</span></span>

<span data-ttu-id="999c8-3881">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3881">5</span></span>

<span data-ttu-id="999c8-3882">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3882">6</span></span>

<span data-ttu-id="999c8-3883">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3883">7</span></span>

<span data-ttu-id="999c8-3884">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3884">8</span></span>

<span data-ttu-id="999c8-3885">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3885">9</span></span>

<span data-ttu-id="999c8-3886">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3886">1</span></span><br/> <span data-ttu-id="999c8-3887">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3887">0</span></span><br/>

<span data-ttu-id="999c8-3888">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3888">1</span></span>

<span data-ttu-id="999c8-3889">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3889">2</span></span>

<span data-ttu-id="999c8-3890">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3890">3</span></span>

<span data-ttu-id="999c8-3891">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3891">4</span></span>

<span data-ttu-id="999c8-3892">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3892">5</span></span>

<span data-ttu-id="999c8-3893">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3893">6</span></span>

<span data-ttu-id="999c8-3894">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3894">7</span></span>

<span data-ttu-id="999c8-3895">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3895">8</span></span>

<span data-ttu-id="999c8-3896">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3896">9</span></span>

<span data-ttu-id="999c8-3897">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3897">2</span></span><br/> <span data-ttu-id="999c8-3898">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3898">0</span></span><br/>

<span data-ttu-id="999c8-3899">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3899">1</span></span>

<span data-ttu-id="999c8-3900">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3900">2</span></span>

<span data-ttu-id="999c8-3901">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3901">3</span></span>

<span data-ttu-id="999c8-3902">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3902">4</span></span>

<span data-ttu-id="999c8-3903">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3903">5</span></span>

<span data-ttu-id="999c8-3904">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3904">6</span></span>

<span data-ttu-id="999c8-3905">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3905">7</span></span>

<span data-ttu-id="999c8-3906">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3906">8</span></span>

<span data-ttu-id="999c8-3907">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3907">9</span></span>

<span data-ttu-id="999c8-3908">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3908">3</span></span><br/> <span data-ttu-id="999c8-3909">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3909">0</span></span><br/>

<span data-ttu-id="999c8-3910">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3910">1</span></span>

<span data-ttu-id="999c8-3911">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="999c8-3911">\_cbValue</span></span>

<span data-ttu-id="999c8-3912">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="999c8-3912">\_fMoreExists</span></span>

<span data-ttu-id="999c8-3913">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="999c8-3913">\_fValueExists</span></span>

<span data-ttu-id="999c8-3914">vType</span><span class="sxs-lookup"><span data-stu-id="999c8-3914">vType</span></span>

<span data-ttu-id="999c8-3915">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="999c8-3915">vValue (variable)</span></span>



 

<span data-ttu-id="999c8-3916">**\_ cbValue**: entier non signé 32 bits contenant la taille totale, en octets, dans vValue.</span><span class="sxs-lookup"><span data-stu-id="999c8-3916">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="999c8-3917">**\_ fMoreExists**: valeur booléenne indiquant si des messages CPMFetchValueOut supplémentaires sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="999c8-3917">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="999c8-3918">S’il est défini sur 0x00000001, il y a des messages CPMFetchValueOut supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="999c8-3918">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="999c8-3919">Si la valeur est 0x00000000, aucun message CPMFetchValueOut supplémentaire n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="999c8-3919">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="999c8-3920">**\_ fValueExists**: valeur booléenne indiquant s’il existe une valeur pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-3920">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="999c8-3921">Si la valeur est définie sur 0x00000001, il existe une valeur pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-3921">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="999c8-3922">Si la valeur est 0x00000000, la valeur de la propriété n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="999c8-3922">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="999c8-3923">**vType**: une valeur de l’énumération VarEnum, consultez la section 2.2.1.1 pour plus d’informations, décrivant le type de la propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="999c8-3924">**vValue**: partie d’un tableau d’octets contenant une structure SERIALIZEDPROPERTYVALUE telle que spécifiée dans la section 2.2.1.32, où l’offset du début de la partie est la valeur de \_ cbSoFar dans CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-3924">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="999c8-3925">La longueur de la partie, indiquée par le \_ champ cbValue, doit être égale à la valeur de \_ CbChunk dans CPMFetchValueIn si \_ fMoreExists est défini sur 0x00000001 et doit être inférieur ou égal à la valeur de cbChunk dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="999c8-3925">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="999c8-3926">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="999c8-3926">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="999c8-3927">Le message CPMGetNotify demande que le client souhaite être averti des modifications de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-3927">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="999c8-3928">Le message ne doit pas inclure un corps ; seul l’en-tête de message, tel que spécifié dans la section 2.2.2, doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="999c8-3928">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="999c8-3929">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="999c8-3929">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="999c8-3930">Le message CPMSendNotifyOut avertit le client qu’une modification a été apportée aux résultats d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3930">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="999c8-3931">Ce message est envoyé uniquement lorsqu’une modification se produit.</span><span class="sxs-lookup"><span data-stu-id="999c8-3931">This message is only sent when a change occurs.</span></span> <span data-ttu-id="999c8-3932">Le format du message CPMSendNotifyOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3932">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-3933">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3933">0</span></span>

<span data-ttu-id="999c8-3934">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3934">1</span></span>

<span data-ttu-id="999c8-3935">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3935">2</span></span>

<span data-ttu-id="999c8-3936">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3936">3</span></span>

<span data-ttu-id="999c8-3937">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3937">4</span></span>

<span data-ttu-id="999c8-3938">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3938">5</span></span>

<span data-ttu-id="999c8-3939">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3939">6</span></span>

<span data-ttu-id="999c8-3940">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3940">7</span></span>

<span data-ttu-id="999c8-3941">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3941">8</span></span>

<span data-ttu-id="999c8-3942">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3942">9</span></span>

<span data-ttu-id="999c8-3943">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3943">1</span></span><br/> <span data-ttu-id="999c8-3944">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3944">0</span></span><br/>

<span data-ttu-id="999c8-3945">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3945">1</span></span>

<span data-ttu-id="999c8-3946">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3946">2</span></span>

<span data-ttu-id="999c8-3947">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3947">3</span></span>

<span data-ttu-id="999c8-3948">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3948">4</span></span>

<span data-ttu-id="999c8-3949">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3949">5</span></span>

<span data-ttu-id="999c8-3950">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3950">6</span></span>

<span data-ttu-id="999c8-3951">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3951">7</span></span>

<span data-ttu-id="999c8-3952">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3952">8</span></span>

<span data-ttu-id="999c8-3953">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3953">9</span></span>

<span data-ttu-id="999c8-3954">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3954">2</span></span><br/> <span data-ttu-id="999c8-3955">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3955">0</span></span><br/>

<span data-ttu-id="999c8-3956">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3956">1</span></span>

<span data-ttu-id="999c8-3957">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3957">2</span></span>

<span data-ttu-id="999c8-3958">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3958">3</span></span>

<span data-ttu-id="999c8-3959">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3959">4</span></span>

<span data-ttu-id="999c8-3960">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3960">5</span></span>

<span data-ttu-id="999c8-3961">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3961">6</span></span>

<span data-ttu-id="999c8-3962">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3962">7</span></span>

<span data-ttu-id="999c8-3963">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3963">8</span></span>

<span data-ttu-id="999c8-3964">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3964">9</span></span>

<span data-ttu-id="999c8-3965">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3965">3</span></span><br/> <span data-ttu-id="999c8-3966">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3966">0</span></span><br/>

<span data-ttu-id="999c8-3967">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3967">1</span></span>

<span data-ttu-id="999c8-3968">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="999c8-3968">\_watchNotify</span></span>



 

<span data-ttu-id="999c8-3969">**\_ watchNotify**: modification de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-3969">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="999c8-3970">Il doit s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-3970">It MUST be one of the following values:</span></span>



| <span data-ttu-id="999c8-3971">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-3971">Value</span></span>                                     | <span data-ttu-id="999c8-3972">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-3972">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="999c8-3973">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-3973">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="999c8-3974">Le nombre de lignes dans l’ensemble de lignes de requête a changé.</span><span class="sxs-lookup"><span data-stu-id="999c8-3974">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="999c8-3975">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-3975">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="999c8-3976">La requête est terminée.</span><span class="sxs-lookup"><span data-stu-id="999c8-3976">The query has completed.</span></span>                            |
| <span data-ttu-id="999c8-3977">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-3977">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="999c8-3978">La requête a été réexécutée.</span><span class="sxs-lookup"><span data-stu-id="999c8-3978">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="999c8-3979">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="999c8-3979">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="999c8-3980">Le message CPMGetApproximatePositionIn demande la position approximative d’un signet dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-3980">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="999c8-3981">Le format du message CPMGetApproximatePositionIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-3981">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-3982">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3982">0</span></span>

<span data-ttu-id="999c8-3983">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3983">1</span></span>

<span data-ttu-id="999c8-3984">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3984">2</span></span>

<span data-ttu-id="999c8-3985">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3985">3</span></span>

<span data-ttu-id="999c8-3986">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3986">4</span></span>

<span data-ttu-id="999c8-3987">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3987">5</span></span>

<span data-ttu-id="999c8-3988">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3988">6</span></span>

<span data-ttu-id="999c8-3989">7</span><span class="sxs-lookup"><span data-stu-id="999c8-3989">7</span></span>

<span data-ttu-id="999c8-3990">8</span><span class="sxs-lookup"><span data-stu-id="999c8-3990">8</span></span>

<span data-ttu-id="999c8-3991">9</span><span class="sxs-lookup"><span data-stu-id="999c8-3991">9</span></span>

<span data-ttu-id="999c8-3992">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3992">1</span></span><br/> <span data-ttu-id="999c8-3993">0</span><span class="sxs-lookup"><span data-stu-id="999c8-3993">0</span></span><br/>

<span data-ttu-id="999c8-3994">1</span><span class="sxs-lookup"><span data-stu-id="999c8-3994">1</span></span>

<span data-ttu-id="999c8-3995">2</span><span class="sxs-lookup"><span data-stu-id="999c8-3995">2</span></span>

<span data-ttu-id="999c8-3996">3</span><span class="sxs-lookup"><span data-stu-id="999c8-3996">3</span></span>

<span data-ttu-id="999c8-3997">4</span><span class="sxs-lookup"><span data-stu-id="999c8-3997">4</span></span>

<span data-ttu-id="999c8-3998">5</span><span class="sxs-lookup"><span data-stu-id="999c8-3998">5</span></span>

<span data-ttu-id="999c8-3999">6</span><span class="sxs-lookup"><span data-stu-id="999c8-3999">6</span></span>

<span data-ttu-id="999c8-4000">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4000">7</span></span>

<span data-ttu-id="999c8-4001">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4001">8</span></span>

<span data-ttu-id="999c8-4002">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4002">9</span></span>

<span data-ttu-id="999c8-4003">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4003">2</span></span><br/> <span data-ttu-id="999c8-4004">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4004">0</span></span><br/>

<span data-ttu-id="999c8-4005">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4005">1</span></span>

<span data-ttu-id="999c8-4006">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4006">2</span></span>

<span data-ttu-id="999c8-4007">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4007">3</span></span>

<span data-ttu-id="999c8-4008">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4008">4</span></span>

<span data-ttu-id="999c8-4009">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4009">5</span></span>

<span data-ttu-id="999c8-4010">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4010">6</span></span>

<span data-ttu-id="999c8-4011">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4011">7</span></span>

<span data-ttu-id="999c8-4012">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4012">8</span></span>

<span data-ttu-id="999c8-4013">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4013">9</span></span>

<span data-ttu-id="999c8-4014">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4014">3</span></span><br/> <span data-ttu-id="999c8-4015">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4015">0</span></span><br/>

<span data-ttu-id="999c8-4016">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4016">1</span></span>

<span data-ttu-id="999c8-4017">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="999c8-4017">\_hCursor</span></span>

<span data-ttu-id="999c8-4018">\_chap</span><span class="sxs-lookup"><span data-stu-id="999c8-4018">\_chapt</span></span>

<span data-ttu-id="999c8-4019">\_bmk</span><span class="sxs-lookup"><span data-stu-id="999c8-4019">\_bmk</span></span>



 

<span data-ttu-id="999c8-4020">**\_ hCursor**: valeur 32 bits représentant le curseur de requête obtenu à partir de CPMCreateQueryOut pour l’ensemble de lignes contenant le signet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4020">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="999c8-4021">**\_ Chapt**: valeur 32 bits représentant le handle du chapitre contenant le signet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4021">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="999c8-4022">**\_ BMK**: valeur 32 bits représentant le handle du signet pour lequel récupérer la position approximative.</span><span class="sxs-lookup"><span data-stu-id="999c8-4022">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="999c8-4023">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4023">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="999c8-4024">Le message CPMGetApproximatePositionOut répond à un message CPMGetApproximatePositionIn décrivant la position approximative du signet dans le chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4024">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="999c8-4025">Le format du message CPMGetApproximatePositionOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4025">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-4026">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4026">0</span></span>

<span data-ttu-id="999c8-4027">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4027">1</span></span>

<span data-ttu-id="999c8-4028">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4028">2</span></span>

<span data-ttu-id="999c8-4029">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4029">3</span></span>

<span data-ttu-id="999c8-4030">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4030">4</span></span>

<span data-ttu-id="999c8-4031">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4031">5</span></span>

<span data-ttu-id="999c8-4032">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4032">6</span></span>

<span data-ttu-id="999c8-4033">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4033">7</span></span>

<span data-ttu-id="999c8-4034">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4034">8</span></span>

<span data-ttu-id="999c8-4035">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4035">9</span></span>

<span data-ttu-id="999c8-4036">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4036">1</span></span><br/> <span data-ttu-id="999c8-4037">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4037">0</span></span><br/>

<span data-ttu-id="999c8-4038">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4038">1</span></span>

<span data-ttu-id="999c8-4039">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4039">2</span></span>

<span data-ttu-id="999c8-4040">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4040">3</span></span>

<span data-ttu-id="999c8-4041">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4041">4</span></span>

<span data-ttu-id="999c8-4042">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4042">5</span></span>

<span data-ttu-id="999c8-4043">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4043">6</span></span>

<span data-ttu-id="999c8-4044">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4044">7</span></span>

<span data-ttu-id="999c8-4045">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4045">8</span></span>

<span data-ttu-id="999c8-4046">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4046">9</span></span>

<span data-ttu-id="999c8-4047">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4047">2</span></span><br/> <span data-ttu-id="999c8-4048">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4048">0</span></span><br/>

<span data-ttu-id="999c8-4049">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4049">1</span></span>

<span data-ttu-id="999c8-4050">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4050">2</span></span>

<span data-ttu-id="999c8-4051">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4051">3</span></span>

<span data-ttu-id="999c8-4052">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4052">4</span></span>

<span data-ttu-id="999c8-4053">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4053">5</span></span>

<span data-ttu-id="999c8-4054">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4054">6</span></span>

<span data-ttu-id="999c8-4055">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4055">7</span></span>

<span data-ttu-id="999c8-4056">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4056">8</span></span>

<span data-ttu-id="999c8-4057">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4057">9</span></span>

<span data-ttu-id="999c8-4058">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4058">3</span></span><br/> <span data-ttu-id="999c8-4059">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4059">0</span></span><br/>

<span data-ttu-id="999c8-4060">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4060">1</span></span>

<span data-ttu-id="999c8-4061">\_numerator</span><span class="sxs-lookup"><span data-stu-id="999c8-4061">\_numerator</span></span>

<span data-ttu-id="999c8-4062">\_denominator</span><span class="sxs-lookup"><span data-stu-id="999c8-4062">\_denominator</span></span>



 

<span data-ttu-id="999c8-4063">**\_ numérateur**: entier non signé 32 bits contenant le numéro de ligne du signet dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4063">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="999c8-4064">En l’absence de lignes, ce champ doit avoir la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4064">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="999c8-4065">**\_ dénominateur**: entier non signé 32 bits contenant le nombre de lignes dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4065">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="999c8-4066">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4066">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="999c8-4067">Le message CPMCompareBmkIn demande une comparaison de deux signets dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4067">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="999c8-4068">Le format du message CPMCompareBmkIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4068">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-4069">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4069">0</span></span>

<span data-ttu-id="999c8-4070">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4070">1</span></span>

<span data-ttu-id="999c8-4071">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4071">2</span></span>

<span data-ttu-id="999c8-4072">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4072">3</span></span>

<span data-ttu-id="999c8-4073">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4073">4</span></span>

<span data-ttu-id="999c8-4074">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4074">5</span></span>

<span data-ttu-id="999c8-4075">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4075">6</span></span>

<span data-ttu-id="999c8-4076">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4076">7</span></span>

<span data-ttu-id="999c8-4077">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4077">8</span></span>

<span data-ttu-id="999c8-4078">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4078">9</span></span>

<span data-ttu-id="999c8-4079">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4079">1</span></span><br/> <span data-ttu-id="999c8-4080">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4080">0</span></span><br/>

<span data-ttu-id="999c8-4081">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4081">1</span></span>

<span data-ttu-id="999c8-4082">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4082">2</span></span>

<span data-ttu-id="999c8-4083">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4083">3</span></span>

<span data-ttu-id="999c8-4084">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4084">4</span></span>

<span data-ttu-id="999c8-4085">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4085">5</span></span>

<span data-ttu-id="999c8-4086">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4086">6</span></span>

<span data-ttu-id="999c8-4087">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4087">7</span></span>

<span data-ttu-id="999c8-4088">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4088">8</span></span>

<span data-ttu-id="999c8-4089">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4089">9</span></span>

<span data-ttu-id="999c8-4090">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4090">2</span></span><br/> <span data-ttu-id="999c8-4091">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4091">0</span></span><br/>

<span data-ttu-id="999c8-4092">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4092">1</span></span>

<span data-ttu-id="999c8-4093">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4093">2</span></span>

<span data-ttu-id="999c8-4094">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4094">3</span></span>

<span data-ttu-id="999c8-4095">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4095">4</span></span>

<span data-ttu-id="999c8-4096">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4096">5</span></span>

<span data-ttu-id="999c8-4097">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4097">6</span></span>

<span data-ttu-id="999c8-4098">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4098">7</span></span>

<span data-ttu-id="999c8-4099">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4099">8</span></span>

<span data-ttu-id="999c8-4100">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4100">9</span></span>

<span data-ttu-id="999c8-4101">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4101">3</span></span><br/> <span data-ttu-id="999c8-4102">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4102">0</span></span><br/>

<span data-ttu-id="999c8-4103">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4103">1</span></span>

<span data-ttu-id="999c8-4104">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="999c8-4104">\_hCursor</span></span>

<span data-ttu-id="999c8-4105">\_chap</span><span class="sxs-lookup"><span data-stu-id="999c8-4105">\_chapt</span></span>

<span data-ttu-id="999c8-4106">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="999c8-4106">\_bmkFirst</span></span>

<span data-ttu-id="999c8-4107">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="999c8-4107">\_bmkSecond</span></span>



 

<span data-ttu-id="999c8-4108">\_**hCursor**: valeur 32 bits représentant le descripteur du message CPMCreateQueryOut pour l’ensemble de lignes contenant les signets.</span><span class="sxs-lookup"><span data-stu-id="999c8-4108">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="999c8-4109">\_**Chapt**: valeur de 32 bits représentant le descripteur du chapitre contenant les signets à comparer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4109">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="999c8-4110">\_**bmkFirst**: valeur 32 bits représentant le handle du premier signet à comparer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4110">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="999c8-4111">\_**bmkSecond**: valeur 32 bits représentant le handle du deuxième signet à comparer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4111">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="999c8-4112">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4112">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="999c8-4113">Le message CPMCompareBmkOut répond à un message CPMCompareBmkIn avec la comparaison des deux signets du chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4113">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="999c8-4114">Le format du message CPMCompareBmkOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4114">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-4115">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4115">0</span></span>

<span data-ttu-id="999c8-4116">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4116">1</span></span>

<span data-ttu-id="999c8-4117">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4117">2</span></span>

<span data-ttu-id="999c8-4118">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4118">3</span></span>

<span data-ttu-id="999c8-4119">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4119">4</span></span>

<span data-ttu-id="999c8-4120">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4120">5</span></span>

<span data-ttu-id="999c8-4121">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4121">6</span></span>

<span data-ttu-id="999c8-4122">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4122">7</span></span>

<span data-ttu-id="999c8-4123">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4123">8</span></span>

<span data-ttu-id="999c8-4124">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4124">9</span></span>

<span data-ttu-id="999c8-4125">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4125">1</span></span><br/> <span data-ttu-id="999c8-4126">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4126">0</span></span><br/>

<span data-ttu-id="999c8-4127">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4127">1</span></span>

<span data-ttu-id="999c8-4128">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4128">2</span></span>

<span data-ttu-id="999c8-4129">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4129">3</span></span>

<span data-ttu-id="999c8-4130">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4130">4</span></span>

<span data-ttu-id="999c8-4131">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4131">5</span></span>

<span data-ttu-id="999c8-4132">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4132">6</span></span>

<span data-ttu-id="999c8-4133">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4133">7</span></span>

<span data-ttu-id="999c8-4134">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4134">8</span></span>

<span data-ttu-id="999c8-4135">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4135">9</span></span>

<span data-ttu-id="999c8-4136">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4136">2</span></span><br/> <span data-ttu-id="999c8-4137">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4137">0</span></span><br/>

<span data-ttu-id="999c8-4138">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4138">1</span></span>

<span data-ttu-id="999c8-4139">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4139">2</span></span>

<span data-ttu-id="999c8-4140">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4140">3</span></span>

<span data-ttu-id="999c8-4141">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4141">4</span></span>

<span data-ttu-id="999c8-4142">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4142">5</span></span>

<span data-ttu-id="999c8-4143">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4143">6</span></span>

<span data-ttu-id="999c8-4144">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4144">7</span></span>

<span data-ttu-id="999c8-4145">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4145">8</span></span>

<span data-ttu-id="999c8-4146">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4146">9</span></span>

<span data-ttu-id="999c8-4147">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4147">3</span></span><br/> <span data-ttu-id="999c8-4148">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4148">0</span></span><br/>

<span data-ttu-id="999c8-4149">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4149">1</span></span>

<span data-ttu-id="999c8-4150">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="999c8-4150">\_dwComparison</span></span>



 

<span data-ttu-id="999c8-4151">\_**dwComparison**: l’une des valeurs suivantes, indiquant les positions relatives des deux signets dans le chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4151">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="999c8-4152">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-4152">Value</span></span>                               | <span data-ttu-id="999c8-4153">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-4153">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="999c8-4154">DBCOMPARE \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-4154">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="999c8-4155">Le premier signet est positionné avant le deuxième.</span><span class="sxs-lookup"><span data-stu-id="999c8-4155">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="999c8-4156">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="999c8-4156">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="999c8-4157">Le premier signet a la même position que le second.</span><span class="sxs-lookup"><span data-stu-id="999c8-4157">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="999c8-4158">DBCOMPARE \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="999c8-4158">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="999c8-4159">Le premier signet est positionné après le deuxième.</span><span class="sxs-lookup"><span data-stu-id="999c8-4159">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="999c8-4160">DBCOMPARE ne \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="999c8-4160">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="999c8-4161">Le premier signet n’a pas la même position que le second.</span><span class="sxs-lookup"><span data-stu-id="999c8-4161">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="999c8-4162">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="999c8-4162">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="999c8-4163">Le premier signet n’est pas comparable au second.</span><span class="sxs-lookup"><span data-stu-id="999c8-4163">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="999c8-4164">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4164">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="999c8-4165">Le message CPMRestartPositionIn déplace la position d’extraction d’un curseur vers le début du chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4165">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="999c8-4166">Comme indiqué dans la section 3.1.5.2.12, le serveur répondra en utilisant le même message, avec les résultats de la requête contenus dans le \_ champ Status de l’en-tête CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-4166">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="999c8-4167">Le format du message CPMRestartPositionIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4167">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-4168">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4168">0</span></span>

<span data-ttu-id="999c8-4169">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4169">1</span></span>

<span data-ttu-id="999c8-4170">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4170">2</span></span>

<span data-ttu-id="999c8-4171">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4171">3</span></span>

<span data-ttu-id="999c8-4172">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4172">4</span></span>

<span data-ttu-id="999c8-4173">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4173">5</span></span>

<span data-ttu-id="999c8-4174">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4174">6</span></span>

<span data-ttu-id="999c8-4175">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4175">7</span></span>

<span data-ttu-id="999c8-4176">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4176">8</span></span>

<span data-ttu-id="999c8-4177">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4177">9</span></span>

<span data-ttu-id="999c8-4178">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4178">1</span></span><br/> <span data-ttu-id="999c8-4179">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4179">0</span></span><br/>

<span data-ttu-id="999c8-4180">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4180">1</span></span>

<span data-ttu-id="999c8-4181">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4181">2</span></span>

<span data-ttu-id="999c8-4182">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4182">3</span></span>

<span data-ttu-id="999c8-4183">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4183">4</span></span>

<span data-ttu-id="999c8-4184">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4184">5</span></span>

<span data-ttu-id="999c8-4185">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4185">6</span></span>

<span data-ttu-id="999c8-4186">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4186">7</span></span>

<span data-ttu-id="999c8-4187">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4187">8</span></span>

<span data-ttu-id="999c8-4188">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4188">9</span></span>

<span data-ttu-id="999c8-4189">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4189">2</span></span><br/> <span data-ttu-id="999c8-4190">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4190">0</span></span><br/>

<span data-ttu-id="999c8-4191">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4191">1</span></span>

<span data-ttu-id="999c8-4192">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4192">2</span></span>

<span data-ttu-id="999c8-4193">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4193">3</span></span>

<span data-ttu-id="999c8-4194">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4194">4</span></span>

<span data-ttu-id="999c8-4195">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4195">5</span></span>

<span data-ttu-id="999c8-4196">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4196">6</span></span>

<span data-ttu-id="999c8-4197">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4197">7</span></span>

<span data-ttu-id="999c8-4198">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4198">8</span></span>

<span data-ttu-id="999c8-4199">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4199">9</span></span>

<span data-ttu-id="999c8-4200">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4200">3</span></span><br/> <span data-ttu-id="999c8-4201">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4201">0</span></span><br/>

<span data-ttu-id="999c8-4202">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4202">1</span></span>

<span data-ttu-id="999c8-4203">\_hCursor (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-4203">\_hCursor (optional)</span></span>

<span data-ttu-id="999c8-4204">\_Chapt (facultatif)</span><span class="sxs-lookup"><span data-stu-id="999c8-4204">\_chapt (optional)</span></span>



 

<span data-ttu-id="999c8-4205">**\_ hCursor**: valeur 32 bits représentant le descripteur, obtenue à partir d’un message CPMCreateQueryOut, qui identifie la requête pour laquelle la position doit être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4205">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="999c8-4206">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4206">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="999c8-4207">**\_ Chapt**: valeur 32 bits représentant le descripteur d’un chapitre à partir duquel récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4207">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="999c8-4208">Ce champ doit être présent lorsque le message est envoyé par le client et doit être absent lorsque le message est envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4208">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="999c8-4209">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4209">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="999c8-4210">Le message CPMFreeCursorIn demande la libération d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4210">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="999c8-4211">Le format du message CPMFreeCursorIn qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4211">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="999c8-4212">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4212">0</span></span>

<span data-ttu-id="999c8-4213">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4213">1</span></span>

<span data-ttu-id="999c8-4214">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4214">2</span></span>

<span data-ttu-id="999c8-4215">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4215">3</span></span>

<span data-ttu-id="999c8-4216">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4216">4</span></span>

<span data-ttu-id="999c8-4217">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4217">5</span></span>

<span data-ttu-id="999c8-4218">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4218">6</span></span>

<span data-ttu-id="999c8-4219">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4219">7</span></span>

<span data-ttu-id="999c8-4220">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4220">8</span></span>

<span data-ttu-id="999c8-4221">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4221">9</span></span>

<span data-ttu-id="999c8-4222">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4222">1</span></span><br/> <span data-ttu-id="999c8-4223">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4223">0</span></span><br/>

<span data-ttu-id="999c8-4224">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4224">1</span></span>

<span data-ttu-id="999c8-4225">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4225">2</span></span>

<span data-ttu-id="999c8-4226">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4226">3</span></span>

<span data-ttu-id="999c8-4227">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4227">4</span></span>

<span data-ttu-id="999c8-4228">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4228">5</span></span>

<span data-ttu-id="999c8-4229">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4229">6</span></span>

<span data-ttu-id="999c8-4230">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4230">7</span></span>

<span data-ttu-id="999c8-4231">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4231">8</span></span>

<span data-ttu-id="999c8-4232">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4232">9</span></span>

<span data-ttu-id="999c8-4233">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4233">2</span></span><br/> <span data-ttu-id="999c8-4234">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4234">0</span></span><br/>

<span data-ttu-id="999c8-4235">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4235">1</span></span>

<span data-ttu-id="999c8-4236">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4236">2</span></span>

<span data-ttu-id="999c8-4237">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4237">3</span></span>

<span data-ttu-id="999c8-4238">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4238">4</span></span>

<span data-ttu-id="999c8-4239">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4239">5</span></span>

<span data-ttu-id="999c8-4240">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4240">6</span></span>

<span data-ttu-id="999c8-4241">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4241">7</span></span>

<span data-ttu-id="999c8-4242">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4242">8</span></span>

<span data-ttu-id="999c8-4243">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4243">9</span></span>

<span data-ttu-id="999c8-4244">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4244">3</span></span><br/> <span data-ttu-id="999c8-4245">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4245">0</span></span><br/>

<span data-ttu-id="999c8-4246">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4246">1</span></span>

<span data-ttu-id="999c8-4247">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="999c8-4247">\_hCursor</span></span>



 

<span data-ttu-id="999c8-4248">**\_ hCursor**: valeur 32 bits représentant le handle du curseur du message CPMCreateQueryOut à libérer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4248">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="999c8-4249">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4249">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="999c8-4250">Le message CPMFreeCursorOut répond à un message CPMFreeCursorIn avec les résultats de la libération d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4250">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="999c8-4251">Le format du message CPMFreeCursorOut qui suit l’en-tête est le suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4251">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="999c8-4252">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4252">0</span></span>

<span data-ttu-id="999c8-4253">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4253">1</span></span>

<span data-ttu-id="999c8-4254">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4254">2</span></span>

<span data-ttu-id="999c8-4255">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4255">3</span></span>

<span data-ttu-id="999c8-4256">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4256">4</span></span>

<span data-ttu-id="999c8-4257">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4257">5</span></span>

<span data-ttu-id="999c8-4258">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4258">6</span></span>

<span data-ttu-id="999c8-4259">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4259">7</span></span>

<span data-ttu-id="999c8-4260">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4260">8</span></span>

<span data-ttu-id="999c8-4261">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4261">9</span></span>

<span data-ttu-id="999c8-4262">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4262">1</span></span><br/> <span data-ttu-id="999c8-4263">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4263">0</span></span><br/>

<span data-ttu-id="999c8-4264">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4264">1</span></span>

<span data-ttu-id="999c8-4265">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4265">2</span></span>

<span data-ttu-id="999c8-4266">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4266">3</span></span>

<span data-ttu-id="999c8-4267">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4267">4</span></span>

<span data-ttu-id="999c8-4268">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4268">5</span></span>

<span data-ttu-id="999c8-4269">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4269">6</span></span>

<span data-ttu-id="999c8-4270">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4270">7</span></span>

<span data-ttu-id="999c8-4271">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4271">8</span></span>

<span data-ttu-id="999c8-4272">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4272">9</span></span>

<span data-ttu-id="999c8-4273">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4273">2</span></span><br/> <span data-ttu-id="999c8-4274">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4274">0</span></span><br/>

<span data-ttu-id="999c8-4275">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4275">1</span></span>

<span data-ttu-id="999c8-4276">2</span><span class="sxs-lookup"><span data-stu-id="999c8-4276">2</span></span>

<span data-ttu-id="999c8-4277">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4277">3</span></span>

<span data-ttu-id="999c8-4278">4</span><span class="sxs-lookup"><span data-stu-id="999c8-4278">4</span></span>

<span data-ttu-id="999c8-4279">5</span><span class="sxs-lookup"><span data-stu-id="999c8-4279">5</span></span>

<span data-ttu-id="999c8-4280">6</span><span class="sxs-lookup"><span data-stu-id="999c8-4280">6</span></span>

<span data-ttu-id="999c8-4281">7</span><span class="sxs-lookup"><span data-stu-id="999c8-4281">7</span></span>

<span data-ttu-id="999c8-4282">8</span><span class="sxs-lookup"><span data-stu-id="999c8-4282">8</span></span>

<span data-ttu-id="999c8-4283">9</span><span class="sxs-lookup"><span data-stu-id="999c8-4283">9</span></span>

<span data-ttu-id="999c8-4284">3</span><span class="sxs-lookup"><span data-stu-id="999c8-4284">3</span></span><br/> <span data-ttu-id="999c8-4285">0</span><span class="sxs-lookup"><span data-stu-id="999c8-4285">0</span></span><br/>

<span data-ttu-id="999c8-4286">1</span><span class="sxs-lookup"><span data-stu-id="999c8-4286">1</span></span>

<span data-ttu-id="999c8-4287">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="999c8-4287">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="999c8-4288">**\_ cCursorsRemaining**: entier non signé 32 bits indiquant le nombre de curseurs encore utilisés pour la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4288">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="999c8-4289">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="999c8-4289">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="999c8-4290">Le message CPMDisconnect met fin à la connexion avec le serveur</span><span class="sxs-lookup"><span data-stu-id="999c8-4290">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="999c8-4291">Le message ne doit pas inclure un corps ; seul l’en-tête de message, tel que spécifié dans la section 2.2.2, doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="999c8-4291">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="999c8-4292">Erreurs 2.2.4</span><span class="sxs-lookup"><span data-stu-id="999c8-4292">2.2.4 Errors</span></span>

<span data-ttu-id="999c8-4293">Tous les messages du protocole de service d’indexation de contenu doivent retourner 0x00000000 en cas de réussite ; dans le cas contraire, ils retournent un code d’erreur non nul 32 bits qui peut être un HRESULT ou une valeur NTSTATUS (voir la section 1,8).</span><span class="sxs-lookup"><span data-stu-id="999c8-4293">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="999c8-4294">Si une mémoire tampon est trop petite pour contenir un résultat, un code d’état de \_ l’État ressources insuffisantes \_ (0XC0000009A) doit être retourné et l’opération ayant échoué doit être retentée avec une mémoire tampon plus grande.</span><span class="sxs-lookup"><span data-stu-id="999c8-4294">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="999c8-4295">Toutes les autres valeurs d’erreur doivent être traitées de la même façon.</span><span class="sxs-lookup"><span data-stu-id="999c8-4295">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="999c8-4296">(Notez que actuellement, les espaces de numérotation HRESULT et NTSTATUS ne se chevauchent pas, à l’exception des valeurs de signification identique, mais même s’ils étaient des conflits à l’avenir, cela ne provoque aucun problème de protocole tant que la valeur de l’état \_ Les ressources insuffisantes \_ restent uniques, car toutes les autres valeurs d’erreur sont traitées de la même façon.)</span><span class="sxs-lookup"><span data-stu-id="999c8-4296">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="999c8-4297">3 Détails du protocole</span><span class="sxs-lookup"><span data-stu-id="999c8-4297">3 Protocol Details</span></span>

-   [<span data-ttu-id="999c8-4298">Détails du serveur 3,1</span><span class="sxs-lookup"><span data-stu-id="999c8-4298">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="999c8-4299">Détails du client 3,2</span><span class="sxs-lookup"><span data-stu-id="999c8-4299">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="999c8-4300">Les demandes de message CISP pour l’interrogation à distance des catalogues du service d’indexation ne nécessitent pas de séquence particulière.</span><span class="sxs-lookup"><span data-stu-id="999c8-4300">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="999c8-4301">Il est recommandé que la couche supérieure adhère à une séquence de messages significative, comme pour les messages reçus à partir de cette séquence ou avec des données non valides, le serveur répond avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4301">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="999c8-4302">Certains messages dépendent également de la couche supérieure qui fournit des données valides qui ont été reçues dans les messages précédemment dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="999c8-4302">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="999c8-4303">Une séquence de message standard pour une requête simple à partir d’un client vers un ordinateur distant est illustrée dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="999c8-4303">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![séquence de message pour une requête simple](images/protocoldetails.jpg)

<span data-ttu-id="999c8-4305">Les messages représentés dans le diagramme précédent représentent un sous-ensemble de tous les messages CISP utilisés pour l’interrogation d’un catalogue du service d’indexation à distance.</span><span class="sxs-lookup"><span data-stu-id="999c8-4305">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="999c8-4306">Détails du serveur 3,1</span><span class="sxs-lookup"><span data-stu-id="999c8-4306">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="999c8-4307">3.1.1 Modèle de données abstraites</span><span class="sxs-lookup"><span data-stu-id="999c8-4307">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="999c8-4308">La section suivante spécifie les données et l’état géré par le serveur CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-4308">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="999c8-4309">Les données fournies ici sont pour faciliter l’explication du comportement du protocole.</span><span class="sxs-lookup"><span data-stu-id="999c8-4309">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="999c8-4310">Cette section ne stipule pas que les implémentations adhèrent à ce modèle tant que leur comportement externe est cohérent avec celui décrit dans ce document.</span><span class="sxs-lookup"><span data-stu-id="999c8-4310">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="999c8-4311">Un service d’indexation qui implémente CISP doit conserver les éléments de données abstraits suivants :</span><span class="sxs-lookup"><span data-stu-id="999c8-4311">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="999c8-4312">Liste des clients connectés au serveur</span><span class="sxs-lookup"><span data-stu-id="999c8-4312">The list of clients connected to the server</span></span>
-   <span data-ttu-id="999c8-4313">Informations sur chaque client, notamment :</span><span class="sxs-lookup"><span data-stu-id="999c8-4313">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="999c8-4314">Version du client (comme indiqué dans le message CPMConnectIn spécifié dans la section 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="999c8-4314">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="999c8-4315">Catalogue associé au client (par un message CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="999c8-4315">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="999c8-4316">Propriétés client supplémentaires comme indiqué dans la section 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-4316">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="999c8-4317">Requête de recherche du client</span><span class="sxs-lookup"><span data-stu-id="999c8-4317">Client's search query</span></span>
    -   <span data-ttu-id="999c8-4318">Liste des handles de curseur pour la requête et la position dans le jeu de résultats pour chaque descripteur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4318">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="999c8-4319">Ensemble actuel de liaisons</span><span class="sxs-lookup"><span data-stu-id="999c8-4319">Current set of bindings</span></span>
    -   <span data-ttu-id="999c8-4320">État actuel de la requête qui comprend (pour chaque curseur) :</span><span class="sxs-lookup"><span data-stu-id="999c8-4320">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="999c8-4321">Nombre de lignes dans le résultat de la requête</span><span class="sxs-lookup"><span data-stu-id="999c8-4321">Number of rows in query result</span></span>
        -   <span data-ttu-id="999c8-4322">Numérateur et dénominateur de la saisie semi-automatique des requêtes</span><span class="sxs-lookup"><span data-stu-id="999c8-4322">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="999c8-4323">Nombre de lignes indiqué par le message CPMRatioFinishedOut le plus récent pour ce curseur</span><span class="sxs-lookup"><span data-stu-id="999c8-4323">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="999c8-4324">Si la requête est analysée par le serveur pour les modifications des résultats de la requête et si elle est analysée, ce qui a changé dans les résultats de la requête depuis son dernier rapport au client par CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4324">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="999c8-4325">Liste des descripteurs de chapitres, servis par cette requête à un client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4325">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="999c8-4326">Liste de handles de signet pour chaque curseur, servie par cette requête à un client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4326">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="999c8-4327">État actuel du service d’indexation, qui peut être « non initialisé », « en cours d’exécution » ou « arrêt en cours ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4327">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="999c8-4328">Notez que la plupart du serveur de temps est dans l’État « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4328">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="999c8-4329">Voici le diagramme d’ordinateur d’État pour le serveur :</span><span class="sxs-lookup"><span data-stu-id="999c8-4329">Following is the state machine diagram for the server:</span></span>

    ![diagramme d’ordinateur d’État du serveur de service d’indexation](images/abstractdatamodel.jpg)

-   <span data-ttu-id="999c8-4331">Informations par catalogue : nombre de documents indexés, taille de l’index, nombre de clés uniques, etc. (voir la section 2.2.3.1 pour obtenir la liste complète), State (qui correspond aux valeurs de dwNewState dans la section 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="999c8-4331">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="999c8-4332">Pour chaque langue prise en charge, une base de données de variantes Word, comme indiqué dans la section 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="999c8-4332">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="999c8-4333">3.1.2 Minuteurs</span><span class="sxs-lookup"><span data-stu-id="999c8-4333">3.1.2 Timers</span></span>

<span data-ttu-id="999c8-4334">Aucun minuteur de protocole n’est requis.</span><span class="sxs-lookup"><span data-stu-id="999c8-4334">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="999c8-4335">3.1.3 Initialisation</span><span class="sxs-lookup"><span data-stu-id="999c8-4335">3.1.3 Initialization</span></span>

<span data-ttu-id="999c8-4336">Lors de l’initialisation, le serveur doit définir son état sur « non initialisé » et commencer à écouter les messages sur le canal nommé spécifié dans la section 1,9.</span><span class="sxs-lookup"><span data-stu-id="999c8-4336">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="999c8-4337">Une fois l’initialisation interne effectuée, elle doit passer à l’État « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4337">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="999c8-4338">3.1.4 Événements déclenchés de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="999c8-4338">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="999c8-4339">Aucun.</span><span class="sxs-lookup"><span data-stu-id="999c8-4339">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="999c8-4340">Règles de traitement et de séquencement des messages 3.1.5</span><span class="sxs-lookup"><span data-stu-id="999c8-4340">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="999c8-4341">À chaque fois qu’une erreur se produit lors du traitement d’un message envoyé par un client, le serveur doit signaler une erreur au client comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4341">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="999c8-4342">Arrêter le traitement du message envoyé par le client</span><span class="sxs-lookup"><span data-stu-id="999c8-4342">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="999c8-4343">Répondre avec l’en-tête de message (uniquement) du message envoyé par le client, en conservant le \_ champ MSG intact.</span><span class="sxs-lookup"><span data-stu-id="999c8-4343">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="999c8-4344">Définissez le \_ champ État sur la valeur du code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4344">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="999c8-4345">Lorsqu’un message arrive, le serveur doit vérifier la \_ valeur du champ MSG pour déterminer s’il s’agit d’un type connu (voir la section 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="999c8-4345">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="999c8-4346">Si le type n’est pas connu, il doit signaler un état d' \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4346">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="999c8-4347">Le serveur doit ensuite valider la \_ valeur du champ ulChecksum si le type de message est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="999c8-4347">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="999c8-4348">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="999c8-4348">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="999c8-4349">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="999c8-4349">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="999c8-4350">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="999c8-4350">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="999c8-4351">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="999c8-4351">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="999c8-4352">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="999c8-4352">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="999c8-4353">Pour valider la \_ valeur du champ ulChecksum, le serveur doit vérifier la valeur spécifiée par le client dans le \_ champ iClientVersion du message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4353">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="999c8-4354">Si le \_ champ iClientVersion n’a pas la valeur 0x00000008 et que le \_ champ ulChecksum n’a pas la valeur 0x00000000, le serveur doit signaler une \_ erreur de paramètre non valide d’état \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4354">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="999c8-4355">Le serveur ne doit pas valider le \_ champ ulChecksum pour les clients \_ . le champ iClientVersion a une valeur inférieure à 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="999c8-4355">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="999c8-4356">Si la \_ valeur du champ iClientVersionfield est 0x00000008 ou supérieure, le serveur doit vérifier que le \_ champ ulChecksum a été calculé comme indiqué dans la section 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="999c8-4356">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="999c8-4357">Si la \_ valeur ulChecksum n’est pas valide, le serveur doit signaler une \_ erreur de paramètre non valide d’état \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4357">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="999c8-4358">Ensuite, le serveur vérifie l’État dans lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="999c8-4358">Next, the server checks which state is it in.</span></span> <span data-ttu-id="999c8-4359">Si son état est « non initialisé », le serveur doit signaler une \_ erreur d’E/t \_ non \_ initialisée (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="999c8-4359">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="999c8-4360">Si l’État est « arrêt en cours », le serveur doit signaler une \_ erreur d’arrêt de l’E/ \_ 0X80041812 (ci).</span><span class="sxs-lookup"><span data-stu-id="999c8-4360">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="999c8-4361">Une fois qu’un en-tête a été déterminé comme étant valide et que le serveur est en état d’exécution, un traitement spécifique des messages doit être effectué comme indiqué dans les sous-sections ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="999c8-4361">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="999c8-4362">Gestion du catalogue du service d’indexation à distance 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="999c8-4362">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="999c8-4363">3.1.5.1.1 recevant une demande CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4363">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="999c8-4364">Lorsque le serveur reçoit une demande de message CPMCIStateInOut du client, le serveur doit d’abord vérifier si le client figure dans une liste de clients connectés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4364">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="999c8-4365">Si le client ne figure pas dans la liste, le serveur doit signaler une erreur de paramètre d’état \_ non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4365">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="999c8-4366">Dans le cas contraire, il doit répondre au client avec un message CPMCIStateInOut, en le remplissant avec les informations relatives au catalogue associé du client, comme indiqué dans la section 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="999c8-4366">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="999c8-4367">3.1.5.1.2 recevant une demande CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4367">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="999c8-4368">Lorsque le serveur reçoit une demande de message CPMSetCatStateIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4368">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4369">Vérifiez que le client dispose d’un accès administratif.</span><span class="sxs-lookup"><span data-stu-id="999c8-4369">Check that client has administrative access.</span></span> <span data-ttu-id="999c8-4370">Si le client ne dispose pas d’un accès administrateur, le serveur doit signaler une erreur d’état \_ accès \_ refusé (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="999c8-4370">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="999c8-4371">Si \_ dwNewState n’est pas égal à CICAT \_ All \_ Opened, modifiez l’état du catalogue spécifié dans le champ CatName comme spécifié par le \_ champ dwNewState.</span><span class="sxs-lookup"><span data-stu-id="999c8-4371">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="999c8-4372">Pour plus d’informations, consultez la section 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="999c8-4372">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="999c8-4373">Si le serveur ne trouve pas de catalogue avec le nom spécifié dans le champ CatName, le serveur doit retourner une \_ erreur de paramètre non valide de l’état \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4373">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4374">Répondez au client avec un message CPMSetCatStateOut, où \_ DWOLDSTATE doit être défini à l’état précédent du catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-4374">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="999c8-4375">Si \_ dwNewState est égal à CICAT \_ All \_ Opened, le serveur doit vérifier l’état de tous les catalogues et, s’ils sont tous démarrés, il doit définir \_ dwOldState sur 0x00000001 et, sinon, définir \_ dwOldState sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4375">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="999c8-4376">3.1.5.1.3 recevant une demande CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4376">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="999c8-4377">Lorsque le serveur reçoit une demande de message CPMUpdateDocumentsIn, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4377">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4378">Vérifiez si le client figure dans une liste de clients connectés (auxquels est associé un catalogue).</span><span class="sxs-lookup"><span data-stu-id="999c8-4378">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="999c8-4379">Si le client ne figure pas dans la liste, le serveur doit signaler une erreur de paramètre d’état \_ non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4379">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4380">Vérifiez que le client dispose d’un accès administratif.</span><span class="sxs-lookup"><span data-stu-id="999c8-4380">Check that client has administrative access.</span></span> <span data-ttu-id="999c8-4381">Si le client ne dispose pas d’un accès administratif au serveur, le serveur doit signaler une \_ erreur d’accès \_ refusé (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="999c8-4381">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="999c8-4382">Commencez le processus d’indexation du chemin d’accès spécifié par le client, en procédant à une analyse complète ou incrémentielle, en fonction de la valeur du \_ champ d’indicateur dans le message CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4382">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="999c8-4383">Si le chemin d’accès n’était pas déjà indexé, il doit être ajouté à la collection d’emplacements indexés et une analyse complète est effectuée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4383">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="999c8-4384">Si une valeur non conforme du \_ champ indicateur est spécifiée, le serveur doit agir comme si \_ Flag était défini sur UPD \_ Init et effectuer une analyse complète.</span><span class="sxs-lookup"><span data-stu-id="999c8-4384">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="999c8-4385">Cette opération doit être effectuée dans le catalogue associé au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4385">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="999c8-4386">Répondez au client avec l’en-tête de message pour CPMUpdateDocumentsIn et définissez le \_ champ Status sur les résultats de la demande.</span><span class="sxs-lookup"><span data-stu-id="999c8-4386">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="999c8-4387">3.1.5.1.4 recevant une demande CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4387">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="999c8-4388">Lorsque le serveur reçoit une demande de message CPMForceMergeIn, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4388">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4389">Vérifiez si le client figure dans une liste de clients connectés (auxquels est associé un catalogue).</span><span class="sxs-lookup"><span data-stu-id="999c8-4389">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="999c8-4390">Si le client ne figure pas dans la liste, le serveur doit signaler un état d' \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4390">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4391">Vérifiez que le client dispose d’un accès administratif.</span><span class="sxs-lookup"><span data-stu-id="999c8-4391">Check that client has administrative access.</span></span> <span data-ttu-id="999c8-4392">Si le client ne dispose pas d’un accès administrateur, le serveur doit signaler une erreur d’état \_ accès \_ refusé (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="999c8-4392">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="999c8-4393">Commencez tout processus de maintenance nécessaire pour améliorer les performances des requêtes sur un catalogue, associées au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4393">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="999c8-4394">Répondez au client avec un en-tête de message pour CPMForceMergeIn et définissez le \_ champ Status sur les résultats de la demande.</span><span class="sxs-lookup"><span data-stu-id="999c8-4394">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="999c8-4395">Notez que le processus de maintenance est asynchrone et peut continuer une fois que le client a reçu le message de réponse.</span><span class="sxs-lookup"><span data-stu-id="999c8-4395">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="999c8-4396">Ce processus n’affecte pas directement le protocole de quelque façon que ce soit (autre que le temps de réponse).</span><span class="sxs-lookup"><span data-stu-id="999c8-4396">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="999c8-4397">interrogation du service d’indexation à distance 3.1.5.2</span><span class="sxs-lookup"><span data-stu-id="999c8-4397">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="999c8-4398">3.1.5.2.1 recevant une demande CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4398">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="999c8-4399">Lorsque le serveur reçoit une requête CPMConnectIn à partir d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4399">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4400">Vérifiez si le client figure dans la liste des clients connectés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4400">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="999c8-4401">Si c’est le cas, le serveur doit signaler une \_ erreur de \_ paramètre non valide (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4401">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4402">Vérifie si le catalogue spécifié existe et s’il n’est pas à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="999c8-4402">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="999c8-4403">Si ce n’est pas le cas, le serveur doit disposer d’une erreur de l’état d' \_ \_ absence du \_ catalogue (0x8004181D) du rapport ci.</span><span class="sxs-lookup"><span data-stu-id="999c8-4403">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="999c8-4404">Ajoutez le client à la liste des clients connectés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4404">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="999c8-4405">Associez le catalogue au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4405">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="999c8-4406">Stockez les informations transmises dans le message CPMConnectIn (telles que le nom du catalogue, la version du client, etc.) dans l’état du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4406">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="999c8-4407">Répondez au client avec un message CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4407">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="999c8-4408">3.1.5.2.2 recevant une demande CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4408">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="999c8-4409">Lorsque le serveur reçoit une demande de message CPMCreateQueryIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4409">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4410">Vérifiez si le client figure dans la liste des clients connectés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4410">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="999c8-4411">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4411">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4412">Vérifiez si une requête est déjà associée au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4412">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="999c8-4413">Si c’est le cas, le serveur doit signaler une \_ erreur de \_ paramètre non valide (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4413">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4414">Vérifiez si le catalogue associé au client est dans l’État, ce qui permet le traitement de la requête (CICAT \_ ReadOnly ou CICAT \_ accessible en écriture).</span><span class="sxs-lookup"><span data-stu-id="999c8-4414">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="999c8-4415">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur requête S \_ aucune \_ requête (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="999c8-4415">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="999c8-4416">Analysez l’ensemble de restrictions, les ordres de tri et les regroupements spécifiés dans la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4416">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="999c8-4417">Si le serveur rencontre une erreur, il doit signaler une erreur appropriée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4417">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="999c8-4418">Si cette étape échoue pour une autre raison, le serveur doit signaler l’erreur rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4418">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="999c8-4419">Pour plus d’informations sur les erreurs de requête du service d’indexation, consultez \[ MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="999c8-4419">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="999c8-4420">Enregistrez la requête de recherche dans l’état du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4420">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="999c8-4421">Effectuez les préparatifs nécessaires pour servir les lignes à un client et associez la requête aux handles de curseur appropriés (en fonction des informations transmises dans le message CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="999c8-4421">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="999c8-4422">Ajoutez ces handles à la liste des handles de curseurs du client et initialisez les listes de handles de chapitre et de signets.</span><span class="sxs-lookup"><span data-stu-id="999c8-4422">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="999c8-4423">Initialise la liste des descripteurs de chapitre pour chaque curseur de cette requête sur DB \_ null \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="999c8-4423">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="999c8-4424">Initialisez la liste des descripteurs de signet pour chaque curseur de cette requête sur un ensemble de DBBMK \_ et de DBBMK en \_ dernier.</span><span class="sxs-lookup"><span data-stu-id="999c8-4424">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="999c8-4425">Marquez la requête comme non surveillée pour les modifications.</span><span class="sxs-lookup"><span data-stu-id="999c8-4425">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="999c8-4426">Initialisez le nombre de lignes sur le nombre de lignes actuellement calculé (ce qui peut être 0 si la requête n’a pas commencé à s’exécuter ou un nombre si la requête est en cours d’exécution) et initialisez le numérateur et le dénominateur de la saisie semi-automatique des requêtes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4426">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="999c8-4427">Répondez au client avec un message CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4427">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="999c8-4428">3.1.5.2.3 recevant une demande CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4428">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="999c8-4429">Lorsque le serveur reçoit une demande de message CPMGetQueryStatusIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4429">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4430">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4430">Check if the client has query associated with it.</span></span> <span data-ttu-id="999c8-4431">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4431">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4432">Vérifiez si le handle de curseur se trouve dans une liste de handles de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4432">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="999c8-4433">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4433">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4434">Préparez un message CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4434">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="999c8-4435">Le serveur doit récupérer l’état actuel de la requête et le définir dans le \_ champ QStatus (consultez 2.2.3.11 pour connaître les valeurs possibles).</span><span class="sxs-lookup"><span data-stu-id="999c8-4435">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="999c8-4436">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4436">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="999c8-4437">Répondez au client avec le message CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4437">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="999c8-4438">3.1.5.2.4 recevant une demande CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4438">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="999c8-4439">Lorsque le serveur reçoit une demande de message CPMGetQueryStatusExIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4439">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4440">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4440">Check if the client has a query associated with it.</span></span> <span data-ttu-id="999c8-4441">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4441">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4442">Vérifiez si le handle de curseur réussi figure dans une liste de handles de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4442">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="999c8-4443">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4443">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4444">Préparez un message CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4444">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="999c8-4445">Le serveur doit récupérer l’état de la requête actuelle et la progression de la requête et définir QStatus (consultez 2.2.3.11 pour connaître les valeurs possibles), \_ dwRatioFinishedDenominator et \_ dwRatioFinishedNumerator respectivement.</span><span class="sxs-lookup"><span data-stu-id="999c8-4445">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="999c8-4446">Il doit ensuite définir le nombre de lignes dans les résultats de la requête sur \_ cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="999c8-4446">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="999c8-4447">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4447">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="999c8-4448">Récupérez des informations sur le catalogue du client et remplissez \_ cFilteredDocuments et \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="999c8-4448">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="999c8-4449">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4449">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="999c8-4450">Récupérez la position du signet indiquée par la poignée dans le \_ champ BMK, puis remplissez le \_ champ iRowBmk restant dans le message CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4450">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="999c8-4451">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4451">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="999c8-4452">Répondez au client avec le message CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4452">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="999c8-4453">3.1.5.2.5 recevant une demande CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4453">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="999c8-4454">Lorsque le serveur reçoit une demande de message CPMRatioFinishedIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4454">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4455">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4455">Check if the client has query associated with it.</span></span> <span data-ttu-id="999c8-4456">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4456">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4457">Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4457">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="999c8-4458">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4458">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4459">Préparez un message CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4459">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="999c8-4460">Le serveur doit récupérer l’état de la requête du client et remplir les \_ champs ulNumerator, \_ ulDenominator et \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="999c8-4460">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="999c8-4461">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4461">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="999c8-4462">Si \_ Crows est égal au dernier nombre de lignes signalées pour cette requête, définissez \_ fNewRows sur 0x00000000. sinon, affectez-lui la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-4462">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="999c8-4463">Met à jour le dernier nombre de lignes signalées pour cette requête à la valeur de \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="999c8-4463">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="999c8-4464">Répondez au client avec le message CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4464">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="999c8-4465">3.1.5.2.6 recevant une demande CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4465">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="999c8-4466">Lorsque le serveur reçoit une demande de message CPMSetBindingsIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4466">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4467">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4467">Check if the client has a query associated with it.</span></span> <span data-ttu-id="999c8-4468">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4468">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4469">Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4469">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="999c8-4470">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4470">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4471">Vérifiez que les informations de liaison sont valides (c’est-à-dire que la colonne spécifie au moins la valeur, la longueur ou l’État à renvoyer ; aucun chevauchement des liaisons pour la valeur, la longueur ou l’État ; et la valeur, la longueur et l’État s’ajustent à la taille de ligne spécifiée) et si aucune erreur de base de données \_ \_ BADBINDINFO (0x80040E08) n’est signalée</span><span class="sxs-lookup"><span data-stu-id="999c8-4471">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="999c8-4472">Enregistrez les informations de liaison associées aux colonnes spécifiées dans le champ aColumns.</span><span class="sxs-lookup"><span data-stu-id="999c8-4472">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="999c8-4473">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4473">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="999c8-4474">Répondez au client avec un en-tête de message (uniquement) avec \_ MSG défini sur CPMSetBindingsIn et \_ Status défini sur les résultats de la liaison spécifiée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4474">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="999c8-4475">3.1.5.2.7 recevant une demande CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4475">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="999c8-4476">Lorsque le serveur reçoit une demande de message CPMGetRowsIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4476">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4477">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4477">Check if the client has query associated with it.</span></span> <span data-ttu-id="999c8-4478">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4478">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4479">Vérifiez si le handle de curseur passé est dans athelist des handles de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4479">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="999c8-4480">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4480">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4481">Vérifiez si le client dispose d’un ensemble de liaisons en cours.</span><span class="sxs-lookup"><span data-stu-id="999c8-4481">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="999c8-4482">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4482">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4483">Préparez un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4483">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="999c8-4484">Le serveur doit positionner le curseur dans les résultats de la requête comme indiqué par la description de la recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-4484">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="999c8-4485">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4485">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="999c8-4486">Récupérez autant de lignes que vous le configurez dans une mémoire tampon, dont la taille est indiquée par \_ cbReadBuffer, mais pas plus que ce qui est indiqué par \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4486">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="999c8-4487">Lors de l’extraction de lignes, le serveur doit comparer le type de valeur de propriété de chaque colonne sélectionnée au type spécifié dans le jeu de liaisons actuel du client (section 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="999c8-4487">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="999c8-4488">Si le type de la liaison n’est pas de type VT \_ , le serveur doit tenter de convertir la valeur de la propriété de la colonne en ce type.</span><span class="sxs-lookup"><span data-stu-id="999c8-4488">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="999c8-4489">Sinon, si l' \_ indicateur DBPROP USEEXTENDEDDBTYPES est défini dans le jeu de propriétés DBPROPSET QUERYEXT du client \_ , ou si la valeur de la propriété de la colonne n’est pas un \_ type de vecteur VT, la valeur de la propriété doit être retournée dans son type normal.</span><span class="sxs-lookup"><span data-stu-id="999c8-4489">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="999c8-4490">Si aucune de ces conditions n’est respectée (c’est-à-dire que le serveur a un \_ type de vecteur VT et que le client ne prend pas en charge VT \_ Vector), le serveur doit tenter de le convertir en un \_ type de tableau VT comme suit : les \_ éléments VT I8, VT \_ UI8, VT \_ fileTime et VT \_ CLSID du tableau ne peuvent pas être convertis et échouent à la place ; \_ \_ Les éléments de tableau VT LPSTR et VT LPWStr doivent être convertis en \_ BSTR BSTR ; les éléments de tableau de tous les autres types doivent rester inchangés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4490">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="999c8-4491">Enfin, si les colonnes de ligne contiennent des handles de chapitre ou de signet, le serveur doit mettre à jour les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4491">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="999c8-4492">Si cette étape échoue pour une raison quelconque, le serveur doit signaler qu’une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4492">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="999c8-4493">Stockez le nombre réel de lignes extraites dans \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="999c8-4493">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="999c8-4494">Copiez la description de recherche et le champ de chapitre de CPMGetRowsIn dans un message CPMGetRowsOut à envoyer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4494">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="999c8-4495">Stockez les lignes extraites dans le champ Rows (voir la remarque sur l’octet d’état ci-dessous et la section 2.2.3.16 dans la structure du champ Rows).</span><span class="sxs-lookup"><span data-stu-id="999c8-4495">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="999c8-4496">Répondez au client avec le message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4496">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="999c8-4497">Remarque sur le champ octet d’État :</span><span class="sxs-lookup"><span data-stu-id="999c8-4497">Note on status byte field:</span></span>

<span data-ttu-id="999c8-4498">Si StatusUsed est défini sur 0x01 dans le CTableColumn du message CPMSetBindingIn pour la colonne, le serveur doit définir l’octet d’État (qui se trouve à StatusOffset à partir du début de la ligne) pour cette colonne à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4498">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="999c8-4499">Value</span><span class="sxs-lookup"><span data-stu-id="999c8-4499">Value</span></span> | <span data-ttu-id="999c8-4500">Signification</span><span class="sxs-lookup"><span data-stu-id="999c8-4500">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="999c8-4501">0x00</span><span class="sxs-lookup"><span data-stu-id="999c8-4501">0x00</span></span>  | <span data-ttu-id="999c8-4502">StatusOK</span><span class="sxs-lookup"><span data-stu-id="999c8-4502">StatusOK</span></span>       |
| <span data-ttu-id="999c8-4503">0x01</span><span class="sxs-lookup"><span data-stu-id="999c8-4503">0x01</span></span>  | <span data-ttu-id="999c8-4504">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="999c8-4504">StatusDeferred</span></span> |
| <span data-ttu-id="999c8-4505">0x02</span><span class="sxs-lookup"><span data-stu-id="999c8-4505">0x02</span></span>  | <span data-ttu-id="999c8-4506">StatusNull</span><span class="sxs-lookup"><span data-stu-id="999c8-4506">StatusNull</span></span>     |



 

<span data-ttu-id="999c8-4507">Si la valeur de propriété est absente pour cette ligne, le serveur doit définir l’octet d’État sur StatusNull.</span><span class="sxs-lookup"><span data-stu-id="999c8-4507">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="999c8-4508">Si la valeur est trop grande pour être transférée dans le message CPMGetRowsOut, le serveur doit définir l’octet d’État sur StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="999c8-4508">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="999c8-4509">Dans le cas contraire, le serveur doit définir l’octet d’État sur StatusOK.</span><span class="sxs-lookup"><span data-stu-id="999c8-4509">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="999c8-4510">3.1.5.2.8 recevant une demande CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4510">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="999c8-4511">Lorsque le serveur reçoit une demande de message CPMFetchValueIn d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4511">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4512">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4512">Check if the client has query associated with it.</span></span> <span data-ttu-id="999c8-4513">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4513">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4514">Préparez un message CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4514">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="999c8-4515">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4515">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="999c8-4516">Recherchez le document indiqué par le \_ champ wid et vérifiez si l’ID de propriété de ce document (ultérieurement appelé « valeur de propriété ») indiqué par la structure PropSpec est disponible pour ce client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4516">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="999c8-4517">Si cette valeur n’est pas disponible, le serveur doit définir \_ fValueExists sur 0x00000000 et, sinon, définir \_ fValueExists sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-4517">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="999c8-4518">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="999c8-4519">Si \_ fValueExists est égal à 0x00000001, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4519">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="999c8-4520">Sérialisez la valeur de la propriété dans une structure SERIALIZEDPROPERTYVALUE et copiez-la, en commençant par l' \_ offset cbSoFar, au maximum \_ cbChunk octets (mais sans dépasser la fin de la propriété sérialisée) dans le champ vValue.</span><span class="sxs-lookup"><span data-stu-id="999c8-4520">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="999c8-4521">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4521">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="999c8-4522">Définissez \_ cbValue sur le nombre d’octets copiés à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="999c8-4522">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="999c8-4523">Définissez vType sur le type de propriété de la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-4523">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="999c8-4524">Si la longueur de la propriété sérialisée est supérieure à \_ cbSoFar ajoutée à \_ cbValue, affectez à fMoreExists la valeur \_ 0x00000001. sinon, affectez-lui la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4524">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="999c8-4525">Répondre au client avec le message CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4525">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="999c8-4526">3.1.5.2.9 recevant une demande CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="999c8-4526">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="999c8-4527">Lorsque le serveur reçoit un message CPMGetNotify d’un client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4527">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4528">Vérifiez si le client est associé à une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4528">Check if the client has query associated with it.</span></span> <span data-ttu-id="999c8-4529">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4529">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4530">Si aucune modification n’a été apportée dans le jeu de résultats de la requête depuis le dernier message CPMSendNotifyOut pour ce client, ou si la requête n’est pas actuellement surveillée pour les modifications dans le jeu de résultats, le serveur doit répondre avec le message CPMGetNotify et commencer à analyser la requête pour rechercher les modifications dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="999c8-4530">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="999c8-4531">Si, par la suite, une modification est apportée au jeu de résultats de la requête, le serveur doit envoyer un seul message CPMSendNotifyOut au client et doit spécifier la modification dans le \_ champ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="999c8-4531">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="999c8-4532">Si des modifications ont été apportées au jeu de résultats de la requête depuis le dernier message CPMSendNotifyOut, le serveur doit répondre avec CPMSendNotifyOut et doit spécifier la modification dans le \_ champ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="999c8-4532">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="999c8-4533">Notez que, dans le cas de nombreuses modifications des résultats de la requête, DBWATCHNOTIFY \_ ROWSCHANGED prend la priorité (c’est-à-dire, si la requête a été exécutée, réexécutée et que le nombre de lignes modifiées et la requête a été effectué à nouveau, l’événement signalé est DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="999c8-4533">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="999c8-4534">3.1.5.2.10 recevant une demande CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4534">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="999c8-4535">Lorsque le serveur reçoit une demande de message CPMGetApproximatePositionIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4535">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4536">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4536">Check if the client has a query associated with it.</span></span> <span data-ttu-id="999c8-4537">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4537">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4538">Vérifiez si le handle de curseur, le handle de chapitre et le handle de signet passés se trouvent dans les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4538">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="999c8-4539">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4539">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4540">Recherchez une ligne qui est associée au handle de signet dans les résultats de la requête et déterminez approximativement la position de la ligne dans l’ensemble de lignes, référencée par le handle de chapitre, et déterminez le numérateur et le dénominateur de la position.</span><span class="sxs-lookup"><span data-stu-id="999c8-4540">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="999c8-4541">Notez que lorsque le descripteur de chapitre est DB \_ null \_ HCHAPTER, le chapitre correspondant est l’ensemble de lignes principal de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4541">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="999c8-4542">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4542">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="999c8-4543">Répondez au client avec un message CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4543">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="999c8-4544">3.1.5.2.11 recevant une demande CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4544">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="999c8-4545">Lorsque le serveur reçoit une demande de message CPMCompareBmkIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4545">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4546">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4546">Check if the client has a query associated with it.</span></span> <span data-ttu-id="999c8-4547">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4547">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4548">Vérifiez si le handle de curseur, le handle de chapitre et les handles de signet réussis se trouvent dans les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4548">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="999c8-4549">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4549">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4550">Préparez un message CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4550">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="999c8-4551">Si les poignées de signet sont égales, \_ DWCOMPARISON doit avoir la valeur DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="999c8-4551">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="999c8-4552">Sinon, si l’un des descripteurs de signets est DBBMK \_ First ou DBBMK \_ Last, \_ dwComparison doit être défini sur DBCOMPARE ne \_ .</span><span class="sxs-lookup"><span data-stu-id="999c8-4552">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="999c8-4553">Dans le cas contraire, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4553">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="999c8-4554">Rechercher les lignes référencées par chaque handle de signet dans les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="999c8-4554">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="999c8-4555">Si l’une des lignes n’est pas dans le chapitre indiqué par le descripteur de chapitre dans CPMCompareBmkIn, \_ DWCOMPARISON doit être défini sur DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="999c8-4555">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="999c8-4556">Dans le cas contraire, lorsque les deux lignes se trouvent dans le même chapitre, le serveur doit arrondir la position de ces lignes dans l’ensemble de lignes référencé par le handle de ce chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4556">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="999c8-4557">Il doit ensuite comparer les valeurs de position et définir \_ dwComparison sur DBCOMPARE \_ lt si la position de la première ligne est inférieure à la position de la deuxième ligne ; sinon, \_ dwComparison doit être défini sur DBCOMPARE \_ gt.</span><span class="sxs-lookup"><span data-stu-id="999c8-4557">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="999c8-4558">Répondez au client avec un message CPMCompareBmkOut rempli.</span><span class="sxs-lookup"><span data-stu-id="999c8-4558">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="999c8-4559">3.1.5.2.12 recevant une demande CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4559">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="999c8-4560">Lorsque le serveur reçoit la demande de message CPMRestartPositionIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4560">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4561">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4561">Check if the client has a query associated with it.</span></span> <span data-ttu-id="999c8-4562">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4562">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4563">Vérifiez si le handle de curseur et le descripteur de chapitre sont dans les listes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4563">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="999c8-4564">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4564">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4565">Placez le curseur au début du chapitre, identifié par le handle de chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4565">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="999c8-4566">Notez que lorsque le descripteur de chapitre est DB \_ null \_ HCHAPTER, le chapitre correspondant est l’ensemble de lignes principal de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4566">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="999c8-4567">Si cette étape échoue pour une raison quelconque, le serveur doit signaler une erreur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4567">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="999c8-4568">Répondez au client avec un message CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4568">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="999c8-4569">3.1.5.2.13 recevant une demande CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4569">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="999c8-4570">Lorsque le serveur reçoit une demande de message CPMFreeCursorIn du client, le serveur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4570">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4571">Vérifiez si une requête est associée au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4571">Check if the client has a query associated with it.</span></span> <span data-ttu-id="999c8-4572">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur de paramètre non valide \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="999c8-4572">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="999c8-4573">Vérifiez si le handle de curseur réussi figure dans la liste des poignées de curseur du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4573">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="999c8-4574">Si ce n’est pas le cas, le serveur doit signaler une \_ erreur E Fail (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="999c8-4574">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="999c8-4575">Libérer le curseur et les ressources associées (voir la section 3.1.1 pour obtenir la liste complète) pour ce handle de curseur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4575">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="999c8-4576">Supprimez le curseur de la liste des curseurs pour ce client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4576">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="999c8-4577">Répondez avec un message CPMFreeCursorOut, en définissant le \_ champ cCursorsRemaining avec le nombre de curseurs restants.</span><span class="sxs-lookup"><span data-stu-id="999c8-4577">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="999c8-4578">dans la liste de ce client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4578">in this client's list.</span></span>
-   <span data-ttu-id="999c8-4579">S’il n’y a plus de curseurs pour ce client, le serveur doit libérer la requête et les ressources associées (voir la section 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="999c8-4579">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="999c8-4580">3.1.5.2.14 recevant une demande CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="999c8-4580">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="999c8-4581">Lorsque le serveur reçoit une demande de message CPMDisconnect du client, le serveur doit supprimer le client de la liste des clients connectés et libérer toutes les ressources associées au client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4581">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="999c8-4582">Événements de minuterie 3.1.6</span><span class="sxs-lookup"><span data-stu-id="999c8-4582">3.1.6 Timer Events</span></span>

<span data-ttu-id="999c8-4583">Aucun.</span><span class="sxs-lookup"><span data-stu-id="999c8-4583">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="999c8-4584">3.1.7 autres événements locaux</span><span class="sxs-lookup"><span data-stu-id="999c8-4584">3.1.7 Other Local Events</span></span>

<span data-ttu-id="999c8-4585">Quand le serveur est arrêté, il doit d’abord passer à l’état « arrêt ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4585">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="999c8-4586">Il doit ensuite arrêter d’écouter le canal, effectuer d’autres tâches d’arrêt spécifiques à l’implémentation, puis passer à l’état « arrêté ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4586">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="999c8-4587">Détails du client 3,2</span><span class="sxs-lookup"><span data-stu-id="999c8-4587">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="999c8-4588">3.2.1 modèle de données abstraites</span><span class="sxs-lookup"><span data-stu-id="999c8-4588">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="999c8-4589">La section suivante spécifie les données et l’état géré par le client du protocole du service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-4589">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="999c8-4590">Les données fournies sont pour faciliter l’explication du comportement du protocole.</span><span class="sxs-lookup"><span data-stu-id="999c8-4590">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="999c8-4591">Cette section ne stipule pas que les implémentations adhèrent à ce modèle tant que leur comportement externe est cohérent avec celui décrit dans ce document.</span><span class="sxs-lookup"><span data-stu-id="999c8-4591">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="999c8-4592">Un client a l’État abstrait suivant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4592">A client has the following abstract state:</span></span>

-   <span data-ttu-id="999c8-4593">**Dernier message envoyé**: copie du dernier message envoyé au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4593">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="999c8-4594">**Valeur de propriété actuelle**: valeur partielle d’une propriété « différée », qui est en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="999c8-4594">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="999c8-4595">**Octets actuels reçus**: nombre d’octets reçus pour la valeur de propriété actuelle jusqu’à présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-4595">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="999c8-4596">**État de la connexion de canal nommé**: une connexion au serveur</span><span class="sxs-lookup"><span data-stu-id="999c8-4596">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="999c8-4597">les minuteurs 3.2.2</span><span class="sxs-lookup"><span data-stu-id="999c8-4597">3.2.2 Timers</span></span>

<span data-ttu-id="999c8-4598">Aucun minuteur de protocole n’est requis.</span><span class="sxs-lookup"><span data-stu-id="999c8-4598">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="999c8-4599">3.2.3 initialisation</span><span class="sxs-lookup"><span data-stu-id="999c8-4599">3.2.3 Initialization</span></span>

<span data-ttu-id="999c8-4600">Aucune action n’est effectuée tant qu’une demande de couche supérieure n’a pas été reçue.</span><span class="sxs-lookup"><span data-stu-id="999c8-4600">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="999c8-4601">3.2.4 Higher-Layer événements déclenchés</span><span class="sxs-lookup"><span data-stu-id="999c8-4601">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="999c8-4602">Lorsqu’une demande est reçue à partir d’une couche supérieure, le client doit créer une connexion de canal nommé au serveur, à l’aide des détails spécifiés dans la section 2,1.</span><span class="sxs-lookup"><span data-stu-id="999c8-4602">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="999c8-4603">Si ce n’est pas le cas, la demande de couche supérieure doit être en échec.</span><span class="sxs-lookup"><span data-stu-id="999c8-4603">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="999c8-4604">Autrement dit, en cas de défaillance de la connexion, il incombe au niveau supérieur de réessayer si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="999c8-4604">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="999c8-4605">Un en-tête doit être préalablement associé à des champs définis comme indiqué dans la section 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="999c8-4605">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="999c8-4606">Pour les messages spécifiés comme nécessitant une somme de contrôle différente de zéro, la \_ valeur ULCHECKSUM doit être calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4606">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="999c8-4607">Le contenu du message après que le \_ champ ulReserved2 de l’en-tête de message doit être interprété comme une séquence d’entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-4607">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="999c8-4608">Le client doit calculer la somme des valeurs numériques fournies par ces entiers.</span><span class="sxs-lookup"><span data-stu-id="999c8-4608">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="999c8-4609">Calcule l’opération de bits XOR de cette valeur avec 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="999c8-4609">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="999c8-4610">Soustrait la valeur donnée par \_ MSG de la valeur qui résulte de l’opération de bits XOR.</span><span class="sxs-lookup"><span data-stu-id="999c8-4610">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="999c8-4611">Gestion du catalogue du service d’indexation à distance 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="999c8-4611">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="999c8-4612">Chaque message est déclenché par une demande de la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4612">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="999c8-4613">Aucune séquence de message n’est appliquée par le client pour les demandes de message CISP pour la gestion à distance des catalogues, mais (à l’exception d’un message CPMSetCatStateIn) le serveur répondra uniquement avec succès si le client s’est connecté précédemment au moyen d’un message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4613">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="999c8-4614">3.2.4.1.1 envoyant une demande CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4614">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="999c8-4615">En règle générale, la couche supérieure demande au client de protocole d’envoyer un message CPMCiStateInOut lorsqu’il a besoin d’informations sur les services d’indexation sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4615">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="999c8-4616">Lorsque vous demandez à envoyer ce message, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4616">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4617">Envoyez un message CPMCiStateInOut tel que spécifié dans la section 2.2.3.1 au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4617">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="999c8-4618">Attendez de recevoir le message CPMCiStateInOut du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-4618">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="999c8-4619">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, la structure d’information pour revenir à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4619">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="999c8-4620">3.2.4.1.2 envoyant une demande CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4620">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="999c8-4621">En règle générale, la couche supérieure demande au client de protocole d’envoyer un message CPMSetCatStateIn lorsqu’il a besoin d’informations sur un catalogue ou sur tous les catalogues.</span><span class="sxs-lookup"><span data-stu-id="999c8-4621">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="999c8-4622">Pour ce message, la couche supérieure doit fournir au client de protocole une valeur pour \_ dwNewState et, si nécessaire, le nom du catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-4622">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="999c8-4623">Lorsque vous demandez à envoyer ce message, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4623">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4624">Envoi d’un message CPMSetCatStateIn tel que spécifié dans 2.2.3.2 au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4624">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="999c8-4625">Attendez de recevoir un message CPMSetCatStateOut du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-4625">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="999c8-4626">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, \_ redwOldState à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4626">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="999c8-4627">3.2.4.1.3 envoyant une demande CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4627">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="999c8-4628">En général, la couche supérieure demande à envoyer ce message lorsqu’il doit mettre à jour des documents dans un chemin d’accès existant ou ajouter un nouveau chemin d’accès de fichier à l’index.</span><span class="sxs-lookup"><span data-stu-id="999c8-4628">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="999c8-4629">La couche supérieure est donc de fournir le chemin d’accès et le type d’une analyse, qui est spécifiée comme dans la section 2.2.3.4 où une mise à jour incrémentielle ou complète est destinée à des chemins d’accès existants, et l’initialisation de nouvelles est destinée aux nouveaux chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="999c8-4629">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="999c8-4630">Pour répondre à la demande de couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4630">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4631">Envoyez un message CPMUpdateDocumentsIn tel que spécifié dans la section 2.2.3.4 au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4631">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="999c8-4632">Attendez de recevoir le message CPMUpdateDocumentsIn du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-4632">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="999c8-4633">Signalez la valeur du \_ champ d’état de la réponse à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4633">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="999c8-4634">3.2.4.1.4 envoyant une demande CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4634">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="999c8-4635">En règle générale, la couche supérieure demande à envoyer ce message lorsqu’il est nécessaire d’améliorer les performances des requêtes ou qu’elle fait partie de la maintenance planifiée du service d’indexation.</span><span class="sxs-lookup"><span data-stu-id="999c8-4635">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="999c8-4636">Afin de servir la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4636">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4637">Envoie le message CPMForceMergeIn tel que spécifié par la section 2.2.3.5 au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4637">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="999c8-4638">Attente de réception d’un message CPMUpdateDocumentsIn à partir du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-4638">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="999c8-4639">Signalez la valeur du \_ champ d’état de la réponse à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4639">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="999c8-4640">Messages de requête du catalogue du service d’indexation à distance 3.2.4.2</span><span class="sxs-lookup"><span data-stu-id="999c8-4640">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="999c8-4641">À l’exception de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, il existe une relation un-à-un entre les messages CISP et les demandes de couche supérieures.</span><span class="sxs-lookup"><span data-stu-id="999c8-4641">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="999c8-4642">Pour les deux exceptions mentionnées ci-dessus, il peut y avoir plusieurs messages générés par le client pour répondre aux exigences de taille, ou pour récupérer une propriété complète.</span><span class="sxs-lookup"><span data-stu-id="999c8-4642">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="999c8-4643">La couche supérieure effectue généralement le suivi de toutes les informations spécifiques à la requête (telles que les handles de curseur ouverts, les valeurs autorisées pour les descripteurs de signet et de chapitre, les valeurs wid pour les valeurs de propriété différées, etc.) et effectue également le suivi si le client est dans un état connecté, mais cela n’est pas appliqué par le client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4643">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="999c8-4644">À des fins d’illustration, la partie cliente du diagramme de la section 3 illustre cette séquence pour une requête de service d’indexation simple.</span><span class="sxs-lookup"><span data-stu-id="999c8-4644">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="999c8-4645">3.2.4.2.1 envoyant une demande CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4645">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="999c8-4646">Ce message est généralement la toute première requête de la couche supérieure (comme si le client n’est pas connecté, le serveur échouera la plupart des messages avec l’exception de CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="999c8-4646">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="999c8-4647">Le niveau supérieur fournit au client de protocole les informations nécessaires pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="999c8-4647">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="999c8-4648">Afin de servir la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4648">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4649">Renseignez le message à l’aide des informations fournies par le client de couche supérieure (voir la section 2.2.3.6) dans \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 et aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4649">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="999c8-4650">Définissez \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet et cExtPropSet comme spécifié dans 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="999c8-4650">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="999c8-4651">Définissez la somme de contrôle dans le \_ champ ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="999c8-4651">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="999c8-4652">Envoyez le message CPMConnectIn au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4652">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="999c8-4653">Attente de réception d’un message CPMConnectOut à partir du serveur, en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-4653">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="999c8-4654">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, \_ restaurez la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4654">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="999c8-4655">À des fins d’information, il est prévu que les couches supérieures effectuent généralement les actions suivantes lors de la connexion réussie, mais elles ne sont pas appliquées par le client CISP :</span><span class="sxs-lookup"><span data-stu-id="999c8-4655">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="999c8-4656">Utiliser les messages de gestion du catalogue du service d’indexation à distance pour les tâches d’administration</span><span class="sxs-lookup"><span data-stu-id="999c8-4656">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="999c8-4657">Utilisez une demande CPMCreateQueryIn pour créer une requête de recherche dans le but de récupérer les résultats du catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-4657">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="999c8-4658">3.2.4.2.2 envoyant une demande CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4658">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="999c8-4659">La couche supérieure fournit généralement des informations pour la création de la requête une fois que le client de protocole est connecté.</span><span class="sxs-lookup"><span data-stu-id="999c8-4659">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="999c8-4660">La couche supérieure fournit au client un ensemble de restrictions, un jeu de colonnes, des règles d’ordre de tri et un ensemble de catégorisation (chacune d’elles peut être omise), des propriétés d’ensemble de lignes et la structure du mappeur d’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="999c8-4660">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="999c8-4661">Lorsque cette demande est reçue à partir d’une couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4661">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4662">Préparez un CPMCreateQueryOut comme suit.</span><span class="sxs-lookup"><span data-stu-id="999c8-4662">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="999c8-4663">Si un jeu de colonnes est présent, définissez CColumnsSetPreset sur 0x01 et remplissez le champ ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4663">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="999c8-4664">Si des restrictions sont présentes, définissez CRestrictionPresent sur 0x01 et remplissez le champ restriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-4664">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="999c8-4665">Si un ensemble de tris est présent, renseignez le champ SortSet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4665">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="999c8-4666">Si un ensemble de catégorisations est présent, définissez CSortSetPresent sur 0x01 et remplissez le champ CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4666">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="999c8-4667">Définir le reste des champs comme indiqué dans 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="999c8-4667">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="999c8-4668">Calculez \_ le champ ulCheckSum dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4668">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="999c8-4669">Envoyez le message CPMCreateQueryIn au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4669">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="999c8-4670">Attendez de recevoir le message CPMCreateQueryOut (voir les détails dans la section 3.2.5.1.1), en ignorant silencieusement tous les autres messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-4670">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="999c8-4671">Signalez la valeur du \_ champ d’état de la réponse et, si elle a réussi, le tableau de handles de curseur et les valeurs booléennes informatifs (comme spécifié dans 2.2.3.9) à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4671">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="999c8-4672">3.2.4.2.3 envoyant une demande CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4672">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="999c8-4673">En règle générale, la couche supérieure définit des liaisons pour chaque colonne à retourner dans les lignes lorsqu’elle a déjà un handle de curseur valide (après avoir reçu avec succès CPMCreateQueryOut, consultez la section 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="999c8-4673">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="999c8-4674">Le plus élevé est supposé fournir un tableau de structures CTableColumn, comme indiqué dans la section 2.2.4.31, pour le champ aColumns et un handle de curseur valide.</span><span class="sxs-lookup"><span data-stu-id="999c8-4674">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="999c8-4675">Lorsque cette demande est reçue de la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4675">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4676">Calculez le nombre de structures CTableColumn dans le tableau aColumns et définissez le champ cColumns sur cette valeur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4676">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="999c8-4677">Calculez la taille totale en octets des champs cColumns et aColumns, puis affectez la \_ valeur au champ cbBindingDesc.</span><span class="sxs-lookup"><span data-stu-id="999c8-4677">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="999c8-4678">Définissez les champs spécifiés dans le message CPMSetBindingsIn sur les valeurs fournies par la couche d’application supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4678">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="999c8-4679">Définissez le \_ champ ulChecksum sur la valeur calculée comme indiqué dans la section 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="999c8-4679">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="999c8-4680">Envoyez le message CPMSetBindignsIn terminé au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4680">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="999c8-4681">Attendez de recevoir un message CPMSetBindingsIn du serveur, en ignorant les autres messages.</span><span class="sxs-lookup"><span data-stu-id="999c8-4681">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="999c8-4682">Indiquez l’état du \_ champ État de la réponse à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4682">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="999c8-4683">À des fins d’information, il est prévu que les couches supérieures demandent généralement à un client d’envoyer un message CPMGetRowsIn, mais cela n’est pas appliqué par le protocole de service d’indexation de contenu.</span><span class="sxs-lookup"><span data-stu-id="999c8-4683">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="999c8-4684">3.2.4.2.4 envoyant une demande CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4684">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="999c8-4685">Lorsque la couche supérieure est sur le point de recevoir des informations sur les lignes, elle fournit au client de protocole un pointeur et un handle de chapitre valides et donne une description de recherche appropriée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4685">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="999c8-4686">En règle générale, une couche supérieure est censée le faire lorsqu’elle a un handle de curseur et/ou de chapitre valide et que les liaisons ont été définies avec un message CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4686">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="999c8-4687">Pour accéder à l’ensemble de lignes dans un chapitre, la couche supérieure est d’utiliser le descripteur de chapitre reçu du serveur dans un message CPMGetRowsOut précédent.</span><span class="sxs-lookup"><span data-stu-id="999c8-4687">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="999c8-4688">Lorsque cette demande est reçue de la couche supérieure, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4688">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4689">Déterminez la valeur de l’entier non signé à spécifier pour le \_ champ cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4689">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="999c8-4690">Pour déterminer cette valeur, le client doit prendre la valeur maximale de ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4690">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="999c8-4691">1000 fois la valeur du champ c \_ RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="999c8-4691">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="999c8-4692">Valeur de \_ cbRowWidth, arrondie au multiple de 512 octets le plus proche.</span><span class="sxs-lookup"><span data-stu-id="999c8-4692">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="999c8-4693">Prenez la valeur la plus élevée de ces deux valeurs, jusqu’à la limite de 16 Ko.</span><span class="sxs-lookup"><span data-stu-id="999c8-4693">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="999c8-4694">Dans les cas où une seule ligne est supérieure à 16 Ko, le serveur ne peut pas retourner les résultats de cette requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4694">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="999c8-4695">Spécifiez une base de client pour les données de ligne de taille variable dans l’espace d’adressage du client dans le \_ champ ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="999c8-4695">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="999c8-4696">*Comportement de Windows : pour un client 32 bits communiquant avec un serveur 32 bits, ou un client 64 bits parlant à un serveur 64 bits, cette valeur est définie sur une adresse mémoire de la mémoire tampon de réception dans le processus d’application. Cela permet aux pointeurs, qui sont reçus dans le champ de lignes de CPMGetRowsOut d’être des pointeurs de mémoire corrects dans un processus d’application cliente. Sinon, la valeur est 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="999c8-4696">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="999c8-4697">Calculez la taille de la description de la recherche et définissez-la dans le \_ champ cbSeek.</span><span class="sxs-lookup"><span data-stu-id="999c8-4697">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="999c8-4698">Définissez la valeur de cbReserved (qui ferait office de décalage pour les lignes de début) à la valeur de \_ cbSeek plus 0x14.</span><span class="sxs-lookup"><span data-stu-id="999c8-4698">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="999c8-4699">Envoi d’un message CPMConnectIn tel que spécifié dans 2.2.3.15 au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4699">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="999c8-4700">3.2.4.2.5 envoyant une demande CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4700">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="999c8-4701">Si le client reçoit une réponse CPMGetRowsOut du serveur avec le champ d’état de la colonne défini sur StatusDeferred (0x01), cela signifie que la valeur de propriété n’a pas été incluse dans le champ Rows du message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4701">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="999c8-4702">Dans ce cas, la couche supérieure demande généralement au client de protocole de récupérer la valeur au moyen du message CPMFetchValueIn et fournit la valeur PropSpec et \_ wid pour une propriété différée, que le client de protocole doit utiliser dans le premier message CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4702">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="999c8-4703">S’il s’agit du premier message CPMFetchValueIn que le client a envoyé pour demander la propriété spécifiée, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4703">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4704">Définissez tous les champs d’un message comme indiqué dans la section 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="999c8-4704">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="999c8-4705">Affectez \_ à cbSoFar la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4705">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="999c8-4706">Définir les octets actuels reçus à 0.</span><span class="sxs-lookup"><span data-stu-id="999c8-4706">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="999c8-4707">Envoyez le message CPMFetchValueIn au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4707">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="999c8-4708">3.2.4.2.6 envoyant une demande CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="999c8-4708">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="999c8-4709">Une fois que le niveau supérieur n’utilise plus la requête de recherche, il peut libérer les ressources sur le serveur en demandant au client d’envoyer un message CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4709">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="999c8-4710">Lorsque cette demande est reçue, le client doit envoyer un message CPMFreeCursorIn tel que spécifié dans 2.2.3.28 au serveur, contenant le descripteur spécifié par la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4710">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="999c8-4711">3.2.4.2.7 envoi d’un message CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="999c8-4711">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="999c8-4712">Si la couche supérieure n’a plus de requêtes pour le service d’indexation, pour libérer davantage de ressources serveur, l’application peut demander que le client envoie un message CPMDisconnect au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4712">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="999c8-4713">Lorsque cette requête est reçue, le client doit simplement envoyer le message comme demandé.</span><span class="sxs-lookup"><span data-stu-id="999c8-4713">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="999c8-4714">Il n’y a aucune réponse à ce message à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4714">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="999c8-4715">3.2.5 traitement des messages et règles de séquencement</span><span class="sxs-lookup"><span data-stu-id="999c8-4715">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="999c8-4716">Lorsque le client reçoit une réponse de message du serveur, le client doit utiliser le dernier message envoyé pour déterminer si le message reçu du serveur est celui attendu par le client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4716">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="999c8-4717">Tous les messages dont \_ le champ MSG est différent de celui du dernier message d’envoi doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4717">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="999c8-4718">3.2.5.1 recevant une réponse CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4718">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="999c8-4719">Lorsque le client reçoit une réponse de message CPMCreateQueryOut du serveur, le client doit renvoyer l' \_ État et (si l’État est réussi) les valeurs de handle de curseur sont retournées à une couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4719">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="999c8-4720">Toutes les actions supplémentaires sont effectuées jusqu’à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4720">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="999c8-4721">Comme la couche supérieure est consciente de la structure de la requête, elle devrait toujours s’attendre à ce que le nombre de handles de curseur soit renvoyé dans le message CPMCreateOueryOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4721">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="999c8-4722">Les handles de curseur sont retournés dans l’ordre suivant : le premier descripteur est l’ensemble de lignes non chapitre, le second est le premier ensemble de lignes chapitre (qui est le regroupement de résultats en fonction de la première catégorie spécifiée dans le champ CategorizationSet du message CPMCreateQueryIn.)</span><span class="sxs-lookup"><span data-stu-id="999c8-4722">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="999c8-4723">À des fins d’information, il est prévu que les couches supérieures puissent effectuer les actions suivantes, mais elles ne sont pas appliquées par le client CISP :</span><span class="sxs-lookup"><span data-stu-id="999c8-4723">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="999c8-4724">Utilisez CPMSetBindingsIn pour définir des liaisons pour des colonnes individuelles et effectuer toutes les actions suivantes sur le chemin d’accès de la requête</span><span class="sxs-lookup"><span data-stu-id="999c8-4724">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="999c8-4725">Utilisez CPMGetQueryStatusIn pour vérifier la progression de l’exécution d’une requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4725">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="999c8-4726">Utilisez CPMRatioFinishedIn pour demander le pourcentage d’achèvement de la requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4726">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="999c8-4727">3.2.5.2 recevant une réponse CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4727">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="999c8-4728">Lorsque le client reçoit une réponse de message CPMGetRowsOut du serveur, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4728">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4729">Vérifiez si le \_ champ d’État dans l’en-tête indique réussite ou échec.</span><span class="sxs-lookup"><span data-stu-id="999c8-4729">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="999c8-4730">Si la \_ valeur d’État est mémoire tampon d’État insuffisante \_ \_ \_ (0xC0000023), le client doit vérifier l’état du dernier message envoyé.</span><span class="sxs-lookup"><span data-stu-id="999c8-4730">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="999c8-4731">S’il ne contient pas de message CPMGetRowsIn, le message reçu doit être ignoré en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="999c8-4731">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="999c8-4732">Dans le cas contraire, le client doit envoyer au serveur un nouveau message CPMGetRowsIn avec tous les champs identiques à ceux qui sont stockés, sauf que le \_ CBREADBUFFER doit être augmenté de 512 (mais pas supérieur à 0x4000).</span><span class="sxs-lookup"><span data-stu-id="999c8-4732">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="999c8-4733">Si \_ l’État est \_ \_ trop \_ petit pour le tampon d’État (0xC0000023) et que le dernier message envoyé a déjà un \_ CBREADBUFFER égal au client 0x4000 doit signaler l’erreur au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4733">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="999c8-4734">Si la \_ valeur d’État est une autre valeur d’erreur, le client doit indiquer l’échec jusqu’à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4734">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="999c8-4735">Si la \_ valeur d’État indique une réussite, les résultats doivent être indiqués jusqu’à la couche supérieure demandant les informations, et d’autres actions sont effectuées sur la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4735">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="999c8-4736">À des fins d’information, il est prévu que les couches supérieures effectuent généralement les actions suivantes, mais elles ne sont pas appliquées par le client du protocole du service d’indexation de contenu :</span><span class="sxs-lookup"><span data-stu-id="999c8-4736">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="999c8-4737">Si les valeurs des lignes représentent les ID de document, les poignées de chapitre ou de signet, la couche supérieure les stocke en général pour une utilisation dans des opérations ultérieures qui impliquent des ID de document, des handles de chapitre ou de signet valides.</span><span class="sxs-lookup"><span data-stu-id="999c8-4737">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="999c8-4738">En général, la couche supérieure stocke ou affiche ou utilise les données des valeurs de ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-4738">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="999c8-4739">Pour les valeurs qui ont été marquées comme couches supérieures différées, la valeur est extraite à l’aide de messages CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4739">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="999c8-4740">La description de la recherche est également retournée à la couche supérieure et peut être réutilisée ou examinée par la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4740">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="999c8-4741">À des fins d’information, si la couche supérieure a demandé des descripteurs aux chapitres et aux signets qui ont été reçus dans les lignes, elle peut effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4741">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="999c8-4742">Utilisez CPMGetQueryStatusExIn pour vérifier la progression de l’exécution d’une requête, ainsi que des informations d’État supplémentaires, telles que le nombre de documents filtrés, les documents restants à filtrer, le rapport entre les documents traités par la requête, le nombre total de lignes dans la requête et la position du signet dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4742">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="999c8-4743">Utilisez CPMGetNotify pour demander que le serveur informe le client des modifications de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4743">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="999c8-4744">Utilisez CPMGetApproximatePositionIn pour demander la position approximative d’un signet dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4744">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="999c8-4745">Utilisez CPMCompareBmkIn pour demander une comparaison de deux signets dans un chapitre.</span><span class="sxs-lookup"><span data-stu-id="999c8-4745">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="999c8-4746">Utilisez CPMRestartPositionIn pour que le serveur modifie l’emplacement du curseur au début de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4746">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="999c8-4747">3.2.5.3 recevant une réponse CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4747">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="999c8-4748">Lorsque le client reçoit une réponse de message CPMGetRowsOut du serveur, le client doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4748">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="999c8-4749">Vérifiez si le \_ champ d’État dans l’en-tête indique réussite ou échec.</span><span class="sxs-lookup"><span data-stu-id="999c8-4749">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="999c8-4750">En cas d’échec, notifiez la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4750">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="999c8-4751">Dans le cas contraire, continuez ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="999c8-4751">Otherwise, continue below.</span></span>
-   <span data-ttu-id="999c8-4752">Vérifiez \_ fValueExist et, s’il a la valeur 0x00000000, informez la couche supérieure que la valeur est introuvable.</span><span class="sxs-lookup"><span data-stu-id="999c8-4752">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="999c8-4753">Sinon, ajoutez \_ cbValue octets de vValue à la valeur de propriété actuelle.</span><span class="sxs-lookup"><span data-stu-id="999c8-4753">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="999c8-4754">Si \_ \_ fMoreExists a la valeur 0x00000001, incrémentez \_ les octets actuels reçus par \_ cbValue et envoyez un message CPMFetchValueIn au serveur, en définissant \_ CbSoFar sur la valeur des octets actuels reçus, \_ cbPropSpec sur zéro et \_ cbChunk sur la taille de la mémoire tampon souhaitée par la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4754">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="999c8-4755">Si \_ fMoreExists a la valeur 0x00000000, indiquez la valeur de propriété de la valeur de propriété actuelle à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4755">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="999c8-4756">3.2.5.4 recevant une réponse CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="999c8-4756">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="999c8-4757">Lorsque le client reçoit une réponse de message CPMFreeCursorOut réussie du serveur, le client doit renvoyer la \_ valeur cCursorsRemaining à la couche supérieure.</span><span class="sxs-lookup"><span data-stu-id="999c8-4757">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="999c8-4758">Les informations suivantes sont fournies à des fins d’information uniquement et ne sont pas appliquées par le client CISP.</span><span class="sxs-lookup"><span data-stu-id="999c8-4758">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="999c8-4759">La couche supérieure est supposée effectuer le suivi des poignées de curseur et ne pas utiliser celles qui ont déjà été libérées.</span><span class="sxs-lookup"><span data-stu-id="999c8-4759">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="999c8-4760">Une fois que le nombre de \_ cCursorsRemaining est égal à 0x00000000, la couche supérieure peut utiliser la connexion pour spécifier une autre requête (à l’aide d’un message CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="999c8-4760">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="999c8-4761">Événements de minuterie 3.2.6</span><span class="sxs-lookup"><span data-stu-id="999c8-4761">3.2.6 Timer Events</span></span>

<span data-ttu-id="999c8-4762">Aucun.</span><span class="sxs-lookup"><span data-stu-id="999c8-4762">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="999c8-4763">3.2.7 autres événements locaux</span><span class="sxs-lookup"><span data-stu-id="999c8-4763">3.2.7 Other Local Events</span></span>

<span data-ttu-id="999c8-4764">Aucun.</span><span class="sxs-lookup"><span data-stu-id="999c8-4764">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="999c8-4765">4 Exemples de protocoles</span><span class="sxs-lookup"><span data-stu-id="999c8-4765">4 Protocol Examples</span></span>

-   [<span data-ttu-id="999c8-4766">4,1 exemple 1</span><span class="sxs-lookup"><span data-stu-id="999c8-4766">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="999c8-4767">4,2 exemple 2</span><span class="sxs-lookup"><span data-stu-id="999c8-4767">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="999c8-4768">4,1 exemple 1</span><span class="sxs-lookup"><span data-stu-id="999c8-4768">4.1 Example 1</span></span>

<span data-ttu-id="999c8-4769">Dans l’exemple suivant, nous considérons un scénario dans lequel l’utilisateur JOHN sur l’ordinateur A souhaite obtenir la taille des fichiers qui contiennent le mot « Microsoft » à partir de l’ensemble de documents stockés sur le serveur X dans le système de catalogue.</span><span class="sxs-lookup"><span data-stu-id="999c8-4769">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="999c8-4770">Supposons que l’ordinateur A exécute un système d’exploitation Windows XP 32 bits et que l’ordinateur X exécute un système d’exploitation Windows Server 2003 32 bits.</span><span class="sxs-lookup"><span data-stu-id="999c8-4770">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="999c8-4771">L’utilisateur lance une application de recherche et entre dans la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="999c8-4771">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="999c8-4772">L’application transmet à son tour la requête de recherche au client du protocole.</span><span class="sxs-lookup"><span data-stu-id="999c8-4772">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="999c8-4773">Le client de protocole établit une connexion avec le serveur d’indexation X. Le client de protocole utilise le \\ canal de canal nommé \\ ci \_ SKADS pour se connecter au serveur X sur SMB.</span><span class="sxs-lookup"><span data-stu-id="999c8-4773">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="999c8-4774">Le client de protocole prépare ensuite un message CPMConnectIn avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4774">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="999c8-4775">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4775">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4776">**\_ MSG** a la valeur 0x000000C8, ce qui indique qu’il s’agit d’un message CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4776">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="999c8-4777">l' **\_ État** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4777">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="999c8-4778">**\_ ulChecksum** contient la somme de contrôle, calculée comme indiqué dans la section 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="999c8-4778">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="999c8-4779">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4779">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="999c8-4780">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4780">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4781">**\_ iClientVersion** est défini sur 0x00000008, ce qui indique que le serveur doit valider le champ de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="999c8-4781">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="999c8-4782">**\_ fClientIsRemote** a la valeur 0x00000001, ce qui indique que le serveur est un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="999c8-4782">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="999c8-4783">**\_ cbBlob1** est défini sur la taille, en octets, des champs cPropSet, PropertySet1 et PropertySet2 combinés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4783">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="999c8-4784">**\_ cbBlob2** a la valeur 0x00000004 (ce qui signifie qu’il n’y a pas de jeux de propriétés supplémentaires).</span><span class="sxs-lookup"><span data-stu-id="999c8-4784">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="999c8-4785">**MachineName** a pour valeur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4785">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="999c8-4786">Le **nom d’utilisateur** est défini sur John.</span><span class="sxs-lookup"><span data-stu-id="999c8-4786">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="999c8-4787">**cPropSets** a la valeur 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="999c8-4787">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="999c8-4788">Le champ **PropertySet1** est de type CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4788">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="999c8-4789">La structure CDbPropSet comprenant le champ PropertySet1 est remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4789">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="999c8-4790">Le champ **GuidPropSet** est défini sur A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ ext).</span><span class="sxs-lookup"><span data-stu-id="999c8-4790">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="999c8-4791">le champ **cProperties** est défini sur 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="999c8-4791">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="999c8-4792">le champ **aProps** est un tableau de structures CDbProp.</span><span class="sxs-lookup"><span data-stu-id="999c8-4792">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="999c8-4793">Pour l' **élément \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4793">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="999c8-4794">**PropId** a la valeur 0X00000002 (DBPROP \_ ci \_ nom du catalogue \_ ).</span><span class="sxs-lookup"><span data-stu-id="999c8-4794">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="999c8-4795">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4795">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="999c8-4796">**DBPROPSTATUS** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4796">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4797">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4797">For the **ColId** element:</span></span>
                -   <span data-ttu-id="999c8-4798">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid)</span><span class="sxs-lookup"><span data-stu-id="999c8-4798">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="999c8-4799">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-4799">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="999c8-4800">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4800">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4801">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4801">For the **vValue** element:</span></span>
                -   <span data-ttu-id="999c8-4802">**vType** est défini sur 0X001F (VT \_ LPWStr).</span><span class="sxs-lookup"><span data-stu-id="999c8-4802">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="999c8-4803">**vValue** est défini sur « System », le nom du catalogue souhaité.</span><span class="sxs-lookup"><span data-stu-id="999c8-4803">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="999c8-4804">Pour l' **élément \[ aProps \] 1** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4804">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="999c8-4805">**PropId** est défini sur 0x00000007 ( \_ type de \_ requête DBPROP ci \_ )</span><span class="sxs-lookup"><span data-stu-id="999c8-4805">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="999c8-4806">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4806">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="999c8-4807">**DBPROPSTATUS** est défini sur to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4807">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4808">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4808">For the **ColId** element:</span></span>
                -   <span data-ttu-id="999c8-4809">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="999c8-4809">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="999c8-4810">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-4810">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="999c8-4811">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4811">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4812">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4812">For the **vValue** element:</span></span>
                -   <span data-ttu-id="999c8-4813">**vType** est défini sur 0X0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="999c8-4813">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="999c8-4814">**vValue** a la valeur 0X00000000 (CiNormal), ce qui signifie qu’il s’agit d’une requête normale.</span><span class="sxs-lookup"><span data-stu-id="999c8-4814">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="999c8-4815">Pour l' **élément \[ aProps \] 2** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4815">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="999c8-4816">**PropId** a la valeur 0x00000004 (indicateurs d’étendue d’DBPROP \_ ci \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="999c8-4816">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="999c8-4817">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4817">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="999c8-4818">**DBPROPSTATUS** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4818">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4819">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4819">For the **ColId** element:</span></span>
                -   <span data-ttu-id="999c8-4820">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="999c8-4820">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="999c8-4821">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-4821">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="999c8-4822">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4822">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4823">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4823">For the **vValue** element:</span></span>
                -   <span data-ttu-id="999c8-4824">**vType**: 0X1003 (VT \_ Vector \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="999c8-4824">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="999c8-4825">**vValue**: 0x00000001/0x00000001 (un élément avec la valeur 1), ce qui signifie que les sous-dossiers de recherche</span><span class="sxs-lookup"><span data-stu-id="999c8-4825">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="999c8-4826">Pour l' **élément \[ aProps \] 3** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4826">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="999c8-4827">**PropId**: 0X00000003 (DBPROP \_ ci \_ include include \_ )</span><span class="sxs-lookup"><span data-stu-id="999c8-4827">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="999c8-4828">**DBPROPOPTIONS**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="999c8-4828">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="999c8-4829">**DBPROPSTATUS**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-4829">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="999c8-4830">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4830">For the **ColId** element:</span></span>
                -   <span data-ttu-id="999c8-4831">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="999c8-4831">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="999c8-4832">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-4832">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="999c8-4833">**ulID** a la valeur 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-4833">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="999c8-4834">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4834">For the **vValue** element:</span></span>
                -   <span data-ttu-id="999c8-4835">**vType** est défini sur 0X101F (VT \_ Vector \| VT \_ LPWStr).</span><span class="sxs-lookup"><span data-stu-id="999c8-4835">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="999c8-4836">**vValue** est défini sur 0x00000001/0x00000002/" \\ " (un élément avec une chaîne de 2 caractères se terminant par un caractère null), ce qui correspond à l’étendue racine.</span><span class="sxs-lookup"><span data-stu-id="999c8-4836">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="999c8-4837">Le champ **PropertySet2** est de type CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4837">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="999c8-4838">La structure CDbPropSet comprenant le champ PropertySet1 est remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4838">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="999c8-4839">**GuidPropSet** est défini sur AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ ext).</span><span class="sxs-lookup"><span data-stu-id="999c8-4839">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="999c8-4840">le champ **cProperties** est défini sur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-4840">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="999c8-4841">Le champ **aProps** est un tableau de structures CDbProp.</span><span class="sxs-lookup"><span data-stu-id="999c8-4841">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="999c8-4842">Pour l' **élément \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4842">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="999c8-4843">**PropId** a la valeur 0X00000002 (DBPROP \_ machine).</span><span class="sxs-lookup"><span data-stu-id="999c8-4843">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="999c8-4844">**DBPROPOPTIONS** est défini sur 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4844">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="999c8-4845">**DBPROPSTATUS** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4845">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4846">Pour l’élément **colid** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4846">For the **ColId** element:</span></span>
                -   <span data-ttu-id="999c8-4847">**eKind** a la valeur 0X00000001 (DBKIND \_ GUID \_ propid),</span><span class="sxs-lookup"><span data-stu-id="999c8-4847">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="999c8-4848">**GUID** est null (tous les zéros), ce qui signifie que la valeur s’applique à la requête, et pas seulement à une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="999c8-4848">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="999c8-4849">**ulID** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4849">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4850">Pour l’élément **vValue** :</span><span class="sxs-lookup"><span data-stu-id="999c8-4850">For **vValue** element:</span></span>
                -   <span data-ttu-id="999c8-4851">**vType**: 0X0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="999c8-4851">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="999c8-4852">**vValue**: 0x04/"x" (4 octets/chaîne Unicode terminée par un caractère null), signifiant "X"-nom d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4852">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="999c8-4853">le champ **cExtPropSet** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4853">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="999c8-4854">le tableau **aPropertySets** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="999c8-4854">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="999c8-4855">Les différents champs de remplissage sont renseignés en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="999c8-4855">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="999c8-4856">Le message est envoyé au serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4856">The message is sent to the server.</span></span>

4.  <span data-ttu-id="999c8-4857">Le serveur vérifie que le **\_ ulChecksum** est correct, vérifie que l’utilisateur est autorisé à effectuer cette demande et répond avec un message CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4857">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="999c8-4858">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4858">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4859">**\_ MSG** a la valeur 0x000000C8, ce qui indique qu’il s’agit d’un message CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4859">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="999c8-4860">l' **\_ État** est défini sur 0X0000000 indiquant la réussite.</span><span class="sxs-lookup"><span data-stu-id="999c8-4860">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="999c8-4861">**\_ ulChecksum** a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="999c8-4861">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="999c8-4862">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4862">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="999c8-4863">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4863">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4864">le champ **\_ ServerVersion** est défini sur 0x00000007 (32 bits windows XP ou 32 bits Windows Server 2003).</span><span class="sxs-lookup"><span data-stu-id="999c8-4864">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="999c8-4865">les champs **\_ réservés** sont remplis avec des données arbitraires.</span><span class="sxs-lookup"><span data-stu-id="999c8-4865">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="999c8-4866">Le client prépare un message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4866">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="999c8-4867">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4867">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4868">**\_ MSG** a la valeur 0x000000CA, ce qui indique qu’il s’agit d’un message CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4868">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="999c8-4869">l' **\_ État** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4869">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="999c8-4870">**\_ ulChecksum** contient la somme de contrôle calculée d’après 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="999c8-4870">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="999c8-4871">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4871">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="999c8-4872">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4872">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4873">Le champ **taille** est défini sur la taille du reste du message.</span><span class="sxs-lookup"><span data-stu-id="999c8-4873">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="999c8-4874">Le champ **CColumnSetPresent** est défini sur 0x01.</span><span class="sxs-lookup"><span data-stu-id="999c8-4874">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="999c8-4875">Le champ **ColumnSet** est de type CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="999c8-4875">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="999c8-4876">La structure CColumnSet comprenant ce champ est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4876">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="999c8-4877">le champ **\_ Count** a la valeur 0x00000001, indiquant qu’une colonne est retournée.</span><span class="sxs-lookup"><span data-stu-id="999c8-4877">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="999c8-4878">le tableau d' **index** est 0x00000000 et indique la première entrée dans \_ aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="999c8-4878">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="999c8-4879">Le champ **CRestrictionPresent** est défini sur 0x01, ce qui indique que le champ de **restriction** est présent.</span><span class="sxs-lookup"><span data-stu-id="999c8-4879">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="999c8-4880">Le champ de **restriction** est de type CRestriction et a la valeur :</span><span class="sxs-lookup"><span data-stu-id="999c8-4880">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="999c8-4881">**\_ ulType** est défini sur 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="999c8-4881">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="999c8-4882">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4882">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="999c8-4883">Le reste du champ contient une structure CContentRestriction :</span><span class="sxs-lookup"><span data-stu-id="999c8-4883">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="999c8-4884">La **\_ propriété** est définie sur GUID B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13 qui représente le corps du document.</span><span class="sxs-lookup"><span data-stu-id="999c8-4884">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="999c8-4885">**\_ CC** est défini sur 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="999c8-4885">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="999c8-4886">**\_ pwcsphrase** est défini sur la chaîne « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4886">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="999c8-4887">**\_ LCID** est défini sur 0x40C (pour l’anglais).</span><span class="sxs-lookup"><span data-stu-id="999c8-4887">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="999c8-4888">**\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).</span><span class="sxs-lookup"><span data-stu-id="999c8-4888">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="999c8-4889">**CSortPresent** est défini sur 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-4889">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="999c8-4890">**CCategorizationSetPresent** est défini sur 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-4890">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="999c8-4891">**RowSetProperties** est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4891">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="999c8-4892">**\_ uBooleanOptions** a la valeur 0x00000001 (Sequential).</span><span class="sxs-lookup"><span data-stu-id="999c8-4892">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="999c8-4893">**\_ ulMaxOpenRows** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4893">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="999c8-4894">**\_ ulMemoryUsage** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4894">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="999c8-4895">\_**cMaxResults** est défini sur 0x00000100 (retourner au maximum 256 lignes).</span><span class="sxs-lookup"><span data-stu-id="999c8-4895">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="999c8-4896">**\_ cCmdTimeOut** a la valeur 0x00000000 (jamais timeout).</span><span class="sxs-lookup"><span data-stu-id="999c8-4896">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="999c8-4897">**PidMapper** a la valeur :</span><span class="sxs-lookup"><span data-stu-id="999c8-4897">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="999c8-4898">**\_ Count** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-4898">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="999c8-4899">**\_ aPropSpec** est défini sur GUID B725F130-47EF-101A-a5-F1-02608C9EEBAC/0X00000001 (pour PRSPEC \_ propid)/0x0000000c qui représente la propriété de taille de fichier Windows.</span><span class="sxs-lookup"><span data-stu-id="999c8-4899">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="999c8-4900">Le serveur le traite et répond avec un message CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4900">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="999c8-4901">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4901">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4902">**\_ MSG** a la valeur 0x000000CA, ce qui indique qu’il s’agit d’un message CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4902">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="999c8-4903">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="999c8-4903">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="999c8-4904">**\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="999c8-4904">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="999c8-4905">**\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="999c8-4905">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="999c8-4906">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4906">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4907">**\_ fTrueSeqeuntial** a la valeur 0x00000000, ce qui indique que la requête peut utiliser un index.</span><span class="sxs-lookup"><span data-stu-id="999c8-4907">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="999c8-4908">**\_ fWorkIdUnique** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-4908">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="999c8-4909">Le tableau **aCursors** contient un seul élément, représentant un handle de curseur pour cette requête.</span><span class="sxs-lookup"><span data-stu-id="999c8-4909">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="999c8-4910">La valeur dépend de l’état du serveur.</span><span class="sxs-lookup"><span data-stu-id="999c8-4910">The value depends on the state of the server.</span></span> <span data-ttu-id="999c8-4911">Supposons que la valeur retournée est 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="999c8-4911">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="999c8-4912">Le client émet un message de demande CPMSetBindingsIn pour définir le format d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="999c8-4912">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="999c8-4913">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4913">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4914">**\_ MSG** a la valeur 0x000000D0, ce qui indique qu’il s’agit d’un message CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4914">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="999c8-4915">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="999c8-4915">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="999c8-4916">**\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="999c8-4916">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="999c8-4917">**\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="999c8-4917">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="999c8-4918">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4918">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4919">**\_ hCursor** est défini sur 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="999c8-4919">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="999c8-4920">**\_ cbRow** est défini sur 0x10 (suffisamment grand pour tenir les colonnes).</span><span class="sxs-lookup"><span data-stu-id="999c8-4920">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="999c8-4921">**\_ cbBindingDesc** est défini sur la taille des champs **\_ CColumns** et **\_ aColumns** combinés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4921">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="999c8-4922">**\_ CColumns** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-4922">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="999c8-4923">le tableau **\_ aColumns** est défini de façon à contenir une structure CTableColumn contenant :</span><span class="sxs-lookup"><span data-stu-id="999c8-4923">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="999c8-4924">**\_ PropSpec** est défini sur GUID b725f130-47EF-101A-a5-F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x0000000c qui représente la propriété de taille de fichier Windows.</span><span class="sxs-lookup"><span data-stu-id="999c8-4924">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="999c8-4925">**\_ vType** est défini sur 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="999c8-4925">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="999c8-4926">**\_ ValueUsed** est défini sur 0x01 (colonne transférée dans la ligne).</span><span class="sxs-lookup"><span data-stu-id="999c8-4926">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="999c8-4927">**\_ ValueOffset** est défini sur 0x0002 (au début de la ligne).</span><span class="sxs-lookup"><span data-stu-id="999c8-4927">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="999c8-4928">**\_ Value** est défini sur 0x08 (taille d’un UI8 VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="999c8-4928">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="999c8-4929">**\_ StatusUsed** est défini sur 0x01.</span><span class="sxs-lookup"><span data-stu-id="999c8-4929">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="999c8-4930">**\_ StatusOffset** est défini sur 0x0A.</span><span class="sxs-lookup"><span data-stu-id="999c8-4930">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="999c8-4931">**\_ LengthUsed** est défini sur 0x00.</span><span class="sxs-lookup"><span data-stu-id="999c8-4931">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="999c8-4932">Le serveur le traite et répond avec un message CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4932">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="999c8-4933">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4933">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4934">**\_ MSG** est défini sur 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="999c8-4934">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="999c8-4935">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="999c8-4935">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="999c8-4936">**\_ ulChecksum** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="999c8-4936">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="999c8-4937">**\_ ulReserved2** a la valeur 0x00000000 (ou toute autre valeur arbitraire).</span><span class="sxs-lookup"><span data-stu-id="999c8-4937">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="999c8-4938">Le client émet un message de demande CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4938">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="999c8-4939">Supposons que le client est prêt à accepter 100 lignes à ce stade et qu’il les souhaite dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="999c8-4939">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="999c8-4940">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4940">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4941">**\_ MSG** a la valeur 0x000000CC, ce qui indique qu’il s’agit d’un message CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="999c8-4941">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="999c8-4942">l' **\_ État** est défini sur 0x00000000</span><span class="sxs-lookup"><span data-stu-id="999c8-4942">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="999c8-4943">**\_ ulChecksum** contient la somme de contrôle calculée en fonction de la section 0.</span><span class="sxs-lookup"><span data-stu-id="999c8-4943">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="999c8-4944">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4944">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="999c8-4945">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4945">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4946">**\_ hCursor** est défini sur 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="999c8-4946">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="999c8-4947">**\_ cRowsToTransfer** est défini sur 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="999c8-4947">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="999c8-4948">**\_ cRowWidth** est défini sur 0x00000010 (à partir des liaisons).</span><span class="sxs-lookup"><span data-stu-id="999c8-4948">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="999c8-4949">**\_ cbSeek** est défini sur 0x14, qui est la taille des champs ETYPE, \_ Chapt et CRowSeekNext combinés.</span><span class="sxs-lookup"><span data-stu-id="999c8-4949">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="999c8-4950">**\_ cbReserved** a la valeur 0x18 (0x14 plus \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="999c8-4950">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="999c8-4951">**\_ cbReadBuffer** est défini sur 0x800 (0x64 \* 0x10 est arrondi au multiple suivant de 0x200).</span><span class="sxs-lookup"><span data-stu-id="999c8-4951">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="999c8-4952">**\_ ulClientBase** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4952">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="999c8-4953">**\_ fBwdfetch** a la valeur 0x00000000, ce qui indique que les lignes doivent être extraites dans l’ordre de transmission.</span><span class="sxs-lookup"><span data-stu-id="999c8-4953">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="999c8-4954">**ETYPE** a la valeur 0x0000001, ce qui indique que le client souhaite les lignes suivantes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4954">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="999c8-4955">**\_ Chapt** a la valeur 0 (pas un résultat chapitre).</span><span class="sxs-lookup"><span data-stu-id="999c8-4955">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="999c8-4956">**SeekDescription** est défini sur CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="999c8-4956">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="999c8-4957">La structure CRowSeekNext contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="999c8-4957">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="999c8-4958">**CiTblChapt** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4958">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="999c8-4959">**\_ hRegion** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4959">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="999c8-4960">**\_ cSkip** a la valeur 0, ce qui indique que le client ne souhaite pas ignorer les lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4960">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="999c8-4961">Le serveur le traite et répond avec un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4961">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="999c8-4962">Supposons que le serveur a trouvé 100 documents qui contiennent le mot « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4962">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="999c8-4963">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4963">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4964">**\_ MSG** a la valeur 0x000000CC, ce qui indique qu’il s’agit d’un message CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="999c8-4964">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="999c8-4965">l' **\_ État** est défini sur succès.</span><span class="sxs-lookup"><span data-stu-id="999c8-4965">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="999c8-4966">**\_ ulChecksum** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4966">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="999c8-4967">**\_ ulReserved2** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4967">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="999c8-4968">Le corps du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4968">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4969">**\_ CRowsReturned** est défini sur 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="999c8-4969">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="999c8-4970">**ETYPE** a la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="999c8-4970">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="999c8-4971">**\_ Chapt** a la valeur 0x00000000 (pas un résultat chapitre).</span><span class="sxs-lookup"><span data-stu-id="999c8-4971">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="999c8-4972">**SeekDescription** contient une structure CRowSeekNext, remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4972">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="999c8-4973">**CiTblChapt** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4973">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="999c8-4974">**\_ hRegion** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4974">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="999c8-4975">**\_ cSkip** a la valeur 0, ce qui indique que le client ne souhaite pas ignorer les lignes.</span><span class="sxs-lookup"><span data-stu-id="999c8-4975">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="999c8-4976">**Lignes** contient la taille des documents 100 qui contiennent le mot « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4976">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="999c8-4977">Étant donné qu’il s’agit de données de taille fixe, elles sont simplement structurées sous la forme d’une liste d’entiers non signés de 100 à 8 octets.</span><span class="sxs-lookup"><span data-stu-id="999c8-4977">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="999c8-4978">Le client envoie un message CPMDisconnect pour mettre fin à la connexion.</span><span class="sxs-lookup"><span data-stu-id="999c8-4978">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="999c8-4979">L’en-tête du message est rempli comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4979">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="999c8-4980">**\_ MSG** a la valeur 0x000000C9, ce qui indique qu’il s’agit d’un message CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="999c8-4980">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="999c8-4981">l' **\_ État** est défini sur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4981">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="999c8-4982">**\_ ulChecksum** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4982">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="999c8-4983">Le serveur traite le message et supprime tous les États du client.</span><span class="sxs-lookup"><span data-stu-id="999c8-4983">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="999c8-4984">4,2 exemple 2</span><span class="sxs-lookup"><span data-stu-id="999c8-4984">4.2 Example 2</span></span>

<span data-ttu-id="999c8-4985">Dans l’exemple précédent, la requête était assez simple.</span><span class="sxs-lookup"><span data-stu-id="999c8-4985">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="999c8-4986">Prenons maintenant une requête légèrement plus complexe.</span><span class="sxs-lookup"><span data-stu-id="999c8-4986">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="999c8-4987">Supposons que l’utilisateur souhaite récupérer la taille des documents qui contiennent les deux mots suivants : « Microsoft » et « Office ».</span><span class="sxs-lookup"><span data-stu-id="999c8-4987">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="999c8-4988">Cela est spécifié en modifiant le champ de restriction contenu dans le message CPMCreateQueryIn envoyé à l’étape 5 comme suit :</span><span class="sxs-lookup"><span data-stu-id="999c8-4988">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="999c8-4989">Le champ de **restriction** est de type CRestriction et a la valeur :</span><span class="sxs-lookup"><span data-stu-id="999c8-4989">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="999c8-4990">**\_ ulType** est défini sur 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="999c8-4990">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="999c8-4991">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4991">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="999c8-4992">Le reste du champ contient une structure CNodeRestriction :</span><span class="sxs-lookup"><span data-stu-id="999c8-4992">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="999c8-4993">**\_ CNode** a la valeur 0x00000002, ce qui indique qu’il existe deux nœuds dans le tableau paNode.</span><span class="sxs-lookup"><span data-stu-id="999c8-4993">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="999c8-4994">Le champ **\_ paNode** est un tableau de deux structures CRestriction.</span><span class="sxs-lookup"><span data-stu-id="999c8-4994">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="999c8-4995">**\_ paNode \[ 0 \]** contient :</span><span class="sxs-lookup"><span data-stu-id="999c8-4995">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="999c8-4996">**\_ ulType** est défini sur 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="999c8-4996">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="999c8-4997">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-4997">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-4998">Le reste du champ contient une structure CContentRestriction :</span><span class="sxs-lookup"><span data-stu-id="999c8-4998">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="999c8-4999">La **\_ propriété** est définie sur GUID b725f130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="999c8-4999">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="999c8-5000">**\_ CC** est défini sur 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="999c8-5000">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="999c8-5001">**\_ pwcsphrase** est défini sur la chaîne « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="999c8-5001">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="999c8-5002">**\_ LCID** est défini sur 0x40C (pour l’anglais).</span><span class="sxs-lookup"><span data-stu-id="999c8-5002">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="999c8-5003">**\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).</span><span class="sxs-lookup"><span data-stu-id="999c8-5003">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="999c8-5004">**\_ paNode \[ 1 \]** contient :</span><span class="sxs-lookup"><span data-stu-id="999c8-5004">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="999c8-5005">**\_ ulType** est défini sur 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="999c8-5005">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="999c8-5006">**\_ Weight** a la valeur 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="999c8-5006">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="999c8-5007">Le reste du champ contient une structure CContentRestriction :</span><span class="sxs-lookup"><span data-stu-id="999c8-5007">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="999c8-5008">La **\_ propriété** est définie sur GUID b725f130-47EF-101A-A5F1-02608c9eebac/0X00000001 (pour PRSPEC \_ propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="999c8-5008">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="999c8-5009">**\_ CC** est défini sur 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="999c8-5009">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="999c8-5010">**\_ pwcsphrase** est défini sur la chaîne « Office ».</span><span class="sxs-lookup"><span data-stu-id="999c8-5010">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="999c8-5011">**\_ LCID** est défini sur 0x40C (pour l’anglais).</span><span class="sxs-lookup"><span data-stu-id="999c8-5011">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="999c8-5012">**\_ ulGenerateMethod** a la valeur 0x00000000 (correspondance exacte).</span><span class="sxs-lookup"><span data-stu-id="999c8-5012">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="999c8-5013">5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="999c8-5013">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="999c8-5014">5.1 Considérations relatives à la sécurité pour les implémenteurs</span><span class="sxs-lookup"><span data-stu-id="999c8-5014">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="999c8-5015">Les implémentations d’indexation qui permettent d’indexer du contenu sécurisé doivent envisager d’utiliser le contexte utilisateur fourni par SMB \[ MS-SMB \] pour supprimer les résultats de recherche et retourner uniquement ceux accessibles à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="999c8-5015">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="999c8-5016">5.2 Index de paramètres de sécurité</span><span class="sxs-lookup"><span data-stu-id="999c8-5016">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="999c8-5017">Paramètre de sécurité</span><span class="sxs-lookup"><span data-stu-id="999c8-5017">Security Parameter</span></span>  | <span data-ttu-id="999c8-5018">Section</span><span class="sxs-lookup"><span data-stu-id="999c8-5018">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="999c8-5019">Niveau d'emprunt d'identité</span><span class="sxs-lookup"><span data-stu-id="999c8-5019">Impersonation level</span></span> | <span data-ttu-id="999c8-5020">2.1</span><span class="sxs-lookup"><span data-stu-id="999c8-5020">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="999c8-5021">6 index du comportement spécifique à la version</span><span class="sxs-lookup"><span data-stu-id="999c8-5021">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="999c8-5022">Comportement spécifique à la version</span><span class="sxs-lookup"><span data-stu-id="999c8-5022">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="999c8-5023">Section</span><span class="sxs-lookup"><span data-stu-id="999c8-5023">Section</span></span>   | <span data-ttu-id="999c8-5024">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="999c8-5024">Windows 2000</span></span> | <span data-ttu-id="999c8-5025">Windows XP</span><span class="sxs-lookup"><span data-stu-id="999c8-5025">Windows XP</span></span> | <span data-ttu-id="999c8-5026">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="999c8-5026">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="999c8-5027">Ce protocole est implémenté sur Windows 2000, Windows XP, Windows Server 2003 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="999c8-5027">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="999c8-5028">1.3.2</span><span class="sxs-lookup"><span data-stu-id="999c8-5028">1.3.2</span></span>     | <span data-ttu-id="999c8-5029">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5029">X</span></span>            | <span data-ttu-id="999c8-5030">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5030">X</span></span>          | <span data-ttu-id="999c8-5031">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5031">X</span></span>                   |
| <span data-ttu-id="999c8-5032">Les applications interagissent généralement avec un wrapper d’interface OLE DB</span><span class="sxs-lookup"><span data-stu-id="999c8-5032">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="999c8-5033">1.4</span><span class="sxs-lookup"><span data-stu-id="999c8-5033">1.4</span></span>       | <span data-ttu-id="999c8-5034">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5034">X</span></span>            | <span data-ttu-id="999c8-5035">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5035">X</span></span>          | <span data-ttu-id="999c8-5036">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5036">X</span></span>                   |
| <span data-ttu-id="999c8-5037">Valeurs NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="999c8-5037">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="999c8-5038">1.8</span><span class="sxs-lookup"><span data-stu-id="999c8-5038">1.8</span></span>       | <span data-ttu-id="999c8-5039">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5039">X</span></span>            | <span data-ttu-id="999c8-5040">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5040">X</span></span>          | <span data-ttu-id="999c8-5041">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5041">X</span></span>                   |
| <span data-ttu-id="999c8-5042">Le client définit le \_ champ d’État dans chaque en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="999c8-5042">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="999c8-5043">2.2.2</span><span class="sxs-lookup"><span data-stu-id="999c8-5043">2.2.2</span></span>     | <span data-ttu-id="999c8-5044">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5044">X</span></span>            | <span data-ttu-id="999c8-5045">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5045">X</span></span>          | <span data-ttu-id="999c8-5046">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5046">X</span></span>                   |
| <span data-ttu-id="999c8-5047">la valeur de cPendingScans est généralement zéro</span><span class="sxs-lookup"><span data-stu-id="999c8-5047">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="999c8-5048">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="999c8-5048">2.2.3.1</span></span>   | <span data-ttu-id="999c8-5049">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5049">X</span></span>            | <span data-ttu-id="999c8-5050">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5050">X</span></span>          | <span data-ttu-id="999c8-5051">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5051">X</span></span>                   |
| <span data-ttu-id="999c8-5052">valeur iClientVersion</span><span class="sxs-lookup"><span data-stu-id="999c8-5052">iClientVersion value</span></span>                                                                              | <span data-ttu-id="999c8-5053">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="999c8-5053">2.2.3.6</span></span>   | <span data-ttu-id="999c8-5054">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5054">X</span></span>            | <span data-ttu-id="999c8-5055">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5055">X</span></span>          | <span data-ttu-id="999c8-5056">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5056">X</span></span>                   |
| <span data-ttu-id="999c8-5057">\_valeur cbChunk</span><span class="sxs-lookup"><span data-stu-id="999c8-5057">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="999c8-5058">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="999c8-5058">2.2.3.19</span></span>  | <span data-ttu-id="999c8-5059">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5059">X</span></span>            | <span data-ttu-id="999c8-5060">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5060">X</span></span>          | <span data-ttu-id="999c8-5061">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5061">X</span></span>                   |
| <span data-ttu-id="999c8-5062">adresses mémoire 32 bits et 64 bits</span><span class="sxs-lookup"><span data-stu-id="999c8-5062">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="999c8-5063">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="999c8-5063">3.2.4.2.4</span></span> | <span data-ttu-id="999c8-5064">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5064">X</span></span>            | <span data-ttu-id="999c8-5065">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5065">X</span></span>          | <span data-ttu-id="999c8-5066">X</span><span class="sxs-lookup"><span data-stu-id="999c8-5066">X</span></span>                   |



 

 

 





