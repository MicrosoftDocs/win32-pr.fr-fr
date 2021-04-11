---
description: Préparation d’un fichier de configuration de ressource
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Préparation d’un fichier de configuration de ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112810"
---
# <a name="preparing-a-resource-configuration-file"></a><span data-ttu-id="22c35-103">Préparation d’un fichier de configuration de ressource</span><span class="sxs-lookup"><span data-stu-id="22c35-103">Preparing a Resource Configuration File</span></span>

<span data-ttu-id="22c35-104">Les utilitaires du compilateur MUIRCT et RC décrits dans [utilitaires de ressources](resource-utilities.md) fournissent une option de ligne de commande qui vous permet de spécifier un fichier de configuration de ressources pour les ressources de langue de base.</span><span class="sxs-lookup"><span data-stu-id="22c35-104">Both the MUIRCT and the RC Compiler utilities described in [Resource Utilities](resource-utilities.md) provide a command line option that allows you to specify a resource configuration file for the base language resources.</span></span> <span data-ttu-id="22c35-105">L’utilisation de ce fichier XML public et explicite permet de mieux contrôler le fractionnement des ressources que ce qui peut être obtenu à l’aide des commutateurs de ligne de commande standard des utilitaires.</span><span class="sxs-lookup"><span data-stu-id="22c35-105">Use of this public, human-readable XML file allows more control over the splitting of resources than can be obtained using the regular command line switches of the utilities.</span></span> <span data-ttu-id="22c35-106">Toutefois, même si vous ne fournissez pas de fichier de configuration de ressources comme entrée, les fichiers de ressources de la LN et spécifiques à la langue contiennent des données de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="22c35-106">However, even if you do not provide a resource configuration file as an input, the LN and language-specific resource files will contain resource configuration data.</span></span>

<span data-ttu-id="22c35-107">Tous les fichiers de configuration de ressources pour les applications Win32 commencent et se terminent de la même manière :</span><span class="sxs-lookup"><span data-stu-id="22c35-107">All resource configuration files for Win32 applications begin and end identically:</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



<span data-ttu-id="22c35-108">Cette rubrique se concentre sur les aspects du schéma XML qui sont utiles lors de la création de code non managé sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="22c35-108">This topic focuses on the aspects of the XML schema that are useful in building unmanaged code on Windows Vista and later.</span></span> <span data-ttu-id="22c35-109">En particulier, il est uniquement concerné par le comportement de l’élément win32Resources.</span><span class="sxs-lookup"><span data-stu-id="22c35-109">In particular, it is only concerned with the behavior of the win32Resources element.</span></span>

## <a name="win32resources-element"></a><span data-ttu-id="22c35-110">Élément win32Resources</span><span class="sxs-lookup"><span data-stu-id="22c35-110">win32Resources Element</span></span>

<span data-ttu-id="22c35-111">L’élément win32Resources a les attributs décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22c35-111">The win32Resources element has the attributes described in the following table.</span></span>



