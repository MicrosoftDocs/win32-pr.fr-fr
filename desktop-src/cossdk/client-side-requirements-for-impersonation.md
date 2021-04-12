---
description: Client-Side la configuration requise pour l’emprunt d’identité
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side la configuration requise pour l’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317941"
---
# <a name="client-side-requirements-for-impersonation"></a><span data-ttu-id="fb752-103">Client-Side la configuration requise pour l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="fb752-103">Client-Side Requirements for Impersonation</span></span>

<span data-ttu-id="fb752-104">Les deux paramètres suivants peuvent être spécifiés par rapport à l’emprunt d’identité côté client :</span><span class="sxs-lookup"><span data-stu-id="fb752-104">The following two settings can be specified relative to impersonation on the client side:</span></span>

-   <span data-ttu-id="fb752-105">Le niveau d’emprunt d’identité, qui indique la volonté du client de faire en sorte que le serveur utilise son identité.</span><span class="sxs-lookup"><span data-stu-id="fb752-105">Impersonation level, which indicates the client's willingness to have the server use its identity.</span></span>
-   <span data-ttu-id="fb752-106">Paramètre du service Active Directory par le biais duquel le compte client peut être marqué « le compte est sensible et ne peut pas être délégué », ce qui désactive la délégation.</span><span class="sxs-lookup"><span data-stu-id="fb752-106">A setting in the Active Directory Service through which the client account can be marked "Account is sensitive and cannot be delegated," which will disable delegation.</span></span>

<span data-ttu-id="fb752-107">Le niveau d’emprunt d’identité peut être défini de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="fb752-107">The impersonation level can be set in a variety of ways.</span></span> <span data-ttu-id="fb752-108">Si le client n’indique pas un niveau d’emprunt d’identité, la valeur par défaut à l’échelle de l’ordinateur est utilisée par COM.</span><span class="sxs-lookup"><span data-stu-id="fb752-108">If the client does not indicate an impersonation level, the machine-wide default will be used by COM.</span></span> <span data-ttu-id="fb752-109">La valeur par défaut à l’ensemble de l’ordinateur peut être définie à l’aide de l’outil d’administration Services de composants ou Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="fb752-109">The machine-wide default can be set using either the Component Services administrative tool or Dcomcnfg.exe.</span></span> <span data-ttu-id="fb752-110">Le client peut également indiquer un niveau d’emprunt d’identité préféré de manière administrative avec Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="fb752-110">The client can also indicate a preferred impersonation level administratively with Dcomcnfg.exe.</span></span>

<span data-ttu-id="fb752-111">Le client peut indiquer le niveau d’emprunt d’identité par programmation, à l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), équivalent à [**IClientSecurity :: SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), qui peut être appelé aussi souvent que nécessaire, ou [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), qui peut être appelé une fois par processus.</span><span class="sxs-lookup"><span data-stu-id="fb752-111">The client can indicate the impersonation level programmatically, using either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)—equivalent to [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), which can be called as often as necessary—or [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), which can be called once per process.</span></span>

<span data-ttu-id="fb752-112">Si le client indique l’emprunt d’identité au niveau du délégué (l’autorité la plus étendue qu’il peut accorder au serveur), le client doit s’exécuter sous une identité correctement configurée dans le service Active Directory pour permettre la délégation de son identité.</span><span class="sxs-lookup"><span data-stu-id="fb752-112">If the client indicates delegate-level impersonation—the broadest authority it can grant to the server—the client should be running under an identity that is properly configured in the Active Directory Service to enable its identity to be delegated.</span></span>

<span data-ttu-id="fb752-113">Pour plus d’informations sur les niveaux d’emprunt d’identité et la configuration requise pour le fonctionnement de la délégation, consultez [délégation et emprunt d’identité](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="fb752-113">For more detail regarding impersonation levels and the requirements for delegation to work, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

<span data-ttu-id="fb752-114">Les applications COM+ peuvent toujours agir comme des clients, bien sûr.</span><span class="sxs-lookup"><span data-stu-id="fb752-114">COM+ applications can always act as clients, of course.</span></span> <span data-ttu-id="fb752-115">Lorsque l’application COM+ fait un appel à une autre application ou ressource, elle exprime un niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="fb752-115">When the COM+ application makes a call to another application or resource, it expresses an impersonation level.</span></span> <span data-ttu-id="fb752-116">Pour les applications serveur COM+, vous pouvez définir un niveau d’emprunt d’identité de manière administrative.</span><span class="sxs-lookup"><span data-stu-id="fb752-116">For COM+ server applications, you can set an impersonation level administratively.</span></span> <span data-ttu-id="fb752-117">Les applications de bibliothèque COM+ ne peuvent pas définir leur propre niveau d’emprunt d’identité ; ils utilisent à la place celui du processus hôte.</span><span class="sxs-lookup"><span data-stu-id="fb752-117">COM+ library applications cannot set their own impersonation level; they use that of the host process instead.</span></span> <span data-ttu-id="fb752-118">Pour savoir comment définir l’emprunt d’identité pour une application COM+, consultez [définition d’un niveau d’emprunt d’identité](setting-an-impersonation-level.md).</span><span class="sxs-lookup"><span data-stu-id="fb752-118">To learn how to set impersonation for a COM+ application, see [Setting an Impersonation Level](setting-an-impersonation-level.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb752-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb752-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb752-120">Emprunt d’identité et délégation du client</span><span class="sxs-lookup"><span data-stu-id="fb752-120">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="fb752-121">Masquer</span><span class="sxs-lookup"><span data-stu-id="fb752-121">Cloaking</span></span>](cloaking.md)
</dt> <dt>

[<span data-ttu-id="fb752-122">Exigences côté serveur pour l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="fb752-122">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
