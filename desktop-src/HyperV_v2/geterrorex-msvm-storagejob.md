---
description: Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune \_ instance d’erreur MSVM.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Méthode GetErrorEx de la classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514039"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="a7a7a-103">Méthode GetErrorEx de la \_ classe StorageJob MSVM</span><span class="sxs-lookup"><span data-stu-id="a7a7a-103">GetErrorEx method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="a7a7a-104">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune instance d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="a7a7a-104">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="a7a7a-105">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une ou plusieurs instances d' **\_ erreur MSVM** sont retournées.</span><span class="sxs-lookup"><span data-stu-id="a7a7a-105">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a7a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7a7a-106">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="a7a7a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7a7a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7a7a-108">*Erreurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a7a7a-108">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7a7a-109">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a7a7a-109">Type: **string\[\]**</span></span>

<span data-ttu-id="a7a7a-110">Si l’état opérationnel du travail n’est pas « OK », cette méthode retourne un tableau d’instances d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="a7a7a-110">If the operational status of the job is not "OK", this method returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="a7a7a-111">Sinon, si la tâche est « OK », la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="a7a7a-111">Otherwise, if the job is "OK", **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7a7a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7a7a-112">Return value</span></span>

<span data-ttu-id="a7a7a-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7a7a-113">Type: **uint32**</span></span>

<span data-ttu-id="a7a7a-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7a7a-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a7a7a-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a7a7a-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="a7a7a-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a7a7a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a7a7a-127">Remarks</span></span>

<span data-ttu-id="a7a7a-128">L’accès à la classe [**MSVM \_ StorageJob**](msvm-storagejob.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="a7a7a-128">Access to the [**Msvm\_StorageJob**](msvm-storagejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a7a7a-129">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a7a7a-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7a7a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7a7a-130">Requirements</span></span>



| <span data-ttu-id="a7a7a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7a7a-131">Requirement</span></span> | <span data-ttu-id="a7a7a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7a7a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a7a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a7a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a7a-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7a7a-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a7a7a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a7a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a7a-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7a7a-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7a7a-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a7a7a-137">Namespace</span></span><br/>                | <span data-ttu-id="a7a7a-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a7a7a-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a7a7a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a7a7a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7a7a-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7a7a-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7a7a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a7a7a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7a7a-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a7a7a-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a7a7a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7a7a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a7a-144">**MSVM \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="a7a7a-144">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

