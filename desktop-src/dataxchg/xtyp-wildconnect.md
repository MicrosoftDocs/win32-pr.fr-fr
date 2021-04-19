---
title: XTYP_WILDCONNECT transaction (Ddeml. h)
description: Permet à un client d’établir une conversation sur chacune des paires nom de service et nom de rubrique du serveur qui correspondent au nom du service et au nom de la rubrique spécifiés.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Échange de données de transaction XTYP_WILDCONNECT
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510140"
---
# <a name="xtyp_wildconnect-transaction"></a><span data-ttu-id="5c03b-104">\_Transaction WILDCONNECT XTYP</span><span class="sxs-lookup"><span data-stu-id="5c03b-104">XTYP\_WILDCONNECT transaction</span></span>

<span data-ttu-id="5c03b-105">Permet à un client d’établir une conversation sur chacune des paires nom de service et nom de rubrique du serveur qui correspondent au nom du service et au nom de la rubrique spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5c03b-105">Enables a client to establish a conversation on each of the server's service name and topic name pairs that match the specified service name and topic name.</span></span> <span data-ttu-id="5c03b-106">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie un nom de service **null** , un nom de rubrique **null** ou les deux dans un appel à la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) ou [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="5c03b-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a **NULL** service name, a **NULL** topic name, or both in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) or [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="5c03b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c03b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c03b-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="5c03b-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-109">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="5c03b-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5c03b-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="5c03b-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c03b-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c03b-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="5c03b-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c03b-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c03b-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5c03b-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-115">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="5c03b-115">A handle to the topic name.</span></span> <span data-ttu-id="5c03b-116">Si ce paramètre a la **valeur null**, le client demande une conversation sur tous les noms de rubriques que le serveur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="5c03b-116">If this parameter is **NULL**, the client is requesting a conversation on all topic names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="5c03b-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5c03b-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-118">Handle vers le nom du service.</span><span class="sxs-lookup"><span data-stu-id="5c03b-118">A handle to the service name.</span></span> <span data-ttu-id="5c03b-119">Si ce paramètre a la **valeur null**, le client demande une conversation sur tous les noms de service pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="5c03b-119">If this parameter is **NULL**, the client is requesting a conversation on all service names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="5c03b-120">*hdata*</span><span class="sxs-lookup"><span data-stu-id="5c03b-120">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-121">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c03b-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c03b-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5c03b-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-123">Pointeur vers une structure [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) qui contient des informations de contexte pour la conversation.</span><span class="sxs-lookup"><span data-stu-id="5c03b-123">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="5c03b-124">Si le client n’est pas une application DDEML, ce paramètre a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="5c03b-124">If the client is not a DDEML application, this parameter is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="5c03b-125">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5c03b-125">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5c03b-126">Spécifie si le client est la même instance d’application que le serveur.</span><span class="sxs-lookup"><span data-stu-id="5c03b-126">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="5c03b-127">Si le paramètre est 1, le client est la même instance.</span><span class="sxs-lookup"><span data-stu-id="5c03b-127">If the parameter is 1, the client is same instance.</span></span> <span data-ttu-id="5c03b-128">Si le paramètre a la valeur 0, le client est une instance différente.</span><span class="sxs-lookup"><span data-stu-id="5c03b-128">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c03b-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c03b-129">Return value</span></span>

<span data-ttu-id="5c03b-130">Le serveur doit retourner un handle de données qui identifie un tableau de structures [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="5c03b-130">The server should return a data handle that identifies an array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="5c03b-131">Le tableau doit contenir une structure pour chaque paire Service-Name et Topic-Name qui correspond à la paire Service-Name et Topic-Name demandée par le client.</span><span class="sxs-lookup"><span data-stu-id="5c03b-131">The array should contain one structure for each service-name and topic-name pair that matches the service-name and topic-name pair requested by the client.</span></span> <span data-ttu-id="5c03b-132">Le tableau doit se terminer par un handle de chaîne **null** .</span><span class="sxs-lookup"><span data-stu-id="5c03b-132">The array must be terminated by a **NULL** string handle.</span></span> <span data-ttu-id="5c03b-133">Le système envoie la [**transaction \_ \_ Confirm XTYP Connect**](xtyp-connect-confirm.md) au serveur pour confirmer chaque conversation et transmettre les descripteurs de conversation au serveur.</span><span class="sxs-lookup"><span data-stu-id="5c03b-133">The system sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server to confirm each conversation and to pass the conversation handles to the server.</span></span> <span data-ttu-id="5c03b-134">Le serveur ne recevra pas ces confirmations s’il a spécifié l’indicateur **CBF \_ Skip \_ Connect \_ Confirm** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="5c03b-134">The server will not receive these confirmations if it specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="5c03b-135">Le serveur doit retourner la **valeur null** pour refuser la transaction **XTYP \_ WILDCONNECT** .</span><span class="sxs-lookup"><span data-stu-id="5c03b-135">The server should return **NULL** to refuse the **XTYP\_WILDCONNECT** transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c03b-136">Notes</span><span class="sxs-lookup"><span data-stu-id="5c03b-136">Remarks</span></span>

<span data-ttu-id="5c03b-137">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Fail \_ connections** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="5c03b-137">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="5c03b-138">Un serveur ne peut pas bloquer ce type de transaction ; le \_ Code de retour de bloc CBR est ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c03b-138">A server cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c03b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c03b-139">Requirements</span></span>



| <span data-ttu-id="5c03b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c03b-140">Requirement</span></span> | <span data-ttu-id="5c03b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c03b-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c03b-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c03b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5c03b-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c03b-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5c03b-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c03b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5c03b-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c03b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5c03b-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c03b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c03b-147"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c03b-147"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c03b-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c03b-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c03b-149">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5c03b-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c03b-150">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="5c03b-150">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="5c03b-151">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="5c03b-151">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="5c03b-152">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="5c03b-152">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="5c03b-153">**HSZPAIR**</span><span class="sxs-lookup"><span data-stu-id="5c03b-153">**HSZPAIR**</span></span>](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

<span data-ttu-id="5c03b-154">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5c03b-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c03b-155">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="5c03b-155">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

