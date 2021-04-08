---
description: L’exemple de code PropertyEdit montre comment convertir le nom de propriété canonique en PROPERTYKEY, définir la valeur de la Banque de propriétés sur celle de l’élément, puis réécrire les données dans le flux de fichier.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862166"
---
# <a name="propertyedit"></a><span data-ttu-id="1e834-103">PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="1e834-103">PropertyEdit</span></span>

<span data-ttu-id="1e834-104">L’exemple de code PropertyEdit montre comment convertir le nom de propriété canonique en PROPERTYKEY, définir la valeur de la Banque de propriétés sur celle de l’élément, puis réécrire les données dans le flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e834-104">The PropertyEdit code sample demonstrates how to convert the canonical property name to a PROPERTYKEY, set the value of the property store to that of the item, and write the data back to the file stream.</span></span>

<span data-ttu-id="1e834-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e834-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1e834-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e834-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1e834-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1e834-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="1e834-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1e834-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="1e834-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1e834-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="1e834-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e834-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="1e834-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e834-111">Requirements</span></span>



| <span data-ttu-id="1e834-112">Produit</span><span class="sxs-lookup"><span data-stu-id="1e834-112">Product</span></span>     | <span data-ttu-id="1e834-113">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="1e834-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="1e834-114">Windows</span><span class="sxs-lookup"><span data-stu-id="1e834-114">Windows</span></span>     | <span data-ttu-id="1e834-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e834-115">Windows 7</span></span>               |
| <span data-ttu-id="1e834-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="1e834-116">Windows SDK</span></span> | <span data-ttu-id="1e834-117">7.0</span><span class="sxs-lookup"><span data-stu-id="1e834-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1e834-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1e834-118">Downloading the Sample</span></span>

<span data-ttu-id="1e834-119">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="1e834-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="1e834-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="1e834-120">Location</span></span>      | <span data-ttu-id="1e834-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="1e834-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="1e834-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="1e834-122">GitHub</span></span>  | [<span data-ttu-id="1e834-123">Exemple PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="1e834-123">PropertyEdit sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> <span data-ttu-id="1e834-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="1e834-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="1e834-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1e834-125">Building the Sample</span></span>

<span data-ttu-id="1e834-126">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="1e834-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="1e834-127">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="1e834-127">Open the Command Prompt window and navigate to the **PropertyEdit** project directory.</span></span> 
2.  <span data-ttu-id="1e834-128">Entrez `msbuild PropertyEdit.sln`.</span><span class="sxs-lookup"><span data-stu-id="1e834-128">Enter `msbuild PropertyEdit.sln`.</span></span>

<span data-ttu-id="1e834-129">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="1e834-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="1e834-130">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="1e834-130">Open Windows Explorer and navigate to the **PropertyEdit** project directory.</span></span>
2.  <span data-ttu-id="1e834-131">Double-cliquez sur l’icône du fichier PropertyEdit. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1e834-131">Double-click the icon for the PropertyEdit.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="1e834-132">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e834-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="1e834-133">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="1e834-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="1e834-134">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="1e834-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="1e834-135">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1e834-135">Running the Sample</span></span>

1.  <span data-ttu-id="1e834-136">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="1e834-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="1e834-137">À l’invite de commandes, entrez `PropertyEdit.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de PropertyEdit.exe.</span><span class="sxs-lookup"><span data-stu-id="1e834-137">At the command prompt, enter `PropertyEdit.exe`, or from Windows Explorer, double-click the icon for PropertyEdit.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e834-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e834-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1e834-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1e834-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e834-140">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="1e834-140">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="1e834-141">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="1e834-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1e834-142">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="1e834-142">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[<span data-ttu-id="1e834-143">À propos des propriétés et gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="1e834-143">About Properties and Property Handlers</span></span>](../properties/building-property-handlers-properties.md)
</dt> <dt>

<span data-ttu-id="1e834-144">[Schéma de la description de propriété](/previous-versions//cc144127(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e834-144">[Property Description Schema](/previous-versions//cc144127(v=vs.85))</span></span>
</dt> </dl>

 

 
