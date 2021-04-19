---
description: Le service de notification d’événements système (SENS) définit la coclasse SENSe dans le cadre de la bibliothèque de types SENSe.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Objet SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521907"
---
# <a name="sens-object"></a><span data-ttu-id="1041a-103">Objet SENS</span><span class="sxs-lookup"><span data-stu-id="1041a-103">SENS Object</span></span>

<span data-ttu-id="1041a-104">Le service de notification d’événements système (SENS) définit la coclasse SENSe dans le cadre de la bibliothèque de types SENSe.</span><span class="sxs-lookup"><span data-stu-id="1041a-104">The System Event Notification Service (SENS) defines the SENS coclass as part of the SENS type library.</span></span>

## <a name="implementation"></a><span data-ttu-id="1041a-105">Implémentation</span><span class="sxs-lookup"><span data-stu-id="1041a-105">Implementation</span></span>

<span data-ttu-id="1041a-106">L’implémentation d’objet SENSe est fournie par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1041a-106">The SENS object implementation is provided by the operating system.</span></span>

## <a name="creationaccess-functions"></a><span data-ttu-id="1041a-107">Fonctions de création et d’accès</span><span class="sxs-lookup"><span data-stu-id="1041a-107">Creation/Access Functions</span></span>



| <span data-ttu-id="1041a-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="1041a-108">Function</span></span>                                      | <span data-ttu-id="1041a-109">Description</span><span class="sxs-lookup"><span data-stu-id="1041a-109">Description</span></span>                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="1041a-110">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="1041a-110">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | <span data-ttu-id="1041a-111">Crée une instance de l’objet SENS à l’aide de son CLSID.</span><span class="sxs-lookup"><span data-stu-id="1041a-111">Creates an instance of the SENS object using its CLSID.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="1041a-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1041a-112">Interfaces</span></span>



| <span data-ttu-id="1041a-113">Interface</span><span class="sxs-lookup"><span data-stu-id="1041a-113">Interface</span></span>                            | <span data-ttu-id="1041a-114">Description</span><span class="sxs-lookup"><span data-stu-id="1041a-114">Description</span></span>                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1041a-115">**IsensNetwork**</span><span class="sxs-lookup"><span data-stu-id="1041a-115">**IsensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | <span data-ttu-id="1041a-116">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="1041a-116">Default.</span></span> <span data-ttu-id="1041a-117">Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="1041a-117">Outgoing interface implemented by sink object in subscriber application.</span></span>                   |
| [<span data-ttu-id="1041a-118">**IsensOnNow**</span><span class="sxs-lookup"><span data-stu-id="1041a-118">**IsensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | <span data-ttu-id="1041a-119">Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="1041a-119">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="1041a-120">**IsensLogon**</span><span class="sxs-lookup"><span data-stu-id="1041a-120">**IsensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | <span data-ttu-id="1041a-121">Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="1041a-121">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="1041a-122">**IsensLogon2**</span><span class="sxs-lookup"><span data-stu-id="1041a-122">**IsensLogon2**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | <span data-ttu-id="1041a-123">Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="1041a-123">Outgoing interface implemented by sink object in subscriber application.</span></span> <span data-ttu-id="1041a-124">Disponible avec Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1041a-124">Available with Windows XP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1041a-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1041a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1041a-126">**ISensLogon**</span><span class="sxs-lookup"><span data-stu-id="1041a-126">**ISensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[<span data-ttu-id="1041a-127">**ISensNetwork**</span><span class="sxs-lookup"><span data-stu-id="1041a-127">**ISensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[<span data-ttu-id="1041a-128">**ISensOnNow**</span><span class="sxs-lookup"><span data-stu-id="1041a-128">**ISensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[<span data-ttu-id="1041a-129">À propos du service de notification d’événements système</span><span class="sxs-lookup"><span data-stu-id="1041a-129">About System Event Notification Service</span></span>](about-system-event-notification-service.md)
</dt> </dl>

 

 
