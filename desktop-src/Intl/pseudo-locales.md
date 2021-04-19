---
description: 'Windows Vista et versions ultérieures : NLS définit plusieurs Pseudo-paramètres régionaux à utiliser en plus des paramètres régionaux Windows existants.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514420"
---
# <a name="pseudo-locales"></a><span data-ttu-id="45462-103">Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="45462-103">Pseudo-Locales</span></span>

<span data-ttu-id="45462-104">**Windows Vista et versions ultérieures :** NLS définit plusieurs Pseudo-paramètres régionaux à utiliser en plus des paramètres régionaux Windows existants.</span><span class="sxs-lookup"><span data-stu-id="45462-104">**Windows Vista and later:** NLS defines several pseudo-locales for use in addition to the existing Windows locales.</span></span> <span data-ttu-id="45462-105">Utilisez ces pseudo-paramètres régionaux pour tester la localisation de vos applications.</span><span class="sxs-lookup"><span data-stu-id="45462-105">Use these pseudo-locales for testing the localization of your applications.</span></span> <span data-ttu-id="45462-106">Pour plus d’informations sur l’implémentation, consultez [utilisation de Pseudo-Locales pour le test de localisation](using-pseudo-locales-for-localization-testing.md).</span><span class="sxs-lookup"><span data-stu-id="45462-106">For implementation details, see [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).</span></span>

## <a name="supported-pseudo-locales"></a><span data-ttu-id="45462-107">Pseudo-Locales pris en charge</span><span class="sxs-lookup"><span data-stu-id="45462-107">Supported Pseudo-Locales</span></span>

<span data-ttu-id="45462-108">Les pseudo-paramètres régionaux pris en charge par NLS sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="45462-108">The pseudo-locales supported by NLS are:</span></span>

-   <span data-ttu-id="45462-109">Pseudo-paramètres régionaux de base</span><span class="sxs-lookup"><span data-stu-id="45462-109">Base pseudo-locale</span></span>
-   <span data-ttu-id="45462-110">Pseudo-paramètres régionaux mis en miroir (de droite à gauche)</span><span class="sxs-lookup"><span data-stu-id="45462-110">Mirrored (right-to-left) pseudo-locale</span></span>
-   <span data-ttu-id="45462-111">Pseudo-paramètres régionaux de langue orientale</span><span class="sxs-lookup"><span data-stu-id="45462-111">East Asian-language pseudo-locale</span></span>

<span data-ttu-id="45462-112">Choisissez les pseudo-paramètres régionaux particuliers à utiliser en fonction de leurs affectations de pages de codes et des chaînes de localisation, par exemple, les noms de mois et les noms de jours.</span><span class="sxs-lookup"><span data-stu-id="45462-112">Choose the particular pseudo-locale to use based on its code page assignments and the strings for localization, for example, month names, day names.</span></span> <span data-ttu-id="45462-113">Les données pour chaque Pseudo-paramètres régionaux incluent non seulement les pages de code pertinentes et les chaînes de jour et de mois pour la localisation, mais également des données pour plusieurs autres cas de test pour NLS.</span><span class="sxs-lookup"><span data-stu-id="45462-113">Data for each pseudo-locale includes not only relevant code pages and day and month strings for localization, but also data for several other test cases for NLS.</span></span> <span data-ttu-id="45462-114">Les cas de test examinent les types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="45462-114">The test cases examine the following types of data:</span></span>

