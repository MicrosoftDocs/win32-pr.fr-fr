---
description: Récupère l’erreur.
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Méthode GetError de la classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7d8ff9c2c01bb21343b4859e2db2dbed7ad643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866397"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="c30dc-103">Méthode GetError de la \_ classe StorageJob MSVM</span><span class="sxs-lookup"><span data-stu-id="c30dc-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="c30dc-104">Récupère l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c30dc-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="c30dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c30dc-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="c30dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c30dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c30dc-107">*Erreur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c30dc-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c30dc-108">Erreur récupérée.</span><span class="sxs-lookup"><span data-stu-id="c30dc-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c30dc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c30dc-109">Return value</span></span>

<span data-ttu-id="c30dc-110">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c30dc-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c30dc-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c30dc-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-112">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c30dc-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-113">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c30dc-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-114">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c30dc-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-115">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c30dc-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-116">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c30dc-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-117">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c30dc-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-118">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c30dc-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-119">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c30dc-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-120">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c30dc-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-121">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c30dc-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c30dc-122">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c30dc-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c30dc-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c30dc-123">Requirements</span></span>



| <span data-ttu-id="c30dc-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c30dc-124">Requirement</span></span> | <span data-ttu-id="c30dc-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c30dc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c30dc-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c30dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c30dc-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c30dc-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c30dc-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c30dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c30dc-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c30dc-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c30dc-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c30dc-130">Namespace</span></span><br/>                | <span data-ttu-id="c30dc-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c30dc-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c30dc-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c30dc-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c30dc-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c30dc-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c30dc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c30dc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c30dc-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c30dc-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c30dc-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c30dc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c30dc-137">**MSVM \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="c30dc-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




