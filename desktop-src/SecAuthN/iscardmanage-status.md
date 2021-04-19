---
description: Obtient l’état actuel de la carte à puce ou du lecteur.
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: 'ISCardManage :: Status, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518419"
---
# <a name="iscardmanagestatus-method"></a><span data-ttu-id="974cb-103">ISCardManage :: Status, méthode</span><span class="sxs-lookup"><span data-stu-id="974cb-103">ISCardManage::Status method</span></span>

<span data-ttu-id="974cb-104">\[La méthode **Status** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="974cb-104">\[The **Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="974cb-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="974cb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="974cb-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="974cb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="974cb-107">La méthode **Status** obtient l’état actuel de la [*carte à puce*](../secgloss/s-gly.md) ou du [*lecteur*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="974cb-107">The **Status** method gets the current status of the [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="974cb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="974cb-108">Syntax</span></span>


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a><span data-ttu-id="974cb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="974cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="974cb-110">*pStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="974cb-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="974cb-111">Pointeur désignant une \_ valeur d’énumération des États cicatrices.</span><span class="sxs-lookup"><span data-stu-id="974cb-111">Pointer to an SCARD\_STATES enumeration value.</span></span> <span data-ttu-id="974cb-112">Au retour, contient l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="974cb-112">On return, contains the current status/state.</span></span>

</dd> <dt>

<span data-ttu-id="974cb-113">*pProtocols* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="974cb-113">*pProtocols* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="974cb-114">Pointeur vers une valeur d' \_ énumération de protocoles cicatrices.</span><span class="sxs-lookup"><span data-stu-id="974cb-114">Pointer to an SCARD\_PROTOCOLS enumeration value.</span></span> <span data-ttu-id="974cb-115">Au retour, contient le protocole en cours.</span><span class="sxs-lookup"><span data-stu-id="974cb-115">On return, contains the current protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="974cb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="974cb-116">Return value</span></span>

<span data-ttu-id="974cb-117">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="974cb-117">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="974cb-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="974cb-118">Return code</span></span>                                                                                   | <span data-ttu-id="974cb-119">Description</span><span class="sxs-lookup"><span data-stu-id="974cb-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="974cb-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="974cb-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="974cb-121">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="974cb-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="974cb-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="974cb-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="974cb-123">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="974cb-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="974cb-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="974cb-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="974cb-125">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="974cb-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="974cb-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="974cb-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="974cb-127">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="974cb-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="974cb-128">Notes</span><span class="sxs-lookup"><span data-stu-id="974cb-128">Remarks</span></span>

<span data-ttu-id="974cb-129">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="974cb-129">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="974cb-130">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="974cb-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="974cb-131">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="974cb-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="974cb-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="974cb-132">Requirements</span></span>



| <span data-ttu-id="974cb-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="974cb-133">Requirement</span></span> | <span data-ttu-id="974cb-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="974cb-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="974cb-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="974cb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="974cb-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="974cb-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="974cb-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="974cb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="974cb-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="974cb-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="974cb-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="974cb-139">End of client support</span></span><br/>    | <span data-ttu-id="974cb-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="974cb-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="974cb-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="974cb-141">End of server support</span></span><br/>    | <span data-ttu-id="974cb-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="974cb-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="974cb-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="974cb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="974cb-144">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="974cb-144">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
