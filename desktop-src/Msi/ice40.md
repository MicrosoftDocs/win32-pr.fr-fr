---
description: ICE40 effectue une validation diverse.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115755"
---
# <a name="ice40"></a><span data-ttu-id="7784b-103">ICE40</span><span class="sxs-lookup"><span data-stu-id="7784b-103">ICE40</span></span>

<span data-ttu-id="7784b-104">ICE40 effectue une validation diverse.</span><span class="sxs-lookup"><span data-stu-id="7784b-104">ICE40 does miscellaneous validation.</span></span>

## <a name="result"></a><span data-ttu-id="7784b-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="7784b-105">Result</span></span>

<span data-ttu-id="7784b-106">ICE40 publie des avertissements sur les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7784b-106">ICE40 posts warnings on the following:</span></span>

-   <span data-ttu-id="7784b-107">La propriété [**REINSTALLMODE**](reinstallmode.md) a été substituée.</span><span class="sxs-lookup"><span data-stu-id="7784b-107">The [**REINSTALLMODE**](reinstallmode.md) property has been overridden.</span></span>
-   <span data-ttu-id="7784b-108">La [table RemoveIniFile](removeinifile-table.md) possède une entrée de balise DELETE sans valeur.</span><span class="sxs-lookup"><span data-stu-id="7784b-108">The [RemoveIniFile table](removeinifile-table.md) has a Delete Tag entry with no value.</span></span>
-   <span data-ttu-id="7784b-109">La [table d’erreurs](error-table.md) est manquante dans le fichier. msi et la propriété de résumé du [**nombre de pages**](page-count-summary.md) est inférieure ou égale à 100.</span><span class="sxs-lookup"><span data-stu-id="7784b-109">The .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <span data-ttu-id="7784b-110">Cet avertissement ICE est obsolète, car Windows Installer ne requiert pas que le package ait une table d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="7784b-110">This ICE warning is obsolete because Windows Installer does not require the package to have an Error table.</span></span> <span data-ttu-id="7784b-111">Les messages d’erreur peuvent être récupérés à l’aide de Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="7784b-111">Error messages can be retrieved using Msimsg.dll.</span></span>

## <a name="example"></a><span data-ttu-id="7784b-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="7784b-112">Example</span></span>

[<span data-ttu-id="7784b-113">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="7784b-113">Property Table</span></span>](property-table.md)



| <span data-ttu-id="7784b-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="7784b-114">Property</span></span>                               | <span data-ttu-id="7784b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7784b-115">Value</span></span> |
|----------------------------------------|-------|
| [<span data-ttu-id="7784b-116">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="7784b-116">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="7784b-117">Un</span><span class="sxs-lookup"><span data-stu-id="7784b-117">A</span></span>     |



 

[<span data-ttu-id="7784b-118">Table RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="7784b-118">RemoveIniFile Table</span></span>](removeinifile-table.md)



| <span data-ttu-id="7784b-119">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="7784b-119">RemoveIniFile</span></span>                          | <span data-ttu-id="7784b-120">Action</span><span class="sxs-lookup"><span data-stu-id="7784b-120">Action</span></span> | <span data-ttu-id="7784b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7784b-121">Value</span></span> |
|----------------------------------------|--------|-------|
| [<span data-ttu-id="7784b-122">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="7784b-122">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="7784b-123">4</span><span class="sxs-lookup"><span data-stu-id="7784b-123">4</span></span>      |       |



 

## <a name="results"></a><span data-ttu-id="7784b-124">Résultats</span><span class="sxs-lookup"><span data-stu-id="7784b-124">Results</span></span>

<span data-ttu-id="7784b-125">ICE40 signale les erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7784b-125">ICE40 would report the following errors.</span></span>



| <span data-ttu-id="7784b-126">Erreur ICE40</span><span class="sxs-lookup"><span data-stu-id="7784b-126">ICE40 error</span></span>                                                                                           | <span data-ttu-id="7784b-127">Description</span><span class="sxs-lookup"><span data-stu-id="7784b-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7784b-128">[**REINSTALLMODE**](reinstallmode.md) est défini dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7784b-128">[**REINSTALLMODE**](reinstallmode.md) is defined in the Property table.</span></span> <span data-ttu-id="7784b-129">Cela peut entraîner des difficultés.</span><span class="sxs-lookup"><span data-stu-id="7784b-129">This may cause difficulties.</span></span> | <span data-ttu-id="7784b-130">La définition de la propriété [**REINSTALLMODE**](reinstallmode.md) dans le fichier. msi peut entraîner un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="7784b-130">Defining the [**REINSTALLMODE**](reinstallmode.md) property in .msi file can lead to unexpected behavior.</span></span> <span data-ttu-id="7784b-131">Pour corriger cette erreur, ne définissez pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="7784b-131">To fix this error, do not define this property.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7784b-132">L’entrée RemoveIniFile Remove1 doit avoir une valeur, car l’action est « supprimer la balise » (4).</span><span class="sxs-lookup"><span data-stu-id="7784b-132">RemoveIniFile entry Remove1 must have a value, because the Action is "Delete Tag" (4).</span></span>                | <span data-ttu-id="7784b-133">Il existe une action supprimer la balise dans la colonne RemoveIniFile de la [table RemoveIniFile](removeinifile-table.md) sans spécifier de balise à supprimer dans la colonne valeur.</span><span class="sxs-lookup"><span data-stu-id="7784b-133">There is a Delete Tag action in the in the RemoveIniFile column of the [RemoveIniFile table](removeinifile-table.md) without specifying a tag to delete in the Value column.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7784b-134">La table d’erreurs est manquante.</span><span class="sxs-lookup"><span data-stu-id="7784b-134">Error Table is missing.</span></span> <span data-ttu-id="7784b-135">Seuls les messages d’erreur numériques seront générés.</span><span class="sxs-lookup"><span data-stu-id="7784b-135">Only numerical error messages will be generated.</span></span>                              | <span data-ttu-id="7784b-136">Cet avertissement ICE est obsolète, car Windows Installer ne requiert pas que le package ait une [table d’erreurs](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="7784b-136">This ICE warning is obsolete because Windows Installer does not require the package to have an [Error table](error-table.md).</span></span> <span data-ttu-id="7784b-137">Les messages d’erreur peuvent être récupérés à l’aide de Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="7784b-137">Error messages can be retrieved using Msimsg.dll.</span></span><br/> <span data-ttu-id="7784b-138">Cet avertissement signifie que la [table d’erreurs](error-table.md) est manquante dans le fichier. msi et que la propriété de résumé du [**nombre de pages**](page-count-summary.md) est inférieure ou égale à 100.</span><span class="sxs-lookup"><span data-stu-id="7784b-138">This warning means that the .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <br/> <span data-ttu-id="7784b-139">Pour corriger cette erreur, utilisez une version actuelle du Windows Installer ou ajoutez une table d’erreurs au package d’installation et créez des modèles de mise en forme dans la colonne message pour les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7784b-139">To fix this error, use a current version of the Windows Installer, or add an Error table to the installation package and author formatting templates in the Message column for error messages.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7784b-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7784b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7784b-141">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="7784b-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




