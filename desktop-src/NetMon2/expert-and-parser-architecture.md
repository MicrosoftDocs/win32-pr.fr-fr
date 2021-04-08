---
description: L’illustration suivante montre la relation entre les applications d’analyse et d’analyse et d’autres composants de l’architecture Moniteur réseau.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Architecture de l’analyseur et de l’expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112246"
---
# <a name="expert-and-parser-architecture"></a><span data-ttu-id="52be2-103">Architecture de l’analyseur et de l’expert</span><span class="sxs-lookup"><span data-stu-id="52be2-103">Expert and Parser Architecture</span></span>

<span data-ttu-id="52be2-104">L’illustration suivante montre la [relation entre les](experts.md) applications d’analyse et d' [analyse](parsers.md) et d’autres composants de l’architecture Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="52be2-104">The following figure shows the relationship between [expert](experts.md) and [parser](parsers.md) applications and other components of the Network Monitor architecture.</span></span>

![relation entre les applications d’analyse et d’experts](images/nm-arch1.png)

<span data-ttu-id="52be2-106">Le trafic réseau est collecté, sous forme de trames individuelles, à partir du pilote NDIS.</span><span class="sxs-lookup"><span data-stu-id="52be2-106">The network traffic is collected, as individual frames, from the NDIS driver.</span></span> <span data-ttu-id="52be2-107">Le pilote de Moniteur réseau (Nmnt.sys) achemine ensuite les trames vers un fournisseur de paquets réseau (NPP), qui capture les données et les place dans un ou plusieurs fichiers de capture.</span><span class="sxs-lookup"><span data-stu-id="52be2-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which captures the data and places it in one or more capture files.</span></span> <span data-ttu-id="52be2-108">Le NPP est une collection d’interfaces COM utilisées pour capturer des données.</span><span class="sxs-lookup"><span data-stu-id="52be2-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="52be2-109">Dans ce cas, l’interface [**IDelaydC**](idelaydc.md) est utilisée pour effectuer une capture différée.</span><span class="sxs-lookup"><span data-stu-id="52be2-109">In this case, the [**IDelaydC**](idelaydc.md) interface is used to perform a delayed capture.</span></span>

> [!Note]  
> <span data-ttu-id="52be2-110">Le NPP est utilisé pour les captures retardées et en temps réel.</span><span class="sxs-lookup"><span data-stu-id="52be2-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="52be2-111">Pour les captures en temps réel, l’interface [**IRTC**](irtc.md) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="52be2-111">For real-time captures, the [**IRTC**](irtc.md) interface is used.</span></span>

 

<span data-ttu-id="52be2-112">Lorsque les trames réseau sont stockées dans le fichier de capture et que le fichier est accessible, les experts et les analyseurs peuvent utiliser l’interface utilisateur Moniteur réseau et les fonctions Moniteur réseau fournies dans Nmapi.dll pour analyser les données.</span><span class="sxs-lookup"><span data-stu-id="52be2-112">When the network frames are stored in the capture file and the file is accessible, experts and parsers can use the Network Monitor UI and the Network Monitor functions provided in Nmapi.dll to analyze the data.</span></span> <span data-ttu-id="52be2-113">Les fichiers de capture ne sont pas accessibles tant que la capture n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="52be2-113">Capture files are not accessible until the capture is complete.</span></span>

 

 



