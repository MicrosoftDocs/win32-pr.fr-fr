---
description: Décrit les liens physiques et les jonctions.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Liens physiques et jonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545092"
---
# <a name="hard-links-and-junctions"></a><span data-ttu-id="659ef-103">Liens physiques et jonctions</span><span class="sxs-lookup"><span data-stu-id="659ef-103">Hard Links and Junctions</span></span>

<span data-ttu-id="659ef-104">Il existe trois types de liens de fichiers pris en charge dans le système de fichiers NTFS : les liens physiques, les jonctions et les liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="659ef-104">There are three types of file links supported in the NTFS file system: hard links, junctions, and symbolic links.</span></span> <span data-ttu-id="659ef-105">Cette rubrique est une vue d’ensemble des liens physiques et des jonctions.</span><span class="sxs-lookup"><span data-stu-id="659ef-105">This topic is an overview of hard links and junctions.</span></span> <span data-ttu-id="659ef-106">Pour plus d’informations sur les liens symboliques, consultez [création de liens symboliques](creating-symbolic-links.md).</span><span class="sxs-lookup"><span data-stu-id="659ef-106">For information about symbolic links, see [Creating Symbolic Links](creating-symbolic-links.md).</span></span>

## <a name="hard-links"></a><span data-ttu-id="659ef-107">Liens physiques</span><span class="sxs-lookup"><span data-stu-id="659ef-107">Hard Links</span></span>

<span data-ttu-id="659ef-108">Un *lien physique* est la représentation de système de fichiers d’un fichier par lequel plusieurs chemins d’accès font référence à un seul fichier dans le même volume.</span><span class="sxs-lookup"><span data-stu-id="659ef-108">A *hard link* is the file system representation of a file by which more than one path references a single file in the same volume.</span></span> <span data-ttu-id="659ef-109">Pour créer un lien physique, utilisez la fonction [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) .</span><span class="sxs-lookup"><span data-stu-id="659ef-109">To create a hard link, use the [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) function.</span></span> <span data-ttu-id="659ef-110">Toutes les modifications apportées à ce fichier sont instantanément visibles par les applications qui y accèdent via les liens physiques qui y font référence.</span><span class="sxs-lookup"><span data-stu-id="659ef-110">Any changes to that file are instantly visible to applications that access it through the hard links that reference it.</span></span> <span data-ttu-id="659ef-111">Toutefois, la taille de l’entrée de répertoire et les informations d’attribut sont mises à jour uniquement pour le lien par le biais duquel la modification a été apportée.</span><span class="sxs-lookup"><span data-stu-id="659ef-111">However, the directory entry size and attribute information is updated only for the link through which the change was made.</span></span> <span data-ttu-id="659ef-112">Notez que les attributs du fichier sont reflétés dans chaque lien physique vers ce fichier, et les modifications apportées aux attributs de ce fichier sont propagées à tous les liens physiques.</span><span class="sxs-lookup"><span data-stu-id="659ef-112">Note that the attributes on the file are reflected in every hard link to that file, and changes to that file's attributes propagate to all the hard links.</span></span> <span data-ttu-id="659ef-113">Par exemple, si vous réinitialisez l’attribut READONLY sur un lien physique pour supprimer ce lien physique particulier, et qu’il y a plusieurs liens physiques vers le fichier réel, vous devrez réinitialiser le bit READONLY sur le fichier à partir de l’un des autres liens physiques pour ramener le fichier et tous les autres liens physiques à l’État READONLY.</span><span class="sxs-lookup"><span data-stu-id="659ef-113">For example if you reset the READONLY attribute on a hard link to delete that particular hard link, and there are multiple hard links to the actual file, then you will need to reset the READONLY bit on the file from one of the remaining hard links to bring the file and all remaining hard links back to the READONLY state.</span></span>

<span data-ttu-id="659ef-114">Par exemple, dans un système où C : et D : sont des lecteurs locaux et Z : est un lecteur réseau mappé à \\ \\ Fred \\ share, les références suivantes sont autorisées en tant que lien physique :</span><span class="sxs-lookup"><span data-stu-id="659ef-114">For example, in a system where C: and D: are local drives and Z: is a network drive mapped to \\\\fred\\share, the following references are permitted as a hard link:</span></span>

-   <span data-ttu-id="659ef-115">C : \\ dira \\ethel.txt lié à c : \\ DIRB \\ DIRC \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="659ef-115">C:\\dira\\ethel.txt linked to C:\\dirb\\dirc\\lucy.txt</span></span>
-   <span data-ttu-id="659ef-116">D : \\ dir1 \\tinker.txt à d : \\ dir2 \\ DirX \\bell.txt</span><span class="sxs-lookup"><span data-stu-id="659ef-116">D:\\dir1\\tinker.txt to D:\\dir2\\dirx\\bell.txt</span></span>
-   <span data-ttu-id="659ef-117">C : \\ DirY \\ Bob. bak lié à c : \\ dir2 \\mina.txt</span><span class="sxs-lookup"><span data-stu-id="659ef-117">C:\\diry\\bob.bak linked to C:\\dir2\\mina.txt</span></span>

