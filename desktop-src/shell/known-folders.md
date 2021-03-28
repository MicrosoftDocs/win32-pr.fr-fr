---
description: Windows Vista introduit de nouveaux scénarios de stockage et un nouvel espace de noms de profil utilisateur.
title: Dossiers connus
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973494"
---
# <a name="known-folders"></a><span data-ttu-id="d80b7-103">Dossiers connus</span><span class="sxs-lookup"><span data-stu-id="d80b7-103">Known Folders</span></span>

<span data-ttu-id="d80b7-104">Windows Vista introduit de nouveaux scénarios de stockage et un nouvel espace de noms de profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d80b7-104">Windows Vista introduces new storage scenarios and a new user profile namespace.</span></span> <span data-ttu-id="d80b7-105">Pour répondre à ces nouveaux facteurs, l’ancien système de référence aux dossiers standard par une valeur [**CSIDL**](csidl.md) a été remplacé.</span><span class="sxs-lookup"><span data-stu-id="d80b7-105">To address these new factors, the older system of referring to standard folders by a [**CSIDL**](csidl.md) value has been replaced.</span></span> <span data-ttu-id="d80b7-106">À compter de Windows Vista, ces dossiers sont référencés par un nouvel ensemble de valeurs GUID appelé ID de dossier connu.</span><span class="sxs-lookup"><span data-stu-id="d80b7-106">As of Windows Vista, those folders are referenced by a new set of GUID values called Known Folder IDs.</span></span>

<span data-ttu-id="d80b7-107">Le système de dossiers connu offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="d80b7-107">The Known Folder system provides these advantages:</span></span>

-   <span data-ttu-id="d80b7-108">Les éditeurs de logiciels indépendants (ISV) peuvent étendre l’ensemble des ID de dossiers connus avec leur propre ID.</span><span class="sxs-lookup"><span data-stu-id="d80b7-108">Independent software vendors (ISVs) can extend the set of Known Folder IDs with their own.</span></span> <span data-ttu-id="d80b7-109">Ils peuvent définir des dossiers, leur attribuer des ID et les inscrire auprès du système.</span><span class="sxs-lookup"><span data-stu-id="d80b7-109">They can define folders, give them IDs, and register them with the system.</span></span> <span data-ttu-id="d80b7-110">Impossible d’étendre les valeurs CSIDL.</span><span class="sxs-lookup"><span data-stu-id="d80b7-110">CSIDL values could not be extended.</span></span>
-   <span data-ttu-id="d80b7-111">Tous les dossiers connus sur un système peuvent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="d80b7-111">All Known Folders on a system can be enumerated.</span></span> <span data-ttu-id="d80b7-112">Aucune API n’offrait cette fonctionnalité pour les valeurs CSIDL.</span><span class="sxs-lookup"><span data-stu-id="d80b7-112">No API provided this functionality for CSIDL values.</span></span> <span data-ttu-id="d80b7-113">Pour plus d’informations, consultez [**IKnownFolderManager :: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) .</span><span class="sxs-lookup"><span data-stu-id="d80b7-113">See [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) for more information.</span></span>
-   <span data-ttu-id="d80b7-114">Un dossier connu ajouté par un éditeur de logiciels indépendant peut ajouter des propriétés personnalisées qui lui permettent d’expliquer son rôle et son utilisation prévue.</span><span class="sxs-lookup"><span data-stu-id="d80b7-114">A known folder added by an ISV can add custom properties that allow it to explain its purpose and intended use.</span></span>
-   <span data-ttu-id="d80b7-115">De nombreux dossiers connus peuvent être redirigés vers de nouveaux emplacements, y compris des emplacements réseau.</span><span class="sxs-lookup"><span data-stu-id="d80b7-115">Many known folders can be redirected to new locations, including network locations.</span></span> <span data-ttu-id="d80b7-116">Sous le système CSIDL, seul le dossier **Mes documents** peut être redirigé.</span><span class="sxs-lookup"><span data-stu-id="d80b7-116">Under the CSIDL system, only the **My Documents** folder could be redirected.</span></span>
-   <span data-ttu-id="d80b7-117">Les dossiers connus peuvent avoir des gestionnaires personnalisés à utiliser lors de la création ou de la suppression.</span><span class="sxs-lookup"><span data-stu-id="d80b7-117">Known folders can have custom handlers for use during creation or deletion.</span></span>

<span data-ttu-id="d80b7-118">Le système CSIDL et les API qui font appel aux valeurs CSIDL sont toujours pris en charge pour la compatibilité.</span><span class="sxs-lookup"><span data-stu-id="d80b7-118">The CSIDL system and APIs that make use of CSIDL values are still supported for compatibility.</span></span> <span data-ttu-id="d80b7-119">Toutefois, il n’est pas recommandé de les utiliser dans un nouveau développement.</span><span class="sxs-lookup"><span data-stu-id="d80b7-119">However, it is not recommended to use them in any new development.</span></span>


<span data-ttu-id="d80b7-120">Les rubriques suivantes décrivent les caractéristiques du système de dossiers connus.</span><span class="sxs-lookup"><span data-stu-id="d80b7-120">The following topics discuss the specifics of the Known Folders system.</span></span>

