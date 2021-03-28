---
description: Montre comment énumérer les bibliothèques en tant que conteneurs.
title: Sauvegarde de bibliothèque Shell, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 206356B2-3998-4a19-BC4D-F6A043AFDBD3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e1b4746d2e559b567adb4cbd2305ea474b03129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973751"
---
# <a name="shell-library-backup-sample"></a><span data-ttu-id="705ec-103">Sauvegarde de bibliothèque Shell, exemple</span><span class="sxs-lookup"><span data-stu-id="705ec-103">Shell Library Backup Sample</span></span>

<span data-ttu-id="705ec-104">Montre comment énumérer les bibliothèques en tant que conteneurs.</span><span class="sxs-lookup"><span data-stu-id="705ec-104">Demonstrates how to enumerate libraries as containers.</span></span> <span data-ttu-id="705ec-105">Les bibliothèques sont le nouveau paradigme de stockage pour les fichiers utilisateur et sont introduits dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="705ec-105">Libraries are the new storage paradigm for user files and are introduced in Windows 7.</span></span>

<span data-ttu-id="705ec-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="705ec-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="705ec-107">Description</span><span class="sxs-lookup"><span data-stu-id="705ec-107">Description</span></span>](#description)
-   [<span data-ttu-id="705ec-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="705ec-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="705ec-109">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="705ec-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="705ec-110">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="705ec-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="705ec-111">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="705ec-111">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="705ec-112">Description</span><span class="sxs-lookup"><span data-stu-id="705ec-112">Description</span></span>

<span data-ttu-id="705ec-113">Cet exemple est une application de sauvegarde fictive qui montre comment sélectionner des bibliothèques dans la boîte de dialogue de fichier commune.</span><span class="sxs-lookup"><span data-stu-id="705ec-113">This sample is a fictional backup application that shows how to pick libraries through the common file dialog.</span></span> <span data-ttu-id="705ec-114">Il montre également comment sauvegarder des bibliothèques à l’aide de l’Explorateur d’espaces de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="705ec-114">It also demonstrates how to back up libraries using the Shell namespace walker.</span></span>

## <a name="requirements"></a><span data-ttu-id="705ec-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="705ec-115">Requirements</span></span>



| <span data-ttu-id="705ec-116">Produit</span><span class="sxs-lookup"><span data-stu-id="705ec-116">Product</span></span>                                | <span data-ttu-id="705ec-117">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="705ec-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="705ec-118">Windows</span><span class="sxs-lookup"><span data-stu-id="705ec-118">Windows</span></span>                                | <span data-ttu-id="705ec-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="705ec-119">Windows 7</span></span>               |
| <span data-ttu-id="705ec-120">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="705ec-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="705ec-121">7.0</span><span class="sxs-lookup"><span data-stu-id="705ec-121">7.0</span></span>                     |



 

<span data-ttu-id="705ec-122">Pour obtenir des spécifications supplémentaires, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="705ec-122">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="705ec-123">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="705ec-123">Downloading the Sample</span></span>

| <span data-ttu-id="705ec-124">Emplacement</span><span class="sxs-lookup"><span data-stu-id="705ec-124">Location</span></span>      | <span data-ttu-id="705ec-125">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="705ec-125">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705ec-126">GitHub</span><span class="sxs-lookup"><span data-stu-id="705ec-126">GitHub</span></span>  | [<span data-ttu-id="705ec-127">Exemple ShellLibraryBackup</span><span class="sxs-lookup"><span data-stu-id="705ec-127">ShellLibraryBackup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryBackup) |

## <a name="building-the-sample"></a><span data-ttu-id="705ec-128">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="705ec-128">Building the Sample</span></span>

<span data-ttu-id="705ec-129">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="705ec-129">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="705ec-130">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="705ec-130">Running the Sample</span></span>

<span data-ttu-id="705ec-131">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="705ec-131">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



