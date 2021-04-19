---
title: Modifications apportées au meilleur itinéraire sur un réseau
description: Une modification de l’une des valeurs suivantes pour le meilleur itinéraire vers un réseau de destination donné entraîne la génération par le gestionnaire de tables de routage d’un message de notification envoyé à chaque client inscrit et aux redirecteurs
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510019"
---
# <a name="changes-to-the-best-route-to-a-network"></a><span data-ttu-id="3426d-103">Modifications apportées au meilleur itinéraire sur un réseau</span><span class="sxs-lookup"><span data-stu-id="3426d-103">Changes to the Best Route to a Network</span></span>

<span data-ttu-id="3426d-104">**Windows Server 2003 :** Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3426d-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="3426d-105">Les nouvelles applications doivent utiliser l’API du gestionnaire de table de routage version 2.</span><span class="sxs-lookup"><span data-stu-id="3426d-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="3426d-106">Une modification de l’une des valeurs suivantes pour le meilleur itinéraire vers un réseau de destination donné entraîne la génération par le gestionnaire de tables de routage d’un message de notification envoyé à chaque client inscrit et aux redirecteurs :</span><span class="sxs-lookup"><span data-stu-id="3426d-106">A change in any of the following values for the best route to a given destination network causes the routing table manager to generate a notification message sent to each registered client and to the forwarders:</span></span>

-   <span data-ttu-id="3426d-107">Identificateur de protocole</span><span class="sxs-lookup"><span data-stu-id="3426d-107">Protocol identifier</span></span>
-   <span data-ttu-id="3426d-108">Index d’interface</span><span class="sxs-lookup"><span data-stu-id="3426d-108">Interface index</span></span>
-   <span data-ttu-id="3426d-109">Adresse du routeur du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="3426d-109">Address of next-hop router</span></span>
-   <span data-ttu-id="3426d-110">Données spécifiques à la famille de protocoles qui incluent les métriques d’itinéraire</span><span class="sxs-lookup"><span data-stu-id="3426d-110">Protocol family-specific data that includes route metrics</span></span>

<span data-ttu-id="3426d-111">Une modification de l’identificateur de protocole, de l’index d’interface ou de l’adresse du routeur de saut suivant se produit lorsqu’une nouvelle entrée de routage plus performante est ajoutée, ou lorsque l’entrée la mieux adaptée est supprimée ou obsolète, et laisse un autre itinéraire en tant que nouveau meilleur itinéraire.</span><span class="sxs-lookup"><span data-stu-id="3426d-111">A change in protocol identifier, interface index, or next-hop router address occurs when a new, better-route entry is added, or when the current best-route entry is deleted or aged out, and leaves another route as the new best route.</span></span>

 

 




