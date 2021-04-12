---
title: Raisons de l’inaccessibilité
description: Le tableau suivant répertorie les valeurs constantes qui indiquent la raison pour laquelle une interface est inaccessible.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031590"
---
# <a name="unreachability-reasons"></a><span data-ttu-id="4a238-103">Raisons de l’inaccessibilité</span><span class="sxs-lookup"><span data-stu-id="4a238-103">Unreachability Reasons</span></span>

<span data-ttu-id="4a238-104">Le tableau suivant répertorie les valeurs constantes qui indiquent la raison pour laquelle une interface est inaccessible.</span><span class="sxs-lookup"><span data-stu-id="4a238-104">The following table lists constant values that indicate why an interface is unreachable.</span></span>



| <span data-ttu-id="4a238-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a238-105">Value</span></span>                                       | <span data-ttu-id="4a238-106">Signification</span><span class="sxs-lookup"><span data-stu-id="4a238-106">Meaning</span></span>                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a238-107">administration de l' \_ interface MPR \_ \_ désactivée</span><span class="sxs-lookup"><span data-stu-id="4a238-107">MPR\_INTERFACE\_ADMIN\_DISABLED</span></span>             | <span data-ttu-id="4a238-108">L’administrateur a désactivé l’interface.</span><span class="sxs-lookup"><span data-stu-id="4a238-108">The administrator has disabled the interface.</span></span>                                                  |
| <span data-ttu-id="4a238-109">échec de connexion de l' \_ interface MPR \_ \_</span><span class="sxs-lookup"><span data-stu-id="4a238-109">MPR\_INTERFACE\_CONNECTION\_FAILURE</span></span>         | <span data-ttu-id="4a238-110">La tentative de connexion précédente a échoué.</span><span class="sxs-lookup"><span data-stu-id="4a238-110">The previous connection attempt failed.</span></span> <span data-ttu-id="4a238-111">Examinez le membre **dwLastError** pour obtenir le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4a238-111">Look at the **dwLastError** member for the error code.</span></span> |
| <span data-ttu-id="4a238-112">DIALOUT de l’interface MPR- \_ \_ \_ restriction des heures \_</span><span class="sxs-lookup"><span data-stu-id="4a238-112">MPR\_INTERFACE\_DIALOUT\_HOURS\_RESTRICTION</span></span> | <span data-ttu-id="4a238-113">La numérotation à distance n’est pas autorisée à l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="4a238-113">Dial-out is not allowed at the current time.</span></span>                                                   |
| <span data-ttu-id="4a238-114">\_interface MPR \_ hors \_ des \_ ressources</span><span class="sxs-lookup"><span data-stu-id="4a238-114">MPR\_INTERFACE\_OUT\_OF\_RESOURCES</span></span>          | <span data-ttu-id="4a238-115">Aucun port ou périphérique ne peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="4a238-115">No ports or devices are available for use.</span></span>                                                     |
| <span data-ttu-id="4a238-116">\_service d’interface MPR \_ \_ suspendu</span><span class="sxs-lookup"><span data-stu-id="4a238-116">MPR\_INTERFACE\_SERVICE\_PAUSED</span></span>             | <span data-ttu-id="4a238-117">Le service est suspendu.</span><span class="sxs-lookup"><span data-stu-id="4a238-117">The service is paused.</span></span>                                                                         |
| <span data-ttu-id="4a238-118">\_interface MPR \_ aucune \_ détection de support \_</span><span class="sxs-lookup"><span data-stu-id="4a238-118">MPR\_INTERFACE\_NO\_MEDIA\_SENSE</span></span>            | <span data-ttu-id="4a238-119">Le câble réseau est déconnecté de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="4a238-119">The network cable is disconnected from the network card.</span></span>                                       |
| <span data-ttu-id="4a238-120">\_interface MPR \_ sans \_ appareil</span><span class="sxs-lookup"><span data-stu-id="4a238-120">MPR\_INTERFACE\_NO\_DEVICE</span></span>                  | <span data-ttu-id="4a238-121">La carte réseau a été supprimée de la machine.</span><span class="sxs-lookup"><span data-stu-id="4a238-121">The network card has been removed from the machine.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="4a238-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a238-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a238-123">**\_Interface MPR \_ 0**</span><span class="sxs-lookup"><span data-stu-id="4a238-123">**MPR\_INTERFACE\_0**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[<span data-ttu-id="4a238-124">**\_Interface MPR \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4a238-124">**MPR\_INTERFACE\_1**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[<span data-ttu-id="4a238-125">**\_IFROW MIB**</span><span class="sxs-lookup"><span data-stu-id="4a238-125">**MIB\_IFROW**</span></span>](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[<span data-ttu-id="4a238-126">**\_IFSTATUS MIB**</span><span class="sxs-lookup"><span data-stu-id="4a238-126">**MIB\_IFSTATUS**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 