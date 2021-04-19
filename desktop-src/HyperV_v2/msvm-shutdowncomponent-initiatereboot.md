---
description: Lance une opération de redémarrage du système d’exploitation sur l’ordinateur virtuel enfant associé.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Méthode InitiateReboot de la classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533612"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="24aa6-103">Méthode InitiateReboot de la \_ classe ShutdownComponent MSVM</span><span class="sxs-lookup"><span data-stu-id="24aa6-103">InitiateReboot method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="24aa6-104">Lance une opération de redémarrage du système d’exploitation sur l’ordinateur virtuel enfant associé.</span><span class="sxs-lookup"><span data-stu-id="24aa6-104">Initiates an operating system reboot operation on the associated child virtual machine.</span></span>

<span data-ttu-id="24aa6-105">Si la valeur zéro (0) est retournée, le redémarrage a été lancé avec succès.</span><span class="sxs-lookup"><span data-stu-id="24aa6-105">If zero (0) is returned, then the reboot was initiated successfully.</span></span> <span data-ttu-id="24aa6-106">Tout autre code de retour indique une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="24aa6-106">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="24aa6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24aa6-107">Syntax</span></span>


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="24aa6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24aa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24aa6-109">*Force* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="24aa6-109">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24aa6-110">Indicateur qui, si la valeur est TRUE, force la fermeture des applications malgré la non-enregistrement des données.</span><span class="sxs-lookup"><span data-stu-id="24aa6-110">A flag which, if TRUE, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="24aa6-111">*Raison* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="24aa6-111">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24aa6-112">Raison de l’opération de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="24aa6-112">The reason for the reboot operation.</span></span> <span data-ttu-id="24aa6-113">Il s’agit d’une chaîne définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="24aa6-113">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24aa6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24aa6-114">Return value</span></span>

<span data-ttu-id="24aa6-115">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="24aa6-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="24aa6-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="24aa6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="24aa6-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="24aa6-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="24aa6-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="24aa6-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="24aa6-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="24aa6-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="24aa6-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="24aa6-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="24aa6-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="24aa6-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="24aa6-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="24aa6-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="24aa6-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-130">**Le système n’est pas prêt** (32780)</span><span class="sxs-lookup"><span data-stu-id="24aa6-130">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-131">**L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option force** (32781)</span><span class="sxs-lookup"><span data-stu-id="24aa6-131">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="24aa6-132">**Un arrêt système est en cours** (32782)</span><span class="sxs-lookup"><span data-stu-id="24aa6-132">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="24aa6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24aa6-133">Requirements</span></span>



| <span data-ttu-id="24aa6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24aa6-134">Requirement</span></span> | <span data-ttu-id="24aa6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="24aa6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24aa6-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24aa6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="24aa6-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24aa6-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="24aa6-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24aa6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="24aa6-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="24aa6-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="24aa6-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="24aa6-140">Namespace</span></span><br/>                | <span data-ttu-id="24aa6-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="24aa6-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24aa6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="24aa6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24aa6-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24aa6-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24aa6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="24aa6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24aa6-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24aa6-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24aa6-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24aa6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24aa6-147">**MSVM \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="24aa6-147">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




