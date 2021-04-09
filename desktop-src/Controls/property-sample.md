---
title: Exemple de propriété
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'En savoir plus sur : exemple de propriété'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110151"
---
# <a name="property-sample"></a><span data-ttu-id="b53da-103">Exemple de propriété</span><span class="sxs-lookup"><span data-stu-id="b53da-103">Property Sample</span></span>

<span data-ttu-id="b53da-104">Cette rubrique décrit l’exemple de code de propriété.</span><span class="sxs-lookup"><span data-stu-id="b53da-104">This topic describes the Property Sample code sample.</span></span> <span data-ttu-id="b53da-105">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="b53da-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="b53da-106">Description</span><span class="sxs-lookup"><span data-stu-id="b53da-106">Description</span></span>](#description)
-   [<span data-ttu-id="b53da-107">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="b53da-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="b53da-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b53da-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b53da-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b53da-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b53da-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b53da-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b53da-111">Description</span><span class="sxs-lookup"><span data-stu-id="b53da-111">Description</span></span>

<span data-ttu-id="b53da-112">L’exemple de propriété montre comment implémenter trois styles différents de feuilles de propriétés : modal, non modal et Assistant.</span><span class="sxs-lookup"><span data-stu-id="b53da-112">The Property Sample shows how to implement three different styles of property sheets: modal, modeless, and wizard.</span></span> <span data-ttu-id="b53da-113">Il montre également comment utiliser la fonction [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) pour modifier la boîte de dialogue de la feuille de propriétés avant ou après sa création.</span><span class="sxs-lookup"><span data-stu-id="b53da-113">It also shows how to use the [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) function to modify the property sheet dialog before or after it is created.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="b53da-114">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="b53da-114">Minimum Requirements</span></span>



| <span data-ttu-id="b53da-115">Produit</span><span class="sxs-lookup"><span data-stu-id="b53da-115">Product</span></span>          | <span data-ttu-id="b53da-116">Version</span><span class="sxs-lookup"><span data-stu-id="b53da-116">Version</span></span>                              |
|------------------|--------------------------------------|
| <span data-ttu-id="b53da-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b53da-117">DLL</span></span>              | <span data-ttu-id="b53da-118">comctl32.dll version 4,0</span><span class="sxs-lookup"><span data-stu-id="b53da-118">comctl32.dll version 4.0</span></span>             |
| <span data-ttu-id="b53da-119">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b53da-119">Operating System</span></span> | <span data-ttu-id="b53da-120">Windows 95, Microsoft Windows NT 3,1</span><span class="sxs-lookup"><span data-stu-id="b53da-120">Windows 95, Microsoft Windows NT 3.1</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b53da-121">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b53da-121">Downloading the Sample</span></span>

<span data-ttu-id="b53da-122">L’exemple de propriété est installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx) et est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="b53da-122">The Property Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="b53da-123">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b53da-123">Location</span></span>    | <span data-ttu-id="b53da-124">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="b53da-124">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b53da-125">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="b53da-125">Windows SDK</span></span> | <span data-ttu-id="b53da-126">% Program Files% \\ Microsoft SDK \\ \\ \[ numéro de version Windows exemples d’exemples de \] \\ \\ \\ contrôle WinUI \\ \\ propriété commune</span><span class="sxs-lookup"><span data-stu-id="b53da-126">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\property</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="b53da-127">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b53da-127">Building the Sample</span></span>

<span data-ttu-id="b53da-128">Pour générer l’exemple à l’aide de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="b53da-128">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="b53da-129">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="b53da-129">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="b53da-130">Entrez `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="b53da-130">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="b53da-131">Pour générer l’exemple à l’aide de Visual Studio :</span><span class="sxs-lookup"><span data-stu-id="b53da-131">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="b53da-132">Ouvrez l’Explorateur Windows et accédez au répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="b53da-132">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="b53da-133">Double-cliquez sur l’icône du fichier. vcproj pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b53da-133">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="b53da-134">Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution.</span><span class="sxs-lookup"><span data-stu-id="b53da-134">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b53da-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b53da-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b53da-136">À propos des feuilles de propriétés</span><span class="sxs-lookup"><span data-stu-id="b53da-136">About Property Sheets</span></span>](property-sheets.md)
</dt> </dl>

 

 




