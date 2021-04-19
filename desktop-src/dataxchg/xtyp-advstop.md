---
title: XTYP_ADVSTOP transaction (Ddeml. h)
description: Un client utilise la \_ transaction XTYP ADVSTOP pour mettre fin à une boucle de notification avec un serveur. Une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit cette transaction lorsqu’un client spécifie XTYP \_ ADVSTOP dans la fonction DdeClientTransaction.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- Échange de données de transaction XTYP_ADVSTOP
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513788"
---
# <a name="xtyp_advstop-transaction"></a><span data-ttu-id="24edc-105">\_Transaction ADVSTOP XTYP</span><span class="sxs-lookup"><span data-stu-id="24edc-105">XTYP\_ADVSTOP transaction</span></span>

<span data-ttu-id="24edc-106">Un client utilise la transaction **XTYP \_ ADVSTOP** pour mettre fin à une boucle de notification avec un serveur.</span><span class="sxs-lookup"><span data-stu-id="24edc-106">A client uses the **XTYP\_ADVSTOP** transaction to end an advise loop with a server.</span></span> <span data-ttu-id="24edc-107">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie **XTYP \_ ADVSTOP** dans la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="24edc-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTOP** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a><span data-ttu-id="24edc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24edc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24edc-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="24edc-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-110">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="24edc-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="24edc-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="24edc-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-112">Le format de données associé à la boucle de notification est terminé.</span><span class="sxs-lookup"><span data-stu-id="24edc-112">The data format associated with the advise loop being ended.</span></span>

</dd> <dt>

<span data-ttu-id="24edc-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="24edc-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-114">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="24edc-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="24edc-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="24edc-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-116">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="24edc-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="24edc-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="24edc-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-118">Handle du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="24edc-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="24edc-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="24edc-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24edc-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="24edc-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="24edc-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24edc-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="24edc-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="24edc-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="24edc-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24edc-124">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24edc-125">Notes</span><span class="sxs-lookup"><span data-stu-id="24edc-125">Remarks</span></span>

<span data-ttu-id="24edc-126">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur de **\_ \_ notifications d’échec CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="24edc-126">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="24edc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24edc-127">Requirements</span></span>



| <span data-ttu-id="24edc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24edc-128">Requirement</span></span> | <span data-ttu-id="24edc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="24edc-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24edc-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24edc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="24edc-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24edc-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="24edc-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24edc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="24edc-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24edc-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="24edc-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="24edc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="24edc-135"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24edc-135"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24edc-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24edc-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="24edc-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="24edc-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24edc-138">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="24edc-138">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="24edc-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="24edc-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="24edc-140">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="24edc-140">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="24edc-141">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="24edc-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24edc-142">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="24edc-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

