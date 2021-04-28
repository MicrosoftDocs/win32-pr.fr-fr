---
description: La méthode ModifyServiceSettings de la classe Msvm_TerminalService-modifie les données de paramètre pour le service.
ms.assetid: 76669180-fa95-4d6e-b89a-53e45da664c4
title: Méthode ModifyServiceSettings de la classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 930b29c5c07c755b493a0aabad88ae776c0803e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119327"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="da506-103">Méthode ModifyServiceSettings de la \_ classe TerminalService MSVM</span><span class="sxs-lookup"><span data-stu-id="da506-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="da506-104">Modifie les données de paramètre pour le service.</span><span class="sxs-lookup"><span data-stu-id="da506-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="da506-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da506-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="da506-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da506-107">*ServiceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da506-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da506-108">Représentation sous forme de chaîne de la classe [**MSVM \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) qui contient les données de paramètre modifiées pour le service.</span><span class="sxs-lookup"><span data-stu-id="da506-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="da506-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="da506-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da506-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da506-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da506-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da506-111">Return value</span></span>

<span data-ttu-id="da506-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="da506-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="da506-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="da506-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da506-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="da506-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="da506-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="da506-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="da506-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="da506-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="da506-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="da506-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="da506-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="da506-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="da506-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="da506-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="da506-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="da506-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="da506-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="da506-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="da506-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="da506-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="da506-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="da506-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="da506-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="da506-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="da506-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="da506-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="da506-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da506-126">Requirements</span></span>



| <span data-ttu-id="da506-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da506-127">Requirement</span></span> | <span data-ttu-id="da506-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="da506-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da506-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da506-129">Minimum supported client</span></span><br/> | <span data-ttu-id="da506-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da506-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="da506-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da506-131">Minimum supported server</span></span><br/> | <span data-ttu-id="da506-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da506-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da506-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="da506-133">Namespace</span></span><br/>                | <span data-ttu-id="da506-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="da506-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="da506-135">MOF</span><span class="sxs-lookup"><span data-stu-id="da506-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da506-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da506-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da506-137">DLL</span><span class="sxs-lookup"><span data-stu-id="da506-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da506-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da506-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="da506-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da506-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da506-140">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="da506-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

