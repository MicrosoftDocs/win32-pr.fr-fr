---
title: Gestion des modifications d’affichage
description: Décrit comment mettre à jour la vue client du magasin de stockage d’un fournisseur.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 99ace7849b8967748f26210d9d6b770e424c349359aa39e828c8ad9af36a65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792646"
---
# <a name="handling-view-changes"></a>Gestion des modifications d’affichage

À mesure que les fichiers et les répertoires sous la racine de virtualisation sont ouverts, le fournisseur crée des espaces réservés sur le disque, et à mesure que les fichiers sont lus, les espaces réservés sont alimentés avec le contenu.  Ces espaces réservés représentent l’état du magasin de stockage au moment où ils ont été créés.  Ces éléments mis en cache, combinés aux éléments projetés par le fournisseur dans les énumérations, constituent la « vue » du magasin de stockage du client.  De temps à autre, le fournisseur peut souhaiter mettre à jour l’affichage du client, que ce soit en raison de modifications dans le magasin de stockage, ou en raison d’une action explicite effectuée par l’utilisateur pour modifier son affichage.

> Si le fournisseur met à jour la vue de manière proactive, lorsque le magasin de stockage change, il est recommandé d’utiliser des modifications de vue relativement peu fréquentes.  En effet, une modification de la vue d’un élément qui a été ouvert et, par conséquent, avait un espace réservé créé sur le disque, exige que l’élément sur disque soit mis à jour ou supprimé pour refléter la modification de la vue.  Des mises à jour fréquentes peuvent entraîner une activité supplémentaire sur le disque qui peut avoir un impact négatif sur les performances du système.

## <a name="item-versioning"></a>Contrôle de version des éléments

Pour prendre en charge la gestion de plusieurs vues, ProjFS fournit le struct **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** .  Un fournisseur utilise ce struct autonome dans les appels à **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, et il est incorporé dans les structs **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** et **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .  **PRJ_PLACEHOLDER_VERSION_INFO**. Le champ ContentID est l’emplacement où le fournisseur stocke jusqu’à 128 octets d’informations de version pour un fichier ou un répertoire.  Le fournisseur peut ensuite associer cette valeur à une valeur qui identifie une vue particulière.

Par exemple, un fournisseur qui virtualise un référentiel de contrôle de code source peut choisir d’utiliser un hachage du contenu d’un fichier pour servir de ContentID, et il peut utiliser des horodateurs pour identifier les vues du référentiel à différents moments précis dans le temps.  Les horodateurs peuvent être le moment où les validations sur le référentiel ont été effectuées.

À l’aide de l’exemple d’un référentiel indexé par horodateur, un workflow classique pour l’utilisation du ContentID d’un élément peut être :

1. Le client établit une vue en spécifiant l’horodateur auquel présenter le contenu du référentiel.  Cela se fait par le biais d’une interface implémentée par le fournisseur, et non par le biais d’une API ProjFS.  Par exemple, le fournisseur peut avoir un outil en ligne de commande qui peut être utilisé pour indiquer au fournisseur que l’utilisateur souhaite obtenir.
1. Lorsque le client crée un handle vers un fichier ou un répertoire virtualisé, le fournisseur crée un espace réservé pour celui-ci, à l’aide des métadonnées du système de fichiers du magasin de stockage.  L’ensemble de métadonnées qu’il utilise est identifié par la valeur ContentID associée à l’horodateur de la vue souhaitée.  Lorsque le fournisseur appelle **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** pour écrire les informations d’espace réservé, il fournit le contentid dans le membre VERSIONINFO de l’argument _placeholderInfo_ .  Le fournisseur doit ensuite enregistrer qu’un espace réservé pour ce fichier ou ce répertoire a été créé dans cette vue.
1. Lorsque le client lit à partir d’un espace réservé, le rappel **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** du fournisseur est appelé.  Le membre VersionInfo du paramètre _callbackdata_ contient contentid le fournisseur spécifié dans **PrjWritePlaceholderInfo** lors de la création de l’espace réservé de fichier.  Le fournisseur utilise ce ContentID pour récupérer le contenu correct du fichier à partir de son magasin de stockage.
1. Le client demande une modification de la vue en spécifiant un nouvel horodateur.  Pour chaque espace réservé que le fournisseur a créé dans l’affichage précédent, si une autre version de ce fichier existe dans la nouvelle vue, le fournisseur peut remplacer l’espace réservé sur le disque par un autre dont le ContentID est associé au nouvel horodateur en appelant **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.  Le fournisseur peut également supprimer l’espace réservé en appelant **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** afin que la nouvelle vue du fichier soit projetée dans les énumérations.  Si le fichier n’existe pas dans la nouvelle vue, le fournisseur doit le supprimer en appelant **PrjDeleteFile**.

Notez que le fournisseur doit s’assurer que lorsque le client énumère un répertoire, le fournisseur fournira le contenu qui correspond à la vue du client.  Par exemple, le fournisseur peut utiliser le membre VersionInfo du paramètre _callbackdata_ du **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** et **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** les rappels pour récupérer le contenu du répertoire à la volée.  Il peut également créer une structure de répertoires pour cette vue dans le magasin de stockage dans le cadre de l’établissement de la vue, puis énumérer simplement cette structure.

> Chaque fois qu’un rappel de fournisseur est appelé pour un espace réservé ou un fichier partiel, les informations de version que le fournisseur a spécifié lors de la création de l’élément sont fournies dans le membre VersionInfo du paramètre _callbackdata_ du rappel.

## <a name="updating-the-view"></a>Mise à jour de la vue

Voici un exemple de fonction illustrant comment un fournisseur peut mettre à jour l’affichage local lorsque l’utilisateur spécifie un nouvel horodateur.  La fonction récupère une liste des espaces réservés que le fournisseur a créé pour la vue que l’utilisateur vient de modifier, et met à jour l’état du cache local en fonction de l’état de chaque espace réservé dans la nouvelle vue.  Par souci de clarté, cette routine omet certaines complexités liées au système de fichiers.  Par exemple, dans l’ancienne vue, un répertoire donné peut exister avec certains fichiers ou répertoires, mais dans la nouvelle vue, le répertoire (et son contenu) n’existe plus.  Pour éviter de rencontrer des erreurs dans une telle situation, le fournisseur doit mettre à jour l’état du fichier et des répertoires sous la racine de la virtualisation de manière à la profondeur.

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