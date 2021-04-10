---
title: Informations d’identification d’authentification du client
description: Chaque client authentifié doit fournir des informations d’authentification au serveur.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029787"
---
# <a name="client-authentication-credentials"></a><span data-ttu-id="f88e8-103">Informations d’identification d’authentification du client</span><span class="sxs-lookup"><span data-stu-id="f88e8-103">Client Authentication Credentials</span></span>

<span data-ttu-id="f88e8-104">Chaque client authentifié doit fournir des informations d’authentification au serveur.</span><span class="sxs-lookup"><span data-stu-id="f88e8-104">Each authenticated client must provide authentication credentials to the server.</span></span> <span data-ttu-id="f88e8-105">Sous RPC, le client stocke ses informations d’authentification dans la liaison entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="f88e8-105">Under RPC, the client stores its authentication credentials in the binding between the client and the server.</span></span> <span data-ttu-id="f88e8-106">Pour ce faire, le client appelle [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span><span class="sxs-lookup"><span data-stu-id="f88e8-106">To do this, the client calls [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span></span>

<span data-ttu-id="f88e8-107">Il existe deux types d’informations d’identification : implicite et explicite :</span><span class="sxs-lookup"><span data-stu-id="f88e8-107">There are two types of credentials—implicit and explicit:</span></span>

-   <span data-ttu-id="f88e8-108">Des informations d’identification explicites existent lorsque le client fournit le nom d’utilisateur, le mot de passe et le domaine.</span><span class="sxs-lookup"><span data-stu-id="f88e8-108">Explicit credentials exist when the client supplies username, password, and domain.</span></span>
-   <span data-ttu-id="f88e8-109">Des informations d’identification implicites existent lorsque le client utilise des informations d’identification du thread ou du jeton de processus appelant les fonctions **RpcBindingSetAuthInfo** ou **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="f88e8-109">Implicit credentials exist when the client uses credentials from the thread or process token calling the **RpcBindingSetAuthInfo** or **RpcBindingSetAuthInfoEx** functions.</span></span>

<span data-ttu-id="f88e8-110">Les clients doivent s’abstenir de fournir des informations d’identification explicites, car le stockage, la manipulation et la récupération d’un mot de passe utilisateur peuvent introduire une faille de sécurité dans un système distribué si des informations d’identification explicites sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="f88e8-110">Clients should refrain from supplying explicit credentials because storing, manipulating, and retrieving a user password can introduce a security vulnerability into a distributed system if explicit credentials are used.</span></span>

<span data-ttu-id="f88e8-111">Pour utiliser des informations d’identification implicites, le client appelle **RpcBindingSetAuthInfo**(*ex*).</span><span class="sxs-lookup"><span data-stu-id="f88e8-111">To use implicit credentials, the client calls **RpcBindingSetAuthInfo**(*Ex*).</span></span> <span data-ttu-id="f88e8-112">Le système de sécurité et RPC obtiennent les informations d’identification à partir du thread ou du jeton de processus pour une utilisation dans la session d’authentification.</span><span class="sxs-lookup"><span data-stu-id="f88e8-112">The security system and RPC obtain credentials from the thread or process token for use in the authentication session.</span></span>

<span data-ttu-id="f88e8-113">Si le client utilise des informations d’identification explicites, le cinquième paramètre de ces deux fonctions est de type [**RPC \_ auth \_ Identity \_ handle**](rpc-auth-identity-handle.md).</span><span class="sxs-lookup"><span data-stu-id="f88e8-113">If the client uses explicit credentials, the fifth parameter of these two functions is of type [**RPC\_AUTH\_IDENTITY\_HANDLE**](rpc-auth-identity-handle.md).</span></span> <span data-ttu-id="f88e8-114">Il s’agit d’un type flexible qui est un pointeur vers une structure de données.</span><span class="sxs-lookup"><span data-stu-id="f88e8-114">This is a flexible type that is a pointer to a data structure.</span></span> <span data-ttu-id="f88e8-115">Le contenu de la structure de données peut être différent avec chaque service d’authentification.</span><span class="sxs-lookup"><span data-stu-id="f88e8-115">The contents of the data structure can differ with each authentication service.</span></span> <span data-ttu-id="f88e8-116">À l’heure actuelle, les fournisseurs de sécurité partagés pris en charge par RPC requièrent que votre application définisse le **\_ handle d' \_ identité \_ RPC auth** pour pointer vers une structure d' [**\_ \_ \_ identité Winnt auth**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="f88e8-116">Currently, the SSPs that RPC supports require that your application set **RPC\_AUTH\_IDENTITY\_HANDLE** to point to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="f88e8-117">La structure de l' **\_ \_ \_ identité d’authentification Winnt** de la sec contient des champs pour un nom d’utilisateur, un domaine et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f88e8-117">The **SEC\_WINNT\_AUTH\_IDENTITY** structure contains fields for a user name, domain, and password.</span></span>

 

 




