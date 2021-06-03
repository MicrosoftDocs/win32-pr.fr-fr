---
description: Les composants internationaux pour Unicode (ICU) sont un ensemble d’API de globalisation Open source largement utilisé et mature.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: ICU (International Components for Unicode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560a2f344a3024685e17df0f434f8ffa040b5c8b
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349988"
---
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="c7626-103">ICU (International Components for Unicode)</span><span class="sxs-lookup"><span data-stu-id="c7626-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="c7626-104">Les composants internationaux pour Unicode (ICU) sont un ensemble d’API de globalisation Open source largement utilisé et mature.</span><span class="sxs-lookup"><span data-stu-id="c7626-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="c7626-105">ICU utilise le vaste référentiel de données de paramètres régionaux (CLDR) d’Unicode comme bibliothèque de données, offrant ainsi une prise en charge de la globalisation pour les applications logicielles.</span><span class="sxs-lookup"><span data-stu-id="c7626-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="c7626-106">ICU est largement portable et donne aux applications les mêmes résultats sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="c7626-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="c7626-107">Principales caractéristiques des services API de globalisation fournis par ICU</span><span class="sxs-lookup"><span data-stu-id="c7626-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="c7626-108">**Conversion de page de codes**: convertissez des données de texte vers ou à partir d’Unicode et presque tout autre jeu de caractères ou encodage.</span><span class="sxs-lookup"><span data-stu-id="c7626-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="c7626-109">Les tables de conversion d’ICU sont basées sur des données de jeu de caractères collectées par IBM au cours de nombreuses décennies et sont les plus complètes disponibles partout.</span><span class="sxs-lookup"><span data-stu-id="c7626-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="c7626-110">**Classement**: Comparez les chaînes en fonction des conventions et des normes d’une langue, d’une région ou d’un pays particulier.</span><span class="sxs-lookup"><span data-stu-id="c7626-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="c7626-111">Le classement de l’ICU est basé sur l’algorithme de classement Unicode et les règles de comparaison spécifiques aux paramètres régionaux de CLDR.</span><span class="sxs-lookup"><span data-stu-id="c7626-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="c7626-112">**Mise en forme**: mettez en forme les nombres, les dates, les heures et les devises selon les conventions des paramètres régionaux choisis.</span><span class="sxs-lookup"><span data-stu-id="c7626-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="c7626-113">Cela comprend la conversion des noms de mois et de jours dans la langue sélectionnée, le choix des abréviations appropriées, le classement correct des champs, etc. Ces données proviennent également du référentiel de données de paramètres régionaux commun.</span><span class="sxs-lookup"><span data-stu-id="c7626-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="c7626-114">**Calculs de temps**: plusieurs types de calendriers sont fournis au-delà du calendrier grégorien traditionnel.</span><span class="sxs-lookup"><span data-stu-id="c7626-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="c7626-115">Un ensemble complet d’API de calcul de fuseau horaire est fourni.</span><span class="sxs-lookup"><span data-stu-id="c7626-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="c7626-116">**Prise en charge d’Unicode**: ICU suit étroitement la norme Unicode, en fournissant un accès facile à toutes les nombreuses propriétés de caractères Unicode, à la normalisation Unicode, au repli de cas et à d’autres opérations fondamentales, comme spécifié par la [norme Unicode](https://www.unicode.org/).</span><span class="sxs-lookup"><span data-stu-id="c7626-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="c7626-117">**Expression régulière**: les expressions régulières d’ICU prennent entièrement en charge Unicode tout en offrant des performances très compétitives.</span><span class="sxs-lookup"><span data-stu-id="c7626-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="c7626-118">**Bidirectionnel**: prise en charge de la gestion du texte contenant un mélange de données de gauche à droite (anglais) et de droite à gauche (arabe ou hébreu).</span><span class="sxs-lookup"><span data-stu-id="c7626-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="c7626-119">Pour plus d’informations, vous pouvez visiter le site Web ICU : <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="c7626-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="c7626-120">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="c7626-120">Overview</span></span>

<span data-ttu-id="c7626-121">Dans Windows 10 Creators Update, ICU a été intégré à Windows, ce qui rendait les API et les données C accessibles publiquement.</span><span class="sxs-lookup"><span data-stu-id="c7626-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7626-122">La version d’ICU dans Windows expose uniquement les API C.</span><span class="sxs-lookup"><span data-stu-id="c7626-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="c7626-123">Elle n’expose pas les API C++.</span><span class="sxs-lookup"><span data-stu-id="c7626-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="c7626-124">Malheureusement, il est impossible d’exposer les API C++ en raison de l’absence d’un ABI stable en C++.</span><span class="sxs-lookup"><span data-stu-id="c7626-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="c7626-125">Pour obtenir de la documentation sur les API de la bibliothèque ICU C, consultez la page de documentation ICU officielle ici : <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="c7626-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="c7626-126">Historique des modifications apportées à la bibliothèque ICU dans Windows</span><span class="sxs-lookup"><span data-stu-id="c7626-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="c7626-127">Version 1703 (Creators Update)</span><span class="sxs-lookup"><span data-stu-id="c7626-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="c7626-128">La bibliothèque ICU a été ajoutée pour la première fois au système d’exploitation Windows 10 dans cette version.</span><span class="sxs-lookup"><span data-stu-id="c7626-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="c7626-129">Elle a été ajoutée en tant que :</span><span class="sxs-lookup"><span data-stu-id="c7626-129">It was added as:</span></span>
- <span data-ttu-id="c7626-130">Deux DLL système :</span><span class="sxs-lookup"><span data-stu-id="c7626-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="c7626-131">**icuuc.dll** (il s’agit de la bibliothèque « commune » ICU)</span><span class="sxs-lookup"><span data-stu-id="c7626-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="c7626-132">**icuin.dll** (il s’agit de la bibliothèque ICU « i18n »)</span><span class="sxs-lookup"><span data-stu-id="c7626-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="c7626-133">Deux fichiers d’en-tête dans le kit de développement logiciel Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="c7626-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="c7626-134">**icucommon. h**</span><span class="sxs-lookup"><span data-stu-id="c7626-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="c7626-135">**icui18n. h**</span><span class="sxs-lookup"><span data-stu-id="c7626-135">**icui18n.h**</span></span>
- <span data-ttu-id="c7626-136">Deux bibliothèques d’importation dans le kit de développement logiciel (SDK) Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="c7626-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="c7626-137">**icuuc. lib**</span><span class="sxs-lookup"><span data-stu-id="c7626-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="c7626-138">**icuin. lib**</span><span class="sxs-lookup"><span data-stu-id="c7626-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="c7626-139">Version 1709 (mise à jour des créateurs de automne)</span><span class="sxs-lookup"><span data-stu-id="c7626-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="c7626-140">Un fichier d’en-tête combiné, **ICU. h**, a été ajouté, qui contient le contenu des deux fichiers d’en-tête ci-dessus (icucommon. h et icui18n. h), et modifie également le type de `UCHAR` en `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="c7626-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="c7626-141">Version 1903 (mai 2019 mise à jour)</span><span class="sxs-lookup"><span data-stu-id="c7626-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="c7626-142">Une nouvelle DLL combinée, **icu.dll**, a été ajoutée, qui contient les bibliothèques « communes » et « i18n ».</span><span class="sxs-lookup"><span data-stu-id="c7626-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="c7626-143">En outre, une nouvelle bibliothèque d’importation a été ajoutée au kit de développement logiciel (SDK) Windows 10 : **ICU. lib**.</span><span class="sxs-lookup"><span data-stu-id="c7626-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="c7626-144">À l’avenir, aucune nouvelle API ne sera ajoutée aux anciens en-têtes (icucommon. h et icui18n. h) ou aux anciennes bibliothèques d’importation (icuuc. lib et icuin. lib).</span><span class="sxs-lookup"><span data-stu-id="c7626-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="c7626-145">Les nouvelles API sont ajoutées uniquement à l’en-tête combiné (ICU. h) et à la bibliothèque d’importation combinée (ICU. lib).</span><span class="sxs-lookup"><span data-stu-id="c7626-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="c7626-146">Mise en route</span><span class="sxs-lookup"><span data-stu-id="c7626-146">Getting Started</span></span>

<span data-ttu-id="c7626-147">Il existe trois étapes principales à suivre : (Windows 10 Creators Update ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="c7626-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="c7626-148">Votre application doit cibler Windows 10 version 1703 (Creators Update) ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c7626-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="c7626-149">Ajoutez les en-têtes :</span><span class="sxs-lookup"><span data-stu-id="c7626-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="c7626-150">Sur Windows 10 version 1709 et versions ultérieures, vous devez inclure l’en-tête combiné à la place :</span><span class="sxs-lookup"><span data-stu-id="c7626-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="c7626-151">Lien vers les deux bibliothèques :</span><span class="sxs-lookup"><span data-stu-id="c7626-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="c7626-152">icuuc. lib</span><span class="sxs-lookup"><span data-stu-id="c7626-152">icuuc.lib</span></span>
   -   <span data-ttu-id="c7626-153">icuin. lib</span><span class="sxs-lookup"><span data-stu-id="c7626-153">icuin.lib</span></span>

   <span data-ttu-id="c7626-154">Sur Windows 10 version 1903 et versions ultérieures, vous devez utiliser la bibliothèque combinée à la place :</span><span class="sxs-lookup"><span data-stu-id="c7626-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="c7626-155">ICU. lib</span><span class="sxs-lookup"><span data-stu-id="c7626-155">icu.lib</span></span>

</dl>

<span data-ttu-id="c7626-156">Ensuite, vous pouvez appeler l’API ICU C à partir de ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="c7626-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="c7626-157">(Aucune API C++ n’est exposée.)</span><span class="sxs-lookup"><span data-stu-id="c7626-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7626-158">Si vous utilisez les bibliothèques d’importation héritées, icuuc. lib et icuin. lib, assurez-vous qu’elles sont répertoriées avant les bibliothèques de parapluie, telles que onecoreuap. lib ou WindowsApp. lib, dans le paramètre de l’éditeur de liens dépendances supplémentaires (Voir l’image ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="c7626-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="c7626-159">Dans le cas contraire, l’éditeur de liens sera lié à ICU. lib, ce qui entraînera une tentative de chargement de icu.dll au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c7626-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="c7626-160">Cette DLL est présente uniquement depuis la version 1903.</span><span class="sxs-lookup"><span data-stu-id="c7626-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="c7626-161">Par conséquent, si un utilisateur met à niveau le kit de développement logiciel (SDK) Windows 10 sur un ordinateur Windows antérieur à la version 1903, l’application ne peut pas se charger et s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="c7626-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="c7626-162">Pour obtenir un historique des bibliothèques ICU dans Windows, consultez [historique des modifications apportées à la bibliothèque ICU dans Windows](#history-of-changes-to-the-icu-library-in-windows).</span><span class="sxs-lookup"><span data-stu-id="c7626-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![exemple ICU](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="c7626-164">Il s’agit de la configuration pour « toutes les plateformes ».</span><span class="sxs-lookup"><span data-stu-id="c7626-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="c7626-165">Pour que les applications Win32 utilisent ICU, elles doivent d’abord appeler [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="c7626-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span> <span data-ttu-id="c7626-166">Sur Windows 10 version 1903 et versions ultérieures, où la bibliothèque ICU combinée (icu.dll/ICU.lib) est disponible, vous pouvez omettre l’appel de CoInitializeEx à l’aide de la bibliothèque combinée.</span><span class="sxs-lookup"><span data-stu-id="c7626-166">On Windows 10 version 1903 and above, where the combined ICU library (icu.dll/icu.lib) is available, you can omit the CoInitializeEx call by using the combined library.</span></span>
> - <span data-ttu-id="c7626-167">Toutes les données retournées par les API ICU ne sont pas alignées sur le système d’exploitation Windows, car ce travail d’alignement est toujours en cours.</span><span class="sxs-lookup"><span data-stu-id="c7626-167">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="c7626-168">Exemple d’application ICU</span><span class="sxs-lookup"><span data-stu-id="c7626-168">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="c7626-169">Exemple d’extrait de code</span><span class="sxs-lookup"><span data-stu-id="c7626-169">Example code snippet</span></span>

<span data-ttu-id="c7626-170">Voici un exemple illustrant l’utilisation d’API ICU à partir d’une application UWP C++.</span><span class="sxs-lookup"><span data-stu-id="c7626-170">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="c7626-171">(Il n’est pas destiné à être une application autonome complète, mais il s’agit simplement d’un exemple d’appel d’une méthode ICU.)</span><span class="sxs-lookup"><span data-stu-id="c7626-171">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="c7626-172">Le petit exemple suivant suppose qu’il existe des méthodes **ErrorMessage** et **OutputMessage** qui génèrent les chaînes à l’utilisateur d’une certaine manière.</span><span class="sxs-lookup"><span data-stu-id="c7626-172">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



