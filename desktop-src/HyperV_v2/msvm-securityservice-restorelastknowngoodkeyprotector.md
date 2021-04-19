---
description: Restaure le dernier protecteur de clé valide connu.
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Méthode RestoreLastKnownGoodKeyProtector de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523726"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="754c7-103">Méthode RestoreLastKnownGoodKeyProtector de la \_ classe securityservice MSVM</span><span class="sxs-lookup"><span data-stu-id="754c7-103">RestoreLastKnownGoodKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="754c7-104">Restaure le dernier protecteur de clé valide connu.</span><span class="sxs-lookup"><span data-stu-id="754c7-104">Restores back to the last known good key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="754c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="754c7-105">Syntax</span></span>


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="754c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="754c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="754c7-107">*SecuritySettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="754c7-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754c7-108">La chaîne contient une instance incorporée de la classe [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md) représentant les paramètres de sécurité d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="754c7-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="754c7-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="754c7-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="754c7-110">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="754c7-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="754c7-111">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="754c7-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="754c7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="754c7-112">Return value</span></span>

<span data-ttu-id="754c7-113">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="754c7-113">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="754c7-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="754c7-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="754c7-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="754c7-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="754c7-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="754c7-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="754c7-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="754c7-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="754c7-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="754c7-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="754c7-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="754c7-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="754c7-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="754c7-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="754c7-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="754c7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="754c7-127">Requirements</span></span>



| <span data-ttu-id="754c7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="754c7-128">Requirement</span></span> | <span data-ttu-id="754c7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="754c7-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="754c7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="754c7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="754c7-131">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="754c7-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="754c7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="754c7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="754c7-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="754c7-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="754c7-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="754c7-134">Namespace</span></span><br/>                | <span data-ttu-id="754c7-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="754c7-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="754c7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="754c7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="754c7-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="754c7-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="754c7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="754c7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="754c7-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="754c7-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="754c7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="754c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="754c7-141">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="754c7-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