| <span data-ttu-id="22c35-112">Nom de l’attribut</span><span class="sxs-lookup"><span data-stu-id="22c35-112">Attribute name</span></span>           | <span data-ttu-id="22c35-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22c35-113">Mandatory</span></span> | <span data-ttu-id="22c35-114">Description</span><span class="sxs-lookup"><span data-stu-id="22c35-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c35-115">fileType</span><span class="sxs-lookup"><span data-stu-id="22c35-115">fileType</span></span>                 | <span data-ttu-id="22c35-116">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-116">No</span></span>        | <span data-ttu-id="22c35-117">Type de fichier.</span><span class="sxs-lookup"><span data-stu-id="22c35-117">Type of file.</span></span> <span data-ttu-id="22c35-118">Doit toujours être « application ».</span><span class="sxs-lookup"><span data-stu-id="22c35-118">Should always be "Application".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="22c35-119">somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="22c35-119">checksum</span></span>                 | <span data-ttu-id="22c35-120">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-120">No</span></span>        | <span data-ttu-id="22c35-121">Valeur de somme de contrôle à afficher dans les données de configuration de ressource du fichier LN et des fichiers de ressources spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-121">Checksum value to appear in the resource configuration data of the LN file and language-specific resource files.</span></span> <span data-ttu-id="22c35-122">Par exemple, cet attribut vous permet de copier la somme de contrôle à partir d’un seul fichier de ressources spécifique à une langue, en le comparant à celle de l’anglais (États-Unis), et de placer la somme de contrôle dans un fichier de ressources spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-122">For example, this attribute allows you to copy the checksum from a single language-specific resource file, by convention the one for English (United States), and place the checksum in a different language-specific resource file.</span></span> <span data-ttu-id="22c35-123">La somme de contrôle peut être spécifiée sous la forme d’une chaîne de nombres hexadécimaux ne dépassant pas 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="22c35-123">The checksum can be specified as a hexadecimal number string that is no longer than 32 characters.</span></span> <span data-ttu-id="22c35-124">La valeur numérique doit être contenance dans un nombre de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="22c35-124">The numerical value must be containable in a 128-bit number.</span></span> |
| <span data-ttu-id="22c35-125">langage</span><span class="sxs-lookup"><span data-stu-id="22c35-125">language</span></span>                 | <span data-ttu-id="22c35-126">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-126">No</span></span>        | <span data-ttu-id="22c35-127">Langue spécifiée à l’aide d’un format de nom conforme à la norme RFC 4646 (Windows Vista et versions ultérieures), par exemple, en-US pour l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="22c35-127">Language specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="22c35-128">ultimateFallbackLanguage</span><span class="sxs-lookup"><span data-stu-id="22c35-128">ultimateFallbackLanguage</span></span> | <span data-ttu-id="22c35-129">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-129">No</span></span>        | <span data-ttu-id="22c35-130">Langue à insérer dans les données de configuration de ressource pour le fichier LN, représentant le langage de secours ultime à utiliser dans une recherche de fichier de ressources spécifique à une langue correspondante.</span><span class="sxs-lookup"><span data-stu-id="22c35-130">Language to insert into the resource configuration data for the LN file, representing the ultimate fallback language to use in a search for a corresponding language-specific resource file.</span></span> <span data-ttu-id="22c35-131">Si le chargeur de ressources ne parvient pas à charger un fichier de ressources demandé à partir des langues d’interface utilisateur préférées du thread, il utilise un langage de secours ultime comme dernière tentative.</span><span class="sxs-lookup"><span data-stu-id="22c35-131">If the resource loader fails to load a requested resource file from the thread preferred UI languages, it uses an ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="22c35-132">Le langage est spécifié à l’aide d’un format de nom conforme à la norme RFC 4646 (Windows Vista et versions ultérieures), par exemple, en-US pour l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="22c35-132">The language is specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>       |
| <span data-ttu-id="22c35-133">ultimateFallbackLocation</span><span class="sxs-lookup"><span data-stu-id="22c35-133">ultimateFallbackLocation</span></span> | <span data-ttu-id="22c35-134">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-134">No</span></span>        | <span data-ttu-id="22c35-135">Emplacement de secours.</span><span class="sxs-lookup"><span data-stu-id="22c35-135">Fallback location.</span></span> <span data-ttu-id="22c35-136">Spécifiez « Internal » si les ressources de secours ultimes sont compilées dans le fichier LN.</span><span class="sxs-lookup"><span data-stu-id="22c35-136">Specify "internal" if ultimate fallback resources are compiled into the LN file.</span></span> <span data-ttu-id="22c35-137">Spécifiez « External » (valeur par défaut) si le fichier LN doit faire référence à un fichier de ressources spécifique à une langue pour ses ressources de secours ultimes.</span><span class="sxs-lookup"><span data-stu-id="22c35-137">Specify "external" (default) if the LN file is to reference a language-specific resource file for its ultimate fallback resources.</span></span>                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="22c35-138">Dans le fichier de configuration de ressource, l’élément win32Resources contient les sous-éléments décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22c35-138">In the resource configuration file, the win32Resources element has the sub-elements described in the next table.</span></span>



