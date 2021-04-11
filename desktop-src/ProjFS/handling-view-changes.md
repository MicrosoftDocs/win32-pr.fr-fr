---
title: Gestion des modifications d’affichage
description: Décrit comment mettre à jour la vue client du magasin de stockage d’un fournisseur.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 1d5a709752f92b7449d2ccc38f67c4417edf8d62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031359"
---
# <a name="handling-view-changes"></a><span data-ttu-id="cafe4-103">Gestion des modifications d’affichage</span><span class="sxs-lookup"><span data-stu-id="cafe4-103">Handling View Changes</span></span>

<span data-ttu-id="cafe4-104">À mesure que les fichiers et les répertoires sous la racine de virtualisation sont ouverts, le fournisseur crée des espaces réservés sur le disque, et à mesure que les fichiers sont lus, les espaces réservés sont alimentés avec le contenu.</span><span class="sxs-lookup"><span data-stu-id="cafe4-104">As files and directories under the virtualization root are opened, the provider creates placeholders on disk, and as files are read the placeholders are hydrated with contents.</span></span>  <span data-ttu-id="cafe4-105">Ces espaces réservés représentent l’état du magasin de stockage au moment où ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="cafe4-105">These placeholders represent the state of the backing store at the time they were created.</span></span>  <span data-ttu-id="cafe4-106">Ces éléments mis en cache, combinés aux éléments projetés par le fournisseur dans les énumérations, constituent la « vue » du magasin de stockage du client.</span><span class="sxs-lookup"><span data-stu-id="cafe4-106">These cached items, combined with the items projected by the provider in enumerations, constitute the client's "view" of the backing store.</span></span>  <span data-ttu-id="cafe4-107">De temps à autre, le fournisseur peut souhaiter mettre à jour l’affichage du client, que ce soit en raison de modifications dans le magasin de stockage, ou en raison d’une action explicite effectuée par l’utilisateur pour modifier son affichage.</span><span class="sxs-lookup"><span data-stu-id="cafe4-107">From time to time the provider may wish to update the client's view, whether because of changes in the backing store, or because of explicit action taken by the user to change their view.</span></span>

> <span data-ttu-id="cafe4-108">Si le fournisseur met à jour la vue de manière proactive, lorsque le magasin de stockage change, il est recommandé d’utiliser des modifications de vue relativement peu fréquentes.</span><span class="sxs-lookup"><span data-stu-id="cafe4-108">If the provider updates the view proactively, as the backing store changes, it is recommended that view changes be relatively infrequent.</span></span>  <span data-ttu-id="cafe4-109">En effet, une modification de la vue d’un élément qui a été ouvert et, par conséquent, avait un espace réservé créé sur le disque, exige que l’élément sur disque soit mis à jour ou supprimé pour refléter la modification de la vue.</span><span class="sxs-lookup"><span data-stu-id="cafe4-109">This is because a view change to an item that has been opened, and therefore had a placeholder created on disk, requires that the on-disk item be either updated or deleted to reflect the view change.</span></span>  <span data-ttu-id="cafe4-110">Des mises à jour fréquentes peuvent entraîner une activité supplémentaire sur le disque qui peut avoir un impact négatif sur les performances du système.</span><span class="sxs-lookup"><span data-stu-id="cafe4-110">Frequent updates may result in extra disk activity that can negatively impact system performance.</span></span>

## <a name="item-versioning"></a><span data-ttu-id="cafe4-111">Contrôle de version des éléments</span><span class="sxs-lookup"><span data-stu-id="cafe4-111">Item Versioning</span></span>

<span data-ttu-id="cafe4-112">Pour prendre en charge la gestion de plusieurs vues, ProjFS fournit le struct **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** .</span><span class="sxs-lookup"><span data-stu-id="cafe4-112">To support maintaining multiple views, ProjFS provides the **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span></span>  <span data-ttu-id="cafe4-113">Un fournisseur utilise ce struct autonome dans les appels à **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, et il est incorporé dans les structs **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** et **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .</span><span class="sxs-lookup"><span data-stu-id="cafe4-113">A provider uses this struct standalone in calls to **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, and it is embedded in the **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** and **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.</span></span>  <span data-ttu-id="cafe4-114">**PRJ_PLACEHOLDER_VERSION_INFO**. Le champ ContentID est l’emplacement où le fournisseur stocke jusqu’à 128 octets d’informations de version pour un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="cafe4-114">The **PRJ_PLACEHOLDER_VERSION_INFO**.ContentID field is where the provider stores up to 128 bytes of version information for a file or directory.</span></span>  <span data-ttu-id="cafe4-115">Le fournisseur peut ensuite associer cette valeur à une valeur qui identifie une vue particulière.</span><span class="sxs-lookup"><span data-stu-id="cafe4-115">The provider may then internally associate this value to some value that identifies a particular view.</span></span>

