---
description: Le terme &\# 0034 ; language&\# 0034 ; indique une collection de propriétés utilisées dans des communications orales et écrites.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Paramètres régionaux et langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524930"
---
# <a name="locales-and-languages"></a><span data-ttu-id="161f6-103">Paramètres régionaux et langues</span><span class="sxs-lookup"><span data-stu-id="161f6-103">Locales and Languages</span></span>

<span data-ttu-id="161f6-104">Le terme « langue » indique une collection de propriétés utilisées dans des communications orales et écrites.</span><span class="sxs-lookup"><span data-stu-id="161f6-104">The term "language" indicates a collection of properties used in spoken and written communication.</span></span> <span data-ttu-id="161f6-105">Chaque langue a un nom de langue et un identificateur de langue qui indiquent la [page de codes](code-pages.md) particulière (ANSI, dos, Macintosh) utilisée pour représenter l' [emplacement géographique](table-of-geographical-locations.md) de la langue sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="161f6-105">Each language has a language name and a language identifier that indicate the particular [code page](code-pages.md) (ANSI, DOS, Macintosh) used to represent the [geographical location](table-of-geographical-locations.md) for the language on the operating system.</span></span> <span data-ttu-id="161f6-106">Une langue neutre est indiquée par un nom tel que « en » pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="161f6-106">A neutral language is indicated by a name such as "en" for English.</span></span> <span data-ttu-id="161f6-107">Une langue plus spécifique à chaque graphique peut être indiquée par un nom qui comprend des informations sur les paramètres régionaux et les pays/région.</span><span class="sxs-lookup"><span data-stu-id="161f6-107">A more geographically specific language can be indicated by a name that includes both locale and country/region information.</span></span> <span data-ttu-id="161f6-108">Par exemple, les paramètres régionaux anglais (États-Unis) ont le nom de langue « en-US ».</span><span class="sxs-lookup"><span data-stu-id="161f6-108">For example, the locale English (United States) has the language name "en-US".</span></span>

<span data-ttu-id="161f6-109">Les paramètres régionaux sont une collection d’informations de préférences d’utilisateur liées à la langue, représentées sous la forme d’une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="161f6-109">A "locale" is a collection of language-related user preference information represented as a list of values.</span></span> <span data-ttu-id="161f6-110">Windows XP prend en charge plus de 150 de paramètres régionaux et Windows Vista prend en charge environ 200.</span><span class="sxs-lookup"><span data-stu-id="161f6-110">Windows XP supports more than 150 locales, and Windows Vista supports about 200.</span></span> <span data-ttu-id="161f6-111">Chaque paramètre régional est défini par une langue et un ordre de tri, et a à la fois un nom de paramètres régionaux et un identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="161f6-111">Each locale is defined by a language and a sort order, and has both a locale name and a locale identifier.</span></span> <span data-ttu-id="161f6-112">Un exemple de nom de paramètres régionaux pour l’allemand (Allemagne) est « de-DE- \_ Phonebook ».</span><span class="sxs-lookup"><span data-stu-id="161f6-112">An example of a locale name for German (Germany) is "de-DE\_phonebook".</span></span>

