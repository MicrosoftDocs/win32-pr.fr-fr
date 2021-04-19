---
title: Méthode IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces. h)
description: Récupère des informations de version pour le système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Méthode GetOsVersionInfo Virtual PC
- Méthode GetOsVersionInfo Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106544180"
---
# <a name="ivmguestosgetosversioninfo-method"></a><span data-ttu-id="40804-106">IVMGuestOS :: GetOsVersionInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="40804-106">IVMGuestOS::GetOsVersionInfo method</span></span>

<span data-ttu-id="40804-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40804-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40804-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="40804-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40804-109">Récupère des informations de version pour le système d’exploitation invité en cours d’exécution sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="40804-109">Retrieves version information for the guest operating system running in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="40804-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40804-110">Syntax</span></span>


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="40804-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40804-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40804-112">*guestOsVersionInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="40804-112">*guestOsVersionInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="40804-113">Pointeur vers une structure [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) .</span><span class="sxs-lookup"><span data-stu-id="40804-113">A pointer to a [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40804-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40804-114">Return value</span></span>

<span data-ttu-id="40804-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="40804-115">This method can return one of these values.</span></span>



| <span data-ttu-id="40804-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="40804-116">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="40804-117">Description</span><span class="sxs-lookup"><span data-stu-id="40804-117">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40804-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40804-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="40804-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="40804-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="40804-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="40804-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="40804-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="40804-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="40804-122">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="40804-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="40804-123">La mémoire disponible est insuffisante pour effectuer cette requête.</span><span class="sxs-lookup"><span data-stu-id="40804-123">There is not enough memory available to complete this request.</span></span><br/> |
| <dl> <span data-ttu-id="40804-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="40804-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="40804-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="40804-125">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="40804-126"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="40804-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="40804-127">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="40804-127">The VM is not running.</span></span><br/>                                         |
| <dl> <span data-ttu-id="40804-128"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="40804-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="40804-129">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="40804-129">Integration components are not installed in this VM.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="40804-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40804-130">Requirements</span></span>



| <span data-ttu-id="40804-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40804-131">Requirement</span></span> | <span data-ttu-id="40804-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="40804-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40804-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40804-133">Minimum supported client</span></span><br/> | <span data-ttu-id="40804-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40804-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40804-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40804-135">Minimum supported server</span></span><br/> | <span data-ttu-id="40804-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40804-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40804-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="40804-137">End of client support</span></span><br/>    | <span data-ttu-id="40804-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40804-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40804-139">Produit</span><span class="sxs-lookup"><span data-stu-id="40804-139">Product</span></span><br/>                  | <span data-ttu-id="40804-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40804-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40804-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="40804-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="40804-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="40804-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40804-143">IID</span><span class="sxs-lookup"><span data-stu-id="40804-143">IID</span></span><br/>                      | <span data-ttu-id="40804-144">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="40804-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="40804-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40804-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40804-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="40804-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

