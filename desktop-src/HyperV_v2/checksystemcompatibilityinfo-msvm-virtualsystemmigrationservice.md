---
description: Vérifie les informations de compatibilité pour la compatibilité avec le système de l’ordinateur hôte.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Méthode CheckSystemCompatibilityInfo de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862081"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="598f6-103">Méthode CheckSystemCompatibilityInfo de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="598f6-103">CheckSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="598f6-104">Vérifie les informations de compatibilité pour la compatibilité avec le système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="598f6-104">Checks the compatibility information for compatibility with the hosting computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="598f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="598f6-105">Syntax</span></span>


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a><span data-ttu-id="598f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="598f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598f6-107">*CompatibilityInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="598f6-107">*CompatibilityInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="598f6-108">Objet blob de données obtenu en appelant la méthode [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) sur le système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="598f6-108">A blob of data obtained by calling the [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="598f6-109">*Raisons pour lesquelles* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="598f6-109">*Reasons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="598f6-110">Tableau de chaînes qui reçoit les instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) qui représentent des avertissements ou des erreurs.</span><span class="sxs-lookup"><span data-stu-id="598f6-110">An array of strings that receives the embedded instances of the [**Msvm\_Error**](msvm-error.md) class that represent any warnings or errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598f6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="598f6-111">Return value</span></span>

<span data-ttu-id="598f6-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="598f6-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="598f6-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="598f6-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="598f6-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="598f6-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="598f6-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="598f6-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="598f6-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="598f6-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="598f6-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="598f6-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="598f6-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="598f6-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="598f6-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="598f6-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="598f6-126">**Non compatible** (32784)</span><span class="sxs-lookup"><span data-stu-id="598f6-126">**Not compatible** (32784)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="598f6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="598f6-127">Requirements</span></span>



| <span data-ttu-id="598f6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="598f6-128">Requirement</span></span> | <span data-ttu-id="598f6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="598f6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="598f6-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="598f6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="598f6-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="598f6-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="598f6-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="598f6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="598f6-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="598f6-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="598f6-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="598f6-134">Namespace</span></span><br/>                | <span data-ttu-id="598f6-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="598f6-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="598f6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="598f6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="598f6-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="598f6-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="598f6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="598f6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="598f6-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="598f6-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="598f6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="598f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598f6-141">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="598f6-141">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




