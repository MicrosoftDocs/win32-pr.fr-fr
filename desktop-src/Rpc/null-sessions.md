---
title: Sessions null
description: Parfois, un appel arrivant sur la session NULL peut apparaître comme un appel authentifié.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462415"
---
# <a name="null-sessions"></a><span data-ttu-id="7349f-103">Sessions null</span><span class="sxs-lookup"><span data-stu-id="7349f-103">Null Sessions</span></span>

<span data-ttu-id="7349f-104">Parfois, un appel arrivant sur la session NULL peut apparaître comme un appel authentifié.</span><span class="sxs-lookup"><span data-stu-id="7349f-104">Sometimes a call arriving on the null session can appear like an authenticated call.</span></span> <span data-ttu-id="7349f-105">Plus précisément, l’appel de la fonction [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) retourne le niveau d’authentification et le fournisseur de sécurité utilisés pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="7349f-105">Specifically, calling the [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function returns the authentication level and security provider used for the call.</span></span> <span data-ttu-id="7349f-106">Cette opération ne signifie pas que l’appel n’était pas sur une session NULL.</span><span class="sxs-lookup"><span data-stu-id="7349f-106">This operation does not mean the call was not on a null session.</span></span> <span data-ttu-id="7349f-107">Les deux problèmes sont orthogonals.</span><span class="sxs-lookup"><span data-stu-id="7349f-107">The two issues are orthogonal.</span></span> <span data-ttu-id="7349f-108">Sur Microsoft Windows 2000, un appel de procédure distante peut tenter d’emprunter l’identité d’un appelant et vérifier les autorisations après l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="7349f-108">On Microsoft Windows 2000, a remote procedure call can attempt to impersonate a caller and check the permissions after impersonation.</span></span> <span data-ttu-id="7349f-109">Sur Microsoft Windows XP, il est plus rapide d’appeler la fonction [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) et de vérifier l’indicateur **NullSession** .</span><span class="sxs-lookup"><span data-stu-id="7349f-109">On Microsoft Windows XP, it is faster to call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function and check for the **NullSession** flag.</span></span>

<span data-ttu-id="7349f-110">Il existe une autre différence pertinente entre Windows 2000 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7349f-110">Another relevant difference exists between Windows 2000 and Windows XP.</span></span> <span data-ttu-id="7349f-111">Si seul l’indicateur RPC uniquement si l’option \_ \_ autoriser les \_ sécurisés \_ est spécifié, les appels sur la session NULL sont effectués dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7349f-111">If only the RPC\_IF\_ALLOW\_SECURE\_ONLY flag is specified, calls on the null session go through in Windows 2000.</span></span> <span data-ttu-id="7349f-112">Dans Windows XP, avec le renforcement général des paramètres de sécurité par défaut, lorsque cet indicateur est spécifié, les appels sur la session NULL sont rejetés avec l’accès refusé.</span><span class="sxs-lookup"><span data-stu-id="7349f-112">In Windows XP, with the general tightening of default security settings, when this flag is specified, calls on the null session are rejected with access denied.</span></span> <span data-ttu-id="7349f-113">Toutefois, même avec l' \_ indicateur RPC if \_ allow \_ Secure \_ only, RPC ne garantit pas le niveau de privilège de l’utilisateur appelant.</span><span class="sxs-lookup"><span data-stu-id="7349f-113">However, even with the RPC\_IF\_ALLOW\_SECURE\_ONLY flag, RPC does not guarantee the privilege level of the calling user.</span></span> <span data-ttu-id="7349f-114">Toutes les vérifications RPC sont que l’utilisateur dispose d’informations d’identification valides.</span><span class="sxs-lookup"><span data-stu-id="7349f-114">All RPC checks is that the user has valid credentials.</span></span> <span data-ttu-id="7349f-115">Il est possible que l’utilisateur appelant utilise le compte invité ou d’autres comptes à faibles privilèges.</span><span class="sxs-lookup"><span data-stu-id="7349f-115">It is possible that the calling user is using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="7349f-116">Assurez-vous que le serveur n’assume pas un privilège élevé une fois RPC \_ si l' \_ autorisation \_ sécurisée \_ uniquement est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7349f-116">Make sure the server does not assume high privilege once RPC\_IF\_ALLOW\_SECURE\_ONLY is used.</span></span>

 

 




