---
title: Message CQPM_ENABLE (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour activer ou désactiver la page.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Message de CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032499"
---
# <a name="cqpm_enable-message"></a><span data-ttu-id="5bbb0-104">CQPM \_ activer le message</span><span class="sxs-lookup"><span data-stu-id="5bbb0-104">CQPM\_ENABLE message</span></span>

<span data-ttu-id="5bbb0-105">Le message d' **\_ activation de CQPM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour activer ou désactiver la page.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-105">The **CQPM\_ENABLE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to enable or disable the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="5bbb0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bbb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbb0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5bbb0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbb0-108">Contient zéro pour désactiver la page ou une valeur différente de zéro pour activer la page.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-108">Contains zero to disable the page or nonzero to enable the page.</span></span>

</dd> <dt>

<span data-ttu-id="5bbb0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5bbb0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbb0-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbb0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bbb0-111">Return value</span></span>

<span data-ttu-id="5bbb0-112">La valeur de retour de ce message est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbb0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bbb0-113">Requirements</span></span>



| <span data-ttu-id="5bbb0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bbb0-114">Requirement</span></span> | <span data-ttu-id="5bbb0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bbb0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbb0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bbb0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbb0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bbb0-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="5bbb0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bbb0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbb0-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bbb0-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="5bbb0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bbb0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bbb0-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bbb0-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bbb0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bbb0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbb0-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="5bbb0-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





