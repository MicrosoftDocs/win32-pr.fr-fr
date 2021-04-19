---
description: Contient la méthode utilisée pour obtenir un point de terminaison utilisé pour se connecter à un service.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interface IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514639"
---
# <a name="iupdateendpointprovider-interface"></a><span data-ttu-id="ac1d2-103">Interface IUpdateEndpointProvider</span><span class="sxs-lookup"><span data-stu-id="ac1d2-103">IUpdateEndpointProvider interface</span></span>

<span data-ttu-id="ac1d2-104">Contient la méthode utilisée pour obtenir un point de terminaison utilisé pour se connecter à un service.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-104">Contains the method used to get an endpoint that is used to connect to a service.</span></span> <span data-ttu-id="ac1d2-105">Cette interface est implémentée lors de l’écriture d’un fournisseur de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-105">This interface is implemented when writing an endpoint provider.</span></span>

## <a name="members"></a><span data-ttu-id="ac1d2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ac1d2-106">Members</span></span>

<span data-ttu-id="ac1d2-107">L’interface **IUpdateEndpointProvider** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ac1d2-107">The **IUpdateEndpointProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ac1d2-108">**IUpdateEndpointProvider** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ac1d2-108">**IUpdateEndpointProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="ac1d2-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ac1d2-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ac1d2-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ac1d2-110">Methods</span></span>

<span data-ttu-id="ac1d2-111">L’interface **IUpdateEndpointProvider** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-111">The **IUpdateEndpointProvider** interface has these methods.</span></span>



| <span data-ttu-id="ac1d2-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="ac1d2-112">Method</span></span>                                                                       | <span data-ttu-id="ac1d2-113">Description</span><span class="sxs-lookup"><span data-stu-id="ac1d2-113">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="ac1d2-114">**GetServiceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="ac1d2-114">**GetServiceEndpoint**</span></span>](iupdateendpointauthprovider-getserviceendpoint.md) | <span data-ttu-id="ac1d2-115">Demande un point de terminaison utilisé pour se connecter à un service.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-115">Requests an endpoint that is used to connect to a service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac1d2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ac1d2-116">Remarks</span></span>

<span data-ttu-id="ac1d2-117">WUA appelle la méthode [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) pour démarrer le processus de négociation.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-117">WUA calls the [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) method to start the negotiation process.</span></span> <span data-ttu-id="ac1d2-118">Lorsque l’appel est effectué, WUA passe les types de jetons inscrits et l’implémentation de cette interface retourne les types de jetons qu’il préfère utiliser.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-118">When the call is made, WUA passes in the registered token types, and the implementation of this interface returns the token types that it prefers to use.</span></span>

 

 
