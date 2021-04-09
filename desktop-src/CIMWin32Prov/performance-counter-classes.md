---
description: Les classes de compteur de performance permettent aux scripts et aux programmes d’accéder aux données de performances système calculées par les fournisseurs de haute performance existants.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classes du compteur de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861746"
---
# <a name="performance-counter-classes"></a><span data-ttu-id="2c80b-103">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="2c80b-103">Performance Counter Classes</span></span>

<span data-ttu-id="2c80b-104">Les classes de compteur de performance permettent aux scripts et aux programmes d’accéder aux données de performances système calculées par les fournisseurs de haute performance existants.</span><span class="sxs-lookup"><span data-stu-id="2c80b-104">Performance Counter classes allow script and program access to system performance data calculated by existing high-performance providers.</span></span> <span data-ttu-id="2c80b-105">Ces classes se composent de classes de compteur de performances brutes et de classes de compteurs de performance mises en forme.</span><span class="sxs-lookup"><span data-stu-id="2c80b-105">These classes consist of raw performance counter classes and formatted performance counter classes.</span></span>

<span data-ttu-id="2c80b-106">Différents fournisseurs fournissent des données de bibliothèque de performances via WMI.</span><span class="sxs-lookup"><span data-stu-id="2c80b-106">Different providers supply performance library data through WMI.</span></span> <span data-ttu-id="2c80b-107">Les fournisseurs [wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider) et [wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider) fournissent des classes pour les [compteurs de performance](/windows/desktop/PerfCtrs/performance-counters-portal)version 1 et version 2.</span><span class="sxs-lookup"><span data-stu-id="2c80b-107">The [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) and [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) providers supply classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="2c80b-108">Ces fournisseurs maintiennent la compatibilité avec les classes disponibles dans les systèmes d’exploitation antérieurs.</span><span class="sxs-lookup"><span data-stu-id="2c80b-108">These providers maintain compatibility with the classes available in earlier operating systems.</span></span>

<span data-ttu-id="2c80b-109">Les classes de cette section sont les classes de base abstraites utilisées pour créer des classes de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="2c80b-109">The classes in this section are the abstract base classes used to create performance counter classes.</span></span> <span data-ttu-id="2c80b-110">Il ne s’agit pas d’une liste complète des classes que vous pouvez trouver sur votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2c80b-110">This is not a complete list of classes that you may find on your operating system.</span></span> <span data-ttu-id="2c80b-111">Pour plus d’informations, consultez [bibliothèques de performances et WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2c80b-111">For more information, see [Performance Libraries and WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2c80b-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2c80b-112">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2c80b-113">**\_Performances Win32**</span><span class="sxs-lookup"><span data-stu-id="2c80b-113">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dd>

<span data-ttu-id="2c80b-114">Classe de base pour les classes de compteur de performance [**Win32 \_ PerfRawData**](win32-perfrawdata.md) et [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="2c80b-114">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

</dd> <dt>

[<span data-ttu-id="2c80b-115">**\_PerfFormattedData Win32**</span><span class="sxs-lookup"><span data-stu-id="2c80b-115">**Win32\_PerfFormattedData**</span></span>](win32-perfformatteddata.md)
</dt> <dd>

<span data-ttu-id="2c80b-116">classe de base abstraite pour les classes de données calculées préinstallées.</span><span class="sxs-lookup"><span data-stu-id="2c80b-116">an abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

[<span data-ttu-id="2c80b-117">**\_PerfRawData Win32**</span><span class="sxs-lookup"><span data-stu-id="2c80b-117">**Win32\_PerfRawData**</span></span>](win32-perfrawdata.md)
</dt> <dd>

<span data-ttu-id="2c80b-118">Classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes.</span><span class="sxs-lookup"><span data-stu-id="2c80b-118">The abstract base class for all concrete raw performance counter classes.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2c80b-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c80b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c80b-120">Classes Win32</span><span class="sxs-lookup"><span data-stu-id="2c80b-120">Win32 Classes</span></span>](win32-provider.md)
</dt> </dl>

 

 
