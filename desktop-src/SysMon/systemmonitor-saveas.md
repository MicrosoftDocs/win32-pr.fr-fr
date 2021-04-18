---
title: SystemMonitor. SaveAs, méthode
description: Enregistre les valeurs de compteur de la vue du graphique dans un fichier journal.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs, méthode SysMon
- SaveAs, méthode SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527157"
---
# <a name="systemmonitorsaveas-method"></a><span data-ttu-id="3c5de-106">SystemMonitor. SaveAs, méthode</span><span class="sxs-lookup"><span data-stu-id="3c5de-106">SystemMonitor.SaveAs method</span></span>

<span data-ttu-id="3c5de-107">Enregistre les valeurs de compteur de la vue du graphique dans un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="3c5de-107">Saves the counter values in the graph view to a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c5de-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c5de-108">Syntax</span></span>


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a><span data-ttu-id="3c5de-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c5de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c5de-110">*nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c5de-110">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c5de-111">Chemin d’accès du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="3c5de-111">File path of the log file.</span></span> <span data-ttu-id="3c5de-112">Vous pouvez spécifier le chemin d’accès en tant que chemin d’accès absolu, relatif ou UNC.</span><span class="sxs-lookup"><span data-stu-id="3c5de-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="3c5de-113">L’extension de nom de fichier journal doit être. TSV ou. htm.</span><span class="sxs-lookup"><span data-stu-id="3c5de-113">The log file name extension must be either .tsv or .htm.</span></span> <span data-ttu-id="3c5de-114">Si un dossier du chemin d’accès n’existe pas, SYSMON le crée.</span><span class="sxs-lookup"><span data-stu-id="3c5de-114">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="3c5de-115">Si le fichier existe, le fichier est remplacé.</span><span class="sxs-lookup"><span data-stu-id="3c5de-115">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="3c5de-116">SYSMON applique les listes de contrôle d’accès par défaut à partir du répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="3c5de-116">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="3c5de-117">*filetype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c5de-117">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c5de-118">Format des données de compteur enregistrées dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="3c5de-118">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="3c5de-119">Vous pouvez spécifier [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) ou **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="3c5de-119">You can specify either [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c5de-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c5de-120">Return value</span></span>

<span data-ttu-id="3c5de-121">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3c5de-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c5de-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3c5de-122">Remarks</span></span>

<span data-ttu-id="3c5de-123">Seules les données de compteur visibles dans la vue du graphique sont enregistrées (pour le nombre réel de points de données enregistrés, consultez [**systemmonitor. DataPointCount**](systemmonitor-datapointcount.md)).</span><span class="sxs-lookup"><span data-stu-id="3c5de-123">Only the counter data visible in the graph view is saved (for the actual number of data points saved, see [**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c5de-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c5de-124">Requirements</span></span>



| <span data-ttu-id="3c5de-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c5de-125">Requirement</span></span> | <span data-ttu-id="3c5de-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c5de-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5de-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c5de-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5de-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c5de-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c5de-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c5de-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5de-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c5de-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c5de-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3c5de-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c5de-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3c5de-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c5de-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c5de-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5de-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3c5de-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="3c5de-135">**SystemMonitor. relog**</span><span class="sxs-lookup"><span data-stu-id="3c5de-135">**SystemMonitor.Relog**</span></span>](systemmonitor-relog.md)
</dt> </dl>

 

 





