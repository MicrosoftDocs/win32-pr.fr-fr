---
description: Les adresses de transport (XAddrs) incluses dans les messages messages ProbeMatches et ResolveMatches sont soumises à la validation de base avant que WSDAPI envoie un message HTTP, tel qu’une demande de métadonnées.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Règles de validation XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202141"
---
# <a name="xaddr-validation-rules"></a><span data-ttu-id="b7a5e-103">Règles de validation XAddr</span><span class="sxs-lookup"><span data-stu-id="b7a5e-103">XAddr Validation Rules</span></span>

<span data-ttu-id="b7a5e-104">Les adresses de transport (XAddrs) incluses dans les messages [messages ProbeMatches](probematches-message.md) et [ResolveMatches](resolvematches-message.md) sont soumises à la validation de base avant que wsdapi envoie un message http, tel qu’une demande de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-104">Transport addresses (XAddrs) included in [ProbeMatches](probematches-message.md) and [ResolveMatches](resolvematches-message.md) messages are subject to basic validation before WSDAPI sends an HTTP message, such as a metadata request.</span></span>

<span data-ttu-id="b7a5e-105">Cela permet de s’assurer que les XAddrs se trouvent sur le même sous-réseau que le client.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-105">This is in order to ensure that the XAddrs are on the same subnet as the client.</span></span>

<span data-ttu-id="b7a5e-106">Le code XML suivant montre un exemple d’élément XAddrs.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-106">The following XML shows a sample XAddrs element.</span></span> <span data-ttu-id="b7a5e-107">Le préfixe WSD fait référence à l’espace de noms `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="b7a5e-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

<span data-ttu-id="b7a5e-108">Toutes les conditions suivantes doivent être satisfaites pour que le message HTTP soit envoyé sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-108">All of the following conditions must be met before the HTTP message will go out over the wire.</span></span>

-   <span data-ttu-id="b7a5e-109">XAddrs doit être une adresse HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-109">XAddrs must be HTTP or HTTPS addresses.</span></span> <span data-ttu-id="b7a5e-110">Les XAddrs d’autres schémas sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-110">XAddrs of other schemes are ignored.</span></span>
-   <span data-ttu-id="b7a5e-111">Si des XAddrs HTTPs sont présents, tous les XAddrs doivent être HTTPs.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-111">If any HTTPS XAddrs are present, all XAddrs must be HTTPS.</span></span> <span data-ttu-id="b7a5e-112">Les sections XAddr qui incluent des adresses HTTP et HTTPs sont entièrement ignorées.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-112">XAddr sections which include both HTTP and HTTPS addresses are completely ignored.</span></span> <span data-ttu-id="b7a5e-113">En outre, l’adresse de point de terminaison de l’appareil doit correspondre exactement à l’XAddrs HTTPs.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-113">Additionally, the device's endpoint address must match the HTTPS XAddrs exactly.</span></span>
-   <span data-ttu-id="b7a5e-114">XAddrs doit être une adresse IP ou des noms d’hôte pouvant être résolus via DNS.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-114">XAddrs must be IP addresses or hostnames resolvable through DNS.</span></span> <span data-ttu-id="b7a5e-115">En règle générale, les adresses IP sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-115">Usually, IP addresses are used.</span></span>
-   <span data-ttu-id="b7a5e-116">Au moins une adresse IP incluse dans le XAddrs (ou l’adresse IP résolue à partir d’un nom d’hôte inclus dans le XAddrs) doit se trouver sur le même sous-réseau que la carte sur laquelle le message [messages ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) a été reçu.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-116">At least one IP address included in the XAddrs (or IP address resolved from a hostname included in the XAddrs) must be on the same subnet as the adapter over which the [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message was received.</span></span>
-   <span data-ttu-id="b7a5e-117">L’adresse et le port spécifiés dans le premier XAddr doivent être accessibles.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-117">The address and port specified in the first XAddr must be accessible.</span></span> <span data-ttu-id="b7a5e-118">WSDAPI tente de se connecter à cette adresse lors de l’établissement d’une connexion HTTP.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-118">WSDAPI attempts to connect to this address when establishing an HTTP connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7a5e-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7a5e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7a5e-120">Messages ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="b7a5e-120">ProbeMatches</span></span>](probematches-message.md)
</dt> <dt>

[<span data-ttu-id="b7a5e-121">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="b7a5e-121">ResolveMatches</span></span>](resolvematches-message.md)
</dt> <dt>

[<span data-ttu-id="b7a5e-122">Modèles de message d’échange de métadonnées et de découverte</span><span class="sxs-lookup"><span data-stu-id="b7a5e-122">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



