---
description: La bibliothèque de fichiers remplace le dossier de documents
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La bibliothèque de fichiers remplace le dossier de documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699c645d574012a419f77538bcc58d61a4938120
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088377"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="ae1e7-103">La bibliothèque de fichiers remplace le dossier de documents</span><span class="sxs-lookup"><span data-stu-id="ae1e7-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ae1e7-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="ae1e7-104">Affected Platforms</span></span>

<span data-ttu-id="ae1e7-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae1e7-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="ae1e7-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae1e7-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="ae1e7-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ae1e7-107">Feature Impact</span></span>

<span data-ttu-id="ae1e7-108">**Gravité** -moyenne</span><span class="sxs-lookup"><span data-stu-id="ae1e7-108">**Severity** - Medium</span></span>  
<span data-ttu-id="ae1e7-109">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="ae1e7-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="ae1e7-110">Description</span><span class="sxs-lookup"><span data-stu-id="ae1e7-110">Description</span></span>

<span data-ttu-id="ae1e7-111">Les bibliothèques fournissent une expérience de type dossier centralisé pour le stockage des fichiers, la recherche et l’accès à plusieurs emplacements, à la fois locaux et distants.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="ae1e7-112">Les emplacements par défaut utilisés par les boîtes de dialogue de fichier courantes (par exemple, ouvrir et enregistrer) ont été modifiés depuis le dossier de documents vers la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="ae1e7-113">L’interface utilisateur est inchangée, mais l’utilisateur peut désormais afficher, parcourir et rechercher la bibliothèque à l’aide de plusieurs vues de la structure.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="ae1e7-114">Les fichiers sont enregistrés dans l’emplacement d’enregistrement par défaut de la bibliothèque, sauf si l’utilisateur modifie l’emplacement d’enregistrement par défaut ou choisit un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="ae1e7-115">Les développeurs peuvent créer leurs propres bibliothèques ou ajouter des emplacements à des bibliothèques existantes à l’aide de l’interface IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="ae1e7-116">Les utilisateurs peuvent rechercher des bibliothèques à l’aide du système de dossiers connu (par exemple, FOLDERID \_ DocumentsLibrary).</span><span class="sxs-lookup"><span data-stu-id="ae1e7-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="ae1e7-117">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="ae1e7-117">Manifestation of Impact</span></span>

<span data-ttu-id="ae1e7-118">La bibliothèque est elle-même un fichier et non un dossier.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="ae1e7-119">Par conséquent, les manipulations de chemin d’accès peuvent entraîner des erreurs en raison de la tentative de concaténation des fichiers par l’application pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="ae1e7-120">Solution</span><span class="sxs-lookup"><span data-stu-id="ae1e7-120">Solution</span></span>

<span data-ttu-id="ae1e7-121">Lorsque vous utilisez IFileDialog, vous devez utiliser la méthode GetResult au lieu de la combinaison de GetFolder et GetFilename, comme vous le feriez dans les versions précédentes du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="ae1e7-122">Utilisez les API de l’interpréteur de commandes dans la mesure du possible pour interagir avec et manipuler des éléments dans l’espace de noms Shell (par exemple, IShellItem).</span><span class="sxs-lookup"><span data-stu-id="ae1e7-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="ae1e7-123">Exploitation des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ae1e7-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="ae1e7-124">Si vous souhaitez créer vos propres bibliothèques ou ajouter des emplacements à des bibliothèques existantes, vous devez utiliser l’API IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="ae1e7-125">Les bibliothèques sont elles-mêmes des dossiers Shell, ce qui vous permet de les énumérer comme n’importe quel autre dossier shell.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="ae1e7-126">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="ae1e7-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="ae1e7-127">À l’aide de la boîte de dialogue fichier commun, vous pouvez vous assurer que les utilisateurs peuvent enregistrer directement dans leurs bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="ae1e7-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ae1e7-128">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="ae1e7-128">Links to Other Resources</span></span>

-   <span data-ttu-id="ae1e7-129">**Bibliothèques Windows :**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="ae1e7-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="ae1e7-130">**Maintien de la synchronisation avec une bibliothèque :**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="ae1e7-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 



