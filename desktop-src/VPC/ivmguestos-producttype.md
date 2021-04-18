---
title: IVMGuestOS ProductType, propriété (VPCCOMInterfaces. h)
description: Récupère le type de produit du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- ProductType propriété Virtual PC
- ProductType, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété ProductType
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512162"
---
# <a name="ivmguestosproducttype-property"></a><span data-ttu-id="a6265-106">IVMGuestOS ::P propriété roductType</span><span class="sxs-lookup"><span data-stu-id="a6265-106">IVMGuestOS::ProductType property</span></span>

<span data-ttu-id="a6265-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a6265-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a6265-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a6265-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a6265-109">Récupère le type de produit du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a6265-109">Retrieves the product type of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="a6265-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a6265-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6265-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6265-111">Syntax</span></span>


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a><span data-ttu-id="a6265-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a6265-112">Property value</span></span>

<span data-ttu-id="a6265-113">Type de produit.</span><span class="sxs-lookup"><span data-stu-id="a6265-113">The product type.</span></span> <span data-ttu-id="a6265-114">Les valeurs de chaîne suivantes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a6265-114">The following string values are supported.</span></span>



| <span data-ttu-id="a6265-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6265-115">Value</span></span>                                                                                  | <span data-ttu-id="a6265-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a6265-116">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6265-117"><dt>"0x0000002"</dt></span><span class="sxs-lookup"><span data-stu-id="a6265-117"><dt>"0x0000002"</dt></span></span> </dl> | <span data-ttu-id="a6265-118">Le système est un contrôleur de domaine et le système d’exploitation est Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a6265-118">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="a6265-119"><dt>"0x0000003"</dt></span><span class="sxs-lookup"><span data-stu-id="a6265-119"><dt>"0x0000003"</dt></span></span> </dl> | <span data-ttu-id="a6265-120">Le système d’exploitation est Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a6265-120">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="a6265-121">Notez qu’un serveur qui est également un contrôleur de domaine est signalé en tant que **\_ \_ \_ contrôleur de domaine NT**, pas **ver \_ NT \_ Server**.</span><span class="sxs-lookup"><span data-stu-id="a6265-121">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <dl> <span data-ttu-id="a6265-122"><dt>"0x0000001"</dt></span><span class="sxs-lookup"><span data-stu-id="a6265-122"><dt>"0x0000001"</dt></span></span> </dl> | <span data-ttu-id="a6265-123">Le système d’exploitation est Windows 7, Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="a6265-123">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="a6265-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6265-124">Requirements</span></span>



| <span data-ttu-id="a6265-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6265-125">Requirement</span></span> | <span data-ttu-id="a6265-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6265-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6265-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6265-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a6265-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6265-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6265-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6265-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a6265-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6265-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a6265-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a6265-131">End of client support</span></span><br/>    | <span data-ttu-id="a6265-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6265-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a6265-133">Produit</span><span class="sxs-lookup"><span data-stu-id="a6265-133">Product</span></span><br/>                  | <span data-ttu-id="a6265-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a6265-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a6265-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6265-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6265-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6265-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a6265-137">IID</span><span class="sxs-lookup"><span data-stu-id="a6265-137">IID</span></span><br/>                      | <span data-ttu-id="a6265-138">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="a6265-138">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a6265-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6265-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6265-140">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="a6265-140">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

