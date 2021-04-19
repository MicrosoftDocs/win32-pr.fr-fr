---
title: ProjFS, fonctions
description: Les fonctions suivantes sont déclarées dans projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 40f3f2aec8e52d2caafdcf1554d0871e9bb185de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509075"
---
# <a name="projfs-functions"></a>ProjFS, fonctions

Les fonctions suivantes sont déclarées dans projectedfslib. h.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Alloue une mémoire tampon qui répond aux exigences d’alignement de la mémoire du dispositif de stockage de l’instance de virtualisation. |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Vide le cache de chemin d’accès négatif de l’instance de virtualisation, si elle est active. |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Indique que le fournisseur a terminé le traitement d’un rappel à partir duquel il a précédemment retourné HRESULT_FROM_WIN32 (ERROR_IO_PENDING). |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Permet à un fournisseur de supprimer un élément qui a été mis en cache dans le système de fichiers local. |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Détermine si un nom contient des caractères génériques. |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Compare deux noms de fichiers et retourne une valeur qui indique leur ordre de classement relatif. |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Détermine si un nom de fichier correspond à un modèle de recherche. |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Fournit des informations pour un fichier ou un répertoire à une énumération. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Fournit des informations pour un fichier ou un répertoire à une énumération et permet à l’appelant de spécifier des informations étendues. |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Libère une mémoire tampon allouée. |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Obtient l’état du fichier sur disque pour un fichier ou un répertoire. |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Récupère des informations sur l’instance de virtualisation. |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Convertit un répertoire existant en un espace réservé de répertoire. |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Configure une instance de virtualisation ProjFS et la démarre, afin de la rendre disponible pour les e/s de service et d’appeler les rappels sur le fournisseur. |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Arrête une instance de virtualisation ProjFS en cours d’exécution, ce qui la rend non disponible pour les e/s de service ou implique des rappels sur le fournisseur. |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Permet à un fournisseur de mettre à jour un élément qui a été mis en cache sur le système de fichiers local. |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Envoie le contenu du fichier à ProjFS. |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Envoie des métadonnées de fichier ou de répertoire à ProjFS. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Envoie des métadonnées de fichier ou de répertoire à ProjFS et permet à l’appelant de spécifier des informations étendues. |
