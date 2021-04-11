---
title: SystemMonitor propriété SqlDsnName
description: Récupère ou définit le nom de source de données (DSN) ODBC.
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Propriété SqlDsnName SysMon
- Propriété SqlDsnName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, propriété SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383827"
---
# <a name="systemmonitorsqldsnname-property"></a><span data-ttu-id="fbc7d-106">SystemMonitor :: SqlDsnName, propriété</span><span class="sxs-lookup"><span data-stu-id="fbc7d-106">SystemMonitor::SqlDsnName property</span></span>

<span data-ttu-id="fbc7d-107">Récupère ou définit le nom de source de données (DSN) ODBC.</span><span class="sxs-lookup"><span data-stu-id="fbc7d-107">Retrieves or sets the ODBC data source name (DSN).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc7d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbc7d-108">Syntax</span></span>


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a><span data-ttu-id="fbc7d-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fbc7d-109">Property value</span></span>

<span data-ttu-id="fbc7d-110">Nom de la source de données ODBC qui pointe vers une base de données qui contient les tables Perfmon appropriées.</span><span class="sxs-lookup"><span data-stu-id="fbc7d-110">ODBC data source name that points to a database that contains the correct Perfmon tables.</span></span> <span data-ttu-id="fbc7d-111">Le format est SQL : DSN.</span><span class="sxs-lookup"><span data-stu-id="fbc7d-111">The format is SQL:DSN.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc7d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fbc7d-112">Remarks</span></span>

<span data-ttu-id="fbc7d-113">Vous devez utiliser le composant logiciel enfichable MMC Perfmon. msc pour générer le fichier journal SQL.</span><span class="sxs-lookup"><span data-stu-id="fbc7d-113">You must use the Perfmon.msc MMC snap-in to generate the SQL log file.</span></span> <span data-ttu-id="fbc7d-114">Les journaux de compteur se trouvent sous **journaux et alertes de performance**.</span><span class="sxs-lookup"><span data-stu-id="fbc7d-114">The counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="fbc7d-115">Pour spécifier un journal SQL, cliquez avec le bouton droit sur le fichier journal que vous avez créé, puis sélectionnez **Propriétés** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="fbc7d-115">To specify an SQL log, right-click the log file you created and select **Properties** from the menu.</span></span> <span data-ttu-id="fbc7d-116">Sur la page de propriétés **fichiers journaux** , sélectionnez **SQL Database** dans la zone de liste déroulante **type de fichier journal** .</span><span class="sxs-lookup"><span data-stu-id="fbc7d-116">On the **Log Files** property page, select **SQL Database** from the **Log file type** drop-down list box.</span></span>

<span data-ttu-id="fbc7d-117">**Avant Windows Vista :** Vous ne pouvez pas modifier cette propriété si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="fbc7d-117">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="fbc7d-118">Vous devez d’abord spécifier le nom, puis définir **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonSqlLog**.</span><span class="sxs-lookup"><span data-stu-id="fbc7d-118">You must first specify the name and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonSqlLog**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc7d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbc7d-119">Requirements</span></span>



| <span data-ttu-id="fbc7d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbc7d-120">Requirement</span></span> | <span data-ttu-id="fbc7d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbc7d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc7d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbc7d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc7d-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbc7d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fbc7d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbc7d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc7d-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbc7d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbc7d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fbc7d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbc7d-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="fbc7d-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbc7d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbc7d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc7d-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="fbc7d-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="fbc7d-130">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="fbc7d-130">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





