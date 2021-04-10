---
title: Niveaux d’authentification
description: Microsoft RPC fournit plusieurs niveaux d’authentification.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196725"
---
# <a name="authentication-levels"></a><span data-ttu-id="11068-103">Niveaux d’authentification</span><span class="sxs-lookup"><span data-stu-id="11068-103">Authentication Levels</span></span>

<span data-ttu-id="11068-104">Microsoft RPC fournit plusieurs niveaux d’authentification.</span><span class="sxs-lookup"><span data-stu-id="11068-104">Microsoft RPC provides multiple levels of authentication.</span></span> <span data-ttu-id="11068-105">En fonction du niveau d’authentification, l’origine du trafic (le principal de sécurité qui a envoyé le trafic) peut être vérifiée lorsque la connexion est établie, lorsque le client démarre un nouvel appel de procédure distante ou au cours de chaque échange de paquets entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="11068-105">Depending on the authentication level, the origin of the traffic (which security principal sent the traffic) can be verified when the connection is established, when the client starts a new remote procedure call, or during each packet exchange between the client and server.</span></span>

<span data-ttu-id="11068-106">Même lorsque l’expéditeur du trafic est vérifié, la sécurité est toujours faible, car cette vérification ne garantit pas que le paquet n’a pas été modifié ou endommagé en cours d’acheminement. Il vérifie uniquement que le paquet provient du principal donné.</span><span class="sxs-lookup"><span data-stu-id="11068-106">Even when the sender of the traffic is verified, security is still weak, since such verification does not ensure the packet was not modified or corrupted en route; it only verifies that the packet came from the given principal.</span></span> <span data-ttu-id="11068-107">Pour une sécurité accrue, les applications distribuées peuvent définir la bibliothèque Runtime RPC pour vérifier qu’aucune des données échangées entre le client et le serveur n’est modifiée.</span><span class="sxs-lookup"><span data-stu-id="11068-107">For greater security, distributed applications can set the RPC run-time library to verify that none of the data exchanged between the client and server is modified.</span></span> <span data-ttu-id="11068-108">La bibliothèque RPC peut également chiffrer le contenu de chaque paquet avant de l’envoyer.</span><span class="sxs-lookup"><span data-stu-id="11068-108">The RPC library can also encrypt the contents of every packet before sending it.</span></span> <span data-ttu-id="11068-109">En général, les applications qui souhaitent sécuriser leur trafic doivent utiliser uniquement les deux derniers niveaux : l’intégrité et la confidentialité.</span><span class="sxs-lookup"><span data-stu-id="11068-109">In general, applications that want to secure their traffic should use only the last two levels—integrity and privacy.</span></span>

<span data-ttu-id="11068-110">Sachez que les niveaux d’authentification plus élevés nécessitent une surcharge de calcul plus élevée.</span><span class="sxs-lookup"><span data-stu-id="11068-110">Be aware that higher levels of authentication require higher computational overhead.</span></span> <span data-ttu-id="11068-111">En tant que développeur, vous devez décider de ce qui est plus important pour votre application : la vitesse ou la sécurité.</span><span class="sxs-lookup"><span data-stu-id="11068-111">You, as the developer, must decide which is more important for your application—speed or security.</span></span> <span data-ttu-id="11068-112">La plupart des développeurs trouvent qu’avec des tests de performances, ils peuvent atteindre des niveaux de performances acceptables tout en conservant une sécurité appropriée.</span><span class="sxs-lookup"><span data-stu-id="11068-112">Most developers find that with some performance testing, they can achieve acceptable performance levels while maintaining adequate security.</span></span>

<span data-ttu-id="11068-113">Les parties client et serveur de l’application distribuée doivent utiliser le même niveau d’authentification.</span><span class="sxs-lookup"><span data-stu-id="11068-113">The client and the server portions of the distributed application must use the same authentication level.</span></span> <span data-ttu-id="11068-114">Pour obtenir la liste des niveaux d’authentification RPC, consultez [constantes au niveau de l’authentification](authentication-level-constants.md).</span><span class="sxs-lookup"><span data-stu-id="11068-114">For a list of RPC authentication levels, see [Authentication-Level Constants](authentication-level-constants.md).</span></span>

 

 




