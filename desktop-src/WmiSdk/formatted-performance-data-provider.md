---
description: Fournitures calculées (&\# 0034 ;&cuit \# 0034 ;) données du compteur de performances. Fournit des données dynamiques aux classes WMI dérivées de Win32 \_ PerfFormattedData. Également connu sous le nom de fournisseur de compteurs cuit.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Fournisseur de données de performance mis en forme
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524149"
---
# <a name="formatted-performance-data-provider"></a><span data-ttu-id="2aedd-105">Fournisseur de données de performance mis en forme</span><span class="sxs-lookup"><span data-stu-id="2aedd-105">Formatted Performance Data Provider</span></span>

<span data-ttu-id="2aedd-106">\[Le Fournisseur de données de performance mis en forme, également connu sous le nom de « fournisseur de compteurs cuit », ne peut plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2aedd-106">\[The Formatted Performance Data Provider, also known as the "Cooked Counter Provider," is no longer available for use.</span></span> <span data-ttu-id="2aedd-107">Au lieu de cela, utilisez le fournisseur [wmiperfinst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="2aedd-107">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="2aedd-108">Le fournisseur de données de performances mis en forme hautes performances fournit des données de compteur de performances (« cuites ») calculées, telles que le pourcentage de temps passé par un disque à écrire des données.</span><span class="sxs-lookup"><span data-stu-id="2aedd-108">The high-performance Formatted Performance Data provider supplies calculated ("cooked") performance counter data, such as the percentage of time a disk spends writing data.</span></span> <span data-ttu-id="2aedd-109">Ce fournisseur fournit des données dynamiques aux classes WMI dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="2aedd-109">This provider supplies dynamic data to the WMI classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="2aedd-110">La différence entre ce fournisseur et le [fournisseur de compteur de performance](performance-counter-provider.md) est que le fournisseur de compteurs de performance fournit des données brutes et que le fournisseur de compteurs cuit fournit des données de performances qui s’affichent exactement comme dans le [*Moniteur système*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="2aedd-110">The difference between this provider and the [Performance Counter provider](performance-counter-provider.md) is that the Performance Counter provider supplies raw data and the Cooked Counter provider supplies performance data that appears exactly as in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="2aedd-111">Le nom de l’instance [**\_ \_ Win32Provider**](--win32provider.md) est « HiPerfCooker \_ v1 ».</span><span class="sxs-lookup"><span data-stu-id="2aedd-111">The [**\_\_Win32Provider**](--win32provider.md) instance name is "HiPerfCooker\_v1".</span></span>

<span data-ttu-id="2aedd-112">Le nom de classe au format WMI pour un objet de compteur se présente sous la forme « Win32 \_ PerfFormattedData \_ *service \_ Name* \_ *\_ Name*».</span><span class="sxs-lookup"><span data-stu-id="2aedd-112">The WMI formatted class name for a counter object is of the form "Win32\_PerfFormattedData\_*service\_name*\_*object\_name*".</span></span> <span data-ttu-id="2aedd-113">Par exemple, le nom de classe WMI qui contient les compteurs de disque logique est **Win32 \_ PerfFormattedData \_ Perfdisk \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="2aedd-113">For example, the WMI class name that contains the logical disk counters is **Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**.</span></span> <span data-ttu-id="2aedd-114">Ces classes se trouvent dans l’espace de \\ noms « root cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="2aedd-114">These classes are located in the "Root\\CIMv2" namespace.</span></span>

<span data-ttu-id="2aedd-115">Étant donné que les classes de données de performances sont ajoutées et modifiées dynamiquement sur un système donné, il n’est pas possible de documenter formellement les propriétés de tous les objets de performance connus.</span><span class="sxs-lookup"><span data-stu-id="2aedd-115">Because performance data classes are added and modified dynamically on a given system, it is not possible to formally document the properties of all known performance objects.</span></span> <span data-ttu-id="2aedd-116">Pour déterminer les classes à votre disposition et pour identifier les membres de ces classes, consultez [récupération de la documentation sur les objets de données de performances brutes et mises en forme](retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="2aedd-116">To determine what classes are available to you, and to identify what members those classes have, see [Retrieving Documentation for Raw and Formatted Performance Data Objects](retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="2aedd-117">Les [**classes \_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) utilisent le qualificateur **CookingType** dans les [types de compteurs de performance WMI](wmi-performance-counter-types.md) pour spécifier la formule pour le calcul des données de performances.</span><span class="sxs-lookup"><span data-stu-id="2aedd-117">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes use the **CookingType** qualifier in [WMI Performance Counter Types](wmi-performance-counter-types.md) to specify the formula for calculating performance data.</span></span> <span data-ttu-id="2aedd-118">Ce qualificateur est le même que **le qualificateur de l’identificateur** de classe dans les classes [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="2aedd-118">This qualifier is the same as the **CounterType** qualifier in the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span>

<span data-ttu-id="2aedd-119">En tant que fournisseur de haute performance, le fournisseur de compteur cuit implémente l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que la méthode [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) et les méthodes [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) suivantes :</span><span class="sxs-lookup"><span data-stu-id="2aedd-119">As a high-performance provider, the Cooked Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="2aedd-120">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="2aedd-120">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="2aedd-121">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="2aedd-121">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="2aedd-122">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="2aedd-122">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="2aedd-123">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="2aedd-123">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="2aedd-124">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="2aedd-124">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="2aedd-125">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="2aedd-125">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="2aedd-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2aedd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aedd-127">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="2aedd-127">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
