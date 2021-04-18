---
description: Interrogation des informations de cluster à partir de l’hôte Hyper-V vers l’invité.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Méthode QueryGuestClusterInformation de la classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525179"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a><span data-ttu-id="daa2c-103">Méthode QueryGuestClusterInformation de la \_ classe VssService MSVM</span><span class="sxs-lookup"><span data-stu-id="daa2c-103">QueryGuestClusterInformation method of the Msvm\_VssService class</span></span>

<span data-ttu-id="daa2c-104">Interrogation des informations de cluster à partir de l’hôte Hyper-V vers l’invité.</span><span class="sxs-lookup"><span data-stu-id="daa2c-104">Querying cluster information from the Hyper-V host to the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daa2c-105">Syntax</span></span>


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a><span data-ttu-id="daa2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daa2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa2c-107">*GuestClusterInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="daa2c-107">*GuestClusterInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daa2c-108">En cas de réussite, contient un [**\_ GuestClusterInformation MSVM**](msvm-guestclusterinformation.md) qui décrit le cluster invité.</span><span class="sxs-lookup"><span data-stu-id="daa2c-108">On success, contains an [**Msvm\_GuestClusterInformation**](msvm-guestclusterinformation.md) that describes the guest cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daa2c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="daa2c-109">Return value</span></span>

<span data-ttu-id="daa2c-110">En cas de réussite, retourne 0 (terminé sans erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="daa2c-110">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="daa2c-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="daa2c-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-112">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="daa2c-112">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-113">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="daa2c-113">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-114">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="daa2c-114">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-115">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="daa2c-115">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-116">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="daa2c-116">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-117">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="daa2c-117">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-118">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="daa2c-118">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-119">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="daa2c-119">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-120">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="daa2c-120">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-121">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="daa2c-121">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-122">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="daa2c-122">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="daa2c-123">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="daa2c-123">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="daa2c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daa2c-124">Requirements</span></span>



| <span data-ttu-id="daa2c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daa2c-125">Requirement</span></span> | <span data-ttu-id="daa2c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="daa2c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa2c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daa2c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="daa2c-128">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="daa2c-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="daa2c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daa2c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="daa2c-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="daa2c-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="daa2c-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="daa2c-131">Namespace</span></span><br/>                | <span data-ttu-id="daa2c-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="daa2c-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="daa2c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="daa2c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="daa2c-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="daa2c-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="daa2c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="daa2c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daa2c-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="daa2c-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="daa2c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daa2c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa2c-138">**MSVM \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="daa2c-138">**Msvm\_VssService**</span></span>](msvm-vssservice.md)
</dt> </dl>

 

 




