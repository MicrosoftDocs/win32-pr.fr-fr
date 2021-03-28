---
description: Montre comment contrôler le comportement de regroupement de la barre des tâches des fenêtres d’une application par le biais de la propriété System.AppUserModel.ID.
title: Propriété de fenêtre d’ID de modèle d’utilisateur d’application, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973543"
---
# <a name="application-user-model-id-appid-window-property-sample"></a><span data-ttu-id="ea912-103">Exemple de propriété de fenêtre AppID (application User Model ID)</span><span class="sxs-lookup"><span data-stu-id="ea912-103">Application User Model ID (AppID) Window Property Sample</span></span>

<span data-ttu-id="ea912-104">Montre comment contrôler le comportement de regroupement de la barre des tâches des fenêtres d’une application par le biais de la propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="ea912-104">Demonstrates how to control the taskbar grouping behavior of an application's windows through the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property.</span></span>

<span data-ttu-id="ea912-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea912-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ea912-106">Description</span><span class="sxs-lookup"><span data-stu-id="ea912-106">Description</span></span>](#description)
-   [<span data-ttu-id="ea912-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea912-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ea912-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ea912-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ea912-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ea912-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ea912-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ea912-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="ea912-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea912-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="ea912-112">Description</span><span class="sxs-lookup"><span data-stu-id="ea912-112">Description</span></span>

<span data-ttu-id="ea912-113">Cet exemple montre comment définir la propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) à l’aide de l’implémentation [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de la fenêtre, obtenue par le biais de [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span><span class="sxs-lookup"><span data-stu-id="ea912-113">This sample shows how to set the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property through the use of the window's [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, which is obtained through [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea912-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea912-114">Requirements</span></span>



| <span data-ttu-id="ea912-115">Produit</span><span class="sxs-lookup"><span data-stu-id="ea912-115">Product</span></span>                                | <span data-ttu-id="ea912-116">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="ea912-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="ea912-117">Windows</span><span class="sxs-lookup"><span data-stu-id="ea912-117">Windows</span></span>                                | <span data-ttu-id="ea912-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea912-118">Windows 7</span></span>               |
| <span data-ttu-id="ea912-119">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="ea912-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="ea912-120">7.0</span><span class="sxs-lookup"><span data-stu-id="ea912-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ea912-121">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ea912-121">Downloading the Sample</span></span>

| <span data-ttu-id="ea912-122">Emplacement</span><span class="sxs-lookup"><span data-stu-id="ea912-122">Location</span></span>      | <span data-ttu-id="ea912-123">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="ea912-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea912-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="ea912-124">GitHub</span></span>  | [<span data-ttu-id="ea912-125">Exemple AppUserModelIDWindowProperty</span><span class="sxs-lookup"><span data-stu-id="ea912-125">AppUserModelIDWindowProperty sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a><span data-ttu-id="ea912-126">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ea912-126">Building the Sample</span></span>

<span data-ttu-id="ea912-127">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="ea912-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="ea912-128">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="ea912-128">Open the command prompt window and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="ea912-129">Entrez `msbuild AppUserModelIDWindowProperty.sln`.</span><span class="sxs-lookup"><span data-stu-id="ea912-129">Enter `msbuild AppUserModelIDWindowProperty.sln`.</span></span>

<span data-ttu-id="ea912-130">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="ea912-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="ea912-131">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="ea912-131">Open Windows Explorer and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="ea912-132">Double-cliquez sur l’icône du fichier AppUserModelIDWindowProperty. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ea912-132">Double-click the icon for the AppUserModelIDWindowProperty.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="ea912-133">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="ea912-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ea912-134">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ea912-134">Running the Sample</span></span>

1.  <span data-ttu-id="ea912-135">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="ea912-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="ea912-136">Sur la ligne de commande, entrez `AppUserModelIDWindowProperty.exe` .</span><span class="sxs-lookup"><span data-stu-id="ea912-136">At the command line, enter `AppUserModelIDWindowProperty.exe`.</span></span> <span data-ttu-id="ea912-137">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de AppUserModelIDWindowProperty.exe.</span><span class="sxs-lookup"><span data-stu-id="ea912-137">Alternatively, from Windows Explorer double-click the icon for AppUserModelIDWindowProperty.exe.</span></span>
3.  <span data-ttu-id="ea912-138">Pour illustrer l’effet des ID de modèle utilisateur de l’application (AppUserModelIDs) sur le regroupement de la barre des tâches, lancez au moins trois instances de l’application en même temps.</span><span class="sxs-lookup"><span data-stu-id="ea912-138">To demonstrate the effect Application User Model IDs (AppUserModelIDs) have on taskbar grouping, launch at least three instances of the application at the same time.</span></span>
4.  <span data-ttu-id="ea912-139">Utilisez le menu pour définir une valeur AppUserModelID différente sur chacune des trois fenêtres.</span><span class="sxs-lookup"><span data-stu-id="ea912-139">Use the menu to set a different AppUserModelID on each of the three windows.</span></span> <span data-ttu-id="ea912-140">Notez que chaque AppUserModelID distincte produit un bouton distinct de la barre des tâches et que Windows peut modifier son identité au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ea912-140">Notice that each separate AppUserModelID results in a separate taskbar button and that windows can change their identity at runtime.</span></span>
5.  <span data-ttu-id="ea912-141">Définissez au moins deux fenêtres à la seconde AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="ea912-141">Set at least two windows to the second AppUserModelID.</span></span> <span data-ttu-id="ea912-142">Notez qu’ils se déplacent tous deux dans le même groupe de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="ea912-142">Notice that they both move into the same taskbar group.</span></span>
6.  <span data-ttu-id="ea912-143">Ouvrez la fenêtre **des propriétés de la barre des tâches et du menu Démarrer** en cliquant avec le bouton droit sur la barre des tâches et en sélectionnant **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ea912-143">Open the **Taskbar and Start Menu Properties** window by right-clicking the taskbar and selecting **Properties** in the context menu.</span></span> <span data-ttu-id="ea912-144">Modifiez les **boutons de la barre des tâches :** liste déroulante entre la **combinaison lorsque la barre des tâches est complète** et **ne jamais combiner** les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ea912-144">Change the **Taskbar buttons:** drop-down between the **Combine when taskbar is full** and **Never combine** values.</span></span> <span data-ttu-id="ea912-145">Notez que chaque fenêtre peut obtenir un bouton distinct, mais que les boutons sont regroupés par AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="ea912-145">Notice that each window can get a separate button, but that the buttons are grouped by AppUserModelID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea912-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea912-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea912-147">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="ea912-147">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
