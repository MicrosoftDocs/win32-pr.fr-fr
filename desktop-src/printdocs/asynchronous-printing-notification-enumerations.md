---
description: Les énumérations suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Énumérations de notification d’impression asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2baf2a4476ac858a883dda55b2864a79d78cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517691"
---
# <a name="asynchronous-printing-notification-enumerations"></a><span data-ttu-id="af86a-103">Énumérations de notification d’impression asynchrone</span><span class="sxs-lookup"><span data-stu-id="af86a-103">Asynchronous Printing Notification Enumerations</span></span>

<span data-ttu-id="af86a-104">Les énumérations suivantes sont utilisées dans la communication asynchrone entre les applications et les composants qui sont hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.</span><span class="sxs-lookup"><span data-stu-id="af86a-104">The following enumerations are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af86a-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="af86a-105">In this section</span></span>



| <span data-ttu-id="af86a-106">Énumération</span><span class="sxs-lookup"><span data-stu-id="af86a-106">Enumeration</span></span>                                                                               | <span data-ttu-id="af86a-107">Description</span><span class="sxs-lookup"><span data-stu-id="af86a-107">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af86a-108">**PrintAsyncNotifyConversationStyle**</span><span class="sxs-lookup"><span data-stu-id="af86a-108">**PrintAsyncNotifyConversationStyle**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | <span data-ttu-id="af86a-109">Spécifie si la communication est bidirectionnelle ou unidirectionnelle entre les applications et les composants hébergés par le spouleur d’impression, tels que les pilotes d’imprimante, les processeurs d’impression et les moniteurs de port.</span><span class="sxs-lookup"><span data-stu-id="af86a-109">Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.</span></span><br/>           |
| [<span data-ttu-id="af86a-110">**PrintAsyncNotifyError**</span><span class="sxs-lookup"><span data-stu-id="af86a-110">**PrintAsyncNotifyError**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | <span data-ttu-id="af86a-111">Spécifie la partie du code d’erreur du **HRESULT** retourné après un échec de notification asynchrone.</span><span class="sxs-lookup"><span data-stu-id="af86a-111">Specifies the error code portion of the **HRESULT** returned after an asynchronous notification failure.</span></span><br/>                                                                                            |
| [<span data-ttu-id="af86a-112">**PrintAsyncNotifyUserFilter**</span><span class="sxs-lookup"><span data-stu-id="af86a-112">**PrintAsyncNotifyUserFilter**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | <span data-ttu-id="af86a-113">Spécifie si les notifications vont uniquement aux applications d’écoute associées au même utilisateur que l’expéditeur hébergé par le spouleur d’impression ou à un ensemble plus large d’applications d’écoute.</span><span class="sxs-lookup"><span data-stu-id="af86a-113">Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.</span></span><br/> |



 

 

 




