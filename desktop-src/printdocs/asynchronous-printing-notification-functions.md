---
description: Découvrez les fonctions utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Fonctions de notification d’impression asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394854"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="ef24a-103">Fonctions de notification d’impression asynchrone</span><span class="sxs-lookup"><span data-stu-id="ef24a-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="ef24a-104">Les fonctions suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.</span><span class="sxs-lookup"><span data-stu-id="ef24a-104">The following functions are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef24a-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="ef24a-105">In this section</span></span>



| <span data-ttu-id="ef24a-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="ef24a-106">Function</span></span>                                                                                        | <span data-ttu-id="ef24a-107">Description</span><span class="sxs-lookup"><span data-stu-id="ef24a-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef24a-108">**CreatePrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="ef24a-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="ef24a-109">Crée un canal de communication entre un composant d’impression hébergé par le spouleur d’impression, tel qu’un pilote d’impression ou un moniteur de port, et une application qui reçoit les notifications du composant.</span><span class="sxs-lookup"><span data-stu-id="ef24a-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="ef24a-110">**RegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="ef24a-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="ef24a-111">Permet à une application de s’inscrire aux notifications à partir de composants d’impression hébergés par le spouleur d’impression, tels que les pilotes d’imprimante, les processeurs d’impression et les moniteurs de port.</span><span class="sxs-lookup"><span data-stu-id="ef24a-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="ef24a-112">**UnRegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="ef24a-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="ef24a-113">Permet à une application qui s’est inscrite de recevoir des notifications des composants d’impression hébergés par le spouleur d’impression de se désinscrire.</span><span class="sxs-lookup"><span data-stu-id="ef24a-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




