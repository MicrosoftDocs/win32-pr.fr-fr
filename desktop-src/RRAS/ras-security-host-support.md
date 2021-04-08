---
title: Prise en charge de l’hôte de sécurité RAS
description: Windows NT 4,0 fournit un moyen pour une DLL de sécurité RAS tierce pour améliorer les fonctionnalités de sécurité RAS intégrées. Windows 95 ne fournit pas cette prise en charge.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Prise en charge des hôtes, RAS
- Prise en charge de l’hôte de sécurité, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674026"
---
# <a name="ras-security-host-support"></a><span data-ttu-id="5379a-106">Prise en charge de l’hôte de sécurité RAS</span><span class="sxs-lookup"><span data-stu-id="5379a-106">RAS Security Host Support</span></span>

<span data-ttu-id="5379a-107">Windows NT 4,0 fournit un moyen pour une DLL de sécurité RAS tierce pour améliorer les fonctionnalités de sécurité RAS intégrées.</span><span class="sxs-lookup"><span data-stu-id="5379a-107">Windows NT 4.0 provides a way for a third-party RAS security DLL to enhance the built-in RAS security features.</span></span> <span data-ttu-id="5379a-108">Windows 95 ne fournit pas cette prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5379a-108">Windows 95 does not provide this support.</span></span>

<span data-ttu-id="5379a-109">Un serveur RAS Windows NT/Windows 2000 fournit des mécanismes de sécurité pour valider l’accès réseau des utilisateurs distants.</span><span class="sxs-lookup"><span data-stu-id="5379a-109">A Windows NT/Windows 2000 RAS server provides security mechanisms for validating the network access of remote users.</span></span> <span data-ttu-id="5379a-110">Lorsqu’un serveur RAS reçoit un appel, il valide les informations d’identification de l’utilisateur par rapport à la base de données de comptes locaux ou de domaine.</span><span class="sxs-lookup"><span data-stu-id="5379a-110">When a RAS server receives a call, it validates the user's credentials against the local or domain account database.</span></span> <span data-ttu-id="5379a-111">RAS prend également en charge la sécurité de rappel, dans laquelle le serveur RAS se bloque, puis rappelle à l’utilisateur distant pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="5379a-111">RAS also supports call-back security, in which the RAS server hangs up and then calls back to the remote user to establish the connection.</span></span> <span data-ttu-id="5379a-112">Pour les réseaux dans lesquels ce niveau de sécurité n’est pas suffisant, vous pouvez installer une DLL de sécurité RAS tierce.</span><span class="sxs-lookup"><span data-stu-id="5379a-112">For networks in which this level of security is not enough, you can install a third-party RAS security DLL.</span></span> <span data-ttu-id="5379a-113">La DLL de sécurité peut ensuite authentifier un utilisateur distant en lisant les informations de sécurité dans une base de données autre que la base de données de compte d’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="5379a-113">The security DLL can then authenticate a remote user by reading security information from a database other than the standard user account database.</span></span>

<span data-ttu-id="5379a-114">Lorsque le serveur RAS reçoit un appel, il appelle la DLL de sécurité pour authentifier l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="5379a-114">When the RAS server receives a call, it invokes the security DLL to authenticate the remote user.</span></span> <span data-ttu-id="5379a-115">La prise en charge de l’hôte de sécurité RAS fournit un mécanisme permettant à la DLL de sécurité de communiquer avec l’utilisateur distant par le biais d’une fenêtre de terminal sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="5379a-115">The RAS security host support provides a mechanism for the security DLL to communicate with the remote user through a terminal window on the remote computer.</span></span> <span data-ttu-id="5379a-116">Dans un scénario classique, la DLL de sécurité demande le nom d’ouverture de session de l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="5379a-116">In a typical scenario, the security DLL asks for the logon name of the remote user.</span></span> <span data-ttu-id="5379a-117">La DLL utilise ensuite sa base de données de sécurité privée pour formuler un défi à envoyer au terminal distant.</span><span class="sxs-lookup"><span data-stu-id="5379a-117">The DLL then uses its private security database to formulate a challenge to send to the remote terminal.</span></span> <span data-ttu-id="5379a-118">Par exemple, le défi peut être un code que l’utilisateur doit fournir comme entrée à un lecteur Cardkey.</span><span class="sxs-lookup"><span data-stu-id="5379a-118">For example, the challenge could be a code that the user must provide as input to a cardkey reader.</span></span> <span data-ttu-id="5379a-119">Le lecteur Cardkey affiche ensuite une réponse que l’utilisateur distant tape dans la fenêtre de terminal.</span><span class="sxs-lookup"><span data-stu-id="5379a-119">The cardkey reader then displays a response that the remote user types in the terminal window.</span></span> <span data-ttu-id="5379a-120">La DLL de sécurité valide ensuite la réponse par rapport aux informations de l’utilisateur dans la base de données de sécurité privée.</span><span class="sxs-lookup"><span data-stu-id="5379a-120">The security DLL then validates the response against the user's information in the private security database.</span></span>

<span data-ttu-id="5379a-121">Si la DLL de sécurité authentifie l’utilisateur distant, le serveur RAS effectue sa propre authentification.</span><span class="sxs-lookup"><span data-stu-id="5379a-121">If the security DLL authenticates the remote user, the RAS server performs its own authentication.</span></span> <span data-ttu-id="5379a-122">Cela garantit que la sécurité RAS authentifie toujours un utilisateur distant, même si une DLL de sécurité qui accorde l’accès à tous les utilisateurs est installée.</span><span class="sxs-lookup"><span data-stu-id="5379a-122">This ensures that RAS security always authenticates a remote user, even if a security DLL is installed that grants access to all users.</span></span>

> [!Note]  
> <span data-ttu-id="5379a-123">Windows NT/Windows 2000 fournit actuellement la prise en charge de l’hôte de sécurité RAS uniquement pour les connexions de modem asynchrones. les autres types de connexions, comme Ethernet (qui n’est pas une connexion par modem), VPN (qui n’est pas non plus une connexion par modem) ou RNIS (qui est synchrone), ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5379a-123">Windows NT/Windows 2000 currently provides RAS security host support only for asynchronous modem connections; other types of connections such as Ethernet (which is not a modem connection), VPN (which is also not a modem connection), or ISDN (which is synchronous), are not supported.</span></span>

 

 

 




