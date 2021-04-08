---
title: XTYP_ADVSTART transaction (Ddeml. h)
description: Un client utilise la \_ transaction XTYP ADVSTART pour établir une boucle de notification avec un serveur.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- Échange de données de transaction XTYP_ADVSTART
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741860"
---
# <a name="xtyp_advstart-transaction"></a><span data-ttu-id="f6c9d-104">\_Transaction ADVSTART XTYP</span><span class="sxs-lookup"><span data-stu-id="f6c9d-104">XTYP\_ADVSTART transaction</span></span>

<span data-ttu-id="f6c9d-105">Un client utilise la transaction **XTYP \_ ADVSTART** pour établir une boucle de notification avec un serveur.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-105">A client uses the **XTYP\_ADVSTART** transaction to establish an advise loop with a server.</span></span> <span data-ttu-id="f6c9d-106">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie **XTYP \_ ADVSTART** comme paramètre *wType* de la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="f6c9d-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTART** as the *wType* parameter of the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a><span data-ttu-id="f6c9d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6c9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c9d-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-109">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="f6c9d-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-111">Format de données demandé par le client.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-111">The data format requested by the client.</span></span>

</dd> <dt>

<span data-ttu-id="f6c9d-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-113">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="f6c9d-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-115">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="f6c9d-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-117">Handle du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-117">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="f6c9d-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-119">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f6c9d-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-121">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f6c9d-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c9d-123">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-123">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c9d-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6c9d-124">Return value</span></span>

<span data-ttu-id="f6c9d-125">Une fonction de rappel de serveur doit retourner **true** pour autoriser une boucle de notification sur le nom de rubrique et la paire de noms d’élément spécifiés, ou **false** pour refuser la boucle de notification.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-125">A server callback function should return **TRUE** to allow an advise loop on the specified topic name and item name pair, or **FALSE** to deny the advise loop.</span></span> <span data-ttu-id="f6c9d-126">Si la fonction de rappel retourne la **valeur true**, tous les appels suivants à la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) par le serveur sur les mêmes paires nom de rubrique et nom d’élément provoquent l’envoi de transactions [**\_ ADVREQ XTYP**](xtyp-advreq.md) au serveur par le système.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-126">If the callback function returns **TRUE**, any subsequent calls to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function by the server on the same topic name and item name pair causes the system to send [**XTYP\_ADVREQ**](xtyp-advreq.md) transactions to the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c9d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f6c9d-127">Remarks</span></span>

<span data-ttu-id="f6c9d-128">Si un client demande une boucle de notification sur un nom de rubrique, un nom d’élément et un format de données pour une boucle de notification déjà établie, la bibliothèque de gestion échange dynamique de données (DDEML) ne crée pas de boucle de notification en double, mais modifie à la place les indicateurs de boucle de notification (**XTYPF \_ ACKREQ** et **XTYPF \_ NoData**) pour qu’ils correspondent à la dernière requête.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-128">If a client requests an advise loop on a topic name, item name, and data format for an advise loop that is already established, the Dynamic Data Exchange Management Library (DDEML) does not create a duplicate advise loop but instead alters the advise loop flags (**XTYPF\_ACKREQ** and **XTYPF\_NODATA**) to match the latest request.</span></span>

<span data-ttu-id="f6c9d-129">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur de **\_ \_ notifications d’échec CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="f6c9d-129">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c9d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6c9d-130">Requirements</span></span>



| <span data-ttu-id="f6c9d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6c9d-131">Requirement</span></span> | <span data-ttu-id="f6c9d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6c9d-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c9d-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6c9d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c9d-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6c9d-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f6c9d-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6c9d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c9d-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6c9d-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f6c9d-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6c9d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c9d-138"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6c9d-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6c9d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6c9d-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6c9d-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f6c9d-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6c9d-141">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="f6c9d-141">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="f6c9d-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="f6c9d-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="f6c9d-143">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="f6c9d-143">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="f6c9d-144">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f6c9d-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6c9d-145">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="f6c9d-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

