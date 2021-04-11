---
description: Crée une instance de machine virtuelle.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Méthode DefineSystem de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204025"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a633a-103">Méthode DefineSystem de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="a633a-103">DefineSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a633a-104">Crée une instance de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a633a-104">Creates a new virtual machine instance.</span></span> <span data-ttu-id="a633a-105">Les propriétés qui ne sont pas spécifiées sont remplies avec les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="a633a-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a633a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a633a-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a633a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a633a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a633a-108">*SystemSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a633a-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a633a-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a633a-109">Type: **string**</span></span>

<span data-ttu-id="a633a-110">Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) utilisée pour définir les attributs de l’ordinateur virtuel à créer.</span><span class="sxs-lookup"><span data-stu-id="a633a-110">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is used to define the attributes of the virtual machine to be created.</span></span> <span data-ttu-id="a633a-111">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a633a-111">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="a633a-112">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a633a-112">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a633a-113">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a633a-113">Type: **string\[\]**</span></span>

<span data-ttu-id="a633a-114">Nombre d’instances incorporées de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (ou classes dérivées de celles-ci).</span><span class="sxs-lookup"><span data-stu-id="a633a-114">A number of embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class (or derived classes thereof).</span></span> <span data-ttu-id="a633a-115">Ensemble, ces instances décrivent les ressources virtuelles de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a633a-115">Together these instances describe the virtual resources of the virtual machine.</span></span> <span data-ttu-id="a633a-116">Un ensemble d’appareils par défaut sera créé pour l’ordinateur virtuel, que ce paramètre soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="a633a-116">A default set of devices will be created for the virtual machine regardless of whether this parameter is set.</span></span> <span data-ttu-id="a633a-117">Par exemple, le processeur et la mémoire sont automatiquement créés et configurés avec les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="a633a-117">For example, processor and memory are automatically created and configured with default values.</span></span>

</dd> <dt>

<span data-ttu-id="a633a-118">*ReferenceConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a633a-118">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a633a-119">Type : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="a633a-119">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="a633a-120">Référence à une instance de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui est l’objet de niveau supérieur d’une configuration d’ordinateur virtuel de référence.</span><span class="sxs-lookup"><span data-stu-id="a633a-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is the top level object of a reference virtual machine configuration.</span></span> <span data-ttu-id="a633a-121">La configuration de référence est utilisée pour compléter la configuration du nouvel ordinateur virtuel si les paramètres *SystemSettings* et *ResourceSettings* n’ont pas fourni d’informations respectives.</span><span class="sxs-lookup"><span data-stu-id="a633a-121">The reference configuration is used to complement the configuration of the new virtual machine if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="a633a-122">*ResultingSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a633a-122">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a633a-123">Type : **CIM \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="a633a-123">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="a633a-124">Référence à une instance de la classe [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="a633a-124">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly created virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a633a-125">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a633a-125">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a633a-126">Type : **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="a633a-126">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="a633a-127">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a633a-127">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a633a-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a633a-128">Return value</span></span>

<span data-ttu-id="a633a-129">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a633a-129">Type: **uint32**</span></span>

<span data-ttu-id="a633a-130">Si cette méthode est exécutée de façon synchrone, elle retourne 0 si elle réussit.</span><span class="sxs-lookup"><span data-stu-id="a633a-130">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="a633a-131">Si cette méthode est exécutée de façon asynchrone, elle retourne 4096 et le paramètre de sortie de la *tâche* peut être utilisé pour suivre la progression de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a633a-131">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="a633a-132">Toute autre valeur de retour indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="a633a-132">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="a633a-133">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a633a-133">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-134">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a633a-134">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-135">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="a633a-135">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-136">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="a633a-136">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-137">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="a633a-137">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-138">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a633a-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-139">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="a633a-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-140">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a633a-140">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a633a-141">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a633a-141">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a633a-142">Notes</span><span class="sxs-lookup"><span data-stu-id="a633a-142">Remarks</span></span>

<span data-ttu-id="a633a-143">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="a633a-143">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a633a-144">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a633a-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a633a-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a633a-145">Requirements</span></span>



| <span data-ttu-id="a633a-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a633a-146">Requirement</span></span> | <span data-ttu-id="a633a-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="a633a-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a633a-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a633a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a633a-149">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a633a-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a633a-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a633a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a633a-151">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a633a-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a633a-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a633a-152">Namespace</span></span><br/>                | <span data-ttu-id="a633a-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a633a-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a633a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a633a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a633a-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a633a-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a633a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a633a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a633a-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a633a-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a633a-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a633a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a633a-159">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a633a-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

