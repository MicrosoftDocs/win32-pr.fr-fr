---
description: Crée une interface ISCardVerify.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: 'ISCardManage :: CreateCHVerification, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a5909a8782571f9bd01a1c31e5ccd04c3d029df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210009"
---
# <a name="iscardmanagecreatechverification-method"></a><span data-ttu-id="773b7-103">ISCardManage :: CreateCHVerification, méthode</span><span class="sxs-lookup"><span data-stu-id="773b7-103">ISCardManage::CreateCHVerification method</span></span>

<span data-ttu-id="773b7-104">\[La méthode **CreateCHVerification** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="773b7-104">\[The **CreateCHVerification** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="773b7-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="773b7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="773b7-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="773b7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="773b7-107">La méthode **CreateCHVerification** crée une interface [**ISCardVerify**](iscardverify.md) .</span><span class="sxs-lookup"><span data-stu-id="773b7-107">The **CreateCHVerification** method creates an [**ISCardVerify**](iscardverify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="773b7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="773b7-108">Syntax</span></span>


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a><span data-ttu-id="773b7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="773b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="773b7-110">*ppISCardVerify* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="773b7-110">*ppISCardVerify* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="773b7-111">Renvoi d’un pointeur vers l’interface [**ISCardVerify**](iscardverify.md) créée.</span><span class="sxs-lookup"><span data-stu-id="773b7-111">Returned pointer to the created [**ISCardVerify**](iscardverify.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="773b7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="773b7-112">Return value</span></span>

<span data-ttu-id="773b7-113">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="773b7-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="773b7-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="773b7-114">Return code</span></span>                                                                                   | <span data-ttu-id="773b7-115">Description</span><span class="sxs-lookup"><span data-stu-id="773b7-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="773b7-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="773b7-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="773b7-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="773b7-117">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="773b7-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="773b7-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="773b7-119">Le paramètre *ppISCardVerify* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="773b7-119">The *ppISCardVerify* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="773b7-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="773b7-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="773b7-121">Un pointeur incorrect a été passé dans *ppISCardVerify*.</span><span class="sxs-lookup"><span data-stu-id="773b7-121">A bad pointer was passed in *ppISCardVerify*.</span></span><br/> |
| <dl> <span data-ttu-id="773b7-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="773b7-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="773b7-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="773b7-123">Out of memory.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="773b7-124">Notes</span><span class="sxs-lookup"><span data-stu-id="773b7-124">Remarks</span></span>

<span data-ttu-id="773b7-125">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="773b7-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="773b7-126">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="773b7-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="773b7-127">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="773b7-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="773b7-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="773b7-128">Requirements</span></span>



| <span data-ttu-id="773b7-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="773b7-129">Requirement</span></span> | <span data-ttu-id="773b7-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="773b7-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="773b7-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="773b7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="773b7-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="773b7-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="773b7-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="773b7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="773b7-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="773b7-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="773b7-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="773b7-135">End of client support</span></span><br/>    | <span data-ttu-id="773b7-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="773b7-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="773b7-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="773b7-137">End of server support</span></span><br/>    | <span data-ttu-id="773b7-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="773b7-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="773b7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="773b7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773b7-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="773b7-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="773b7-141">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="773b7-141">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
