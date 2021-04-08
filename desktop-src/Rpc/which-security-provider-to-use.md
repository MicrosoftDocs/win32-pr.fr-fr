---
title: Le fournisseur de sécurité à utiliser
description: Tous les autres éléments sont égaux, utilisez RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673246"
---
# <a name="which-security-provider-to-use"></a><span data-ttu-id="77544-103">Le fournisseur de sécurité à utiliser</span><span class="sxs-lookup"><span data-stu-id="77544-103">Which Security Provider to Use</span></span>

<span data-ttu-id="77544-104">Tous les autres éléments sont égaux, utilisez RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.</span><span class="sxs-lookup"><span data-stu-id="77544-104">All other things being equal, use RPC\_C\_AUTHN\_GSS\_KERBEROS or RPC\_C\_AUTHN\_GSS\_NEGOTIATE.</span></span> <span data-ttu-id="77544-105">Chaque offre le service le plus évolutif et le plus sécurisé.</span><span class="sxs-lookup"><span data-stu-id="77544-105">Each provides the most scalable and secure service.</span></span> <span data-ttu-id="77544-106">Si vous utilisez RPC \_ C \_ Authn \_ GSS \_ Negotiate sur le serveur, les clients de niveau supérieur, tels que les clients NTLM, peuvent se connecter à votre serveur.</span><span class="sxs-lookup"><span data-stu-id="77544-106">If you use RPC\_C\_AUTHN\_GSS\_NEGOTIATE on the server, this allows down-level clients, such as NTLM clients, to connect to your server.</span></span> <span data-ttu-id="77544-107">Si ce n’est pas souhaitable, limitez le choix à RPC \_ C \_ Authn \_ GSS \_ Kerberos uniquement, ou appelez [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) pour déterminer le fournisseur de sécurité utilisé par le client et refuser l’accès aux clients à l’aide de NTLM.</span><span class="sxs-lookup"><span data-stu-id="77544-107">If that is undesirable, either limit the choice to RPC\_C\_AUTHN\_GSS\_KERBEROS only, or call [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to determine which security provider the client is using, and deny access to clients using NTLM.</span></span> <span data-ttu-id="77544-108">La méthode recommandée pour déterminer quel fournisseur de sécurité est utilisé par le client est la fonction [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .</span><span class="sxs-lookup"><span data-stu-id="77544-108">The preferred method of establishing which security provider the client is using is the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function.</span></span>

 

 




