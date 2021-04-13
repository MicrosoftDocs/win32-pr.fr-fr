---
description: Récupère le protecteur de clé pour un système virtuel.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Méthode GetKeyProtector de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321237"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="490ee-103">Méthode GetKeyProtector de la \_ classe securityservice MSVM</span><span class="sxs-lookup"><span data-stu-id="490ee-103">GetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="490ee-104">Récupère le protecteur de clé pour un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="490ee-104">Retrieves the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="490ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="490ee-105">Syntax</span></span>


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a><span data-ttu-id="490ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="490ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="490ee-107">*SecuritySettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="490ee-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="490ee-108">La chaîne contient une instance incorporée de la classe [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md) représentant les paramètres de sécurité d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="490ee-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="490ee-109">*Keyprotector* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="490ee-109">*KeyProtector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="490ee-110">Reçoit le tableau d’octets bruts qui contient le protecteur de clé en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="490ee-110">Receives the raw byte array that contains the key protector currently in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="490ee-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="490ee-111">Return value</span></span>

<span data-ttu-id="490ee-112">En cas de réussite, retourne 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="490ee-112">On success, returns a 0 or 4096.</span></span> <span data-ttu-id="490ee-113">Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="490ee-113">Otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="490ee-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="490ee-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="490ee-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="490ee-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="490ee-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="490ee-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="490ee-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="490ee-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="490ee-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="490ee-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="490ee-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="490ee-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="490ee-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="490ee-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="490ee-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="490ee-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="490ee-127">Requirements</span></span>



| <span data-ttu-id="490ee-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="490ee-128">Requirement</span></span> | <span data-ttu-id="490ee-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="490ee-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="490ee-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="490ee-130">Minimum supported client</span></span><br/> | <span data-ttu-id="490ee-131">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="490ee-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="490ee-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="490ee-132">Minimum supported server</span></span><br/> | <span data-ttu-id="490ee-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="490ee-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="490ee-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="490ee-134">Namespace</span></span><br/>                | <span data-ttu-id="490ee-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="490ee-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="490ee-136">MOF</span><span class="sxs-lookup"><span data-stu-id="490ee-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="490ee-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="490ee-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="490ee-138">DLL</span><span class="sxs-lookup"><span data-stu-id="490ee-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="490ee-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="490ee-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="490ee-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="490ee-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490ee-141">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="490ee-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




