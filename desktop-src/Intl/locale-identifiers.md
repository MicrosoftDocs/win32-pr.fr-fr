---
description: Chaque paramètre régional a un identificateur unique, une valeur de 32 bits qui se compose d’un identificateur de langue et d’un identificateur d’ordre de tri.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificateurs de paramètres régionaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514973"
---
# <a name="locale-identifiers"></a><span data-ttu-id="a8030-103">Identificateurs de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="a8030-103">Locale Identifiers</span></span>

<span data-ttu-id="a8030-104">Chaque [paramètre régional](locales-and-languages.md) a un identificateur unique, une valeur de 32 bits qui se compose d’un [identificateur de langue](language-identifiers.md) et d’un [identificateur d’ordre de tri](sort-order-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="a8030-104">Each [locale](locales-and-languages.md) has a unique identifier, a 32-bit value that consists of a [language identifier](language-identifiers.md) and a [sort order identifier](sort-order-identifiers.md).</span></span> <span data-ttu-id="a8030-105">L’identificateur de paramètres régionaux est une abréviation numérique internationale standard et contient les composants nécessaires pour identifier de manière unique l’un des paramètres régionaux définis par le système d’exploitation installés.</span><span class="sxs-lookup"><span data-stu-id="a8030-105">The locale identifier is a standard international numeric abbreviation and has the components necessary to uniquely identify one of the installed operating system-defined locales.</span></span> <span data-ttu-id="a8030-106">NLS prend en charge les identificateurs de paramètres régionaux prédéfinis et les identificateurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="a8030-106">NLS supports both predefined locale identifiers and custom identifiers.</span></span>

> [!Note]  
> <span data-ttu-id="a8030-107">Les noms de paramètres régionaux peuvent être utilisés avec les fonctions introduites dans Windows Vista qui acceptent un [nom de paramètres régionaux](locale-names.md) en tant que paramètre, au lieu d’un identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="a8030-107">Locale names can be used with functions introduced in Windows Vista that take a [locale name](locale-names.md) as a parameter, instead of a locale identifier.</span></span> <span data-ttu-id="a8030-108">Pour plus d’informations, consultez [appel des fonctions « nom des paramètres régionaux »](calling-the--locale-name--functions.md).</span><span class="sxs-lookup"><span data-stu-id="a8030-108">For more information, see [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="a8030-109">L’utilisation de noms de paramètres régionaux au lieu des identificateurs de paramètres régionaux est toujours préférable.</span><span class="sxs-lookup"><span data-stu-id="a8030-109">Use of locale names instead of locale identifiers is always preferable.</span></span>

 

<span data-ttu-id="a8030-110">L’illustration suivante montre le format des bits dans un identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="a8030-110">The following illustration shows the format of the bits in a locale identifier.</span></span>

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a><span data-ttu-id="a8030-111">Identificateurs de paramètres régionaux prédéfinis</span><span class="sxs-lookup"><span data-stu-id="a8030-111">Predefined Locale Identifiers</span></span>

<span data-ttu-id="a8030-112">Les identificateurs de paramètres régionaux prédéfinis pris en charge par NLS sont définis dans les informations de référence sur l' [API NLS (National Language Support)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span><span class="sxs-lookup"><span data-stu-id="a8030-112">The predefined locale identifiers supported by NLS are defined in the [National Language Support (NLS) API Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span></span>

<span data-ttu-id="a8030-113">NLS utilise les constantes d’informations de paramètres régionaux suivantes pour représenter les identificateurs de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="a8030-113">NLS uses the following locale information constants to represent locale identifiers.</span></span>

-   <span data-ttu-id="a8030-114">[Paramètres \_ régionaux SLANGUAGE](locale-slanguage.md) ou [paramètres régionaux \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a8030-114">[LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span></span>
-   [<span data-ttu-id="a8030-115">paramètres régionaux \_ SNAME</span><span class="sxs-lookup"><span data-stu-id="a8030-115">LOCALE\_SNAME</span></span>](locale-sname.md)
-   [<span data-ttu-id="a8030-116">paramètres régionaux \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="a8030-116">LOCALE\_SSCRIPTS</span></span>](locale-sscripts.md)
-   [<span data-ttu-id="a8030-117">paramètres régionaux \_ IDEFAULTANSICODEPAGE</span><span class="sxs-lookup"><span data-stu-id="a8030-117">LOCALE\_IDEFAULTANSICODEPAGE</span></span>](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a><span data-ttu-id="a8030-118">Identificateurs de paramètres régionaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="a8030-118">Custom Locale Identifiers</span></span>

<span data-ttu-id="a8030-119">**Windows Vista :** NLS prend en charge les identificateurs de paramètres régionaux personnalisés représentés par les constantes d’informations de paramètres régionaux suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8030-119">**Windows Vista:** NLS supports the custom locale identifiers represented by the following locale information constants.</span></span>

-   [<span data-ttu-id="a8030-120">paramètres régionaux \_ personnalisés \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="a8030-120">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="a8030-121">paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_</span><span class="sxs-lookup"><span data-stu-id="a8030-121">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="a8030-122">paramètres régionaux \_ personnalisés \_ non spécifiés</span><span class="sxs-lookup"><span data-stu-id="a8030-122">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

## <a name="building-a-locale"></a><span data-ttu-id="a8030-123">Génération de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="a8030-123">Building a Locale</span></span>

<span data-ttu-id="a8030-124">Vous pouvez utiliser l’utilitaire locale Builder fourni par NLS pour créer des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="a8030-124">You can use the Locale Builder utility provided by NLS to build locales.</span></span> <span data-ttu-id="a8030-125">Pour plus d’informations, consultez [Microsoft locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span><span class="sxs-lookup"><span data-stu-id="a8030-125">For more information, see [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span></span>

<span data-ttu-id="a8030-126">Votre application peut créer un identificateur de paramètres régionaux à l’aide de la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="a8030-126">Your application can construct a locale identifier using the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro.</span></span> <span data-ttu-id="a8030-127">Vous pouvez également utiliser l’un des identificateurs par défaut correspondant aux constantes listées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a8030-127">Alternatively it can use one of the default identifiers corresponding to the constants listed below.</span></span>

-   [<span data-ttu-id="a8030-128">paramètres régionaux \_ INvariants</span><span class="sxs-lookup"><span data-stu-id="a8030-128">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="a8030-129">paramètres régionaux \_ \_ par défaut du système</span><span class="sxs-lookup"><span data-stu-id="a8030-129">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="a8030-130">paramètres régionaux \_ par défaut de l’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="a8030-130">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a><span data-ttu-id="a8030-131">Récupération des identificateurs de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="a8030-131">Retrieval of Locale Identifiers</span></span>

<span data-ttu-id="a8030-132">Une application peut récupérer les identificateurs de paramètres régionaux actuels à l’aide des fonctions [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) et [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) .</span><span class="sxs-lookup"><span data-stu-id="a8030-132">An application can retrieve the current locale identifiers by using the [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) and [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) functions.</span></span> <span data-ttu-id="a8030-133">Chaque thread peut définir et récupérer ses propres paramètres régionaux avec [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) et [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span><span class="sxs-lookup"><span data-stu-id="a8030-133">Each thread can set and retrieve its own locale with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) and [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8030-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8030-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8030-135">Paramètres régionaux et langues</span><span class="sxs-lookup"><span data-stu-id="a8030-135">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="a8030-136">Identificateurs de langue</span><span class="sxs-lookup"><span data-stu-id="a8030-136">Language Identifiers</span></span>](language-identifiers.md)
</dt> <dt>

[<span data-ttu-id="a8030-137">Noms de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="a8030-137">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="a8030-138">Identificateurs d’ordre de tri</span><span class="sxs-lookup"><span data-stu-id="a8030-138">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="a8030-139">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="a8030-139">**MAKELCID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
