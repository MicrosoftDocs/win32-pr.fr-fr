---
title: Fonctions et structures du gestionnaire de compression audio
description: Fonctions et structures du gestionnaire de compression audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimédia, fonctions ACM
- audio, fonctions ACM
- le gestionnaire de compression audio (ACM), fonctions
- ACM (gestionnaire de compression audio), fonctions
- audio multimédia, structures ACM
- audio, structures ACM
- le gestionnaire de compression audio (ACM), structures
- ACM (gestionnaire de compression audio), structures
- Structures ACM
- Fonctions ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106533555"
---
# <a name="audio-compression-manager-functions-and-structures"></a><span data-ttu-id="fe9cb-113">Fonctions et structures du gestionnaire de compression audio</span><span class="sxs-lookup"><span data-stu-id="fe9cb-113">Audio Compression Manager Functions and Structures</span></span>

<span data-ttu-id="fe9cb-114">Les fonctions ACM se répartissent en plusieurs catégories.</span><span class="sxs-lookup"><span data-stu-id="fe9cb-114">The ACM functions fall into several categories.</span></span> <span data-ttu-id="fe9cb-115">Les conventions d’affectation des noms pour les fonctions facilitent l’identification de ces catégories.</span><span class="sxs-lookup"><span data-stu-id="fe9cb-115">Naming conventions for the functions make it easy to identify these categories.</span></span> <span data-ttu-id="fe9cb-116">Les noms de fonctions (à deux exceptions près) se présentent sous la forme *acmGroupFunction*, où *Group* désigne la catégorie ACM (telle que « Driver », « format », « FormatTag », « Filter », « FilterTag » ou « Stream ») et *Function* décrit l’action effectuée par la fonction.</span><span class="sxs-lookup"><span data-stu-id="fe9cb-116">Function names (with two exceptions) are of the form *acmGroupFunction*, where *Group* designates the ACM category (such as "Driver," "Format," "FormatTag," "Filter," "FilterTag," or "Stream"), and *Function* describes the action performed by the function.</span></span>

<span data-ttu-id="fe9cb-117">Les fonctions dans les groupes de filtres et de formats sont très similaires.</span><span class="sxs-lookup"><span data-stu-id="fe9cb-117">The functions in the filter and format groups are very similar.</span></span> <span data-ttu-id="fe9cb-118">Presque toutes les fonctions qui agissent sur les filtres possèdent une fonction parallèle qui agit sur les formats.</span><span class="sxs-lookup"><span data-stu-id="fe9cb-118">Almost every function that acts on filters has a parallel function that acts on formats.</span></span>

<span data-ttu-id="fe9cb-119">Dans le groupe format, certaines fonctions utilisent des balises de format Waveform-Audio (le membre **wFormatTag** d’une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ), tandis que d’autres requièrent des formats audio Wave complets (la structure **WAVEFORMATEX** complète).</span><span class="sxs-lookup"><span data-stu-id="fe9cb-119">In the format group, some functions use waveform-audio format tags (the **wFormatTag** member of a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure) while others require full waveform-audio formats (the full **WAVEFORMATEX** structure).</span></span> <span data-ttu-id="fe9cb-120">(Pour obtenir des informations de référence sur la structure **WAVEFORMATEX** , consultez [erreur](error.md).)</span><span class="sxs-lookup"><span data-stu-id="fe9cb-120">(For reference information about the **WAVEFORMATEX** structure, see [Error](error.md).)</span></span>

<span data-ttu-id="fe9cb-121">Dans le groupe filtre, certaines fonctions utilisent des balises de filtre Waveform-Audio (le membre **dwFilterTag** d’une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), tandis que d’autres requièrent des filtres Wave-audio complets (la structure **WAVEFILTER** complète).</span><span class="sxs-lookup"><span data-stu-id="fe9cb-121">In the filter group, some functions use waveform-audio filter tags (the **dwFilterTag** member of a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure), while others require full waveform-audio filters (the full **WAVEFILTER** structure).</span></span>

<span data-ttu-id="fe9cb-122">Les fonctions du groupe de flux représentent les nombreuses étapes impliquées dans une conversion : ouverture d’une instance de conversion, préparation de la conversion, exécution de la conversion, nettoyage après la conversion terminée et fermeture de l’instance de conversion.</span><span class="sxs-lookup"><span data-stu-id="fe9cb-122">The functions in the stream group represent the many steps involved in a conversion: opening a conversion instance, preparing for the conversion, performing the conversion, cleaning up after the conversion is complete, and closing the conversion instance.</span></span>

 

 