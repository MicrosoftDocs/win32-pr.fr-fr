---
title: Interface IConnectionBrokerRequest (Cbclient. h)
description: Fournit les méthodes nécessaires pour obtenir les résultats de la méthode asynchrone IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IConnectionBrokerRequest
- Services Bureau à distance de l’interface IConnectionBrokerRequest, Description
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743661"
---
# <a name="iconnectionbrokerrequest-interface"></a><span data-ttu-id="ad9c1-105">Interface IConnectionBrokerRequest</span><span class="sxs-lookup"><span data-stu-id="ad9c1-105">IConnectionBrokerRequest interface</span></span>

<span data-ttu-id="ad9c1-106">Fournit les méthodes nécessaires pour obtenir les résultats de la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ad9c1-106">Provides the methods needed to obtain the results of the asynchronous [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

<span data-ttu-id="ad9c1-107">Cette interface est implémentée par le système.</span><span class="sxs-lookup"><span data-stu-id="ad9c1-107">This interface is implemented by the system.</span></span> <span data-ttu-id="ad9c1-108">Une instance de cette interface est fournie à l’appelant à l’aide de la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ad9c1-108">An instance of this interface is provided to the caller with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="ad9c1-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ad9c1-109">Members</span></span>

<span data-ttu-id="ad9c1-110">L’interface **IConnectionBrokerRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ad9c1-110">The **IConnectionBrokerRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ad9c1-111">**IConnectionBrokerRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ad9c1-111">**IConnectionBrokerRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="ad9c1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ad9c1-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad9c1-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ad9c1-113">Methods</span></span>

<span data-ttu-id="ad9c1-114">L’interface **IConnectionBrokerRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ad9c1-114">The **IConnectionBrokerRequest** interface has these methods.</span></span>



| <span data-ttu-id="ad9c1-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="ad9c1-115">Method</span></span>                                                      | <span data-ttu-id="ad9c1-116">Description</span><span class="sxs-lookup"><span data-stu-id="ad9c1-116">Description</span></span>                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="ad9c1-117">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="ad9c1-117">**CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md) | <span data-ttu-id="ad9c1-118">Appelé pour déterminer l’état d’une requête asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ad9c1-118">Called to determine the status of an asynchronous request.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad9c1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad9c1-119">Requirements</span></span>



| <span data-ttu-id="ad9c1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad9c1-120">Requirement</span></span> | <span data-ttu-id="ad9c1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad9c1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9c1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad9c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ad9c1-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ad9c1-123">Windows 8</span></span><br/>                                                                        |
| <span data-ttu-id="ad9c1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad9c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ad9c1-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad9c1-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ad9c1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad9c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad9c1-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c1-127"><dt>Cbclient.h</dt></span></span> </dl>       |
| <span data-ttu-id="ad9c1-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad9c1-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad9c1-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c1-129"><dt>Cbclient.lib</dt></span></span> </dl>     |
| <span data-ttu-id="ad9c1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ad9c1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad9c1-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c1-131"><dt>Cbclient.dll</dt></span></span> </dl>     |
| <span data-ttu-id="ad9c1-132">IID</span><span class="sxs-lookup"><span data-stu-id="ad9c1-132">IID</span></span><br/>                      | <span data-ttu-id="ad9c1-133">IID \_ IConnectionBrokerRequest est défini comme 25114427-ED5D-46a6-AF53-C62D33A4108E</span><span class="sxs-lookup"><span data-stu-id="ad9c1-133">IID\_IConnectionBrokerRequest is defined as 25114427-ED5D-46A6-AF53-C62D33A4108E</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad9c1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad9c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9c1-135">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="ad9c1-135">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

