---
title: Message CQPM_INITIALIZE (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête lorsque la page est ajoutée à un formulaire.
ms.assetid: 29cb39d5-9bc4-472e-8a2f-dc6cd505144a
ms.tgt_platform: multiple
keywords:
- Message de CQPM_INITIALIZE Active Directory
topic_type:
- apiref
api_name:
- CQPM_INITIALIZE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e95c7087a9cd2d40387c8d7dd07aa93c8f697fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032804"
---
# <a name="cqpm_initialize-message"></a><span data-ttu-id="53629-104">CQPM \_ initialiser le message</span><span class="sxs-lookup"><span data-stu-id="53629-104">CQPM\_INITIALIZE message</span></span>

<span data-ttu-id="53629-105">Le **message \_ d’initialisation de CQPM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête lorsque la page est ajoutée à un formulaire.</span><span class="sxs-lookup"><span data-stu-id="53629-105">The **CQPM\_INITIALIZE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is added to a form.</span></span>

## <a name="parameters"></a><span data-ttu-id="53629-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53629-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53629-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53629-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53629-108">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="53629-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="53629-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53629-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53629-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="53629-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53629-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53629-111">Return value</span></span>

<span data-ttu-id="53629-112">La valeur de retour de ce message est ignorée.</span><span class="sxs-lookup"><span data-stu-id="53629-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="53629-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53629-113">Requirements</span></span>



| <span data-ttu-id="53629-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53629-114">Requirement</span></span> | <span data-ttu-id="53629-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="53629-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53629-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53629-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53629-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53629-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="53629-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53629-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53629-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53629-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="53629-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="53629-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53629-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="53629-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53629-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53629-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53629-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="53629-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





