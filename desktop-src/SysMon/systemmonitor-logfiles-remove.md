---
title: LogFiles. Remove, méthode
description: Supprime l’instance LogFileItem spécifiée de la collection.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Supprimer la méthode SysMon
- Remove, méthode SysMon, classe LogFiles
- LogFiles, classe SysMon, Remove, méthode
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742933"
---
# <a name="logfilesremove-method"></a><span data-ttu-id="507c0-106">LogFiles. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="507c0-106">LogFiles.Remove method</span></span>

<span data-ttu-id="507c0-107">Supprime l’instance [**LogFileItem**](logfileitem.md) spécifiée de la collection.</span><span class="sxs-lookup"><span data-stu-id="507c0-107">Removes the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="507c0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="507c0-108">Syntax</span></span>


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="507c0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="507c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="507c0-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="507c0-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="507c0-111">Index entier du fichier journal à supprimer de la collection.</span><span class="sxs-lookup"><span data-stu-id="507c0-111">Integer index of the log file to remove from the collection.</span></span> <span data-ttu-id="507c0-112">L’index est de base un.</span><span class="sxs-lookup"><span data-stu-id="507c0-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="507c0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="507c0-113">Return value</span></span>

<span data-ttu-id="507c0-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="507c0-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="507c0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="507c0-115">Remarks</span></span>

<span data-ttu-id="507c0-116">**Avant Windows Vista :** Vous ne pouvez pas supprimer les fichiers journaux de la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="507c0-116">**Prior to Windows Vista:** You cannot remove log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="507c0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="507c0-117">Requirements</span></span>



| <span data-ttu-id="507c0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="507c0-118">Requirement</span></span> | <span data-ttu-id="507c0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="507c0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="507c0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="507c0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="507c0-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="507c0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="507c0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="507c0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="507c0-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="507c0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="507c0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="507c0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="507c0-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="507c0-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507c0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="507c0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507c0-127">LogFiles</span><span class="sxs-lookup"><span data-stu-id="507c0-127">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="507c0-128">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="507c0-128">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="507c0-129">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="507c0-129">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





