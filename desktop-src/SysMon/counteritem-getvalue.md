---
title: CounterItem. GetValue, méthode
description: Récupère la dernière valeur du compteur.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- GetValue, méthode SysMon
- GetValue, méthode SysMon, CounterItem, classe
- CounterItem classe SysMon, GetValue, méthode
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518098"
---
# <a name="counteritemgetvalue-method"></a><span data-ttu-id="f836e-106">CounterItem. GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="f836e-106">CounterItem.GetValue method</span></span>

<span data-ttu-id="f836e-107">Récupère la dernière valeur du compteur.</span><span class="sxs-lookup"><span data-stu-id="f836e-107">Retrieves the last value of the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f836e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f836e-108">Syntax</span></span>


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="f836e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f836e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f836e-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f836e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f836e-111">Dernière valeur échantillonnée du compteur.</span><span class="sxs-lookup"><span data-stu-id="f836e-111">Last sampled value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="f836e-112">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f836e-112">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f836e-113">Indique si la valeur est valide.</span><span class="sxs-lookup"><span data-stu-id="f836e-113">Indicates if the value is valid.</span></span>



| <span data-ttu-id="f836e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f836e-114">Value</span></span>                                                                                              | <span data-ttu-id="f836e-115">Signification</span><span class="sxs-lookup"><span data-stu-id="f836e-115">Meaning</span></span>                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="f836e-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f836e-116"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f836e-117">La valeur est valide.</span><span class="sxs-lookup"><span data-stu-id="f836e-117">The value is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="f836e-118"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="f836e-118"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="f836e-119">La valeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f836e-119">The value is not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f836e-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f836e-120">Return value</span></span>

<span data-ttu-id="f836e-121">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f836e-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f836e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f836e-122">Remarks</span></span>

<span data-ttu-id="f836e-123">Si la source des données de compteur provient d’un fichier journal, la valeur est la dernière valeur de compteur dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="f836e-123">If the source of the counter data is from a log file, the value is the last counter value in the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="f836e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f836e-124">Requirements</span></span>



| <span data-ttu-id="f836e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f836e-125">Requirement</span></span> | <span data-ttu-id="f836e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f836e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f836e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f836e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f836e-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f836e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f836e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f836e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f836e-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f836e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f836e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f836e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f836e-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f836e-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f836e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f836e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f836e-134">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="f836e-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="f836e-135">**CounterItem.GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="f836e-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="f836e-136">**CounterItem. Value**</span><span class="sxs-lookup"><span data-stu-id="f836e-136">**CounterItem.Value**</span></span>](counteritem-value.md)
</dt> </dl>

 

 





