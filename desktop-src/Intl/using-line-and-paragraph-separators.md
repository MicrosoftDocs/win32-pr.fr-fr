---
description: Vos applications doivent utiliser le caractère de séparation de ligne (0x2028) et le caractère de séparation de paragraphe (0x2029) pour diviser le texte brut. Une ligne est créée après chaque séparateur de lignes. Un paragraphe est créé après chaque séparateur de paragraphes.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Utilisation de séparateurs de ligne et de paragraphe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210938"
---
# <a name="using-line-and-paragraph-separators"></a><span data-ttu-id="af255-105">Utilisation de séparateurs de ligne et de paragraphe</span><span class="sxs-lookup"><span data-stu-id="af255-105">Using Line and Paragraph Separators</span></span>

<span data-ttu-id="af255-106">Vos applications doivent utiliser le caractère de séparation de ligne (0x2028) et le caractère de séparation de paragraphe (0x2029) pour diviser le texte brut.</span><span class="sxs-lookup"><span data-stu-id="af255-106">Your applications should use the line separator character (0x2028) and the paragraph separator character (0x2029) to divide plain text.</span></span> <span data-ttu-id="af255-107">Une ligne est créée après chaque séparateur de lignes.</span><span class="sxs-lookup"><span data-stu-id="af255-107">A new line is begun after each line separator.</span></span> <span data-ttu-id="af255-108">Un paragraphe est créé après chaque séparateur de paragraphes.</span><span class="sxs-lookup"><span data-stu-id="af255-108">A new paragraph is begun after each paragraph separator.</span></span>

<span data-ttu-id="af255-109">Il n’est pas nécessaire de commencer la première ligne ou le premier paragraphe dans un fichier contenant ces caractères ou de mettre fin à la dernière ligne ou au dernier paragraphe.</span><span class="sxs-lookup"><span data-stu-id="af255-109">It is not necessary to start the first line or paragraph in a file with these characters, or to end the last line or paragraph with them.</span></span> <span data-ttu-id="af255-110">Cela indique qu’il y a une ligne ou un paragraphe vide à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="af255-110">Doing so indicates that there is an empty line or paragraph in that location.</span></span>

<span data-ttu-id="af255-111">L’application peut utiliser le séparateur de ligne pour indiquer une fin de ligne inconditionnelle.</span><span class="sxs-lookup"><span data-stu-id="af255-111">The application can use the line separator to indicate an unconditional end of line.</span></span> <span data-ttu-id="af255-112">Toutefois, les séparateurs de lignes ne correspondent pas aux caractères distincts de retour chariot et de saut de ligne, ni à une combinaison de ces caractères.</span><span class="sxs-lookup"><span data-stu-id="af255-112">However, line separators do not correspond to the separate carriage return and linefeed characters, or to a combination of these characters.</span></span> <span data-ttu-id="af255-113">Les séparateurs de lignes doivent être traités séparément des caractères de saut de ligne et de retour chariot.</span><span class="sxs-lookup"><span data-stu-id="af255-113">Line separators must be processed separately from carriage return and linefeed characters.</span></span>

<span data-ttu-id="af255-114">L’application peut insérer un séparateur de paragraphe entre des paragraphes de texte.</span><span class="sxs-lookup"><span data-stu-id="af255-114">The application can insert a paragraph separator between paragraphs of text.</span></span> <span data-ttu-id="af255-115">L’utilisation de ce séparateur vous permet de créer des fichiers de texte brut qui peuvent être mis en forme avec des largeurs de ligne distinctes sur différents systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="af255-115">Use of this separator allows creation of plain text files that can be formatted with different line widths on different operating systems.</span></span> <span data-ttu-id="af255-116">Le système cible peut ignorer les séparateurs de lignes et interrompre les paragraphes uniquement au niveau des séparateurs de paragraphes.</span><span class="sxs-lookup"><span data-stu-id="af255-116">The target system can ignore any line separators and break paragraphs only at the paragraph separators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af255-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af255-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af255-118">Utilisation de caractères spéciaux en Unicode</span><span class="sxs-lookup"><span data-stu-id="af255-118">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



