---
description: Rend un fichier (EF ou DF) qui a été précédemment rendu non valide à l’aide de la méthode Invalidate, accessible par l’application.
ms.assetid: 1906fcc5-ae76-4950-b2eb-e5ce1882637f
title: 'ISCardFileAccess :: rehabilite, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Rehabilitate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7ed02131de08104dab8aff23ee9054659fd4cd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521591"
---
# <a name="iscardfileaccessrehabilitate-method"></a><span data-ttu-id="bdbec-103">ISCardFileAccess :: rehabilite, méthode</span><span class="sxs-lookup"><span data-stu-id="bdbec-103">ISCardFileAccess::Rehabilitate method</span></span>

<span data-ttu-id="bdbec-104">\[La **méthode de** réutilisation peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="bdbec-104">\[The **Rehabilitate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bdbec-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bdbec-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bdbec-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bdbec-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bdbec-107">La **méthode de** réutilisation rend un fichier (EF ou DF) qui a été précédemment rendu non valide à l’aide de la méthode [**Invalidate**](iscardfileaccess-invalidate.md) , accessible par l’application.</span><span class="sxs-lookup"><span data-stu-id="bdbec-107">The **Rehabilitate** method makes a file (EF or DF) that was previously made not valid by using the [**Invalidate**](iscardfileaccess-invalidate.md) method, accessible by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbec-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdbec-108">Syntax</span></span>


```C++
HRESULT Rehabilitate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="bdbec-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdbec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbec-110">*bstrPathSpec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdbec-110">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbec-111">Fichier à réhabiliter.</span><span class="sxs-lookup"><span data-stu-id="bdbec-111">File to rehabilitate.</span></span>

</dd> <dt>

<span data-ttu-id="bdbec-112">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdbec-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbec-113">Spécifie si la messagerie sécurisée doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bdbec-113">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="bdbec-114">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="bdbec-114">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbec-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdbec-115">Return value</span></span>

<span data-ttu-id="bdbec-116">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="bdbec-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bdbec-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bdbec-117">Return code</span></span>                                                                                   | <span data-ttu-id="bdbec-118">Description</span><span class="sxs-lookup"><span data-stu-id="bdbec-118">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bdbec-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbec-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bdbec-120">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bdbec-120">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bdbec-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbec-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bdbec-122">Un paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bdbec-122">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="bdbec-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbec-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bdbec-124">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="bdbec-124">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="bdbec-125">Notes</span><span class="sxs-lookup"><span data-stu-id="bdbec-125">Remarks</span></span>

<span data-ttu-id="bdbec-126">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="bdbec-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="bdbec-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="bdbec-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bdbec-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bdbec-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdbec-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdbec-129">Requirements</span></span>



| <span data-ttu-id="bdbec-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdbec-130">Requirement</span></span> | <span data-ttu-id="bdbec-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdbec-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bdbec-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdbec-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bdbec-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdbec-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bdbec-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdbec-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bdbec-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdbec-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bdbec-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bdbec-136">End of client support</span></span><br/>    | <span data-ttu-id="bdbec-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bdbec-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="bdbec-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bdbec-138">End of server support</span></span><br/>    | <span data-ttu-id="bdbec-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bdbec-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="bdbec-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdbec-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbec-141">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="bdbec-141">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)
</dt> <dt>

[<span data-ttu-id="bdbec-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="bdbec-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