| <span data-ttu-id="22c35-139">Nom de l’élément</span><span class="sxs-lookup"><span data-stu-id="22c35-139">Element Name</span></span>       | <span data-ttu-id="22c35-140">Description</span><span class="sxs-lookup"><span data-stu-id="22c35-140">Description</span></span>                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c35-141">localizedResources</span><span class="sxs-lookup"><span data-stu-id="22c35-141">localizedResources</span></span> | <span data-ttu-id="22c35-142">Ressources qui encapsulent des informations sur les types de ressources et les ressources individuelles contenues dans un fichier de ressources spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-142">Resources that encapsulate information about the resource types and individual resources contained in a language-specific resource file.</span></span> |
| <span data-ttu-id="22c35-143">neutralResources</span><span class="sxs-lookup"><span data-stu-id="22c35-143">neutralResources</span></span>   | <span data-ttu-id="22c35-144">Ressources qui encapsulent des informations sur les types de ressources contenus dans un fichier LN.</span><span class="sxs-lookup"><span data-stu-id="22c35-144">Resources that encapsulate information about the resource types contained in an LN file.</span></span>                                                 |



 

## <a name="localizedresources-element"></a><span data-ttu-id="22c35-145">Élément localizedResources</span><span class="sxs-lookup"><span data-stu-id="22c35-145">localizedResources Element</span></span>

<span data-ttu-id="22c35-146">Élément des ressources localisées.</span><span class="sxs-lookup"><span data-stu-id="22c35-146">Localized resources element.</span></span> <span data-ttu-id="22c35-147">Par défaut, cet élément n’a pas d’attributs et un seul type de sous-élément.</span><span class="sxs-lookup"><span data-stu-id="22c35-147">By default, this element has no attributes and only one type of sub-element.</span></span> <span data-ttu-id="22c35-148">Il s’agit simplement d’un conteneur pour les éléments resourceType.</span><span class="sxs-lookup"><span data-stu-id="22c35-148">It is just a container for resourceType elements.</span></span>



| <span data-ttu-id="22c35-149">Nom d’attribut</span><span class="sxs-lookup"><span data-stu-id="22c35-149">Attribute Name</span></span> | <span data-ttu-id="22c35-150">Description</span><span class="sxs-lookup"><span data-stu-id="22c35-150">Description</span></span>                                                                    |
|----------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="22c35-151">resourceType</span><span class="sxs-lookup"><span data-stu-id="22c35-151">resourceType</span></span>   | <span data-ttu-id="22c35-152">Type d’une ressource individuelle contenue dans un fichier de ressources spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-152">Type of an individual resource contained in a language-specific resource file.</span></span> |



 

## <a name="neutralresources-element"></a><span data-ttu-id="22c35-153">Élément neutralResources</span><span class="sxs-lookup"><span data-stu-id="22c35-153">neutralResources Element</span></span>

<span data-ttu-id="22c35-154">Élément ressources neutres.</span><span class="sxs-lookup"><span data-stu-id="22c35-154">Neutral resources element.</span></span> <span data-ttu-id="22c35-155">Cet élément est simplement un conteneur pour les éléments resourceType.</span><span class="sxs-lookup"><span data-stu-id="22c35-155">This element is just a container for resourceType elements.</span></span>



| <span data-ttu-id="22c35-156">Nom d’attribut</span><span class="sxs-lookup"><span data-stu-id="22c35-156">Attribute Name</span></span> | <span data-ttu-id="22c35-157">Description</span><span class="sxs-lookup"><span data-stu-id="22c35-157">Description</span></span>                                        |
|----------------|----------------------------------------------------|
| <span data-ttu-id="22c35-158">resourceType</span><span class="sxs-lookup"><span data-stu-id="22c35-158">resourceType</span></span>   | <span data-ttu-id="22c35-159">Type d’une ressource unique contenue dans un fichier LN.</span><span class="sxs-lookup"><span data-stu-id="22c35-159">Type of a single resource contained in an LN file.</span></span> |



 

## <a name="resourcetype-element"></a><span data-ttu-id="22c35-160">resourceType, élément</span><span class="sxs-lookup"><span data-stu-id="22c35-160">resourceType Element</span></span>

