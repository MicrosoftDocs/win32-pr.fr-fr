---
description: L’objet CallHub expose des méthodes qui récupèrent des informations relatives aux participants dans un appel multifournisseur.
ms.assetid: 928c3abb-1b4e-42f3-a8cc-41889ad573ed
title: Interfaces d’objet CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe448c7f559d38bef671144c1a6457f43d4a6b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866590"
---
# <a name="callhub-object-interfaces"></a><span data-ttu-id="dbd93-103">Interfaces d’objet CallHub</span><span class="sxs-lookup"><span data-stu-id="dbd93-103">CallHub Object Interfaces</span></span>

<span data-ttu-id="dbd93-104">L' [objet CallHub](callhub-object.md) expose des méthodes qui récupèrent des informations relatives aux participants dans un appel multifournisseur.</span><span class="sxs-lookup"><span data-stu-id="dbd93-104">The [CallHub object](callhub-object.md) exposes methods that retrieve information concerning participants in a multi-party call.</span></span>

<span data-ttu-id="dbd93-105">Les interfaces [**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) et [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) ne sont pas directement exposées sur l’objet CallHub, mais sont étroitement liées à celle-ci et sont répertoriées ici pour des raisons de commodité de référence.</span><span class="sxs-lookup"><span data-stu-id="dbd93-105">The [**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) and [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) interfaces are not directly exposed on the CallHub Object, but are tightly related to it and are listed here for reference convenience.</span></span>



| <span data-ttu-id="dbd93-106">Interface</span><span class="sxs-lookup"><span data-stu-id="dbd93-106">Interface</span></span>                                | <span data-ttu-id="dbd93-107">Description</span><span class="sxs-lookup"><span data-stu-id="dbd93-107">Description</span></span>                                                           |
|------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="dbd93-108">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="dbd93-108">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)           | <span data-ttu-id="dbd93-109">Fournit des méthodes pour récupérer des informations relatives à un objet CallHub.</span><span class="sxs-lookup"><span data-stu-id="dbd93-109">Provides methods to retrieve information concerning a CallHub object.</span></span> |
| [<span data-ttu-id="dbd93-110">**ITCallHubEvent**</span><span class="sxs-lookup"><span data-stu-id="dbd93-110">**ITCallHubEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) | <span data-ttu-id="dbd93-111">Utilisé pour obtenir des informations concernant les événements CallHub.</span><span class="sxs-lookup"><span data-stu-id="dbd93-111">Used to acquire information concerning CallHub events.</span></span>                |
| [<span data-ttu-id="dbd93-112">**IEnumCallHub**</span><span class="sxs-lookup"><span data-stu-id="dbd93-112">**IEnumCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub)     | <span data-ttu-id="dbd93-113">Énumère [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span><span class="sxs-lookup"><span data-stu-id="dbd93-113">Enumerates [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span></span>                            |



 

 

 



