---
description: L’objet Phone est l’entité qui représente l’appareil téléphonique réel et tous ses contrôles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Interfaces d’objet téléphonique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529328"
---
# <a name="phone-object-interfaces"></a><span data-ttu-id="279a2-103">Interfaces d’objet téléphonique</span><span class="sxs-lookup"><span data-stu-id="279a2-103">Phone Object Interfaces</span></span>

<span data-ttu-id="279a2-104">L’objet Phone est l’entité qui représente l’appareil téléphonique réel et tous ses contrôles.</span><span class="sxs-lookup"><span data-stu-id="279a2-104">The Phone object is the entity that represents the actual phone device and all of its controls.</span></span>

<span data-ttu-id="279a2-105">Les interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) et [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) ne sont pas directement exposées sur l’objet Phone, mais sont étroitement liées à celle-ci et sont répertoriées ici pour des raisons de commodité de référence.</span><span class="sxs-lookup"><span data-stu-id="279a2-105">The [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) and [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) interfaces are not directly exposed on the Phone object, but are tightly related to it and are listed here for convenience of reference.</span></span>



| <span data-ttu-id="279a2-106">Interface</span><span class="sxs-lookup"><span data-stu-id="279a2-106">Interface</span></span>                                                  | <span data-ttu-id="279a2-107">Description</span><span class="sxs-lookup"><span data-stu-id="279a2-107">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="279a2-108">**ITPhone**</span><span class="sxs-lookup"><span data-stu-id="279a2-108">**ITPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | <span data-ttu-id="279a2-109">Autorise l’accès au périphérique téléphonique à un niveau comparable à celui disponible avec l’interface TAPI 2. API *x* C.</span><span class="sxs-lookup"><span data-stu-id="279a2-109">Allows access to the phone device at a level comparable to that available with the TAPI 2.*x* C API.</span></span>                                      |
| [<span data-ttu-id="279a2-110">**ITAutomatedPhoneControl**</span><span class="sxs-lookup"><span data-stu-id="279a2-110">**ITAutomatedPhoneControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | <span data-ttu-id="279a2-111">Fournit des méthodes pour le contrôle automatique des tonalités et des anneaux d’un téléphone, et pour la gestion automatique des appels basée sur l’État hookswitch d’un téléphone.</span><span class="sxs-lookup"><span data-stu-id="279a2-111">Provides methods for automated control of a phone's tones and rings, and for automated call handling based on a phone's hookswitch state.</span></span> |
| [<span data-ttu-id="279a2-112">**ITPhoneEvent**</span><span class="sxs-lookup"><span data-stu-id="279a2-112">**ITPhoneEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | <span data-ttu-id="279a2-113">Récupère la description des événements de téléphone.</span><span class="sxs-lookup"><span data-stu-id="279a2-113">Retrieves the description of phone events.</span></span>                                                                                                |
| [<span data-ttu-id="279a2-114">**IEnumPhone**</span><span class="sxs-lookup"><span data-stu-id="279a2-114">**IEnumPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | <span data-ttu-id="279a2-115">Énumère [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span><span class="sxs-lookup"><span data-stu-id="279a2-115">Enumerates [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span></span>                                                                                                    |



 

 

 