<span data-ttu-id="22c35-161">L’élément resourceType encapsule des informations sur un type de ressource unique ou une ressource individuelle.</span><span class="sxs-lookup"><span data-stu-id="22c35-161">The resourceType element encapsulates information about a single resource type or individual resource.</span></span> <span data-ttu-id="22c35-162">Il possède les attributs indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="22c35-162">It has the attributes listed below.</span></span>

> [!Caution]  
> <span data-ttu-id="22c35-163">Certains défauts de configuration des ressources sont interceptés uniquement par le compilateur RC ou MUIRCT, selon le fichier de ressources d’entrée ou le contenu du fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="22c35-163">Some resource configuration defects are caught only by RC Compiler or MUIRCT, depending on the input resource file or binary file content.</span></span> <span data-ttu-id="22c35-164">Les erreurs resourceType dans le fichier de configuration de ressource qui n’existent pas dans le fichier d’entrée ne sont pas interceptées, ce qui entraîne un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="22c35-164">The resourceType errors in the resource configuration file that do not exist in the input file are not caught, resulting in unexpected behavior.</span></span> <span data-ttu-id="22c35-165">Les utilisateurs peuvent utiliser un fichier de configuration de ressource défectueux et ne savent pas jusqu’à ce qu’ils introduisent des fichiers binaires qui utilisent les parties cassées du fichier de configuration de ressources, ce qui crée l’apparence des arrêts des fichiers binaires actuels.</span><span class="sxs-lookup"><span data-stu-id="22c35-165">Users can be using a defective resource configuration file and do not know until they introduce binaries that use the broken parts of the resource configuration file, which creates the appearance that the breaks are from the current binaries.</span></span>

 



