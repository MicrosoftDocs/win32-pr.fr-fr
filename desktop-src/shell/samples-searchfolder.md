---
description: Montre comment créer une recherche avec des contraintes de requête à l’aide du modèle de programmation de l’interpréteur de commandes.
title: Recherche dans un dossier, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: DF3432AB-39DF-44c6-9A08-4630408D6B9B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c86a29c4a7d01fad3b91db20035cb84751e0b78a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203824"
---
# <a name="search-folder-sample"></a><span data-ttu-id="3a093-103">Recherche dans un dossier, exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-103">Search Folder Sample</span></span>

<span data-ttu-id="3a093-104">Montre comment créer une recherche avec des contraintes de requête à l’aide du modèle de programmation de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="3a093-104">Demonstrates how to create a search with query constraints using the Shell programming model.</span></span>

<span data-ttu-id="3a093-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a093-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a093-106">Description</span><span class="sxs-lookup"><span data-stu-id="3a093-106">Description</span></span>](#description)
-   [<span data-ttu-id="3a093-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a093-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3a093-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3a093-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3a093-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="3a093-111">Description</span><span class="sxs-lookup"><span data-stu-id="3a093-111">Description</span></span>

<span data-ttu-id="3a093-112">Cet exemple montre comment créer une recherche avec restriction à l’aide de l’interface [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) pour construire un élément de Shell de dossier (un conteneur) qui représente la requête.</span><span class="sxs-lookup"><span data-stu-id="3a093-112">This sample shows how to create a constrained search by using the [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) interface to construct a folder Shell item (a container) that represents the query.</span></span> <span data-ttu-id="3a093-113">Les résultats s’affichent à l’aide de la boîte de dialogue Ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="3a093-113">The results are displayed using the file open dialog.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a093-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a093-114">Requirements</span></span>



| <span data-ttu-id="3a093-115">Produit</span><span class="sxs-lookup"><span data-stu-id="3a093-115">Product</span></span>                                | <span data-ttu-id="3a093-116">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="3a093-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3a093-117">Windows</span><span class="sxs-lookup"><span data-stu-id="3a093-117">Windows</span></span>                                | <span data-ttu-id="3a093-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a093-118">Windows Vista</span></span>           |
| <span data-ttu-id="3a093-119">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="3a093-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3a093-120">7.0</span><span class="sxs-lookup"><span data-stu-id="3a093-120">7.0</span></span>                     |



 

<span data-ttu-id="3a093-121">Pour obtenir des spécifications supplémentaires, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="3a093-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3a093-122">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-122">Downloading the Sample</span></span>

| <span data-ttu-id="3a093-123">Emplacement</span><span class="sxs-lookup"><span data-stu-id="3a093-123">Location</span></span>      | <span data-ttu-id="3a093-124">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="3a093-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a093-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="3a093-125">GitHub</span></span>  | [<span data-ttu-id="3a093-126">SearchFolder, exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-126">SearchFolder sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/searchfolder) |

## <a name="building-the-sample"></a><span data-ttu-id="3a093-127">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-127">Building the Sample</span></span>

<span data-ttu-id="3a093-128">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="3a093-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3a093-129">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a093-129">Running the Sample</span></span>

<span data-ttu-id="3a093-130">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="3a093-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



