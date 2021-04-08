---
description: Modifie les paramètres pour le service de réplication Hyper-V.
ms.assetid: e203f9f5-da4b-4ba7-8637-add7169990d3
title: Méthode ModifyServiceSettings de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe20f8e6f113dce05961eb11fbafdc7841f39e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752213"
---
# <a name="modifyservicesettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f0d91-103">Méthode ModifyServiceSettings de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="f0d91-103">ModifyServiceSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f0d91-104">Modifie les paramètres pour le service de réplication Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f0d91-104">Modifies the settings for the Hyper-V Replica service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0d91-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f0d91-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0d91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d91-107">*SettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0d91-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-108">Représentation sous forme de chaîne de la classe [**MSVM \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) qui contient les données de paramètre modifiées pour le service.</span><span class="sxs-lookup"><span data-stu-id="f0d91-108">A string representation of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f0d91-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0d91-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0d91-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0d91-111">Return value</span></span>

<span data-ttu-id="f0d91-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0d91-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f0d91-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="f0d91-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="f0d91-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="f0d91-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="f0d91-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="f0d91-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="f0d91-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="f0d91-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="f0d91-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="f0d91-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="f0d91-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="f0d91-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f0d91-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f0d91-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="f0d91-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f0d91-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0d91-126">Requirements</span></span>



| <span data-ttu-id="f0d91-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0d91-127">Requirement</span></span> | <span data-ttu-id="f0d91-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0d91-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d91-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0d91-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d91-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0d91-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0d91-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0d91-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d91-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0d91-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0d91-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f0d91-133">Namespace</span></span><br/>                | <span data-ttu-id="f0d91-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f0d91-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0d91-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f0d91-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0d91-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0d91-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0d91-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f0d91-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0d91-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0d91-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0d91-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0d91-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d91-140">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="f0d91-140">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

