---
description: Octroie l’accès à la session interactive de l’ordinateur virtuel à la liste de confiance spécifiée.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Méthode GrantInteractiveSessionAccess de la classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8bd49805b5fdc5545a81e4f0b816fe35a6c37b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520507"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="85920-103">Méthode GrantInteractiveSessionAccess de la \_ classe TerminalService MSVM</span><span class="sxs-lookup"><span data-stu-id="85920-103">GrantInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="85920-104">Octroie l’accès à la session interactive de l’ordinateur virtuel à la liste de confiance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="85920-104">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="85920-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85920-105">Syntax</span></span>


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="85920-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85920-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85920-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85920-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85920-108">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel auquel l’accès sera accordé.</span><span class="sxs-lookup"><span data-stu-id="85920-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to which access will be granted.</span></span>

</dd> <dt>

<span data-ttu-id="85920-109">*Des approbations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85920-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85920-110">Tableau de chaînes, chacune identifiant un tiers de confiance qui sera autorisé à accéder à la session interactive de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="85920-110">An array of strings, each identifying a trustee that will be granted access to the interactive session of the virtual machine.</span></span> <span data-ttu-id="85920-111">Les identificateurs de tiers de confiance doivent être spécifiés au format compatible SAM Windows ou au format de chaîne SID Windows.</span><span class="sxs-lookup"><span data-stu-id="85920-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="85920-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="85920-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85920-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85920-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85920-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85920-114">Return value</span></span>

<span data-ttu-id="85920-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="85920-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="85920-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="85920-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85920-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="85920-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85920-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="85920-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85920-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="85920-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85920-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="85920-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85920-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="85920-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="85920-122">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="85920-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="85920-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="85920-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85920-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="85920-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="85920-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="85920-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="85920-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="85920-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="85920-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85920-127">Requirements</span></span>



| <span data-ttu-id="85920-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85920-128">Requirement</span></span> | <span data-ttu-id="85920-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="85920-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85920-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85920-130">Minimum supported client</span></span><br/> | <span data-ttu-id="85920-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85920-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="85920-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85920-132">Minimum supported server</span></span><br/> | <span data-ttu-id="85920-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85920-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85920-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="85920-134">Namespace</span></span><br/>                | <span data-ttu-id="85920-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="85920-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85920-136">MOF</span><span class="sxs-lookup"><span data-stu-id="85920-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85920-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85920-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85920-138">DLL</span><span class="sxs-lookup"><span data-stu-id="85920-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85920-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85920-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85920-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85920-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85920-141">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="85920-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

