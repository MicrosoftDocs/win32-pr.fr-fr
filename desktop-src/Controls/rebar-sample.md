---
title: Rebar, exemple
ms.assetid: f26c0819-523d-42a5-be2f-3cd75748b4a6
description: 'En savoir plus sur : rebar, exemple'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72b58a66c22b0ef8cc60d97c0965a8ae29a20fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950443"
---
# <a name="rebar-sample"></a><span data-ttu-id="3ca52-103">Rebar, exemple</span><span class="sxs-lookup"><span data-stu-id="3ca52-103">Rebar Sample</span></span>

<span data-ttu-id="3ca52-104">Cette rubrique décrit l’exemple de code Rebar.</span><span class="sxs-lookup"><span data-stu-id="3ca52-104">This topic describes the Rebar Sample code sample.</span></span> <span data-ttu-id="3ca52-105">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ca52-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="3ca52-106">Description</span><span class="sxs-lookup"><span data-stu-id="3ca52-106">Description</span></span>](#description)
-   [<span data-ttu-id="3ca52-107">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="3ca52-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="3ca52-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3ca52-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3ca52-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3ca52-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3ca52-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ca52-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="3ca52-111">Description</span><span class="sxs-lookup"><span data-stu-id="3ca52-111">Description</span></span>

<span data-ttu-id="3ca52-112">L’exemple Rebar montre comment implémenter un contrôle commun Rebar simple dans une application.</span><span class="sxs-lookup"><span data-stu-id="3ca52-112">The Rebar Sample shows how to implement a simple rebar common control in an application.</span></span> <span data-ttu-id="3ca52-113">Cet exemple crée un contrôle rebar avec deux bandes.</span><span class="sxs-lookup"><span data-stu-id="3ca52-113">This example creates a rebar control that has two bands.</span></span> <span data-ttu-id="3ca52-114">L’un contient une zone de liste déroulante et l’autre contient un bouton de commande.</span><span class="sxs-lookup"><span data-stu-id="3ca52-114">One contains a combo box and the other contains a push button.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="3ca52-115">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="3ca52-115">Minimum Requirements</span></span>



| <span data-ttu-id="3ca52-116">Produit</span><span class="sxs-lookup"><span data-stu-id="3ca52-116">Product</span></span>          | <span data-ttu-id="3ca52-117">Version</span><span class="sxs-lookup"><span data-stu-id="3ca52-117">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="3ca52-118">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca52-118">DLL</span></span>              | <span data-ttu-id="3ca52-119">comctl32.dll version 4,71</span><span class="sxs-lookup"><span data-stu-id="3ca52-119">comctl32.dll version 4.71</span></span>             |
| <span data-ttu-id="3ca52-120">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3ca52-120">Operating System</span></span> | <span data-ttu-id="3ca52-121">Windows 95 avec Internet Explorer 4,0</span><span class="sxs-lookup"><span data-stu-id="3ca52-121">Windows 95 with Internet Explorer 4.0</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3ca52-122">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3ca52-122">Downloading the Sample</span></span>

<span data-ttu-id="3ca52-123">L’exemple Rebar est installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx) et est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="3ca52-123">The Rebar Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="3ca52-124">Emplacement</span><span class="sxs-lookup"><span data-stu-id="3ca52-124">Location</span></span>    | <span data-ttu-id="3ca52-125">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="3ca52-125">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca52-126">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="3ca52-126">Windows SDK</span></span> | <span data-ttu-id="3ca52-127">% Program Files% \\ Microsoft SDK \\ \\ \[ numéro de version Windows exemples d’exemples de \] \\ \\ contrôle WinUI contrôles d’WinUI \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3ca52-127">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\rebar</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="3ca52-128">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3ca52-128">Building the Sample</span></span>

<span data-ttu-id="3ca52-129">Pour générer l’exemple à l’aide de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="3ca52-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="3ca52-130">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="3ca52-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="3ca52-131">Entrez `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="3ca52-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="3ca52-132">Pour générer l’exemple à l’aide de Visual Studio :</span><span class="sxs-lookup"><span data-stu-id="3ca52-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="3ca52-133">Ouvrez l’Explorateur Windows et accédez au répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="3ca52-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="3ca52-134">Double-cliquez sur l’icône du fichier. vcproj pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3ca52-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="3ca52-135">Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution.</span><span class="sxs-lookup"><span data-stu-id="3ca52-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ca52-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ca52-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ca52-137">Contrôles Rebar</span><span class="sxs-lookup"><span data-stu-id="3ca52-137">Rebar Controls</span></span>](rebar-controls.md)
</dt> </dl>

 

 




