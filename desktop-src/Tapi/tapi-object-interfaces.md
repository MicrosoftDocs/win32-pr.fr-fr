---
description: L’objet TAPI est l’objet principal pour TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfaces d’objet TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535504"
---
# <a name="tapi-object-interfaces"></a><span data-ttu-id="9941d-103">Interfaces d’objet TAPI</span><span class="sxs-lookup"><span data-stu-id="9941d-103">TAPI Object Interfaces</span></span>

<span data-ttu-id="9941d-104">L' [objet TAPI](tapi-object.md) est l’objet principal pour TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="9941d-104">The [TAPI Object](tapi-object.md) is the main object for TAPI 3.</span></span>

<span data-ttu-id="9941d-105">L’interface [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) n’est pas directement exposée sur l’objet TAPI, mais est étroitement liée à celle-ci et est répertoriée ici pour des raisons de commodité de référence.</span><span class="sxs-lookup"><span data-stu-id="9941d-105">The [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) interface is not directly exposed on the TAPI Object, but is tightly related to it and is listed here for reference convenience.</span></span>



| <span data-ttu-id="9941d-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9941d-106">Interfaces</span></span>                                                 | <span data-ttu-id="9941d-107">Description</span><span class="sxs-lookup"><span data-stu-id="9941d-107">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9941d-108">**ITTAPI**</span><span class="sxs-lookup"><span data-stu-id="9941d-108">**ITTAPI**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | <span data-ttu-id="9941d-109">Interface TAPI principale 3.</span><span class="sxs-lookup"><span data-stu-id="9941d-109">Primary TAPI 3 interface.</span></span>                                                                                                                              |
| [<span data-ttu-id="9941d-110">**ITTAPI2**</span><span class="sxs-lookup"><span data-stu-id="9941d-110">**ITTAPI2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | <span data-ttu-id="9941d-111">Dérive de [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); fournit des méthodes supplémentaires qui prennent en charge les appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="9941d-111">Derives from [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); provides additional methods that support phone devices.</span></span>                                                         |
| [<span data-ttu-id="9941d-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="9941d-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | <span data-ttu-id="9941d-113">Interface sortante utilisée pour recevoir des informations asynchrones sur les événements TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="9941d-113">Outgoing interface used to receive asynchronous information about TAPI 3 events.</span></span>                                                                       |
| [<span data-ttu-id="9941d-114">**ITTAPICallCenter**</span><span class="sxs-lookup"><span data-stu-id="9941d-114">**ITTAPICallCenter**</span></span>](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | <span data-ttu-id="9941d-115">Fournit une interface d’entrée dans les contrôles de centre d’appels.</span><span class="sxs-lookup"><span data-stu-id="9941d-115">Provides an entry interface into call center controls.</span></span>                                                                                                 |
| [<span data-ttu-id="9941d-116">**ITTAPIObjectEvent**</span><span class="sxs-lookup"><span data-stu-id="9941d-116">**ITTAPIObjectEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | <span data-ttu-id="9941d-117">Fournit des méthodes pour récupérer des informations concernant les événements d’objet TAPI.</span><span class="sxs-lookup"><span data-stu-id="9941d-117">Provides methods to retrieve information concerning TAPI object events.</span></span>                                                                                |
| [<span data-ttu-id="9941d-118">**ITTAPIObjectEvent2**</span><span class="sxs-lookup"><span data-stu-id="9941d-118">**ITTAPIObjectEvent2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | <span data-ttu-id="9941d-119">Étend [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); fournit une méthode pour récupérer un pointeur vers l’objet Phone qui a provoqué l’événement d’objet TAPI.</span><span class="sxs-lookup"><span data-stu-id="9941d-119">Extends [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); provides a method to retrieve a pointer to the phone object that caused the TAPI object event.</span></span> |



 

 

 
