---
description: Révoque l’accès à la session interactive de l’ordinateur virtuel à partir de la liste de confiance spécifiée.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Méthode RevokeInteractiveSessionAccess de la classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756501"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="c50b5-103">Méthode RevokeInteractiveSessionAccess de la \_ classe TerminalService MSVM</span><span class="sxs-lookup"><span data-stu-id="c50b5-103">RevokeInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="c50b5-104">Révoque l’accès à la session interactive de l’ordinateur virtuel à partir de la liste de confiance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c50b5-104">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50b5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c50b5-105">Syntax</span></span>


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c50b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c50b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50b5-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c50b5-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c50b5-108">Référence à une instance de la classe [**CIM \_ CIM**](cim-computersystem.md) qui représente l’ordinateur virtuel sur lequel l’accès sera révoqué.</span><span class="sxs-lookup"><span data-stu-id="c50b5-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to which access will be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="c50b5-109">*Des approbations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c50b5-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c50b5-110">Tableau de chaînes, chacune identifiant un tiers de confiance dont les droits d’accès seront révoqués.</span><span class="sxs-lookup"><span data-stu-id="c50b5-110">An array of strings, each identifying a trustee whose access rights will be revoked.</span></span> <span data-ttu-id="c50b5-111">Les identificateurs de tiers de confiance doivent être spécifiés au format compatible SAM Windows ou au format de chaîne SID Windows.</span><span class="sxs-lookup"><span data-stu-id="c50b5-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="c50b5-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c50b5-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c50b5-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c50b5-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50b5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c50b5-114">Return value</span></span>

<span data-ttu-id="c50b5-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c50b5-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c50b5-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c50b5-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="c50b5-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="c50b5-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="c50b5-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="c50b5-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="c50b5-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-122">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="c50b5-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c50b5-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c50b5-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c50b5-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c50b5-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c50b5-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c50b5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c50b5-127">Requirements</span></span>



| <span data-ttu-id="c50b5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c50b5-128">Requirement</span></span> | <span data-ttu-id="c50b5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c50b5-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c50b5-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c50b5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c50b5-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c50b5-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c50b5-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c50b5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c50b5-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c50b5-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c50b5-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c50b5-134">Namespace</span></span><br/>                | <span data-ttu-id="c50b5-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c50b5-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c50b5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c50b5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c50b5-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c50b5-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c50b5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c50b5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c50b5-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c50b5-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c50b5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c50b5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50b5-141">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="c50b5-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

