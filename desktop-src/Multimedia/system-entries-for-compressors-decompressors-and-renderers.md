---
title: Entrées système pour les compresseurs, les décompresseurs et les convertisseurs
description: Entrées système pour les compresseurs, les décompresseurs et les convertisseurs
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Video for Windows (VFW), entrées système du compresseur
- VFW (vidéo pour Windows), entrées du système de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675066"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a><span data-ttu-id="1a7f2-105">Entrées système pour les compresseurs, les décompresseurs et les convertisseurs</span><span class="sxs-lookup"><span data-stu-id="1a7f2-105">System Entries for Compressors, Decompressors, and Renderers</span></span>

<span data-ttu-id="1a7f2-106">Le système utilise des entrées du Registre pour rechercher les pilotes VCM.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-106">The system uses entries in the registry to find VCM drivers.</span></span> <span data-ttu-id="1a7f2-107">Ces entrées se présentent sous la forme de codes de 2 4 caractères séparés par un point.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-107">These entries are in the form of two four-character codes separated by a period.</span></span> <span data-ttu-id="1a7f2-108">Le premier code à quatre caractères est défini par le système et peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a7f2-108">The first four-character code is defined by the system and can be one of the following:</span></span>



| <span data-ttu-id="1a7f2-109">Code à quatre caractères</span><span class="sxs-lookup"><span data-stu-id="1a7f2-109">Four-character code</span></span> | <span data-ttu-id="1a7f2-110">Description</span><span class="sxs-lookup"><span data-stu-id="1a7f2-110">Description</span></span>                               |
|---------------------|-------------------------------------------|
| <span data-ttu-id="1a7f2-111">VIDC</span><span class="sxs-lookup"><span data-stu-id="1a7f2-111">"VIDC"</span></span>              | <span data-ttu-id="1a7f2-112">Identifie les compresseurs et les décompresseurs.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-112">Identifies compressors and decompressors.</span></span> |
| <span data-ttu-id="1a7f2-113">"VIDS"</span><span class="sxs-lookup"><span data-stu-id="1a7f2-113">"VIDS"</span></span>              | <span data-ttu-id="1a7f2-114">Identifie les convertisseurs de flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-114">Identifies video-stream renderers.</span></span>        |
| <span data-ttu-id="1a7f2-115">"TXTS"</span><span class="sxs-lookup"><span data-stu-id="1a7f2-115">"TXTS"</span></span>              | <span data-ttu-id="1a7f2-116">Identifie les convertisseurs de flux de texte.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-116">Identifies text-stream renderers.</span></span>         |
| <span data-ttu-id="1a7f2-117">"AUDS"</span><span class="sxs-lookup"><span data-stu-id="1a7f2-117">"AUDS"</span></span>              | <span data-ttu-id="1a7f2-118">Identifie les gestionnaires de flux audio.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-118">Identifies audio-stream handlers.</span></span>         |



 

<span data-ttu-id="1a7f2-119">Les convertisseurs personnalisés peuvent définir leurs propres codes à quatre caractères.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-119">Custom renderers can define their own four-character codes.</span></span>

<span data-ttu-id="1a7f2-120">Le deuxième code à quatre caractères est défini par le pilote.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-120">The second four-character code is defined by the driver.</span></span> <span data-ttu-id="1a7f2-121">En règle générale, le deuxième code de quatre caractères correspond au type de données que le pilote peut gérer.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-121">Typically, the second four-character code corresponds to the type of data the driver can handle.</span></span>

<span data-ttu-id="1a7f2-122">Lors de l’ouverture d’un pilote VCM, une application spécifie le type de pilote et le type de gestionnaire de données dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-122">When opening a VCM driver, an application specifies the type of driver and the type of data handler it needs.</span></span> <span data-ttu-id="1a7f2-123">En règle générale, ces informations proviennent de l’en-tête de flux.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-123">Typically, this information comes from the stream header.</span></span> <span data-ttu-id="1a7f2-124">Le système tente d’ouvrir le gestionnaire de données spécifié, mais en cas d’échec, le système recherche un pilote doté du gestionnaire requis dans le registre.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-124">The system tries to open the specified data handler, but if it fails, the system searches the registry for a driver that has the required handler.</span></span>

<span data-ttu-id="1a7f2-125">Lors de la recherche du pilote, le système tente de faire correspondre les codes à quatre caractères spécifiés pour le type de pilote et le gestionnaire de données avec ceux spécifiés dans l’entrée du pilote.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-125">When searching for the driver, the system tries to match the four-character codes specified for the driver type and data handler with those specified in the driver entry.</span></span> <span data-ttu-id="1a7f2-126">Par exemple, si une application spécifie le compresseur MSSQ, le système recherche l’entrée de pilote VIDC. MSSQ dans le registre.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-126">For example, if an application specifies the compressor MSSQ, the system searches the registry for the driver entry VIDC.MSSQ.</span></span> <span data-ttu-id="1a7f2-127">S’il ne trouve pas de correspondance, il ouvre chaque pilote correspondant au type de pilote et en trouve un qui peut gérer le type de données que votre application spécifie.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-127">If it cannot find a match, it opens each driver corresponding to the driver type and locates one that can handle the type of data your application specifies.</span></span> <span data-ttu-id="1a7f2-128">Dans l’exemple précédent, si le système n’a pas pu trouver VIDC. MSSQ, il ouvre tous les pilotes avec le code à quatre caractères « VIDC » et en trouve un qui peut gérer les données.</span><span class="sxs-lookup"><span data-stu-id="1a7f2-128">In the previous example, if the system could not find VIDC.MSSQ, it would open all drivers with the "VIDC" four-character code and locate one that can handle the data.</span></span>

 

 