<span data-ttu-id="cafe4-116">Par exemple, un fournisseur qui virtualise un référentiel de contrôle de code source peut choisir d’utiliser un hachage du contenu d’un fichier pour servir de ContentID, et il peut utiliser des horodateurs pour identifier les vues du référentiel à différents moments précis dans le temps.</span><span class="sxs-lookup"><span data-stu-id="cafe4-116">For example, a provider that virtualizes a source control repository might choose to use a hash of a file's contents to serve as the ContentID, and it might use timestamps to identify views of the repository at various points in time.</span></span>  <span data-ttu-id="cafe4-117">Les horodateurs peuvent être le moment où les validations sur le référentiel ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="cafe4-117">The timestamps might be the times that commits to the repository were performed.</span></span>

<span data-ttu-id="cafe4-118">À l’aide de l’exemple d’un référentiel indexé par horodateur, un workflow classique pour l’utilisation du ContentID d’un élément peut être :</span><span class="sxs-lookup"><span data-stu-id="cafe4-118">Using the example of a timestamp-indexed repository, a typical flow for using an item's ContentID might be:</span></span>

1. <span data-ttu-id="cafe4-119">Le client établit une vue en spécifiant l’horodateur auquel présenter le contenu du référentiel.</span><span class="sxs-lookup"><span data-stu-id="cafe4-119">The client establishes a view by specifying the timestamp at which to present the repository contents.</span></span>  <span data-ttu-id="cafe4-120">Cela se fait par le biais d’une interface implémentée par le fournisseur, et non par le biais d’une API ProjFS.</span><span class="sxs-lookup"><span data-stu-id="cafe4-120">This would be done through some interface implemented by the provider, not via a ProjFS API.</span></span>  <span data-ttu-id="cafe4-121">Par exemple, le fournisseur peut avoir un outil en ligne de commande qui peut être utilisé pour indiquer au fournisseur que l’utilisateur souhaite obtenir.</span><span class="sxs-lookup"><span data-stu-id="cafe4-121">For example, the provider may have a command-line tool that could be used to tell the provider which view the user desires.</span></span>
1. <span data-ttu-id="cafe4-122">Lorsque le client crée un handle vers un fichier ou un répertoire virtualisé, le fournisseur crée un espace réservé pour celui-ci, à l’aide des métadonnées du système de fichiers du magasin de stockage.</span><span class="sxs-lookup"><span data-stu-id="cafe4-122">When the client creates a handle to a virtualized file or directory, the provider creates a placeholder for it, using file system metadata from the backing store.</span></span>  <span data-ttu-id="cafe4-123">L’ensemble de métadonnées qu’il utilise est identifié par la valeur ContentID associée à l’horodateur de la vue souhaitée.</span><span class="sxs-lookup"><span data-stu-id="cafe4-123">The particular set of metadata it uses is identified by the ContentID value associated with the timestamp of the desired view.</span></span>  <span data-ttu-id="cafe4-124">Lorsque le fournisseur appelle **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** pour écrire les informations d’espace réservé, il fournit le contentid dans le membre VERSIONINFO de l’argument _placeholderInfo_ .</span><span class="sxs-lookup"><span data-stu-id="cafe4-124">When the provider calls **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to write the placeholder information, it supplies the ContentID in the VersionInfo member of the _placeholderInfo_ argument.</span></span>  <span data-ttu-id="cafe4-125">Le fournisseur doit ensuite enregistrer qu’un espace réservé pour ce fichier ou ce répertoire a été créé dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="cafe4-125">The provider should then record that a placeholder for that file or directory was created in this view.</span></span>
1. <span data-ttu-id="cafe4-126">Lorsque le client lit à partir d’un espace réservé, le rappel **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** du fournisseur est appelé.</span><span class="sxs-lookup"><span data-stu-id="cafe4-126">When the client reads from a placeholder, the provider's **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback is invoked.</span></span>  <span data-ttu-id="cafe4-127">Le membre VersionInfo du paramètre _callbackdata_ contient contentid le fournisseur spécifié dans **PrjWritePlaceholderInfo** lors de la création de l’espace réservé de fichier.</span><span class="sxs-lookup"><span data-stu-id="cafe4-127">The _callbackData_ parameter's VersionInfo member contains the ContentID the provider specified in **PrjWritePlaceholderInfo** when it created the file placeholder.</span></span>  <span data-ttu-id="cafe4-128">Le fournisseur utilise ce ContentID pour récupérer le contenu correct du fichier à partir de son magasin de stockage.</span><span class="sxs-lookup"><span data-stu-id="cafe4-128">The provider uses that ContentID to retrieve the correct contents of the file from its backing store.</span></span>
1. <span data-ttu-id="cafe4-129">Le client demande une modification de la vue en spécifiant un nouvel horodateur.</span><span class="sxs-lookup"><span data-stu-id="cafe4-129">The client requests a view change by specifying a new timestamp.</span></span>  <span data-ttu-id="cafe4-130">Pour chaque espace réservé que le fournisseur a créé dans l’affichage précédent, si une autre version de ce fichier existe dans la nouvelle vue, le fournisseur peut remplacer l’espace réservé sur le disque par un autre dont le ContentID est associé au nouvel horodateur en appelant **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span><span class="sxs-lookup"><span data-stu-id="cafe4-130">For each placeholder the provider created in the previous view, if a different version of that file exists in the new view the provider may replace the placeholder on disk with an updated one whose ContentID is associated with the new timestamp by calling **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span></span>  <span data-ttu-id="cafe4-131">Le fournisseur peut également supprimer l’espace réservé en appelant **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** afin que la nouvelle vue du fichier soit projetée dans les énumérations.</span><span class="sxs-lookup"><span data-stu-id="cafe4-131">Alternatively, the provider may delete the placeholder by calling **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** so that the new view of the file will be projected in enumerations.</span></span>  <span data-ttu-id="cafe4-132">Si le fichier n’existe pas dans la nouvelle vue, le fournisseur doit le supprimer en appelant **PrjDeleteFile**.</span><span class="sxs-lookup"><span data-stu-id="cafe4-132">If the file does not exist in the new view, the provider must delete it by calling **PrjDeleteFile**.</span></span>

