---
title: Recherche d’un format spécifique
description: Recherche d’un format spécifique
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- le gestionnaire de compression audio (ACM), recherche de formats
- ACM (gestionnaire de compression audio), recherche de formats
- Exemples ACM, recherche de formats
- recherche de formats
- acmFormatEnum fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940231"
---
# <a name="finding-a-specific-format"></a><span data-ttu-id="b0fb9-108">Recherche d’un format spécifique</span><span class="sxs-lookup"><span data-stu-id="b0fb9-108">Finding a Specific Format</span></span>

<span data-ttu-id="b0fb9-109">Une application ne peut avoir qu’une spécification partielle pour un format lorsqu’elle a besoin de la spécification complète.</span><span class="sxs-lookup"><span data-stu-id="b0fb9-109">An application might have only a partial specification for a format when it needs the full specification.</span></span> <span data-ttu-id="b0fb9-110">Par exemple, la spécification peut stipuler un format ADPCM à 16 bits, qui n’est pas le nombre moyen d’octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="b0fb9-110">For example, the specification might stipulate an 11-kHz mono, 4-bit ADPCM format, but not the average bytes per second.</span></span> <span data-ttu-id="b0fb9-111">L’application peut obtenir le format complet sans intervention de l’utilisateur à l’aide de la fonction [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) et en spécifiant des indicateurs dans le paramètre *fdwEnum* .</span><span class="sxs-lookup"><span data-stu-id="b0fb9-111">The application can get the full format without user intervention by using the [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) function and specifying flags in the *fdwEnum* parameter.</span></span>

 

 




