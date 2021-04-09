---
title: SystemMonitor propriété SqlLogSetName
description: Récupère ou définit le nom convivial du jeu de journaux.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propriété SqlLogSetName SysMon
- Propriété SqlLogSetName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, propriété SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032315"
---
# <a name="systemmonitorsqllogsetname-property"></a><span data-ttu-id="105f7-106">SystemMonitor :: SqlLogSetName, propriété</span><span class="sxs-lookup"><span data-stu-id="105f7-106">SystemMonitor::SqlLogSetName property</span></span>

<span data-ttu-id="105f7-107">Récupère ou définit le nom convivial du jeu de journaux.</span><span class="sxs-lookup"><span data-stu-id="105f7-107">Retrieves or sets the friendly name of the log set.</span></span>

## <a name="syntax"></a><span data-ttu-id="105f7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="105f7-108">Syntax</span></span>


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a><span data-ttu-id="105f7-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="105f7-109">Property value</span></span>

<span data-ttu-id="105f7-110">Nom convivial du jeu de journaux, qui correspond à un fichier journal unique contenant des données binaires ou de texte dans la base de données SQL.</span><span class="sxs-lookup"><span data-stu-id="105f7-110">Friendly name of the log set, which corresponds to a single log file containing binary or text data in the SQL database.</span></span>

## <a name="remarks"></a><span data-ttu-id="105f7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="105f7-111">Remarks</span></span>

<span data-ttu-id="105f7-112">**Avant Windows Vista :** Vous ne pouvez pas modifier cette propriété si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="105f7-112">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonSqlLog.</span></span>

## <a name="requirements"></a><span data-ttu-id="105f7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="105f7-113">Requirements</span></span>



| <span data-ttu-id="105f7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="105f7-114">Requirement</span></span> | <span data-ttu-id="105f7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="105f7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="105f7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="105f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="105f7-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="105f7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="105f7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="105f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="105f7-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="105f7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="105f7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="105f7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="105f7-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="105f7-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="105f7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="105f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105f7-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="105f7-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="105f7-124">**SystemMonitor.SqlDsnName**</span><span class="sxs-lookup"><span data-stu-id="105f7-124">**SystemMonitor.SqlDsnName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





