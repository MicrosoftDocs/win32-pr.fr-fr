---
title: Message CQPM_RELEASE (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête lorsque la page va être déchargée.
ms.assetid: b935ae8d-a07f-4f0d-b379-5512e96a25a5
ms.tgt_platform: multiple
keywords:
- Message de CQPM_RELEASE Active Directory
topic_type:
- apiref
api_name:
- CQPM_RELEASE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4957f02b57f499d80f7802b4fe9bd2639485b8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032802"
---
# <a name="cqpm_release-message"></a><span data-ttu-id="aa9e2-104">Message de publication de CQPM \_</span><span class="sxs-lookup"><span data-stu-id="aa9e2-104">CQPM\_RELEASE message</span></span>

<span data-ttu-id="aa9e2-105">Le message de **\_ libération de CQPM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête lorsque la page est sur le déchargée.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-105">The **CQPM\_RELEASE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is about to be unloaded.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa9e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa9e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa9e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa9e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa9e2-108">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aa9e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa9e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa9e2-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa9e2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa9e2-111">Return value</span></span>

<span data-ttu-id="aa9e2-112">La valeur de retour de ce message est ignorée.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9e2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa9e2-113">Requirements</span></span>



| <span data-ttu-id="aa9e2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa9e2-114">Requirement</span></span> | <span data-ttu-id="aa9e2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa9e2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9e2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa9e2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9e2-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa9e2-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="aa9e2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa9e2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9e2-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa9e2-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="aa9e2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa9e2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa9e2-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9e2-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9e2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa9e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9e2-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="aa9e2-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





