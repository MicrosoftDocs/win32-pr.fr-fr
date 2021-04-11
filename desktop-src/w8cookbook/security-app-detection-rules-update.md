---
title: Mise à jour des règles de détection des applications de sécurité
description: Mise à jour des règles de détection des applications de sécurité
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031989"
---
# <a name="security-app-detection-rules-update"></a><span data-ttu-id="a3902-103">Mise à jour des règles de détection des applications de sécurité</span><span class="sxs-lookup"><span data-stu-id="a3902-103">Security app detection rules update</span></span>

## <a name="platforms"></a><span data-ttu-id="a3902-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="a3902-104">Platforms</span></span>

<span data-ttu-id="a3902-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3902-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="a3902-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3902-106">**Servers** – Windows Server 2012</span></span>  


### <a name="description"></a><span data-ttu-id="a3902-107">Description</span><span class="sxs-lookup"><span data-stu-id="a3902-107">Description</span></span>

<span data-ttu-id="a3902-108">Les applications du Windows Store ajoutées dans Windows 8 sont toutes installées à un emplacement commun sous « Program Files » (% ProgramFiles%) appelé \\ Program Files \\ WindowsApps.</span><span class="sxs-lookup"><span data-stu-id="a3902-108">The Windows Store apps being added in Windows 8 are all being installed to a common location under “Program Files” (%programfiles%) called \\program files\\WindowsApps.</span></span>

### <a name="manifestation"></a><span data-ttu-id="a3902-109">Manifestation</span><span class="sxs-lookup"><span data-stu-id="a3902-109">Manifestation</span></span>

<span data-ttu-id="a3902-110">Cela peut provoquer des collisions avec les configurations existantes, et certains détecteurs d’antivirus/anti-programme malveillant voient cet emplacement comme un emplacement potentiel qui est à l’origine de la préoccupation.</span><span class="sxs-lookup"><span data-stu-id="a3902-110">This can cause collisions with existing configurations, and some antivirus/anti-malware detectors see this location as a potential location that is a cause for concern.</span></span>

### <a name="mitigation"></a><span data-ttu-id="a3902-111">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="a3902-111">Mitigation</span></span>

<span data-ttu-id="a3902-112">Les recommandations actuelles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3902-112">The current recommendations are:</span></span>

-   <span data-ttu-id="a3902-113">Quitter \\ les fichiers programme \\ WindowsApps pour stocker les applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="a3902-113">Move away from \\program files\\WindowsApps for storing any custom apps</span></span>
-   <span data-ttu-id="a3902-114">Les fournisseurs d’antivirus et de logiciels anti-programme malveillant doivent mettre à jour leurs heuristiques afin qu’ils n’identifient pas cet emplacement comme un emplacement malveillant</span><span class="sxs-lookup"><span data-stu-id="a3902-114">Antivirus/antimalware vendors should update their heuristics so they do not identify that location as a malware location</span></span>

 

 




