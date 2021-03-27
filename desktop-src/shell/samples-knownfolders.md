---
description: Montre comment définir, inscrire, énumérer et rechercher le chemin d’accès pour tous les dossiers connus sur le système actuel.
title: Dossiers connus, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 49799A9E-BA86-4977-B5F3-590BE1E5FBF6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d3784e64986a338f6554534199852191bd06ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952244"
---
# <a name="known-folders-sample"></a><span data-ttu-id="746f4-103">Dossiers connus, exemple</span><span class="sxs-lookup"><span data-stu-id="746f4-103">Known Folders Sample</span></span>

<span data-ttu-id="746f4-104">Montre comment définir, inscrire, énumérer et rechercher le chemin d’accès pour tous les dossiers connus sur le système actuel.</span><span class="sxs-lookup"><span data-stu-id="746f4-104">Demonstrates how to define, register, enumerate and find the path for all known folders on the current system.</span></span>

<span data-ttu-id="746f4-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="746f4-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="746f4-106">Description</span><span class="sxs-lookup"><span data-stu-id="746f4-106">Description</span></span>](#description)
-   [<span data-ttu-id="746f4-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="746f4-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="746f4-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="746f4-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="746f4-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="746f4-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="746f4-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="746f4-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="746f4-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="746f4-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="746f4-112">Description</span><span class="sxs-lookup"><span data-stu-id="746f4-112">Description</span></span>

<span data-ttu-id="746f4-113">Cet exemple comprend un fichier de Registre qui montre comment inscrire un dossier connu en écrivant des clés et des valeurs de Registre communes pour les développeurs qui préfèrent l’accès au registre.</span><span class="sxs-lookup"><span data-stu-id="746f4-113">This sample includes a registry file that demonstrates how to register a known folder by writing some common registry keys and values for developers who prefer registry access.</span></span>

## <a name="requirements"></a><span data-ttu-id="746f4-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="746f4-114">Requirements</span></span>



| <span data-ttu-id="746f4-115">Produit</span><span class="sxs-lookup"><span data-stu-id="746f4-115">Product</span></span>                                | <span data-ttu-id="746f4-116">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="746f4-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="746f4-117">Windows</span><span class="sxs-lookup"><span data-stu-id="746f4-117">Windows</span></span>                                | <span data-ttu-id="746f4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="746f4-118">Windows Vista</span></span>           |
| <span data-ttu-id="746f4-119">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="746f4-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="746f4-120">6.1</span><span class="sxs-lookup"><span data-stu-id="746f4-120">6.1</span></span>                     |



 

<span data-ttu-id="746f4-121">Pour obtenir des spécifications supplémentaires, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="746f4-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="746f4-122">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="746f4-122">Downloading the Sample</span></span>

| <span data-ttu-id="746f4-123">Emplacement</span><span class="sxs-lookup"><span data-stu-id="746f4-123">Location</span></span>      | <span data-ttu-id="746f4-124">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="746f4-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="746f4-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="746f4-125">GitHub</span></span>  | [<span data-ttu-id="746f4-126">Exemple fichier KnownFolders</span><span class="sxs-lookup"><span data-stu-id="746f4-126">KnownFolders sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/knownfolders) |

## <a name="building-the-sample"></a><span data-ttu-id="746f4-127">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="746f4-127">Building the Sample</span></span>

<span data-ttu-id="746f4-128">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="746f4-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="746f4-129">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="746f4-129">Running the Sample</span></span>

<span data-ttu-id="746f4-130">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="746f4-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="746f4-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="746f4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="746f4-132">Dossiers connus</span><span class="sxs-lookup"><span data-stu-id="746f4-132">Known Folders</span></span>](known-folders.md)
</dt> </dl>

 

 



