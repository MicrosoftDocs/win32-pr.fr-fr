---
title: XTYP_ADVREQ transaction (Ddeml. h)
description: La \_ transaction XTYP ADVREQ informe le serveur qu’une transaction de notification est en suspens sur le nom de rubrique et la paire de noms d’éléments spécifiés et que les données correspondant à la paire nom de la rubrique et nom de l’élément ont changé.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- Échange de données de transaction XTYP_ADVREQ
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384783"
---
# <a name="xtyp_advreq-transaction"></a><span data-ttu-id="5cf79-104">\_Transaction ADVREQ XTYP</span><span class="sxs-lookup"><span data-stu-id="5cf79-104">XTYP\_ADVREQ transaction</span></span>

<span data-ttu-id="5cf79-105">La transaction **XTYP \_ ADVREQ** informe le serveur qu’une transaction de notification est en suspens sur le nom de rubrique et la paire de noms d’éléments spécifiés et que les données correspondant à la paire nom de la rubrique et nom de l’élément ont changé.</span><span class="sxs-lookup"><span data-stu-id="5cf79-105">The **XTYP\_ADVREQ** transaction informs the server that an advise transaction is outstanding on the specified topic name and item name pair and that data corresponding to the topic name and item name pair has changed.</span></span> <span data-ttu-id="5cf79-106">Le système envoie cette transaction à la fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), une fois que le serveur a appelé la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="5cf79-106">The system sends this transaction to the Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), after the server calls the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="5cf79-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cf79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cf79-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="5cf79-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-109">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="5cf79-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5cf79-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="5cf79-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-111">Format dans lequel les données doivent être envoyées au client.</span><span class="sxs-lookup"><span data-stu-id="5cf79-111">The format in which the data should be submitted to the client.</span></span>

</dd> <dt>

<span data-ttu-id="5cf79-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="5cf79-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-113">Handle de la conversation.</span><span class="sxs-lookup"><span data-stu-id="5cf79-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="5cf79-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5cf79-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-115">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="5cf79-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="5cf79-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5cf79-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-117">Handle du nom de l’élément qui a changé.</span><span class="sxs-lookup"><span data-stu-id="5cf79-117">A handle to the item name that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="5cf79-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="5cf79-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-119">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5cf79-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5cf79-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5cf79-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-121">Nombre, dans le mot de poids faible, des transactions **XTYP \_ ADVREQ** qui restent à traiter sur la même rubrique, le même élément et le même nom de format définis dans le contexte de l’appel actuel à la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="5cf79-121">The count, in the low-order word, of **XTYP\_ADVREQ** transactions that remain to be processed on the same topic, item, and format name set within the context of the current call to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span> <span data-ttu-id="5cf79-122">Le nombre est égal à zéro si la transaction **XTYP \_ ADVREQ** actuelle est la dernière.</span><span class="sxs-lookup"><span data-stu-id="5cf79-122">The count is zero if the current **XTYP\_ADVREQ** transaction is the last one.</span></span> <span data-ttu-id="5cf79-123">Un serveur peut utiliser ce nombre pour déterminer s’il faut créer un descripteur de données **HDATA \_ APPOWNED** pour les données de notification.</span><span class="sxs-lookup"><span data-stu-id="5cf79-123">A server can use this count to determine whether to create an **HDATA\_APPOWNED** data handle to the advise data.</span></span>

<span data-ttu-id="5cf79-124">Le mot de poids faible est défini sur **CADV \_ LATEACK** si le Ddeml a émis la transaction **XTYP \_ ADVREQ** en raison d’un message d’accusé de réception DDE \_ d’un client Outrun par le serveur.</span><span class="sxs-lookup"><span data-stu-id="5cf79-124">The low-order word is set to **CADV\_LATEACK** if the DDEML issued the **XTYP\_ADVREQ** transaction because of a late-arriving DDE\_ACK message from a client being outrun by the server.</span></span>

<span data-ttu-id="5cf79-125">Le mot de poids fort n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5cf79-125">The high-order word is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5cf79-126">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5cf79-126">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf79-127">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5cf79-127">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cf79-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5cf79-128">Return value</span></span>

<span data-ttu-id="5cf79-129">Le serveur doit d’abord appeler la fonction [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) pour créer un handle de données qui identifie les données modifiées, puis retourner le descripteur.</span><span class="sxs-lookup"><span data-stu-id="5cf79-129">The server should first call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the changed data and then return the handle.</span></span> <span data-ttu-id="5cf79-130">Le serveur doit retourner la **valeur null** s’il ne parvient pas à terminer la transaction.</span><span class="sxs-lookup"><span data-stu-id="5cf79-130">The server should return **NULL** if it is unable to complete the transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf79-131">Notes</span><span class="sxs-lookup"><span data-stu-id="5cf79-131">Remarks</span></span>

<span data-ttu-id="5cf79-132">Un serveur ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="5cf79-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf79-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cf79-133">Requirements</span></span>



| <span data-ttu-id="5cf79-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cf79-134">Requirement</span></span> | <span data-ttu-id="5cf79-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cf79-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf79-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cf79-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf79-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cf79-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5cf79-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cf79-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf79-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cf79-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5cf79-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cf79-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cf79-141"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cf79-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf79-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cf79-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="5cf79-143">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5cf79-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5cf79-144">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="5cf79-144">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="5cf79-145">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="5cf79-145">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="5cf79-146">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="5cf79-146">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="5cf79-147">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5cf79-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5cf79-148">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="5cf79-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

