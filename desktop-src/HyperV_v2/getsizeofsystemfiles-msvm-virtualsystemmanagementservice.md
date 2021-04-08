---
description: Récupère la taille totale des fichiers système de l’ordinateur virtuel.
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Méthode GetSizeOfSystemFiles de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9fcf93093e17c2989121bf33ee5f5fbf09bab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752220"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6fe99-103">Méthode GetSizeOfSystemFiles de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="6fe99-103">GetSizeOfSystemFiles method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6fe99-104">Récupère la taille totale des fichiers système de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6fe99-104">Retrieves the total size of the system files of virtual machine.</span></span> <span data-ttu-id="6fe99-105">Il s’agit notamment des fichiers de configuration et d’état enregistré.</span><span class="sxs-lookup"><span data-stu-id="6fe99-105">These include the configuration and saved state files.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe99-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fe99-106">Syntax</span></span>


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a><span data-ttu-id="6fe99-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fe99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe99-108">*Vssd* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe99-108">*Vssd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe99-109">Référence à l’instance [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) dont la taille des fichiers système doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="6fe99-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose system files size are to be retrieved.</span></span> <span data-ttu-id="6fe99-110">Cette instance peut représenter l’instanciation actuelle de l’ordinateur virtuel ou une instance d’une capture instantanée d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6fe99-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="6fe99-111">*Taille* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6fe99-111">*Size* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe99-112">Taille totale, en octets, des fichiers système.</span><span class="sxs-lookup"><span data-stu-id="6fe99-112">The total size, in bytes, of system files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe99-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fe99-113">Return value</span></span>

<span data-ttu-id="6fe99-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6fe99-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6fe99-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6fe99-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6fe99-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="6fe99-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="6fe99-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="6fe99-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="6fe99-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="6fe99-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="6fe99-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="6fe99-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="6fe99-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="6fe99-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="6fe99-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6fe99-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="6fe99-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6fe99-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fe99-128">Requirements</span></span>



| <span data-ttu-id="6fe99-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fe99-129">Requirement</span></span> | <span data-ttu-id="6fe99-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fe99-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe99-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe99-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe99-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe99-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6fe99-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe99-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe99-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe99-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6fe99-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6fe99-135">Namespace</span></span><br/>                | <span data-ttu-id="6fe99-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6fe99-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6fe99-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6fe99-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fe99-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fe99-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fe99-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6fe99-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fe99-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6fe99-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6fe99-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe99-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe99-142">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6fe99-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

