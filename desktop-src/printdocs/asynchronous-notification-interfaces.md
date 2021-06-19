---
description: En savoir plus sur les interfaces utilisées pour la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notification d’impression asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396094"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="c56cf-103">Interfaces de notification d’impression asynchrone</span><span class="sxs-lookup"><span data-stu-id="c56cf-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="c56cf-104">Les interfaces suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.</span><span class="sxs-lookup"><span data-stu-id="c56cf-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c56cf-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c56cf-105">In this section</span></span>



| <span data-ttu-id="c56cf-106">Interface</span><span class="sxs-lookup"><span data-stu-id="c56cf-106">Interface</span></span>                                                                     | <span data-ttu-id="c56cf-107">Description</span><span class="sxs-lookup"><span data-stu-id="c56cf-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c56cf-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="c56cf-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="c56cf-109">Crée et gère un canal de communication utilisé par les applications et les composants qui sont hébergés par le spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="c56cf-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="c56cf-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="c56cf-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="c56cf-111">Représente un canal de communication utilisé par les composants hébergés par le spouleur d’impression pour envoyer des notifications aux applications.</span><span class="sxs-lookup"><span data-stu-id="c56cf-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="c56cf-112">Si le canal est bidirectionnel, les applications peuvent utiliser le même canal pour renvoyer des réponses au composant.</span><span class="sxs-lookup"><span data-stu-id="c56cf-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="c56cf-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="c56cf-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="c56cf-114">Encapsule les données envoyées dans un canal de notification.</span><span class="sxs-lookup"><span data-stu-id="c56cf-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