<span data-ttu-id="cafe4-133">Notez que le fournisseur doit s’assurer que lorsque le client énumère un répertoire, le fournisseur fournira le contenu qui correspond à la vue du client.</span><span class="sxs-lookup"><span data-stu-id="cafe4-133">Note that the provider must ensure that when the client enumerates a directory, the provider will supply the contents that correspond to the client's view.</span></span>  <span data-ttu-id="cafe4-134">Par exemple, le fournisseur peut utiliser le membre VersionInfo du paramètre _callbackdata_ du **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** et **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** les rappels pour récupérer le contenu du répertoire à la volée.</span><span class="sxs-lookup"><span data-stu-id="cafe4-134">For example, the provider could use the VersionInfo member of the _callbackData_ parameter of the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** and **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** callbacks to retrieve directory contents on the fly.</span></span>  <span data-ttu-id="cafe4-135">Il peut également créer une structure de répertoires pour cette vue dans le magasin de stockage dans le cadre de l’établissement de la vue, puis énumérer simplement cette structure.</span><span class="sxs-lookup"><span data-stu-id="cafe4-135">Alternatively it could build a directory structure for that view in its backing store as part of establishing the view, and then simply enumerate that structure.</span></span>

> <span data-ttu-id="cafe4-136">Chaque fois qu’un rappel de fournisseur est appelé pour un espace réservé ou un fichier partiel, les informations de version que le fournisseur a spécifié lors de la création de l’élément sont fournies dans le membre VersionInfo du paramètre _callbackdata_ du rappel.</span><span class="sxs-lookup"><span data-stu-id="cafe4-136">Whenever a provider callback is invoked for a placeholder or partial file, the version information the provider specified when creating the item is provided in the VersionInfo member of the callback's _callbackData_ parameter.</span></span>

## <a name="updating-the-view"></a><span data-ttu-id="cafe4-137">Mise à jour de la vue</span><span class="sxs-lookup"><span data-stu-id="cafe4-137">Updating the View</span></span>

