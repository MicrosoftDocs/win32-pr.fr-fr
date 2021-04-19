---
description: Rend le fichier spécifié (EF ou DF) non valide. Les autres méthodes ne peuvent pas accéder à un fichier qui n’est pas valide avant d’utiliser la réutilisation.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'ISCardFileAccess :: Invalidate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534672"
---
# <a name="iscardfileaccessinvalidate-method"></a><span data-ttu-id="872a8-104">ISCardFileAccess :: Invalidate, méthode</span><span class="sxs-lookup"><span data-stu-id="872a8-104">ISCardFileAccess::Invalidate method</span></span>

<span data-ttu-id="872a8-105">\[La méthode **Invalidate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="872a8-105">\[The **Invalidate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="872a8-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="872a8-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="872a8-107">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="872a8-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="872a8-108">La méthode **Invalidate** rend le fichier spécifié (EF ou DF) non valide.</span><span class="sxs-lookup"><span data-stu-id="872a8-108">The **Invalidate** method makes the specified file (EF or DF) not valid.</span></span> <span data-ttu-id="872a8-109">Les autres méthodes ne peuvent pas accéder à un fichier qui n’est pas valide avant [**d’utiliser la**](iscardfileaccess-rehabilitate.md)réutilisation.</span><span class="sxs-lookup"><span data-stu-id="872a8-109">A file that is not valid cannot be accessed by other methods prior to using [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="872a8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="872a8-110">Syntax</span></span>


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="872a8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="872a8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872a8-112">*bstrPathSpec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="872a8-112">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872a8-113">Fichier.</span><span class="sxs-lookup"><span data-stu-id="872a8-113">File.</span></span>

</dd> <dt>

<span data-ttu-id="872a8-114">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="872a8-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872a8-115">Spécifie si la messagerie sécurisée doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="872a8-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="872a8-116">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="872a8-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="872a8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="872a8-117">Return value</span></span>

<span data-ttu-id="872a8-118">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="872a8-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="872a8-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="872a8-119">Return code</span></span>                                                                                   | <span data-ttu-id="872a8-120">Description</span><span class="sxs-lookup"><span data-stu-id="872a8-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="872a8-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="872a8-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="872a8-122">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="872a8-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="872a8-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="872a8-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="872a8-124">Un paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="872a8-124">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="872a8-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="872a8-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="872a8-126">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="872a8-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="872a8-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="872a8-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="872a8-128">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="872a8-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="872a8-129">Notes</span><span class="sxs-lookup"><span data-stu-id="872a8-129">Remarks</span></span>

<span data-ttu-id="872a8-130">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="872a8-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="872a8-131">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="872a8-131">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="872a8-132">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="872a8-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="872a8-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="872a8-133">Requirements</span></span>



| <span data-ttu-id="872a8-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="872a8-134">Requirement</span></span> | <span data-ttu-id="872a8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="872a8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="872a8-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="872a8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="872a8-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="872a8-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="872a8-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="872a8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="872a8-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="872a8-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="872a8-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="872a8-140">End of client support</span></span><br/>    | <span data-ttu-id="872a8-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="872a8-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="872a8-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="872a8-142">End of server support</span></span><br/>    | <span data-ttu-id="872a8-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="872a8-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="872a8-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="872a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872a8-145">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="872a8-145">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="872a8-146">**Réhabiliter**</span><span class="sxs-lookup"><span data-stu-id="872a8-146">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
