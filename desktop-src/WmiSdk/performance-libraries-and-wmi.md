---
description: Le fournisseur WMIPerfClass et le fournisseur WMIPerfInst fournissent dynamiquement des données de compteurs de performances pour les classes de compteur de performance WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliothèques de performances et WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524937"
---
# <a name="performance-libraries-and-wmi"></a><span data-ttu-id="a0d09-103">Bibliothèques de performances et WMI</span><span class="sxs-lookup"><span data-stu-id="a0d09-103">Performance Libraries and WMI</span></span>

<span data-ttu-id="a0d09-104">Le fournisseur [wmiperfclass](wmiperfclass-provider.md) et le [fournisseur WMIPerfInst](wmiperfinst-provider.md) fournissent dynamiquement des données de compteurs de performances pour les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="a0d09-104">The [WMIPerfClass Provider](wmiperfclass-provider.md) and the [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provide performance counter data for the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span>

## <a name="wmiperfclass-and-wmiperfinst-providers"></a><span data-ttu-id="a0d09-105">Fournisseurs WMIPerfClass et WMIPerfInst</span><span class="sxs-lookup"><span data-stu-id="a0d09-105">WMIPerfClass and WMIPerfInst Providers</span></span>

<span data-ttu-id="a0d09-106">Le [fournisseur wmiperfclass](wmiperfclass-provider.md) crée des [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI au moment de l’initialisation du système.</span><span class="sxs-lookup"><span data-stu-id="a0d09-106">[WMIPerfClass Provider](wmiperfclass-provider.md) creates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) at system initialization.</span></span> <span data-ttu-id="a0d09-107">Le [fournisseur WMIPerfInst](wmiperfinst-provider.md) fournit dynamiquement des données de compteurs de performance pour ces classes.</span><span class="sxs-lookup"><span data-stu-id="a0d09-107">The [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provides performance counter data for these classes.</span></span> <span data-ttu-id="a0d09-108">Le fournisseur WMIPerfClass fournit des classes pour les [compteurs de performance](/windows/desktop/PerfCtrs/performance-counters-portal)version 1 et version 2.</span><span class="sxs-lookup"><span data-stu-id="a0d09-108">The WMIPerfClass Provider provider supplies classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="a0d09-109">Les compteurs de la version 1 se trouvent dans le Registre sous **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services**.</span><span class="sxs-lookup"><span data-stu-id="a0d09-109">Version 1 counters are found in the registry under **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span> <span data-ttu-id="a0d09-110">Les services qui fournissent des données de performances ont une sous-clé de **performance** .</span><span class="sxs-lookup"><span data-stu-id="a0d09-110">Services that provide performance data have a **Performance** subkey.</span></span> <span data-ttu-id="a0d09-111">Les classes de performance WMI créées à partir des compteurs de la version 1 n’ont pas de « compteurs » dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="a0d09-111">WMI performance classes created from version 1 counters do not have "Counters" as part of their name.</span></span>

<span data-ttu-id="a0d09-112">Le **GUID** identifiant un fournisseur de compteurs de performance version 2 se trouve dans le Registre sous **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.</span><span class="sxs-lookup"><span data-stu-id="a0d09-112">The **GUID** s identifying a version 2 performance counter provider are found in the registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib\\\_V2Providers**.</span></span>

<span data-ttu-id="a0d09-113">WMIPerfClass est inscrit en tant que fournisseur de classe WMI normal.</span><span class="sxs-lookup"><span data-stu-id="a0d09-113">WMIPerfClass is registered as a normal WMI class provider.</span></span> <span data-ttu-id="a0d09-114">WMIPerfInst est un fournisseur d’instances WMI qui fournit des données de performance Data Helper (PDH) pour les compteurs version 1 et version 2.</span><span class="sxs-lookup"><span data-stu-id="a0d09-114">WMIPerfInst is a WMI instance provider that supplies data from Performance Data Helper (PDH) for both version 1 and version 2 counters.</span></span> <span data-ttu-id="a0d09-115">Pour plus d’informations, consultez [utilisation des fonctions PDH pour consommer des données de compteur](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="a0d09-115">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0d09-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0d09-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d09-117">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="a0d09-117">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="a0d09-118">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="a0d09-118">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
