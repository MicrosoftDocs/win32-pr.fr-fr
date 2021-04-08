---
title: XTYP_UNREGISTER transaction (Ddeml. h)
description: Une fonction de rappel échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction d’annulation d’inscription XTYP chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (Ddeml) utilise la fonction DdeNameService pour annuler l’inscription d’un nom de service, ou chaque fois qu’une application non Ddeml qui prend en charge la rubrique système est terminée.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Échange de données de transaction XTYP_UNREGISTER
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742869"
---
# <a name="xtyp_unregister-transaction"></a><span data-ttu-id="bd825-104">XTYP \_ Annuler l’inscription de la transaction</span><span class="sxs-lookup"><span data-stu-id="bd825-104">XTYP\_UNREGISTER transaction</span></span>

<span data-ttu-id="bd825-105">Une fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction d' **annulation d' \_ inscription XTYP** chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (Ddeml) utilise la fonction [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour annuler l’inscription d’un nom de service, ou chaque fois qu’une application non Ddeml qui prend en charge la rubrique système est terminée.</span><span class="sxs-lookup"><span data-stu-id="bd825-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_UNREGISTER** transaction whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to unregister a service name, or whenever a non-DDEML application that supports the System topic is terminated.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="bd825-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd825-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd825-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="bd825-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-108">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="bd825-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="bd825-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd825-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="bd825-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd825-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="bd825-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-114">Handle vers le nom du service de base en cours d’annulation de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="bd825-114">A handle to the base service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="bd825-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-116">Handle vers le nom de service spécifique à l’instance qui est désinscrit.</span><span class="sxs-lookup"><span data-stu-id="bd825-116">A handle to the instance-specific service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="bd825-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd825-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="bd825-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd825-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="bd825-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd825-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd825-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bd825-123">Remarks</span></span>

<span data-ttu-id="bd825-124">Cette transaction est filtrée si l’application a spécifié l’indicateur **\_ \_ d’omission des inscriptions CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="bd825-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="bd825-125">Une application ne peut pas bloquer ce type de transaction ; le \_ Code de retour de bloc CBR est ignoré.</span><span class="sxs-lookup"><span data-stu-id="bd825-125">A application cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

<span data-ttu-id="bd825-126">Une application doit utiliser le paramètre *HSZ1* pour supprimer le nom du service de la liste des serveurs disponibles pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd825-126">An application should use the *hsz1* parameter to remove the service name from the list of servers available to the user.</span></span> <span data-ttu-id="bd825-127">Une application doit utiliser le paramètre *hsz2* pour identifier l’instance d’application qui s’est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="bd825-127">An application should use the *hsz2* parameter to identify which application instance has terminated.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd825-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd825-128">Requirements</span></span>



| <span data-ttu-id="bd825-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd825-129">Requirement</span></span> | <span data-ttu-id="bd825-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd825-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd825-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd825-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bd825-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd825-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bd825-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd825-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bd825-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd825-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="bd825-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd825-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd825-136"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd825-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd825-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd825-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd825-138">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bd825-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd825-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="bd825-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="bd825-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="bd825-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="bd825-141">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="bd825-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bd825-142">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="bd825-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

