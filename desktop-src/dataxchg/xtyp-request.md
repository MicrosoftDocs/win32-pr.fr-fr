---
title: XTYP_REQUEST transaction (Ddeml. h)
description: Un client utilise la \_ transaction de demande XTYP pour demander des données à un serveur. Une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit cette transaction lorsqu’un client spécifie \_ la demande XTYP dans la fonction DdeClientTransaction.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- Échange de données de transaction XTYP_REQUEST
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740325"
---
# <a name="xtyp_request-transaction"></a><span data-ttu-id="66178-105">\_Transaction de requête XTYP</span><span class="sxs-lookup"><span data-stu-id="66178-105">XTYP\_REQUEST transaction</span></span>

<span data-ttu-id="66178-106">Un client utilise la transaction de **\_ demande XTYP** pour demander des données à un serveur.</span><span class="sxs-lookup"><span data-stu-id="66178-106">A client uses the **XTYP\_REQUEST** transaction to request data from a server.</span></span> <span data-ttu-id="66178-107">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie la **\_ demande XTYP** dans la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="66178-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_REQUEST** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a><span data-ttu-id="66178-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66178-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66178-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="66178-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-110">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="66178-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="66178-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="66178-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-112">Format dans lequel le serveur doit envoyer des données au client.</span><span class="sxs-lookup"><span data-stu-id="66178-112">The format in which the server should submit data to the client.</span></span>

</dd> <dt>

<span data-ttu-id="66178-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="66178-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-114">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="66178-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="66178-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="66178-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-116">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="66178-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="66178-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="66178-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-118">Handle du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="66178-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="66178-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="66178-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="66178-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="66178-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="66178-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="66178-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="66178-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="66178-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="66178-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="66178-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66178-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66178-125">Return value</span></span>

<span data-ttu-id="66178-126">Le serveur doit appeler la fonction [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) pour créer un handle de données qui identifie les données, puis retourne le descripteur.</span><span class="sxs-lookup"><span data-stu-id="66178-126">The server should call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the data and then return the handle.</span></span> <span data-ttu-id="66178-127">Le serveur doit retourner la **valeur null** s’il ne parvient pas à terminer la transaction.</span><span class="sxs-lookup"><span data-stu-id="66178-127">The server should return **NULL** if it is unable to complete the transaction.</span></span> <span data-ttu-id="66178-128">Si le serveur retourne la **valeur null**, le client recevra un \_ indicateur DDE FNOTPROCESSED.</span><span class="sxs-lookup"><span data-stu-id="66178-128">If the server returns **NULL**, the client will receive a DDE\_FNOTPROCESSED flag.</span></span>

## <a name="remarks"></a><span data-ttu-id="66178-129">Notes</span><span class="sxs-lookup"><span data-stu-id="66178-129">Remarks</span></span>

<span data-ttu-id="66178-130">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Fail \_ requests** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="66178-130">This transaction is filtered if the server application specified the **CBF\_FAIL\_REQUESTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="66178-131">Si la réponse à cette transaction nécessite un traitement long, le serveur peut renvoyer le \_ Code de retour du bloc CBR pour interrompre les transactions futures sur la conversation en cours, puis traiter la transaction de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="66178-131">If responding to this transaction requires lengthy processing, the server can return the CBR\_BLOCK return code to suspend future transactions on the current conversation and then process the transaction asynchronously.</span></span> <span data-ttu-id="66178-132">Une fois que le serveur est terminé et que les données sont prêtes à être transmises au client, le serveur peut appeler la fonction [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) pour reprendre la conversation.</span><span class="sxs-lookup"><span data-stu-id="66178-132">When the server has finished and the data is ready to pass to the client, the server can call the [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) function to resume the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="66178-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66178-133">Requirements</span></span>



| <span data-ttu-id="66178-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66178-134">Requirement</span></span> | <span data-ttu-id="66178-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="66178-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66178-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66178-136">Minimum supported client</span></span><br/> | <span data-ttu-id="66178-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66178-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="66178-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66178-138">Minimum supported server</span></span><br/> | <span data-ttu-id="66178-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66178-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="66178-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="66178-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="66178-141"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66178-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66178-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66178-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="66178-143">**Référence**</span><span class="sxs-lookup"><span data-stu-id="66178-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66178-144">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="66178-144">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="66178-145">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="66178-145">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="66178-146">**DdeEnableCallback**</span><span class="sxs-lookup"><span data-stu-id="66178-146">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[<span data-ttu-id="66178-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="66178-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="66178-148">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="66178-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="66178-149">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="66178-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

