---
description: Négociation du niveau d’authentification
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Négociation du niveau d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513333"
---
# <a name="negotiation-of-authentication-level"></a><span data-ttu-id="c923e-103">Négociation du niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="c923e-103">Negotiation of Authentication Level</span></span>

<span data-ttu-id="c923e-104">Le client et le serveur doivent participer à l’authentification, et chaque tiers indique qu’il souhaite effectuer un certain niveau d’authentification.</span><span class="sxs-lookup"><span data-stu-id="c923e-104">Both client and server must participate in authentication, and each party indicates that it wants to perform a certain level of authentication.</span></span> <span data-ttu-id="c923e-105">Au début d’un appel, le niveau d’authentification est négocié entre les deux parties, un service approprié est choisi, et l’appel est authentifié et se poursuit (avec un chiffrement possible, selon le niveau d’authentification choisi).</span><span class="sxs-lookup"><span data-stu-id="c923e-105">At the beginning of a call, the authentication level is negotiated between the two parties, an appropriate service is chosen, and the call is authenticated and proceeds (with possible encryption, depending on the authentication level chosen).</span></span> <span data-ttu-id="c923e-106">Le niveau d’authentification négocié entre le client et le serveur est déterminé comme étant maximal (*préférence du client*, *préférence du serveur*).</span><span class="sxs-lookup"><span data-stu-id="c923e-106">The authentication level negotiated between client and server is determined as Maximum(*Client preference*, *Server preference*).</span></span> <span data-ttu-id="c923e-107">L’effet de cela signifie que le serveur peut toujours dicter un niveau minimal d’authentification avec lequel il est familiarisé. autrement dit, l’authentification peut être imposée de façon administrative à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="c923e-107">The effect of this means that the server can always dictate a minimum level of authentication that it is comfortable with; that is, authentication can be administratively dictated from the server.</span></span>

<span data-ttu-id="c923e-108">Le client spécifie qu’il souhaite effectuer l’authentification à un certain niveau comme avec n’importe quelle application COM.</span><span class="sxs-lookup"><span data-stu-id="c923e-108">The client specifies that it wants to perform authentication at a certain level as with any COM application.</span></span> <span data-ttu-id="c923e-109">Le niveau d’authentification du client peut être indiqué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c923e-109">The client authentication level can be indicated as follows:</span></span>

-   <span data-ttu-id="c923e-110">Par ordinateur client, avec le niveau d’authentification COM à l’échelle de l’ordinateur défini à l’aide de [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) ou de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="c923e-110">Per client machine, with the machine-wide COM authentication level set by using either [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) or the Component Services administrative tool.</span></span>
-   <span data-ttu-id="c923e-111">Par application cliente administrativement, à l’aide de [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) ou de l’outil d’administration Services de composants si le client doit être une application com+.</span><span class="sxs-lookup"><span data-stu-id="c923e-111">Per client application administratively, using [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) or using the Component Services administrative tool if the client should be a COM+ application.</span></span>
-   <span data-ttu-id="c923e-112">Par programme client par programme, avec la procédure [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c923e-112">Per client process programmatically, with [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="c923e-113">À tout moment, par programmation, à l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="c923e-113">At any point programmatically, using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="c923e-114">L’application serveur COM+ spécifie un niveau d’authentification de manière administrative à l’aide de l’outil d’administration Services de composants (ou d’un script d’administration).</span><span class="sxs-lookup"><span data-stu-id="c923e-114">The COM+ server application specifies an authentication level administratively by using the Component Services administrative tool (or through an administrative script).</span></span>

<span data-ttu-id="c923e-115">La négociation de l’authentification pour un appel se poursuit dans la séquence suivante :</span><span class="sxs-lookup"><span data-stu-id="c923e-115">Negotiating authentication for a call proceeds in the following sequence:</span></span>

1.  <span data-ttu-id="c923e-116">Le niveau d’authentification est choisi comme maximum (*client*, *serveur*).</span><span class="sxs-lookup"><span data-stu-id="c923e-116">Authentication level is chosen as MAX(*client*, *server*).</span></span>
2.  <span data-ttu-id="c923e-117">Négociation du protocole d’authentification.</span><span class="sxs-lookup"><span data-stu-id="c923e-117">Negotiation of authentication protocol.</span></span>
3.  <span data-ttu-id="c923e-118">Le serveur authentifie l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="c923e-118">Server authenticates client identity.</span></span>
4.  <span data-ttu-id="c923e-119">Le cas échéant, le client authentifie l’identité du serveur, en fonction du protocole d’authentification.</span><span class="sxs-lookup"><span data-stu-id="c923e-119">Optionally, client authenticates server identity, depending on the authentication protocol.</span></span>
5.  <span data-ttu-id="c923e-120">Les appels de méthode sont communiqués avec le niveau d’authentification choisi.</span><span class="sxs-lookup"><span data-stu-id="c923e-120">Method calls are communicated with the chosen level of authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c923e-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c923e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c923e-122">Authentification du client</span><span class="sxs-lookup"><span data-stu-id="c923e-122">Client Authentication</span></span>](client-authentication.md)
</dt> </dl>

 

 
