---
title: Considérations sur la sécurité des points de contrôle
description: Lorsque vous créez un point de contrôle, vous devez prendre en compte les problèmes de sécurité suivants.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940178"
---
# <a name="control-point-security-considerations"></a><span data-ttu-id="3d01b-103">Considérations sur la sécurité des points de contrôle</span><span class="sxs-lookup"><span data-stu-id="3d01b-103">Control Point Security Considerations</span></span>

<span data-ttu-id="3d01b-104">Lorsque vous créez un point de contrôle, vous devez prendre en compte les problèmes de sécurité suivants.</span><span class="sxs-lookup"><span data-stu-id="3d01b-104">When you are creating a control point, you need to take into consideration the following security issues.</span></span>

-   <span data-ttu-id="3d01b-105">Toutes les recherches de points de contrôle sont envoyées par défaut avec une durée de vie de 1.</span><span class="sxs-lookup"><span data-stu-id="3d01b-105">All control point searches are by default sent with a TTL of 1.</span></span> <span data-ttu-id="3d01b-106">Cela signifie que seuls les appareils au sein du même sous-réseau sont découverts.</span><span class="sxs-lookup"><span data-stu-id="3d01b-106">This means that only devices within the same subnet are discovered.</span></span> <span data-ttu-id="3d01b-107">Vous pouvez configurer une durée de vie plus élevée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="3d01b-107">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="3d01b-108">L’appareil et la description de service d’un appareil sont téléchargés uniquement s’ils sont présents sur le même appareil que celui qui a envoyé l’annonce de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3d01b-108">A device's device and service description is only downloaded if it is present on the same device which sent the device announcement.</span></span>
-   <span data-ttu-id="3d01b-109">Un appareil reçoit uniquement des demandes de contrôle et d’abonnement si ses URL de contrôle et d’abonnement se trouvent sur le même appareil que celui qui a envoyé les annonces de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3d01b-109">A device is only sent control and subscription requests if its control and subscription URLs are on the same device that sent the device announcements.</span></span>

 

 




