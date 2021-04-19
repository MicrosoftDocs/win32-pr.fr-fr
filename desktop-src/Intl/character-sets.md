---
description: Un &\# 0034 ; jeu de caractères&\# 0034 ; est un mappage de caractères avec leurs valeurs de code d’identification.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Character Sets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514172"
---
# <a name="character-sets"></a><span data-ttu-id="1fa93-103">Character Sets</span><span class="sxs-lookup"><span data-stu-id="1fa93-103">Character Sets</span></span>

<span data-ttu-id="1fa93-104">Un « jeu de caractères » est un mappage de caractères avec leurs valeurs de code d’identification.</span><span class="sxs-lookup"><span data-stu-id="1fa93-104">A "character set" is a mapping of characters to their identifying code values.</span></span> <span data-ttu-id="1fa93-105">Le jeu de caractères le plus couramment utilisé dans les ordinateurs actuels est [Unicode](unicode.md), une norme globale pour l’encodage des caractères.</span><span class="sxs-lookup"><span data-stu-id="1fa93-105">The character set most commonly used in computers today is [Unicode](unicode.md), a global standard for character encoding.</span></span> <span data-ttu-id="1fa93-106">En interne, les applications Windows utilisent l’implémentation UTF-16 d’Unicode.</span><span class="sxs-lookup"><span data-stu-id="1fa93-106">Internally, Windows applications use the UTF-16 implementation of Unicode.</span></span> <span data-ttu-id="1fa93-107">En UTF-16, la plupart des caractères sont identifiés par des codes à deux octets.</span><span class="sxs-lookup"><span data-stu-id="1fa93-107">In UTF-16, most characters are identified by two-byte codes.</span></span> <span data-ttu-id="1fa93-108">Les caractères supplémentaires les moins communément utilisés sont représentés par une paire de substitution, qui est une paire de codes à deux octets.</span><span class="sxs-lookup"><span data-stu-id="1fa93-108">The less commonly used supplementary characters are each represented by a surrogate pair, which is a pair of two-byte codes.</span></span> <span data-ttu-id="1fa93-109">Pour plus d’informations, consultez [substituts et caractères supplémentaires](surrogates-and-supplementary-characters.md).</span><span class="sxs-lookup"><span data-stu-id="1fa93-109">For more information, see [Surrogates and Supplementary Characters](surrogates-and-supplementary-characters.md).</span></span>

<span data-ttu-id="1fa93-110">Certaines applications Windows doivent fonctionner avec les jeux de caractères plus anciens qui sont natifs pour Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="1fa93-110">Some Windows applications must work with the older character sets that are native to Windows Me/98/95.</span></span> <span data-ttu-id="1fa93-111">Les [pages de codes Windows](code-pages.md) permettent à votre application de travailler avec ces jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="1fa93-111">[Windows code pages](code-pages.md) allow your application to work with these character sets.</span></span> <span data-ttu-id="1fa93-112">Ces jeux de caractères peuvent être divisés en :</span><span class="sxs-lookup"><span data-stu-id="1fa93-112">These character sets can be divided into:</span></span>

-   <span data-ttu-id="1fa93-113">[Jeux de caractères codés sur un octet](single-byte-character-sets.md) (SBCS).</span><span class="sxs-lookup"><span data-stu-id="1fa93-113">[Single-byte character sets](single-byte-character-sets.md) (SBCS).</span></span> <span data-ttu-id="1fa93-114">Dans un SBCS, chaque caractère est identifié par une valeur d’un octet en largeur.</span><span class="sxs-lookup"><span data-stu-id="1fa93-114">In an SBCS, each character is identified by a value one byte wide.</span></span>
-   <span data-ttu-id="1fa93-115">Jeux de caractères multioctets, en particulier les [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS).</span><span class="sxs-lookup"><span data-stu-id="1fa93-115">Multibyte character sets, in particular the [double-byte character sets](double-byte-character-sets.md) (DBCS).</span></span> <span data-ttu-id="1fa93-116">Les jeux de caractères multioctets offrent un moyen de représenter le grand nombre de caractères dans de nombreuses langues asiatiques.</span><span class="sxs-lookup"><span data-stu-id="1fa93-116">Multibyte character sets provide a means to represent the large number of characters in many Asian languages.</span></span>

<span data-ttu-id="1fa93-117">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fa93-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1fa93-118">Pages de codes</span><span class="sxs-lookup"><span data-stu-id="1fa93-118">Code Pages</span></span>](code-pages.md)
-   [<span data-ttu-id="1fa93-119">Jeux de caractères codés sur deux octets</span><span class="sxs-lookup"><span data-stu-id="1fa93-119">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
-   [<span data-ttu-id="1fa93-120">Jeux de caractères codés sur un octet</span><span class="sxs-lookup"><span data-stu-id="1fa93-120">Single-byte Character Sets</span></span>](single-byte-character-sets.md)
-   [<span data-ttu-id="1fa93-121">Substituts et caractères supplémentaires</span><span class="sxs-lookup"><span data-stu-id="1fa93-121">Surrogates and Supplementary Characters</span></span>](surrogates-and-supplementary-characters.md)
-   [<span data-ttu-id="1fa93-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="1fa93-122">Unicode</span></span>](unicode.md)

## <a name="related-topics"></a><span data-ttu-id="1fa93-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fa93-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa93-124">À propos d’Unicode et des jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="1fa93-124">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



