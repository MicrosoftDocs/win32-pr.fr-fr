---
description: Un processus enfant peut hériter de handles de son processus parent. Un handle hérité est valide uniquement dans le contexte du processus enfant. Pour permettre à un processus enfant d’hériter des handles ouverts de son processus parent, procédez comme suit.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Gérer l’héritage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545088"
---
# <a name="handle-inheritance"></a><span data-ttu-id="52ab2-105">Gérer l’héritage</span><span class="sxs-lookup"><span data-stu-id="52ab2-105">Handle Inheritance</span></span>

<span data-ttu-id="52ab2-106">Un processus enfant peut hériter de handles de son processus parent.</span><span class="sxs-lookup"><span data-stu-id="52ab2-106">A child process can inherit handles from its parent process.</span></span> <span data-ttu-id="52ab2-107">Un handle hérité est valide uniquement dans le contexte du processus enfant.</span><span class="sxs-lookup"><span data-stu-id="52ab2-107">An inherited handle is valid only in the context of the child process.</span></span> <span data-ttu-id="52ab2-108">Pour permettre à un processus enfant d’hériter des handles ouverts de son processus parent, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="52ab2-108">To enable a child process to inherit open handles from its parent process, use the following steps.</span></span>

1.  <span data-ttu-id="52ab2-109">Créez le descripteur avec le membre **bInheritHandle** de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="52ab2-109">Create the handle with the **bInheritHandle** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure set to **TRUE**.</span></span>
2.  <span data-ttu-id="52ab2-110">Créez le processus enfant à l’aide de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , avec le paramètre *BInheritHandles* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="52ab2-110">Create the child process using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, with the *bInheritHandles* parameter set to **TRUE**.</span></span>

<span data-ttu-id="52ab2-111">La fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplique un handle à utiliser dans le processus en cours ou dans un autre processus.</span><span class="sxs-lookup"><span data-stu-id="52ab2-111">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function duplicates a handle to be used in the current process or in another process.</span></span> <span data-ttu-id="52ab2-112">Si une application duplique l’un de ses descripteurs pour un autre processus, le handle dupliqué est valide uniquement dans le contexte de l’autre processus.</span><span class="sxs-lookup"><span data-stu-id="52ab2-112">If an application duplicates one of its handles for another process, the duplicated handle is valid only in the context of the other process.</span></span>

<span data-ttu-id="52ab2-113">Un handle dupliqué ou un handle hérité est une valeur unique, mais il fait référence au même objet que le handle d’origine.</span><span class="sxs-lookup"><span data-stu-id="52ab2-113">A duplicated or inherited handle is a unique value, but it refers to the same object as the original handle.</span></span> <span data-ttu-id="52ab2-114">Les processus peuvent hériter ou dupliquer des handles vers les types d’objets suivants :</span><span class="sxs-lookup"><span data-stu-id="52ab2-114">Processes can inherit or duplicate handles to the following types of objects:</span></span>

-   <span data-ttu-id="52ab2-115">Jeton d'accès</span><span class="sxs-lookup"><span data-stu-id="52ab2-115">Access Token</span></span>
-   <span data-ttu-id="52ab2-116">Appareil de communication</span><span class="sxs-lookup"><span data-stu-id="52ab2-116">Communications device</span></span>
-   <span data-ttu-id="52ab2-117">Entrée de la console</span><span class="sxs-lookup"><span data-stu-id="52ab2-117">Console input</span></span>
-   <span data-ttu-id="52ab2-118">Mémoire tampon d’écran de la console</span><span class="sxs-lookup"><span data-stu-id="52ab2-118">Console screen buffer</span></span>
-   <span data-ttu-id="52ab2-119">Bureau</span><span class="sxs-lookup"><span data-stu-id="52ab2-119">Desktop</span></span>
-   <span data-ttu-id="52ab2-120">Répertoire</span><span class="sxs-lookup"><span data-stu-id="52ab2-120">Directory</span></span>
-   <span data-ttu-id="52ab2-121">Événement</span><span class="sxs-lookup"><span data-stu-id="52ab2-121">Event</span></span>
-   <span data-ttu-id="52ab2-122">Fichier</span><span class="sxs-lookup"><span data-stu-id="52ab2-122">File</span></span>
-   <span data-ttu-id="52ab2-123">Mappage de fichiers</span><span class="sxs-lookup"><span data-stu-id="52ab2-123">File mapping</span></span>
-   <span data-ttu-id="52ab2-124">Travail</span><span class="sxs-lookup"><span data-stu-id="52ab2-124">Job</span></span>
-   <span data-ttu-id="52ab2-125">Mailslots</span><span class="sxs-lookup"><span data-stu-id="52ab2-125">Mailslot</span></span>
-   <span data-ttu-id="52ab2-126">Mutex</span><span class="sxs-lookup"><span data-stu-id="52ab2-126">Mutex</span></span>
-   <span data-ttu-id="52ab2-127">Pipe</span><span class="sxs-lookup"><span data-stu-id="52ab2-127">Pipe</span></span>
-   <span data-ttu-id="52ab2-128">Process</span><span class="sxs-lookup"><span data-stu-id="52ab2-128">Process</span></span>
-   <span data-ttu-id="52ab2-129">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="52ab2-129">Registry key</span></span>
-   <span data-ttu-id="52ab2-130">Semaphore</span><span class="sxs-lookup"><span data-stu-id="52ab2-130">Semaphore</span></span>
-   <span data-ttu-id="52ab2-131">Prise</span><span class="sxs-lookup"><span data-stu-id="52ab2-131">Socket</span></span>
-   <span data-ttu-id="52ab2-132">Thread</span><span class="sxs-lookup"><span data-stu-id="52ab2-132">Thread</span></span>
-   <span data-ttu-id="52ab2-133">Minuteur</span><span class="sxs-lookup"><span data-stu-id="52ab2-133">Timer</span></span>
-   <span data-ttu-id="52ab2-134">Station Windows</span><span class="sxs-lookup"><span data-stu-id="52ab2-134">Window station</span></span>

<span data-ttu-id="52ab2-135">Tous les autres objets sont privés pour le processus qui les a créés ; leurs handles d’objet ne peuvent pas être dupliqués ou hérités.</span><span class="sxs-lookup"><span data-stu-id="52ab2-135">All other objects are private to the process that created them; their object handles cannot be duplicated or inherited.</span></span>

<span data-ttu-id="52ab2-136">Pour plus d’informations, consultez [Héritage](/windows/desktop/ProcThread/inheritance).</span><span class="sxs-lookup"><span data-stu-id="52ab2-136">For more information, see [Inheritance](/windows/desktop/ProcThread/inheritance).</span></span>

 

 
