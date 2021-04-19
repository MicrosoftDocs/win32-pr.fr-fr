---
description: Diagnostique la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Méthode DiagnoseNetworkConnection de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514151"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="205ad-103">Méthode DiagnoseNetworkConnection de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="205ad-103">DiagnoseNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="205ad-104">Diagnostique la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.</span><span class="sxs-lookup"><span data-stu-id="205ad-104">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="205ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="205ad-105">Syntax</span></span>


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="205ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="205ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205ad-107">*TargetNetworkAdapter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="205ad-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205ad-108">Référence à un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) qui décrit la carte réseau cible.</span><span class="sxs-lookup"><span data-stu-id="205ad-108">Reference to an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) that describes the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="205ad-109">*DiagnosticSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="205ad-109">*DiagnosticSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205ad-110">Paramètres de diagnostic à utiliser.</span><span class="sxs-lookup"><span data-stu-id="205ad-110">The diagnostic settings to use.</span></span>

</dd> <dt>

<span data-ttu-id="205ad-111">*DiagnosticInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="205ad-111">*DiagnosticInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="205ad-112">En cas de réussite, retourne les informations de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="205ad-112">On success, returns the diagnostic information.</span></span>

</dd> <dt>

<span data-ttu-id="205ad-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="205ad-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="205ad-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="205ad-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205ad-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="205ad-115">Return value</span></span>

<span data-ttu-id="205ad-116">Retourne une valeur 0 ou 4096 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="205ad-116">Returns a 0 or 4096 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="205ad-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="205ad-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-118">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="205ad-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-119">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="205ad-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-120">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="205ad-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-121">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="205ad-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="205ad-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="205ad-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="205ad-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="205ad-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="205ad-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="205ad-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="205ad-126">Requirements</span></span>



| <span data-ttu-id="205ad-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="205ad-127">Requirement</span></span> | <span data-ttu-id="205ad-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="205ad-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205ad-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="205ad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="205ad-130">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="205ad-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="205ad-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="205ad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="205ad-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="205ad-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="205ad-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="205ad-133">Namespace</span></span><br/>                | <span data-ttu-id="205ad-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="205ad-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="205ad-135">MOF</span><span class="sxs-lookup"><span data-stu-id="205ad-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="205ad-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="205ad-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="205ad-137">DLL</span><span class="sxs-lookup"><span data-stu-id="205ad-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="205ad-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="205ad-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="205ad-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="205ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205ad-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="205ad-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

