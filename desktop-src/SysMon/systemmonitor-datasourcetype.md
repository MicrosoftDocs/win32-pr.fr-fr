---
title: SystemMonitor propriété DataSourceType
description: Récupère ou définit la source des données du compteur de performance.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Propriété DataSourceType SysMon
- Propriété DataSourceType SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, propriété DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033075"
---
# <a name="systemmonitordatasourcetype-property"></a><span data-ttu-id="0e254-106">SystemMonitor ::D propriété ataSourceType</span><span class="sxs-lookup"><span data-stu-id="0e254-106">SystemMonitor::DataSourceType property</span></span>

<span data-ttu-id="0e254-107">Récupère ou définit la source des données du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="0e254-107">Retrieves or sets the source of the performance counter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e254-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e254-108">Syntax</span></span>


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="0e254-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0e254-109">Property value</span></span>

<span data-ttu-id="0e254-110">Source des données du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="0e254-110">Source of the performance counter data.</span></span> <span data-ttu-id="0e254-111">Pour connaître les valeurs possibles, consultez [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="0e254-111">For possible values, see [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="0e254-112">Exceptions</span><span class="sxs-lookup"><span data-stu-id="0e254-112">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e254-113">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="0e254-113">Exception type</span></span></th>
<th><span data-ttu-id="0e254-114">Condition</span><span class="sxs-lookup"><span data-stu-id="0e254-114">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e254-115"><strong>System.ArgumentException</strong></span><span class="sxs-lookup"><span data-stu-id="0e254-115"><strong>System.ArgumentException</strong></span></span></td>
<td><span data-ttu-id="0e254-116">Vous pouvez recevoir cette exception pour l’une des raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e254-116">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="0e254-117">La valeur de la source de données spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0e254-117">The specified data source value is not valid.</span></span></li>
<li><span data-ttu-id="0e254-118">Si la source de données est un fichier journal, SYSMON ne peut pas trouver l’un des fichiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0e254-118">If the data source is a log file, SYSMON cannot find one of the specified files.</span></span> <span data-ttu-id="0e254-119">La valeur de Err. Number est 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="0e254-119">The Err.Number value is 0xC0000BD1.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0e254-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0e254-120">Remarks</span></span>

<span data-ttu-id="0e254-121">**Avant Windows Vista :** Vous ne pouvez pas ajouter ou supprimer des fichiers journaux de la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de cette propriété est définie sur sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="0e254-121">**Prior to Windows Vista:** You cannot add or remove a log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of this property is set to sysmonLogFiles.</span></span> <span data-ttu-id="0e254-122">Définissez uniquement la valeur de cette propriété sur sysmonLogFiles après avoir créé ou modifié la collection de fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="0e254-122">Only set the value of this property to sysmonLogFiles after creating or modifying the log file collection.</span></span>

<span data-ttu-id="0e254-123">En outre, vous ne pouvez pas modifier les propriétés [**SqlDsnName**](systemmonitor-sqldsnname.md) et [**SqlLogSetName**](systemmonitor-sqllogsetname.md) si la valeur de cette propriété ne doit pas être définie sur sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="0e254-123">Also, you cannot modify the [**SqlDsnName**](systemmonitor-sqldsnname.md) and [**SqlLogSetName**](systemmonitor-sqllogsetname.md) properties if the value of this property must not be set to sysmonSqlLog.</span></span> <span data-ttu-id="0e254-124">Définissez uniquement la valeur de cette propriété sur sysmonSqlLog après avoir modifié les noms du serveur et de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0e254-124">Only set the value of this property to sysmonSqlLog after modifying the server and database names.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e254-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e254-125">Requirements</span></span>



| <span data-ttu-id="0e254-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e254-126">Requirement</span></span> | <span data-ttu-id="0e254-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e254-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e254-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e254-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e254-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e254-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0e254-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e254-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e254-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e254-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e254-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0e254-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e254-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0e254-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e254-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e254-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e254-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="0e254-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





