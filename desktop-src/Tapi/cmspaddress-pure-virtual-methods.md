---
description: Ces méthodes doivent être remplacées par des classes dérivées.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress des méthodes virtuelles pures
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518712"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="ba853-103">CMSPAddress des méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="ba853-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="ba853-104">Ces méthodes doivent être remplacées par des classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="ba853-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="ba853-105">CMSPAddress des méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="ba853-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="ba853-106">Description</span><span class="sxs-lookup"><span data-stu-id="ba853-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba853-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="ba853-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="ba853-108">La méthode private AddRef pour l’adresse.</span><span class="sxs-lookup"><span data-stu-id="ba853-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ba853-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="ba853-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="ba853-110">Méthode de mise en sortie privée pour l’adresse.</span><span class="sxs-lookup"><span data-stu-id="ba853-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="ba853-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="ba853-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="ba853-112">Appelé par l’interface TAPI pour créer un objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="ba853-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="ba853-113">L’implémentation dans la classe dérivée doit simplement appeler la fonction [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="ba853-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="ba853-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="ba853-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="ba853-115">Appelé par l’interface TAPI pour arrêter un objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="ba853-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="ba853-116">L’implémentation dans la classe dérivée doit simplement appeler la fonction [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="ba853-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="ba853-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="ba853-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="ba853-118">Obtient les types de médias pris en charge par le MSP.</span><span class="sxs-lookup"><span data-stu-id="ba853-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="ba853-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba853-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba853-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="ba853-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



