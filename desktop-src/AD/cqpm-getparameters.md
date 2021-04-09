---
title: Message CQPM_GETPARAMETERS (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour récupérer des données sur la requête exécutée par la page.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- Message de CQPM_GETPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843213"
---
# <a name="cqpm_getparameters-message"></a><span data-ttu-id="6c07a-104">\_Message CQPM GETPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c07a-104">CQPM\_GETPARAMETERS message</span></span>

<span data-ttu-id="6c07a-105">Le **message \_ GETPARAMETERS CQPM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour récupérer des données sur la requête exécutée par la page.</span><span class="sxs-lookup"><span data-stu-id="6c07a-105">The **CQPM\_GETPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to retrieve data about the query performed by the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c07a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c07a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c07a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c07a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c07a-108">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6c07a-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6c07a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c07a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c07a-110">Pointeur vers une valeur [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) qui reçoit des données sur la requête exécutée par la page.</span><span class="sxs-lookup"><span data-stu-id="6c07a-110">Pointer to a [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) value that receives data about the query performed by the page.</span></span> <span data-ttu-id="6c07a-111">Si ce paramètre a la **valeur null**, la structure **DSQUERYPARAMS** doit être allouée par l’extension à l’aide de la fonction [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .</span><span class="sxs-lookup"><span data-stu-id="6c07a-111">If this parameter is **NULL**, the **DSQUERYPARAMS** structure must be allocated by the extension using the [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c07a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c07a-112">Return value</span></span>

<span data-ttu-id="6c07a-113">Retourne **S \_ OK** en cas de réussite ou un code d’erreur **HRESULT** standard dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6c07a-113">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c07a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c07a-114">Requirements</span></span>



| <span data-ttu-id="6c07a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c07a-115">Requirement</span></span> | <span data-ttu-id="6c07a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c07a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c07a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c07a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6c07a-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c07a-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="6c07a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c07a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6c07a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c07a-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="6c07a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c07a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c07a-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c07a-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c07a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c07a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c07a-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="6c07a-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="6c07a-125">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="6c07a-125">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[<span data-ttu-id="6c07a-126">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="6c07a-126">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

