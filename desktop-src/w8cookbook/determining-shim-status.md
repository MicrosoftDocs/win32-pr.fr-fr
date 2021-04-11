---
title: Détermination de l’état des shims
description: Détermination de l’état des shims
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310905"
---
# <a name="determining-shim-status"></a><span data-ttu-id="aacc0-103">Détermination de l’état des shims</span><span class="sxs-lookup"><span data-stu-id="aacc0-103">Determining shim status</span></span>

## <a name="platforms"></a><span data-ttu-id="aacc0-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="aacc0-104">Platforms</span></span>

<dl> <span data-ttu-id="aacc0-105">Clients-Windows 8</span><span class="sxs-lookup"><span data-stu-id="aacc0-105">Clients - Windows 8</span></span>  
<span data-ttu-id="aacc0-106">Serveurs-Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aacc0-106">Servers - Windows Server 2012</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="aacc0-107">Description</span><span class="sxs-lookup"><span data-stu-id="aacc0-107">Description</span></span>

<span data-ttu-id="aacc0-108">Windows 8 enregistre les événements lorsque les applications sont corrigées pour différentes raisons.</span><span class="sxs-lookup"><span data-stu-id="aacc0-108">Windows 8 logs events when apps are being shimmed for various reasons.</span></span> <span data-ttu-id="aacc0-109">Le moyen le plus simple de déterminer si votre application est corrigée consiste à consulter l’observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="aacc0-109">The easiest way to determine if your app is being shimmed is to check the event viewer.</span></span> <span data-ttu-id="aacc0-110">Accédez à journaux des applications et des services \\ Microsoft Windows Application-Experience programme \\ télémétrie.</span><span class="sxs-lookup"><span data-stu-id="aacc0-110">Go to Applications and Services Logs\\Microsoft Windows Application-Experience Program\\Telemetry.</span></span>

## <a name="mitigation"></a><span data-ttu-id="aacc0-111">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="aacc0-111">Mitigation</span></span>

<span data-ttu-id="aacc0-112">La meilleure façon de vous sortir de la correction consiste à renommer l’exécutable ou à augmenter la version principale de 1 (recompiler l’exécutable).</span><span class="sxs-lookup"><span data-stu-id="aacc0-112">The best way to get yourself out of shimming is to rename the executable or to increase the major version by 1 (recompile the executable).</span></span>

 

 




