---
title: XTYP_POKE transaction (Ddeml. h)
description: Un client utilise la \_ transaction d’XTYPe pour envoyer des données non sollicitées au serveur. Une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit cette transaction lorsqu’un client spécifie XTYP \_ dans la fonction DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Échange de données de transaction XTYP_POKE
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942039"
---
# <a name="xtyp_poke-transaction"></a><span data-ttu-id="e58ed-105">XTYP \_ transaction de journalisation</span><span class="sxs-lookup"><span data-stu-id="e58ed-105">XTYP\_POKE transaction</span></span>

<span data-ttu-id="e58ed-106">Un client utilise la **transaction \_ d’XTYPe** pour envoyer des données non sollicitées au serveur.</span><span class="sxs-lookup"><span data-stu-id="e58ed-106">A client uses the **XTYP\_POKE** transaction to send unsolicited data to the server.</span></span> <span data-ttu-id="e58ed-107">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie **XTYP \_** dans la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="e58ed-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_POKE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="e58ed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e58ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58ed-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="e58ed-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-110">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="e58ed-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="e58ed-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="e58ed-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-112">Format des données envoyées à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="e58ed-112">The format of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="e58ed-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="e58ed-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-114">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="e58ed-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="e58ed-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="e58ed-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-116">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="e58ed-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="e58ed-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="e58ed-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-118">Handle du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="e58ed-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="e58ed-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="e58ed-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-120">Handle vers les données que le client envoie au serveur.</span><span class="sxs-lookup"><span data-stu-id="e58ed-120">A handle to the data that the client is sending to the server.</span></span>

</dd> <dt>

<span data-ttu-id="e58ed-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="e58ed-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="e58ed-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e58ed-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="e58ed-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="e58ed-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="e58ed-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e58ed-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e58ed-125">Return value</span></span>

<span data-ttu-id="e58ed-126">Une fonction de rappel de serveur doit retourner l’indicateur **\_ Fack DDE** si elle traite cette transaction, l’indicateur **DDE \_ FBUSY** s’il est trop occupé pour traiter cette transaction, ou l’indicateur **DDE \_ FNOTPROCESSED** s’il rejette cette transaction.</span><span class="sxs-lookup"><span data-stu-id="e58ed-126">A server callback function should return the **DDE\_FACK** flag if it processes this transaction, the **DDE\_FBUSY** flag if it is too busy to process this transaction, or the **DDE\_FNOTPROCESSED** flag if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="e58ed-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e58ed-127">Remarks</span></span>

<span data-ttu-id="e58ed-128">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur d' **\_ \_ échec** de l’CBF dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="e58ed-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_POKES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58ed-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e58ed-129">Requirements</span></span>



| <span data-ttu-id="e58ed-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e58ed-130">Requirement</span></span> | <span data-ttu-id="e58ed-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e58ed-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58ed-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e58ed-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e58ed-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e58ed-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e58ed-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e58ed-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e58ed-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e58ed-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="e58ed-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="e58ed-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e58ed-137"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e58ed-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e58ed-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e58ed-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="e58ed-139">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e58ed-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e58ed-140">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="e58ed-140">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="e58ed-141">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="e58ed-141">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="e58ed-142">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e58ed-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e58ed-143">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="e58ed-143">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

