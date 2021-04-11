---
title: Services d’autorisation
description: Un service d’autorisation est la méthode utilisée par le fournisseur de services partagés pour autoriser l’accès à une procédure distante. Les SSP peuvent fournir plusieurs services d’autorisation. Toutefois, ils sélectionnent généralement un par défaut.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029520"
---
# <a name="authorization-services"></a><span data-ttu-id="31d79-105">Services d’autorisation</span><span class="sxs-lookup"><span data-stu-id="31d79-105">Authorization Services</span></span>

<span data-ttu-id="31d79-106">Un service d’autorisation est la méthode utilisée par le fournisseur de services partagés pour autoriser l’accès à une procédure distante.</span><span class="sxs-lookup"><span data-stu-id="31d79-106">An authorization service is the method that the SSP uses to authorize access to a remote procedure.</span></span> <span data-ttu-id="31d79-107">Les SSP peuvent fournir plusieurs services d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="31d79-107">SSPs can provide more than one authorization service.</span></span> <span data-ttu-id="31d79-108">Toutefois, ils sélectionnent généralement un par défaut.</span><span class="sxs-lookup"><span data-stu-id="31d79-108">However, they usually select one as a default.</span></span>

<span data-ttu-id="31d79-109">Votre application peut utiliser la méthode d’autorisation par défaut pour le fournisseur de services partagés actuel ou en spécifier une.</span><span class="sxs-lookup"><span data-stu-id="31d79-109">Your application can use the default authorization method for the current SSP, or it can specify one.</span></span> <span data-ttu-id="31d79-110">À l’heure actuelle, Microsoft RPC prend en charge deux méthodes d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="31d79-110">At present, Microsoft RPC supports two methods of authorization.</span></span> <span data-ttu-id="31d79-111">L’un est pour le serveur de fournir une autorisation basée sur le nom du programme client.</span><span class="sxs-lookup"><span data-stu-id="31d79-111">One is for the server to provide authorization based on the name of the client program.</span></span> <span data-ttu-id="31d79-112">L’autre est que le serveur compare les informations d’identification d’authentification du client à la liste de contrôle d’accès (ACL) du serveur.</span><span class="sxs-lookup"><span data-stu-id="31d79-112">The other is for the server to compare the client's authentication credentials against the server's access control list (ACL).</span></span>

<span data-ttu-id="31d79-113">Pour obtenir la liste des services d’autorisation, consultez [autorisations-services, constantes](authorization-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="31d79-113">For a list of authorization services, see [Authorization-Service Constants](authorization-service-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="31d79-114">Il est recommandé que les développeurs utilisent l’autorisation RPC \_ C \_ auth \_ aucun.</span><span class="sxs-lookup"><span data-stu-id="31d79-114">It is recommended that developers use RPC\_C\_AUTHZ\_NONE.</span></span>

 

 

 