| <span data-ttu-id="22c35-166">Nom de l’attribut</span><span class="sxs-lookup"><span data-stu-id="22c35-166">Attribute name</span></span> | <span data-ttu-id="22c35-167">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22c35-167">Mandatory</span></span> | <span data-ttu-id="22c35-168">Description</span><span class="sxs-lookup"><span data-stu-id="22c35-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c35-169">typeNameId</span><span class="sxs-lookup"><span data-stu-id="22c35-169">typeNameId</span></span>     | <span data-ttu-id="22c35-170">Oui</span><span class="sxs-lookup"><span data-stu-id="22c35-170">Yes</span></span>       | <span data-ttu-id="22c35-171">Nom de type ou identificateur de la ressource.</span><span class="sxs-lookup"><span data-stu-id="22c35-171">Type name or identifier for the resource.</span></span> <span data-ttu-id="22c35-172">Spécifiez un nom de chaîne ou un nombre.</span><span class="sxs-lookup"><span data-stu-id="22c35-172">Specify a string name or a number.</span></span> <span data-ttu-id="22c35-173">Si vous utilisez un nombre, faites précéder la chaîne d’un « \# » pour indiquer qu’elle représente un nombre.</span><span class="sxs-lookup"><span data-stu-id="22c35-173">If using a number, prepend the string with a "\#" to indicate that it represents a number.</span></span> <span data-ttu-id="22c35-174">Chaque élément resourceType ne doit avoir qu’un seul attribut *typeNameId* .</span><span class="sxs-lookup"><span data-stu-id="22c35-174">Each resourceType element must have only one *typeNameId* attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="22c35-175">itemName</span><span class="sxs-lookup"><span data-stu-id="22c35-175">itemName</span></span>       | <span data-ttu-id="22c35-176">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-176">No</span></span>        | <span data-ttu-id="22c35-177">Chaîne de nom d’élément de la ressource, à placer dans le fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-177">Item name string for the resource, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="22c35-178">Vous pouvez spécifier plusieurs noms, séparés par des espaces blancs, par exemple, « HTML MOFDATA ».</span><span class="sxs-lookup"><span data-stu-id="22c35-178">You can specify multiple names, separated by white spaces, for example, "HTML MOFDATA".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="22c35-179">itemId</span><span class="sxs-lookup"><span data-stu-id="22c35-179">itemId</span></span>         | <span data-ttu-id="22c35-180">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-180">No</span></span>        | <span data-ttu-id="22c35-181">Identificateur d’un élément de ressource individuel à placer dans le fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-181">Identifier of individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="22c35-182">L’élément peut être spécifié sous la forme d’une plage (par exemple, « 1-12 ») ou d’identificateurs individuels séparés par des espaces blancs (par exemple, « 1 3 4 »).</span><span class="sxs-lookup"><span data-stu-id="22c35-182">The item can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="22c35-183">stringId</span><span class="sxs-lookup"><span data-stu-id="22c35-183">stringId</span></span>       | <span data-ttu-id="22c35-184">Non</span><span class="sxs-lookup"><span data-stu-id="22c35-184">No</span></span>        | <span data-ttu-id="22c35-185">Identificateur de chaîne pour un élément de ressource individuel, à placer dans le fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-185">String identifier for individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="22c35-186">La chaîne peut être spécifiée sous la forme d’une plage (par exemple, « 1-12 ») ou par identificateurs individuels séparés par des espaces blancs (par exemple, « 1 3 4 »). Cet attribut permet de spécifier à la fois les entrées de table de chaînes localisables et celles qui ne sont pas localisables.</span><span class="sxs-lookup"><span data-stu-id="22c35-186">The string can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").This attribute allows the specification of both localizable and nonlocalizable string table entries.</span></span> <span data-ttu-id="22c35-187">Elle doit être utilisée conjointement avec la valeur *typeNameId* de « 6 », ce qui dénote un type de ressource d’entrée de table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="22c35-187">It must be used in conjunction with the *typeNameId* value of "6", denoting a string table entry resource type.</span></span><br/> <span data-ttu-id="22c35-188">Les chaînes sont stockées dans des blocs de 16 dans une table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="22c35-188">Strings are stored in blocks of 16 in a string table.</span></span> <span data-ttu-id="22c35-189">Par exemple, les chaînes 0 à 15 sont stockées dans un bloc d’élément de ressource unique et peuvent être référencées dans le fichier de configuration de ressource en tant qu' *ItemId* 1, ou en tant que *stringid* « 0-15 ».</span><span class="sxs-lookup"><span data-stu-id="22c35-189">For example, strings 0 to 15 are stored in a single resource item block and can be referenced in the resource configuration file as *itemId* 1, or as *stringId* "0-15".</span></span> <span data-ttu-id="22c35-190">Par exemple, s’il existe cinq chaînes localisables et trois chaînes qui ne sont pas localisables, vous devez assigner des identificateurs de chaîne 0-4 pour les chaînes localisables et des identificateurs de chaîne 16-18 pour les chaînes qui ne peuvent pas être localisées.</span><span class="sxs-lookup"><span data-stu-id="22c35-190">For example, if there are five localizable strings and three nonlocalizable strings, you should assign string identifiers 0-4 for the localizable strings, and string identifiers 16-18 for the nonlocalizable strings.</span></span> <span data-ttu-id="22c35-191">Si vous n’organisez pas les chaînes de cette manière, les blocs de chaînes affectés sont placés à la fois dans le fichier LN et dans le fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-191">If you do not organize strings this way, the affected blocks of strings are placed in both the LN file and the language-specific resource file.</span></span><br/> |



 

<span data-ttu-id="22c35-192">Si vous spécifiez les attributs *ItemName*, *ItemId* et/ou *stringid* pour un type de ressource particulier sous l’élément localizedResource, seuls les éléments ou chaînes spécifiés pour le type de ressource désigné sont placés dans le fichier de ressources spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-192">If you specify the *itemName*, *itemId*, and/or *stringId* attributes for a particular resource type under the localizedResource element, only these specified items or strings for the designated resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="22c35-193">Si un élément resourceType est spécifié sans nom d’élément explicite, identificateur d’élément ou identificateur de chaîne, tous les éléments du type de ressource spécifié sont placés dans le fichier de ressources spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="22c35-193">If a resourceType element is specified without any explicit item name, item identifier, or string identifier, all items of the specified resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="22c35-194">Les éléments ou types non répertoriés dans un élément localizedResource sont placés dans le fichier LN.</span><span class="sxs-lookup"><span data-stu-id="22c35-194">Items or types not listed in any localizedResource element are placed in the LN file.</span></span>

