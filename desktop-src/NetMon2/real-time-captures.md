---
description: Les moniteurs reçoivent les trames réseau capturées en temps réel. Les trames sont capturées par un fournisseur de paquets réseau (NPP) à l’aide de l’interface COM des fournisseurs IRTC et transmises à l’analyse dans l’un des deux threads d’exécution du moniteur.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Captures de Real-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869033"
---
# <a name="real-time-captures"></a><span data-ttu-id="f8be1-104">Captures de Real-Time</span><span class="sxs-lookup"><span data-stu-id="f8be1-104">Real-Time Captures</span></span>

<span data-ttu-id="f8be1-105">Les moniteurs reçoivent les trames réseau capturées en temps réel.</span><span class="sxs-lookup"><span data-stu-id="f8be1-105">Monitors receive captured network frames in real-time mode.</span></span> <span data-ttu-id="f8be1-106">Les trames sont capturées par un [*fournisseur de paquets réseau*](n.md) (NPP) à l’aide de l’interface com [IRTC](irtc.md) du fournisseur et transmises à l’analyse dans l’un des deux threads d’exécution de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="f8be1-106">The frames are captured by a [*network packet provider*](n.md) (NPP) using the provider's [IRTC](irtc.md) COM interface, and passed on to the monitor in one of the monitor's two execution threads.</span></span>

<span data-ttu-id="f8be1-107">Les analyses peuvent limiter le nombre d’images qu’elles doivent traiter en passant un [*filtre de capture*](c.md) au NPP qui fournit les frames.</span><span class="sxs-lookup"><span data-stu-id="f8be1-107">Monitors can limit the number of frames they have to process by passing a [*capture filter*](c.md) to the NPP that is supplying the frames.</span></span> <span data-ttu-id="f8be1-108">En règle générale, une analyse spécifique est conçue pour surveiller des types spécifiques de trafic, tels que HTTP, RIPX ou SMB.</span><span class="sxs-lookup"><span data-stu-id="f8be1-108">Typically, a specific monitor is designed to watch for specific types of traffic, such as HTTP, RIPX, or SMB.</span></span> <span data-ttu-id="f8be1-109">À la différence des experts qui utilisent des analyseurs sophistiqués pour sélectionner les informations à analyser, un moniteur doit examiner chaque cadre pour déterminer les conditions qu’il a été prévu de détecter.</span><span class="sxs-lookup"><span data-stu-id="f8be1-109">Unlike experts, which use sophisticated parsers to select the information to be analyzed, a monitor must examine each frame for the conditions it was designed to detect.</span></span> <span data-ttu-id="f8be1-110">La raison de cette approche Frame-by-frame est la performance.</span><span class="sxs-lookup"><span data-stu-id="f8be1-110">The reason behind this frame-by-frame approach is performance.</span></span> <span data-ttu-id="f8be1-111">Une analyse doit traiter ses frames suffisamment rapidement pour ne pas se trouver derrière le pilote qui fournit les frames au NPP.</span><span class="sxs-lookup"><span data-stu-id="f8be1-111">A monitor must process its frames quickly enough so that it does not fall behind the driver supplying the frames to the NPP.</span></span> <span data-ttu-id="f8be1-112">Dans le cas contraire, les données seront perdues.</span><span class="sxs-lookup"><span data-stu-id="f8be1-112">Otherwise, data will be lost.</span></span>

 

 



