---
description: Crée un lien de communication vers une carte à puce (ICC) à l’aide d’un handle retourné par le gestionnaire de ressources de carte à puce.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'ISCardManage :: AttachByHandle, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866013"
---
# <a name="iscardmanageattachbyhandle-method"></a><span data-ttu-id="b0e21-103">ISCardManage :: AttachByHandle, méthode</span><span class="sxs-lookup"><span data-stu-id="b0e21-103">ISCardManage::AttachByHandle method</span></span>

<span data-ttu-id="b0e21-104">\[La méthode **AttachByHandle** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b0e21-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b0e21-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b0e21-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b0e21-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="b0e21-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b0e21-107">La méthode **AttachByHandle** crée un lien de communication vers une [*carte à puce*](../secgloss/s-gly.md) (ICC) à l’aide d’un handle renvoyé par le gestionnaire de [*ressources*](../secgloss/r-gly.md)de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="b0e21-107">The **AttachByHandle** method creates a communication link to a [*smart card*](../secgloss/s-gly.md) (ICC) using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e21-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0e21-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a><span data-ttu-id="b0e21-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0e21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e21-110">*hICC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0e21-110">*hICC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e21-111">Handle d’une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="b0e21-111">A handle to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e21-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0e21-112">Return value</span></span>

<span data-ttu-id="b0e21-113">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0e21-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b0e21-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b0e21-114">Return code</span></span>                                                                                   | <span data-ttu-id="b0e21-115">Description</span><span class="sxs-lookup"><span data-stu-id="b0e21-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="b0e21-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e21-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b0e21-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b0e21-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="b0e21-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e21-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b0e21-119">Le paramètre *hICC* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b0e21-119">The *hICC* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="b0e21-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e21-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b0e21-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="b0e21-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="b0e21-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b0e21-122">Remarks</span></span>

<span data-ttu-id="b0e21-123">Pour joindre un appel de [*lecteur*](../secgloss/r-gly.md) [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="b0e21-123">To attach a [*reader*](../secgloss/r-gly.md) call [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="b0e21-124">Pour libérer le [**détachement**](iscardmanage-detach.md)d’un appel de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b0e21-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="b0e21-125">Pour vous reconnecter à la carte à puce sans appeler [**Detach**](iscardmanage-detach.md) et **AttachByHandle**, appelez [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="b0e21-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByHandle**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="b0e21-126">Pour obtenir la liste de toutes les méthodes définies par l’interface [**ISCardManage**](iscardmanage.md) , consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="b0e21-126">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="b0e21-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="b0e21-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b0e21-128">Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b0e21-128">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e21-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0e21-129">Requirements</span></span>



| <span data-ttu-id="b0e21-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0e21-130">Requirement</span></span> | <span data-ttu-id="b0e21-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0e21-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0e21-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e21-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e21-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0e21-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b0e21-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e21-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e21-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0e21-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b0e21-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b0e21-136">End of client support</span></span><br/>    | <span data-ttu-id="b0e21-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0e21-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b0e21-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b0e21-138">End of server support</span></span><br/>    | <span data-ttu-id="b0e21-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0e21-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b0e21-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0e21-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e21-141">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="b0e21-141">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="b0e21-142">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="b0e21-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="b0e21-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="b0e21-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="b0e21-144">**Reconnexion**</span><span class="sxs-lookup"><span data-stu-id="b0e21-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
