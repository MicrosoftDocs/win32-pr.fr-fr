---
description: En fonction de la taxonomie définie pour les schémas multipoint/multidiffusion indépendante du protocole Windows Sockets 2, la technologie ATM se trouve dans la catégorie des données enracinées et des plans de contrôle enracinés.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Détails de la fonction ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114290"
---
# <a name="winsock-atm-function-details"></a><span data-ttu-id="3b565-103">Détails de la fonction ATM Winsock</span><span class="sxs-lookup"><span data-stu-id="3b565-103">Winsock ATM Function Details</span></span>

<span data-ttu-id="3b565-104">En fonction de la taxonomie définie pour les schémas multipoint/multidiffusion indépendante du protocole Windows Sockets 2, la technologie ATM se trouve dans la catégorie des données enracinées et des plans de contrôle enracinés.</span><span class="sxs-lookup"><span data-stu-id="3b565-104">Based on the taxonomy defined for Windows Sockets 2 protocol-independent multipoint/multicast schemes, ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="3b565-105">(Pour plus d’informations, consultez la spécification de l’API Windows Sockets 2, annexe D.) Une application agissant comme racine crée des \_ sockets racine c, et les homologues exécutés sur les nœuds terminaux utilisent des \_ sockets de feuille c.</span><span class="sxs-lookup"><span data-stu-id="3b565-105">(See the Windows Sockets 2 API Specification, Appendix D for more information.) An application acting as the root would create c\_root sockets, and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="3b565-106">L’application racine utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour ajouter de nouveaux nœuds terminaux.</span><span class="sxs-lookup"><span data-stu-id="3b565-106">The root application will use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="3b565-107">Les applications correspondantes sur les nœuds terminaux auront défini leurs \_ sockets de feuille c en mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="3b565-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into the listening mode.</span></span> <span data-ttu-id="3b565-108">**WSAJoinLeaf** avec un \_ Socket racine c spécifié sera MAPPÉ au message d’installation Q. 2931 (pour la première feuille) ou au message d’ajout de tiers (pour les autres feuilles).</span><span class="sxs-lookup"><span data-stu-id="3b565-108">**WSAJoinLeaf** with a c\_root socket specified will be mapped to the Q.2931 SETUP message (for the first leaf) or ADD PARTY message (for any subsequent leaves).</span></span>

> [!Note]  
> <span data-ttu-id="3b565-109">Les paramètres de qualité de service (QoS) spécifiés dans **WSAJoinLeaf** pour les autres feuilles doivent être ignorés par la spécification Uni du Forum ATM.</span><span class="sxs-lookup"><span data-stu-id="3b565-109">The QoS parameters specified in **WSAJoinLeaf** for any subsequent leaves should be ignored per the ATM Forum UNI specification.</span></span>

 

<span data-ttu-id="3b565-110">La jointure initiée par feuille ne fait pas partie du ATM UNI 3,1, mais elle est prise en charge dans le ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="3b565-110">The leaf-initiated join is not part of the ATM UNI 3.1, but is supported in the ATM UNI 4.0.</span></span> <span data-ttu-id="3b565-111">Par conséquent, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) avec un \_ Socket feuille c spécifié peut être MAPPÉ au message ATM Uni 4,0 approprié.</span><span class="sxs-lookup"><span data-stu-id="3b565-111">Thus [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) with a c\_leaf socket specified can be mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="3b565-112">Le paramètre AAL et la négociation B-LLI sont pris en charge par la modification des IEs correspondants dans le paramètre *lpSQOS* lors de l’appel de la fonction conditionnelle spécifiée dans [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span><span class="sxs-lookup"><span data-stu-id="3b565-112">The AAL Parameter and B-LLI negotiation is supported through the modification of the corresponding IEs in the *lpSQOS* parameter upon the invocation of the condition function specified in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span></span>

> [!Note]  
> <span data-ttu-id="3b565-113">Seuls certains champs dans ces deux champs peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="3b565-113">Only certain fields in those two IEs can be modified.</span></span> <span data-ttu-id="3b565-114">Pour plus d’informations, consultez la spécification UNI du Forum ATM annexe C et annexe F.</span><span class="sxs-lookup"><span data-stu-id="3b565-114">See the ATM Forum UNI specification Appendix C and Appendix F for details.</span></span>

 

 

 



