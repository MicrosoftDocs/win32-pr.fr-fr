---
title: Configuration requise du serveur DLL
description: Alors que la plupart des dll peuvent s’exécuter dans un substitut, certaines dll ne le peuvent pas.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029864"
---
# <a name="dll-server-requirements"></a><span data-ttu-id="ec256-103">Configuration requise du serveur DLL</span><span class="sxs-lookup"><span data-stu-id="ec256-103">DLL Server Requirements</span></span>

<span data-ttu-id="ec256-104">Alors que la plupart des dll peuvent s’exécuter dans un substitut, certaines dll ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="ec256-104">While most DLLs can run in a surrogate, some DLLs cannot.</span></span>

<span data-ttu-id="ec256-105">La DLL doit être correctement comportée si vous souhaitez utiliser le substitut fourni par le système.</span><span class="sxs-lookup"><span data-stu-id="ec256-105">The DLL must be well-behaved if you want to use the system-supplied surrogate.</span></span> <span data-ttu-id="ec256-106">Par exemple, une DLL qui appelle des méthodes qui inscrivent des rappels à partir du client essaiera d’appeler ces rappels comme si les pointeurs de fonction reçus étaient pour des instructions dans son espace d’adressage, ce qui n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="ec256-106">For example, a DLL that calls methods that register callbacks from the client would try to invoke those callbacks as if the function pointers it received were for instructions in its address space, which is not the case.</span></span> <span data-ttu-id="ec256-107">De même, une DLL qui utilise une variable globale qui s’attend à ce que le client accède ne fonctionnerait pas.</span><span class="sxs-lookup"><span data-stu-id="ec256-107">Similarly, a DLL that uses a global variable that it expects the client to access would not work.</span></span> <span data-ttu-id="ec256-108">En général, les paramètres qui ne peuvent pas être correctement marshalés empêcheront le serveur DLL de s’exécuter en dehors du processus client.</span><span class="sxs-lookup"><span data-stu-id="ec256-108">In general, parameters that cannot be properly marshaled will prevent the DLL server from running outside the client process.</span></span> <span data-ttu-id="ec256-109">Dans de nombreux cas, vous pouvez écrire un substitut personnalisé spécifiquement conçu pour compenser le comportement « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="ec256-109">In many cases, you can write a custom surrogate specifically designed to compensate for "bad" behavior.</span></span> <span data-ttu-id="ec256-110">(Pour plus d’informations, consultez [écriture d’un substitut personnalisé](writing-a-custom-surrogate.md).)</span><span class="sxs-lookup"><span data-stu-id="ec256-110">(For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).)</span></span>

<span data-ttu-id="ec256-111">Si le serveur de DLL utilise des interfaces personnalisées, vous devez vous assurer que le code de marshaling est disponible pour ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="ec256-111">If the DLL server uses custom interfaces, you would have to ensure that marshaling code is available for those interfaces.</span></span> <span data-ttu-id="ec256-112">Par exemple, vous pouvez générer et inscrire une DLL proxy ou fournir et inscrire une bibliothèque de types qui permettrait au serveur de fonctionner correctement lors de son exécution dans un substitut.</span><span class="sxs-lookup"><span data-stu-id="ec256-112">For example, you could build and register a proxy DLL or provide and register a type library that would allow the server to function correctly while running in a surrogate.</span></span>

<span data-ttu-id="ec256-113">Les serveurs DLL sont chargés uniquement dans un processus de substitution s’exécutant dans le contexte de sécurité approprié.</span><span class="sxs-lookup"><span data-stu-id="ec256-113">DLL servers will be loaded only into a surrogate process running in the proper security context.</span></span> <span data-ttu-id="ec256-114">Le contexte de sécurité pour le substitut du serveur DLL est déterminé de la même façon que pour les serveurs EXE.</span><span class="sxs-lookup"><span data-stu-id="ec256-114">The security context for the DLL server surrogate is determined in the same way as for EXE servers.</span></span> <span data-ttu-id="ec256-115">Le substitut de serveur DLL s’exécute dans le même contexte de sécurité que le client, à moins qu’une valeur **runas** , qui détermine le contexte de sécurité, soit définie dans la section [AppID](appid-clsid.md) Registry du serveur.</span><span class="sxs-lookup"><span data-stu-id="ec256-115">The DLL server surrogate runs in the same security context as the client, unless a **RunAs** value, which determines the security context, is set in the [AppID](appid-clsid.md) registry section for the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec256-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec256-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec256-117">Substituts de DLL</span><span class="sxs-lookup"><span data-stu-id="ec256-117">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




