---
description: Une application peut créer et supprimer par programmation des répertoires.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Création et suppression de répertoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114338"
---
# <a name="creating-and-deleting-directories"></a><span data-ttu-id="1be2d-103">Création et suppression de répertoires</span><span class="sxs-lookup"><span data-stu-id="1be2d-103">Creating and Deleting Directories</span></span>

<span data-ttu-id="1be2d-104">Une application peut créer et supprimer par programmation des répertoires.</span><span class="sxs-lookup"><span data-stu-id="1be2d-104">An application can programmatically create and delete directories.</span></span>

<span data-ttu-id="1be2d-105">Pour créer un répertoire, utilisez la fonction [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)ou [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="1be2d-105">To create a new directory, use the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa), or [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) function.</span></span> <span data-ttu-id="1be2d-106">Un répertoire reçoit le nom spécifié lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="1be2d-106">A directory is given the name specified when it is created.</span></span> <span data-ttu-id="1be2d-107">Les conventions pour nommer un répertoire obéissent aux conventions pour nommer un fichier.</span><span class="sxs-lookup"><span data-stu-id="1be2d-107">The conventions for naming a directory follow the conventions for naming a file.</span></span> <span data-ttu-id="1be2d-108">Pour obtenir une description de ces conventions, consultez [attribution d’un nom à un fichier](naming-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="1be2d-108">For a description of these conventions, see [Naming a File](naming-a-file.md).</span></span>

<span data-ttu-id="1be2d-109">Pour supprimer un répertoire existant, utilisez la fonction [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) ou [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="1be2d-109">To delete an existing directory, use the [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) or [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) function.</span></span> <span data-ttu-id="1be2d-110">Avant de supprimer un répertoire, vous devez vous assurer que le répertoire est vide et que vous disposez du privilège supprimer l’accès pour le répertoire.</span><span class="sxs-lookup"><span data-stu-id="1be2d-110">Before removing a directory, you must ensure that the directory is empty and that you have the delete access privilege for the directory.</span></span> <span data-ttu-id="1be2d-111">Pour ce faire, appelez la fonction [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="1be2d-111">To do the latter, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span>

 

 
