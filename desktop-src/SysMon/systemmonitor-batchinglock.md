---
title: SystemMonitor.Batméthode chingLock
description: Verrouille le moniteur système pour l’empêcher d’échantillonner les données de compteur à partir du nouveau compteur ou fichier journal.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Méthode BatchingLock SysMon
- Méthode BatchingLock SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511569"
---
# <a name="systemmonitorbatchinglock-method"></a><span data-ttu-id="541a9-106">SystemMonitor.Batméthode chingLock</span><span class="sxs-lookup"><span data-stu-id="541a9-106">SystemMonitor.BatchingLock method</span></span>

<span data-ttu-id="541a9-107">Verrouille le moniteur système pour l’empêcher d’échantillonner les données de compteur à partir du nouveau compteur ou fichier journal.</span><span class="sxs-lookup"><span data-stu-id="541a9-107">Locks the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="541a9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="541a9-108">Syntax</span></span>


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a><span data-ttu-id="541a9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="541a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541a9-110">*verrou* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="541a9-110">*lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541a9-111">Affectez la valeur true pour verrouiller le moniteur système et l’empêcher d’échantillonner les données de compteur à partir du nouveau compteur ou fichier journal.</span><span class="sxs-lookup"><span data-stu-id="541a9-111">Set to True to lock the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span> <span data-ttu-id="541a9-112">Affectez la valeur false pour supprimer le verrou.</span><span class="sxs-lookup"><span data-stu-id="541a9-112">Set to False to remove the lock.</span></span>

</dd> <dt>

<span data-ttu-id="541a9-113">*batchReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="541a9-113">*batchReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541a9-114">Identifie la source des données que vous verrouillez.</span><span class="sxs-lookup"><span data-stu-id="541a9-114">Identifies the source of the data that you are locking.</span></span> <span data-ttu-id="541a9-115">Utilisez la même valeur de raison lorsque vous verrouillez et déverrouillez la ressource.</span><span class="sxs-lookup"><span data-stu-id="541a9-115">Use the same reason value when locking and unlocking the resource.</span></span> <span data-ttu-id="541a9-116">Pour connaître les valeurs possibles, consultez l’énumération [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .</span><span class="sxs-lookup"><span data-stu-id="541a9-116">For possible values, see the [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541a9-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="541a9-117">Return value</span></span>

<span data-ttu-id="541a9-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="541a9-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="541a9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="541a9-119">Remarks</span></span>

<span data-ttu-id="541a9-120">Vous devez appeler cette méthode deux fois, une fois pour verrouiller la source (true) et une fois pour déverrouiller la source (false).</span><span class="sxs-lookup"><span data-stu-id="541a9-120">You must call this method twice, once to lock the source (True) and once to unlock the source (False).</span></span>

<span data-ttu-id="541a9-121">Vous ne pouvez placer qu’un seul verrou.</span><span class="sxs-lookup"><span data-stu-id="541a9-121">You can place only one lock.</span></span> <span data-ttu-id="541a9-122">Par exemple, si vous définissez le verrou pour SysmonBatchAddFiles et que vous effectuez ensuite un deuxième appel à l’aide de SysmonBatchAddCounters comme raison, le deuxième appel supprime le verrou placé par le premier appel.</span><span class="sxs-lookup"><span data-stu-id="541a9-122">For example, if you set the lock for SysmonBatchAddFiles and then make a second call using SysmonBatchAddCounters as the reason, the second call removes the lock placed by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="541a9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="541a9-123">Requirements</span></span>



| <span data-ttu-id="541a9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="541a9-124">Requirement</span></span> | <span data-ttu-id="541a9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="541a9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="541a9-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="541a9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="541a9-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="541a9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="541a9-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="541a9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="541a9-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="541a9-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="541a9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="541a9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="541a9-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="541a9-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="541a9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="541a9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541a9-133">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="541a9-133">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





