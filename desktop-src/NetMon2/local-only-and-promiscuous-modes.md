---
description: Les analyses peuvent examiner des frames en mode local uniquement ou en mode promiscuité.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modes de Local-Only et de promiscuité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514205"
---
# <a name="local-only-and-promiscuous-modes"></a><span data-ttu-id="2dd95-103">Modes de Local-Only et de promiscuité</span><span class="sxs-lookup"><span data-stu-id="2dd95-103">Local-Only and Promiscuous Modes</span></span>

<span data-ttu-id="2dd95-104">Les analyses peuvent examiner des frames en mode local uniquement ou en mode promiscuité.</span><span class="sxs-lookup"><span data-stu-id="2dd95-104">Monitors can examine frames in local-only mode or promiscuous mode.</span></span>

<span data-ttu-id="2dd95-105">En mode local uniquement, le fournisseur de paquets réseau (NPP) renvoie les trames envoyées vers ou à partir de l’ordinateur sur lequel le moniteur est exécuté, y compris les diffusions et les multidiffusions dirigées vers l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2dd95-105">In local-only mode, the network packet provider (NPP) returns frames that are sent to or from the computer on which the monitor is running, including broadcasts and multicasts directed to the local machine.</span></span> <span data-ttu-id="2dd95-106">Bien que limité à des frames dirigés localement, le mode local est également beaucoup moins gourmand en ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="2dd95-106">Although limited to locally directed frames, local-mode is also much less processor intensive.</span></span>

<span data-ttu-id="2dd95-107">En mode promiscuité, le moniteur peut également surveiller le trafic qui n’est pas dirigé vers ou à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2dd95-107">In promiscuous mode, the monitor can also watch for traffic that is not directed to or from the local computer.</span></span> <span data-ttu-id="2dd95-108">À moins que l’analyse n’ait spécifié l’indicateur, MCS \_ Create \_ PMODE \_ not \_ Required, dans la fonction [OnLoadingDLL](onloadingdll.md) , le service de contrôle d’analyse (MCSVC) suppose que le moniteur nécessite un mode de proximité lorsqu’il charge la dll du moniteur.</span><span class="sxs-lookup"><span data-stu-id="2dd95-108">Unless the monitor has specified the flag, MCS\_CREATE\_PMODE\_NOT\_REQUIRED, in the [OnLoadingDLL](onloadingdll.md) function, the Monitor Control Service (MCSVC) assumes that the monitor requires promiscuous mode when it loads the monitor DLL.</span></span>

 

 



