---
description: Un réseau est considéré comme le mécanisme de transport qui transmet les données d’un point à un autre.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485313"
---
# <a name="network"></a><span data-ttu-id="65020-103">Réseau</span><span class="sxs-lookup"><span data-stu-id="65020-103">Network</span></span>

<span data-ttu-id="65020-104">Un réseau est considéré comme le mécanisme de transport qui transmet les données d’un point à un autre.</span><span class="sxs-lookup"><span data-stu-id="65020-104">A network is viewed as the transport mechanism that conveys data from one point to another.</span></span> <span data-ttu-id="65020-105">Les fournisseurs de services TAPI gèrent les protocoles spécifiques requis pour effectuer des opérations telles que l’établissement d’une session de communication sur un réseau donné.</span><span class="sxs-lookup"><span data-stu-id="65020-105">TAPI service providers handle the specific protocols required to perform operations such as establishing a communications session on a given network.</span></span> <span data-ttu-id="65020-106">Une application de serveur ou d’utilisateur final ne requiert normalement que des informations très générales sur le réseau, telles que le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="65020-106">An end-user or server application normally requires only very general network information, such as address type.</span></span>

<span data-ttu-id="65020-107">Certains types de réseaux courants :</span><span class="sxs-lookup"><span data-stu-id="65020-107">Some common types of networks:</span></span>

-   <span data-ttu-id="65020-108">**Pots (Plain Old Telephone Service) :** La voix et les données sont transmises au format analogique dans la *boucle locale* et sont transmises numériquement ailleurs.</span><span class="sxs-lookup"><span data-stu-id="65020-108">**POTS (Plain Old Telephone Service):** Voice and data are transmitted in analog format while in the *local loop* and are digitally transmitted elsewhere.</span></span> <span data-ttu-id="65020-109">En général, un type de support par appel, un canal par ligne.</span><span class="sxs-lookup"><span data-stu-id="65020-109">Typically, one media type per call, one channel per line.</span></span>
-   <span data-ttu-id="65020-110">**RNIS (réseau numérique à intégration de services) :** Transmis numériquement.</span><span class="sxs-lookup"><span data-stu-id="65020-110">**ISDN (Integrated Services Digital Network):** Transmitted digitally.</span></span> <span data-ttu-id="65020-111">Vitesses allant jusqu’à 128 Kbits/s sur les lignes BRI-RNIS (Basic Rate Interface) et bien plus élevées sur les lignes PRI-RNIS.</span><span class="sxs-lookup"><span data-stu-id="65020-111">Speeds of up to 128 Kbps on Basic Rate Interface (BRI-ISDN) lines and much higher on Primary Rate Interface (PRI-ISDN) lines.</span></span> <span data-ttu-id="65020-112">Au moins trois canaux et jusqu’à 32 canaux, pour une transmission simultanée et indépendante de la voix et des données.</span><span class="sxs-lookup"><span data-stu-id="65020-112">At least three channels and as many as 32 channels, for simultaneous, independently operated transmission of voice and data.</span></span> <span data-ttu-id="65020-113">Norme internationale.</span><span class="sxs-lookup"><span data-stu-id="65020-113">International standard.</span></span>
-   <span data-ttu-id="65020-114">**T1/E1 :** Transmis numériquement.</span><span class="sxs-lookup"><span data-stu-id="65020-114">**T1/E1:** Transmitted digitally.</span></span> <span data-ttu-id="65020-115">T1 est un lien de transmission avec une capacité de 1,544 Mbits/s, généralement utilisée pour connecter des réseaux sur des distances distantes.</span><span class="sxs-lookup"><span data-stu-id="65020-115">T1 is a transmission link with a capacity of 1.544 Mbps, typically used for connecting networks across remote distances.</span></span> <span data-ttu-id="65020-116">Dans l’Union européenne, T1 est appelé E1.</span><span class="sxs-lookup"><span data-stu-id="65020-116">In the European Union T1 is called E1.</span></span>
-   <span data-ttu-id="65020-117">**Commutation 56 :** Signalement à 56 Kbits/s sur des lignes téléphoniques commutées, mais nécessite un équipement spécial.</span><span class="sxs-lookup"><span data-stu-id="65020-117">**Switched 56:** Signaling at 56 Kbps over dial-up telephone lines, but requires special equipment.</span></span> <span data-ttu-id="65020-118">Limité aux appels à d’autres installations spécialement équipées.</span><span class="sxs-lookup"><span data-stu-id="65020-118">Limited to calls to other specially equipped facilities.</span></span>
-   <span data-ttu-id="65020-119">**Centrex :** Services réseau centralisés par le biais de lignes téléphoniques classiques et utilisant l’équipement de la compagnie téléphonique.</span><span class="sxs-lookup"><span data-stu-id="65020-119">**CENTREX:** Centralized network services through regular telephone lines and using telephone company equipment.</span></span> <span data-ttu-id="65020-120">Aucun équipement spécial requis.</span><span class="sxs-lookup"><span data-stu-id="65020-120">No special equipment required.</span></span>
-   <span data-ttu-id="65020-121">**PBX numériques (échange de branche privée) et systèmes clés :** Voix et données transmises sur des systèmes téléphoniques privés à l’aide d’interfaces propriétaires.</span><span class="sxs-lookup"><span data-stu-id="65020-121">**Digital PBXs (private branch exchanges) and key systems:** Voice and data transmitted on private telephone systems using proprietary interfaces.</span></span>
-   <span data-ttu-id="65020-122">**Réseaux IP :** Voix et données transmises sur des réseaux à l’aide du protocole IP (Internet Protocol), comme Internet ou un intranet d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="65020-122">**IP Networks:** Voice and data transmitted on networks using the Internet Protocol (IP), such as the Internet itself or a corporate intranet.</span></span>

<span data-ttu-id="65020-123">Notez que cette liste n'est pas exhaustive.</span><span class="sxs-lookup"><span data-stu-id="65020-123">Please note that this list is not exhaustive.</span></span> <span data-ttu-id="65020-124">Tout mécanisme de transport réseau peut être pris en charge, en fonction des fournisseurs de services appropriés.</span><span class="sxs-lookup"><span data-stu-id="65020-124">Any network transport mechanism can be supported, given appropriate service providers.</span></span>

 

 



