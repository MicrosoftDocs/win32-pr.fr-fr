---
title: XTYP_ADVDATA transaction (Ddeml. h)
description: Informe le client que la valeur de l’élément de données a changé. La fonction de rappel du client échange dynamique de données (DDE), DdeCallback, reçoit cette transaction après avoir établi une boucle de notification avec un serveur.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- Échange de données de transaction XTYP_ADVDATA
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511739"
---
# <a name="xtyp_advdata-transaction"></a><span data-ttu-id="1a52b-105">\_Transaction ADVDATA XTYP</span><span class="sxs-lookup"><span data-stu-id="1a52b-105">XTYP\_ADVDATA transaction</span></span>

<span data-ttu-id="1a52b-106">Informe le client que la valeur de l’élément de données a changé.</span><span class="sxs-lookup"><span data-stu-id="1a52b-106">Informs the client that the value of the data item has changed.</span></span> <span data-ttu-id="1a52b-107">La fonction de rappel du client échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction après avoir établi une boucle de notification avec un serveur.</span><span class="sxs-lookup"><span data-stu-id="1a52b-107">The Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction after establishing an advise loop with a server.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="1a52b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a52b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a52b-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="1a52b-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-110">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="1a52b-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="1a52b-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="1a52b-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-112">Format Atom des données envoyées à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="1a52b-112">The format atom of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="1a52b-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="1a52b-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-114">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="1a52b-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="1a52b-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="1a52b-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-116">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="1a52b-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="1a52b-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="1a52b-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-118">Handle du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="1a52b-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="1a52b-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="1a52b-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-120">Handle vers les données associées au nom de la rubrique et à la paire de noms d’éléments.</span><span class="sxs-lookup"><span data-stu-id="1a52b-120">A handle to the data associated with the topic name and item name pair.</span></span> <span data-ttu-id="1a52b-121">Ce paramètre a la **valeur null** si le client a spécifié l’indicateur **\_ NoData XTYPF** lors de la demande de la boucle de notification.</span><span class="sxs-lookup"><span data-stu-id="1a52b-121">This parameter is **NULL** if the client specified the **XTYPF\_NODATA** flag when it requested the advise loop.</span></span>

</dd> <dt>

<span data-ttu-id="1a52b-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="1a52b-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-123">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a52b-123">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a52b-124">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="1a52b-124">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="1a52b-125">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a52b-125">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a52b-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a52b-126">Return value</span></span>

<span data-ttu-id="1a52b-127">Une fonction de rappel DDE doit retourner le **\_ Fack DDE** si elle traite cette transaction, **DDE \_ FBUSY** si elle est trop occupée pour traiter cette transaction, ou **DDE \_ FNOTPROCESSED** si elle rejette cette transaction.</span><span class="sxs-lookup"><span data-stu-id="1a52b-127">A DDE callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a52b-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1a52b-128">Remarks</span></span>

<span data-ttu-id="1a52b-129">Une application ne doit pas libérer le descripteur de données obtenu pendant cette transaction.</span><span class="sxs-lookup"><span data-stu-id="1a52b-129">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="1a52b-130">Toutefois, une application doit copier les données associées au descripteur de données si l’application doit traiter les données après le retour de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1a52b-130">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="1a52b-131">Une application peut utiliser la fonction [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) pour copier les données.</span><span class="sxs-lookup"><span data-stu-id="1a52b-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a52b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a52b-132">Requirements</span></span>



| <span data-ttu-id="1a52b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a52b-133">Requirement</span></span> | <span data-ttu-id="1a52b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a52b-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a52b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a52b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1a52b-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a52b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1a52b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a52b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1a52b-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a52b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1a52b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a52b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a52b-140"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a52b-140"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a52b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a52b-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a52b-142">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1a52b-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a52b-143">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="1a52b-143">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="1a52b-144">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="1a52b-144">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="1a52b-145">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="1a52b-145">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="1a52b-146">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1a52b-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a52b-147">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="1a52b-147">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

