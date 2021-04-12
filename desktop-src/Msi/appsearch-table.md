---
description: La table AppSearch contient les propriétés nécessaires à la recherche d’un fichier ayant une signature de fichier particulière. La table AppSearch peut également être utilisée pour affecter à une propriété la valeur existante d’une entrée de registre ou de fichier. ini.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Table AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202555"
---
# <a name="appsearch-table"></a><span data-ttu-id="717bf-104">Table AppSearch</span><span class="sxs-lookup"><span data-stu-id="717bf-104">AppSearch Table</span></span>

<span data-ttu-id="717bf-105">La table AppSearch contient les propriétés nécessaires à la recherche d’un fichier ayant une signature de fichier particulière.</span><span class="sxs-lookup"><span data-stu-id="717bf-105">The AppSearch table contains properties needed to search for a file having a particular file signature.</span></span> <span data-ttu-id="717bf-106">La table AppSearch peut également être utilisée pour affecter à une propriété la valeur existante d’une entrée de registre ou de fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="717bf-106">The AppSearch table can also be used to set a property to the existing value of a registry or .ini file entry.</span></span>

<span data-ttu-id="717bf-107">La table AppSearch contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="717bf-107">The AppSearch table has the following columns.</span></span>



| <span data-ttu-id="717bf-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="717bf-108">Column</span></span>      | <span data-ttu-id="717bf-109">Type</span><span class="sxs-lookup"><span data-stu-id="717bf-109">Type</span></span>                         | <span data-ttu-id="717bf-110">Clé</span><span class="sxs-lookup"><span data-stu-id="717bf-110">Key</span></span> | <span data-ttu-id="717bf-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="717bf-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="717bf-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="717bf-112">Property</span></span>    | [<span data-ttu-id="717bf-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="717bf-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="717bf-114">O</span><span class="sxs-lookup"><span data-stu-id="717bf-114">Y</span></span>   | <span data-ttu-id="717bf-115">N</span><span class="sxs-lookup"><span data-stu-id="717bf-115">N</span></span>        |
| <span data-ttu-id="717bf-116">Signature\_</span><span class="sxs-lookup"><span data-stu-id="717bf-116">Signature\_</span></span> | [<span data-ttu-id="717bf-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="717bf-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="717bf-118">O</span><span class="sxs-lookup"><span data-stu-id="717bf-118">Y</span></span>   | <span data-ttu-id="717bf-119">N</span><span class="sxs-lookup"><span data-stu-id="717bf-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="717bf-120">Colonnes</span><span class="sxs-lookup"><span data-stu-id="717bf-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="717bf-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété</span><span class="sxs-lookup"><span data-stu-id="717bf-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="717bf-122">L’exécution de l’action [AppSearch](appsearch-action.md) affecte à cette propriété l’emplacement du fichier indiqué par la \_ colonne signature.</span><span class="sxs-lookup"><span data-stu-id="717bf-122">Running the [AppSearch](appsearch-action.md) action sets this property to the location of the file indicated by the Signature\_ column.</span></span> <span data-ttu-id="717bf-123">Cette propriété est définie si la signature de fichier existe sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="717bf-123">This property is set if the file signature exists on the user's computer.</span></span> <span data-ttu-id="717bf-124">Les propriétés utilisées dans cette colonne doivent être des propriétés [publiques](public-properties.md) et comporter un identificateur qui ne contient pas de minuscules.</span><span class="sxs-lookup"><span data-stu-id="717bf-124">The properties used in this column must be [public](public-properties.md) properties and have an identifier that contains no lowercase letters.</span></span>

<span data-ttu-id="717bf-125">La propriété figurant dans le champ de propriété peut être initialisée dans la table de [Propriétés](property-table.md) ou à partir d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="717bf-125">The property listed in the Property field may be initialized in the [Property](property-table.md) table or from a command line.</span></span> <span data-ttu-id="717bf-126">Si l’action [AppSearch](appsearch-action.md) localise la signature, le programme d’installation remplace la valeur de propriété initialisée par la valeur trouvée.</span><span class="sxs-lookup"><span data-stu-id="717bf-126">If the [AppSearch](appsearch-action.md) action locates the signature, the installer overrides the initialized property value with the found value.</span></span> <span data-ttu-id="717bf-127">Si la signature est introuvable, la valeur initiale de la propriété est utilisée.</span><span class="sxs-lookup"><span data-stu-id="717bf-127">If the signature is not found, then the initial property value is used.</span></span> <span data-ttu-id="717bf-128">Si la propriété n’a jamais été initialisée, la propriété est définie uniquement si la signature est trouvée.</span><span class="sxs-lookup"><span data-stu-id="717bf-128">If the property was never initialized, then the property will only be set if the signature is found.</span></span> <span data-ttu-id="717bf-129">Dans le cas contraire, la propriété n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="717bf-129">Otherwise, the property is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="717bf-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="717bf-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="717bf-131">La \_ colonne signature contient un identificateur unique appelé signature et est également une clé externe dans les tables [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)et [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="717bf-131">The Signature\_ column contains a unique identifier called a signature and is also an external key into the [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span> <span data-ttu-id="717bf-132">Lors de la recherche d’un fichier, la valeur dans cette colonne doit également être une clé étrangère dans la table de [signatures](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="717bf-132">When searching for a file, the value in this column must also be a foreign key into the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="717bf-133">Si la valeur de cette colonne n’est pas indiquée dans la table de signatures, le programme d’installation détermine que la recherche concerne un répertoire.</span><span class="sxs-lookup"><span data-stu-id="717bf-133">If the value in this column is not listed in the Signature table, the installer determines that the search is for a directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="717bf-134">Notes</span><span class="sxs-lookup"><span data-stu-id="717bf-134">Remarks</span></span>

<span data-ttu-id="717bf-135">L’action [AppSearch](appsearch-action.md) dans les [*tables de séquence*](s-gly.md) traite les informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="717bf-135">The [AppSearch](appsearch-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="717bf-136">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="717bf-136">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="717bf-137">L’action [AppSearch](appsearch-action.md) recherche les signatures à l’aide de la table [CompLocator](complocator-table.md) en premier, de la table [RegLocator](reglocator-table.md) , de la table [IniLocator](inilocator-table.md) , troisième, et enfin de la table [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="717bf-137">The [AppSearch](appsearch-action.md) action searches for signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table second, the [IniLocator](inilocator-table.md) table third, and finally the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="717bf-138">Les signatures de fichiers sont répertoriées dans la table de [signature](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="717bf-138">File signatures are listed in the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="717bf-139">Une signature qui ne figure pas dans la table de signature désigne un répertoire et l’action définit la propriété sur le chemin d’accès au répertoire de cette signature.</span><span class="sxs-lookup"><span data-stu-id="717bf-139">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="717bf-140">Consultez [recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="717bf-140">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="717bf-141">Validation</span><span class="sxs-lookup"><span data-stu-id="717bf-141">Validation</span></span>

<dl>

[<span data-ttu-id="717bf-142">ICE03</span><span class="sxs-lookup"><span data-stu-id="717bf-142">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="717bf-143">ICE06</span><span class="sxs-lookup"><span data-stu-id="717bf-143">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="717bf-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="717bf-144">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="717bf-145">ICE52</span><span class="sxs-lookup"><span data-stu-id="717bf-145">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="717bf-146">ICE88</span><span class="sxs-lookup"><span data-stu-id="717bf-146">ICE88</span></span>](ice88.md)  
</dl>

 

 



