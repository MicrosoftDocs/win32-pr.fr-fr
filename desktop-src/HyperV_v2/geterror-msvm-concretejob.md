---
description: Récupère l’objet d’erreur pour le travail, s’il en existe un.
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: Méthode GetError de la classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 63279d8bc08f0b9f1955f694470a3744defd8054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513000"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="b3e6a-103">Méthode GetError de la \_ classe ConcreteJob MSVM</span><span class="sxs-lookup"><span data-stu-id="b3e6a-103">GetError method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="b3e6a-104">Récupère l’objet d’erreur pour le travail, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="b3e6a-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="b3e6a-105">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne pas d’objet d' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3e6a-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="b3e6a-106">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une instance d' **\_ erreur CIM** est retournée.</span><span class="sxs-lookup"><span data-stu-id="b3e6a-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e6a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3e6a-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="b3e6a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3e6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e6a-109">*Erreur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3e6a-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e6a-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3e6a-110">Type: **string**</span></span>

<span data-ttu-id="b3e6a-111">Si l’état opérationnel du travail n’est pas 2 (OK), cette méthode retourne une instance incorporée de la classe d' [**\_ erreur MSVM**](msvm-error.md) , au format CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="b3e6a-111">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="b3e6a-112">Si l’état opérationnel du travail est 2 (OK), la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="b3e6a-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e6a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3e6a-113">Return value</span></span>

<span data-ttu-id="b3e6a-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3e6a-114">Type: **uint32**</span></span>

<span data-ttu-id="b3e6a-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b3e6a-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b3e6a-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b3e6a-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="b3e6a-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b3e6a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b3e6a-128">Remarks</span></span>

<span data-ttu-id="b3e6a-129">L’accès à la classe [**MSVM \_ ConcreteJob**](msvm-concretejob.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="b3e6a-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b3e6a-130">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b3e6a-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e6a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3e6a-131">Requirements</span></span>



| <span data-ttu-id="b3e6a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3e6a-132">Requirement</span></span> | <span data-ttu-id="b3e6a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3e6a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e6a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3e6a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e6a-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3e6a-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b3e6a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3e6a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e6a-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3e6a-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3e6a-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3e6a-138">Namespace</span></span><br/>                | <span data-ttu-id="b3e6a-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b3e6a-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b3e6a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b3e6a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3e6a-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3e6a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3e6a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b3e6a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3e6a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3e6a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3e6a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3e6a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e6a-145">**MSVM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="b3e6a-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

