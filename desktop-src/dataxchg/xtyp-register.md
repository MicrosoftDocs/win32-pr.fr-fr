---
title: XTYP_REGISTER transaction (Ddeml. h)
description: Une fonction de rappel échange dynamique de données (DDE), DdeCallback, reçoit le \_ type de transaction XTYP Register chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (Ddeml) utilise la fonction DdeNameService pour inscrire un nom de service, ou chaque fois qu’une application non Ddeml qui prend en charge la rubrique système est démarrée.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- Échange de données de transaction XTYP_REGISTER
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464950"
---
# <a name="xtyp_register-transaction"></a><span data-ttu-id="ce20a-104">\_Transaction Register XTYP</span><span class="sxs-lookup"><span data-stu-id="ce20a-104">XTYP\_REGISTER transaction</span></span>

<span data-ttu-id="ce20a-105">Une fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit le type de transaction **XTYP \_ Register** chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (Ddeml) utilise la fonction [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour inscrire un nom de service, ou chaque fois qu’une application non Ddeml qui prend en charge la rubrique système est démarrée.</span><span class="sxs-lookup"><span data-stu-id="ce20a-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_REGISTER** transaction type whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to register a service name, or whenever a non-DDEML application that supports the System topic is started.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="ce20a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce20a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce20a-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="ce20a-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-108">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="ce20a-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="ce20a-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="ce20a-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ce20a-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ce20a-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="ce20a-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ce20a-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ce20a-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="ce20a-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-114">Handle vers le nom de service de base en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ce20a-114">A handle to the base service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="ce20a-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="ce20a-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-116">Handle vers le nom de service spécifique à l’instance en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ce20a-116">A handle to the instance-specific service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="ce20a-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="ce20a-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ce20a-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ce20a-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="ce20a-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ce20a-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ce20a-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="ce20a-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="ce20a-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ce20a-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce20a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ce20a-123">Remarks</span></span>

<span data-ttu-id="ce20a-124">Cette transaction est filtrée si l’application a spécifié l’indicateur **\_ \_ d’omission des inscriptions CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="ce20a-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="ce20a-125">Une application ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ce20a-125">A application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

<span data-ttu-id="ce20a-126">Une application doit utiliser le paramètre *HSZ1* pour ajouter le nom du service à la liste des serveurs disponibles pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce20a-126">An application should use the *hsz1* parameter to add the service name to the list of servers available to the user.</span></span> <span data-ttu-id="ce20a-127">Une application doit utiliser le paramètre *hsz2* pour identifier l’instance d’application qui a démarré.</span><span class="sxs-lookup"><span data-stu-id="ce20a-127">An application should use the *hsz2* parameter to identify which application instance has started.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce20a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce20a-128">Requirements</span></span>



| <span data-ttu-id="ce20a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce20a-129">Requirement</span></span> | <span data-ttu-id="ce20a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce20a-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce20a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce20a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ce20a-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce20a-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ce20a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce20a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ce20a-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce20a-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ce20a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce20a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce20a-136"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce20a-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce20a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce20a-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce20a-138">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ce20a-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce20a-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="ce20a-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="ce20a-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="ce20a-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="ce20a-141">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ce20a-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ce20a-142">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="ce20a-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

