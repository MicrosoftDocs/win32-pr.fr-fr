---
title: Sécurité Server-Side
description: Sécurité Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941401"
---
# <a name="server-side-security"></a><span data-ttu-id="766ed-103">Sécurité Server-Side</span><span class="sxs-lookup"><span data-stu-id="766ed-103">Server-Side Security</span></span>

<span data-ttu-id="766ed-104">Le serveur peut récupérer des informations de sécurité sur un appelant ou emprunter l’identité de l’appelant à l’aide des méthodes de [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span><span class="sxs-lookup"><span data-stu-id="766ed-104">The server can retrieve security information about a caller or impersonate the caller by using the methods of [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span></span> <span data-ttu-id="766ed-105">Une implémentation de **IServerSecurity** est fournie par com sur l’objet de contexte pour l’appel actuel lorsque le marshaling standard est utilisé.</span><span class="sxs-lookup"><span data-stu-id="766ed-105">An implementation of **IServerSecurity** is supplied by COM on the context object for the current call when standard marshaling is used.</span></span> <span data-ttu-id="766ed-106">Toutefois, cette interface peut être absente pour certaines interfaces marshalées personnalisées.</span><span class="sxs-lookup"><span data-stu-id="766ed-106">However, this interface may be absent for some custom-marshaled interfaces.</span></span>

<span data-ttu-id="766ed-107">Lorsqu’un appel arrive sur le serveur, le serveur peut appeler [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) pour obtenir un pointeur vers l’interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) .</span><span class="sxs-lookup"><span data-stu-id="766ed-107">When a call arrives at the server, the server can call [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to the [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface.</span></span> <span data-ttu-id="766ed-108">Avec ce pointeur, les méthodes **IServerSecurity** peuvent être appelées par le serveur pour connaître les paramètres d’authentification du client et pour emprunter l’identité du client, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="766ed-108">With this pointer, **IServerSecurity** methods can be called by the server to find out what the client's authentication settings are and to impersonate the client, if needed.</span></span> <span data-ttu-id="766ed-109">L’objet **IServerSecurity** est valide sur n’importe quel thread du cloisonnement jusqu’à ce que l’appel représenté par **IServerSecurity** se termine.</span><span class="sxs-lookup"><span data-stu-id="766ed-109">The **IServerSecurity** object is valid on any thread in the apartment until the call represented by **IServerSecurity** completes.</span></span> <span data-ttu-id="766ed-110">Pour plus d’informations sur l’emprunt d’identité, consultez [emprunt d’identité](impersonation.md) et [masquage](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="766ed-110">For more information about impersonation, see [Impersonation](impersonation.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="766ed-111">Les fonctions d’assistance suivantes qui reposent sur l’implémentation de l’interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) de l’objet de contexte d’appel sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="766ed-111">The following helper functions that rely on the call context object's [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface implementation are also available:</span></span>

-   [<span data-ttu-id="766ed-112">**CoQueryClientBlanket**</span><span class="sxs-lookup"><span data-stu-id="766ed-112">**CoQueryClientBlanket**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [<span data-ttu-id="766ed-113">**CoImpersonateClient**</span><span class="sxs-lookup"><span data-stu-id="766ed-113">**CoImpersonateClient**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [<span data-ttu-id="766ed-114">**CoRevertToSelf**</span><span class="sxs-lookup"><span data-stu-id="766ed-114">**CoRevertToSelf**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a><span data-ttu-id="766ed-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="766ed-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="766ed-116">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="766ed-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 