<span data-ttu-id="22c35-195">Voici les types de ressources standard et leurs identificateurs numériques :</span><span class="sxs-lookup"><span data-stu-id="22c35-195">The following are the standard resource types and their numeric identifiers:</span></span>

-   <span data-ttu-id="22c35-196">CURSOR (1)</span><span class="sxs-lookup"><span data-stu-id="22c35-196">CURSOR(1)</span></span>
-   <span data-ttu-id="22c35-197">BITMAP (2)</span><span class="sxs-lookup"><span data-stu-id="22c35-197">BITMAP(2)</span></span>
-   <span data-ttu-id="22c35-198">ICÔNE (3)</span><span class="sxs-lookup"><span data-stu-id="22c35-198">ICON(3)</span></span>
-   <span data-ttu-id="22c35-199">MENU (4)</span><span class="sxs-lookup"><span data-stu-id="22c35-199">MENU(4)</span></span>
-   <span data-ttu-id="22c35-200">BOÎTE DE DIALOGUE (5)</span><span class="sxs-lookup"><span data-stu-id="22c35-200">DIALOG(5)</span></span>
-   <span data-ttu-id="22c35-201">CHAÎNE (6)</span><span class="sxs-lookup"><span data-stu-id="22c35-201">STRING(6)</span></span>
-   <span data-ttu-id="22c35-202">FONTDIR (7)</span><span class="sxs-lookup"><span data-stu-id="22c35-202">FONTDIR(7)</span></span>
-   <span data-ttu-id="22c35-203">POLICE (8)</span><span class="sxs-lookup"><span data-stu-id="22c35-203">FONT(8)</span></span>
-   <span data-ttu-id="22c35-204">ACCÉLÉRATEURS (9)</span><span class="sxs-lookup"><span data-stu-id="22c35-204">ACCELERATORS(9)</span></span>
-   <span data-ttu-id="22c35-205">RCDATA (10)</span><span class="sxs-lookup"><span data-stu-id="22c35-205">RCDATA(10)</span></span>
-   <span data-ttu-id="22c35-206">MESSAGETABLE (11)</span><span class="sxs-lookup"><span data-stu-id="22c35-206">MESSAGETABLE(11)</span></span>
-   <span data-ttu-id="22c35-207">\_Curseur de groupe (12)</span><span class="sxs-lookup"><span data-stu-id="22c35-207">GROUP\_CURSOR(12)</span></span>
-   <span data-ttu-id="22c35-208">\_Icône de groupe (14)</span><span class="sxs-lookup"><span data-stu-id="22c35-208">GROUP\_ICON(14)</span></span>
-   <span data-ttu-id="22c35-209">VERSION (16)</span><span class="sxs-lookup"><span data-stu-id="22c35-209">VERSION(16)</span></span>
-   <span data-ttu-id="22c35-210">HTML (23)</span><span class="sxs-lookup"><span data-stu-id="22c35-210">HTML(23)</span></span>

## <a name="example"></a><span data-ttu-id="22c35-211">Exemple</span><span class="sxs-lookup"><span data-stu-id="22c35-211">Example</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a><span data-ttu-id="22c35-212">Notes</span><span class="sxs-lookup"><span data-stu-id="22c35-212">Remarks</span></span>

<span data-ttu-id="22c35-213">Si vous incluez des types de ressources icône (3), boîte de dialogue (5), chaîne (6) ou VERSION (16) dans l’élément neutralResources, vous devez dupliquer cette entrée dans l’élément localizedResources.</span><span class="sxs-lookup"><span data-stu-id="22c35-213">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element.</span></span> <span data-ttu-id="22c35-214">Vous pouvez voir ce qui est illustré dans l’exemple ci-dessus, où le type de ressource 16 apparaît dans les sections ressources neutres et ressources localisées.</span><span class="sxs-lookup"><span data-stu-id="22c35-214">You can see this illustrated in the example above, where resource type 16 appears in both neutral and localized resources sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22c35-215">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22c35-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c35-216">Préparation des ressources</span><span class="sxs-lookup"><span data-stu-id="22c35-216">Preparing Resources</span></span>](preparing-resources.md)
</dt> </dl>

 

 




