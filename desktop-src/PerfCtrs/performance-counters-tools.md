---
description: Le tableau suivant répertorie les
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Outils des compteurs de performances
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951996"
---
# <a name="performance-counters-tools"></a><span data-ttu-id="ef6a2-103">Outils des compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="ef6a2-103">Performance Counters Tools</span></span>

## <a name="data-collection-tools"></a><span data-ttu-id="ef6a2-104">Outils de collecte de données</span><span class="sxs-lookup"><span data-stu-id="ef6a2-104">Data collection tools</span></span>

<span data-ttu-id="ef6a2-105">Les outils suivants sont utiles lors de l’utilisation ou de la manipulation des données des compteurs de performances Windows.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-105">The following tools are useful when consuming or manipulating Windows Performance Counter data.</span></span>

|<span data-ttu-id="ef6a2-106">Outil</span><span class="sxs-lookup"><span data-stu-id="ef6a2-106">Tool</span></span>|<span data-ttu-id="ef6a2-107">Description</span><span class="sxs-lookup"><span data-stu-id="ef6a2-107">Description</span></span>
|----|-----------
| [<span data-ttu-id="ef6a2-108">PerfMon</span><span class="sxs-lookup"><span data-stu-id="ef6a2-108">PerfMon</span></span>](/windows-server/administration/windows-commands/perfmon) | <span data-ttu-id="ef6a2-109">Outil d’interface graphique pour la collecte et l’affichage des données des compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-109">GUI tool for collecting and viewing Performance Counter data.</span></span> <span data-ttu-id="ef6a2-110">`perfmon.exe` lance la console MMC avec le composant logiciel enfichable analyseur de performances, qui permet d’accéder à l’analyseur de performances, aux ensembles de collecteurs de données et aux outils de rapports.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-110">`perfmon.exe` launches MMC with the Performance Monitor snap-in, which provides access to the Performance Monitor, Data Collector Sets, and Reports tools.</span></span>
| [<span data-ttu-id="ef6a2-111">TypePerf</span><span class="sxs-lookup"><span data-stu-id="ef6a2-111">TypePerf</span></span>](/windows-server/administration/windows-commands/typeperf) |<span data-ttu-id="ef6a2-112">Outil en ligne de commande pour collecter et imprimer les données des compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-112">Command-line tool for collecting and printing Performance Counter data.</span></span> <span data-ttu-id="ef6a2-113">Peut être utilisé pour répertorier les countersets disponibles, répertorier les compteurs disponibles, imprimer les données de compteur sur la console ou collecter les données de compteur dans un fichier journal (CSV, TDF, BLG).</span><span class="sxs-lookup"><span data-stu-id="ef6a2-113">Can be used to list available countersets, list available counters, print counter data to the console, or collect counter data to a log file (CSV, TDF, BLG).</span></span>
| [<span data-ttu-id="ef6a2-114">Rejournaliser</span><span class="sxs-lookup"><span data-stu-id="ef6a2-114">Relog</span></span>](/windows-server/administration/windows-commands/relog) |<span data-ttu-id="ef6a2-115">Outil en ligne de commande permettant de transformer et de fusionner les fichiers journaux (CSV, TDF, BLG) capturés via `typeperf.exe` ou via les `PDH.dll` API.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-115">Command-line tool for transforming and merging log files (CSV, TDF, BLG) captured via `typeperf.exe` or via the `PDH.dll` APIs.</span></span>
| [<span data-ttu-id="ef6a2-116">LogMan</span><span class="sxs-lookup"><span data-stu-id="ef6a2-116">LogMan</span></span>](/windows-server/administration/windows-commands/logman) |<span data-ttu-id="ef6a2-117">Outil en ligne de commande pour contrôler les ensembles de collecteurs de données.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-117">Command-line tool for controlling Data Collector Sets.</span></span>

## <a name="data-provider-tools"></a><span data-ttu-id="ef6a2-118">Outils du fournisseur de données</span><span class="sxs-lookup"><span data-stu-id="ef6a2-118">Data provider tools</span></span>

<span data-ttu-id="ef6a2-119">Les outils suivants sont utiles lors de la publication de données de compteur de performances Windows.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-119">The following tools are useful when publishing Windows Performance Counter data.</span></span>

|<span data-ttu-id="ef6a2-120">Outil</span><span class="sxs-lookup"><span data-stu-id="ef6a2-120">Tool</span></span>|<span data-ttu-id="ef6a2-121">Description</span><span class="sxs-lookup"><span data-stu-id="ef6a2-121">Description</span></span>
|----|-----------
| [<span data-ttu-id="ef6a2-122">CtrPP</span><span class="sxs-lookup"><span data-stu-id="ef6a2-122">CtrPP</span></span>](ctrpp.md) | <span data-ttu-id="ef6a2-123">Outil de génération à partir de la ligne de commande de la SDK Windows qui valide et compile vos compteurs de performance manifeste du fournisseur v2.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-123">Command-line build tool from the Windows SDK that validates and compiles your Performance Counters V2 provider manifest.</span></span> <span data-ttu-id="ef6a2-124">Cet outil génère les `.h` en-têtes et les `.rc` scripts de ressources nécessaires à la création d’un fournisseur v2.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-124">This tool generates the `.h` headers and `.rc` resource scripts needed to build a V2 provider.</span></span>
| [<span data-ttu-id="ef6a2-125">LodCtr</span><span class="sxs-lookup"><span data-stu-id="ef6a2-125">LodCtr</span></span>](/windows-server/administration/windows-commands/lodctr) | <span data-ttu-id="ef6a2-126">Outil de ligne de commande utilisé pour installer votre fournisseur sur un système.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-126">Command-line tool used to install your provider onto a system.</span></span>
| [<span data-ttu-id="ef6a2-127">UnlodCtr</span><span class="sxs-lookup"><span data-stu-id="ef6a2-127">UnlodCtr</span></span>](/windows-server/administration/windows-commands/unlodctr_1) | <span data-ttu-id="ef6a2-128">Outil de ligne de commande utilisé pour désinstaller votre fournisseur d’un système.</span><span class="sxs-lookup"><span data-stu-id="ef6a2-128">Command-line tool used to uninstall your provider from a system.</span></span>
