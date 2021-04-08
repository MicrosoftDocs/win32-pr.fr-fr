---
title: Registre IAgent
description: Registre IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840125"
---
# <a name="iagentregister"></a><span data-ttu-id="ce4d4-103">IAgent :: Register</span><span class="sxs-lookup"><span data-stu-id="ce4d4-103">IAgent::Register</span></span>

<span data-ttu-id="ce4d4-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ce4d4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

<span data-ttu-id="ce4d4-105">Inscrit un récepteur de notifications pour l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="ce4d4-105">Registers a notification sink for the client application.</span></span>

-   <span data-ttu-id="ce4d4-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ce4d4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ce4d4-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="ce4d4-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="ce4d4-108">Adresse de [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) pour votre interface du récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="ce4d4-108">Address of [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) for your notification sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="ce4d4-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span><span class="sxs-lookup"><span data-stu-id="ce4d4-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="ce4d4-110">Adresse de l’ID du récepteur de notification (utilisée pour annuler l’inscription du récepteur de notification).</span><span class="sxs-lookup"><span data-stu-id="ce4d4-110">Address of notification sink ID (used to unregister the notification sink).</span></span>

</dd> </dl>

<span data-ttu-id="ce4d4-111">Vous devez inscrire votre récepteur de notification (également appelé récepteur de notification ou récepteur d’événements) pour recevoir des événements du serveur Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ce4d4-111">You need to register your notification sink (also known as a notify sink or event sink) to receive events from the Microsoft Agent server.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce4d4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce4d4-112">See Also</span></span>

[<span data-ttu-id="ce4d4-113">**IAgent :: Unregister**</span><span class="sxs-lookup"><span data-stu-id="ce4d4-113">**IAgent::Unregister**</span></span>](iagent--unregister.md)


 

 




