---
description: Fusionne deux tickets d’impression et retourne un ticket d’impression valide et viable.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545858"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a><span data-ttu-id="3aaf4-103">MergeAndValidatePrintTicketThunk2 fonction)</span><span class="sxs-lookup"><span data-stu-id="3aaf4-103">MergeAndValidatePrintTicketThunk2 function</span></span>

<span data-ttu-id="3aaf4-104">\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="3aaf4-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="3aaf4-106">Fusionne deux tickets d’impression et retourne un ticket d’impression valide et viable.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-106">Merges two print tickets and returns a valid, viable print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aaf4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aaf4-107">Syntax</span></span>


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="3aaf4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3aaf4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aaf4-109">*hProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-110">Handle d’un fournisseur de tickets d’impression ouvert.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="3aaf4-111">Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="3aaf4-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-112">*pBasePrintTicket* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-112">*pBasePrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-113">Mémoire tampon qui contient les données de ticket d’impression de base, exprimées en XML, comme décrit dans le [schéma d’impression](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="3aaf4-113">The buffer that contains the base print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-114">*basePrintTicketLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-114">*basePrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-115">Taille, en octets, de la mémoire tampon référencée par *pBasePrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-115">The size, in bytes, of the buffer referenced by *pBasePrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-116">*pDeltaPrintTicket* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-116">*pDeltaPrintTicket* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-117">Mémoire tampon qui contient le ticket d’impression à fusionner.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-117">The buffer that contains the print ticket to merge.</span></span> <span data-ttu-id="3aaf4-118">Les données du ticket d’impression sont exprimées en XML, comme décrit dans le [schéma d’impression](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="3aaf4-118">The print ticket data is expressed in XML as described in the [Print Schema](./printschema.md).</span></span> <span data-ttu-id="3aaf4-119">La valeur de ce paramètre peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-119">The value of this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-120">*deltaPrintTicketLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-120">*deltaPrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-121">Taille, en octets, de la mémoire tampon référencée par *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-121">The size, in bytes, of the buffer referenced by *pDeltaPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-122">*étendue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-122">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-123">Valeur qui spécifie si l’étendue de *pDeltaPrintTicket* et *ppValidatedPrintTicket* est une page unique, un document entier ou tous les documents du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-123">The value that specifies whether the scope of *pDeltaPrintTicket* and *ppValidatedPrintTicket* is a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="3aaf4-124">La valeur de ce paramètre doit être un membre de l’énumération [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , castée en tant que valeur **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-124">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-125">*ppValidatedPrintTicket* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-125">*ppValidatedPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-126">Adresse de la mémoire tampon qui contient les tickets d’impression fusionnés et validés.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-126">The address of the buffer that contains the merged and validated print ticket.</span></span> <span data-ttu-id="3aaf4-127">Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-127">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="3aaf4-128">Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="3aaf4-128">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-129">*pValidatedPrintTicketLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-129">*pValidatedPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-130">Taille, en octets, de la mémoire tampon référencée par *ppValidatedPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-130">The size, in bytes, of the buffer referenced by *ppValidatedPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="3aaf4-131">*pbstrErrorMessage* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-131">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3aaf4-132">Pointeur vers une chaîne qui spécifie ce qui, le cas échéant, n’est pas valide concernant le ticket d’impression dans *pBasePrintTicket* ou *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-132">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pBasePrintTicket* or *pDeltaPrintTicket*.</span></span> <span data-ttu-id="3aaf4-133">Si elles sont toutes deux valides, cette valeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="3aaf4-133">If they are both valid, this value is **NULL**.</span></span> <span data-ttu-id="3aaf4-134">Si *pbstrErrorMessage* n’a pas la **valeur null** lorsque la fonction retourne, l’appelant doit libérer la chaîne avec [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="3aaf4-134">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aaf4-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3aaf4-135">Return value</span></span>

<span data-ttu-id="3aaf4-136">Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3aaf4-136">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="3aaf4-137">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="3aaf4-137">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3aaf4-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aaf4-138">Requirements</span></span>



| <span data-ttu-id="3aaf4-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aaf4-139">Requirement</span></span> | <span data-ttu-id="3aaf4-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aaf4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aaf4-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aaf4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3aaf4-142">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-142">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3aaf4-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aaf4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3aaf4-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3aaf4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3aaf4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aaf4-146"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aaf4-146"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aaf4-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aaf4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aaf4-148">Schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="3aaf4-148">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="3aaf4-149">**PTMergeAndValidatePrintTicket**</span><span class="sxs-lookup"><span data-stu-id="3aaf4-149">**PTMergeAndValidatePrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[<span data-ttu-id="3aaf4-150">Impression</span><span class="sxs-lookup"><span data-stu-id="3aaf4-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3aaf4-151">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="3aaf4-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

