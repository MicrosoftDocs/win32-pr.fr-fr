---
description: Un script complexe est un script pour lequel le membre fComplex des propriétés de SCRIPT \_ a la valeur true. Cette rubrique détaille les propriétés qu’un script complexe peut avoir.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: À propos des scripts complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034797"
---
# <a name="about-complex-scripts"></a><span data-ttu-id="1fc7f-104">À propos des scripts complexes</span><span class="sxs-lookup"><span data-stu-id="1fc7f-104">About Complex Scripts</span></span>

<span data-ttu-id="1fc7f-105">Un [script complexe](uniscribe-glossary.md) est un script pour lequel le membre **fcomplex** des [**\_ Propriétés de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-105">A [complex script](uniscribe-glossary.md) is a script for which the **fComplex** member of [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) is set to **TRUE**.</span></span> <span data-ttu-id="1fc7f-106">Cette rubrique détaille les propriétés qu’un script complexe peut avoir.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-106">This topic details the properties that a complex script might have.</span></span>

## <a name="bidirectional-rendering"></a><span data-ttu-id="1fc7f-107">Rendu bidirectionnel</span><span class="sxs-lookup"><span data-stu-id="1fc7f-107">Bidirectional Rendering</span></span>

<span data-ttu-id="1fc7f-108">Le rendu bidirectionnel est le traitement du texte qui lit de gauche à droite et de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-108">Bidirectional rendering is handling of text that reads both left-to-right and right-to-left.</span></span> <span data-ttu-id="1fc7f-109">Par exemple, dans le rendu bidirectionnel de l’arabe, le sens de lecture par défaut pour le texte est de droite à gauche, mais il est de gauche à droite pour certains nombres.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-109">For example, in the bidirectional rendering of Arabic, the default reading direction for text is right-to-left, but it is left-to-right for some numbers.</span></span> <span data-ttu-id="1fc7f-110">Le traitement d’un script complexe doit tenir compte de la différence entre l’ordre logique (frappe) et l’ordre visuel des glyphes.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-110">Processing a complex script must account for the difference between the logical (keystroke) order and the visual order of the glyphs.</span></span> <span data-ttu-id="1fc7f-111">En outre, le traitement doit correctement gérer le mouvement du signe insertion et le test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-111">In addition, processing must properly deal with caret movement and hit testing.</span></span> <span data-ttu-id="1fc7f-112">Le mappage entre la position de l’écran et un index de caractère requiert une compréhension des algorithmes de disposition pour l’affichage particulier, par exemple, la sélection de texte ou l’affichage du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-112">The mapping between screen position and a character index requires an understanding of the layout algorithms for the particular display, for example, selection of text or caret display.</span></span>

## <a name="contextual-shaping"></a><span data-ttu-id="1fc7f-113">Mise en forme contextuelle</span><span class="sxs-lookup"><span data-stu-id="1fc7f-113">Contextual Shaping</span></span>

<span data-ttu-id="1fc7f-114">Dans le cadre de la mise en forme contextuelle, les caractères de script changent de forme en fonction des caractères qui les entourent.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-114">In contextual shaping, script characters change shape depending on the characters that surround them.</span></span> <span data-ttu-id="1fc7f-115">Une telle mise en forme se produit en anglais en écriture cursive quand un « l » minuscule change de forme en fonction du caractère qui le précède, par exemple un « a » (se connecte au « l ») ou un « o » (se connecte à un niveau élevé).</span><span class="sxs-lookup"><span data-stu-id="1fc7f-115">Such shaping occurs in English cursive writing when a lowercase "l" changes shape depending on the character that precedes it, such as an "a" (connects low to the "l") or an "o" (connects high).</span></span> <span data-ttu-id="1fc7f-116">Par exemple, l’arabe est un script qui présente une mise en forme contextuelle.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-116">For example, Arabic is a script that exhibits contextual shaping.</span></span>

## <a name="combining-characters"></a><span data-ttu-id="1fc7f-117">Combinaison de caractères</span><span class="sxs-lookup"><span data-stu-id="1fc7f-117">Combining Characters</span></span>

<span data-ttu-id="1fc7f-118">La combinaison de caractères, également appelée « ligatures », sont des caractères qui se joignent dans un caractère lorsqu’ils sont placés ensemble.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-118">Combining characters, also called "ligatures," are characters that join into one character when placed together.</span></span> <span data-ttu-id="1fc7f-119">L’arabe est un script qui comporte de nombreux caractères d’association.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-119">Arabic is a script that has many combining characters.</span></span> <span data-ttu-id="1fc7f-120">Un exemple de l’utilisation de la combinaison de caractères est le « a » suivi de « combinaison de caractères graves », pour lequel la représentation rendue est « à ».</span><span class="sxs-lookup"><span data-stu-id="1fc7f-120">One example of the use of combining characters is the "a" followed by "combining grave", for which the rendered representation is "à".</span></span> <span data-ttu-id="1fc7f-121">Le flux Unicode « U + 0061 U + 0300 » requiert un traitement pour s’assurer que la combinaison « combinaison grave » est correctement positionnée au-dessus du « a ».</span><span class="sxs-lookup"><span data-stu-id="1fc7f-121">The Unicode stream "U+0061 U+0300" requires some processing to make sure the "combining grave" is correctly positioned above the "a".</span></span>

## <a name="specialized-word-break-and-justification"></a><span data-ttu-id="1fc7f-122">Césure et justification de mot spécialisées</span><span class="sxs-lookup"><span data-stu-id="1fc7f-122">Specialized Word Break and Justification</span></span>

<span data-ttu-id="1fc7f-123">Certains scripts, par exemple, le thaï, comportent des règles complexes pour diviser les mots entre les lignes ou pour justifier du texte sur une ligne.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-123">Some scripts, for example, Thai, have complex rules for dividing words between lines or justifying text on a line.</span></span>

## <a name="filtering-for-illegal-character-combinations"></a><span data-ttu-id="1fc7f-124">Filtrage pour les combinaisons de caractères non conformes</span><span class="sxs-lookup"><span data-stu-id="1fc7f-124">Filtering for Illegal Character Combinations</span></span>

<span data-ttu-id="1fc7f-125">Un script complexe, par exemple thaï, peut filtrer les combinaisons de caractères non conformes lorsqu’une langue n’autorise pas certaines combinaisons de caractères.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-125">A complex script, for example, Thai, can filter out illegal character combinations when a language does not allow certain character combinations.</span></span>

## <a name="font-fallback"></a><span data-ttu-id="1fc7f-126">Police de secours</span><span class="sxs-lookup"><span data-stu-id="1fc7f-126">Font Fallback</span></span>

<span data-ttu-id="1fc7f-127">La police de secours est la sélection automatisée d’une police autre que la police sélectionnée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-127">Font fallback is the automated selection of a font other than the font selected by the user.</span></span> <span data-ttu-id="1fc7f-128">Dans Uniscribe, la police de secours est appliquée par la fonction [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) lorsque la totalité ou une partie du texte est dans un script que la police sélectionnée par l’utilisateur ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-128">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span> <span data-ttu-id="1fc7f-129">Pour plus d’informations, consultez Utilisation de la [police de secours](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="1fc7f-129">For more information, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fc7f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fc7f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fc7f-131">À propos de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="1fc7f-131">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



