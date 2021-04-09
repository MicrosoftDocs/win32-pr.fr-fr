---
description: Un répertoire qui contient un ou plusieurs répertoires est le parent du répertoire ou des répertoires contenus, et chaque répertoire contenu est un enfant du répertoire parent. La structure hiérarchique des répertoires est appelée arborescence de répertoires.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: À propos de la gestion d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862658"
---
# <a name="about-directory-management"></a><span data-ttu-id="0b6c7-104">À propos de la gestion d’annuaire</span><span class="sxs-lookup"><span data-stu-id="0b6c7-104">About Directory Management</span></span>

<span data-ttu-id="0b6c7-105">Un répertoire qui contient un ou plusieurs répertoires est le *parent* du répertoire ou des répertoires contenus, et chaque répertoire contenu est un *enfant* du répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-105">A directory that contains one or more directories is the *parent* of the contained directory or directories, and each contained directory is a *child* of the parent directory.</span></span> <span data-ttu-id="0b6c7-106">La structure hiérarchique des répertoires est appelée *arborescence de répertoires*.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-106">The hierarchical structure of directories is referred to as a *directory tree*.</span></span>

<span data-ttu-id="0b6c7-107">Le système de fichiers NTFS implémente le lien logique entre un répertoire et les fichiers qu’il contient comme *table d’entrée de répertoire*.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-107">The NTFS file system implements the logical link between a directory and the files it contains as a *directory entry table*.</span></span> <span data-ttu-id="0b6c7-108">Lorsqu’un fichier est déplacé dans un répertoire, une entrée est créée dans la table pour le fichier déplacé et le nom du fichier est placé dans l’entrée.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-108">When a file is moved into a directory, an entry is created in the table for the moved file and the name of the file is placed in the entry.</span></span> <span data-ttu-id="0b6c7-109">Lorsqu’un fichier contenu dans un répertoire est supprimé, le nom et l’entrée correspondant au fichier supprimé sont également supprimés de la table.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-109">When a file contained in a directory is deleted, the name and entry corresponding to the deleted file is also deleted from the table.</span></span> <span data-ttu-id="0b6c7-110">Il peut exister plusieurs entrées pour un seul fichier dans une table d’entrée de répertoire.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-110">More than one entry for a single file can exist in a directory entry table.</span></span> <span data-ttu-id="0b6c7-111">Si une entrée supplémentaire est créée dans la table pour un fichier, cette entrée est appelée un *lien physique* vers ce fichier.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-111">If an additional entry is created in the table for a file, that entry is referred to as a *hard link* to that file.</span></span> <span data-ttu-id="0b6c7-112">Il n’existe aucune limite au nombre de liens physiques qui peuvent être créés pour un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-112">There is no limit to the number of hard links that can be created for a single file.</span></span>

<span data-ttu-id="0b6c7-113">Les répertoires peuvent également contenir des jonctions et des points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-113">Directories can also contain junctions and reparse points.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0b6c7-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="0b6c7-114">In this section</span></span>



| <span data-ttu-id="0b6c7-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="0b6c7-115">Topic</span></span>                                                                                 | <span data-ttu-id="0b6c7-116">Description</span><span class="sxs-lookup"><span data-stu-id="0b6c7-116">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b6c7-117">Création et suppression de répertoires</span><span class="sxs-lookup"><span data-stu-id="0b6c7-117">Creating and Deleting Directories</span></span>](creating-and-deleting-directories.md)<br/> | <span data-ttu-id="0b6c7-118">Une application peut créer et supprimer par programmation des répertoires.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-118">An application can programmatically create and delete directories.</span></span><br/>                          |
| [<span data-ttu-id="0b6c7-119">Handles de répertoire</span><span class="sxs-lookup"><span data-stu-id="0b6c7-119">Directory Handles</span></span>](obtaining-a-handle-to-a-directory.md)<br/>                 | <span data-ttu-id="0b6c7-120">Chaque fois qu’un processus crée ou ouvre un objet d’annuaire, il reçoit un descripteur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-120">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span><br/> |
| [<span data-ttu-id="0b6c7-121">Points d'analyse</span><span class="sxs-lookup"><span data-stu-id="0b6c7-121">Reparse Points</span></span>](reparse-points.md)<br/>                                       | <span data-ttu-id="0b6c7-122">Décrit les points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-122">Describes reparse points.</span></span><br/>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="0b6c7-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b6c7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b6c7-124">Informations de référence sur la gestion d’annuaire</span><span class="sxs-lookup"><span data-stu-id="0b6c7-124">Directory Management Reference</span></span>](directory-management-reference.md)
</dt> </dl>

 

 




