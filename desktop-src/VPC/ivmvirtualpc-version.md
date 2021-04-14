---
title: Propriété version de IVMVirtualPC (VPCCOMInterfaces. h)
description: Récupère la version de cette instance de Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Propriété de version Virtual PC
- Propriété de version Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, propriété version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466978"
---
# <a name="ivmvirtualpcversion-property"></a><span data-ttu-id="a5b3f-106">IVMVirtualPC :: version, propriété</span><span class="sxs-lookup"><span data-stu-id="a5b3f-106">IVMVirtualPC::Version property</span></span>

<span data-ttu-id="a5b3f-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a5b3f-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a5b3f-109">Récupère la version de cette instance de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-109">Retrieves the version of this instance of Windows Virtual PC.</span></span>

<span data-ttu-id="a5b3f-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b3f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5b3f-111">Syntax</span></span>


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a><span data-ttu-id="a5b3f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a5b3f-112">Property value</span></span>

<span data-ttu-id="a5b3f-113">Version.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5b3f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a5b3f-114">Error codes</span></span>



| <span data-ttu-id="a5b3f-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a5b3f-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a5b3f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a5b3f-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5b3f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a5b3f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a5b3f-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a5b3f-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a5b3f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a5b3f-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a5b3f-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a5b3f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a5b3f-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a5b3f-123"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a5b3f-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a5b3f-124">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="a5b3f-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a5b3f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="a5b3f-125">Remarks</span></span>

<span data-ttu-id="a5b3f-126">Les informations de version de Windows Virtual PC sont retournées sous la forme d’une valeur de chaîne au format suivant : «*v*. *s*. *BBB*. *tee*», où *v* est le numéro de version principale, *s* est le numéro de version mineure, *BBB* est le numéro de build, *t* est le type de build (0 = version Release) et *EE* est l’édition Server (se = Standard Edition, EE = Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="a5b3f-126">The Windows Virtual PC version information is returned as a string value with the following format: "*v*.*s*.*bbb*.*tee*", where *v* is the major version number, *s* is the minor version number, *bbb* is the build number, *t* is the build type (0 = release build), and *ee* is the server edition (SE = Standard Edition, EE = Enterprise Edition).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b3f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5b3f-127">Requirements</span></span>



| <span data-ttu-id="a5b3f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5b3f-128">Requirement</span></span> | <span data-ttu-id="a5b3f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5b3f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b3f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b3f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b3f-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5b3f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b3f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b3f-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b3f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a5b3f-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a5b3f-134">End of client support</span></span><br/>    | <span data-ttu-id="a5b3f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5b3f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a5b3f-136">Produit</span><span class="sxs-lookup"><span data-stu-id="a5b3f-136">Product</span></span><br/>                  | <span data-ttu-id="a5b3f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a5b3f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a5b3f-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5b3f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b3f-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b3f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a5b3f-140">IID</span><span class="sxs-lookup"><span data-stu-id="a5b3f-140">IID</span></span><br/>                      | <span data-ttu-id="a5b3f-141">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a5b3f-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a5b3f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5b3f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b3f-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

