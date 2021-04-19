---
description: La liste suivante contient les méthodes internes d’adresse CMSP.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Méthodes d’assistance interne CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525758"
---
# <a name="cmspaddress-internal-helper-methods"></a><span data-ttu-id="84deb-103">Méthodes d’assistance interne CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="84deb-103">CMSPAddress Internal Helper Methods</span></span>



| <span data-ttu-id="84deb-104">Méthodes d’assistance interne CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="84deb-104">CMSPAddress internal helper methods</span></span>                                        | <span data-ttu-id="84deb-105">Description</span><span class="sxs-lookup"><span data-stu-id="84deb-105">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84deb-106">**GetStaticTerminals**</span><span class="sxs-lookup"><span data-stu-id="84deb-106">**GetStaticTerminals**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | <span data-ttu-id="84deb-107">Appelée par [**\_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) et [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) pour récupérer un tableau de terminaux statiques qui peuvent être utilisés sur cette adresse.</span><span class="sxs-lookup"><span data-stu-id="84deb-107">Called by [**get\_StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) and [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) to get an array of static terminals that can be used on this address.</span></span>                                     |
| [<span data-ttu-id="84deb-108">**GetDynamicTerminalClasses**</span><span class="sxs-lookup"><span data-stu-id="84deb-108">**GetDynamicTerminalClasses**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | <span data-ttu-id="84deb-109">Appelée par [**\_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) et [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) pour récupérer un tableau de classes de terminaux dynamiques qui peuvent être utilisées sur cette adresse.</span><span class="sxs-lookup"><span data-stu-id="84deb-109">Called by [**get\_DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) and [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) to get an array of dynamic terminal classes that can be used on this address.</span></span> |
| [<span data-ttu-id="84deb-110">**UpdateTerminalList**</span><span class="sxs-lookup"><span data-stu-id="84deb-110">**UpdateTerminalList**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | <span data-ttu-id="84deb-111">Remplit la liste des terminaux statiques du MSP.</span><span class="sxs-lookup"><span data-stu-id="84deb-111">Populates the MSP's list of static terminals.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="84deb-112">**ReceiveTSPAddressData**</span><span class="sxs-lookup"><span data-stu-id="84deb-112">**ReceiveTSPAddressData**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | <span data-ttu-id="84deb-113">Appelé lorsqu’un message de données TSP est destiné à être traité par l’adresse plutôt que par un appel spécifique.</span><span class="sxs-lookup"><span data-stu-id="84deb-113">Called when a TSP data message is intended to be processed by the address rather than by a specific call.</span></span>                                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="84deb-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84deb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84deb-115">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="84deb-115">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
