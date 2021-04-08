---
description: Remplace le code des IVT en cours (vérification du détenteur de la carte) par le nouveau code IVT.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'ISCardVerify :: ChangeCode, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757018"
---
# <a name="iscardverifychangecode-method"></a><span data-ttu-id="b8982-103">ISCardVerify :: ChangeCode, méthode</span><span class="sxs-lookup"><span data-stu-id="b8982-103">ISCardVerify::ChangeCode method</span></span>

<span data-ttu-id="b8982-104">\[La méthode **ChangeCode** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b8982-104">\[The **ChangeCode** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b8982-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b8982-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b8982-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="b8982-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b8982-107">La méthode **ChangeCode** remplace le code IVT actuel (vérification du détenteur de la carte) par le nouveau code IVT.</span><span class="sxs-lookup"><span data-stu-id="b8982-107">The **ChangeCode** method replaces the current CHV (card holder verification) code with new CHV code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8982-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8982-108">Syntax</span></span>


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="b8982-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8982-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8982-110">*pOldCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8982-110">*pOldCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8982-111">Pointeur vers un [**IByteBuffer**](ibytebuffer.md) contenant le code actuel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b8982-111">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the user's current code.</span></span>

</dd> <dt>

<span data-ttu-id="b8982-112">*pNewCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8982-112">*pNewCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8982-113">Pointeur vers un [**IByteBuffer**](ibytebuffer.md) contenant le nouveau code qui sera présenté à la [*carte à puce*](../secgloss/s-gly.md) pendant le processus de modification pour authentifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b8982-113">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the new code that will be presented to the [*smart card*](../secgloss/s-gly.md) during the change process to authenticate the user.</span></span>

</dd> <dt>

<span data-ttu-id="b8982-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b8982-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8982-115">Indique si le code est global ou local, et si le code doit être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="b8982-115">Indicates whether the code is global or local, and whether the code should be enabled or disabled.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="b8982-116">**SC \_ FL \_ IHV \_ global**</span><span class="sxs-lookup"><span data-stu-id="b8982-116">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="b8982-117">**SC \_ FL \_ IHV \_ local**</span><span class="sxs-lookup"><span data-stu-id="b8982-117">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

<span data-ttu-id="b8982-118">**activation de SC \_ FL \_ IHV \_**</span><span class="sxs-lookup"><span data-stu-id="b8982-118">**SC\_FL\_IHV\_ENABLE**</span></span>
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

<span data-ttu-id="b8982-119">**désactivation de SC \_ FL \_ IHV \_**</span><span class="sxs-lookup"><span data-stu-id="b8982-119">**SC\_FL\_IHV\_DISABLE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b8982-120">*lRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8982-120">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8982-121">Référence spécifique à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="b8982-121">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8982-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8982-122">Return value</span></span>

<span data-ttu-id="b8982-123">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8982-123">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b8982-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b8982-124">Return code</span></span>                                                                                   | <span data-ttu-id="b8982-125">Description</span><span class="sxs-lookup"><span data-stu-id="b8982-125">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b8982-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8982-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b8982-127">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b8982-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b8982-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b8982-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b8982-129">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="b8982-129">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="b8982-130"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b8982-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b8982-131">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="b8982-131">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="b8982-132"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="b8982-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b8982-133">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="b8982-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b8982-134">Notes</span><span class="sxs-lookup"><span data-stu-id="b8982-134">Remarks</span></span>

<span data-ttu-id="b8982-135">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="b8982-135">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="b8982-136">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="b8982-136">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b8982-137">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b8982-137">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8982-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8982-138">Requirements</span></span>



| <span data-ttu-id="b8982-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8982-139">Requirement</span></span> | <span data-ttu-id="b8982-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8982-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8982-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8982-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b8982-142">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8982-142">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b8982-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8982-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b8982-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8982-144">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b8982-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b8982-145">End of client support</span></span><br/>    | <span data-ttu-id="b8982-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8982-146">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b8982-147">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b8982-147">End of server support</span></span><br/>    | <span data-ttu-id="b8982-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8982-148">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b8982-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8982-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8982-150">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="b8982-150">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> <dt>

[<span data-ttu-id="b8982-151">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="b8982-151">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

[<span data-ttu-id="b8982-152">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="b8982-152">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
