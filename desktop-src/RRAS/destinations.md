---
title: Destinations
description: Une destination dans la table de routage est une entrée réseau représentée par une adresse réseau et un masque de réseau.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840162"
---
# <a name="destinations"></a><span data-ttu-id="32376-103">Destinations</span><span class="sxs-lookup"><span data-stu-id="32376-103">Destinations</span></span>

<span data-ttu-id="32376-104">Une destination dans la table de routage est une entrée réseau représentée par une adresse réseau et un masque de réseau.</span><span class="sxs-lookup"><span data-stu-id="32376-104">A destination in the routing table is a network entry represented by a network address and a network mask.</span></span>

<span data-ttu-id="32376-105">Une entrée de destination dans la table de routage comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32376-105">A destination entry in the routing table includes:</span></span>

-   <span data-ttu-id="32376-106">Adresse, exprimée sous la forme d’une adresse réseau et d’un masque de réseau.</span><span class="sxs-lookup"><span data-stu-id="32376-106">The address, expressed as a network address and network mask.</span></span>
-   <span data-ttu-id="32376-107">Liste des itinéraires vers la destination.</span><span class="sxs-lookup"><span data-stu-id="32376-107">A list of routes to the destination.</span></span>
-   <span data-ttu-id="32376-108">Liste d’emplacements de pointeurs opaques.</span><span class="sxs-lookup"><span data-stu-id="32376-108">A list of opaque pointer slots.</span></span>
-   <span data-ttu-id="32376-109">Vues dans lesquelles cette destination est valide.</span><span class="sxs-lookup"><span data-stu-id="32376-109">The views in which this destination is valid.</span></span> <span data-ttu-id="32376-110">La destination contient une structure pour chaque vue qui contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="32376-110">The destination contains a structure for each view that contains the following information:</span></span>
    -   <span data-ttu-id="32376-111">Identificateur de la vue.</span><span class="sxs-lookup"><span data-stu-id="32376-111">An identifier for the view.</span></span>
    -   <span data-ttu-id="32376-112">Pointeur vers le meilleur itinéraire vers la destination dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="32376-112">A pointer to the best route to the destination in this view.</span></span>
    -   <span data-ttu-id="32376-113">Propriétaire du meilleur itinéraire dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="32376-113">The owner of the best route in this view.</span></span>
    -   <span data-ttu-id="32376-114">Indicateurs associés au meilleur itinéraire dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="32376-114">Flags associated with the best route in this view.</span></span>
    -   <span data-ttu-id="32376-115">Handle vers tous les itinéraires qui sont dans un état de blocage dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="32376-115">Handle to any routes that are in a hold-down state in this view.</span></span>

 

 