-   [<span data-ttu-id="d80b7-121">Utilisation de dossiers connus dans les applications</span><span class="sxs-lookup"><span data-stu-id="d80b7-121">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
-   [<span data-ttu-id="d80b7-122">Comment étendre des dossiers connus avec des dossiers personnalisés</span><span class="sxs-lookup"><span data-stu-id="d80b7-122">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
-   [<span data-ttu-id="d80b7-123">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="d80b7-123">**KNOWNFOLDERID**</span></span>](knownfolderid.md)

<span data-ttu-id="d80b7-124">Les pages de référence suivantes décrivent les fonctions de dossiers connus Win32, qui peuvent être utilisées pour récupérer l’emplacement des dossiers connus ou les rediriger vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="d80b7-124">The following reference pages explain the Win32 Known Folders functions, which can be used to retrieve the location of Known Folders or redirect them to a new location.</span></span> <span data-ttu-id="d80b7-125">Ces fonctions remplacent les anciennes fonctions Win32.</span><span class="sxs-lookup"><span data-stu-id="d80b7-125">These functions replace older Win32 functions.</span></span> <span data-ttu-id="d80b7-126">Les nouvelles fonctions sont fournies pour fournir un comportement équivalent aux anciennes fonctions, mais chaque nouvelle fonction est également dupliquée par une API COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="d80b7-126">The new functions are provided to give equivalent behavior to the old functions, but each new function is also duplicated by a Component Object Model (COM) API.</span></span>



| <span data-ttu-id="d80b7-127">Nouvelle fonction</span><span class="sxs-lookup"><span data-stu-id="d80b7-127">New Function</span></span>                                             | <span data-ttu-id="d80b7-128">Remplace</span><span class="sxs-lookup"><span data-stu-id="d80b7-128">Replaces</span></span>                                           | <span data-ttu-id="d80b7-129">Équivalent COM</span><span class="sxs-lookup"><span data-stu-id="d80b7-129">COM Equivalent</span></span>                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="d80b7-130">**SHGetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="d80b7-130">**SHGetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [<span data-ttu-id="d80b7-131">**SHGetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="d80b7-131">**SHGetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [<span data-ttu-id="d80b7-132">**IKnownFolder::GetPath**</span><span class="sxs-lookup"><span data-stu-id="d80b7-132">**IKnownFolder::GetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [<span data-ttu-id="d80b7-133">**SHGetKnownFolderIDList**</span><span class="sxs-lookup"><span data-stu-id="d80b7-133">**SHGetKnownFolderIDList**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [<span data-ttu-id="d80b7-134">**SHGetFolderLocation**</span><span class="sxs-lookup"><span data-stu-id="d80b7-134">**SHGetFolderLocation**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [<span data-ttu-id="d80b7-135">**IKnownFolder::GetIDList**</span><span class="sxs-lookup"><span data-stu-id="d80b7-135">**IKnownFolder::GetIDList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [<span data-ttu-id="d80b7-136">**SHSetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="d80b7-136">**SHSetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [<span data-ttu-id="d80b7-137">**SHSetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="d80b7-137">**SHSetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [<span data-ttu-id="d80b7-138">**IKnownFolder::SetPath**</span><span class="sxs-lookup"><span data-stu-id="d80b7-138">**IKnownFolder::SetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

<span data-ttu-id="d80b7-139">Les pages de référence suivantes décrivent les API de dossiers connus COM, qui fournissent toutes les fonctionnalités des API Win32 répertoriées ci-dessus, ainsi que la possibilité d’énumérer tous les dossiers connus, d’accéder aux propriétés de dossier connues et d’étendre l’ensemble standard de dossiers connus.</span><span class="sxs-lookup"><span data-stu-id="d80b7-139">The following reference pages explain the COM Known Folders APIs, which provide all of the functionality of the Win32 APIs listed above, plus add the ability to enumerate all Known Folders, access Known Folder properties, and extend the standard set of Known Folders.</span></span>

-   [<span data-ttu-id="d80b7-140">**IKnownFolder**</span><span class="sxs-lookup"><span data-stu-id="d80b7-140">**IKnownFolder**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [<span data-ttu-id="d80b7-141">**IKnownFolderManager**</span><span class="sxs-lookup"><span data-stu-id="d80b7-141">**IKnownFolderManager**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

<span data-ttu-id="d80b7-142">Un exemple C++ qui illustre les API de dossiers connus est inclus dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="d80b7-142">A C++ sample that demonstrates the Known Folder APIs is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d80b7-143">Une fois que vous avez installé le SDK Windows sur votre ordinateur, l’exemple se trouve sous% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppPlatform \\ fichier KnownFolders.</span><span class="sxs-lookup"><span data-stu-id="d80b7-143">Once you have installed the Windows SDK on your computer, the sample can be found under %ProgramFiles%\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppPlatform\\KnownFolders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d80b7-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d80b7-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d80b7-145">[Dossiers connus, exemple](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d80b7-145">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
