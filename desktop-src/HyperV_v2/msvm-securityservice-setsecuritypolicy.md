---
description: Définit le protecteur de clé pour un système virtuel.
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Méthode SetSecurityPolicy de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 35954f27d1184b714091058a35f32a6347d4ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530381"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="1f5ad-103">Méthode SetSecurityPolicy de la \_ classe securityservice MSVM</span><span class="sxs-lookup"><span data-stu-id="1f5ad-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="1f5ad-104">Définit le protecteur de clé pour un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f5ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f5ad-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1f5ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f5ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f5ad-107">*SecuritySettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f5ad-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f5ad-108">La chaîne contient une instance incorporée de la classe [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md) représentant les paramètres de sécurité d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-109">*SecurityPolicy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f5ad-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f5ad-110">Tableau d’octets bruts qui contient la stratégie de sécurité à définir.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f5ad-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f5ad-112">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="1f5ad-113">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f5ad-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f5ad-114">Return value</span></span>

<span data-ttu-id="1f5ad-115">Sur, Success, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1f5ad-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1f5ad-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f5ad-129">Requirements</span></span>



| <span data-ttu-id="1f5ad-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f5ad-130">Requirement</span></span> | <span data-ttu-id="1f5ad-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f5ad-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f5ad-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f5ad-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1f5ad-133">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f5ad-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1f5ad-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f5ad-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1f5ad-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1f5ad-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1f5ad-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1f5ad-136">Namespace</span></span><br/>                | <span data-ttu-id="1f5ad-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1f5ad-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1f5ad-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1f5ad-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f5ad-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f5ad-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f5ad-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1f5ad-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f5ad-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f5ad-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1f5ad-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f5ad-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f5ad-143">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




