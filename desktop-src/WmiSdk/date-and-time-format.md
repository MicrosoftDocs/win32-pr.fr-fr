---
description: Décrit le format de date et d’heure Common Information Model (CIM) utilisé par WMI. Ce format est indépendant des paramètres régionaux, de sorte que les scripts utilisant DATETIME peuvent s’exécuter dans de nombreux fuseaux horaires.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Format de date et d’heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e8f97930efa33942fe87b2109aa7cd7ba9d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115043"
---
# <a name="date-and-time-format"></a><span data-ttu-id="24bca-104">Format de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="24bca-104">Date and Time Format</span></span>

<span data-ttu-id="24bca-105">WMI utilise les formats de date et d’heure définis par la spécification[DMTF.org](https://www.dmtf.org/)(Distributed Management Task Force) Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="24bca-105">WMI uses the date and time formats defined by the Distributed Management Task Force ([DMTF.org](https://www.dmtf.org/)) Common Information Model (CIM) specification.</span></span>

<span data-ttu-id="24bca-106">Le **format \_ DateTime CIM** est implémenté dans Microsoft [format MOF (MOF)](managed-object-format--mof-.md) par le type de données MOF [DateTime](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="24bca-106">The **CIM\_DATETIME** format is implemented in the Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) by the [DATETIME](datetime.md) MOF datatype.</span></span> <span data-ttu-id="24bca-107">Les formats de date et d’heure peuvent également exprimer un intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="24bca-107">The date and time formats can also express an interval of time.</span></span>

<span data-ttu-id="24bca-108">Pour plus d’informations sur les formats WMI, voir [format d’intervalle](interval-format.md)et [ \_ DateTime CIM](cim-datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="24bca-108">For more information about WMI formats, see [CIM\_DATETIME](cim-datetime.md) and [Interval Format](interval-format.md).</span></span>

<span data-ttu-id="24bca-109">Pour plus d’informations sur la conversion vers et à partir du format DATETIME WMI, consultez [**SWbemDateTime**](swbemdatetime.md) et l’article sur technet scriptcenter [il s’agit du temps (Oh, et à propos des dates)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="24bca-109">For more information about converting to and from the WMI DATETIME format, see [**SWbemDateTime**](swbemdatetime.md) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24bca-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24bca-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24bca-111">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="24bca-111">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



