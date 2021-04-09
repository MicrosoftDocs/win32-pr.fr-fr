---
description: Un jeu de caractères codés sur un octet (SBCS) est un mappage de 256 caractères individuels à leurs valeurs de code d’identification, implémenté comme une page de codes.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Jeux de caractères codés sur un octet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953089"
---
# <a name="single-byte-character-sets"></a><span data-ttu-id="49f6d-103">Jeux de caractères codés sur un octet</span><span class="sxs-lookup"><span data-stu-id="49f6d-103">Single-byte Character Sets</span></span>

<span data-ttu-id="49f6d-104">Un jeu de caractères codés sur un octet (SBCS) est un mappage de 256 caractères individuels à leurs valeurs de code d’identification, implémenté comme une page de codes.</span><span class="sxs-lookup"><span data-stu-id="49f6d-104">A single-byte character set (SBCS) is a mapping of 256 individual characters to their identifying code values, implemented as a code page.</span></span> <span data-ttu-id="49f6d-105">Une valeur SBCS peut correspondre à une page de codes Windows ou à une page de codes OEM.</span><span class="sxs-lookup"><span data-stu-id="49f6d-105">An SBCS can correspond either to a Windows code page or an OEM code page.</span></span> <span data-ttu-id="49f6d-106">Une page de codes SBCS peut également inclure une page de codes non native, par exemple, une page de codes EBCDIC.</span><span class="sxs-lookup"><span data-stu-id="49f6d-106">An SBCS code page can also include a non-native code page, for example, an EBCDIC code page.</span></span> <span data-ttu-id="49f6d-107">Pour obtenir les définitions de ces pages de codes, consultez [pages de codes](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="49f6d-107">For definitions of these code pages, see [Code Pages](code-pages.md).</span></span>

> [!Note]  
> <span data-ttu-id="49f6d-108">Les nouvelles applications Windows doivent utiliser [Unicode](unicode.md) pour éviter les incohérences de pages de codes variées et pour faciliter la localisation.</span><span class="sxs-lookup"><span data-stu-id="49f6d-108">New Windows applications should use [Unicode](unicode.md) to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="49f6d-109">Toutefois, certains protocoles hérités requièrent l’utilisation d’un SBCS.</span><span class="sxs-lookup"><span data-stu-id="49f6d-109">However, some legacy protocols require the use of an SBCS.</span></span> <span data-ttu-id="49f6d-110">Chaque page de codes SBCS prend en charge des caractères différents, mais aucune page ne prend en charge l’intégralité des caractères fournis par Unicode.</span><span class="sxs-lookup"><span data-stu-id="49f6d-110">Each SBCS code page supports different characters, but no page supports the full breadth of characters provided by Unicode.</span></span> <span data-ttu-id="49f6d-111">Chaque page de codes SBCS prend en charge un sous-ensemble différent, encodé différemment.</span><span class="sxs-lookup"><span data-stu-id="49f6d-111">Each SBCS code page supports a different subset, differently encoded.</span></span> <span data-ttu-id="49f6d-112">Les données converties d’une page de codes SBCS vers une autre sont susceptibles d’être endommagées, car la même valeur de données sur des pages de codes différentes peut encoder un caractère différent.</span><span class="sxs-lookup"><span data-stu-id="49f6d-112">Data converted from one SBCS code page to another is subject to corruption, because the same data value on different code pages can encode a different character.</span></span> <span data-ttu-id="49f6d-113">Les données converties d’Unicode en SBCS sont sujettes à des pertes de données, car une page de codes donnée peut ne pas être en mesure de représenter chaque caractère utilisé dans ces données Unicode particulières.</span><span class="sxs-lookup"><span data-stu-id="49f6d-113">Data converted from Unicode to SBCS is subject to data loss because a given code page might not be able to represent every character used in that particular Unicode data.</span></span>

 

<span data-ttu-id="49f6d-114">Vos applications utilisent des pages de code Windows SBCS avec les versions « A » des fonctions Windows.</span><span class="sxs-lookup"><span data-stu-id="49f6d-114">Your applications use SBCS Windows code pages with the "A" versions of Windows functions.</span></span> <span data-ttu-id="49f6d-115">Consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md) et les [pages de codes](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="49f6d-115">See [Conventions for Function Prototypes](conventions-for-function-prototypes.md) and [Code Pages](code-pages.md).</span></span> <span data-ttu-id="49f6d-116">Pour faciliter l’identification d’une page de codes SBCS, une application peut utiliser la fonction [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) ou [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="49f6d-116">To help identify an SBCS code page, an application can use the [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) or [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) function.</span></span> <span data-ttu-id="49f6d-117">En outre, une application peut utiliser les fonctions [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) pour effectuer un mappage entre les chaînes Unicode et SBCS.</span><span class="sxs-lookup"><span data-stu-id="49f6d-117">In addition, an application can use the [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) functions to map between Unicode and SBCS strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49f6d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49f6d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f6d-119">Jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="49f6d-119">Character Sets</span></span>](character-sets.md)
</dt> <dt>

[<span data-ttu-id="49f6d-120">Jeux de caractères codés sur deux octets</span><span class="sxs-lookup"><span data-stu-id="49f6d-120">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
</dt> </dl>

 

 