-   <span data-ttu-id="45462-115">[identificateurs de paramètres régionaux](locale-identifiers.md)9 bits.</span><span class="sxs-lookup"><span data-stu-id="45462-115">9-bit [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="45462-116">Les pseudo-paramètres régionaux offrent une bonne opportunité de tester le fonctionnement des identificateurs de paramètres régionaux 9 bits.</span><span class="sxs-lookup"><span data-stu-id="45462-116">Pseudo-locales provide a good opportunity to test the operation of 9-bit locale identifiers.</span></span>
-   <span data-ttu-id="45462-117">Chaînes de langues qui doivent utiliser de petites polices.</span><span class="sxs-lookup"><span data-stu-id="45462-117">Strings from languages that must use small fonts.</span></span> <span data-ttu-id="45462-118">En raison des limitations de l’interface GDI (Graphics Device Interface), la police de l’interface utilisateur pour certaines langues est plus petite que optimale.</span><span class="sxs-lookup"><span data-stu-id="45462-118">Because of limitations in the graphics device interface (GDI), the user interface font for some languages is smaller than optimal.</span></span> <span data-ttu-id="45462-119">Les pseudo-paramètres régionaux incluent plusieurs chaînes de ces langages, combinées avec des chaînes de langages avec une gestion des polices plus standard.</span><span class="sxs-lookup"><span data-stu-id="45462-119">Pseudo-locales include several strings from these languages, combined with strings from languages with more standard font handling.</span></span> <span data-ttu-id="45462-120">Vous pouvez utiliser ces chaînes dans le test pour déterminer comment une police limitée par GDI est restituée.</span><span class="sxs-lookup"><span data-stu-id="45462-120">You can use these strings in testing to determine how a GDI-limited font renders.</span></span>
-   <span data-ttu-id="45462-121">Longueurs de chaîne inhabituelles.</span><span class="sxs-lookup"><span data-stu-id="45462-121">Unusual string lengths.</span></span> <span data-ttu-id="45462-122">Certaines constantes d’informations de paramètres régionaux, par exemple, les [paramètres régionaux \_ slist](locale-slist.md) et les [paramètres régionaux \_ ICURRENCY](locale-icurrency.md), ont des limites conventionnelles sur la taille de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="45462-122">Some locale information constants, for example, [LOCALE\_SLIST](locale-slist.md) and [LOCALE\_ICURRENCY](locale-icurrency.md), have conventional limits on string size.</span></span> <span data-ttu-id="45462-123">Les pseudo-paramètres régionaux prennent en charge l’examen des longueurs de chaîne variables.</span><span class="sxs-lookup"><span data-stu-id="45462-123">The pseudo-locales support the examination of varied string lengths.</span></span>
-   <span data-ttu-id="45462-124">Autres tris.</span><span class="sxs-lookup"><span data-stu-id="45462-124">Alternate sorts.</span></span> <span data-ttu-id="45462-125">Les pseudo-paramètres régionaux peuvent être utilisés pour tester les fonctionnalités de tri de remplacement lorsque l' [identificateur d’ordre de tri](sort-order-identifiers.md) de remplacement diffère de l’identificateur d’ordre de tri de base qui est généralement associé aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="45462-125">Pseudo-locales can be used to test alternate sort functionality when the alternate [sort order identifier](sort-order-identifiers.md) differs from the base sort order identifier that is usually associated with the locale.</span></span>

## <a name="pseudo-locale-names-and-identifiers"></a><span data-ttu-id="45462-126">Noms et identificateurs de Pseudo-paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="45462-126">Pseudo-locale Names and Identifiers</span></span>

<span data-ttu-id="45462-127">Les pseudo-paramètres régionaux ont des [noms de paramètres régionaux](locale-names.md) qui sont choisis à partir de l’espace d’utilisation privé pour éviter tout conflit avec les chaînes possibles introduites dans les normes Organisation internationale de normalisation (iso) 639 et ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="45462-127">The pseudo-locales have [locale names](locale-names.md) that are chosen from the private use space to avoid conflict with possible strings introduced into the International Organization for Standardization (ISO) 639 and ISO 3166 standards.</span></span> <span data-ttu-id="45462-128">Chaque Pseudo-paramètres régionaux a également son propre identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="45462-128">Each pseudo-locale also has its own locale identifier.</span></span> <span data-ttu-id="45462-129">Le tableau suivant fournit les noms et les identificateurs pour les pseudo-paramètres régionaux définis.</span><span class="sxs-lookup"><span data-stu-id="45462-129">The following table provides the names and identifiers for the defined pseudo-locales.</span></span>



| <span data-ttu-id="45462-130">Pseudo-paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="45462-130">Pseudo-locale</span></span>       | <span data-ttu-id="45462-131">Nom des paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="45462-131">Locale name</span></span> | <span data-ttu-id="45462-132">Identificateur de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="45462-132">Locale identifier</span></span> |
|---------------------|-------------|-------------------|
| <span data-ttu-id="45462-133">Base</span><span class="sxs-lookup"><span data-stu-id="45462-133">Base</span></span>                | <span data-ttu-id="45462-134">RPS-Ploc</span><span class="sxs-lookup"><span data-stu-id="45462-134">qps-ploc</span></span>    | <span data-ttu-id="45462-135">0501</span><span class="sxs-lookup"><span data-stu-id="45462-135">0501</span></span>              |
| <span data-ttu-id="45462-136">En miroir</span><span class="sxs-lookup"><span data-stu-id="45462-136">Mirrored</span></span>            | <span data-ttu-id="45462-137">RPS-plocm</span><span class="sxs-lookup"><span data-stu-id="45462-137">qps-plocm</span></span>   | <span data-ttu-id="45462-138">09ff</span><span class="sxs-lookup"><span data-stu-id="45462-138">09ff</span></span>              |
| <span data-ttu-id="45462-139">Asie de l’est-langue</span><span class="sxs-lookup"><span data-stu-id="45462-139">East Asian-language</span></span> | <span data-ttu-id="45462-140">RPS-Ploca</span><span class="sxs-lookup"><span data-stu-id="45462-140">qps-ploca</span></span>   | <span data-ttu-id="45462-141">05fe</span><span class="sxs-lookup"><span data-stu-id="45462-141">05fe</span></span>              |



 

## <a name="example"></a><span data-ttu-id="45462-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="45462-142">Example</span></span>

<span data-ttu-id="45462-143">L’exemple suivant affiche le texte affiché pour les pseudo-paramètres régionaux de base :</span><span class="sxs-lookup"><span data-stu-id="45462-143">The following example shows text displayed for a base pseudo-locale:</span></span>

<span data-ttu-id="45462-144">\[Шěđлеśđαỳ !!! \] , 8 ōf \[ Μäŕςћ !! \] ōf 2006</span><span class="sxs-lookup"><span data-stu-id="45462-144">\[Шěđлеśđαỳ !!!\], 8 ōf \[Μäŕςћ !!\] ōf 2006</span></span>

## <a name="related-topics"></a><span data-ttu-id="45462-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45462-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45462-146">Paramètres régionaux et langues</span><span class="sxs-lookup"><span data-stu-id="45462-146">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="45462-147">Identificateurs de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="45462-147">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="45462-148">Noms de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="45462-148">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="45462-149">Identificateurs d’ordre de tri</span><span class="sxs-lookup"><span data-stu-id="45462-149">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="45462-150">Utilisation de Pseudo-Locales pour le test de la localisation</span><span class="sxs-lookup"><span data-stu-id="45462-150">Using Pseudo-Locales for Localization Testing</span></span>](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



