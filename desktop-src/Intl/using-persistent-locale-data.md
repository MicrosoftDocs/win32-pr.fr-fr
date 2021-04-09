---
description: Utilisation des données de paramètres régionaux persistants
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Utilisation des données de paramètres régionaux persistants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869077"
---
# <a name="using-persistent-locale-data"></a><span data-ttu-id="9cb1a-103">Utilisation des données de paramètres régionaux persistants</span><span class="sxs-lookup"><span data-stu-id="9cb1a-103">Using Persistent Locale Data</span></span>

<span data-ttu-id="9cb1a-104">Une application globalisée conserve ou transmet souvent des données, par exemple une heure et une date.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-104">A globalized application often persists or transmits data, for example, time and date.</span></span> <span data-ttu-id="9cb1a-105">Lorsque vous décidez de la manière dont votre application doit gérer la persistance des données, n’oubliez pas que les données ne sont pas nécessairement identiques d’un ordinateur à l’autre ou entre des exécutions de l’application.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-105">When deciding how your application should handle data persistence, remember that data is not guaranteed to be the same from computer to computer or between runs of the application.</span></span> <span data-ttu-id="9cb1a-106">Cela est vrai pour les deux [paramètres régionaux](locales-and-languages.md) fournis avec Windows et les [paramètres régionaux personnalisés](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="9cb1a-106">This is true for both [locales](locales-and-languages.md) that ship with Windows and [custom locales](custom-locales.md).</span></span>

<span data-ttu-id="9cb1a-107">La conception de l’application doit prendre en compte une variété de modifications de données relatives aux paramètres régionaux qui peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-107">Design of the application must take into account a variety of locale-related data changes that can occur.</span></span> <span data-ttu-id="9cb1a-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9cb1a-108">For example:</span></span>

-   <span data-ttu-id="9cb1a-109">Les symboles monétaires peuvent changer à mesure que les pays adoptent l’euro.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-109">Currency symbols can change as countries adopt the Euro.</span></span>
-   <span data-ttu-id="9cb1a-110">Les préférences régionales peuvent changer.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-110">Regional preferences can change.</span></span> <span data-ttu-id="9cb1a-111">Par exemple, le format d/m/y peut passer au format m/d/y pour des paramètres régionaux particuliers.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-111">For example, the format d/m/y might change to the format m/d/y for a particular locale.</span></span>
-   <span data-ttu-id="9cb1a-112">L’orthographe des noms de jours peut changer en raison des réformes orthographiques.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-112">The spelling of day names can change due to spelling reforms.</span></span> <span data-ttu-id="9cb1a-113">En outre, la casse peut changer pour les noms de mois ou de jours.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-113">Additionally, casing can change for month or day names.</span></span>

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a><span data-ttu-id="9cb1a-114">Utiliser des formats de Locale-Independent pour le stockage et l’échange de données</span><span class="sxs-lookup"><span data-stu-id="9cb1a-114">Use Locale-Independent Formats for Storage and Data Interchange</span></span>

<span data-ttu-id="9cb1a-115">Une application qui rend les données persistantes doit utiliser des formats indépendants des paramètres régionaux pour le stockage et l’échange de données.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-115">An application that persists data should use locale-independent formats for storage and data interchange.</span></span> <span data-ttu-id="9cb1a-116">Les formats codés en dur ou standard sont des exemples. le [nom des paramètres régionaux des paramètres \_ \_ ](locale-name-constants.md)régionaux invariants et les formats de stockage binaires.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-116">Examples are hard-coded or standard formats; the invariant locale [LOCALE\_NAME\_INVARIANT](locale-name-constants.md); and binary storage formats.</span></span>

<span data-ttu-id="9cb1a-117">Si des données de tri persistantes sont requises, l’application doit utiliser la fonction [**comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .</span><span class="sxs-lookup"><span data-stu-id="9cb1a-117">If persistent sorting data is required, the application must use the [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) function.</span></span> <span data-ttu-id="9cb1a-118">N’oubliez pas qu’un format indifférent ne reste pas invariant pour le [Tri](sorting.md), uniquement pour les paramètres régionaux et les données de calendrier.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-118">Remember that an invariant format does not remain invariant for [sorting](sorting.md), only for locale and calendar data.</span></span>

## <a name="use-the-user-default-locale-for-data-presentation"></a><span data-ttu-id="9cb1a-119">Utiliser les paramètres régionaux par défaut de l’utilisateur pour la présentation des données</span><span class="sxs-lookup"><span data-stu-id="9cb1a-119">Use the User Default Locale for Data Presentation</span></span>

<span data-ttu-id="9cb1a-120">Pour présenter des données persistantes, il est préférable pour l’application de reformater les données à l’aide des paramètres régionaux par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-120">To present persistent data, it is best for the application to reformat the data using the user default locale.</span></span> <span data-ttu-id="9cb1a-121">L’utilisation de ces paramètres régionaux autorise les remplacements de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-121">Use of this locale allows user overrides.</span></span> <span data-ttu-id="9cb1a-122">Pour plus d’informations, consultez [paramètres \_ régionaux \_ par défaut](locale-user-default.md)de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9cb1a-122">For more information, see [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cb1a-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cb1a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cb1a-124">Utilisation de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="9cb1a-124">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="9cb1a-125">Paramètres régionaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="9cb1a-125">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="9cb1a-126">Tri</span><span class="sxs-lookup"><span data-stu-id="9cb1a-126">Sorting</span></span>](sorting.md)
</dt> </dl>

 

 



