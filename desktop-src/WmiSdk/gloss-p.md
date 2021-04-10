---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952981"
---
# <a name="p-wmi"></a><span data-ttu-id="7ed0d-103">P (WMI)</span><span class="sxs-lookup"><span data-stu-id="7ed0d-103">P (WMI)</span></span>

<span data-ttu-id="7ed0d-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [e](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="7ed0d-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7ed0d-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**compteur de performances**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**performance counter**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-106">Propriété d’une classe de performance dérivée de [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) qui stocke les données de performances.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-106">A property in a performance class that is derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) that stores performance data.</span></span>

</dd> <dt>

<span data-ttu-id="7ed0d-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**objet de performance**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**performance object**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-108">Objet dans une bibliothèque de performances qui stocke des données dans des compteurs.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-108">An object in a performance library that stores data in counters.</span></span> <span data-ttu-id="7ed0d-109">Ces objets sont visibles dans l’utilitaire [*Moniteur système*](gloss-s.md) .</span><span class="sxs-lookup"><span data-stu-id="7ed0d-109">These objects are visible in the [*System Monitor*](gloss-s.md) utility.</span></span> <span data-ttu-id="7ed0d-110">Les exemples sont les objets de cache et de disque logique.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-110">Examples are Cache and Logical Disk objects.</span></span> <span data-ttu-id="7ed0d-111">Lorsqu’ils sont transférés dans WMI par le processus [*adap*](gloss-a.md) , chaque objet devient deux classes de performance WMI.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-111">When transferred into WMI by the [*ADAP*](gloss-a.md) process, each object becomes two WMI performance classes.</span></span> <span data-ttu-id="7ed0d-112">Une classe, contenant des données brutes, dérive de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="7ed0d-112">One class, containing raw data, derives from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="7ed0d-113">L’autre classe dérive de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) et contient les mêmes données visibles dans le moniteur système que celles calculées par le fournisseur de compteur cuit.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-113">The other class derives from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and contains the same data visible in System Monitor as calculated by the Cooked Counter provider.</span></span>

</dd> <dt>

<span data-ttu-id="7ed0d-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consommateur permanent**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**permanent consumer**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-115">[*Consommateur d’événements*](gloss-e.md) dont l’inscription dure jusqu’à ce qu’elle soit explicitement annulée.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-115">An [*event consumer*](gloss-e.md) whose registration lasts until it is explicitly canceled.</span></span> <span data-ttu-id="7ed0d-116">Voir aussi [*consommateur temporaire*](gloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="7ed0d-116">Also see [*temporary consumer*](gloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ed0d-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consommateur physique**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physical consumer**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-118">Objet COM implémenté par un [*fournisseur de consommateur d’événements*](gloss-e.md) qui comprend un [*récepteur*](gloss-s.md) pour recevoir des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-118">A COM object that is implemented by an [*event consumer provider*](gloss-e.md) that includes a [*sink*](gloss-s.md) for receiving event notifications.</span></span>

</dd> <dt>

<span data-ttu-id="7ed0d-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**propriété**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-120">Une paire nom/valeur qui décrit une unité de données pour une classe.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-120">A name/value pair that describes a unit of data for a class.</span></span> <span data-ttu-id="7ed0d-121">Les valeurs de propriété doivent avoir un type de données [*format MOF (MOF)*](gloss-m.md) valide.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-121">Property values must have a valid [*Managed Object Format (MOF)*](gloss-m.md) data type.</span></span> <span data-ttu-id="7ed0d-122">Consultez également la [*propriété Reference*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="7ed0d-122">Also see [*reference property*](gloss-r.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ed0d-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**fournisseur de propriétés**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**property provider**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-124">Serveur COM qui prend en charge la récupération et la modification des propriétés WMI.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-124">A COM server that supports the retrieval and modification of WMI properties.</span></span> <span data-ttu-id="7ed0d-125">Les fournisseurs de propriétés implémentent les interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .</span><span class="sxs-lookup"><span data-stu-id="7ed0d-125">Property providers implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="7ed0d-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**moteur**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-127">Serveur COM qui communique avec des objets gérés pour accéder aux données et aux notifications d’événements, telles que le registre ou un périphérique SNMP.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-127">A COM server that communicates with managed objects to access data and event notifications, such as the registry or an SNMP device.</span></span> <span data-ttu-id="7ed0d-128">Les fournisseurs transfèrent ces données au [*Gestionnaire d’objets CIMOM*](gloss-c.md) pour l’intégration et l’interprétation.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-128">Providers forward this data to the [*CIM Object Manager*](gloss-c.md) for integration and interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="7ed0d-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**méthode du fournisseur**</span><span class="sxs-lookup"><span data-stu-id="7ed0d-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider method**</span></span>
</dt> <dd>

<span data-ttu-id="7ed0d-130">Méthode implémentée par un *fournisseur* WMI.</span><span class="sxs-lookup"><span data-stu-id="7ed0d-130">A method that a WMI *provider* implements.</span></span>

</dd> </dl>

 

 
