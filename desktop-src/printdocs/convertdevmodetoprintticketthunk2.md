---
description: Convertit une structure DEVMODE en un ticket d’impression.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524631"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a><span data-ttu-id="f8844-103">ConvertDevModeToPrintTicketThunk2 fonction)</span><span class="sxs-lookup"><span data-stu-id="f8844-103">ConvertDevModeToPrintTicketThunk2 function</span></span>

<span data-ttu-id="f8844-104">\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8844-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="f8844-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]</span><span class="sxs-lookup"><span data-stu-id="f8844-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="f8844-106">Convertit une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un ticket d’impression.</span><span class="sxs-lookup"><span data-stu-id="f8844-106">Converts a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to a print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8844-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8844-107">Syntax</span></span>


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a><span data-ttu-id="f8844-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8844-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8844-109">*hProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8844-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8844-110">Handle d’un fournisseur de tickets d’impression ouvert.</span><span class="sxs-lookup"><span data-stu-id="f8844-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="f8844-111">Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="f8844-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f8844-112">*pDevmode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8844-112">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8844-113">Pointeur vers le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) à convertir.</span><span class="sxs-lookup"><span data-stu-id="f8844-113">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to convert.</span></span>

</dd> <dt>

<span data-ttu-id="f8844-114">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8844-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8844-115">Taille, en octets, du [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passé dans *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="f8844-115">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="f8844-116">*étendue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8844-116">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8844-117">Valeur qui spécifie la portée de *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f8844-117">A value that specifies the scope of *ppPrintTicket*.</span></span> <span data-ttu-id="f8844-118">Cette valeur peut spécifier une page unique, un document entier ou tous les documents du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="f8844-118">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="f8844-119">La valeur de ce paramètre doit être un membre de l’énumération [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , castée en tant que valeur **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f8844-119">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="f8844-120">*ppPrintTicket* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8844-120">*ppPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8844-121">Adresse de la mémoire tampon qui contient un ticket d’impression qui représente le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passé dans *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="f8844-121">The address of the buffer that contains a print ticket that represents the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span> <span data-ttu-id="f8844-122">Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f8844-122">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="f8844-123">Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f8844-123">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="f8844-124">*pcbPrintTicketLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8844-124">*pcbPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8844-125">Taille, en octets, du ticket d’impression retourné dans *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f8844-125">The size, in bytes, of the print ticket returned in *ppPrintTicket*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8844-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8844-126">Return value</span></span>

<span data-ttu-id="f8844-127">Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8844-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="f8844-128">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f8844-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8844-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8844-129">Requirements</span></span>



| <span data-ttu-id="f8844-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8844-130">Requirement</span></span> | <span data-ttu-id="f8844-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8844-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8844-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8844-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f8844-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8844-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f8844-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8844-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f8844-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8844-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f8844-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f8844-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8844-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8844-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8844-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8844-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8844-139">Schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f8844-139">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="f8844-140">**PTConvertDevModeToPrintTicket**</span><span class="sxs-lookup"><span data-stu-id="f8844-140">**PTConvertDevModeToPrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[<span data-ttu-id="f8844-141">Impression</span><span class="sxs-lookup"><span data-stu-id="f8844-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8844-142">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f8844-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

