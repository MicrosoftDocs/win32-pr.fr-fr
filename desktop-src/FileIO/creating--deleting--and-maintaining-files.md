---
description: Fonctions à utiliser pour créer, supprimer et gérer des fichiers.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Création, suppression et maintenance de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531745"
---
# <a name="creating-deleting-and-maintaining-files"></a><span data-ttu-id="43d92-103">Création, suppression et maintenance de fichiers</span><span class="sxs-lookup"><span data-stu-id="43d92-103">Creating, Deleting, and Maintaining Files</span></span>

<span data-ttu-id="43d92-104">Les rubriques suivantes décrivent comment créer, supprimer et gérer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="43d92-104">The following topics describe how to create, delete, and maintain files.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="43d92-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="43d92-105">In this section</span></span>



| <span data-ttu-id="43d92-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="43d92-106">Topic</span></span>                                                                   | <span data-ttu-id="43d92-107">Description</span><span class="sxs-lookup"><span data-stu-id="43d92-107">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43d92-108">Nommage des fichiers, chemins d’accès et espaces de noms</span><span class="sxs-lookup"><span data-stu-id="43d92-108">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)<br/>     | <span data-ttu-id="43d92-109">Règles, conventions et limitations des noms de fichiers et de répertoires, notamment les conventions d’affectation de noms, les noms de fichiers courts et les noms de fichiers longs, les chemins d’accès complets et les chemins d’accès relatifs, la limite de longueur maximale du chemin d’accès, les noms de fichiers 8,3 et les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="43d92-109">Rules, conventions, and limitations of names for files and directories, including naming conventions, short file names vs. long file names, fully qualified paths vs. relative paths, maximum path length limitation, 8.3 file names, and namespaces.</span></span><br/>            |
| [<span data-ttu-id="43d92-110">Création et ouverture de fichiers</span><span class="sxs-lookup"><span data-stu-id="43d92-110">Creating and Opening Files</span></span>](creating-and-opening-files.md)<br/> | <span data-ttu-id="43d92-111">Considérations relatives à la création ou à l’ouverture d’un fichier à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="43d92-111">Considerations for creating or opening a file by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="43d92-112">Déplacement et remplacement de fichiers</span><span class="sxs-lookup"><span data-stu-id="43d92-112">Moving and Replacing Files</span></span>](moving-and-replacing-files.md)<br/> | <span data-ttu-id="43d92-113">Considérations relatives au déplacement et au remplacement de fichiers à l’aide des fonctions CopyFileEx, CreateFile, ReplaceFile et MoveFileEx.</span><span class="sxs-lookup"><span data-stu-id="43d92-113">Considerations for moving and replacing files by using the CopyFileEx, CreateFile, Replacefile, and MoveFileEx functions.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="43d92-114">Fermeture et suppression de fichiers</span><span class="sxs-lookup"><span data-stu-id="43d92-114">Closing and Deleting Files</span></span>](closing-and-deleting-files.md)<br/> | <span data-ttu-id="43d92-115">Pour utiliser efficacement les ressources du système d’exploitation, une application doit fermer les fichiers lorsqu’ils ne sont plus nécessaires à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="43d92-115">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="43d92-116">Si un fichier est ouvert lorsqu’une application se termine, le système le ferme automatiquement.</span><span class="sxs-lookup"><span data-stu-id="43d92-116">If a file is open when an application terminates, the system closes it automatically.</span></span><br/> |
| [<span data-ttu-id="43d92-117">Défragmentation des fichiers</span><span class="sxs-lookup"><span data-stu-id="43d92-117">Defragmenting Files</span></span>](defragmenting-files.md)<br/>               | <span data-ttu-id="43d92-118">La *défragmentation* est le processus qui consiste à déplacer des parties de fichiers sur un disque pour défragmenter des fichiers, c’est-à-dire le processus de déplacement de clusters de fichiers sur un disque afin de les rendre contigus.</span><span class="sxs-lookup"><span data-stu-id="43d92-118">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span><br/>                                                                               |



 

 

