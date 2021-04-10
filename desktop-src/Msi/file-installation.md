---
description: 'Une fois le coût du fichier terminé, le programme d’installation dispose de toutes les informations requises pour traiter les deux actions de manipulation de fichiers : DuplicateFiles et MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Installation du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115670"
---
# <a name="file-installation"></a><span data-ttu-id="c0044-103">Installation du fichier</span><span class="sxs-lookup"><span data-stu-id="c0044-103">File Installation</span></span>

<span data-ttu-id="c0044-104">Une fois le [coût du fichier](file-costing.md) terminé, le programme d’installation dispose de toutes les informations requises pour traiter les deux actions de manipulation de fichiers : [DuplicateFiles](duplicatefiles-action.md) et [MoveFiles](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="c0044-104">Once [file costing](file-costing.md) has been completed, the installer has all the information required to process the two file manipulation actions: [DuplicateFiles](duplicatefiles-action.md) and [MoveFiles](movefiles-action.md).</span></span>

<span data-ttu-id="c0044-105">Utilisez l' [action DuplicateFiles](duplicatefiles-action.md) pour spécifier les fichiers que le programme d’installation doit dupliquer dans la [table DuplicateFile](duplicatefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="c0044-105">Use the [DuplicateFiles action](duplicatefiles-action.md) to specify the files the installer is to duplicate in the [DuplicateFile table](duplicatefile-table.md).</span></span> <span data-ttu-id="c0044-106">Utilisez l' [action MoveFiles](movefiles-action.md)pour déterminer les fichiers à déplacer en interrogeant la [table MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="c0044-106">Use the [MoveFiles action](movefiles-action.md)to determine which files to move by querying the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="c0044-107">Notez que le champ options de la [table MoveFile](movefile-table.md) spécifie si le fichier d’origine doit être supprimé de son emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="c0044-107">Note that the Options field of the [MoveFile table](movefile-table.md) specifies whether or not the original file is to be deleted from its current location.</span></span> <span data-ttu-id="c0044-108">Les fichiers qui sont déplacés ou copiés par l’action MoveFiles ne sont pas supprimés lorsque le produit est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="c0044-108">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

<span data-ttu-id="c0044-109">L' [action InstallFiles](installfiles-action.md) est appelée une fois toutes les autres opérations de manipulation de fichier terminées.</span><span class="sxs-lookup"><span data-stu-id="c0044-109">The [InstallFiles action](installfiles-action.md) is called once all other file manipulation operations have completed.</span></span> <span data-ttu-id="c0044-110">L’action InstallFiles traite la table [multimédia](media-table.md), la [table de fichiers](file-table.md)et la [table de composants](component-table.md) pour déterminer quels fichiers seront copiés de la source vers la destination.</span><span class="sxs-lookup"><span data-stu-id="c0044-110">The InstallFiles action processes the [Media table](media-table.md), the [File table](file-table.md), and the [Component table](component-table.md) to determine which files will be copied from the source to the destination.</span></span>

<span data-ttu-id="c0044-111">L' [action InstallFiles](installfiles-action.md) crée la structure de répertoire nécessaire à l’installation de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="c0044-111">The [InstallFiles action](installfiles-action.md) creates the directory structure necessary to install all files.</span></span> <span data-ttu-id="c0044-112">Si vous devez installer un dossier explicitement vide, l' [action CreateFolders](createfolders-action.md) peut être appelée pour le créer.</span><span class="sxs-lookup"><span data-stu-id="c0044-112">If an explicitly empty folder is required to be installed, the [CreateFolders action](createfolders-action.md) may be called to create it.</span></span>

 

 



