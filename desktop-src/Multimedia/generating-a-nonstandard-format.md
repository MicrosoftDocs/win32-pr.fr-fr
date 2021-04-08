---
title: Génération d’un format non standard
description: Génération d’un format non standard
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Audio Compression Manager (ACM), formats non standard
- ACM (gestionnaire de compression audio), formats non standard
- Exemples ACM, formats non standard
- acmFormatSuggest fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839933"
---
# <a name="generating-a-nonstandard-format"></a><span data-ttu-id="805de-107">Génération d’un format non standard</span><span class="sxs-lookup"><span data-stu-id="805de-107">Generating a Nonstandard Format</span></span>

<span data-ttu-id="805de-108">Parfois, une application a besoin d’un format non standard.</span><span class="sxs-lookup"><span data-stu-id="805de-108">Sometimes an application needs a nonstandard format.</span></span> <span data-ttu-id="805de-109">Par exemple, une application peut nécessiter un fichier au format ADPCM 16 kHz.</span><span class="sxs-lookup"><span data-stu-id="805de-109">For example, an application might need a 16-kHz ADPCM-format file.</span></span> <span data-ttu-id="805de-110">Étant donné que 16 kHz n’est pas standard, les fonctions d’énumération ne génèrent pas ce format.</span><span class="sxs-lookup"><span data-stu-id="805de-110">Because 16 kHz is nonstandard, the enumeration functions will not generate this format.</span></span> <span data-ttu-id="805de-111">En fait, peu de codage personnalisé des algorithmes de format dans l’application, il n’existe pas de méthode fiable pour générer un format non standard.</span><span class="sxs-lookup"><span data-stu-id="805de-111">In fact, short of custom coding the format algorithms into the application, there is no reliable way to generate a nonstandard format.</span></span> <span data-ttu-id="805de-112">Toutefois, il est parfois possible de générer un format analogue en configurant un format PCM valide avec toutes les informations requises, puis en utilisant la fonction [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) .</span><span class="sxs-lookup"><span data-stu-id="805de-112">It is sometimes possible, however, to generate an analogous format by setting up a valid PCM format with all the required information and then using the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function.</span></span> <span data-ttu-id="805de-113">Étant donné que les compresseurs et les décompresseurs essaient de suggérer un format le plus proche du format souhaité, le nombre de canaux et la fréquence sont généralement préservés.</span><span class="sxs-lookup"><span data-stu-id="805de-113">Because compressors and decompressors try to suggest a format that is closest to the desired format, the number of channels and frequency are usually preserved.</span></span>

 

 




