---
description: Crée un lien de communication vers un lecteur, à l’aide d’un nom d’affichage fourni pour le lecteur.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'ISCardManage :: AttachByIFD, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522709"
---
# <a name="iscardmanageattachbyifd-method"></a><span data-ttu-id="25514-103">ISCardManage :: AttachByIFD, méthode</span><span class="sxs-lookup"><span data-stu-id="25514-103">ISCardManage::AttachByIFD method</span></span>

<span data-ttu-id="25514-104">\[La méthode **AttachByIFD** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="25514-104">\[The **AttachByIFD** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="25514-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="25514-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="25514-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="25514-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="25514-107">La méthode **AttachByIFD** crée un lien de communication vers un [*lecteur*](../secgloss/r-gly.md), à l’aide d’un nom d’affichage fourni pour le lecteur.</span><span class="sxs-lookup"><span data-stu-id="25514-107">The **AttachByIFD** method creates a communication link to a [*reader*](../secgloss/r-gly.md), using a supplied display name for the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="25514-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25514-108">Syntax</span></span>


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a><span data-ttu-id="25514-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25514-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25514-110">*bstrIFDName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25514-110">*bstrIFDName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25514-111">Nom complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="25514-111">The display name of the reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25514-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25514-112">Return value</span></span>

<span data-ttu-id="25514-113">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="25514-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="25514-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="25514-114">Return code</span></span>                                                                                   | <span data-ttu-id="25514-115">Description</span><span class="sxs-lookup"><span data-stu-id="25514-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="25514-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25514-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="25514-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="25514-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="25514-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="25514-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="25514-119">Le paramètre *bstrIFDName* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="25514-119">The *bstrIFDName* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="25514-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="25514-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="25514-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="25514-121">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="25514-122">Notes</span><span class="sxs-lookup"><span data-stu-id="25514-122">Remarks</span></span>

<span data-ttu-id="25514-123">Pour joindre un appel de [*carte à puce*](../secgloss/s-gly.md) [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span><span class="sxs-lookup"><span data-stu-id="25514-123">To attach a [*smart card*](../secgloss/s-gly.md) call [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span></span>

<span data-ttu-id="25514-124">Pour libérer le [**détachement**](iscardmanage-detach.md)d’un appel de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="25514-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="25514-125">Pour vous reconnecter à la carte à puce sans appeler [**Detach**](iscardmanage-detach.md) et **AttachByIFD**, appelez [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="25514-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByIFD**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="25514-126">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="25514-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="25514-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="25514-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="25514-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="25514-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25514-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25514-129">Requirements</span></span>



| <span data-ttu-id="25514-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25514-130">Requirement</span></span> | <span data-ttu-id="25514-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="25514-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25514-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25514-132">Minimum supported client</span></span><br/> | <span data-ttu-id="25514-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25514-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="25514-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25514-134">Minimum supported server</span></span><br/> | <span data-ttu-id="25514-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25514-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="25514-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="25514-136">End of client support</span></span><br/>    | <span data-ttu-id="25514-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="25514-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="25514-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="25514-138">End of server support</span></span><br/>    | <span data-ttu-id="25514-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25514-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="25514-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25514-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25514-141">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="25514-141">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="25514-142">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="25514-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="25514-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="25514-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="25514-144">**Reconnexion**</span><span class="sxs-lookup"><span data-stu-id="25514-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
