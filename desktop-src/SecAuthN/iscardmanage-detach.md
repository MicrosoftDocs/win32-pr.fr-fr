---
description: Libère la pièce jointe d’une carte à puce ou d’un lecteur spécifique allouée respectivement par AttachByHandle et AttachByIFD.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: ISCardManage ::D méthode Etach
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114538"
---
# <a name="iscardmanagedetach-method"></a><span data-ttu-id="bbc2c-103">ISCardManage ::D méthode Etach</span><span class="sxs-lookup"><span data-stu-id="bbc2c-103">ISCardManage::Detach method</span></span>

<span data-ttu-id="bbc2c-104">\[La méthode de **détachement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="bbc2c-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bbc2c-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bbc2c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bbc2c-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bbc2c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bbc2c-107">La méthode **Detach** libère l’attachement à une [*carte à puce*](../secgloss/s-gly.md) ou à un [*lecteur*](../secgloss/r-gly.md) spécifique, respectivement alloué par [**AttachByHandle**](iscardmanage-attachbyhandle.md) et [**AttachByIFD**](iscardmanage-attachbyifd.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc2c-107">The **Detach** method releases the attachment to a particular [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) and [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc2c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbc2c-108">Syntax</span></span>


```C++
HRESULT Detach();
```



## <a name="parameters"></a><span data-ttu-id="bbc2c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbc2c-109">Parameters</span></span>

<span data-ttu-id="bbc2c-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bbc2c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbc2c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbc2c-111">Return value</span></span>

<span data-ttu-id="bbc2c-112">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="bbc2c-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="bbc2c-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bbc2c-113">Return code</span></span>                                                                                   | <span data-ttu-id="bbc2c-114">Description</span><span class="sxs-lookup"><span data-stu-id="bbc2c-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bbc2c-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc2c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bbc2c-116">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bbc2c-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bbc2c-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc2c-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bbc2c-118">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="bbc2c-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="bbc2c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="bbc2c-119">Remarks</span></span>

<span data-ttu-id="bbc2c-120">Pour joindre un appel de carte à puce [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="bbc2c-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="bbc2c-121">Pour vous reconnecter à la carte à puce sans appeler **Detach** et [**AttachByHandle**](iscardmanage-attachbyhandle.md), appelez [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="bbc2c-121">To reconnect with the smart card without calling **Detach** and [**AttachByHandle**](iscardmanage-attachbyhandle.md), call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="bbc2c-122">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="bbc2c-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="bbc2c-123">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="bbc2c-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bbc2c-124">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bbc2c-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc2c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbc2c-125">Requirements</span></span>



| <span data-ttu-id="bbc2c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbc2c-126">Requirement</span></span> | <span data-ttu-id="bbc2c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbc2c-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbc2c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbc2c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc2c-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbc2c-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bbc2c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbc2c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc2c-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbc2c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bbc2c-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bbc2c-132">End of client support</span></span><br/>    | <span data-ttu-id="bbc2c-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbc2c-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="bbc2c-134">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bbc2c-134">End of server support</span></span><br/>    | <span data-ttu-id="bbc2c-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bbc2c-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="bbc2c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbc2c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc2c-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="bbc2c-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="bbc2c-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="bbc2c-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="bbc2c-139">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="bbc2c-139">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="bbc2c-140">**Reconnexion**</span><span class="sxs-lookup"><span data-stu-id="bbc2c-140">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
