---
description: L’interface ITTerminalSupport est exposée sur un objet d’adresse s’il existe un MSP. Les méthodes de cette interface permettent à une application de découvrir les terminaux disponibles et/ou d’en créer une, et d’obtenir des pointeurs vers les objets terminal requis.
ms.assetid: 39cb9734-3e70-4e37-9358-c638c6618c11
title: ITTerminalSupport (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63822f55742d5a4c7a0114abeb625f2393a51ae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526955"
---
# <a name="itterminalsupport-mspi"></a><span data-ttu-id="2ee9f-104">ITTerminalSupport (MSPI)</span><span class="sxs-lookup"><span data-stu-id="2ee9f-104">ITTerminalSupport (MSPI)</span></span>

<span data-ttu-id="2ee9f-105">L’interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) est exposée sur un [objet d’adresse](address-object.md) s’il existe un MSP.</span><span class="sxs-lookup"><span data-stu-id="2ee9f-105">The [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is exposed on an [Address object](address-object.md) if an MSP exists.</span></span> <span data-ttu-id="2ee9f-106">Les méthodes de cette interface permettent à une application de découvrir les terminaux disponibles et/ou d’en créer une, et d’obtenir des pointeurs vers les [objets terminal](terminal-object.md)requis.</span><span class="sxs-lookup"><span data-stu-id="2ee9f-106">The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required [Terminal objects](terminal-object.md).</span></span>

<span data-ttu-id="2ee9f-107">L’interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) est implémentée par un MSP et n’est pas disponible s’il n’existe aucun fournisseur de services multimédias associé à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="2ee9f-107">The [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is implemented by an MSP and is not available if there is no media service provider associated with the address.</span></span> <span data-ttu-id="2ee9f-108">Pour plus d’informations sur cette interface, consultez **ITTerminalSupport** dans la section de l’interface MSP.</span><span class="sxs-lookup"><span data-stu-id="2ee9f-108">Please see **ITTerminalSupport** in the MSP Interface section for details on this interface.</span></span>

 

 
