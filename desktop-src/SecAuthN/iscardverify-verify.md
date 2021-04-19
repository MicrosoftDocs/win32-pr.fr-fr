---
description: Demande une vérification de l’utilisateur.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'ISCardVerify :: Verify, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518667"
---
# <a name="iscardverifyverify-method"></a><span data-ttu-id="3a7eb-103">ISCardVerify :: Verify, méthode</span><span class="sxs-lookup"><span data-stu-id="3a7eb-103">ISCardVerify::Verify method</span></span>

<span data-ttu-id="3a7eb-104">\[La méthode **verify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3a7eb-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3a7eb-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3a7eb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3a7eb-107">La méthode **verify** demande une vérification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-107">The **Verify** method requests a verification of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a7eb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a7eb-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="3a7eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a7eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a7eb-110">*pcode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a7eb-110">*pCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a7eb-111">Contient le code à présenter à la [*carte à puce*](../secgloss/s-gly.md) dans le processus des IVT (vérification du détenteur de la carte).</span><span class="sxs-lookup"><span data-stu-id="3a7eb-111">Contains the code to be presented to the [*smart card*](../secgloss/s-gly.md) in the CHV (card holder verification) process.</span></span>

</dd> <dt>

<span data-ttu-id="3a7eb-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3a7eb-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a7eb-113">Indique si le code est global ou local.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-113">Indicates whether the code is global or local.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="3a7eb-114">**SC \_ FL \_ IHV \_ global**</span><span class="sxs-lookup"><span data-stu-id="3a7eb-114">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="3a7eb-115">**SC \_ FL \_ IHV \_ local**</span><span class="sxs-lookup"><span data-stu-id="3a7eb-115">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3a7eb-116">*lRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a7eb-116">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a7eb-117">Référence spécifique à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-117">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a7eb-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a7eb-118">Return value</span></span>

<span data-ttu-id="3a7eb-119">La méthode **verify** retourne l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a7eb-119">The **Verify** method returns one of the following values:</span></span>



| <span data-ttu-id="3a7eb-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3a7eb-120">Return code</span></span>                                                                                   | <span data-ttu-id="3a7eb-121">Description</span><span class="sxs-lookup"><span data-stu-id="3a7eb-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3a7eb-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7eb-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3a7eb-123">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3a7eb-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7eb-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3a7eb-125">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3a7eb-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7eb-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3a7eb-127">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3a7eb-128"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7eb-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3a7eb-129">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3a7eb-130">Notes</span><span class="sxs-lookup"><span data-stu-id="3a7eb-130">Remarks</span></span>

<span data-ttu-id="3a7eb-131">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="3a7eb-131">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="3a7eb-132">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="3a7eb-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3a7eb-133">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3a7eb-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a7eb-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a7eb-134">Requirements</span></span>



| <span data-ttu-id="3a7eb-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a7eb-135">Requirement</span></span> | <span data-ttu-id="3a7eb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a7eb-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a7eb-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a7eb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3a7eb-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a7eb-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3a7eb-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a7eb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3a7eb-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a7eb-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3a7eb-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3a7eb-141">End of client support</span></span><br/>    | <span data-ttu-id="3a7eb-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a7eb-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3a7eb-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3a7eb-143">End of server support</span></span><br/>    | <span data-ttu-id="3a7eb-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3a7eb-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3a7eb-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a7eb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a7eb-146">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="3a7eb-146">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
