---
title: Délégation de QueryInterface
description: Délégation de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102400"
---
# <a name="delegation-of-queryinterface"></a><span data-ttu-id="12dc4-103">Délégation de QueryInterface</span><span class="sxs-lookup"><span data-stu-id="12dc4-103">Delegation of QueryInterface</span></span>

<span data-ttu-id="12dc4-104">Les gestionnaires qui requièrent l’accès à certaines des interfaces internes du gestionnaire proxy doivent parcourir l’interface [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) .</span><span class="sxs-lookup"><span data-stu-id="12dc4-104">Handlers that require access to some of the internal interfaces on the proxy manager have to go through the [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) interface.</span></span> <span data-ttu-id="12dc4-105">Cela empêche les gestionnaires de déléguer et d’exposer aveuglément les interfaces internes de l’agrégat en dehors de l’agrégat.</span><span class="sxs-lookup"><span data-stu-id="12dc4-105">This prevents handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate.</span></span> <span data-ttu-id="12dc4-106">Ces interfaces incluent [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) et [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span><span class="sxs-lookup"><span data-stu-id="12dc4-106">These interfaces include [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span></span> <span data-ttu-id="12dc4-107">Si le gestionnaire souhaite exposer **IClientSecurity** ou **IMultiQI**, il doit les implémenter lui-même.</span><span class="sxs-lookup"><span data-stu-id="12dc4-107">If the handler wants to expose **IClientSecurity** or **IMultiQI**, it should implement them itself.</span></span>

<span data-ttu-id="12dc4-108">Dans le cas de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), si le client tente de définir la sécurité sur une interface exposée par le gestionnaire, le gestionnaire doit définir la sécurité sur le proxy d’interface réseau sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="12dc4-108">In the case of [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.</span></span>

<span data-ttu-id="12dc4-109">Dans le cas de [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), le gestionnaire doit remplir les interfaces qu’il connaît, puis transférer l’appel au gestionnaire de proxy pour que le reste des interfaces soit rempli.</span><span class="sxs-lookup"><span data-stu-id="12dc4-109">In the case of [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to get the rest of the interfaces filled in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12dc4-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12dc4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12dc4-111">Gestionnaire de Client-Side léger</span><span class="sxs-lookup"><span data-stu-id="12dc4-111">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 