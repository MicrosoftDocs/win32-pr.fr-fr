---
description: L’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Création d’un fournisseur d’instances dans un fournisseur de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524249"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a><span data-ttu-id="1969f-103">Création d’un fournisseur d’instances dans un fournisseur de High-Performance</span><span class="sxs-lookup"><span data-stu-id="1969f-103">Making an Instance Provider into a High-Performance Provider</span></span>

<span data-ttu-id="1969f-104">L’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="1969f-104">Writing a WMI high-performance provider to create performance counters is not recommended.</span></span> <span data-ttu-id="1969f-105">À compter de Windows Vista, les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI ne sont plus migrées dans les bibliothèques de performances Windows par l’adaptateur inverse AutoDiscovery/AutoPurge (ADAP).</span><span class="sxs-lookup"><span data-stu-id="1969f-105">Starting with Windows Vista, the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) are no longer migrated into the Windows performance libraries by the AutoDiscovery/AutoPurge (ADAP) reverse adapter.</span></span> <span data-ttu-id="1969f-106">Pour créer un fournisseur de compteurs de performance, utilisez les [compteurs de performance Version 2,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="1969f-106">To create a performance counter provider, use [Performance Counters Version 2.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="1969f-107">Une fois les objets de bibliothèque de performances créés, le [fournisseur wmiperfclass](wmiperfclass-provider.md) analyse les objets et crée ou actualise une classe WMI dérivée de la [**\_ performance Win32**](/windows/desktop/CIMWin32Prov/win32-perf) pour chaque objet de performance.</span><span class="sxs-lookup"><span data-stu-id="1969f-107">After performance library objects are created, the [WMIPerfClass Provider](wmiperfclass-provider.md) parses the objects and creates or refreshes a WMI class derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) for each performance object.</span></span> <span data-ttu-id="1969f-108">Le [fournisseur WMIPerfInst](wmiperfinst-provider.md) fournit ensuite dynamiquement des données de compteur de performances brutes et mises en forme aux classes de performance WMI.</span><span class="sxs-lookup"><span data-stu-id="1969f-108">The [WMIPerfInst Provider](wmiperfinst-provider.md) then dynamically provides raw and formatted performance counter data to the WMI performance classes.</span></span>

<span data-ttu-id="1969f-109">La procédure de haut niveau suivante fournit les étapes nécessaires à la création d’un fournisseur à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="1969f-109">The following high-level procedure provides the steps required to create a high-performance provider.</span></span>

<span data-ttu-id="1969f-110">**Pour créer un fournisseur à hautes performances**</span><span class="sxs-lookup"><span data-stu-id="1969f-110">**To create a high-performance provider**</span></span>

1.  <span data-ttu-id="1969f-111">Inscrivez votre fournisseur auprès de WMI.</span><span class="sxs-lookup"><span data-stu-id="1969f-111">Register your provider with WMI.</span></span> <span data-ttu-id="1969f-112">Pour plus d’informations, consultez [inscription d’un fournisseur de High-Performance](registering-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1969f-112">For more information, see [Registering a High-Performance Provider](registering-a-high-performance-provider.md).</span></span>
2.  <span data-ttu-id="1969f-113">Implémentez votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1969f-113">Implement your provider.</span></span> <span data-ttu-id="1969f-114">Pour plus d’informations, consultez [écriture d’un fournisseur d’instances](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1969f-114">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>
3.  <span data-ttu-id="1969f-115">Implémentez l’interface hautes performances.</span><span class="sxs-lookup"><span data-stu-id="1969f-115">Implement the high-performance interface.</span></span> <span data-ttu-id="1969f-116">Pour plus d’informations, consultez [implémentation de l’Interface High-Performance](implementing-the-high-performance-interface.md).</span><span class="sxs-lookup"><span data-stu-id="1969f-116">For more information, see [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).</span></span>
4.  <span data-ttu-id="1969f-117">Dérivez et écrivez votre schéma format MOF (MOF) pour obtenir des données de performances brutes.</span><span class="sxs-lookup"><span data-stu-id="1969f-117">Derive and write your Managed Object Format (MOF) schema to obtain raw performance data.</span></span> <span data-ttu-id="1969f-118">Pour plus d’informations, consultez [prise en charge de la \_ classe Win32 PerfRawData](supporting-the-win32-perfrawdata-class.md).</span><span class="sxs-lookup"><span data-stu-id="1969f-118">For more information, see [Supporting the Win32\_PerfRawData Class](supporting-the-win32-perfrawdata-class.md).</span></span>
5.  <span data-ttu-id="1969f-119">Dérivez et écrivez votre schéma MOF pour obtenir des données précalculées.</span><span class="sxs-lookup"><span data-stu-id="1969f-119">Derive and write your MOF schema to obtain precalculated data.</span></span> <span data-ttu-id="1969f-120">En prenant en charge cette classe, le fournisseur n’est pas obligé d’effectuer les calculs.</span><span class="sxs-lookup"><span data-stu-id="1969f-120">By supporting this class, the provider is not required to perform the calculations.</span></span> <span data-ttu-id="1969f-121">Ces données sont les mêmes que celles du moniteur système dans Perfmon.</span><span class="sxs-lookup"><span data-stu-id="1969f-121">This data will be the same that appears in the System Monitor in Perfmon.</span></span> <span data-ttu-id="1969f-122">Pour plus d’informations, consultez [prise en charge de la \_ classe Win32 PerfFormattedData](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="1969f-122">For more information, see [Supporting the Win32\_PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1969f-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1969f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1969f-124">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="1969f-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="1969f-125">Bibliothèques de performances et WMI</span><span class="sxs-lookup"><span data-stu-id="1969f-125">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