<span data-ttu-id="cafe4-138">Voici un exemple de fonction illustrant comment un fournisseur peut mettre à jour l’affichage local lorsque l’utilisateur spécifie un nouvel horodateur.</span><span class="sxs-lookup"><span data-stu-id="cafe4-138">Below is a sample function illustrating how a provider might update the local view when the user specifies a new timestamp.</span></span>  <span data-ttu-id="cafe4-139">La fonction récupère une liste des espaces réservés que le fournisseur a créé pour la vue que l’utilisateur vient de modifier, et met à jour l’état du cache local en fonction de l’état de chaque espace réservé dans la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="cafe4-139">The function retrieves a list of the placeholders the provider created for the view the user has just changed from, and updates the local cache state based on each placeholder's state in the new view.</span></span>  <span data-ttu-id="cafe4-140">Par souci de clarté, cette routine omet certaines complexités liées au système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cafe4-140">For clarity, this routine omits certain complexities of dealing with the file system.</span></span>  <span data-ttu-id="cafe4-141">Par exemple, dans l’ancienne vue, un répertoire donné peut exister avec certains fichiers ou répertoires, mais dans la nouvelle vue, le répertoire (et son contenu) n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="cafe4-141">For example, in the old view a given directory may have existed with some files or directories in it, but in the new view that directory (and its contents) may no longer exist.</span></span>  <span data-ttu-id="cafe4-142">Pour éviter de rencontrer des erreurs dans une telle situation, le fournisseur doit mettre à jour l’état du fichier et des répertoires sous la racine de la virtualisation de manière à la profondeur.</span><span class="sxs-lookup"><span data-stu-id="cafe4-142">To avoid encountering errors in such a situation the provider should update the state of the file and directories beneath the virtualization root in a depth-first fashion.</span></span>

```C++
typedef struct MY_ON_DISK_PLACEHOLDER MY_ON_DISK_PLACEHOLDER;

typedef struct MY_ON_DISK_PLACEHOLDER {
    MY_ON_DISK_PLACEHOLDER* Next;
    PWSTR RelativePath;
} MY_ON_DISK_PLACEHOLDER;

HRESULT
MyViewUpdater(
    _In_ PRJ_CALLBACK_DATA callbackData,
    _In_ time_t newViewTime
    )
{
    HRESULT hr = S_OK;

    // MyGetOnDiskPlaceholders is a routine the provider might implement to produce
    // a pointer to a list of the placeholders the provider has created in the view.
    MY_ON_DISK_PLACEHOLDER* placeholder = MyGetOnDiskPlaceholders();
    while (placeholder != NULL)
    {
        // MyGetProjectedFileInfo is a routine the provider might implement to
        // determine whether a given file exists in its backing store at a
        // particular timestamp.  If it does, the routine returns a pointer to
        // a PRJ_PLACEHOLDER_INFO struct populated with information about the
        // file.
        PRJ_PLACEHOLDER_INFO* newViewPlaceholderInfo = NULL;
        UINT32 newViewPlaceholderInfoSize = 0;

        newViewPlaceholderInfo = MyGetProjectedFileInfo(placeholder->RelativePath,
                                                 newViewTime,
                                                 &newViewPlaceholderInfoSize);
        if (newViewPlaceholderInfo == NULL)
        {
            // The file no longer exists in the new view.  We want to remove its
            // placeholder from the local cache.
            PRJ_UPDATE_FAILURE_CAUSES deleteFailureReason;
            hr = PrjDeleteFile(callbackData->NamespaceVirtualizationContext,
                               placeholder->RelativePath,
                               PRJ_UPDATE_ALLOW_DIRTY_METADATA
                               | PRJ_UPDATE_ALLOW_DIRTY_DATA
                               | PRJ_UPDATE_ALLOW_TOMBSTONE,
                               &deleteFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not delete [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", deleteFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error deleting [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyRemovePlaceholderData is a routine the provider might implement
            // to remove an item from its list of placeholders it has created in
            // the view.
            MyRemovePlaceholderData(placeholder);
        }
        else
        {
            // The file exists in the new view.  Its local cache state may need
            // to be updated, for example if its content is different in this view.
            // As an optimization, the provider may compare the file's ContentID
            // in the new view (stored in newViewPlaceholderInfo->ContentId) with
            // the ContentID it had in the old view.  If they are the same, calling
            // PrjUpdateFileIfNeeded would not be needed.
            PRJ_UPDATE_FAILURE_CAUSES updateFailureReason;
            hr = PrjUpdateFileIfNeeded(callbackData->NamespaceVirtualizationContext,
                                       placeholder->RelativePath,
                                       newViewPlaceholderInfo,
                                       newViewPlaceholderInfoSize,
                                       PRJ_UPDATE_ALLOW_DIRTY_METADATA
                                       | PRJ_UPDATE_ALLOW_DIRTY_DATA
                                       | PRJ_UPDATE_ALLOW_TOMBSTONE,
                                       &updateFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not update [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", updateFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error updating [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyUpdatePlaceholderData is a routine the provider might implement
            // to update information about a placeholder it has created in the view.
            MyUpdatePlaceholderData(placeholder, newViewPlaceholderInfo);
        }

        placeholder = placeholder->Next;
    }

    return hr;
}
```