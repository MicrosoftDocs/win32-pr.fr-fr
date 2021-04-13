---
description: Libère l’utilisation exclusive de la carte à puce connectée.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'ISCardManage :: SCardUnlock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202303"
---
# <a name="iscardmanagescardunlock-method"></a><span data-ttu-id="12ea6-103">ISCardManage :: SCardUnlock, méthode</span><span class="sxs-lookup"><span data-stu-id="12ea6-103">ISCardManage::SCardUnlock method</span></span>

<span data-ttu-id="12ea6-104">\[La méthode **SCardUnlock** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="12ea6-104">\[The **SCardUnlock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="12ea6-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="12ea6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="12ea6-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="12ea6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="12ea6-107">La méthode **SCardUnlock** libère l’utilisation exclusive de la [*carte à puce*](../secgloss/s-gly.md)connectée.</span><span class="sxs-lookup"><span data-stu-id="12ea6-107">The **SCardUnlock** method releases exclusive use of the connected [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12ea6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12ea6-108">Syntax</span></span>


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="12ea6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12ea6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ea6-110">*Disposition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12ea6-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ea6-111">État dans lequel la carte à puce doit être laissée lorsque le verrou est libéré.</span><span class="sxs-lookup"><span data-stu-id="12ea6-111">The state to leave the smart card in when the lock is released.</span></span>

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

<span data-ttu-id="12ea6-112">**CONGÉ**</span><span class="sxs-lookup"><span data-stu-id="12ea6-112">**LEAVE**</span></span>
</dt><span id="RESET"></span><span id="reset"></span><dt>

<span data-ttu-id="12ea6-113">**RESET**</span><span class="sxs-lookup"><span data-stu-id="12ea6-113">**RESET**</span></span>
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

<span data-ttu-id="12ea6-114">**Hors tension**</span><span class="sxs-lookup"><span data-stu-id="12ea6-114">**UNPOWER**</span></span>
</dt><span id="EJECT"></span><span id="eject"></span><dt>

<span data-ttu-id="12ea6-115">**ÉMISSION**</span><span class="sxs-lookup"><span data-stu-id="12ea6-115">**EJECT**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ea6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12ea6-116">Return value</span></span>

<span data-ttu-id="12ea6-117">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="12ea6-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="12ea6-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="12ea6-118">Return code</span></span>                                                                                  | <span data-ttu-id="12ea6-119">Description</span><span class="sxs-lookup"><span data-stu-id="12ea6-119">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="12ea6-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12ea6-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="12ea6-121">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="12ea6-121">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="12ea6-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="12ea6-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="12ea6-123">Le paramètre *disposition* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="12ea6-123">The *Disposition* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="12ea6-124">Notes</span><span class="sxs-lookup"><span data-stu-id="12ea6-124">Remarks</span></span>

<span data-ttu-id="12ea6-125">Pour verrouiller la carte à puce connectée, appelez [**SCardLock**](iscardmanage-scardlock.md).</span><span class="sxs-lookup"><span data-stu-id="12ea6-125">To lock the connected smart card, call [**SCardLock**](iscardmanage-scardlock.md).</span></span>

<span data-ttu-id="12ea6-126">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="12ea6-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="12ea6-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="12ea6-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="12ea6-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="12ea6-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12ea6-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12ea6-129">Requirements</span></span>



| <span data-ttu-id="12ea6-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12ea6-130">Requirement</span></span> | <span data-ttu-id="12ea6-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="12ea6-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12ea6-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12ea6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="12ea6-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12ea6-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="12ea6-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12ea6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="12ea6-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12ea6-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="12ea6-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="12ea6-136">End of client support</span></span><br/>    | <span data-ttu-id="12ea6-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="12ea6-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="12ea6-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="12ea6-138">End of server support</span></span><br/>    | <span data-ttu-id="12ea6-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12ea6-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="12ea6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12ea6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ea6-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="12ea6-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="12ea6-142">**SCardLock**</span><span class="sxs-lookup"><span data-stu-id="12ea6-142">**SCardLock**</span></span>](iscardmanage-scardlock.md)
</dt> </dl>

 

 
