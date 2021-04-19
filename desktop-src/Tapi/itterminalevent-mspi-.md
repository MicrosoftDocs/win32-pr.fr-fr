---
description: "Quand la méthode ITTAPIEventNotification :: Event retourne l' \\_ événement TAPI égal au \\_ Terminal te, les méthodes exposées par l’interface ITTerminalEvent peuvent être utilisées pour récupérer des informations concernant l’événement terminal qui s’est produit, si un MSP existe."
ms.assetid: 5277776e-0471-41b6-b662-4346a9d237ec
title: ITTerminalEvent (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593b9a7d048db9843825ccde8b22d0585a0c07fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534007"
---
# <a name="itterminalevent-mspi"></a><span data-ttu-id="5f780-103">ITTerminalEvent (MSPI)</span><span class="sxs-lookup"><span data-stu-id="5f780-103">ITTerminalEvent (MSPI)</span></span>

<span data-ttu-id="5f780-104">Quand la méthode [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) retourne [**l' \_ événement TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) égal **au \_ Terminal te**, les méthodes exposées par l’interface **ITTerminalEvent** peuvent être utilisées pour récupérer des informations concernant l’événement terminal qui s’est produit, si un MSP existe.</span><span class="sxs-lookup"><span data-stu-id="5f780-104">When the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method returns [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_TERMINAL**, the methods exposed by the **ITTerminalEvent** interface can be used to retrieve information concerning the terminal event that has occurred, if an MSP exists.</span></span>

<span data-ttu-id="5f780-105">L’interface **ITTerminalEvent** est implémentée par un MSP et n’est pas disponible s’il n’existe aucun fournisseur de services multimédias associé à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5f780-105">The **ITTerminalEvent** interface is implemented by an MSP and is not available if there is no media service provider associated with the address.</span></span> <span data-ttu-id="5f780-106">Pour plus d’informations sur cette interface, consultez **ITTerminalEvent** dans la section de l’interface MSP.</span><span class="sxs-lookup"><span data-stu-id="5f780-106">Please see **ITTerminalEvent** in the MSP Interface section for details on this interface.</span></span>

 

 



