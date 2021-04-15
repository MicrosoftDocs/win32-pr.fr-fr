---
title: SystemMonitor. LogFileName, propriété
description: Récupère ou définit le nom d’un fichier journal à utiliser comme source des valeurs de compteur affichées dans le moniteur système.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Propriété LogFileName SysMon
- Propriété LogFileName SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété LogFileName
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384704"
---
# <a name="systemmonitorlogfilename-property"></a><span data-ttu-id="f456f-106">SystemMonitor. LogFileName, propriété</span><span class="sxs-lookup"><span data-stu-id="f456f-106">SystemMonitor.LogFileName property</span></span>

<span data-ttu-id="f456f-107">Récupère ou définit le nom d’un fichier journal à utiliser comme source des valeurs de compteur affichées dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="f456f-107">Retrieves or sets the name of a log file to use as the source of counter values displayed in the System Monitor.</span></span>

> [!Note]  
> <span data-ttu-id="f456f-108">Cette propriété a été rendue obsolète par la propriété [**LogFiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="f456f-108">This property has been made obsolete by the [**LogFiles**](systemmonitor-logfiles.md) property.</span></span>

 

<span data-ttu-id="f456f-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f456f-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f456f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f456f-110">Syntax</span></span>


```VB
Property LogFileName As String
```



## <a name="property-value"></a><span data-ttu-id="f456f-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f456f-111">Property value</span></span>

<span data-ttu-id="f456f-112">Chemin d’accès au fichier journal.</span><span class="sxs-lookup"><span data-stu-id="f456f-112">Path to the log file.</span></span> <span data-ttu-id="f456f-113">Vous pouvez spécifier un chemin d’accès absolu, relatif ou UNC.</span><span class="sxs-lookup"><span data-stu-id="f456f-113">You can specify an absolute, relative, or UNC path.</span></span> <span data-ttu-id="f456f-114">L’extension de nom de fichier journal doit être. csv,. TSV ou. BLG.</span><span class="sxs-lookup"><span data-stu-id="f456f-114">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

## <a name="exceptions"></a><span data-ttu-id="f456f-115">Exceptions</span><span class="sxs-lookup"><span data-stu-id="f456f-115">Exceptions</span></span>



| <span data-ttu-id="f456f-116">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="f456f-116">Exception type</span></span>                                  | <span data-ttu-id="f456f-117">Condition</span><span class="sxs-lookup"><span data-stu-id="f456f-117">Condition</span></span>                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f456f-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="f456f-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="f456f-119">Impossible de trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="f456f-119">Unable to find the specified file.</span></span> <span data-ttu-id="f456f-120">La valeur de Err. Number est 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="f456f-120">The Err.Number value is 0xC0000BD1.</span></span> |
| <span data-ttu-id="f456f-121">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="f456f-121">**System.ArgumentException**</span></span>                    | <span data-ttu-id="f456f-122">Vous ne pouvez pas spécifier une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="f456f-122">You cannot specify an empty string.</span></span>                                    |



 

## <a name="remarks"></a><span data-ttu-id="f456f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f456f-123">Remarks</span></span>

<span data-ttu-id="f456f-124">Cette propriété retourne le nom du fichier journal à partir du premier membre de la collection [**LogFiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="f456f-124">This property returns the log file name from the first member of the [**LogFiles**](systemmonitor-logfiles.md) collection.</span></span>

<span data-ttu-id="f456f-125">La définition de cette propriété échoue si la collection [**LogFiles**](systemmonitor-logfiles.md) contient un ou plusieurs membres.</span><span class="sxs-lookup"><span data-stu-id="f456f-125">Setting this property will fail if the [**LogFiles**](systemmonitor-logfiles.md) collection contains one or more members.</span></span>

<span data-ttu-id="f456f-126">Vous devez utiliser l’outil Logman.exe ou le composant logiciel enfichable MMC Perfmon. msc pour générer les fichiers journaux que vous ajoutez à ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="f456f-126">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="f456f-127">Pour Perfmon. msc, les journaux de compteur se trouvent sous **journaux et alertes de performance**.</span><span class="sxs-lookup"><span data-stu-id="f456f-127">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="f456f-128">Pour plus d’informations sur l’utilisation de Logman.exe ou Perfmon. msc, recherchez logman ou à l’aide de performances, respectivement, dans le **Centre d’aide et de support**.</span><span class="sxs-lookup"><span data-stu-id="f456f-128">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f456f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f456f-129">Requirements</span></span>



| <span data-ttu-id="f456f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f456f-130">Requirement</span></span> | <span data-ttu-id="f456f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f456f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f456f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f456f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f456f-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f456f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f456f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f456f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f456f-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f456f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f456f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f456f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f456f-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f456f-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f456f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f456f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f456f-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="f456f-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="f456f-140">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="f456f-140">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





