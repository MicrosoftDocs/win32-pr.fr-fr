---
description: Convertit un ticket d’impression en une structure DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034887"
---
# <a name="convertprinttickettodevmodethunk2-function"></a><span data-ttu-id="f07a6-103">ConvertPrintTicketToDevModeThunk2 fonction)</span><span class="sxs-lookup"><span data-stu-id="f07a6-103">ConvertPrintTicketToDevModeThunk2 function</span></span>

<span data-ttu-id="f07a6-104">\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="f07a6-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="f07a6-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="f07a6-106">Convertit un ticket d’impression en une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="f07a6-106">Converts a print ticket to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f07a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f07a6-107">Syntax</span></span>


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a><span data-ttu-id="f07a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f07a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f07a6-109">*hProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-110">Handle d’un fournisseur de tickets d’impression ouvert.</span><span class="sxs-lookup"><span data-stu-id="f07a6-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="f07a6-111">Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="f07a6-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f07a6-112">*pPrintTicket* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-113">Mémoire tampon qui contient le ticket d’impression à convertir.</span><span class="sxs-lookup"><span data-stu-id="f07a6-113">The buffer that contains the print ticket to convert.</span></span>

</dd> <dt>

<span data-ttu-id="f07a6-114">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-115">Taille, en octets, de la mémoire tampon passée dans *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f07a6-115">The size, in bytes, of the buffer passed in *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="f07a6-116">*BaseType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-116">*baseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-117">Valeur indiquant si le [**DEVMODE par défaut**](/windows/win32/api/wingdi/ns-wingdi-devmodea) de l’utilisateur ou le **DEVMODE** par défaut de la file d’attente à l’impression est utilisé pour fournir des valeurs au **DEVMODE** de sortie lorsque *pPrintTicket* ne spécifie pas tous les paramètres possibles pour un **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="f07a6-117">A value indicating whether the user's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) or the print queue's default **DEVMODE** is used to provide values to the output **DEVMODE** when *pPrintTicket* does not specify every possible setting for a **DEVMODE**.</span></span> <span data-ttu-id="f07a6-118">La valeur de ce paramètre doit être un membre de l’énumération [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , castée en **int**.</span><span class="sxs-lookup"><span data-stu-id="f07a6-118">The value of this parameter must be a member of the [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) enumeration, cast as an **INT**.</span></span>

</dd> <dt>

<span data-ttu-id="f07a6-119">*étendue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-119">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-120">Valeur qui spécifie la portée de *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f07a6-120">A value that specifies the scope of *pPrintTicket*.</span></span> <span data-ttu-id="f07a6-121">Cette valeur peut spécifier une page unique, un document entier ou tous les documents du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="f07a6-121">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="f07a6-122">La valeur de ce paramètre doit être un membre de l’énumération [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , castée en tant que valeur **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f07a6-122">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="f07a6-123">*ppDevmode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-123">*ppDevmode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-124">Adresse de la [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="f07a6-124">The address of the newly created [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span> <span data-ttu-id="f07a6-125">Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f07a6-125">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="f07a6-126">Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f07a6-126">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="f07a6-127">*pcbDevModeLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-127">*pcbDevModeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-128">Taille, en octets, du [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retourné dans *ppDevmode*.</span><span class="sxs-lookup"><span data-stu-id="f07a6-128">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) returned in *ppDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="f07a6-129"> le \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-129">*errMsg* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f07a6-130">Pointeur vers une chaîne qui spécifie ce qui, le cas échéant, n’est pas valide concernant le ticket d’impression dans *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f07a6-130">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pPrintTicket*.</span></span> <span data-ttu-id="f07a6-131">S’il est valide, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="f07a6-131">If it is valid, this is **NULL**.</span></span> <span data-ttu-id="f07a6-132">Si *l'* appel de la fonction n’est pas **null** lorsque la fonction retourne, l’appelant doit libérer la chaîne avec [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="f07a6-132">If *errMsg* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f07a6-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f07a6-133">Return value</span></span>

<span data-ttu-id="f07a6-134">Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f07a6-134">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="f07a6-135">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f07a6-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f07a6-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f07a6-136">Requirements</span></span>



| <span data-ttu-id="f07a6-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f07a6-137">Requirement</span></span> | <span data-ttu-id="f07a6-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="f07a6-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f07a6-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f07a6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f07a6-140">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-140">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f07a6-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f07a6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f07a6-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f07a6-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f07a6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f07a6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f07a6-144"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f07a6-144"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f07a6-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f07a6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f07a6-146">Schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f07a6-146">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="f07a6-147">**PTConvertPrintTicketToDevMode**</span><span class="sxs-lookup"><span data-stu-id="f07a6-147">**PTConvertPrintTicketToDevMode**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[<span data-ttu-id="f07a6-148">Impression</span><span class="sxs-lookup"><span data-stu-id="f07a6-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f07a6-149">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f07a6-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

