---
description: À compter de Windows Vista, le fournisseur WmiPerfInst fournit des données de compteur de performances brutes et mises en forme de manière dynamique aux classes de compteur de performances WMI dérivées de la \_ performance Win32.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Fournisseur WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519036"
---
# <a name="wmiperfinst-provider"></a><span data-ttu-id="12d21-103">Fournisseur WmiPerfInst</span><span class="sxs-lookup"><span data-stu-id="12d21-103">WmiPerfInst Provider</span></span>

<span data-ttu-id="12d21-104">À compter de Windows Vista, le fournisseur WmiPerfInst fournit des données de compteur de performances brutes et mises en forme de manière dynamique aux [classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI dérivées de la [**\_ performance Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="12d21-104">Starting with Windows Vista, the WmiPerfInst provider supplies raw and formatted performance counter data dynamically to WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span> <span data-ttu-id="12d21-105">Ce fournisseur remplace le [fournisseur de données de performance mis en forme](formatted-performance-data-provider.md), également appelé « fournisseur de compteurs cuit », et le [fournisseur de compteur de performance](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="12d21-105">This provider replaces the [Formatted Performance Data Provider](formatted-performance-data-provider.md), also known as the "Cooked Counter Provider", and the [Performance Counter Provider](performance-counter-provider.md).</span></span>

<span data-ttu-id="12d21-106">Le fournisseur WmiPerfInst fournit des données aux classes WMI fournies par le fournisseur [wmiperfclass](wmiperfclass-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="12d21-106">The WmiPerfInst provider supplies data to the WMI classes that are provided by the [WMIPerfClass](wmiperfclass-provider.md) provider.</span></span> <span data-ttu-id="12d21-107">Ce fournisseur est un pont entre les instances de l’application d’assistance des données de performance (PDH) et les classes de performance WMI fournies par le fournisseur WmiPerfClass.</span><span class="sxs-lookup"><span data-stu-id="12d21-107">This provider is a bridge between Performance Data Helper (PDH) instances and the WMI performance classes supplied by the WmiPerfClass Provider.</span></span> <span data-ttu-id="12d21-108">Quand WmiPerfInst reçoit une requête de données, il charge la classe et utilise les [qualificateurs](qualifiers-specific-to-wmi-performance-classes.md) de la classe et de la propriété pour localiser les instances PDH.</span><span class="sxs-lookup"><span data-stu-id="12d21-108">When WmiPerfInst receives a query for data, it loads the class and uses the class and property [qualifiers](qualifiers-specific-to-wmi-performance-classes.md) to locate the PDH instances.</span></span> <span data-ttu-id="12d21-109">Pour plus d’informations, consultez [utilisation des fonctions PDH pour consommer des données de compteur](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="12d21-109">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

<span data-ttu-id="12d21-110">Il n’est pas recommandé de développer de nouveaux objets de performance en créant un fournisseur haute performance WMI et en fonction du processus de l' [*adaptateur inverse adap*](gloss-r.md) pour transférer les données vers les bibliothèques de performances.</span><span class="sxs-lookup"><span data-stu-id="12d21-110">It is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries.</span></span> <span data-ttu-id="12d21-111">La seule exception est lorsque vous développez un pilote Windows Driver Model et que vous souhaitez fournir des données de performances.</span><span class="sxs-lookup"><span data-stu-id="12d21-111">The exception is when you are developing a Windows Driver Model driver and want to supply performance data.</span></span> <span data-ttu-id="12d21-112">Tandis que le processus de l’adaptateur inverse continue de fonctionner pour des raisons de compatibilité descendante, la méthode recommandée consiste à utiliser les [compteurs de performance Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="12d21-112">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="12d21-113">Le nom d’instance [**\_ \_ Win32Provider**](--win32provider.md) de ce fournisseur est « WmiPerfInst ».</span><span class="sxs-lookup"><span data-stu-id="12d21-113">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfInst".</span></span>

## <a name="related-topics"></a><span data-ttu-id="12d21-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12d21-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12d21-115">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="12d21-115">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="12d21-116">Bibliothèques de performances et WMI</span><span class="sxs-lookup"><span data-stu-id="12d21-116">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="12d21-117">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="12d21-117">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
