---
title: Appels de procédure distante à l’aide de RPC sur HTTP
description: Les programmes de navigation Internet emploient généralement le protocole HTTP (Hypertext Transport Protocol) comme moyen principal de parcourir les World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Appel de procédure distante RPC, tâches, à l’aide de RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939559"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a><span data-ttu-id="e3ad8-104">Appels de procédure distante à l’aide de RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="e3ad8-104">Remote Procedure Calls Using RPC over HTTP</span></span>

<span data-ttu-id="e3ad8-105">Les programmes de navigation Internet emploient généralement le protocole HTTP (Hypertext Transport Protocol) comme moyen principal de parcourir les World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-105">Internet browser programs commonly employ the Hypertext Transport Protocol (HTTP) as the primary means of browsing the World Wide Web.</span></span> <span data-ttu-id="e3ad8-106">HTTP, par conséquent, voit une utilisation intensive sur la plupart des ordinateurs dès aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-106">HTTP, therefore, sees extensive usage on most computers today.</span></span> <span data-ttu-id="e3ad8-107">Microsoft a étendu les fonctionnalités de son Internet Information Server (IIS) pour fournir des services d’appel de procédure distante à l’aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-107">Microsoft has extended the capabilities of its Internet Information Server (IIS) to provide remote procedure call services using HTTP.</span></span>

<span data-ttu-id="e3ad8-108">L’implémentation Microsoft RPC sur http (RPC sur HTTP) permet aux clients RPC de se connecter en toute sécurité et de manière efficace via Internet à des programmes serveur RPC et d’exécuter des appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-108">The Microsoft RPC-over-HTTP implementation (RPC over HTTP) allows RPC clients to securely and efficiently connect across the Internet to RPC server programs and execute remote procedure calls.</span></span> <span data-ttu-id="e3ad8-109">Cela s’effectue à l’aide d’un intermédiaire appelé proxy RPC sur HTTP, ou simplement du proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-109">This is accomplished with the help of an intermediary known as the RPC-over-HTTP Proxy, or simply the RPC Proxy.</span></span>

<span data-ttu-id="e3ad8-110">Le proxy RPC s’exécute sur un ordinateur IIS.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-110">The RPC Proxy runs on an IIS computer.</span></span> <span data-ttu-id="e3ad8-111">Il accepte les demandes RPC provenant d’Internet, effectue des vérifications d’authentification, de validation et d’accès sur ces requêtes et, si la demande réussit tous les tests, le proxy RPC transfère la demande au serveur RPC qui effectue le traitement réel.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-111">It accepts RPC requests coming from the Internet, performs authentication, validation, and access checks on those requests, and if the request passes all tests, RPC Proxy forwards the request to the RPC server that performs the actual processing.</span></span> <span data-ttu-id="e3ad8-112">Avec RPC sur HTTP, le client et le serveur RPC ne communiquent pas directement ; au lieu de cela, ils utilisent le proxy RPC comme intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-112">With RPC over HTTP the RPC client and server do not communicate directly; rather, they use the RPC Proxy as intermediary.</span></span> <span data-ttu-id="e3ad8-113">Ce modèle a été choisi pour de nombreuses raisons.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-113">This model was chosen for many reasons.</span></span> <span data-ttu-id="e3ad8-114">Pour plus d’informations, consultez [RPC sur la sécurité http](rpc-over-http-security.md).</span><span class="sxs-lookup"><span data-stu-id="e3ad8-114">For more information, see [RPC over HTTP Security](rpc-over-http-security.md).</span></span>

<span data-ttu-id="e3ad8-115">Cette section fournit une vue d’ensemble de RPC sur HTTP dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3ad8-115">This section provides an overview of RPC over HTTP in the following topics:</span></span>

-   [<span data-ttu-id="e3ad8-116">Utilisation de HTTP comme transport RPC</span><span class="sxs-lookup"><span data-stu-id="e3ad8-116">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
-   [<span data-ttu-id="e3ad8-117">Sécurité RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="e3ad8-117">RPC over HTTP Security</span></span>](rpc-over-http-security.md)
-   [<span data-ttu-id="e3ad8-118">Configuration système requise et interopérabilité pour RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="e3ad8-118">System Requirements and Interoperability for RPC over HTTP</span></span>](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [<span data-ttu-id="e3ad8-119">Configuration des ordinateurs pour RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="e3ad8-119">Configuring Computers for RPC over HTTP</span></span>](configuring-computers-for-rpc-over-http.md)
-   [<span data-ttu-id="e3ad8-120">Recommandations relatives au déploiement de RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="e3ad8-120">RPC over HTTP Deployment Recommendations</span></span>](rpc-over-http-deployment-recommendations.md)

<span data-ttu-id="e3ad8-121">Pour plus d’informations sur les scénarios RPC sur HTTP volumineux, consultez [équilibrage de charge Microsoft RPC](rpc-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="e3ad8-121">For information regarding high volume RPC over HTTP scenarios, please see [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span></span>

 

 




