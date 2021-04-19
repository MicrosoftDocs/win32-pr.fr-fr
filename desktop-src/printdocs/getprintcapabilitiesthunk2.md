---
description: Récupère les fonctionnalités d’imprimantes mises en forme en conformité avec le schéma d’impression XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523236"
---
# <a name="getprintcapabilitiesthunk2-function"></a><span data-ttu-id="26ac5-103">GetPrintCapabilitiesThunk2 fonction)</span><span class="sxs-lookup"><span data-stu-id="26ac5-103">GetPrintCapabilitiesThunk2 function</span></span>

<span data-ttu-id="26ac5-104">\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="26ac5-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="26ac5-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="26ac5-106">Récupère les fonctionnalités de l’imprimante mises en forme en conformité avec le [schéma d’impression](./printschema.md)XML.</span><span class="sxs-lookup"><span data-stu-id="26ac5-106">Retrieves the printer's capabilities formatted in compliance with the XML [Print Schema](./printschema.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="26ac5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ac5-107">Syntax</span></span>


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="26ac5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26ac5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ac5-109">*hProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ac5-110">Handle d’un fournisseur de tickets d’impression ouvert.</span><span class="sxs-lookup"><span data-stu-id="26ac5-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="26ac5-111">Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="26ac5-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="26ac5-112">*pPrintTicket* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ac5-113">Mémoire tampon qui contient les données du ticket d’impression, exprimées en XML, comme décrit dans le [schéma d’impression](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="26ac5-113">The buffer that contains the print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="26ac5-114">*cbPrintTicket* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-114">*cbPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ac5-115">Taille, en octets, de la mémoire tampon référencée par *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="26ac5-115">The size, in bytes, of the buffer referenced by *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="26ac5-116">*ppbPrintCapabilities* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-116">*ppbPrintCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26ac5-117">L’adresse de la mémoire tampon allouée par cette fonction et contient les informations de fonctionnalités d’impression valides, encodées au format XML.</span><span class="sxs-lookup"><span data-stu-id="26ac5-117">The address of the buffer that is allocated by this function and contains the valid print capabilities information, encoded as XML.</span></span> <span data-ttu-id="26ac5-118">Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="26ac5-118">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="26ac5-119">Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="26ac5-119">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="26ac5-120">*pcbPrintCapabilitiesLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-120">*pcbPrintCapabilitiesLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26ac5-121">Taille, en octets, de la mémoire tampon référencée par *ppbPrintCapabilities*.</span><span class="sxs-lookup"><span data-stu-id="26ac5-121">The size, in bytes, of the buffer referenced by *ppbPrintCapabilities*.</span></span>

</dd> <dt>

<span data-ttu-id="26ac5-122">*pbstrErrorMessage* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-122">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26ac5-123">Pointeur vers une chaîne qui spécifie ce qui, le cas échéant, n’est pas valide sur *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="26ac5-123">A pointer to a string that specifies what, if anything, is invalid about *pPrintTicket*.</span></span> <span data-ttu-id="26ac5-124">S’il est valide, cette valeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="26ac5-124">If it is valid, this value is **NULL**.</span></span> <span data-ttu-id="26ac5-125">Si *pbstrErrorMessage* n’a pas la **valeur null** lorsque la fonction retourne, l’appelant doit libérer la chaîne avec [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="26ac5-125">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ac5-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26ac5-126">Return value</span></span>

<span data-ttu-id="26ac5-127">Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26ac5-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="26ac5-128">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="26ac5-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26ac5-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ac5-129">Requirements</span></span>



| <span data-ttu-id="26ac5-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26ac5-130">Requirement</span></span> | <span data-ttu-id="26ac5-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ac5-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26ac5-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ac5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="26ac5-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="26ac5-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ac5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="26ac5-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ac5-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26ac5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="26ac5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26ac5-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26ac5-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ac5-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ac5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ac5-139">**PTGetPrintCapabilities**</span><span class="sxs-lookup"><span data-stu-id="26ac5-139">**PTGetPrintCapabilities**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[<span data-ttu-id="26ac5-140">Schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="26ac5-140">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="26ac5-141">Impression</span><span class="sxs-lookup"><span data-stu-id="26ac5-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="26ac5-142">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="26ac5-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

