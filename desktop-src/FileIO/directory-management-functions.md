---
description: Fonctions utilisées dans la gestion des répertoires.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Fonctions de gestion d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209905"
---
# <a name="directory-management-functions"></a><span data-ttu-id="2470c-103">Fonctions de gestion d’annuaire</span><span class="sxs-lookup"><span data-stu-id="2470c-103">Directory Management Functions</span></span>

<span data-ttu-id="2470c-104">Les fonctions suivantes sont utilisées dans la gestion des répertoires.</span><span class="sxs-lookup"><span data-stu-id="2470c-104">The following functions are used in directory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2470c-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2470c-105">In this section</span></span>



| <span data-ttu-id="2470c-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="2470c-106">Function</span></span>                                                                      | <span data-ttu-id="2470c-107">Description</span><span class="sxs-lookup"><span data-stu-id="2470c-107">Description</span></span>                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2470c-108">**CreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="2470c-108">**CreateDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | <span data-ttu-id="2470c-109">Crée un répertoire.</span><span class="sxs-lookup"><span data-stu-id="2470c-109">Creates a new directory.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="2470c-110">**CreateDirectoryEx**</span><span class="sxs-lookup"><span data-stu-id="2470c-110">**CreateDirectoryEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | <span data-ttu-id="2470c-111">Crée un répertoire avec les attributs d’un répertoire de modèles spécifié.</span><span class="sxs-lookup"><span data-stu-id="2470c-111">Creates a new directory with the attributes of a specified template directory.</span></span><br/>                                                                                 |
| [<span data-ttu-id="2470c-112">**CreateDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="2470c-112">**CreateDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | <span data-ttu-id="2470c-113">Crée un nouveau répertoire en tant qu’opération traitée avec les attributs d’un répertoire de modèles spécifié.</span><span class="sxs-lookup"><span data-stu-id="2470c-113">Creates a new directory as a transacted operation, with the attributes of a specified template directory.</span></span><br/>                                                      |
| [<span data-ttu-id="2470c-114">**FindCloseChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2470c-114">**FindCloseChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | <span data-ttu-id="2470c-115">Arrête la surveillance du handle de notification de modification.</span><span class="sxs-lookup"><span data-stu-id="2470c-115">Stops change notification handle monitoring.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="2470c-116">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2470c-116">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | <span data-ttu-id="2470c-117">Crée un handle de notification de modification et définit des conditions de filtre de notification de modification initiales.</span><span class="sxs-lookup"><span data-stu-id="2470c-117">Creates a change notification handle and sets up initial change notification filter conditions.</span></span><br/>                                                                |
| [<span data-ttu-id="2470c-118">**FindNextChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2470c-118">**FindNextChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | <span data-ttu-id="2470c-119">Demande que le système d’exploitation signale un handle de notification de modification la prochaine fois qu’il détecte une modification appropriée.</span><span class="sxs-lookup"><span data-stu-id="2470c-119">Requests that the operating system signal a change notification handle the next time it detects an appropriate change.</span></span><br/>                                         |
| [<span data-ttu-id="2470c-120">**GetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="2470c-120">**GetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | <span data-ttu-id="2470c-121">Récupère le répertoire actif pour le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="2470c-121">Retrieves the current directory for the current process.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2470c-122">**ReadDirectoryChangesExW**</span><span class="sxs-lookup"><span data-stu-id="2470c-122">**ReadDirectoryChangesExW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | <span data-ttu-id="2470c-123">Récupère des informations qui décrivent les modifications dans le répertoire spécifié, qui peuvent inclure des informations étendues si ce type d’informations est spécifié.</span><span class="sxs-lookup"><span data-stu-id="2470c-123">Retrieves information that describes the changes within the specified directory, which can include extended information if that information type is specified.</span></span><br/> |
| [<span data-ttu-id="2470c-124">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="2470c-124">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | <span data-ttu-id="2470c-125">Récupère des informations qui décrivent les modifications dans le répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="2470c-125">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                               |
| [<span data-ttu-id="2470c-126">**RemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="2470c-126">**RemoveDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | <span data-ttu-id="2470c-127">Supprime un répertoire vide existant.</span><span class="sxs-lookup"><span data-stu-id="2470c-127">Deletes an existing empty directory.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="2470c-128">**RemoveDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="2470c-128">**RemoveDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | <span data-ttu-id="2470c-129">Supprime un répertoire vide existant en tant qu’opération traitée.</span><span class="sxs-lookup"><span data-stu-id="2470c-129">Deletes an existing empty directory as a transacted operation.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="2470c-130">**SetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="2470c-130">**SetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | <span data-ttu-id="2470c-131">Modifie le répertoire actif pour le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="2470c-131">Changes the current directory for the current process.</span></span><br/>                                                                                                         |



 

 

 




