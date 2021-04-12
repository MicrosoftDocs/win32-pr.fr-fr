---
title: XTYP_CONNECT_CONFIRM transaction (Ddeml. h)
description: Une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit \_ la \_ transaction XTYP Connect Confirm pour confirmer qu’une conversation a été établie avec un client et pour fournir au serveur le descripteur de conversation.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- Échange de données de transaction XTYP_CONNECT_CONFIRM
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384779"
---
# <a name="xtyp_connect_confirm-transaction"></a><span data-ttu-id="c7105-104">Transaction de confirmation de \_ connexion XTYP \_</span><span class="sxs-lookup"><span data-stu-id="c7105-104">XTYP\_CONNECT\_CONFIRM transaction</span></span>

<span data-ttu-id="c7105-105">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction **XTYP \_ Connect \_ Confirm** pour confirmer qu’une conversation a été établie avec un client et pour fournir au serveur le descripteur de conversation.</span><span class="sxs-lookup"><span data-stu-id="c7105-105">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_CONNECT\_CONFIRM** transaction to confirm that a conversation has been established with a client and to provide the server with the conversation handle.</span></span> <span data-ttu-id="c7105-106">Le système envoie cette transaction à la suite d’une transaction [**XTYP \_ Connect**](xtyp-connect.md) ou [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="c7105-106">The system sends this transaction as a result of a previous [**XTYP\_CONNECT**](xtyp-connect.md) or [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="c7105-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7105-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7105-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="c7105-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-109">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="c7105-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c7105-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="c7105-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c7105-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7105-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="c7105-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-113">Handle de la nouvelle conversation.</span><span class="sxs-lookup"><span data-stu-id="c7105-113">A handle to the new conversation.</span></span>

</dd> <dt>

<span data-ttu-id="c7105-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c7105-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-115">Handle vers le nom de la rubrique sur laquelle la conversation a été établie.</span><span class="sxs-lookup"><span data-stu-id="c7105-115">A handle to the topic name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="c7105-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c7105-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-117">Handle vers le nom du service sur lequel la conversation a été établie.</span><span class="sxs-lookup"><span data-stu-id="c7105-117">A handle to the service name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="c7105-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="c7105-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-119">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c7105-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7105-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c7105-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-121">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c7105-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7105-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c7105-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c7105-123">Spécifie si le client est la même instance d’application que le serveur.</span><span class="sxs-lookup"><span data-stu-id="c7105-123">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="c7105-124">Si le paramètre est égal à 1, le client est la même instance.</span><span class="sxs-lookup"><span data-stu-id="c7105-124">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="c7105-125">Si le paramètre a la valeur 0, le client est une instance différente.</span><span class="sxs-lookup"><span data-stu-id="c7105-125">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7105-126">Notes</span><span class="sxs-lookup"><span data-stu-id="c7105-126">Remarks</span></span>

<span data-ttu-id="c7105-127">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Skip \_ Connect \_ Confirm** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="c7105-127">This transaction is filtered if the server application specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="c7105-128">Un serveur ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c7105-128">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7105-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7105-129">Requirements</span></span>



| <span data-ttu-id="c7105-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7105-130">Requirement</span></span> | <span data-ttu-id="c7105-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7105-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7105-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7105-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c7105-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7105-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c7105-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7105-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c7105-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7105-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c7105-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7105-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7105-137"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7105-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7105-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7105-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7105-139">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c7105-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7105-140">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="c7105-140">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="c7105-141">**DdeConnectList**</span><span class="sxs-lookup"><span data-stu-id="c7105-141">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[<span data-ttu-id="c7105-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="c7105-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="c7105-143">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c7105-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7105-144">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="c7105-144">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

