---
description: Le SDK Windows (WSDK) contient trois dll d’exemples de performances complètes.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Exemples de DLL de performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534262"
---
# <a name="performance-dll-samples"></a><span data-ttu-id="c7b28-103">Exemples de DLL de performance</span><span class="sxs-lookup"><span data-stu-id="c7b28-103">Performance DLL Samples</span></span>

<span data-ttu-id="c7b28-104">Le SDK Windows (WSDK) contient trois dll d’exemples de performances complètes.</span><span class="sxs-lookup"><span data-stu-id="c7b28-104">The Windows SDK (WSDK) contains three complete sample performance DLLs.</span></span> <span data-ttu-id="c7b28-105">Ces exemples se trouvent dans le répertoire Samples \\ WinBase \\ winnt \\ PerfTool \\ PerfDlls</span><span class="sxs-lookup"><span data-stu-id="c7b28-105">These samples are located in the Samples\\WinBase\\WinNT\\PerfTool\\PerfDlls directory.</span></span> <span data-ttu-id="c7b28-106">La racine de ce chemin d’accès est le répertoire d’installation de base de WSDK.</span><span class="sxs-lookup"><span data-stu-id="c7b28-106">The root of this path is the base installation directory of the WSDK.</span></span> <span data-ttu-id="c7b28-107">Vous pouvez télécharger le WSDK à partir du [Kit de développement logiciel (SDK) Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (recherchez SDK Windows, puis sélectionnez Télécharger pour le dernier système d’exploitation publié).</span><span class="sxs-lookup"><span data-stu-id="c7b28-107">You can download the WSDK from the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (search for Windows SDK and select the download for the latest released operating system).</span></span>

<span data-ttu-id="c7b28-108">Les exemples contenus dans ce répertoire sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c7b28-108">The samples contained in this directory are:</span></span>

-   <span data-ttu-id="c7b28-109">**AppMem**: fournit les équivalents des fonctions [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)et [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) qui signalent les informations de performances.</span><span class="sxs-lookup"><span data-stu-id="c7b28-109">**AppMem**—Provides counterparts of the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc), and [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) functions that report performance information.</span></span> <span data-ttu-id="c7b28-110">Les compteurs de performance dans le registre et l’outil performance peuvent lire les informations de performances.</span><span class="sxs-lookup"><span data-stu-id="c7b28-110">Performance counters in the registry and the Performance tool can read the performance information.</span></span>
-   <span data-ttu-id="c7b28-111">**LeakyBin**: illustre l’utilisation des compteurs de performance de l’application.</span><span class="sxs-lookup"><span data-stu-id="c7b28-111">**LeakyBin**—Demonstrates the use of application performance counters.</span></span>
-   <span data-ttu-id="c7b28-112">**PerfGen**: fournit trois formes d’onde à cinq périodes différentes pour une utilisation avec l’outil performance pour fournir des données à une vitesse et une valeur connues.</span><span class="sxs-lookup"><span data-stu-id="c7b28-112">**PerfGen**—Provides three waveforms at five different periods for use with the Performance tool to provide data at a known rate and value.</span></span> <span data-ttu-id="c7b28-113">Cela peut être utile pour tester des applications qui utilisent des données de performances et nécessitent des valeurs prévisibles pour le test.</span><span class="sxs-lookup"><span data-stu-id="c7b28-113">This can be useful in testing applications that use performance data and need predictable values to test against.</span></span>

 

 
