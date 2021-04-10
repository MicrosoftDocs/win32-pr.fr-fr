---
title: Opérations synchrones
description: Lorsque RasDial est appelé en tant qu’opération synchrone, la fonction ne retourne pas tant que la connexion n’a pas été établie ou qu’une erreur ne se produit pas.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029694"
---
# <a name="synchronous-operations"></a><span data-ttu-id="17abe-103">Opérations synchrones</span><span class="sxs-lookup"><span data-stu-id="17abe-103">Synchronous Operations</span></span>

<span data-ttu-id="17abe-104">Lorsque [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) est appelé en tant qu’opération synchrone, la fonction ne retourne pas tant que la connexion n’a pas été établie ou qu’une erreur ne se produit pas.</span><span class="sxs-lookup"><span data-stu-id="17abe-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as a synchronous operation, the function does not return until the connection has been established or an error occurs.</span></span> <span data-ttu-id="17abe-105">Le mode synchrone offre un moyen simple pour un client RAS d’établir une connexion.</span><span class="sxs-lookup"><span data-stu-id="17abe-105">Synchronous mode provides a simple way for a RAS client to establish a connection.</span></span> <span data-ttu-id="17abe-106">Le client peut simplement appeler **rasdial**, attendre la fin du retour de la fonction, puis appeler la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour déterminer si l’opération de connexion a réussi.</span><span class="sxs-lookup"><span data-stu-id="17abe-106">The client can simply call **RasDial**, wait for the function to return, and then call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to determine whether the connection operation was successful.</span></span> <span data-ttu-id="17abe-107">Une fois la connexion établie, l’application cliente peut se terminer sans rompre la connexion.</span><span class="sxs-lookup"><span data-stu-id="17abe-107">Once the connection has been established, the client application can terminate without breaking the connection.</span></span> <span data-ttu-id="17abe-108">Si une erreur se produit, l’application cliente doit [arrêter l’opération de connexion avant de](disconnecting.md) se terminer.</span><span class="sxs-lookup"><span data-stu-id="17abe-108">If an error occurs, the client application must [shut down the connection operation](disconnecting.md) before terminating.</span></span>

<span data-ttu-id="17abe-109">L’inconvénient du mode synchrone est que le client ne reçoit pas de notifications de progression lorsque l’opération de connexion continue.</span><span class="sxs-lookup"><span data-stu-id="17abe-109">The disadvantage of synchronous mode is that the client does not receive progress notifications as the connection operation proceeds.</span></span> <span data-ttu-id="17abe-110">En guise de solution de contournement pour ce manque de notifications de progression, un client en mode synchrone peut utiliser un thread distinct qui appelle [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour interroger et afficher l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="17abe-110">As a workaround for this lack of progress notifications, a synchronous mode client can use a separate thread that calls [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) to poll for and display the current state.</span></span> <span data-ttu-id="17abe-111">Toutefois, pour les clients RAS qui souhaitent recevoir des informations de progression, la méthode recommandée consiste à appeler [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="17abe-111">However, for RAS clients that want to receive progress information, the preferred technique is to invoke [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchronously.</span></span>

 

 




