---
title: Interface IVMAccountant (VPCCOMInterfaces. h)
description: Permet d’accéder aux informations relatives à la comptabilité pour un ordinateur virtuel.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Virtual PC de l’interface IVMAccountant
- IVMAccountant interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743476"
---
# <a name="ivmaccountant-interface"></a><span data-ttu-id="faf25-105">Interface IVMAccountant</span><span class="sxs-lookup"><span data-stu-id="faf25-105">IVMAccountant interface</span></span>

<span data-ttu-id="faf25-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="faf25-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="faf25-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="faf25-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="faf25-108">Permet d’accéder aux informations relatives à la comptabilité pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="faf25-108">Provides access to accounting-related information for a virtual machine.</span></span> <span data-ttu-id="faf25-109">Pour récupérer les **IVMAccountant** d’un ordinateur virtuel, utilisez la propriété [**IVMVirtualMachine :: comptable**](ivmvirtualmachine-accountant.md) .</span><span class="sxs-lookup"><span data-stu-id="faf25-109">To retrieve the **IVMAccountant** for a virtual machine, use the [**IVMVirtualMachine::Accountant**](ivmvirtualmachine-accountant.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="faf25-110">Membres</span><span class="sxs-lookup"><span data-stu-id="faf25-110">Members</span></span>

<span data-ttu-id="faf25-111">L’interface **IVMAccountant** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="faf25-111">The **IVMAccountant** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="faf25-112">**IVMAccountant** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="faf25-112">**IVMAccountant** also has these types of members:</span></span>

-   [<span data-ttu-id="faf25-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="faf25-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="faf25-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="faf25-114">Properties</span></span>

<span data-ttu-id="faf25-115">L’interface **IVMAccountant** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="faf25-115">The **IVMAccountant** interface has these properties.</span></span>



| <span data-ttu-id="faf25-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="faf25-116">Property</span></span>                                                                        | <span data-ttu-id="faf25-117">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="faf25-117">Access type</span></span>          | <span data-ttu-id="faf25-118">Description</span><span class="sxs-lookup"><span data-stu-id="faf25-118">Description</span></span>                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="faf25-119">**CPUUtilization**</span><span class="sxs-lookup"><span data-stu-id="faf25-119">**CPUUtilization**</span></span>](ivmaccountant-cpuutilization.md)<br/>               | <span data-ttu-id="faf25-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="faf25-120">Read-only</span></span><br/> | <span data-ttu-id="faf25-121">Pourcentage d’utilisation actuelle du processeur pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="faf25-121">The percentage of current CPU utilization for this virtual machine.</span></span><br/>                          |
| [<span data-ttu-id="faf25-122">**CPUUtilizationHistory**</span><span class="sxs-lookup"><span data-stu-id="faf25-122">**CPUUtilizationHistory**</span></span>](ivmaccountant-cpuutilizationhistory.md)<br/> | <span data-ttu-id="faf25-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="faf25-123">Read-only</span></span><br/> | <span data-ttu-id="faf25-124">Utilisation récente du processeur de cet ordinateur virtuel (sous la forme d’un tableau de valeurs de pourcentage).</span><span class="sxs-lookup"><span data-stu-id="faf25-124">The recent CPU utilization of this virtual machine (as an array of percentage values).</span></span><br/>       |
| [<span data-ttu-id="faf25-125">**DiskBytesRead**</span><span class="sxs-lookup"><span data-stu-id="faf25-125">**DiskBytesRead**</span></span>](ivmaccountant-diskbytesread.md)<br/>                 | <span data-ttu-id="faf25-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="faf25-126">Read-only</span></span><br/> | <span data-ttu-id="faf25-127">Nombre total d’octets lus par tous les contrôleurs de stockage pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="faf25-127">The total number of bytes read by all storage controllers for this virtual machine.</span></span><br/>          |
| [<span data-ttu-id="faf25-128">**DiskBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="faf25-128">**DiskBytesWritten**</span></span>](ivmaccountant-diskbyteswritten.md)<br/>           | <span data-ttu-id="faf25-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="faf25-129">Read-only</span></span><br/> | <span data-ttu-id="faf25-130">Nombre total d’octets écrits par tous les contrôleurs de stockage pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="faf25-130">The total number of bytes written by all storage controllers for this virtual machine.</span></span><br/>       |
| [<span data-ttu-id="faf25-131">**NetworkBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="faf25-131">**NetworkBytesReceived**</span></span>](ivmaccountant-networkbytesreceived.md)<br/>   | <span data-ttu-id="faf25-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="faf25-132">Read-only</span></span><br/> | <span data-ttu-id="faf25-133">Nombre total d’octets reçus par toutes les cartes réseau virtuelles de cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="faf25-133">The total number of bytes received by all virtual network adapters for this virtual machine.</span></span><br/> |
| [<span data-ttu-id="faf25-134">**NetworkBytesSent**</span><span class="sxs-lookup"><span data-stu-id="faf25-134">**NetworkBytesSent**</span></span>](ivmaccountant-networkbytessent.md)<br/>           | <span data-ttu-id="faf25-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="faf25-135">Read-only</span></span><br/> | <span data-ttu-id="faf25-136">Nombre total d’octets envoyés par toutes les cartes réseau virtuelles pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="faf25-136">The total number of bytes sent by all virtual network adapters for this virtual machine.</span></span><br/>     |
| [<span data-ttu-id="faf25-137">**Activité**</span><span class="sxs-lookup"><span data-stu-id="faf25-137">**UpTime**</span></span>](ivmaccountant-uptime.md)<br/>                               | <span data-ttu-id="faf25-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="faf25-138">Read-only</span></span><br/> | <span data-ttu-id="faf25-139">Nombre de secondes pendant lequel l’ordinateur virtuel a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="faf25-139">The number of seconds that the virtual machine has been running.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="faf25-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faf25-140">Requirements</span></span>



| <span data-ttu-id="faf25-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faf25-141">Requirement</span></span> | <span data-ttu-id="faf25-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="faf25-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf25-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faf25-143">Minimum supported client</span></span><br/> | <span data-ttu-id="faf25-144">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faf25-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="faf25-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faf25-145">Minimum supported server</span></span><br/> | <span data-ttu-id="faf25-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="faf25-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="faf25-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="faf25-147">End of client support</span></span><br/>    | <span data-ttu-id="faf25-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="faf25-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="faf25-149">Produit</span><span class="sxs-lookup"><span data-stu-id="faf25-149">Product</span></span><br/>                  | <span data-ttu-id="faf25-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="faf25-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="faf25-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="faf25-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="faf25-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="faf25-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="faf25-153">IID</span><span class="sxs-lookup"><span data-stu-id="faf25-153">IID</span></span><br/>                      | <span data-ttu-id="faf25-154">IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="faf25-154">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



 

