---
title: SystemMonitor. Relog, méthode
description: Rejournalise les données de compteur dans un nouveau fichier. Vous pouvez également utiliser cette méthode pour spécifier un nouveau type de fichier et réduire le nombre d’échantillons contenus dans le fichier journal.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Relog, méthode SysMon
- Relog, méthode SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103417"
---
# <a name="systemmonitorrelog-method"></a><span data-ttu-id="b26f7-107">SystemMonitor. Relog, méthode</span><span class="sxs-lookup"><span data-stu-id="b26f7-107">SystemMonitor.Relog method</span></span>

<span data-ttu-id="b26f7-108">Rejournalise les données de compteur dans un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="b26f7-108">Relogs the counter data to a new file.</span></span> <span data-ttu-id="b26f7-109">Vous pouvez également utiliser cette méthode pour spécifier un nouveau type de fichier et réduire le nombre d’échantillons contenus dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="b26f7-109">You can also use this method to specify a new file type and to reduce the number of samples contained in the log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b26f7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b26f7-110">Syntax</span></span>


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="b26f7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b26f7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b26f7-112">*nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b26f7-112">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b26f7-113">Chemin d’accès du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="b26f7-113">File path of the log file.</span></span> <span data-ttu-id="b26f7-114">Vous pouvez spécifier le chemin d’accès en tant que chemin d’accès absolu, relatif ou UNC.</span><span class="sxs-lookup"><span data-stu-id="b26f7-114">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="b26f7-115">L’extension de nom de fichier journal doit être. BLG,. TSV ou. csv.</span><span class="sxs-lookup"><span data-stu-id="b26f7-115">The log file name extension must be either .blg, .tsv, or .csv.</span></span> <span data-ttu-id="b26f7-116">Si un dossier du chemin d’accès n’existe pas, SYSMON le crée.</span><span class="sxs-lookup"><span data-stu-id="b26f7-116">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="b26f7-117">Si le fichier existe, le fichier est remplacé.</span><span class="sxs-lookup"><span data-stu-id="b26f7-117">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="b26f7-118">SYSMON applique les listes de contrôle d’accès par défaut à partir du répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="b26f7-118">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="b26f7-119">*filetype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b26f7-119">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b26f7-120">Format des données de compteur enregistrées dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="b26f7-120">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="b26f7-121">Vous pouvez spécifier [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** ou **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="b26f7-121">You can specify either [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv**, or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> <dt>

<span data-ttu-id="b26f7-122">*filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b26f7-122">*filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b26f7-123">Nombre d’échantillons des anciens fichiers journaux à enregistrer dans le nouveau fichier journal.</span><span class="sxs-lookup"><span data-stu-id="b26f7-123">Number of samples from the old log files to save in the new log file.</span></span> <span data-ttu-id="b26f7-124">Spécifiez 1 pour enregistrer chaque échantillon des anciens fichiers dans les nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="b26f7-124">Specify 1 to save every sample from the old files to the new files.</span></span> <span data-ttu-id="b26f7-125">Spécifiez 2 pour enregistrer un des deux échantillons de l’ancien fichier.</span><span class="sxs-lookup"><span data-stu-id="b26f7-125">Specify 2 to save one out of every two samples from the old file.</span></span> <span data-ttu-id="b26f7-126">Spécifiez 3 pour enregistrer un des trois échantillons de l’ancien fichier.</span><span class="sxs-lookup"><span data-stu-id="b26f7-126">Specify 3 to save one out of every three samples from the old file.</span></span> <span data-ttu-id="b26f7-127">Et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="b26f7-127">And so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b26f7-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b26f7-128">Return value</span></span>

<span data-ttu-id="b26f7-129">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b26f7-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b26f7-130">Notes</span><span class="sxs-lookup"><span data-stu-id="b26f7-130">Remarks</span></span>

<span data-ttu-id="b26f7-131">Cette méthode utilise les fichiers journaux contenus dans la collection [**systemmonitor. LogFiles**](systemmonitor-logfiles.md) pour reconsigner les données de compteur.</span><span class="sxs-lookup"><span data-stu-id="b26f7-131">This method uses the log files contained in the [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) collection to relog the counter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b26f7-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b26f7-132">Requirements</span></span>



| <span data-ttu-id="b26f7-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b26f7-133">Requirement</span></span> | <span data-ttu-id="b26f7-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b26f7-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b26f7-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b26f7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b26f7-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b26f7-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b26f7-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b26f7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b26f7-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b26f7-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b26f7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b26f7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b26f7-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b26f7-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b26f7-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b26f7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b26f7-142">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="b26f7-142">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="b26f7-143">**SystemMonitor. SaveAs**</span><span class="sxs-lookup"><span data-stu-id="b26f7-143">**SystemMonitor.SaveAs**</span></span>](systemmonitor-saveas.md)
</dt> </dl>

 

 





