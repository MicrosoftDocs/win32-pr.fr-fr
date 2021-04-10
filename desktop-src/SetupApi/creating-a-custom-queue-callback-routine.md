---
description: En plus d’utiliser le rappel de file d’attente par défaut, vous pouvez écrire une routine de rappel personnalisée.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Création d’une routine de rappel de file d’attente personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866941"
---
# <a name="creating-a-custom-queue-callback-routine"></a><span data-ttu-id="f75b2-103">Création d’une routine de rappel de file d’attente personnalisée</span><span class="sxs-lookup"><span data-stu-id="f75b2-103">Creating a Custom Queue Callback Routine</span></span>

<span data-ttu-id="f75b2-104">En plus d’utiliser le rappel de file d’attente par défaut, vous pouvez écrire une routine de rappel personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f75b2-104">In addition to using the default queue callback, you can write a custom callback routine.</span></span> <span data-ttu-id="f75b2-105">Cette fonction doit avoir la même forme que [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="f75b2-105">This function must have the same form as [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="f75b2-106">Cela est utile si vous avez besoin d’une routine de rappel pour gérer une notification de manière différente de celle fournie par la routine de rappel de file d’attente par défaut.</span><span class="sxs-lookup"><span data-stu-id="f75b2-106">This is useful if you need a callback routine to handle a notification in a manner other than that provided by the default queue callback routine.</span></span>

<span data-ttu-id="f75b2-107">Si seule une petite partie du comportement de la routine de rappel de la file d’attente par défaut doit être modifiée, vous pouvez créer une routine de rappel personnalisée pour filtrer les notifications, en gérant uniquement celles qui requièrent un comportement spécial et en appelant [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) pour les autres.</span><span class="sxs-lookup"><span data-stu-id="f75b2-107">If only a small portion of the default queue callback routine's behavior needs to be changed, you can create a custom callback routine to filter the notifications, handling only those that require special behavior and calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) for the others.</span></span>

<span data-ttu-id="f75b2-108">Par exemple, si vous souhaitez gérer les erreurs de suppression de fichier personnalisées, vous pouvez créer une fonction de rappel personnalisée, *MyCallBack*.</span><span class="sxs-lookup"><span data-stu-id="f75b2-108">For example, if you wanted to custom-handle file delete errors, you could create a custom callback function, *MyCallback*.</span></span> <span data-ttu-id="f75b2-109">Cette fonction intercepte et traite les notifications [**\_ DELETEERROR SPFILENOTIFY**](spfilenotify-deleteerror.md) et appelle la fonction de rappel de file d’attente par défaut pour toutes les autres notifications.</span><span class="sxs-lookup"><span data-stu-id="f75b2-109">This function would intercept and process [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md) notifications, and call the default queue callback function for all other notifications.</span></span> <span data-ttu-id="f75b2-110">*MyCallBack* retourne une valeur pour les notifications d’erreur de suppression.</span><span class="sxs-lookup"><span data-stu-id="f75b2-110">*MyCallback* returns a value for the delete error notifications.</span></span> <span data-ttu-id="f75b2-111">Pour toutes les autres notifications, *MyCallBack* transmet la valeur que la routine de rappel de file d’attente par défaut a renvoyée à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f75b2-111">For all other notifications, *MyCallback* passes whatever value the default queue callback routine returned to the queue.</span></span>

<span data-ttu-id="f75b2-112">Ce déroulement du contrôle est illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="f75b2-112">This flow of control is illustrated in the following diagram.</span></span>

![flèches et zones présentant le workflow pour une fonction de rappel personnalisée](images/callback.png)

> [!IMPORTANT]
> <span data-ttu-id="f75b2-114">Si la fonction de rappel personnalisé appelle la routine de rappel de file d’attente par défaut, elle doit passer le pointeur void retourné par [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) à la routine de rappel par défaut.</span><span class="sxs-lookup"><span data-stu-id="f75b2-114">If the custom callback function calls the default queue callback routine, it must pass the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) to the default callback routine.</span></span>

 

 

 
