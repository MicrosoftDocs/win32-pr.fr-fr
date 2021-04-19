---
description: Effectue le suivi des demandes enfants générées à partir d’une demande parente.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interface IWbemCausalityAccess (Wbemint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518811"
---
# <a name="iwbemcausalityaccess-interface"></a><span data-ttu-id="0c7c2-103">Interface IWbemCausalityAccess</span><span class="sxs-lookup"><span data-stu-id="0c7c2-103">IWbemCausalityAccess interface</span></span>

<span data-ttu-id="0c7c2-104">L’interface **IWbemCausalityAccess** effectue le suivi des demandes enfants générées à partir d’une demande parente.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-104">The **IWbemCausalityAccess** interface keeps track of child requests that are generated from a parent request.</span></span> <span data-ttu-id="0c7c2-105">Vous pouvez obtenir un objet **IWbemCausalityAccess** à l’aide d’une interface de requête (QI) pour [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span><span class="sxs-lookup"><span data-stu-id="0c7c2-105">You can obtain an **IWbemCausalityAccess** object by using a query interface (QI) for [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span></span> <span data-ttu-id="0c7c2-106">Chaque requête est identifiée par un identificateur global unique (GUID) et peut avoir une requête parente ou peut être une requête principale.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="0c7c2-107">Un GUID est un nombre 128 bits unique.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-107">A GUID is a unique 128-bit number.</span></span> <span data-ttu-id="0c7c2-108">Par exemple, 5b2fc63a-8AF4-44cb-960C-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-108">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

## <a name="members"></a><span data-ttu-id="0c7c2-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0c7c2-109">Members</span></span>

<span data-ttu-id="0c7c2-110">L’interface **IWbemCausalityAccess** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0c7c2-110">The **IWbemCausalityAccess** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0c7c2-111">**IWbemCausalityAccess** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0c7c2-111">**IWbemCausalityAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="0c7c2-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c7c2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0c7c2-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c7c2-113">Methods</span></span>

<span data-ttu-id="0c7c2-114">L’interface **IWbemCausalityAccess** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-114">The **IWbemCausalityAccess** interface has these methods.</span></span>



| <span data-ttu-id="0c7c2-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="0c7c2-115">Method</span></span>                                                    | <span data-ttu-id="0c7c2-116">Description</span><span class="sxs-lookup"><span data-stu-id="0c7c2-116">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c7c2-117">**GetRequestId**</span><span class="sxs-lookup"><span data-stu-id="0c7c2-117">**GetRequestId**</span></span>](iwbemcausalityaccess-getrequestid.md) | <span data-ttu-id="0c7c2-118">Retourne un identificateur GUID unique pour une demande.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-118">Returns a unique GUID identifier for a request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0c7c2-119">**IsChildOf**</span><span class="sxs-lookup"><span data-stu-id="0c7c2-119">**IsChildOf**</span></span>](iwbemcausalityaccess-ischildof.md)       | <span data-ttu-id="0c7c2-120">Détermine si une demande est un enfant d’une requête parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-120">Determines if a request is a child of a specified parent request.</span></span> <span data-ttu-id="0c7c2-121">Une requête parent peut avoir plusieurs requêtes enfants, chacune identifiée par une valeur GUID unique.</span><span class="sxs-lookup"><span data-stu-id="0c7c2-121">A parent request can have multiple child requests, each identified by a unique GUID value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0c7c2-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c7c2-122">Requirements</span></span>



| <span data-ttu-id="0c7c2-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c7c2-123">Requirement</span></span> | <span data-ttu-id="0c7c2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c7c2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c7c2-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c7c2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0c7c2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c7c2-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c7c2-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c7c2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0c7c2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c7c2-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c7c2-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c7c2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c7c2-130"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c7c2-130"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="0c7c2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0c7c2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c7c2-132"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c7c2-132"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c7c2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c7c2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7c2-134">API COM pour WMI</span><span class="sxs-lookup"><span data-stu-id="0c7c2-134">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

