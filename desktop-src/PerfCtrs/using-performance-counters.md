---
description: Pour consommer des données de compteur, consultez consommation des données de compteur.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Using Performance Counters
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531701"
---
# <a name="using-performance-counters"></a><span data-ttu-id="17648-103">Using Performance Counters</span><span class="sxs-lookup"><span data-stu-id="17648-103">Using Performance Counters</span></span>

<span data-ttu-id="17648-104">Les **consommateurs** de compteurs de performances sont des composants logiciels qui collectent et utilisent des données de compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="17648-104">Performance counter **consumers** are software components that collect and make use of performance counter data.</span></span> <span data-ttu-id="17648-105">Exemples de consommateurs fournis par Microsoft : analyseur de performances (perfmon.exe), moniteur de ressource (resmon.exe), gestionnaire de journaux (logman.exe) et typeperf.exe.</span><span class="sxs-lookup"><span data-stu-id="17648-105">Example consumers provided by Microsoft include Performance Monitor (perfmon.exe), Resource Monitor (resmon.exe), Log Manager (logman.exe) and typeperf.exe.</span></span> <span data-ttu-id="17648-106">Les composants logiciels tiers peuvent également collecter des données de performances via des API de collecte de performances ou via des classes de compteur de performances WMI.</span><span class="sxs-lookup"><span data-stu-id="17648-106">Third-party software components may also collect performance data via performance collection APIs or via WMI performance counter classes.</span></span>

<span data-ttu-id="17648-107">Les **fournisseurs** de compteurs de performances sont des composants logiciels qui publient des données de compteur de performances.</span><span class="sxs-lookup"><span data-stu-id="17648-107">Performance counter **providers** are software components that publish performance counter data.</span></span> <span data-ttu-id="17648-108">Les compteurs de performances peuvent être fournis par les composants du système d’exploitation, les pilotes de périphériques et les services.</span><span class="sxs-lookup"><span data-stu-id="17648-108">Performance counters can be provided by operating system components, device drivers, and services.</span></span> <span data-ttu-id="17648-109">De nombreux compteurs de performances sont fournis dans le cadre du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="17648-109">Many performance counters are provided as part of the Windows operating system.</span></span> <span data-ttu-id="17648-110">Des compteurs supplémentaires peuvent être fournis par des composants logiciels tiers via les API du fournisseur de compteurs de performance.</span><span class="sxs-lookup"><span data-stu-id="17648-110">Additional counters may be provided by third-party software components via the performance counter provider APIs.</span></span>

- <span data-ttu-id="17648-111">Utilisez les [outils de compteur de performance](performance-counters-tools.md) lorsque vous souhaitez collecter ou afficher les données de compteur à partir d’un système.</span><span class="sxs-lookup"><span data-stu-id="17648-111">Use [Performance Counter Tools](performance-counters-tools.md) when you want to collect or view the counter data from a system.</span></span>
- <span data-ttu-id="17648-112">Utilisez les [API de consommateur de compteur de performance](consuming-counter-data.md) lorsque vous souhaitez écrire un programme qui collecte des données de compteur à partir du système local.</span><span class="sxs-lookup"><span data-stu-id="17648-112">Use [Performance Counter Consumer APIs](consuming-counter-data.md) when you want to write a program that collects counter data from the local system.</span></span>
- <span data-ttu-id="17648-113">Utilisez les [classes de compteur de performances WMI](/windows/desktop/WmiSdk/monitoring-performance-data) lorsque vous souhaitez collecter des données de compteur à partir d’un système local ou distant à l’aide de WMI.</span><span class="sxs-lookup"><span data-stu-id="17648-113">Use [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) when you want to collect counter data from a local or remote system using WMI.</span></span>
- <span data-ttu-id="17648-114">Utilisez les [API du fournisseur de compteurs de performance](providing-counter-data.md) lorsque vous souhaitez publier des données de compteur de performance à partir de votre composant logiciel.</span><span class="sxs-lookup"><span data-stu-id="17648-114">Use [Performance Counter Provider APIs](providing-counter-data.md) when you want to publish performance counter data from your software component.</span></span>

## <a name="see-also"></a><span data-ttu-id="17648-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17648-115">See also</span></span>

[<span data-ttu-id="17648-116">À propos des compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="17648-116">About Performance Counters</span></span>](about-performance-counters.md)

[<span data-ttu-id="17648-117">Référence des compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="17648-117">Performance Counters Reference</span></span>](performance-counters-reference.md)
