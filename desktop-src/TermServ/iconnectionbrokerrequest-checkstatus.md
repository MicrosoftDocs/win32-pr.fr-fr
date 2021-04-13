---
title: Méthode IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Appelé pour déterminer l’état d’une requête asynchrone.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CheckStatus
- Méthode CheckStatus Services Bureau à distance, interface IConnectionBrokerRequest
- Services Bureau à distance de l’interface IConnectionBrokerRequest, méthode CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385179"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a><span data-ttu-id="bee21-106">IConnectionBrokerRequest :: CheckStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="bee21-106">IConnectionBrokerRequest::CheckStatus method</span></span>

<span data-ttu-id="bee21-107">Appelé pour déterminer l’état d’une requête asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bee21-107">Called to determine the status of an asynchronous request.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee21-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bee21-108">Syntax</span></span>


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a><span data-ttu-id="bee21-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bee21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bee21-110">*pReqStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bee21-110">*pReqStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bee21-111">Adresse d’une variable qui reçoit une valeur de l’énumération de l' [**\_ \_ État de la demande CB**](cb-request-status.md) qui indique l’état de la demande.</span><span class="sxs-lookup"><span data-stu-id="bee21-111">The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bee21-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bee21-112">Return value</span></span>

<span data-ttu-id="bee21-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bee21-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bee21-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bee21-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bee21-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bee21-115">Requirements</span></span>



| <span data-ttu-id="bee21-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bee21-116">Requirement</span></span> | <span data-ttu-id="bee21-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee21-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bee21-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bee21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bee21-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bee21-119">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="bee21-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bee21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bee21-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bee21-121">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="bee21-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bee21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bee21-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bee21-123"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bee21-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bee21-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="bee21-125"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bee21-125"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="bee21-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bee21-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee21-127"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee21-127"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bee21-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bee21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee21-129">**IConnectionBrokerRequest**</span><span class="sxs-lookup"><span data-stu-id="bee21-129">**IConnectionBrokerRequest**</span></span>](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





