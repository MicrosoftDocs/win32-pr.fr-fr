---
description: Une fois que la file d’attente a terminé la validation de ses opérations, elle doit être fermée à l’aide de la fonction SetupCloseFileQueue avec le descripteur créé par SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Fermeture de la file d’attente de fichiers et du fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539135"
---
# <a name="closing-the-file-queue-and-inf-file"></a><span data-ttu-id="42ba0-103">Fermeture de la file d’attente de fichiers et du fichier INF</span><span class="sxs-lookup"><span data-stu-id="42ba0-103">Closing the File Queue and INF File</span></span>

<span data-ttu-id="42ba0-104">Une fois que la file d’attente a terminé la validation de ses opérations, elle doit être fermée à l’aide de la fonction [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) avec le descripteur créé par [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="42ba0-104">After the queue has finished committing its operations, it should be closed using the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span> <span data-ttu-id="42ba0-105">Le rappel de file d’attente par défaut doit être détruit et recréé pour qu’une autre file d’attente puisse être validée.</span><span class="sxs-lookup"><span data-stu-id="42ba0-105">The default queue callback must be destroyed and recreated before another queue can be committed.</span></span>

<span data-ttu-id="42ba0-106">Si un contexte par défaut a été initialisé pour une utilisation par la routine de rappel par défaut, il doit également être arrêté en appelant la fonction [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="42ba0-106">If a default context was initiated for use by the default callback routine, it should also be terminated by calling the [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) function.</span></span> <span data-ttu-id="42ba0-107">Le *contexte* est un pointeur vers la structure retournée par la fonction [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="42ba0-107">The *Context* is a pointer to the structure returned by the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) function.</span></span>

<span data-ttu-id="42ba0-108">Lorsque l’accès aux informations INF n’est plus nécessaire, appelez la fonction [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) avec le descripteur créé par [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) pour libérer des ressources système.</span><span class="sxs-lookup"><span data-stu-id="42ba0-108">When access to the INF information is no longer needed, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) to free system resources.</span></span>

 

 