<span data-ttu-id="659ef-118">Les éléments suivants ne sont pas :</span><span class="sxs-lookup"><span data-stu-id="659ef-118">The following are not:</span></span>

-   <span data-ttu-id="659ef-119">C : \\ dira lié à c : \\ DIRB</span><span class="sxs-lookup"><span data-stu-id="659ef-119">C:\\dira linked to C:\\dirb</span></span>
-   <span data-ttu-id="659ef-120">C : \\ dira \\ethel.txt lié à D : \\ DIRB \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="659ef-120">C:\\dira\\ethel.txt linked to D:\\dirb\\lucy.txt</span></span>
-   <span data-ttu-id="659ef-121">C : \\ dira \\ethel.txt lié à Z : \\ DIRB \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="659ef-121">C:\\dira\\ethel.txt linked to Z:\\dirb\\lucy.txt</span></span>

<span data-ttu-id="659ef-122">Pour supprimer un lien physique, utilisez la fonction [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) .</span><span class="sxs-lookup"><span data-stu-id="659ef-122">To delete a hard link, use the [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function.</span></span> <span data-ttu-id="659ef-123">Vous pouvez supprimer des liens physiques dans n’importe quel ordre, quel que soit l’ordre dans lequel ils sont créés.</span><span class="sxs-lookup"><span data-stu-id="659ef-123">You can delete hard links in any order regardless of the order in which they are created.</span></span>

## <a name="junctions"></a><span data-ttu-id="659ef-124">Jonctions</span><span class="sxs-lookup"><span data-stu-id="659ef-124">Junctions</span></span>

<span data-ttu-id="659ef-125">Une *jonction* (également appelée *lien conditionnel*) diffère d’un lien physique dans la mesure où les objets de stockage qu’elle référencent sont des répertoires distincts et une jonction peut lier des répertoires situés sur des volumes locaux différents sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="659ef-125">A *junction* (also called a *soft link*) differs from a hard link in that the storage objects it references are separate directories, and a junction can link directories located on different local volumes on the same computer.</span></span> <span data-ttu-id="659ef-126">Dans le cas contraire, les jonctions fonctionnent de la même façon que les liens physiques.</span><span class="sxs-lookup"><span data-stu-id="659ef-126">Otherwise, junctions operate identically to hard links.</span></span> <span data-ttu-id="659ef-127">Les jonctions sont implémentées par le biais de [points d’analyse](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="659ef-127">Junctions are implemented through [reparse points](reparse-points.md).</span></span>

<span data-ttu-id="659ef-128">En supposant les mêmes conditions dans la section des liens physiques, les références suivantes sont autorisées en tant que jonctions :</span><span class="sxs-lookup"><span data-stu-id="659ef-128">Assuming the same conditions in the Hard Links section, the following references are permitted as junctions:</span></span>

-   <span data-ttu-id="659ef-129">C : \\ dira lié à c : \\ DIRB \\ DIRC</span><span class="sxs-lookup"><span data-stu-id="659ef-129">C:\\dira linked to C:\\dirb\\dirc</span></span>
-   <span data-ttu-id="659ef-130">C : \\ DirX lié à D : \\ DirY</span><span class="sxs-lookup"><span data-stu-id="659ef-130">C:\\dirx linked to D:\\diry</span></span>

<span data-ttu-id="659ef-131">Les éléments suivants ne sont pas :</span><span class="sxs-lookup"><span data-stu-id="659ef-131">The following are not:</span></span>

-   <span data-ttu-id="659ef-132">C : \\ dira \\one.txt lié à c : \\ DIRB \\two.txt</span><span class="sxs-lookup"><span data-stu-id="659ef-132">C:\\dira\\one.txt linked to C:\\dirb\\two.txt</span></span>
-   <span data-ttu-id="659ef-133">C : \\ dir1 lié à Z : \\ dir2</span><span class="sxs-lookup"><span data-stu-id="659ef-133">C:\\dir1 linked to Z:\\dir2</span></span>

## <a name="related-topics"></a><span data-ttu-id="659ef-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="659ef-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="659ef-135">Création de liens symboliques</span><span class="sxs-lookup"><span data-stu-id="659ef-135">Creating Symbolic Links</span></span>](creating-symbolic-links.md)
</dt> </dl>

 

 



