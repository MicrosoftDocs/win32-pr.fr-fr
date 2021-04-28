---
description: 'Méthode GetError de la classe Msvm_StorageJob : récupère l’erreur.'
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
ms.openlocfilehash: 00434ef529b7f26755f52833ff6f37310c7dc210
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109597"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="58602-103">Méthode GetError de la \_ classe StorageJob MSVM</span><span class="sxs-lookup"><span data-stu-id="58602-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="58602-104">Récupère l’erreur.</span><span class="sxs-lookup"><span data-stu-id="58602-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="58602-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58602-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="58602-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58602-107">*Erreur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="58602-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58602-108">Erreur récupérée.</span><span class="sxs-lookup"><span data-stu-id="58602-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58602-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58602-109">Return value</span></span>

<span data-ttu-id="58602-110">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="58602-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="58602-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="58602-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58602-112">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="58602-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="58602-113">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="58602-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="58602-114">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="58602-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="58602-115">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="58602-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="58602-116">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="58602-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="58602-117">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="58602-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="58602-118">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="58602-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="58602-119">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="58602-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="58602-120">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="58602-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="58602-121">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="58602-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="58602-122">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="58602-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="58602-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58602-123">Requirements</span></span>



| <span data-ttu-id="58602-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58602-124">Requirement</span></span> | <span data-ttu-id="58602-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="58602-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58602-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58602-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58602-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="58602-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="58602-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58602-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58602-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58602-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="58602-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="58602-130">Namespace</span></span><br/>                | <span data-ttu-id="58602-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="58602-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="58602-132">MOF</span><span class="sxs-lookup"><span data-stu-id="58602-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58602-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58602-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58602-134">DLL</span><span class="sxs-lookup"><span data-stu-id="58602-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58602-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58602-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58602-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58602-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58602-137">**MSVM \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="58602-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




