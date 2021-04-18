---
description: La technologie ATM est incluse dans la catégorie des plans de contrôle et des données enracinées.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Point d’ATM vers multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529118"
---
# <a name="atm-point-to-multipoint"></a><span data-ttu-id="414f7-103">Point d’ATM vers multipoint</span><span class="sxs-lookup"><span data-stu-id="414f7-103">ATM Point to Multipoint</span></span>

<span data-ttu-id="414f7-104">La technologie ATM est incluse dans la catégorie des plans de contrôle et des données enracinées.</span><span class="sxs-lookup"><span data-stu-id="414f7-104">ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="414f7-105">Une application agissant comme racine créerait des \_ sockets racine c et des équivalents s’exécutant sur des nœuds terminaux utiliserait des \_ sockets de feuille c.</span><span class="sxs-lookup"><span data-stu-id="414f7-105">An application acting as the root would create c\_root sockets and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="414f7-106">L’application racine utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour ajouter de nouveaux nœuds terminaux.</span><span class="sxs-lookup"><span data-stu-id="414f7-106">The root application uses [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="414f7-107">Les applications correspondantes sur les nœuds terminaux auront défini leurs \_ sockets de feuille c en mode écoute.</span><span class="sxs-lookup"><span data-stu-id="414f7-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into listen mode.</span></span> <span data-ttu-id="414f7-108">**WSAJoinLeaf** avec un \_ Socket racine c spécifié est mappé au message Q. 2931 ADDPARTY.</span><span class="sxs-lookup"><span data-stu-id="414f7-108">**WSAJoinLeaf** with a c\_root socket specified is mapped to the Q.2931 ADDPARTY message.</span></span> <span data-ttu-id="414f7-109">La jointure initiée par feuille n’est pas prise en charge dans ATM UNI 3,1, mais elle est prise en charge dans ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="414f7-109">The leaf-initiated join is not supported in ATM UNI 3.1, but is supported in ATM UNI 4.0.</span></span> <span data-ttu-id="414f7-110">Par conséquent, **WSAJoinLeaf** avec un \_ Socket feuille c spécifié est MAPPÉ au message ATM Uni 4,0 approprié.</span><span class="sxs-lookup"><span data-stu-id="414f7-110">Thus **WSAJoinLeaf** with a c\_leaf socket specified is mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="414f7-111">Il y a d’autres points à prendre en compte pour le point à multipoint :</span><span class="sxs-lookup"><span data-stu-id="414f7-111">There are additional considerations to bear in mind for ATM point-to-multipoint:</span></span>

-   <span data-ttu-id="414f7-112">L’ajout de nouvelles feuilles à la session point à multipoint ATM est basé uniquement sur les invitations.</span><span class="sxs-lookup"><span data-stu-id="414f7-112">The addition of new leaves to the ATM point-to-multipoint session is invitation-based only.</span></span> <span data-ttu-id="414f7-113">Les invitations de la racine quittent, qui ont déjà leur appel de fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , en appelant la fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="414f7-113">The root invites leaves — which have already their [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function call — by calling the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="414f7-114">Le workflow de données dans une session ATM point à multipoint ne concerne que la racine jusqu’au départ. les feuilles ne peuvent pas utiliser la même session pour envoyer des informations à la racine.</span><span class="sxs-lookup"><span data-stu-id="414f7-114">The flow of data in an ATM point-to-multipoint session is from root-to-leaves only; leaves cannot use the same session to send information to the root.</span></span>
-   <span data-ttu-id="414f7-115">Une seule feuille par adaptateur ATM est autorisée.</span><span class="sxs-lookup"><span data-stu-id="414f7-115">Only one leaf per ATM adapter is allowed.</span></span>

 

 



