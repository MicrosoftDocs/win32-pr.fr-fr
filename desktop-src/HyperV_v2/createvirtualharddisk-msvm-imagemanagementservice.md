---
description: Crée un fichier de disque dur virtuel.
ms.assetid: 6c136000-1df2-4456-833c-094671408338
title: Méthode CreateVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b80a309274eb51ad7aff768898a9c3bd211f37cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519439"
---
# <a name="createvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="bfa31-103">Méthode CreateVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="bfa31-103">CreateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="bfa31-104">Crée un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="bfa31-104">Creates a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfa31-105">Syntax</span></span>


```mof
uint32 CreateVirtualHardDisk(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bfa31-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfa31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa31-107">*VirtualDiskSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfa31-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa31-108">Chaîne qui contient une instance incorporée de la classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) utilisée pour définir les attributs du disque dur virtuel à créer.</span><span class="sxs-lookup"><span data-stu-id="bfa31-108">String that contains an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that is used to define attributes of the virtual hard disk to be created.</span></span>

</dd> <dt>

<span data-ttu-id="bfa31-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bfa31-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa31-110">Référence au travail (peut avoir la **valeur null** si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="bfa31-110">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa31-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfa31-111">Return value</span></span>

<span data-ttu-id="bfa31-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bfa31-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bfa31-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="bfa31-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="bfa31-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="bfa31-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="bfa31-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="bfa31-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="bfa31-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="bfa31-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="bfa31-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="bfa31-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="bfa31-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="bfa31-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bfa31-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="bfa31-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bfa31-126">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="bfa31-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bfa31-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bfa31-127">Remarks</span></span>

<span data-ttu-id="bfa31-128">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="bfa31-128">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bfa31-129">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bfa31-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa31-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfa31-130">Requirements</span></span>



| <span data-ttu-id="bfa31-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfa31-131">Requirement</span></span> | <span data-ttu-id="bfa31-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfa31-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa31-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa31-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa31-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfa31-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bfa31-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa31-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa31-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfa31-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfa31-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bfa31-137">Namespace</span></span><br/>                | <span data-ttu-id="bfa31-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bfa31-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bfa31-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bfa31-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfa31-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfa31-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfa31-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa31-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa31-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfa31-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bfa31-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfa31-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa31-144">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="bfa31-144">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

