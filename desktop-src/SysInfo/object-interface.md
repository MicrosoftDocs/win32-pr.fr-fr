---
description: 'Windows fournit des fonctions qui effectuent les tâches suivantes :'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interface d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485248"
---
# <a name="object-interface"></a><span data-ttu-id="84b2c-103">Interface d’objet</span><span class="sxs-lookup"><span data-stu-id="84b2c-103">Object Interface</span></span>

<span data-ttu-id="84b2c-104">Windows fournit des fonctions qui effectuent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="84b2c-104">Windows provides functions that perform the following tasks:</span></span>

-   <span data-ttu-id="84b2c-105">Créer un objet</span><span class="sxs-lookup"><span data-stu-id="84b2c-105">Create an object</span></span>
-   <span data-ttu-id="84b2c-106">Obtient un handle d’objet</span><span class="sxs-lookup"><span data-stu-id="84b2c-106">Get an object handle</span></span>
-   <span data-ttu-id="84b2c-107">Obtenir des informations sur l’objet</span><span class="sxs-lookup"><span data-stu-id="84b2c-107">Get information about the object</span></span>
-   <span data-ttu-id="84b2c-108">Définir les informations relatives à l’objet</span><span class="sxs-lookup"><span data-stu-id="84b2c-108">Set information about the object</span></span>
-   <span data-ttu-id="84b2c-109">Fermer le descripteur d’objet</span><span class="sxs-lookup"><span data-stu-id="84b2c-109">Close the object handle</span></span>
-   <span data-ttu-id="84b2c-110">Détruire l’objet</span><span class="sxs-lookup"><span data-stu-id="84b2c-110">Destroy the object</span></span>

<span data-ttu-id="84b2c-111">Certaines de ces tâches ne sont pas nécessaires pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="84b2c-111">Some of these tasks are not necessary for each object.</span></span> <span data-ttu-id="84b2c-112">Certaines de ces tâches sont combinées pour certains objets.</span><span class="sxs-lookup"><span data-stu-id="84b2c-112">Some of these tasks are combined for certain objects.</span></span> <span data-ttu-id="84b2c-113">Par exemple, une application peut créer un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="84b2c-113">For example, an application can create an event object.</span></span> <span data-ttu-id="84b2c-114">D’autres applications peuvent ouvrir l’événement pour obtenir un descripteur unique de cet objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="84b2c-114">Other applications can open the event to obtain a unique handle to this event object.</span></span> <span data-ttu-id="84b2c-115">À mesure que chaque application se termine à l’aide de l’événement, elle ferme son handle vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="84b2c-115">As each application finishes using the event, it closes its handle to the object.</span></span> <span data-ttu-id="84b2c-116">Lorsqu’il n’y a aucun descripteur ouvert restant pour l’objet d’événement, le système détruit l’objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="84b2c-116">When there are no remaining open handles to the event object, the system destroys the event object.</span></span> <span data-ttu-id="84b2c-117">En revanche, une application peut obtenir un handle vers un objet Window existant.</span><span class="sxs-lookup"><span data-stu-id="84b2c-117">In contrast, an application can obtain a handle to an existing window object.</span></span> <span data-ttu-id="84b2c-118">Lorsque l’objet Window n’est plus nécessaire, l’application doit détruire l’objet, ce qui invalide le handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="84b2c-118">When the window object is no longer needed, the application must destroy the object, which invalidates the window handle.</span></span>

<span data-ttu-id="84b2c-119">Parfois, un objet reste en mémoire après la fermeture de tous les handles d’objet.</span><span class="sxs-lookup"><span data-stu-id="84b2c-119">Occasionally, an object remains in memory after all object handles have been closed.</span></span> <span data-ttu-id="84b2c-120">Par exemple, un thread peut créer un objet d’événement et attendre le descripteur d’événement.</span><span class="sxs-lookup"><span data-stu-id="84b2c-120">For example, a thread could create an event object and wait on the event handle.</span></span> <span data-ttu-id="84b2c-121">Pendant que le thread attend, un autre thread peut fermer le même handle d’objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="84b2c-121">While the thread is waiting, another thread could close the same event object handle.</span></span> <span data-ttu-id="84b2c-122">L’objet d’événement reste en mémoire, sans aucun handle d’objet d’événement, jusqu’à ce que l’objet d’événement soit défini sur l’état signalé et que l’opération d’attente soit terminée.</span><span class="sxs-lookup"><span data-stu-id="84b2c-122">The event object remains in memory, without any event object handles, until the event object is set to the signaled state and the wait operation is completed.</span></span> <span data-ttu-id="84b2c-123">À ce stade, le système supprime l’objet de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="84b2c-123">At this time, the system removes the object from memory.</span></span>

<span data-ttu-id="84b2c-124">Les handles et les objets consomment de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="84b2c-124">Handles and objects consume memory.</span></span> <span data-ttu-id="84b2c-125">Par conséquent, pour préserver les performances du système, vous devez fermer les handles et supprimer les objets dès qu’ils ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="84b2c-125">Therefore, to preserve system performance, you should close handles and delete objects as soon as they are no longer needed.</span></span> <span data-ttu-id="84b2c-126">Si vous ne le faites pas, votre application peut nuire aux performances du système, en raison d’une utilisation excessive du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="84b2c-126">If you do not do this, your application can hurt system performance, due to excessive use of the paging file.</span></span>

<span data-ttu-id="84b2c-127">Lorsqu’un processus se termine, le système ferme automatiquement les handles et supprime les objets créés par le processus.</span><span class="sxs-lookup"><span data-stu-id="84b2c-127">When a process terminates, the system automatically closes handles and deletes objects created by the process.</span></span> <span data-ttu-id="84b2c-128">Toutefois, lorsqu’un thread se termine, le système ne ferme généralement pas les handles ou ne supprime pas les objets.</span><span class="sxs-lookup"><span data-stu-id="84b2c-128">However, when a thread terminates, the system usually does not close handles or delete objects.</span></span> <span data-ttu-id="84b2c-129">Les seules exceptions sont les objets Window, Hook, position de fenêtre et conversation DDE (Dynamic Data Exchange). ces objets sont détruits lorsque le thread de création se termine.</span><span class="sxs-lookup"><span data-stu-id="84b2c-129">The only exceptions are window, hook, window position, and dynamic data exchange (DDE) conversation objects; these objects are destroyed when the creating thread terminates.</span></span>

 

 



