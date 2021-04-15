---
title: Message CQPM_SETDEFAULTPARAMETERS (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour définir d’autres paramètres par défaut pour la page.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- Message de CQPM_SETDEFAULTPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465158"
---
# <a name="cqpm_setdefaultparameters-message"></a><span data-ttu-id="eec68-104">\_Message CQPM SETDEFAULTPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eec68-104">CQPM\_SETDEFAULTPARAMETERS message</span></span>

<span data-ttu-id="eec68-105">Le message **CQPM \_ SETDEFAULTPARAMETERS** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour définir d’autres paramètres par défaut pour la page.</span><span class="sxs-lookup"><span data-stu-id="eec68-105">The **CQPM\_SETDEFAULTPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to set alternate default parameters for the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="eec68-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eec68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec68-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eec68-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eec68-108">Contient une valeur différente de zéro si la page est la page par défaut ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="eec68-108">Contains nonzero if the page is the default page or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="eec68-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eec68-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eec68-110">Pointeur vers une structure [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) qui contient des données sur la boîte de dialogue requête de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="eec68-110">Pointer to an [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) structure that contains data about the directory service query dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec68-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eec68-111">Return value</span></span>

<span data-ttu-id="eec68-112">La valeur de retour de ce message est ignorée.</span><span class="sxs-lookup"><span data-stu-id="eec68-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec68-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eec68-113">Requirements</span></span>



| <span data-ttu-id="eec68-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eec68-114">Requirement</span></span> | <span data-ttu-id="eec68-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="eec68-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eec68-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eec68-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eec68-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eec68-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="eec68-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eec68-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eec68-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eec68-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="eec68-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="eec68-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec68-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec68-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec68-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eec68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec68-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="eec68-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="eec68-124">**OPENQUERYWINDOW**</span><span class="sxs-lookup"><span data-stu-id="eec68-124">**OPENQUERYWINDOW**</span></span>](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





