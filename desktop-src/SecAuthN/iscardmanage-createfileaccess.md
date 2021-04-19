---
description: Crée une interface ISCardFileAccess.
ms.assetid: 06a5948f-c7bd-49bf-9032-f40f3d0d330c
title: 'ISCardManage :: CreateFileAccess, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3eb1f544e05959cc33119091268e1c7fe6266547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541951"
---
# <a name="iscardmanagecreatefileaccess-method"></a><span data-ttu-id="41edb-103">ISCardManage :: CreateFileAccess, méthode</span><span class="sxs-lookup"><span data-stu-id="41edb-103">ISCardManage::CreateFileAccess method</span></span>

<span data-ttu-id="41edb-104">\[La méthode **CreateFileAccess** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="41edb-104">\[The **CreateFileAccess** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="41edb-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="41edb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="41edb-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="41edb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="41edb-107">La méthode **CreateFileAccess** crée une interface [**ISCardFileAccess**](iscardfileaccess.md) .</span><span class="sxs-lookup"><span data-stu-id="41edb-107">The **CreateFileAccess** method creates an [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="41edb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41edb-108">Syntax</span></span>


```C++
HRESULT CreateFileAccess(
  [out] ISCardFileAccess **ppISCardFileAccess
);
```



## <a name="parameters"></a><span data-ttu-id="41edb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41edb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41edb-110">*ppISCardFileAccess* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="41edb-110">*ppISCardFileAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41edb-111">Renvoi d’un pointeur vers l’interface [**ISCardFileAccess**](iscardfileaccess.md) créée.</span><span class="sxs-lookup"><span data-stu-id="41edb-111">Returned pointer to the created [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41edb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41edb-112">Return value</span></span>

<span data-ttu-id="41edb-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="41edb-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="41edb-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="41edb-114">Return code</span></span>                                                                                   | <span data-ttu-id="41edb-115">Description</span><span class="sxs-lookup"><span data-stu-id="41edb-115">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="41edb-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41edb-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="41edb-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="41edb-117">Operation completed successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="41edb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="41edb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="41edb-119">Le paramètre *ppISCardFileAccess* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="41edb-119">The *ppISCardFileAccess* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="41edb-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="41edb-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="41edb-121">Un pointeur incorrect a été passé dans *ppISCardFileAccess*.</span><span class="sxs-lookup"><span data-stu-id="41edb-121">A bad pointer was passed in *ppISCardFileAccess*.</span></span><br/> |
| <dl> <span data-ttu-id="41edb-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="41edb-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="41edb-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="41edb-123">Out of memory.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="41edb-124">Notes</span><span class="sxs-lookup"><span data-stu-id="41edb-124">Remarks</span></span>

<span data-ttu-id="41edb-125">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="41edb-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="41edb-126">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="41edb-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="41edb-127">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="41edb-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41edb-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41edb-128">Requirements</span></span>



| <span data-ttu-id="41edb-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41edb-129">Requirement</span></span> | <span data-ttu-id="41edb-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="41edb-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41edb-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41edb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="41edb-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41edb-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="41edb-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41edb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="41edb-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41edb-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="41edb-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="41edb-135">End of client support</span></span><br/>    | <span data-ttu-id="41edb-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="41edb-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="41edb-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="41edb-137">End of server support</span></span><br/>    | <span data-ttu-id="41edb-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41edb-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="41edb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41edb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41edb-140">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="41edb-140">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="41edb-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="41edb-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
