---
title: LogFiles, objet (Isysmon.h)
description: Utilisez cette classe pour gérer une collection d’un ou de plusieurs fichiers journaux qui contiennent des données de compteurs de performances. Pour récupérer cet objet, appelez SystemMonitor. LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- LogFiles, objet SysMon
- LogFiles, objet SysMon, Description
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464198"
---
# <a name="logfiles-object"></a><span data-ttu-id="b3109-105">LogFiles (objet)</span><span class="sxs-lookup"><span data-stu-id="b3109-105">LogFiles object</span></span>

<span data-ttu-id="b3109-106">Utilisez cette classe pour gérer une collection d’un ou de plusieurs fichiers journaux qui contiennent des données de compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="b3109-106">Use this class to manage a collection of one or more log files that contain performance counter data.</span></span>

<span data-ttu-id="b3109-107">Pour récupérer cet objet, appelez [**systemmonitor. LogFiles**](systemmonitor-logfiles.md).</span><span class="sxs-lookup"><span data-stu-id="b3109-107">To retrieve this object, call [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).</span></span>

## <a name="members"></a><span data-ttu-id="b3109-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b3109-108">Members</span></span>

<span data-ttu-id="b3109-109">L’objet **LogFiles** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b3109-109">The **LogFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="b3109-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b3109-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b3109-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3109-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b3109-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b3109-112">Methods</span></span>

<span data-ttu-id="b3109-113">L’objet **LogFiles** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b3109-113">The **LogFiles** object has these methods.</span></span>



| <span data-ttu-id="b3109-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="b3109-114">Method</span></span>                                          | <span data-ttu-id="b3109-115">Description</span><span class="sxs-lookup"><span data-stu-id="b3109-115">Description</span></span>                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3109-116">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="b3109-116">**Add**</span></span>](systemmonitor-logfiles-add.md)       | <span data-ttu-id="b3109-117">Ajoute une instance [**LogFileItem**](logfileitem.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="b3109-117">Adds a [**LogFileItem**](logfileitem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="b3109-118">**Installez**</span><span class="sxs-lookup"><span data-stu-id="b3109-118">**Remove**</span></span>](systemmonitor-logfiles-remove.md) | <span data-ttu-id="b3109-119">Supprime une instance [**LogFileItem**](logfileitem.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="b3109-119">Removes a [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b3109-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3109-120">Properties</span></span>

<span data-ttu-id="b3109-121">L’objet **LogFiles** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3109-121">The **LogFiles** object has these properties.</span></span>



| <span data-ttu-id="b3109-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="b3109-122">Property</span></span>                                                 | <span data-ttu-id="b3109-123">Description</span><span class="sxs-lookup"><span data-stu-id="b3109-123">Description</span></span>                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3109-124">**Saut**</span><span class="sxs-lookup"><span data-stu-id="b3109-124">**Count**</span></span>](systemmonitor-logfiles-count.md)<br/> | <span data-ttu-id="b3109-125">Récupère le nombre d’instances de [**LogFileItem**](logfileitem.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="b3109-125">Retrieves the number of [**LogFileItem**](logfileitem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="b3109-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b3109-126">**Item**</span></span>](systemmonitor-logfiles-item.md)<br/>   | <span data-ttu-id="b3109-127">Récupère l’instance [**LogFileItem**](logfileitem.md) spécifiée de la collection.</span><span class="sxs-lookup"><span data-stu-id="b3109-127">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3109-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b3109-128">Remarks</span></span>

<span data-ttu-id="b3109-129">Pour que SYSMON affiche des compteurs de performances à partir d’un fichier journal, définissez [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) sur [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="b3109-129">To have SYSMON display performance counters from a log file, set [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="b3109-130">Après avoir ajouté les fichiers journaux à la collection, utilisez la collection de [**compteurs**](counters.md) pour spécifier les données de compteurs que vous souhaitez lire à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="b3109-130">After adding the log files to the collection, use the [**Counters**](counters.md) collection to specify the counters data that you want to read from the log files.</span></span> <span data-ttu-id="b3109-131">Notez que si **systemmonitor. DataSourceType** est défini sur **DataSourceTypeConstants.sysmonLogFiles**, SYSMON rééchantillonnera les fichiers journaux chaque fois que vous ajouterez un fichier journal ou un compteur à leurs collections respectives.</span><span class="sxs-lookup"><span data-stu-id="b3109-131">Note that if **SystemMonitor.DataSourceType** is set to **DataSourceTypeConstants.sysmonLogFiles**, SYSMON will resample the log files each time you add a log file or counter to their respective collections.</span></span>

<span data-ttu-id="b3109-132">**Avant Windows Vista :** Vous ne pouvez pas ajouter de fichiers journaux à la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="b3109-132">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="b3109-133">Tout d’abord, définissez **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonNullDataSource**, ajoutez vos fichiers journaux et compteurs, puis définissez **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="b3109-133">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

<span data-ttu-id="b3109-134">Les propriétés [**systemmonitor. LogViewStart**](systemmonitor-logviewstart.md) et [**systemmonitor. LogViewStop**](systemmonitor-logviewstop.md) spécifient la plage de valeurs échantillonnées dans les fichiers journaux du graphique.</span><span class="sxs-lookup"><span data-stu-id="b3109-134">The [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties specify the range of sampled values from the log files to graph.</span></span> <span data-ttu-id="b3109-135">SYSMON Graph n’affiche qu’une seule vue des données du fichier journal (la vue du graphique ne fait pas défiler l’activité en cours sur l’ordinateur).</span><span class="sxs-lookup"><span data-stu-id="b3109-135">SYSMON graphs only one view worth of data from the log file (the graph view does not scroll as it does when graphing the current activity of the computer).</span></span> <span data-ttu-id="b3109-136">Si les données échantillonnées dépassent ce qui peut être affiché sur une seule vue de graphique, SYSMON compresse les données échantillonnées (chaque point représenté par un graphique représente la moyenne de plusieurs valeurs échantillonnées) pour s’adapter à toutes les données échantillonnées des fichiers journaux sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="b3109-136">If the sampled data exceeds what can be shown on a single graph view, SYSMON compresses the sampled data (each graphed point represents the average of multiple sampled values) to fit all the sampled data from the log files on the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3109-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3109-137">Requirements</span></span>



| <span data-ttu-id="b3109-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3109-138">Requirement</span></span> | <span data-ttu-id="b3109-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3109-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3109-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3109-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b3109-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3109-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b3109-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3109-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b3109-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3109-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3109-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3109-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3109-145"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3109-145"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b3109-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b3109-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3109-147"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b3109-147"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





