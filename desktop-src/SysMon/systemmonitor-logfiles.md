---
title: SystemMonitor. LogFiles, propriété
description: Collection d’un ou de plusieurs fichiers journaux à utiliser comme source des valeurs de compteur affichées dans le moniteur système.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Propriété LogFiles SysMon
- Propriété LogFiles SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété LogFiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513779"
---
# <a name="systemmonitorlogfiles-property"></a><span data-ttu-id="c9db6-106">SystemMonitor. LogFiles, propriété</span><span class="sxs-lookup"><span data-stu-id="c9db6-106">SystemMonitor.LogFiles property</span></span>

<span data-ttu-id="c9db6-107">Collection d’un ou de plusieurs fichiers journaux à utiliser comme source des valeurs de compteur affichées dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="c9db6-107">Collection of one or more log files to use as the source of counter values displayed in the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9db6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9db6-108">Syntax</span></span>


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a><span data-ttu-id="c9db6-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c9db6-109">Property value</span></span>

<span data-ttu-id="c9db6-110">Collection d’objets [**LogFileItem**](logfileitem.md) qui spécifient les fichiers journaux utilisés comme source de données pour le graphique.</span><span class="sxs-lookup"><span data-stu-id="c9db6-110">Collection of [**LogFileItem**](logfileitem.md) objects that specify the log files used as the data source for the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9db6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c9db6-111">Remarks</span></span>

<span data-ttu-id="c9db6-112">Pour ajouter ou supprimer un fichier journal de la collection de fichiers journaux, la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) ne doit pas être définie sur sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="c9db6-112">To add or remove a log file from the log file collection, the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) must not be set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9db6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9db6-113">Requirements</span></span>



| <span data-ttu-id="c9db6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9db6-114">Requirement</span></span> | <span data-ttu-id="c9db6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9db6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9db6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9db6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c9db6-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9db6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c9db6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9db6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c9db6-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9db6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9db6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c9db6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9db6-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c9db6-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9db6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9db6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9db6-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="c9db6-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="c9db6-124">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="c9db6-124">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> <dt>

[<span data-ttu-id="c9db6-125">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="c9db6-125">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="c9db6-126">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="c9db6-126">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="c9db6-127">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="c9db6-127">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





