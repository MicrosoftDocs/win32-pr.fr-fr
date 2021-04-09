---
description: Récupère la liste de contrôle d’accès discrétionnaire (DACL) actuelle qui contrôle l’accès à la session interactive d’un ordinateur virtuel.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Méthode GetInteractiveSessionACL de la classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752236"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="eb000-103">Méthode GetInteractiveSessionACL de la \_ classe TerminalService MSVM</span><span class="sxs-lookup"><span data-stu-id="eb000-103">GetInteractiveSessionACL method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="eb000-104">Récupère la liste de *contrôle d’accès discrétionnaire* (DACL) actuelle qui contrôle l’accès à la session interactive d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eb000-104">Retrieves the current *discretionary access control list* (DACL) that controls access to the interactive session of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb000-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb000-105">Syntax</span></span>


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a><span data-ttu-id="eb000-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb000-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb000-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb000-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb000-108">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel dont la DACL sera récupérée.</span><span class="sxs-lookup"><span data-stu-id="eb000-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine whose DACL will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="eb000-109">*AccessControlList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb000-109">*AccessControlList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb000-110">Tableau de chaînes, chacune contenant une instance incorporée de la classe [**MSVM \_ InteractiveSessionACE**](msvm-interactivesessionace.md) qui représente une *entrée de contrôle d’accès* dans la liste DACL de session interactive de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="eb000-110">An array of strings, each containing an embedded instance of the [**Msvm\_InteractiveSessionACE**](msvm-interactivesessionace.md) class that represents an *access control entry* (ACE) in the virtual machine interactive session DACL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb000-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb000-111">Return value</span></span>

<span data-ttu-id="eb000-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb000-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="eb000-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="eb000-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-114">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="eb000-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-115">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="eb000-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-116">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="eb000-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-117">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="eb000-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-118">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="eb000-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-119">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="eb000-119">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="eb000-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="eb000-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-122">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="eb000-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="eb000-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="eb000-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eb000-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb000-124">Requirements</span></span>



| <span data-ttu-id="eb000-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb000-125">Requirement</span></span> | <span data-ttu-id="eb000-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb000-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb000-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb000-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eb000-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb000-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eb000-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb000-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eb000-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb000-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb000-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb000-131">Namespace</span></span><br/>                | <span data-ttu-id="eb000-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb000-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eb000-133">MOF</span><span class="sxs-lookup"><span data-stu-id="eb000-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb000-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb000-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb000-135">DLL</span><span class="sxs-lookup"><span data-stu-id="eb000-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb000-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb000-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb000-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb000-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb000-138">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="eb000-138">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




