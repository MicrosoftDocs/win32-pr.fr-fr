---
description: Réinitialise le contexte de sécurité actuel de la carte à puce.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'ISCardVerify :: ResetSecurityState, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861978"
---
# <a name="iscardverifyresetsecuritystate-method"></a><span data-ttu-id="fc6e2-103">ISCardVerify :: ResetSecurityState, méthode</span><span class="sxs-lookup"><span data-stu-id="fc6e2-103">ISCardVerify::ResetSecurityState method</span></span>

<span data-ttu-id="fc6e2-104">\[La méthode **ResetSecurityState** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="fc6e2-104">\[The **ResetSecurityState** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fc6e2-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fc6e2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fc6e2-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="fc6e2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fc6e2-107">La méthode **ResetSecurityState** réinitialise le contexte de [*sécurité*](../secgloss/s-gly.md) actuel de la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fc6e2-107">The **ResetSecurityState** method resets the current [*security context*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6e2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc6e2-108">Syntax</span></span>


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a><span data-ttu-id="fc6e2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc6e2-109">Parameters</span></span>

<span data-ttu-id="fc6e2-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fc6e2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc6e2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc6e2-111">Return value</span></span>

<span data-ttu-id="fc6e2-112">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="fc6e2-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="fc6e2-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fc6e2-113">Return code</span></span>                                                                                   | <span data-ttu-id="fc6e2-114">Description</span><span class="sxs-lookup"><span data-stu-id="fc6e2-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fc6e2-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6e2-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fc6e2-116">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="fc6e2-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fc6e2-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6e2-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fc6e2-118">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="fc6e2-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="fc6e2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fc6e2-119">Remarks</span></span>

<span data-ttu-id="fc6e2-120">Pour réactiver le [*contexte de sécurité*](../secgloss/s-gly.md) sans réinitialiser, appelez [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc6e2-120">To re-enable the [*security context*](../secgloss/s-gly.md) without resetting, call [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span></span>

<span data-ttu-id="fc6e2-121">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="fc6e2-121">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="fc6e2-122">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="fc6e2-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fc6e2-123">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fc6e2-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6e2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc6e2-124">Requirements</span></span>



| <span data-ttu-id="fc6e2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc6e2-125">Requirement</span></span> | <span data-ttu-id="fc6e2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc6e2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc6e2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc6e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fc6e2-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc6e2-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fc6e2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc6e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fc6e2-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc6e2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fc6e2-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fc6e2-131">End of client support</span></span><br/>    | <span data-ttu-id="fc6e2-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc6e2-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fc6e2-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fc6e2-133">End of server support</span></span><br/>    | <span data-ttu-id="fc6e2-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc6e2-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="fc6e2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc6e2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6e2-136">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="fc6e2-136">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

<span data-ttu-id="fc6e2-137">[**Verrouillage**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc6e2-137">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>
</dt> </dl>

 

 
