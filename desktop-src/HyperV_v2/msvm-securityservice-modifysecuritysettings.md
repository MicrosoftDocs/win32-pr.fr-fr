---
description: Modifie les paramètres de sécurité actuels d’un ordinateur virtuel.
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Méthode ModifySecuritySettings de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4422f04be1833d66280392704630fcb670eba810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520203"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="5bbb9-103">Méthode ModifySecuritySettings de la \_ classe securityservice MSVM</span><span class="sxs-lookup"><span data-stu-id="5bbb9-103">ModifySecuritySettings method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="5bbb9-104">Modifie les paramètres de sécurité actuels d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-104">Modifies the current security settings of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bbb9-105">Syntax</span></span>


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5bbb9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bbb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbb9-107">*SecuritySettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bbb9-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbb9-108">Nouvelles données de paramètre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-108">The new security setting data.</span></span>

</dd> <dt>

<span data-ttu-id="5bbb9-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5bbb9-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbb9-110">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="5bbb9-111">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbb9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bbb9-112">Return value</span></span>

<span data-ttu-id="5bbb9-113">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5bbb9-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-120">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-123">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5bbb9-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5bbb9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bbb9-125">Requirements</span></span>



| <span data-ttu-id="5bbb9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bbb9-126">Requirement</span></span> | <span data-ttu-id="5bbb9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bbb9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbb9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bbb9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbb9-129">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bbb9-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5bbb9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bbb9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbb9-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5bbb9-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5bbb9-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5bbb9-132">Namespace</span></span><br/>                | <span data-ttu-id="5bbb9-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5bbb9-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5bbb9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5bbb9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bbb9-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bbb9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bbb9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5bbb9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bbb9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5bbb9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5bbb9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bbb9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbb9-139">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="5bbb9-139">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




