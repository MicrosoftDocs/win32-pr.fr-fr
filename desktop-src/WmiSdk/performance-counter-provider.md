---
description: Le fournisseur de compteur de performance est un fournisseur à hautes performances qui fournit des données de compteur de performances brutes aux classes de compteur de performance WMI dérivées de Win32 \_ PerfRawData. Le nom de l' \_ \_ instance Win32Provider est &\# 0034 ; NT5 \_ GenericPerfProvider \_ V1&\# 0034 ;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Fournisseur de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035201"
---
# <a name="performance-counter-provider"></a><span data-ttu-id="b036d-104">Fournisseur de compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="b036d-104">Performance Counter Provider</span></span>

<span data-ttu-id="b036d-105">\[Le fournisseur du compteur de performance n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="b036d-105">\[The Performance Counter Provider is no longer available for use.</span></span> <span data-ttu-id="b036d-106">Au lieu de cela, utilisez le fournisseur [wmiperfinst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="b036d-106">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="b036d-107">Le fournisseur de compteur de performance est un fournisseur à hautes performances qui fournit des données de compteur de performances brutes aux [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="b036d-107">The Performance Counter provider is a high-performance provider that provides raw performance counter data to the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="b036d-108">Le nom de l’instance [**\_ \_ Win32Provider**](--win32provider.md) est « NT5 \_ GenericPerfProvider \_ v1 ».</span><span class="sxs-lookup"><span data-stu-id="b036d-108">The [**\_\_Win32Provider**](--win32provider.md) instance name is "NT5\_GenericPerfProvider\_V1".</span></span>

<span data-ttu-id="b036d-109">Les classes [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) se trouvent dans l’espace de noms WMI « root \\ cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="b036d-109">The [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes are located in the WMI "Root\\CIMv2" namespace.</span></span> <span data-ttu-id="b036d-110">Chaque classe de performance WMI correspond à un objet de performance dans une bibliothèque de performances.</span><span class="sxs-lookup"><span data-stu-id="b036d-110">Each WMI performance class corresponds to a performance object in a performance library.</span></span> <span data-ttu-id="b036d-111">Les propriétés de ces classes représentent les compteurs de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b036d-111">The properties of these classes represent the counters for the object.</span></span> <span data-ttu-id="b036d-112">Le nom de classe WMI d’un objet compteur brut se présente sous la forme \**Win32 \_ PerfRawData \_ \_* service \_ name *\_* \_ Name \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="b036d-112">The WMI class name for a raw counter object is of the form \**Win32\_PerfRawData\_\_* service\_name *\_* object\_name\*\*\*.</span></span> <span data-ttu-id="b036d-113">Par exemple, le nom de classe WMI qui contient les compteurs de disque logique est [**Win32 \_ PerfRawData \_ Perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="b036d-113">For example, the WMI class name that contains the logical disk counters is [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="b036d-114">Vous pouvez utiliser la classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondante pour récupérer les données de performances précalculées affichées dans le [*Moniteur système*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b036d-114">You can use the corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class to get the pre-calculated performance data shown in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="b036d-115">Par exemple, utilisez la classe disque [**\_ \_ \_ logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) pour obtenir des données de disque précalculées.</span><span class="sxs-lookup"><span data-stu-id="b036d-115">For example, use the [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class to get pre-calculated disk data.</span></span>

<span data-ttu-id="b036d-116">Pour plus d’informations sur l’écriture d’un client qui peut accéder aux données de performances brutes, consultez [accès aux données de performances en C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="b036d-116">For more information about how to write a client that can access raw performance data, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="b036d-117">En tant que fournisseur à hautes performances, le fournisseur de compteurs de performance implémente l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que la méthode [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) et les méthodes [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) suivantes :</span><span class="sxs-lookup"><span data-stu-id="b036d-117">As a high-performance provider, the Performance Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="b036d-118">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="b036d-118">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="b036d-119">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="b036d-119">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="b036d-120">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="b036d-120">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="b036d-121">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="b036d-121">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="b036d-122">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="b036d-122">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="b036d-123">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="b036d-123">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="b036d-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b036d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b036d-125">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="b036d-125">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
