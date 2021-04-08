---
description: Les clusters de caractères sont des séquences de glyphes qui ne peuvent pas être fractionnées entre les lignes.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Utilisation de clusters de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760486"
---
# <a name="using-character-clusters"></a><span data-ttu-id="870a4-103">Utilisation de clusters de caractères</span><span class="sxs-lookup"><span data-stu-id="870a4-103">Using Character Clusters</span></span>

<span data-ttu-id="870a4-104">Les clusters de caractères sont des séquences de glyphes qui ne peuvent pas être fractionnées entre les lignes.</span><span class="sxs-lookup"><span data-stu-id="870a4-104">Character clusters are glyph sequences that cannot be split between lines.</span></span> <span data-ttu-id="870a4-105">Certains langages, par exemple thaï et Indo-aryen, limitent l’emplacement du signe insertion aux points entre les clusters.</span><span class="sxs-lookup"><span data-stu-id="870a4-105">Some languages, for example Thai and Indic, restrict caret placement to points between clusters.</span></span> <span data-ttu-id="870a4-106">Cette restriction s’applique au déplacement du signe insertion initié avec les actions du clavier ou de la souris (test de positionnement).</span><span class="sxs-lookup"><span data-stu-id="870a4-106">This restriction applies to caret movement initiated with keyboard or mouse actions (hit testing).</span></span>

<span data-ttu-id="870a4-107">Uniscribe fournit des informations de cluster dans les attributs visuels contenus dans une structure de [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) et les attributs logiques contenus dans une structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="870a4-107">Uniscribe provides cluster information in both the visual attributes contained in a [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure, and the logical attributes contained in a [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="870a4-108">Une fois que l’application a appelé [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), les informations de cluster sont représentées à la fois par séquences de la même valeur dans le tableau **\_ LOGATTR de script** et par le membre **FClusterStart** dans le tableau **\_ VISATTR de script** .</span><span class="sxs-lookup"><span data-stu-id="870a4-108">After the application calls [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), the cluster information is represented both by sequences of the same value in the **SCRIPT\_LOGATTR** array, and by the **fClusterStart** member in the **SCRIPT\_VISATTR** array.</span></span>

<span data-ttu-id="870a4-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) récupère également le membre **fCharStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) pour identifier les positions de cluster.</span><span class="sxs-lookup"><span data-stu-id="870a4-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) also retrieves the **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure to identify cluster positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="870a4-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="870a4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="870a4-111">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="870a4-111">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



