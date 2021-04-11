---
description: L’attribut mstop spécifie l’heure d’arrêt d’un clip, par rapport au fichier multimédia d’origine.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Attribut mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108479"
---
# <a name="mstop-attribute"></a><span data-ttu-id="0d9a3-103">Attribut mstop</span><span class="sxs-lookup"><span data-stu-id="0d9a3-103">mstop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="0d9a3-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0d9a3-104">\[Deprecated.</span></span> <span data-ttu-id="0d9a3-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d9a3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d9a3-106">L' `mstop` attribut spécifie l’heure d’arrêt d’un clip, par rapport au fichier multimédia d’origine.</span><span class="sxs-lookup"><span data-stu-id="0d9a3-106">The `mstop` attribute specifies the stop time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0d9a3-107">S'applique à</span><span class="sxs-lookup"><span data-stu-id="0d9a3-107">Applies To</span></span>

[<span data-ttu-id="0d9a3-108">**clip**</span><span class="sxs-lookup"><span data-stu-id="0d9a3-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="0d9a3-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="0d9a3-109">Possible Values</span></span>

<span data-ttu-id="0d9a3-110">Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes.</span><span class="sxs-lookup"><span data-stu-id="0d9a3-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="0d9a3-111">Exemple : 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="0d9a3-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="0d9a3-112">Les unités de début peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="0d9a3-112">Leading units can be omitted.</span></span> <span data-ttu-id="0d9a3-113">Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.</span><span class="sxs-lookup"><span data-stu-id="0d9a3-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d9a3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d9a3-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9a3-115">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="0d9a3-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d9a3-116">**IAMTimelineSrc::SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="0d9a3-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



