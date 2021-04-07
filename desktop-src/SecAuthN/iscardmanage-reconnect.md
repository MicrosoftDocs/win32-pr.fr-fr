---
description: Permet à une application de se reconnecter à une carte à puce ou à un lecteur sans avoir à émettre un appel de détachement suivi par un appel de AttachByHandle ou AttachByIFD, respectivement.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'ISCardManage :: reconnect, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864046"
---
# <a name="iscardmanagereconnect-method"></a><span data-ttu-id="19339-103">ISCardManage :: reconnect, méthode</span><span class="sxs-lookup"><span data-stu-id="19339-103">ISCardManage::Reconnect method</span></span>

<span data-ttu-id="19339-104">\[La méthode de **reconnexion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="19339-104">\[The **Reconnect** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="19339-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="19339-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="19339-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="19339-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="19339-107">La méthode **reconnect** permet à une application de se reconnecter à une [*carte à puce*](../secgloss/s-gly.md) ou à un [*lecteur*](../secgloss/r-gly.md) sans avoir à émettre un appel de [**détachement**](iscardmanage-detach.md) suivi d’un appel [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="19339-107">The **Reconnect** method allows an application to reconnect to a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) without having to issue a [**Detach**](iscardmanage-detach.md) call followed by an [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) call respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="19339-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19339-108">Syntax</span></span>


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a><span data-ttu-id="19339-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19339-109">Parameters</span></span>

<span data-ttu-id="19339-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="19339-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19339-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19339-111">Return value</span></span>

<span data-ttu-id="19339-112">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="19339-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="19339-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="19339-113">Return code</span></span>                                                                                   | <span data-ttu-id="19339-114">Description</span><span class="sxs-lookup"><span data-stu-id="19339-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="19339-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19339-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="19339-116">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="19339-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="19339-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="19339-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="19339-118">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="19339-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="19339-119">Notes</span><span class="sxs-lookup"><span data-stu-id="19339-119">Remarks</span></span>

<span data-ttu-id="19339-120">Pour joindre un appel de carte à puce [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="19339-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="19339-121">Pour détacher une carte à puce, appelez [**détacher**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="19339-121">To detach a smart card, call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="19339-122">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="19339-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="19339-123">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="19339-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="19339-124">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="19339-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19339-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19339-125">Requirements</span></span>



| <span data-ttu-id="19339-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19339-126">Requirement</span></span> | <span data-ttu-id="19339-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="19339-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19339-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19339-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19339-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19339-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="19339-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19339-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19339-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19339-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="19339-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="19339-132">End of client support</span></span><br/>    | <span data-ttu-id="19339-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="19339-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="19339-134">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="19339-134">End of server support</span></span><br/>    | <span data-ttu-id="19339-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19339-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="19339-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19339-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19339-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="19339-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="19339-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="19339-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="19339-139">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="19339-139">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="19339-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="19339-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
