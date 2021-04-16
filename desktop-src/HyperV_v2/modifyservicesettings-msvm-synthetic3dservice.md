---
description: Modifie les données de paramètre pour le service 3D synthétique.
ms.assetid: 951ba829-2821-4621-800f-4e1a967b41f5
title: Méthode ModifyServiceSettings de la classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 76f6fe18dea67231c9d722352df516bf97c35ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485553"
---
# <a name="modifyservicesettings-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="81ab0-103">Méthode ModifyServiceSettings de la \_ classe Synthetic3DService MSVM</span><span class="sxs-lookup"><span data-stu-id="81ab0-103">ModifyServiceSettings method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="81ab0-104">Modifie les données de paramètre pour le service 3D synthétique.</span><span class="sxs-lookup"><span data-stu-id="81ab0-104">Modifies the setting data for the synthetic 3-D service.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ab0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81ab0-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="81ab0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81ab0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ab0-107">*SettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81ab0-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ab0-108">Représentation sous forme de chaîne de la classe [**MSVM \_ Synthetic3DServiceSettingData**](msvm-synthetic3dservicesettingdata.md) qui contient les données de paramètre modifiées pour le service.</span><span class="sxs-lookup"><span data-stu-id="81ab0-108">A string representation of the [**Msvm\_Synthetic3DServiceSettingData**](msvm-synthetic3dservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="81ab0-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="81ab0-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81ab0-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81ab0-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ab0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81ab0-111">Return value</span></span>

<span data-ttu-id="81ab0-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="81ab0-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="81ab0-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="81ab0-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="81ab0-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="81ab0-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="81ab0-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="81ab0-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="81ab0-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="81ab0-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="81ab0-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="81ab0-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="81ab0-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="81ab0-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="81ab0-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="81ab0-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="81ab0-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="81ab0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81ab0-126">Requirements</span></span>



| <span data-ttu-id="81ab0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81ab0-127">Requirement</span></span> | <span data-ttu-id="81ab0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="81ab0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ab0-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81ab0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="81ab0-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81ab0-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81ab0-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81ab0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="81ab0-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81ab0-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81ab0-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81ab0-133">Namespace</span></span><br/>                | <span data-ttu-id="81ab0-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="81ab0-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81ab0-135">MOF</span><span class="sxs-lookup"><span data-stu-id="81ab0-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81ab0-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81ab0-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81ab0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="81ab0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81ab0-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81ab0-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81ab0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81ab0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ab0-140">**MSVM \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="81ab0-140">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

