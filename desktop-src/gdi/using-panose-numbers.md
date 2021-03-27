---
description: Les fichiers de polices TrueType incluent des nombres Panose, que les applications peuvent utiliser pour choisir une police qui correspond précisément à leurs spécifications.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Utilisation de nombres Panose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209956"
---
# <a name="using-panose-numbers"></a><span data-ttu-id="d309c-103">Utilisation de nombres Panose</span><span class="sxs-lookup"><span data-stu-id="d309c-103">Using PANOSE Numbers</span></span>

<span data-ttu-id="d309c-104">Les fichiers de polices TrueType incluent des nombres Panose, que les applications peuvent utiliser pour choisir une police qui correspond précisément à leurs spécifications.</span><span class="sxs-lookup"><span data-stu-id="d309c-104">TrueType font files include PANOSE numbers, which applications can use to choose a font that closely matches their specifications.</span></span> <span data-ttu-id="d309c-105">Le système PANOSE classe les visages par 10 attributs différents.</span><span class="sxs-lookup"><span data-stu-id="d309c-105">The PANOSE system classifies faces by 10 different attributes.</span></span> <span data-ttu-id="d309c-106">Pour plus d’informations sur ces attributs, consultez [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose).</span><span class="sxs-lookup"><span data-stu-id="d309c-106">For more information about these attributes, see [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose).</span></span> <span data-ttu-id="d309c-107">Une structure **Panose** fait partie de la structure [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (dont les valeurs sont remplies en appelant la fonction [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).</span><span class="sxs-lookup"><span data-stu-id="d309c-107">A **PANOSE** structure is part of the [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) structure (whose values are filled in by calling the [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) function).</span></span>

<span data-ttu-id="d309c-108">Les attributs Panose sont évalués individuellement sur une échelle.</span><span class="sxs-lookup"><span data-stu-id="d309c-108">The PANOSE attributes are rated individually on a scale.</span></span> <span data-ttu-id="d309c-109">Les valeurs résultantes sont concaténées pour produire un nombre.</span><span class="sxs-lookup"><span data-stu-id="d309c-109">The resulting values are concatenated to produce a number.</span></span> <span data-ttu-id="d309c-110">Étant donné ce nombre pour une police et une mesure mathématique pour mesurer les distances dans l’espace Panose, une application peut déterminer les voisins les plus proches.</span><span class="sxs-lookup"><span data-stu-id="d309c-110">Given this number for a font and a mathematical metric to measure distances in the PANOSE space, an application can determine the nearest neighbors.</span></span>

 

 



