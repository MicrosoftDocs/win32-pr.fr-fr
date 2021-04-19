---
description: Le format de police OpenType Unicode étend le format de fichier de police TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Format des polices OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538023"
---
# <a name="opentype-font-format"></a><span data-ttu-id="a0208-103">Format des polices OpenType</span><span class="sxs-lookup"><span data-stu-id="a0208-103">OpenType Font Format</span></span>

<span data-ttu-id="a0208-104">Le format de police OpenType Unicode étend le format de fichier de police TrueType.</span><span class="sxs-lookup"><span data-stu-id="a0208-104">The Unicode-based OpenType font format extends the TrueType font file format.</span></span> <span data-ttu-id="a0208-105">Les polices OpenType autorisent le mappage entre les caractères et les [glyphes](uniscribe-glossary.md), en activant la prise en charge des ligatures, des formes positionnelles, des alternatives et d’autres substitutions.</span><span class="sxs-lookup"><span data-stu-id="a0208-105">OpenType fonts allow mapping between characters and [glyphs](uniscribe-glossary.md), enabling support for ligatures, positional forms, alternates, and other substitutions.</span></span> <span data-ttu-id="a0208-106">Les polices OpenType peuvent également inclure des informations qui prennent en charge le positionnement de glyphes à deux dimensions et une pièce jointe de glyphes, et peuvent contenir des contours TrueType ou PostScript.</span><span class="sxs-lookup"><span data-stu-id="a0208-106">OpenType fonts can also include information that supports two-dimensional glyph positioning and glyph attachment, and can contain either TrueType or PostScript outlines.</span></span>

<span data-ttu-id="a0208-107">Les fonctionnalités de disposition dans les polices OpenType sont organisées par scripts et langages, ce qui permet à une police unique de prendre en charge plusieurs systèmes d’écriture, même au sein du même script.</span><span class="sxs-lookup"><span data-stu-id="a0208-107">Layout features within OpenType fonts are organized by scripts and languages, allowing a single font to support multiple writing systems, even within the same script.</span></span> <span data-ttu-id="a0208-108">Pour garantir la cohérence des opérations de disposition du texte et éviter une surcharge inutile dans les fichiers de polices ou les applications, un grand nombre des algorithmes de mise en page du texte et des algorithmes sémantiques de langage sont inclus dans Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="a0208-108">To ensure consistency in text layout operations and to avoid unnecessary overhead in font files or applications, many of the text layout and language semantic algorithms are included in Uniscribe.</span></span> <span data-ttu-id="a0208-109">Cela évite au développeur de polices d’avoir à définir des règles de script généralisées dans une police.</span><span class="sxs-lookup"><span data-stu-id="a0208-109">This relieves the font developer from having to define generalized script rules within a font.</span></span>

<span data-ttu-id="a0208-110">Les applications peuvent introduire des connaissances ou des préférences spécifiques concernant la disposition des scripts.</span><span class="sxs-lookup"><span data-stu-id="a0208-110">Applications can introduce specific knowledge or preferences regarding script layout.</span></span> <span data-ttu-id="a0208-111">Les polices de disposition OpenType peuvent même contenir des règles de disposition qui dupliquent ou remplacent celles appliquées par les services du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a0208-111">OpenType layout fonts might even contain layout rules that duplicate or supersede those applied by operating system services.</span></span> <span data-ttu-id="a0208-112">La structure en couches des services de système d’exploitation prenant en charge la disposition du texte permet à une application de choisir les informations de mise en page à utiliser, et de choisir comment l’appliquer.</span><span class="sxs-lookup"><span data-stu-id="a0208-112">The layered structure of operating system services supporting text layout allows an application to choose the layout information to use, and select how to apply it.</span></span> <span data-ttu-id="a0208-113">Pour plus d’informations, consultez la [vue d’ensemble des spécifications de typographie Microsoft](https://www.microsoft.com/typography/SpecificationsOverview.mspx) ou la [spécification OpenType](https://www.microsoft.com/typography/otspec/).</span><span class="sxs-lookup"><span data-stu-id="a0208-113">For additional information, see the [Microsoft Typography Specifications overview](https://www.microsoft.com/typography/SpecificationsOverview.mspx) or the [OpenType Specification](https://www.microsoft.com/typography/otspec/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0208-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0208-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0208-115">À propos de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="a0208-115">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



