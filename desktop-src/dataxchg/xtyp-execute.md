---
title: XTYP_EXECUTE transaction (Ddeml. h)
description: Un client utilise la \_ transaction d’exécution XTYP pour envoyer une chaîne de commande au serveur. Une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit cette transaction lorsqu’un client spécifie XTYP \_ Execute dans la fonction DdeClientTransaction.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- Échange de données de transaction XTYP_EXECUTE
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033115"
---
# <a name="xtyp_execute-transaction"></a><span data-ttu-id="5601c-105">XTYP \_ exécuter la transaction</span><span class="sxs-lookup"><span data-stu-id="5601c-105">XTYP\_EXECUTE transaction</span></span>

<span data-ttu-id="5601c-106">Un client utilise la transaction d' **\_ exécution XTYP** pour envoyer une chaîne de commande au serveur.</span><span class="sxs-lookup"><span data-stu-id="5601c-106">A client uses the **XTYP\_EXECUTE** transaction to send a command string to the server.</span></span> <span data-ttu-id="5601c-107">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie **XTYP \_ Execute** dans la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="5601c-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_EXECUTE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="5601c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5601c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5601c-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="5601c-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-110">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="5601c-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5601c-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="5601c-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5601c-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5601c-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="5601c-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-114">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="5601c-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="5601c-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5601c-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-116">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="5601c-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="5601c-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5601c-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5601c-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5601c-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="5601c-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-120">Handle de la chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="5601c-120">A handle to the command string.</span></span>

</dd> <dt>

<span data-ttu-id="5601c-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5601c-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5601c-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5601c-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5601c-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5601c-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5601c-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5601c-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5601c-125">Return value</span></span>

<span data-ttu-id="5601c-126">Une fonction de rappel de serveur doit retourner le **\_ Fack DDE** si elle traite cette transaction, **DDE \_ FBUSY** si elle est trop occupée pour traiter cette transaction, ou **DDE \_ FNOTPROCESSED** si elle rejette cette transaction.</span><span class="sxs-lookup"><span data-stu-id="5601c-126">A server callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="5601c-127">Notes</span><span class="sxs-lookup"><span data-stu-id="5601c-127">Remarks</span></span>

<span data-ttu-id="5601c-128">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Fail \_ Execute** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="5601c-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_EXECUTES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="5601c-129">Une application doit libérer le descripteur de données obtenu pendant cette transaction.</span><span class="sxs-lookup"><span data-stu-id="5601c-129">An application must free the data handle obtained during this transaction.</span></span> <span data-ttu-id="5601c-130">Toutefois, une application doit copier la chaîne de commande associée au descripteur de données si l’application doit traiter la chaîne après le retour de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5601c-130">An application must, however, copy the command string associated with the data handle if the application must process the string after the callback function returns.</span></span> <span data-ttu-id="5601c-131">Une application peut utiliser la fonction [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) pour copier les données.</span><span class="sxs-lookup"><span data-stu-id="5601c-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

<span data-ttu-id="5601c-132">Étant donné que la plupart des applications clientes s’attendent à ce qu’une application serveur effectue une transaction d' **\_ exécution de XTYP** de manière synchrone, un serveur doit tenter d’effectuer tout le traitement de la transaction **XTYP \_ Execute** à partir de la fonction de rappel DDE ou en retournant le code de retour du **\_ bloc CBR** .</span><span class="sxs-lookup"><span data-stu-id="5601c-132">Because most client applications expect a server application to perform an **XTYP\_EXECUTE** transaction synchronously, a server should attempt to perform all processing of the **XTYP\_EXECUTE** transaction either from within the DDE callback function or by returning the **CBR\_BLOCK** return code.</span></span> <span data-ttu-id="5601c-133">Si le paramètre *hdata* est une commande qui indique au serveur de s’arrêter, le serveur doit le faire après avoir traité la transaction **XTYP \_ Execute** .</span><span class="sxs-lookup"><span data-stu-id="5601c-133">If the *hdata* parameter is a command that instructs the server to terminate, the server should do so after processing the **XTYP\_EXECUTE** transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="5601c-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5601c-134">Requirements</span></span>



| <span data-ttu-id="5601c-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5601c-135">Requirement</span></span> | <span data-ttu-id="5601c-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5601c-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5601c-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5601c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5601c-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5601c-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5601c-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5601c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5601c-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5601c-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5601c-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="5601c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5601c-142"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5601c-142"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5601c-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5601c-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="5601c-144">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5601c-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5601c-145">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="5601c-145">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="5601c-146">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="5601c-146">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="5601c-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="5601c-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="5601c-148">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5601c-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5601c-149">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="5601c-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

