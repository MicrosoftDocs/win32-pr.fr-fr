---
description: paramètres régionaux \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516912"
---
# <a name="locale_sscripts"></a><span data-ttu-id="f3fe0-103">paramètres régionaux \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="f3fe0-103">LOCALE\_SSCRIPTS</span></span>

<span data-ttu-id="f3fe0-104">**Windows Vista et versions ultérieures :** Chaîne représentant une liste de scripts, à l’aide de la notation à 4 caractères utilisée dans [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-104">**Windows Vista and later:** A string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="f3fe0-105">Chaque nom de script se compose de quatre caractères latins et la liste est triée par ordre alphabétique avec chaque nom, y compris le dernier, suivi d’un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-105">Each script name consists of four Latin characters and the list is arranged in alphabetical order with each name, including the last, followed by a semicolon.</span></span>

<span data-ttu-id="f3fe0-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) peut être appelé avec *LCTYPE* défini sur locale \_ SSCRIPTS dans le cadre d’une stratégie visant à limiter les problèmes de sécurité liés aux noms de domaine internationaux (IDNs).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can be called with *LCType* set to LOCALE\_SSCRIPTS as part of a strategy to mitigate security issues related to Internationalized Domain Names (IDNs).</span></span> <span data-ttu-id="f3fe0-107">Voici quelques exemples de valeurs :</span><span class="sxs-lookup"><span data-stu-id="f3fe0-107">Here are some example values:</span></span>



| <span data-ttu-id="f3fe0-108">Paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="f3fe0-108">Locale</span></span>                  | <span data-ttu-id="f3fe0-109">Nom de paramètres régionaux/langue</span><span class="sxs-lookup"><span data-stu-id="f3fe0-109">Locale/language name</span></span> | <span data-ttu-id="f3fe0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3fe0-110">Value</span></span>                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3fe0-111">Anglais (États-Unis)</span><span class="sxs-lookup"><span data-stu-id="f3fe0-111">English (United States)</span></span> | <span data-ttu-id="f3fe0-112">fr-FR</span><span class="sxs-lookup"><span data-stu-id="f3fe0-112">en-US</span></span>                | <span data-ttu-id="f3fe0-113">LATN</span><span class="sxs-lookup"><span data-stu-id="f3fe0-113">Latn;</span></span>                                                                                                  |
| <span data-ttu-id="f3fe0-114">Hindi (Inde)</span><span class="sxs-lookup"><span data-stu-id="f3fe0-114">Hindi (India)</span></span>           | <span data-ttu-id="f3fe0-115">hi-IN</span><span class="sxs-lookup"><span data-stu-id="f3fe0-115">hi-IN</span></span>                | <span data-ttu-id="f3fe0-116">Deva</span><span class="sxs-lookup"><span data-stu-id="f3fe0-116">Deva;</span></span>                                                                                                  |
| <span data-ttu-id="f3fe0-117">Japonais (Japon)</span><span class="sxs-lookup"><span data-stu-id="f3fe0-117">Japanese (Japan)</span></span>        | <span data-ttu-id="f3fe0-118">ja-JP</span><span class="sxs-lookup"><span data-stu-id="f3fe0-118">ja-JP</span></span>                | <span data-ttu-id="f3fe0-119">**Windows 7 et versions ultérieures :** Hani; Hira; Jpan; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="f3fe0-119">**Windows 7 and later:** Hani;Hira;Jpan;Kana;</span></span><br/> <span data-ttu-id="f3fe0-120">**Windows Vista :** Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="f3fe0-120">**Windows Vista:** Hani;Hira;Kana;</span></span><br/> |



 

<span data-ttu-id="f3fe0-121">Une valeur de script composé n’inclut pas le script latin, sauf s’il s’agit d’une partie essentielle du système d’écriture utilisé pour les paramètres régionaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-121">A compound script value does not include the Latin script unless it is an essential part of the writing system used for the particular locale.</span></span> <span data-ttu-id="f3fe0-122">Les caractères latins sont souvent utilisés dans le contexte des paramètres régionaux pour lesquels ils ne sont pas natifs, par exemple, pour un nom d’entreprise étranger.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-122">Latin characters are often used in the context of locales for which they are not native, for example, for a foreign business name.</span></span> <span data-ttu-id="f3fe0-123">Dans l’exemple ci-dessus pour l’hindi en Inde, la seule valeur de script est « Deva » (pour « DÉVANÂGARÎ »), bien que les caractères latins puissent également apparaître dans le texte hindi.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-123">In the example above for Hindi in India, the only script value is "Deva" (for "Devanagari"), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="f3fe0-124">La fonction [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) a un indicateur spécial pour traiter ce cas.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-124">The [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) function has a special flag to address this case.</span></span>

 

 




