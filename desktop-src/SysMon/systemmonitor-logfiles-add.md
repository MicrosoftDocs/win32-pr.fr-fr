---
title: LogFiles. Add, méthode
description: Ajoute un fichier journal à la collection.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Ajouter la méthode SysMon
- Add, méthode SysMon, classe LogFiles
- LogFiles, classe SysMon, méthode Add
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103828"
---
# <a name="logfilesadd-method"></a><span data-ttu-id="c4064-106">LogFiles. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="c4064-106">LogFiles.Add method</span></span>

<span data-ttu-id="c4064-107">Ajoute un fichier journal à la collection.</span><span class="sxs-lookup"><span data-stu-id="c4064-107">Adds a log file to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4064-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4064-108">Syntax</span></span>


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a><span data-ttu-id="c4064-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4064-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4064-110">*nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4064-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4064-111">Chemin d’accès au fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c4064-111">Path to the log file.</span></span> <span data-ttu-id="c4064-112">Vous pouvez spécifier le chemin d’accès en tant que chemin d’accès absolu, relatif ou UNC.</span><span class="sxs-lookup"><span data-stu-id="c4064-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="c4064-113">L’extension de nom de fichier journal doit être. csv,. TSV ou. BLG.</span><span class="sxs-lookup"><span data-stu-id="c4064-113">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4064-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c4064-114">Remarks</span></span>

<span data-ttu-id="c4064-115">Vous devez utiliser l’outil Logman.exe ou le composant logiciel enfichable MMC Perfmon. msc pour générer les fichiers journaux que vous ajoutez à ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="c4064-115">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="c4064-116">Pour Perfmon. msc, les journaux de compteur se trouvent sous **journaux et alertes de performance**.</span><span class="sxs-lookup"><span data-stu-id="c4064-116">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="c4064-117">Pour plus d’informations sur l’utilisation de Logman.exe ou Perfmon. msc, recherchez logman ou à l’aide de performances, respectivement, dans le **Centre d’aide et de support**.</span><span class="sxs-lookup"><span data-stu-id="c4064-117">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

<span data-ttu-id="c4064-118">**Avant Windows Vista :** Vous ne pouvez pas ajouter de fichiers journaux à la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="c4064-118">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="c4064-119">Tout d’abord, définissez **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonNullDataSource**, ajoutez vos fichiers journaux et compteurs, puis définissez **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="c4064-119">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4064-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4064-120">Requirements</span></span>



| <span data-ttu-id="c4064-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4064-121">Requirement</span></span> | <span data-ttu-id="c4064-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4064-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4064-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4064-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c4064-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4064-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c4064-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4064-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c4064-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4064-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4064-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c4064-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4064-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c4064-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4064-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4064-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4064-130">LogFiles</span><span class="sxs-lookup"><span data-stu-id="c4064-130">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="c4064-131">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="c4064-131">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="c4064-132">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="c4064-132">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





