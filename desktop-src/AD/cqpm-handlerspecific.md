---
title: Message CQPM_HANDLERSPECIFIC (cmnquery. h)
description: Valeur de base utilisée pour les messages qui sont privés pour le gestionnaire de requêtes.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Message de CQPM_HANDLERSPECIFIC Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464554"
---
# <a name="cqpm_handlerspecific-message"></a><span data-ttu-id="b71a8-104">\_Message CQPM HANDLERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="b71a8-104">CQPM\_HANDLERSPECIFIC message</span></span>

<span data-ttu-id="b71a8-105">Le message **CQPM \_ HANDLERSPECIFIC** est la valeur de base utilisée pour les messages qui sont privés pour le gestionnaire de requêtes.</span><span class="sxs-lookup"><span data-stu-id="b71a8-105">The **CQPM\_HANDLERSPECIFIC** message is the base value used for messages that are private to the query handler.</span></span> <span data-ttu-id="b71a8-106">Le gestionnaire de requêtes doit ajouter cette valeur aux messages privés pour s’assurer que les collisions de message ne se produisent pas.</span><span class="sxs-lookup"><span data-stu-id="b71a8-106">The query handler should add this value to private messages to ensure that message collisions do not occur.</span></span>

## <a name="parameters"></a><span data-ttu-id="b71a8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b71a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b71a8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b71a8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b71a8-109">Contient des données de message supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b71a8-109">Contains additional message data.</span></span> <span data-ttu-id="b71a8-110">Le contenu de ce paramètre est défini par le gestionnaire de requêtes.</span><span class="sxs-lookup"><span data-stu-id="b71a8-110">The content of this parameter is defined by the query handler.</span></span>

</dd> <dt>

<span data-ttu-id="b71a8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b71a8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b71a8-112">Contient des données de message supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b71a8-112">Contains additional message data.</span></span> <span data-ttu-id="b71a8-113">Le contenu de ce paramètre est défini par le gestionnaire de requêtes.</span><span class="sxs-lookup"><span data-stu-id="b71a8-113">The content of this parameter is defined by the query handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b71a8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b71a8-114">Return value</span></span>

<span data-ttu-id="b71a8-115">La signification de la valeur de retour est définie par le gestionnaire de requêtes.</span><span class="sxs-lookup"><span data-stu-id="b71a8-115">The meaning of the return value is defined by the query handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="b71a8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b71a8-116">Requirements</span></span>



| <span data-ttu-id="b71a8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b71a8-117">Requirement</span></span> | <span data-ttu-id="b71a8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b71a8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b71a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b71a8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b71a8-120">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="b71a8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b71a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b71a8-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b71a8-122">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="b71a8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b71a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b71a8-124"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="b71a8-124"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b71a8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b71a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b71a8-126">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="b71a8-126">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





