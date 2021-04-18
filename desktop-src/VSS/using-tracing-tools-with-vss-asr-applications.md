---
description: Vous pouvez utiliser l’outil Logman pour collecter des informations de traçage pour les applications VSS qui utilisent la récupération automatique du système (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Utilisation des outils de suivi avec les applications ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516009"
---
# <a name="using-tracing-tools-with-asr-applications"></a><span data-ttu-id="9091d-103">Utilisation des outils de suivi avec les applications ASR</span><span class="sxs-lookup"><span data-stu-id="9091d-103">Using Tracing Tools with ASR Applications</span></span>

<span data-ttu-id="9091d-104">Vous pouvez utiliser l’outil Logman pour collecter des informations de traçage pour les applications VSS qui utilisent la [récupération automatique du système (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="9091d-104">You can use the Logman tool to collect tracing information for VSS applications that use [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span> <span data-ttu-id="9091d-105">Logman (logman.exe) est un contrôleur de trace pour les événements de trace et les compteurs de performance.</span><span class="sxs-lookup"><span data-stu-id="9091d-105">Logman (logman.exe) is a trace controller for trace events and performance counters.</span></span> <span data-ttu-id="9091d-106">Il est inclus dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="9091d-106">It is included in Windows XP and later versions of Windows.</span></span> <span data-ttu-id="9091d-107">Ou, si vous préférez, vous pouvez utiliser l’outil tracelog pour collecter les mêmes informations de suivi ASR.</span><span class="sxs-lookup"><span data-stu-id="9091d-107">Or, if you prefer, you can use the Tracelog tool to collect the same ASR tracing information.</span></span> <span data-ttu-id="9091d-108">Tracelog est inclus dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="9091d-108">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="9091d-109">Pour utiliser les outils de suivi avec VSS, consultez [utilisation des outils de suivi avec VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="9091d-109">To use tracing tools with VSS, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="using-logman"></a><span data-ttu-id="9091d-110">Utilisation de logman</span><span class="sxs-lookup"><span data-stu-id="9091d-110">Using Logman</span></span>

<span data-ttu-id="9091d-111">La procédure suivante décrit comment utiliser logman avec votre application ASR.</span><span class="sxs-lookup"><span data-stu-id="9091d-111">The following procedure describes how to use Logman with your ASR application.</span></span>

<span data-ttu-id="9091d-112">**Pour utiliser logman avec votre application ASR**</span><span class="sxs-lookup"><span data-stu-id="9091d-112">**To use Logman with your ASR application**</span></span>

1.  <span data-ttu-id="9091d-113">Utilisez la commande suivante pour démarrer le suivi :</span><span class="sxs-lookup"><span data-stu-id="9091d-113">Use the following command to start tracing:</span></span>

    <span data-ttu-id="9091d-114">**logman start ASR-o** *x : \\ \* \* \* ASR. etl-ETS-p {6407345b-94f2-44C8-b3db-4e076be46816} 0xFF 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="9091d-114">**logman start asr -o** *x:\\*\*\*asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="9091d-115">Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké.</span><span class="sxs-lookup"><span data-stu-id="9091d-115">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="9091d-116">Pour des performances optimales, le fichier journal de trace doit se trouver sur un volume qui ne fait pas partie du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="9091d-116">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

2.  <span data-ttu-id="9091d-117">Utilisez la commande suivante pour arrêter le suivi :</span><span class="sxs-lookup"><span data-stu-id="9091d-117">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="9091d-118">**logman arrêter ASR-ETS**</span><span class="sxs-lookup"><span data-stu-id="9091d-118">**logman stop asr -ets**</span></span>

<span data-ttu-id="9091d-119">Le fichier journal des traces est *x \\ :* ASR. etl.</span><span class="sxs-lookup"><span data-stu-id="9091d-119">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="9091d-120">Pour plus d’informations sur l’outil Logman, consultez [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="9091d-120">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="9091d-121">Utilisation de tracelog</span><span class="sxs-lookup"><span data-stu-id="9091d-121">Using Tracelog</span></span>

<span data-ttu-id="9091d-122">La procédure suivante décrit comment utiliser tracelog.</span><span class="sxs-lookup"><span data-stu-id="9091d-122">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="9091d-123">**Pour utiliser tracelog**</span><span class="sxs-lookup"><span data-stu-id="9091d-123">**To use Tracelog**</span></span>

1.  <span data-ttu-id="9091d-124">Créez un fichier texte nommé ASR. CTL qui contient uniquement le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="9091d-124">Create a text file named asr.ctl that contains only the following text:</span></span>

    <span data-ttu-id="9091d-125">**ASR 6407345b-94f2-44C8-b3db-4e076be46816**</span><span class="sxs-lookup"><span data-stu-id="9091d-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span></span>

2.  <span data-ttu-id="9091d-126">Utilisez la commande suivante pour démarrer le suivi :</span><span class="sxs-lookup"><span data-stu-id="9091d-126">Use the following command to start tracing:</span></span>

    <span data-ttu-id="9091d-127">**tracelog-Start ASR-f** *x : \\ \* \* \* ASR. etl-GUID ASR. Ctrl-Flag-niveau 0xFF-niveau 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="9091d-127">**tracelog -start asr -f** *x:\\*\*\*asr.etl -guid asr.ctl -flag 0xff -level 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="9091d-128">Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké.</span><span class="sxs-lookup"><span data-stu-id="9091d-128">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="9091d-129">Pour des performances optimales, le fichier journal de trace doit se trouver sur un volume qui ne fait pas partie du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="9091d-129">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

3.  <span data-ttu-id="9091d-130">Utilisez la commande suivante pour arrêter le suivi :</span><span class="sxs-lookup"><span data-stu-id="9091d-130">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="9091d-131">**tracelog-arrêter ASR**</span><span class="sxs-lookup"><span data-stu-id="9091d-131">**tracelog -stop asr**</span></span>

<span data-ttu-id="9091d-132">Le fichier journal des traces est *x \\ :* ASR. etl.</span><span class="sxs-lookup"><span data-stu-id="9091d-132">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="9091d-133">Pour plus d’informations sur l’outil tracelog, consultez [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="9091d-133">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
