---
description: La table CompLocator contient les informations nécessaires pour trouver un fichier ou un répertoire qui utilise les données de configuration du programme d’installation.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Table CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530238"
---
# <a name="complocator-table"></a><span data-ttu-id="40859-103">Table CompLocator</span><span class="sxs-lookup"><span data-stu-id="40859-103">CompLocator Table</span></span>

<span data-ttu-id="40859-104">La table CompLocator contient les informations nécessaires pour trouver un fichier ou un répertoire qui utilise les données de configuration du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="40859-104">The CompLocator Table contains the information needed to find a file or directory that is using the installer configuration data.</span></span>

<span data-ttu-id="40859-105">La table CompLocator contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="40859-105">The CompLocator table contains the following information.</span></span>



| <span data-ttu-id="40859-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="40859-106">Column</span></span>      | <span data-ttu-id="40859-107">Type</span><span class="sxs-lookup"><span data-stu-id="40859-107">Type</span></span>                         | <span data-ttu-id="40859-108">Clé</span><span class="sxs-lookup"><span data-stu-id="40859-108">Key</span></span> | <span data-ttu-id="40859-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="40859-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="40859-110">Signature\_</span><span class="sxs-lookup"><span data-stu-id="40859-110">Signature\_</span></span> | [<span data-ttu-id="40859-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="40859-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="40859-112">O</span><span class="sxs-lookup"><span data-stu-id="40859-112">Y</span></span>   | <span data-ttu-id="40859-113">N</span><span class="sxs-lookup"><span data-stu-id="40859-113">N</span></span>        |
| <span data-ttu-id="40859-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="40859-114">ComponentId</span></span> | [<span data-ttu-id="40859-115">GUID</span><span class="sxs-lookup"><span data-stu-id="40859-115">GUID</span></span>](guid.md)             | <span data-ttu-id="40859-116">N</span><span class="sxs-lookup"><span data-stu-id="40859-116">N</span></span>   | <span data-ttu-id="40859-117">N</span><span class="sxs-lookup"><span data-stu-id="40859-117">N</span></span>        |
| <span data-ttu-id="40859-118">Type</span><span class="sxs-lookup"><span data-stu-id="40859-118">Type</span></span>        | [<span data-ttu-id="40859-119">Integer</span><span class="sxs-lookup"><span data-stu-id="40859-119">Integer</span></span>](integer.md)       | <span data-ttu-id="40859-120">N</span><span class="sxs-lookup"><span data-stu-id="40859-120">N</span></span>   | <span data-ttu-id="40859-121">O</span><span class="sxs-lookup"><span data-stu-id="40859-121">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="40859-122">Informations sur les colonnes</span><span class="sxs-lookup"><span data-stu-id="40859-122">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="40859-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="40859-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="40859-124">Cette colonne représente une signature de fichier unique et est également la clé externe dans la [table de signatures](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="40859-124">This column represents a unique file signature and is also the external key into the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="40859-125">Si la clé est absente de la table de signatures, la recherche est supposée être en présence d’un répertoire désigné par la table CompLocator.</span><span class="sxs-lookup"><span data-stu-id="40859-125">If the key is absent from the Signature Table, the search is assumed to be for the presence of a directory pointed to by the CompLocator Table.</span></span>

</dd> <dt>

<span data-ttu-id="40859-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="40859-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="40859-127">ID du composant dont le chemin d’accès de clé doit être utilisé pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="40859-127">The component ID of the component whose key path is to be used for the search.</span></span> <span data-ttu-id="40859-128">Il doit s’agir du GUID d’un composant qui apparaît dans le champ ComponentId de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="40859-128">This should be the GUID of a component that appears in the ComponentId field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="40859-129">Il peut s’agir de l’ID d’un composant appartenant à un autre produit installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="40859-129">It may be the component ID of a component belonging to another product installed on the computer.</span></span> <span data-ttu-id="40859-130">Il ne doit pas s’agir du GUID d’un composant publié apparaissant dans le champ ComponentId de la [table PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="40859-130">It should not be the GUID of a published component appearing in the ComponentId field of the [PublishComponent Table](publishcomponent-table.md).</span></span>

<span data-ttu-id="40859-131">Pour trouver la valeur GUID de l’ID du composant pour un fichier installé par un autre produit, accédez au package d’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="40859-131">To find the component ID GUID value for a file installed by another product, go to the installation package of the product.</span></span> <span data-ttu-id="40859-132">Accédez à la [table file](file-table.md) et recherchez la ligne contenant l’identificateur de fichier du fichier.</span><span class="sxs-lookup"><span data-stu-id="40859-132">Go to the [File Table](file-table.md) and find the row that contains the file identifier for the file.</span></span> <span data-ttu-id="40859-133">La \_ colonne composant de cette ligne contient l’identificateur de composant pour le composant qui contrôle le fichier.</span><span class="sxs-lookup"><span data-stu-id="40859-133">The Component\_ column of this row contains the component identifier for the component that controls the file.</span></span> <span data-ttu-id="40859-134">Accédez à la [table des composants](component-table.md) et recherchez la ligne qui contient cet identificateur de composant dans la colonne composant.</span><span class="sxs-lookup"><span data-stu-id="40859-134">Go to the [Component table](component-table.md) and find the row that contains this component identifier in the Component column.</span></span> <span data-ttu-id="40859-135">La colonne ComponentId de cette ligne contient le GUID de l’ID du composant.</span><span class="sxs-lookup"><span data-stu-id="40859-135">The ComponentId column of this row contains the component ID GUID.</span></span>

</dd> <dt>

<span data-ttu-id="40859-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer</span><span class="sxs-lookup"><span data-stu-id="40859-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="40859-137">Valeur booléenne qui détermine si le chemin d’accès de la clé du composant est un nom de fichier ou un emplacement de répertoire.</span><span class="sxs-lookup"><span data-stu-id="40859-137">A Boolean value that determines if the key path of the component is a file name or a directory location.</span></span>

<span data-ttu-id="40859-138">Le tableau suivant répertorie les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="40859-138">The following table lists valid values.</span></span> <span data-ttu-id="40859-139">Si elle est absente, le type est défini sur 1 (un).</span><span class="sxs-lookup"><span data-stu-id="40859-139">If absent, Type is set to be 1 (one).</span></span>



| <span data-ttu-id="40859-140">Constante</span><span class="sxs-lookup"><span data-stu-id="40859-140">Constant</span></span>                      | <span data-ttu-id="40859-141">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="40859-141">Hexadecimal</span></span> | <span data-ttu-id="40859-142">Decimal</span><span class="sxs-lookup"><span data-stu-id="40859-142">Decimal</span></span> | <span data-ttu-id="40859-143">Description</span><span class="sxs-lookup"><span data-stu-id="40859-143">Description</span></span>              |
|-------------------------------|-------------|---------|--------------------------|
| <span data-ttu-id="40859-144">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="40859-144">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="40859-145">0x000</span><span class="sxs-lookup"><span data-stu-id="40859-145">0x000</span></span>       | <span data-ttu-id="40859-146">0</span><span class="sxs-lookup"><span data-stu-id="40859-146">0</span></span>       | <span data-ttu-id="40859-147">Le chemin d’accès de la clé est un répertoire.</span><span class="sxs-lookup"><span data-stu-id="40859-147">Key path is a directory.</span></span> |
| <span data-ttu-id="40859-148">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="40859-148">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="40859-149">0x001</span><span class="sxs-lookup"><span data-stu-id="40859-149">0x001</span></span>       | <span data-ttu-id="40859-150">1</span><span class="sxs-lookup"><span data-stu-id="40859-150">1</span></span>       | <span data-ttu-id="40859-151">Le chemin d’accès de la clé est un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="40859-151">Key path is a file name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40859-152">Notes</span><span class="sxs-lookup"><span data-stu-id="40859-152">Remarks</span></span>

<span data-ttu-id="40859-153">Cette table est utilisée avec la [table AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="40859-153">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="40859-154">En règle générale, les colonnes de cette table ne sont pas localisées.</span><span class="sxs-lookup"><span data-stu-id="40859-154">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="40859-155">Si un auteur décide de rechercher des produits dans plusieurs langues, il peut y avoir une entrée distincte incluse dans le tableau pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="40859-155">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="40859-156">Pour plus d’informations, consultez [recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="40859-156">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="40859-157">Validation</span><span class="sxs-lookup"><span data-stu-id="40859-157">Validation</span></span>

<dl>

[<span data-ttu-id="40859-158">ICE03</span><span class="sxs-lookup"><span data-stu-id="40859-158">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="40859-159">ICE06</span><span class="sxs-lookup"><span data-stu-id="40859-159">ICE06</span></span>](ice06.md)  
</dl>

 

 



