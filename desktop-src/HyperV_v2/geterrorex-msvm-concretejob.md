---
description: Récupère les objets d’erreur pour le travail, le cas échéant.
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Méthode GetErrorEx de la classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e938d41afad430051bebb08fc77d6edf6da44691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542905"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="adb20-103">Méthode GetErrorEx de la \_ classe ConcreteJob MSVM</span><span class="sxs-lookup"><span data-stu-id="adb20-103">GetErrorEx method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="adb20-104">Récupère les objets d’erreur pour le travail, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="adb20-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="adb20-105">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune instance d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="adb20-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="adb20-106">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une ou plusieurs instances d' **\_ erreur MSVM** sont retournées.</span><span class="sxs-lookup"><span data-stu-id="adb20-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb20-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adb20-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="adb20-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adb20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adb20-109">*Erreurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="adb20-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adb20-110">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="adb20-110">Type: **string\[\]**</span></span>

<span data-ttu-id="adb20-111">Si l’état opérationnel du travail n’est pas 2 (OK), cette méthode retourne une ou plusieurs instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) , au format CIM-XML, qui représentent les erreurs rencontrées dans le travail.</span><span class="sxs-lookup"><span data-stu-id="adb20-111">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="adb20-112">Si l’état opérationnel du travail est 2 (OK), la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="adb20-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adb20-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adb20-113">Return value</span></span>

<span data-ttu-id="adb20-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="adb20-114">Type: **uint32**</span></span>

<span data-ttu-id="adb20-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="adb20-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="adb20-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="adb20-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="adb20-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="adb20-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="adb20-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="adb20-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="adb20-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="adb20-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="adb20-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="adb20-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="adb20-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="adb20-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="adb20-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="adb20-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="adb20-128">Notes</span><span class="sxs-lookup"><span data-stu-id="adb20-128">Remarks</span></span>

<span data-ttu-id="adb20-129">L’accès à la classe [**MSVM \_ ConcreteJob**](msvm-concretejob.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="adb20-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="adb20-130">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="adb20-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="adb20-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adb20-131">Requirements</span></span>



| <span data-ttu-id="adb20-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adb20-132">Requirement</span></span> | <span data-ttu-id="adb20-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="adb20-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb20-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adb20-134">Minimum supported client</span></span><br/> | <span data-ttu-id="adb20-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adb20-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="adb20-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adb20-136">Minimum supported server</span></span><br/> | <span data-ttu-id="adb20-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adb20-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="adb20-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="adb20-138">Namespace</span></span><br/>                | <span data-ttu-id="adb20-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="adb20-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="adb20-140">MOF</span><span class="sxs-lookup"><span data-stu-id="adb20-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adb20-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="adb20-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="adb20-142">DLL</span><span class="sxs-lookup"><span data-stu-id="adb20-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adb20-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="adb20-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="adb20-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adb20-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb20-145">**MSVM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="adb20-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

