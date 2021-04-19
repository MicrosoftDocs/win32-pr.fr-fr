---
title: IVMHostInfo ProcessorFeaturesString, propriété (VPCCOMInterfaces. h)
description: Récupère la liste des fonctionnalités prises en charge par le processeur hôte.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- ProcessorFeaturesString propriété Virtual PC
- ProcessorFeaturesString, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511119"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a><span data-ttu-id="d1769-106">IVMHostInfo ::P propriété rocessorFeaturesString</span><span class="sxs-lookup"><span data-stu-id="d1769-106">IVMHostInfo::ProcessorFeaturesString property</span></span>

<span data-ttu-id="d1769-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1769-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1769-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1769-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1769-109">Récupère la liste des fonctionnalités prises en charge par le processeur hôte.</span><span class="sxs-lookup"><span data-stu-id="d1769-109">Retrieves the list features supported by the host processor.</span></span>

<span data-ttu-id="d1769-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d1769-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1769-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1769-111">Syntax</span></span>


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a><span data-ttu-id="d1769-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d1769-112">Property value</span></span>

<span data-ttu-id="d1769-113">Liste de fonctionnalités délimitées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d1769-113">A comma-delimited list of features.</span></span> <span data-ttu-id="d1769-114">Par exemple : « MMX, SSE, SSE2, x86-64 ».</span><span class="sxs-lookup"><span data-stu-id="d1769-114">An example would be "MMX,SSE,SSE2,x86-64".</span></span>



| <span data-ttu-id="d1769-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1769-115">Value</span></span>                                                                                 | <span data-ttu-id="d1769-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d1769-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1769-117"><dt>« AMD-V »</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-117"><dt>"AMD-V"</dt></span></span> </dl>    | <span data-ttu-id="d1769-118">Prend en charge les extensions de virtualisation AMD.</span><span class="sxs-lookup"><span data-stu-id="d1769-118">Supports the AMD Virtualization extensions.</span></span><br/>              |
| <dl> <span data-ttu-id="d1769-119"><dt>« Intel VT »</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-119"><dt>"Intel VT"</dt></span></span> </dl> | <span data-ttu-id="d1769-120">Prend en charge les extensions de la technologie de virtualisation Intel.</span><span class="sxs-lookup"><span data-stu-id="d1769-120">Supports the Intel Virtualization Technology extensions.</span></span><br/> |
| <dl> <span data-ttu-id="d1769-121"><dt>"HAVD"</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-121"><dt>"HAVD"</dt></span></span> </dl>     | <span data-ttu-id="d1769-122">La virtualisation d’assistance matérielle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="d1769-122">Hardware Assisted Virtualization is disabled.</span></span><br/>            |
| <dl> <span data-ttu-id="d1769-123"><dt>AVEZ</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-123"><dt>"HAVE"</dt></span></span> </dl>     | <span data-ttu-id="d1769-124">La virtualisation d’assistance matérielle est activée.</span><span class="sxs-lookup"><span data-stu-id="d1769-124">Hardware Assisted Virtualization is enabled.</span></span><br/>             |
| <dl> <span data-ttu-id="d1769-125"><dt>TECHNOLOGIE</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-125"><dt>"MMX"</dt></span></span> </dl>      | <span data-ttu-id="d1769-126">Prend en charge les extensions MMX.</span><span class="sxs-lookup"><span data-stu-id="d1769-126">Supports the MMX extensions.</span></span><br/>                             |
| <dl> <span data-ttu-id="d1769-127"><dt>SSE</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-127"><dt>"SSE"</dt></span></span> </dl>      | <span data-ttu-id="d1769-128">Prend en charge les extensions streaming SIMD.</span><span class="sxs-lookup"><span data-stu-id="d1769-128">Supports the Streaming SIMD Extensions.</span></span><br/>                  |
| <dl> <span data-ttu-id="d1769-129"><dt>SSE2</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-129"><dt>"SSE2"</dt></span></span> </dl>     | <span data-ttu-id="d1769-130">Prend en charge les extensions streaming SIMD 2.</span><span class="sxs-lookup"><span data-stu-id="d1769-130">Supports the Streaming SIMD Extensions 2.</span></span><br/>                |
| <dl> <span data-ttu-id="d1769-131"><dt>SSE3</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-131"><dt>"SSE3"</dt></span></span> </dl>     | <span data-ttu-id="d1769-132">Prend en charge les extensions streaming SIMD 3.</span><span class="sxs-lookup"><span data-stu-id="d1769-132">Supports the Streaming SIMD Extensions 3.</span></span><br/>                |
| <dl> <span data-ttu-id="d1769-133"><dt>"TXTE"</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-133"><dt>"TXTE"</dt></span></span> </dl>     | <span data-ttu-id="d1769-134">Prend en charge les extensions de la technologie d’exécution de confiance.</span><span class="sxs-lookup"><span data-stu-id="d1769-134">Supports the Trusted Execution Technology extensions.</span></span><br/>    |
| <dl> <span data-ttu-id="d1769-135"><dt>« x86-64 »</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-135"><dt>"x86-64"</dt></span></span> </dl>   | <span data-ttu-id="d1769-136">Prend en charge les extensions x86-64.</span><span class="sxs-lookup"><span data-stu-id="d1769-136">Supports x86-64 extensions.</span></span><br/>                              |



 

## <a name="error-codes"></a><span data-ttu-id="d1769-137">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d1769-137">Error codes</span></span>



| <span data-ttu-id="d1769-138">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="d1769-138">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d1769-139">Signification</span><span class="sxs-lookup"><span data-stu-id="d1769-139">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d1769-140"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-140"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d1769-141">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d1769-141">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d1769-142"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-142"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d1769-143">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d1769-143">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d1769-144"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-144"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d1769-145">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d1769-145">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d1769-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1769-146">Requirements</span></span>



| <span data-ttu-id="d1769-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1769-147">Requirement</span></span> | <span data-ttu-id="d1769-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1769-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1769-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1769-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d1769-150">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1769-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1769-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1769-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d1769-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1769-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1769-153">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d1769-153">End of client support</span></span><br/>    | <span data-ttu-id="d1769-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1769-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1769-155">Produit</span><span class="sxs-lookup"><span data-stu-id="d1769-155">Product</span></span><br/>                  | <span data-ttu-id="d1769-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1769-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1769-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1769-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1769-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1769-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1769-159">IID</span><span class="sxs-lookup"><span data-stu-id="d1769-159">IID</span></span><br/>                      | <span data-ttu-id="d1769-160">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="d1769-160">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d1769-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1769-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1769-162">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="d1769-162">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

