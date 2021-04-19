---
title: XTYP_XACT_COMPLETE transaction (Ddeml. h)
description: Une fonction de rappel client échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction XTYP XACT \_ Complete lorsqu’une transaction asynchrone, initiée par un appel à la fonction DdeClientTransaction, est terminée.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Échange de données de transaction XTYP_XACT_COMPLETE
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512558"
---
# <a name="xtyp_xact_complete-transaction"></a><span data-ttu-id="80e2a-104">\_Transaction XTYP XACT \_ complète</span><span class="sxs-lookup"><span data-stu-id="80e2a-104">XTYP\_XACT\_COMPLETE transaction</span></span>

<span data-ttu-id="80e2a-105">Une fonction de rappel client échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction **XTYP \_ XACT \_ Complete** lorsqu’une transaction asynchrone, initiée par un appel à la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , est terminée.</span><span class="sxs-lookup"><span data-stu-id="80e2a-105">A Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_XACT\_COMPLETE** transaction when an asynchronous transaction, initiated by a call to the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function, has completed.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a><span data-ttu-id="80e2a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e2a-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="80e2a-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-108">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="80e2a-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="80e2a-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="80e2a-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-110">Format des données associées à la transaction terminée (le cas échéant) ou **null** si aucune donnée n’a été échangée pendant la transaction.</span><span class="sxs-lookup"><span data-stu-id="80e2a-110">The format of the data associated with the completed transaction (if applicable) or **NULL** if no data was exchanged during the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="80e2a-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="80e2a-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-112">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="80e2a-112">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="80e2a-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="80e2a-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-114">Handle vers le nom de la rubrique impliquée dans la transaction terminée.</span><span class="sxs-lookup"><span data-stu-id="80e2a-114">A handle to the topic name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="80e2a-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="80e2a-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-116">Handle du nom d’élément impliqué dans la transaction terminée.</span><span class="sxs-lookup"><span data-stu-id="80e2a-116">A handle to the item name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="80e2a-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="80e2a-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-118">Handle vers les données impliquées dans la transaction terminée, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="80e2a-118">A handle to the data involved in the completed transaction, if applicable.</span></span> <span data-ttu-id="80e2a-119">Si la transaction a réussi, mais n’a impliqué aucune donnée, ce paramètre a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="80e2a-119">If the transaction was successful but involved no data, this parameter is **TRUE**.</span></span> <span data-ttu-id="80e2a-120">Ce paramètre a la **valeur null** si la transaction a échoué.</span><span class="sxs-lookup"><span data-stu-id="80e2a-120">This parameter is **NULL** if the transaction was unsuccessful.</span></span>

</dd> <dt>

<span data-ttu-id="80e2a-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="80e2a-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-122">Identificateur de la transaction terminée.</span><span class="sxs-lookup"><span data-stu-id="80e2a-122">The transaction identifier of the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="80e2a-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="80e2a-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="80e2a-124">Tous les indicateurs d’état **DDE \_** applicables dans le mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="80e2a-124">Any applicable **DDE\_** status flags in the low word.</span></span> <span data-ttu-id="80e2a-125">Ce paramètre fournit la prise en charge des applications dépendantes des bits **\_ APPSTATUS DDE** .</span><span class="sxs-lookup"><span data-stu-id="80e2a-125">This parameter provides support for applications dependent on **DDE\_APPSTATUS** bits.</span></span> <span data-ttu-id="80e2a-126">Il est recommandé que les applications n’utilisent plus ces bits. elles ne seront peut-être pas prises en charge dans les futures versions du DDEML.</span><span class="sxs-lookup"><span data-stu-id="80e2a-126">It is recommended that applications no longer use these bits   they may not be supported in future versions of the DDEML.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80e2a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="80e2a-127">Remarks</span></span>

<span data-ttu-id="80e2a-128">Une application ne doit pas libérer le descripteur de données obtenu pendant cette transaction.</span><span class="sxs-lookup"><span data-stu-id="80e2a-128">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="80e2a-129">Toutefois, une application doit copier les données associées au descripteur de données si l’application doit traiter les données après le retour de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="80e2a-129">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="80e2a-130">Une application peut utiliser la fonction [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) pour copier les données.</span><span class="sxs-lookup"><span data-stu-id="80e2a-130">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e2a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80e2a-131">Requirements</span></span>



| <span data-ttu-id="80e2a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80e2a-132">Requirement</span></span> | <span data-ttu-id="80e2a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="80e2a-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e2a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80e2a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="80e2a-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80e2a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="80e2a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80e2a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="80e2a-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80e2a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="80e2a-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="80e2a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="80e2a-139"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80e2a-139"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e2a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80e2a-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="80e2a-141">**Référence**</span><span class="sxs-lookup"><span data-stu-id="80e2a-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="80e2a-142">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="80e2a-142">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="80e2a-143">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="80e2a-143">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

<span data-ttu-id="80e2a-144">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="80e2a-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="80e2a-145">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="80e2a-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

