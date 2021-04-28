---
title: Exemple CustomAccServer
description: Exemple CustomAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088007"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="ba531-103">Exemple CustomAccServer</span><span class="sxs-lookup"><span data-stu-id="ba531-103">CustomAccServer Sample</span></span>

<span data-ttu-id="ba531-104">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba531-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ba531-105">Description</span><span class="sxs-lookup"><span data-stu-id="ba531-105">Description</span></span>](#description)
-   [<span data-ttu-id="ba531-106">Informations sur le téléchargement</span><span class="sxs-lookup"><span data-stu-id="ba531-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="ba531-107">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="ba531-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="ba531-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ba531-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ba531-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ba531-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="ba531-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba531-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="ba531-111">Description</span><span class="sxs-lookup"><span data-stu-id="ba531-111">Description</span></span>

<span data-ttu-id="ba531-112">Cet exemple montre comment implémenter un serveur Microsoft Active Accessibility pour un contrôle personnalisé simple.</span><span class="sxs-lookup"><span data-stu-id="ba531-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="ba531-113">L’objet accessible pour le contrôle se compose de l’élément racine (une zone de liste) et de ses enfants (les éléments de liste).</span><span class="sxs-lookup"><span data-stu-id="ba531-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="ba531-114">Informations sur le téléchargement</span><span class="sxs-lookup"><span data-stu-id="ba531-114">Download Information</span></span>

<span data-ttu-id="ba531-115">L’exemple CustomAccServer est installé dans le cadre du [Kit de développement logiciel (SDK) Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) et est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="ba531-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="ba531-116">Emplacement</span><span class="sxs-lookup"><span data-stu-id="ba531-116">Location</span></span>    | <span data-ttu-id="ba531-117">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="ba531-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba531-118">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="ba531-118">Windows SDK</span></span> | <span data-ttu-id="ba531-119">% Program Files% \\ Microsoft SDK \\ \\ \[ numéro de version Windows exemples d' \] \\ exemples d' \\ WinUI \\ MSAA</span><span class="sxs-lookup"><span data-stu-id="ba531-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="ba531-120">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="ba531-120">Minimum Requirements</span></span>



| <span data-ttu-id="ba531-121">Produit</span><span class="sxs-lookup"><span data-stu-id="ba531-121">Product</span></span>          | <span data-ttu-id="ba531-122">Version</span><span class="sxs-lookup"><span data-stu-id="ba531-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="ba531-123">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ba531-123">Operating System</span></span> | <span data-ttu-id="ba531-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba531-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="ba531-125">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="ba531-125">Windows SDK</span></span>      | <span data-ttu-id="ba531-126">7.0</span><span class="sxs-lookup"><span data-stu-id="ba531-126">7.0</span></span>                             |
| <span data-ttu-id="ba531-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ba531-127">Visual Studio</span></span>    | <span data-ttu-id="ba531-128">2008</span><span class="sxs-lookup"><span data-stu-id="ba531-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="ba531-129">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ba531-129">Building the Sample</span></span>

<span data-ttu-id="ba531-130">Pour générer l’exemple à l’aide de Visual Studio 2008 :</span><span class="sxs-lookup"><span data-stu-id="ba531-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="ba531-131">Exécutez l’outil de configuration du kit de développement logiciel (SDK) Microsoft Windows fourni avec le kit de développement logiciel (SDK) pour ajouter des répertoires Include SDK à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ba531-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="ba531-132">Ouvrez l’Explorateur Windows et accédez au répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="ba531-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="ba531-133">Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ba531-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="ba531-134">Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution.</span><span class="sxs-lookup"><span data-stu-id="ba531-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="ba531-135">L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .</span><span class="sxs-lookup"><span data-stu-id="ba531-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="ba531-136">Pour générer l’exemple à partir de la ligne de commande, consultez génération d’exemples dans les notes de publication de SDK Windows à l’emplacement suivant :% Program Files% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="ba531-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ba531-137">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ba531-137">Running the Sample</span></span>

<span data-ttu-id="ba531-138">Pour exécuter l’exemple :</span><span class="sxs-lookup"><span data-stu-id="ba531-138">To run the sample:</span></span>

1.  <span data-ttu-id="ba531-139">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="ba531-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="ba531-140">Tapez AccServer.exe sur la ligne de commande ou double-cliquez sur l’icône de AccServer.exe pour le lancer à partir de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="ba531-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="ba531-141">Pour exécuter à partir de Visual Studio, appuyez sur F5 ou cliquez sur **Démarrer le débogage** dans le menu **Déboguer** .</span><span class="sxs-lookup"><span data-stu-id="ba531-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba531-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba531-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba531-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="ba531-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




