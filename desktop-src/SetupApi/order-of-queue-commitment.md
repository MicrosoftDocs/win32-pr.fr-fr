---
description: 'Lorsque la fonction SetupCommitFileQueue valide la file d’attente de fichiers, elle traite les opérations de fichiers dans l’ordre suivant : opérations de suppression de fichiers, opérations de changement de nom de fichier et enfin, opérations de copie de fichiers.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Ordre de validation des files d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865717"
---
# <a name="order-of-queue-commitment"></a><span data-ttu-id="fffca-103">Ordre de validation des files d’attente</span><span class="sxs-lookup"><span data-stu-id="fffca-103">Order of Queue Commitment</span></span>

<span data-ttu-id="fffca-104">Lorsque la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) valide la file d’attente de fichiers, elle traite les opérations de fichiers dans l’ordre suivant : opérations de suppression de fichiers, opérations de changement de nom de fichier et enfin, opérations de copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fffca-104">When the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function commits the file queue, it processes the file operations in the following order: file deletion operations, then file renaming operations, and finally, file copying operations.</span></span> <span data-ttu-id="fffca-105">Le schéma suivant illustre le cycle de vie du processus d’engagement d’une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fffca-105">The following outline illustrates the life cycle of a queue's commitment process.</span></span>

 

-   <span data-ttu-id="fffca-106">Démarrer la sous-file d’attente de suppression</span><span class="sxs-lookup"><span data-stu-id="fffca-106">start the delete subqueue</span></span>
    -   <span data-ttu-id="fffca-107">démarrer une opération de suppression de fichier <--répéter pour chaque</span><span class="sxs-lookup"><span data-stu-id="fffca-107">start a file delete operation <-- repeat for each</span></span>
    -   <span data-ttu-id="fffca-108">terminer une opération de suppression de fichier <--suppression de fichier en file d’attente</span><span class="sxs-lookup"><span data-stu-id="fffca-108">finish a file delete operation <-- queued file delete</span></span>
-   <span data-ttu-id="fffca-109">terminer la suppression de la sous-file d’attente</span><span class="sxs-lookup"><span data-stu-id="fffca-109">finish the delete subqueue</span></span>

<!-- -->

-   <span data-ttu-id="fffca-110">Démarrer la sous-file d’attente de renommage</span><span class="sxs-lookup"><span data-stu-id="fffca-110">start the rename subqueue</span></span>
    -   <span data-ttu-id="fffca-111">démarrer une opération de changement de nom de fichier <--répéter pour chaque</span><span class="sxs-lookup"><span data-stu-id="fffca-111">start a file rename operation <-- repeat for each</span></span>
    -   <span data-ttu-id="fffca-112">terminer une opération de suppression de fichier <--renommage de fichier en file d’attente</span><span class="sxs-lookup"><span data-stu-id="fffca-112">finish a file delete operation <-- queued file rename</span></span>
-   <span data-ttu-id="fffca-113">terminer la sous-file d’attente de renommage</span><span class="sxs-lookup"><span data-stu-id="fffca-113">finish the rename subqueue</span></span>

<!-- -->

-   <span data-ttu-id="fffca-114">Démarrer la copie subque</span><span class="sxs-lookup"><span data-stu-id="fffca-114">start the copy subque</span></span>
    -   <span data-ttu-id="fffca-115">démarrer une opération de copie de fichiers <--répéter pour chaque</span><span class="sxs-lookup"><span data-stu-id="fffca-115">start a file copy operation <-- repeat for each</span></span>
    -   <span data-ttu-id="fffca-116">terminer une opération de copie de fichiers <--copie de fichiers en file d’attente</span><span class="sxs-lookup"><span data-stu-id="fffca-116">finish a file copy operation <-- queued file copy</span></span>
    -   <span data-ttu-id="fffca-117">terminer la sous-file d’attente de copie</span><span class="sxs-lookup"><span data-stu-id="fffca-117">finish the copy subqueue</span></span>
-   <span data-ttu-id="fffca-118">terminer la file d’attente</span><span class="sxs-lookup"><span data-stu-id="fffca-118">finish the queue</span></span>

 

<span data-ttu-id="fffca-119">À chaque étape, ou si une erreur se produit, la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envoie une notification à la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="fffca-119">At each step, or if an error occurs, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function sends a notification to the callback routine.</span></span> <span data-ttu-id="fffca-120">La routine de rappel peut utiliser les informations envoyées par la file d’attente pour suivre la progression de l’installation et, si nécessaire, interagir avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fffca-120">The callback routine can use the information sent by the queue to track the installation progress and, if necessary, interact with the user.</span></span>

<span data-ttu-id="fffca-121">Par exemple, si une opération de copie de fichiers a besoin d’un fichier source qui n’était pas disponible dans le chemin d’accès actuel, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enverra une \_ notification NEEDMEDIA SPFILENOTIFY à la routine de rappel, ainsi que des informations sur le fichier et le support requis.</span><span class="sxs-lookup"><span data-stu-id="fffca-121">For example, if a file copy operation needed a source file that was not available at the current path, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) would send a SPFILENOTIFY\_NEEDMEDIA notification to the callback routine, along with information about the file and media required.</span></span> <span data-ttu-id="fffca-122">La routine de rappel peut utiliser ces informations pour générer une boîte de dialogue qui invite l’utilisateur à insérer le disque suivant en appelant [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span><span class="sxs-lookup"><span data-stu-id="fffca-122">The callback routine could use this information to generate a dialog box that prompts the user to insert the next disk by calling [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span></span>

<span data-ttu-id="fffca-123">Une routine de rappel de file d’attente par défaut, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), est incluse avec l’API d’installation.</span><span class="sxs-lookup"><span data-stu-id="fffca-123">A default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), is included with the Setup API.</span></span> <span data-ttu-id="fffca-124">Cette routine gère les notifications de file d’attente et génère des boîtes de dialogue d’erreur et des barres de progression pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="fffca-124">This routine handles queue notifications and generates error dialog boxes and progress bars for the installation.</span></span> <span data-ttu-id="fffca-125">Vous pouvez utiliser la routine de rappel de file d’attente par défaut, ou écrire une routine de rappel de filtre pour gérer un sous-ensemble des notifications et passer les autres à la routine de rappel de file d’attente par défaut.</span><span class="sxs-lookup"><span data-stu-id="fffca-125">You can use the default queue callback routine as it is, or write a filter callback routine to handle a subset of the notifications and pass the others on to the default queue callback routine.</span></span>

<span data-ttu-id="fffca-126">Si aucune des fonctionnalités de la routine de rappel ne répond à vos besoins, vous pouvez écrire une routine de rappel personnalisé autonome qui n’appelle pas la routine de rappel de file d’attente par défaut.</span><span class="sxs-lookup"><span data-stu-id="fffca-126">If none of the functionality of the callback routine suits your needs, you can write a self-contained custom callback routine that does not call the default queue callback routine.</span></span>

<span data-ttu-id="fffca-127">Pour plus d’informations sur les routines de rappel de file d’attente, consultez [routine de rappel de file d’attente par défaut](default-queue-callback-routine.md)et [création d’une routine de rappel de file d’attente personnalisée](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="fffca-127">For more information about queue callback routines, see [Default Queue Callback Routine](default-queue-callback-routine.md), and [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



