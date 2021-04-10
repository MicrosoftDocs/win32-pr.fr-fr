---
title: Message CQPM_CLEARFORM (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page de requête pour l’extension lorsque le contenu de la page doit être réinitialisé sur les valeurs par défaut.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- Message de CQPM_CLEARFORM Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941747"
---
# <a name="cqpm_clearform-message"></a><span data-ttu-id="63d3c-104">\_Message CQPM CLEARFORM</span><span class="sxs-lookup"><span data-stu-id="63d3c-104">CQPM\_CLEARFORM message</span></span>

<span data-ttu-id="63d3c-105">Le message **CQPM \_ CLEARFORM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page de requête pour l’extension lorsque le contenu de la page doit être réinitialisé sur les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="63d3c-105">The **CQPM\_CLEARFORM** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query for extension page when the contents of the page should be reset to the default values.</span></span>

## <a name="parameters"></a><span data-ttu-id="63d3c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63d3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d3c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63d3c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63d3c-108">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="63d3c-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="63d3c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63d3c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63d3c-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="63d3c-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d3c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63d3c-111">Return value</span></span>

<span data-ttu-id="63d3c-112">Retourne **S \_ OK** en cas de réussite ou un code d’erreur **HRESULT** standard dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="63d3c-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d3c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63d3c-113">Requirements</span></span>



| <span data-ttu-id="63d3c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63d3c-114">Requirement</span></span> | <span data-ttu-id="63d3c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="63d3c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63d3c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63d3c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63d3c-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63d3c-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="63d3c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63d3c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63d3c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63d3c-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="63d3c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="63d3c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63d3c-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="63d3c-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d3c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63d3c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d3c-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="63d3c-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





