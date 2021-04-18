---
description: Les fonctions de téléphonie étendues sont répertoriées par catégorie dans les tableaux suivants.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Référence des services de téléphonie étendus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519305"
---
# <a name="extended-telephony-services-reference"></a><span data-ttu-id="2dfa3-103">Référence des services de téléphonie étendus</span><span class="sxs-lookup"><span data-stu-id="2dfa3-103">Extended Telephony Services Reference</span></span>

<span data-ttu-id="2dfa3-104">Les fonctions de téléphonie étendues sont répertoriées par catégorie dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-104">The Extended Telephony functions are listed by category in the following tables.</span></span>

## <a name="extended-telephony-functions-for-line-devices"></a><span data-ttu-id="2dfa3-105">Fonctions de téléphonie étendues pour les appareils de ligne</span><span class="sxs-lookup"><span data-stu-id="2dfa3-105">Extended Telephony Functions for Line Devices</span></span>



| <span data-ttu-id="2dfa3-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="2dfa3-106">Function</span></span>                                                   | <span data-ttu-id="2dfa3-107">Description</span><span class="sxs-lookup"><span data-stu-id="2dfa3-107">Description</span></span>                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dfa3-108">**lineNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="2dfa3-108">**lineNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | <span data-ttu-id="2dfa3-109">Permet à une application de négocier une version d’extension à utiliser avec le périphérique de ligne spécifié.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-109">Allows an application to negotiate an extension version to use with the specified line device.</span></span> <span data-ttu-id="2dfa3-110">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-110">Asynchronous.</span></span> |
| [<span data-ttu-id="2dfa3-111">**lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="2dfa3-111">**lineDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | <span data-ttu-id="2dfa3-112">Permet aux fournisseurs de services d’accéder aux fonctionnalités spécifiques à l’appareil qui ne sont pas proposées par d’autres fonctions TAPI.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-112">Gives service providers access to device-specific features not offered by other TAPI functions.</span></span> <span data-ttu-id="2dfa3-113">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-113">Synchronous.</span></span> |
| [<span data-ttu-id="2dfa3-114">**lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="2dfa3-114">**lineDevSpecificFeature**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | <span data-ttu-id="2dfa3-115">Envoie des fonctionnalités de commutateur spécifiques à l’appareil au commutateur.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-115">Sends device-specific switch features to the switch.</span></span> <span data-ttu-id="2dfa3-116">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-116">Asynchronous.</span></span>                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a><span data-ttu-id="2dfa3-117">Fonctions de téléphonie étendues pour les appareils téléphoniques</span><span class="sxs-lookup"><span data-stu-id="2dfa3-117">Extended Telephony Functions for Phone Devices</span></span>



| <span data-ttu-id="2dfa3-118">Fonction</span><span class="sxs-lookup"><span data-stu-id="2dfa3-118">Function</span></span>                                                     | <span data-ttu-id="2dfa3-119">Description</span><span class="sxs-lookup"><span data-stu-id="2dfa3-119">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dfa3-120">**phoneDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="2dfa3-120">**phoneDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | <span data-ttu-id="2dfa3-121">Fonction d’échappement spécifique à l’appareil pour autoriser les extensions dépendantes du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-121">Device-specific escape function to allow vendor-dependent extensions.</span></span> <span data-ttu-id="2dfa3-122">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-122">Asynchronous.</span></span>                          |
| [<span data-ttu-id="2dfa3-123">**PhoneNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="2dfa3-123">**PhoneNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | <span data-ttu-id="2dfa3-124">Permet à une application de négocier une version d’extension à utiliser avec l’appareil téléphonique spécifié.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-124">Allows an application to negotiate an extension version to use with the specified phone device.</span></span> <span data-ttu-id="2dfa3-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2dfa3-125">Synchronous.</span></span> |



 

 

 