<span data-ttu-id="161f6-113">Chaque système d’exploitation a au moins un paramètre régional installé et a souvent plusieurs paramètres régionaux à partir desquels l’utilisateur peut les sélectionner.</span><span class="sxs-lookup"><span data-stu-id="161f6-113">Each operating system has at least one installed locale and often has many locales from which the user can select.</span></span> <span data-ttu-id="161f6-114">Chaque paramètre régional a une variété d’informations qui lui sont associées, à l’exception de son nom et de son identificateur.</span><span class="sxs-lookup"><span data-stu-id="161f6-114">Each locale has a variety of information associated with it, other than its name and identifier.</span></span> <span data-ttu-id="161f6-115">Les types d’informations de paramètres régionaux sont décrits dans [constantes d’informations de paramètres régionaux](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="161f6-115">Locale information types are described in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="161f6-116">Le système d’exploitation attribue des paramètres régionaux à chaque thread, en affectant initialement les « paramètres régionaux par défaut du système » définis par la [ \_ \_ valeur par défaut du système de paramètres régionaux](locale-system-default.md).</span><span class="sxs-lookup"><span data-stu-id="161f6-116">The operating system assigns a locale to each thread, initially assigning the "system default locale," defined by [LOCALE\_SYSTEM\_DEFAULT](locale-system-default.md).</span></span> <span data-ttu-id="161f6-117">Ces paramètres régionaux sont définis lors de l’installation du système d’exploitation ou lorsque l’utilisateur le sélectionne à l’aide de la section Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="161f6-117">This locale is set when the operating system is installed or when the user selects it using the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="161f6-118">Lors de l’exécution d’un thread dans un processus appartenant à l’utilisateur, le système d’exploitation affecte les « paramètres régionaux par défaut de l’utilisateur » au thread.</span><span class="sxs-lookup"><span data-stu-id="161f6-118">When running a thread in a process belonging to the user, the operating system assigns the "user default locale" to the thread.</span></span> <span data-ttu-id="161f6-119">Ces paramètres régionaux sont définis par les paramètres [régionaux \_ \_ par défaut](locale-user-default.md)de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="161f6-119">This locale is defined by [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="161f6-120">Une application peut remplacer l’option par défaut à l’aide de la fonction [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) pour définir explicitement les paramètres régionaux d’un thread.</span><span class="sxs-lookup"><span data-stu-id="161f6-120">An application can override either default by using the [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) function to explicitly set the locale for a thread.</span></span>

<span data-ttu-id="161f6-121">L’implémentation d’un langage requiert des paramètres régionaux correspondants.</span><span class="sxs-lookup"><span data-stu-id="161f6-121">Implementation of a language requires a corresponding locale.</span></span> <span data-ttu-id="161f6-122">Le système d’exploitation implémente une langue neutre en sélectionnant les données pour les paramètres régionaux associés à une version spécifique de la langue, généralement les paramètres régionaux les plus répandus.</span><span class="sxs-lookup"><span data-stu-id="161f6-122">The operating system implements a neutral language by selecting the data for the locale associated with a specific version of the language, usually the most widespread locale.</span></span>

<span data-ttu-id="161f6-123">À compter de Windows Vista, il est possible qu’une langue particulière corresponde à des paramètres régionaux supplémentaires, qui est un type de paramètres régionaux personnalisés.</span><span class="sxs-lookup"><span data-stu-id="161f6-123">Starting with Windows Vista, it is possible for a particular language to correspond to a supplemental locale, which is a type of custom locale.</span></span> <span data-ttu-id="161f6-124">Étant donné que les paramètres régionaux supplémentaires partagent tous un identificateur de paramètres régionaux unique, vos applications doivent gérer ces paramètres régionaux et les langues correspondantes par leur nom plutôt que par leur identificateur.</span><span class="sxs-lookup"><span data-stu-id="161f6-124">Since supplemental locales all share a single locale identifier, your applications should handle these locales and the corresponding languages by name instead of by identifier.</span></span>

<span data-ttu-id="161f6-125">Les concepts de langage sont étroitement liés aux concepts des paramètres régionaux, mais les deux termes ne sont pas interchangeables.</span><span class="sxs-lookup"><span data-stu-id="161f6-125">Language concepts are closely related to locale concepts, but the two terms are not interchangeable.</span></span> <span data-ttu-id="161f6-126">En règle générale, les fonctions liées à l' [interface utilisateur multilingue](multilingual-user-interface.md) concernent les langues, tandis que les fonctions nls agissent sur les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="161f6-126">As a general rule, functions related to the [Multilingual User Interface](multilingual-user-interface.md) deal with languages, while the NLS functions act upon locales.</span></span>

<span data-ttu-id="161f6-127">Les rubriques traitées dans cette section sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="161f6-127">The following topics are covered in this section:</span></span>

-   [<span data-ttu-id="161f6-128">Paramètres régionaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="161f6-128">Custom Locales</span></span>](custom-locales.md)
-   [<span data-ttu-id="161f6-129">Identificateurs de langue</span><span class="sxs-lookup"><span data-stu-id="161f6-129">Language Identifiers</span></span>](language-identifiers.md)
-   [<span data-ttu-id="161f6-130">Noms des langues</span><span class="sxs-lookup"><span data-stu-id="161f6-130">Language Names</span></span>](language-names.md)
-   [<span data-ttu-id="161f6-131">Identificateurs de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="161f6-131">Locale Identifiers</span></span>](locale-identifiers.md)
-   [<span data-ttu-id="161f6-132">Noms de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="161f6-132">Locale Names</span></span>](locale-names.md)
-   [<span data-ttu-id="161f6-133">Pseudo-paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="161f6-133">Pseudo-Locales</span></span>](pseudo-locales.md)

## <a name="related-topics"></a><span data-ttu-id="161f6-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="161f6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="161f6-135">À propos de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="161f6-135">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="161f6-136">Pages de codes</span><span class="sxs-lookup"><span data-stu-id="161f6-136">Code Pages</span></span>](code-pages.md)
</dt> <dt>

[<span data-ttu-id="161f6-137">Constantes d’informations de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="161f6-137">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="161f6-138">Interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="161f6-138">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="161f6-139">Tableau des zones géographiques</span><span class="sxs-lookup"><span data-stu-id="161f6-139">Table of Geographical Locations</span></span>](table-of-geographical-locations.md)
</dt> <dt>

[<span data-ttu-id="161f6-140">Gestion de la langue de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="161f6-140">User Interface Language Management</span></span>](user-interface-language-management.md)
</dt> <dt>

[<span data-ttu-id="161f6-141">**SetThreadLocale**</span><span class="sxs-lookup"><span data-stu-id="161f6-141">**SetThreadLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



