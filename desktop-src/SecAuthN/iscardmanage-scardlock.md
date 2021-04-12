---
description: Verrouille une carte à puce connectée pour une utilisation exclusive.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'ISCardManage :: SCardLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202305"
---
# <a name="iscardmanagescardlock-method"></a><span data-ttu-id="d54dc-103">ISCardManage :: SCardLock, méthode</span><span class="sxs-lookup"><span data-stu-id="d54dc-103">ISCardManage::SCardLock method</span></span>

<span data-ttu-id="d54dc-104">\[La méthode **SCardLock** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d54dc-104">\[The **SCardLock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d54dc-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d54dc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d54dc-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d54dc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d54dc-107">La méthode **SCardLock** verrouille une [*carte à puce*](../secgloss/s-gly.md) connectée pour une utilisation exclusive.</span><span class="sxs-lookup"><span data-stu-id="d54dc-107">The **SCardLock** method locks a connected [*smart card*](../secgloss/s-gly.md) for exclusive use.</span></span>

## <a name="syntax"></a><span data-ttu-id="d54dc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d54dc-108">Syntax</span></span>


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a><span data-ttu-id="d54dc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d54dc-109">Parameters</span></span>

<span data-ttu-id="d54dc-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d54dc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d54dc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d54dc-111">Return value</span></span>

<span data-ttu-id="d54dc-112">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="d54dc-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="d54dc-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d54dc-113">Return code</span></span>                                                                            | <span data-ttu-id="d54dc-114">Description</span><span class="sxs-lookup"><span data-stu-id="d54dc-114">Description</span></span>                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d54dc-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d54dc-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d54dc-116">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d54dc-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d54dc-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="d54dc-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d54dc-118">L’opération n’a pas pu se terminer.</span><span class="sxs-lookup"><span data-stu-id="d54dc-118">Operation failed to complete.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="d54dc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d54dc-119">Remarks</span></span>

<span data-ttu-id="d54dc-120">Pour libérer l’utilisation exclusive de la carte à puce connectée, appelez [**SCardUnlock**](iscardmanage-scardunlock.md).</span><span class="sxs-lookup"><span data-stu-id="d54dc-120">To releases exclusive use of the connected smart card, call [**SCardUnlock**](iscardmanage-scardunlock.md).</span></span>

<span data-ttu-id="d54dc-121">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="d54dc-121">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="d54dc-122">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="d54dc-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d54dc-123">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d54dc-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d54dc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d54dc-124">Requirements</span></span>



| <span data-ttu-id="d54dc-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d54dc-125">Requirement</span></span> | <span data-ttu-id="d54dc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d54dc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d54dc-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d54dc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d54dc-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d54dc-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d54dc-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d54dc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d54dc-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d54dc-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d54dc-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d54dc-131">End of client support</span></span><br/>    | <span data-ttu-id="d54dc-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d54dc-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d54dc-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d54dc-133">End of server support</span></span><br/>    | <span data-ttu-id="d54dc-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d54dc-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d54dc-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d54dc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54dc-136">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="d54dc-136">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="d54dc-137">**SCardUnlock**</span><span class="sxs-lookup"><span data-stu-id="d54dc-137">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
