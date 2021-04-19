---
description: Considérations relatives à la programmation pour l’utilisation des liens symboliques.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considérations relatives à la programmation (systèmes de fichiers locaux)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106538435"
---
# <a name="programming-considerations-local-file-systems"></a><span data-ttu-id="82105-103">Considérations relatives à la programmation (systèmes de fichiers locaux)</span><span class="sxs-lookup"><span data-stu-id="82105-103">Programming Considerations (Local File Systems)</span></span>

<span data-ttu-id="82105-104">Gardez à l’esprit les considérations de programmation suivantes lorsque vous utilisez des liens symboliques :</span><span class="sxs-lookup"><span data-stu-id="82105-104">Keep the following programming considerations in mind when working with symbolic links:</span></span>

-   <span data-ttu-id="82105-105">Les liens symboliques peuvent pointer vers une cible inexistante.</span><span class="sxs-lookup"><span data-stu-id="82105-105">Symbolic links can point to a non-existent target.</span></span>
-   <span data-ttu-id="82105-106">Lorsque vous créez un lien symbolique, le système d’exploitation ne vérifie pas si la cible existe.</span><span class="sxs-lookup"><span data-stu-id="82105-106">When creating a symbolic link, the operating system does not check to see if the target exists.</span></span>
-   <span data-ttu-id="82105-107">Si une application tente d’ouvrir une cible inexistante, **le \_ fichier d’erreur \_ \_ introuvable** est retourné.</span><span class="sxs-lookup"><span data-stu-id="82105-107">If an application tries to open a non-existent target, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>
-   <span data-ttu-id="82105-108">Les liens symboliques sont des points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="82105-108">Symbolic links are reparse points.</span></span> <span data-ttu-id="82105-109">Pour plus d’informations, consultez [déterminer si un répertoire est un dossier monté](determining-whether-a-directory-is-a-volume-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="82105-109">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>
-   <span data-ttu-id="82105-110">Il y a un maximum de 63 points d’analyse (et par conséquent des liens symboliques) autorisés dans un chemin d’accès particulier.</span><span class="sxs-lookup"><span data-stu-id="82105-110">There is a maximum of 63 reparse points (and therefore symbolic links) allowed in a particular path.</span></span>

    <span data-ttu-id="82105-111">**Windows Server 2003 et Windows XP :** Il existe une limite de 31 points d’analyse sur un chemin d’accès donné.</span><span class="sxs-lookup"><span data-stu-id="82105-111">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82105-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82105-112">Related topics</span></span>

<dl> <span data-ttu-id="82105-113"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="82105-113"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="82105-114">Liens physiques et jonctions</span><span class="sxs-lookup"><span data-stu-id="82105-114">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> </dl>

 

 



