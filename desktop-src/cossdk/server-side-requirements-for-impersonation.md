---
description: Server-Side la configuration requise pour l’emprunt d’identité
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side la configuration requise pour l’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515782"
---
# <a name="server-side-requirements-for-impersonation"></a><span data-ttu-id="e767a-103">Server-Side la configuration requise pour l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="e767a-103">Server-Side Requirements for Impersonation</span></span>

<span data-ttu-id="e767a-104">Le serveur effectue l’emprunt d’identité par programmation.</span><span class="sxs-lookup"><span data-stu-id="e767a-104">The server performs impersonation programmatically.</span></span> <span data-ttu-id="e767a-105">Il suppose explicitement les informations d’identification de sécurité du client à l’aide de [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span><span class="sxs-lookup"><span data-stu-id="e767a-105">It explicitly assumes the client's security credentials by using [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="e767a-106">Lorsque le client a accordé au serveur une autorité suffisante, cela a pour effet de remplacer les informations d’identification de sécurité du client par le jeton de thread du serveur, à la place du jeton de processus.</span><span class="sxs-lookup"><span data-stu-id="e767a-106">When the client has granted the server sufficient authority, this has the effect of substituting the client's security credentials with the server thread token, in place of the process token.</span></span>

<span data-ttu-id="e767a-107">Une fois cette opération effectuée, le serveur peut, par exemple, utiliser le jeton client pour accéder aux ressources protégées par un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e767a-107">When this has been done, the server can, for example, use the client token to access resources guarded with a security descriptor.</span></span> <span data-ttu-id="e767a-108">Ou elle peut effectuer des appels sous l’identité du client, si le masquage est activé.</span><span class="sxs-lookup"><span data-stu-id="e767a-108">Or it can make calls under the client identity, if cloaking is enabled.</span></span>

<span data-ttu-id="e767a-109">Le serveur peut explicitement définir le masquage par programme, ou il peut s’appuyer sur un paramètre d’administration.</span><span class="sxs-lookup"><span data-stu-id="e767a-109">The server can explicitly set cloaking programmatically, or it can rely on an administrative setting.</span></span> <span data-ttu-id="e767a-110">Par défaut, les applications COM+ sont configurées pour utiliser le masquage dynamique.</span><span class="sxs-lookup"><span data-stu-id="e767a-110">By default, COM+ applications are configured to use dynamic cloaking.</span></span> <span data-ttu-id="e767a-111">Pour plus d’informations, consultez [masquage](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="e767a-111">For more detail, see [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="e767a-112">Si le serveur implémente la délégation pour le compte du client (à l’aide de l’identité du client sur le réseau), l’identité du processus serveur doit être marquée comme « approuvée pour la délégation » dans le service Active Directory ; dans le cas contraire, la délégation échouera.</span><span class="sxs-lookup"><span data-stu-id="e767a-112">If the server is implementing delegation on behalf of the client—using the client identity over network—the server process identity must be marked as "Trusted for delegation" in the Active Directory Service; otherwise, delegation will fail.</span></span>

<span data-ttu-id="e767a-113">Lorsqu’il a terminé d’utiliser l’identité du client, le serveur peut revenir à son propre jeton de processus à l’aide de [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="e767a-113">When it has finished using the client's identity, the server can revert to its own process token using [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="e767a-114">Pour plus d’informations sur l’implémentation de l’emprunt d’identité et de la délégation, consultez [délégation et emprunt d’identité](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="e767a-114">For details on implementing impersonation and delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e767a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e767a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e767a-116">Emprunt d’identité et délégation du client</span><span class="sxs-lookup"><span data-stu-id="e767a-116">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="e767a-117">Exigences côté client pour l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="e767a-117">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="e767a-118">Masquer</span><span class="sxs-lookup"><span data-stu-id="e767a-118">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

 
