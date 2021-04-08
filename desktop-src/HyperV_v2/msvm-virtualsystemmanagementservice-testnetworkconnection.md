---
description: Teste la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Méthode TestNetworkConnection de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112283"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a5e18-103">Méthode TestNetworkConnection de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="a5e18-103">TestNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a5e18-104">Teste la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.</span><span class="sxs-lookup"><span data-stu-id="a5e18-104">Tests the network connectivity of a VM in a Windows network virtualization environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e18-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5e18-105">Syntax</span></span>


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a5e18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5e18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e18-107">*TargetNetworkAdapter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-108">Référence à un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) décrivant la carte réseau cible.</span><span class="sxs-lookup"><span data-stu-id="a5e18-108">Reference to a [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) describing the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-109">*IsSender* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-109">*IsSender* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-110">Indique si cette méthode est appelée au niveau de l’expéditeur ou du récepteur.</span><span class="sxs-lookup"><span data-stu-id="a5e18-110">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-111">*SenderIP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-111">*SenderIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-112">Adresse IP de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a5e18-112">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-113">*ReceiverIP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-113">*ReceiverIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-114">Adresse MAC de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a5e18-114">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-115">*ReceiverMac* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-115">*ReceiverMac* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-116">Adresse MAC de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a5e18-116">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-117">*IsolationId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-117">*IsolationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-118">ID d’isolation.</span><span class="sxs-lookup"><span data-stu-id="a5e18-118">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-119"> N \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-119">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-120">ID d’isolation.</span><span class="sxs-lookup"><span data-stu-id="a5e18-120">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-121">*RoundtripTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-121">*RoundTripTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-122">Durée de l’aller-retour.</span><span class="sxs-lookup"><span data-stu-id="a5e18-122">The round trip time.</span></span>

</dd> <dt>

<span data-ttu-id="a5e18-123">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a5e18-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e18-124">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5e18-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e18-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5e18-125">Return value</span></span>

<span data-ttu-id="a5e18-126">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a5e18-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a5e18-127">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a5e18-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-128">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a5e18-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-129">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="a5e18-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-130">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="a5e18-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-131">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="a5e18-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-132">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a5e18-132">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-133">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="a5e18-133">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-134">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a5e18-134">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a5e18-135">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a5e18-135">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a5e18-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5e18-136">Requirements</span></span>



| <span data-ttu-id="a5e18-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5e18-137">Requirement</span></span> | <span data-ttu-id="a5e18-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5e18-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e18-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5e18-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e18-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a5e18-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a5e18-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5e18-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e18-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a5e18-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a5e18-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a5e18-143">Namespace</span></span><br/>                | <span data-ttu-id="a5e18-144">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a5e18-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a5e18-145">MOF</span><span class="sxs-lookup"><span data-stu-id="a5e18-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5e18-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5e18-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5e18-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e18-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5e18-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5e18-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5e18-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5e18-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e18-150">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a5e18-150">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

