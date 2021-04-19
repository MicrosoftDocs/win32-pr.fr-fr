---
title: XTYP_ERROR transaction (Ddeml. h)
description: Une fonction de rappel échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction d’erreur XTYP lorsqu’une erreur critique se produit.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Échange de données de transaction XTYP_ERROR
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106530805"
---
# <a name="xtyp_error-transaction"></a><span data-ttu-id="695a8-104">\_Transaction d’erreur XTYP</span><span class="sxs-lookup"><span data-stu-id="695a8-104">XTYP\_ERROR transaction</span></span>

<span data-ttu-id="695a8-105">Une fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction d' **\_ erreur XTYP** lorsqu’une erreur critique se produit.</span><span class="sxs-lookup"><span data-stu-id="695a8-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_ERROR** transaction when a critical error occurs.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="695a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="695a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695a8-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="695a8-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-108">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="695a8-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="695a8-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="695a8-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="695a8-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-112">Handle de la conversation associée à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="695a8-112">A handle to the conversation associated with the error.</span></span> <span data-ttu-id="695a8-113">Ce paramètre a la **valeur null** si l’erreur n’est pas associée à une conversation.</span><span class="sxs-lookup"><span data-stu-id="695a8-113">This parameter is **NULL** if the error is not associated with a conversation.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="695a8-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-115">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="695a8-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="695a8-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="695a8-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="695a8-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-119">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="695a8-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="695a8-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-121">Code d’erreur dans le mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="695a8-121">The error code in the low-order word.</span></span> <span data-ttu-id="695a8-122">Actuellement, seul le code d’erreur suivant est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="695a8-122">Currently, only the following error code is supported.</span></span>



| <span data-ttu-id="695a8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="695a8-123">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="695a8-124">Signification</span><span class="sxs-lookup"><span data-stu-id="695a8-124">Meaning</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <span data-ttu-id="695a8-125"><dt>**\_mémoire insuffisante DMLERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="695a8-125"><dt>**DMLERR\_LOW\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="695a8-126">La mémoire est insuffisante ; les données de notification, d’endiguement ou d’exécution peuvent être perdues ou le système peut échouer.</span><span class="sxs-lookup"><span data-stu-id="695a8-126">Memory is low; advise, poke, or execute data may be lost, or the system may fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="695a8-127">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="695a8-127">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="695a8-128">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="695a8-128">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="695a8-129">Notes</span><span class="sxs-lookup"><span data-stu-id="695a8-129">Remarks</span></span>

<span data-ttu-id="695a8-130">Une application ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="695a8-130">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span> <span data-ttu-id="695a8-131">La DDEML (échange dynamique de données Management Library) tente de libérer de la mémoire en supprimant les ressources non critiques.</span><span class="sxs-lookup"><span data-stu-id="695a8-131">The Dynamic Data Exchange Management Library (DDEML) attempts to free memory by removing noncritical resources.</span></span> <span data-ttu-id="695a8-132">Une application qui a bloqué les conversations doit les débloquer.</span><span class="sxs-lookup"><span data-stu-id="695a8-132">An application that has blocked conversations should unblock them.</span></span>

## <a name="requirements"></a><span data-ttu-id="695a8-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="695a8-133">Requirements</span></span>



| <span data-ttu-id="695a8-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="695a8-134">Requirement</span></span> | <span data-ttu-id="695a8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="695a8-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="695a8-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="695a8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="695a8-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="695a8-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="695a8-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="695a8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="695a8-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="695a8-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="695a8-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="695a8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="695a8-141"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="695a8-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="695a8-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="695a8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="695a8-143">Vue d’ensemble de la bibliothèque de gestion échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="695a8-143">Dynamic Data Exchange Management Library Overview</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

