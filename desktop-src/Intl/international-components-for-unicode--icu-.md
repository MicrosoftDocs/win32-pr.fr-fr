---
description: Les composants internationaux pour Unicode (ICU) sont un ensemble d’API de globalisation Open source largement utilisé et mature.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: ICU (International Components for Unicode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00a72885b37efebf8de0d5eb60a22fe01dfba4f
ms.sourcegitcommit: 176ef0a00690f849282cb48464c97f6526a82113
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2021
ms.locfileid: "103953267"
---
# <a name="international-components-for-unicode-icu"></a>ICU (International Components for Unicode)

Les composants internationaux pour Unicode (ICU) sont un ensemble d’API de globalisation Open source largement utilisé et mature. ICU utilise le vaste référentiel de données de paramètres régionaux (CLDR) d’Unicode comme bibliothèque de données, offrant ainsi une prise en charge de la globalisation pour les applications logicielles. ICU est largement portable et donne aux applications les mêmes résultats sur toutes les plateformes.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Principales caractéristiques des services API de globalisation fournis par ICU

-   **Conversion de page de codes**: convertissez des données de texte vers ou à partir d’Unicode et presque tout autre jeu de caractères ou encodage. Les tables de conversion d’ICU sont basées sur des données de jeu de caractères collectées par IBM au cours de nombreuses décennies et sont les plus complètes disponibles partout.
-   **Classement**: Comparez les chaînes en fonction des conventions et des normes d’une langue, d’une région ou d’un pays particulier. Le classement de l’ICU est basé sur l’algorithme de classement Unicode et les règles de comparaison spécifiques aux paramètres régionaux de CLDR.
-   **Mise en forme**: mettez en forme les nombres, les dates, les heures et les devises selon les conventions des paramètres régionaux choisis. Cela comprend la conversion des noms de mois et de jours dans la langue sélectionnée, le choix des abréviations appropriées, le classement correct des champs, etc. Ces données proviennent également du référentiel de données de paramètres régionaux commun.
-   **Calculs de temps**: plusieurs types de calendriers sont fournis au-delà du calendrier grégorien traditionnel. Un ensemble complet d’API de calcul de fuseau horaire est fourni.
-   **Prise en charge d’Unicode**: ICU suit étroitement la norme Unicode, en fournissant un accès facile à toutes les nombreuses propriétés de caractères Unicode, à la normalisation Unicode, au repli de cas et à d’autres opérations fondamentales, comme spécifié par la [norme Unicode](https://www.unicode.org/).
-   **Expression régulière**: les expressions régulières d’ICU prennent entièrement en charge Unicode tout en offrant des performances très compétitives.
-   **Bidirectionnel**: prise en charge de la gestion du texte contenant un mélange de données de gauche à droite (anglais) et de droite à gauche (arabe ou hébreu).

Pour plus d’informations, vous pouvez visiter le site Web ICU : <http://site.icu-project.org/>

## <a name="overview"></a>Vue d’ensemble

Dans Windows 10 Creators Update, ICU a été intégré à Windows, ce qui rendait les API et les données C accessibles publiquement.

> [!IMPORTANT]
> La version d’ICU dans Windows expose uniquement les API C. Elle n’expose pas les API C++. Malheureusement, il est impossible d’exposer les API C++ en raison de l’absence d’un ABI stable en C++.

Pour obtenir de la documentation sur les API de la bibliothèque ICU C, consultez la page de documentation ICU officielle ici : <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Historique des modifications apportées à la bibliothèque ICU dans Windows

### <a name="version-1703-creators-update"></a>Version 1703 (Creators Update)
La bibliothèque ICU a été ajoutée pour la première fois au système d’exploitation Windows 10 dans cette version.
Elle a été ajoutée en tant que :
- Deux DLL système :
    -   **icuuc.dll** (il s’agit de la bibliothèque « commune » ICU)
    -   **icuin.dll** (il s’agit de la bibliothèque ICU « i18n »)
- Deux fichiers d’en-tête dans le kit de développement logiciel Windows 10 :
    -   **icucommon. h**
    -   **icui18n. h**
- Deux bibliothèques d’importation dans le kit de développement logiciel (SDK) Windows 10 :
    -   **icuuc. lib**
    -   **icuin. lib**

### <a name="version-1709-fall-creators-update"></a>Version 1709 (mise à jour des créateurs de automne)
Un fichier d’en-tête combiné, **ICU. h**, a été ajouté, qui contient le contenu des deux fichiers d’en-tête ci-dessus (icucommon. h et icui18n. h), et modifie également le type de `UCHAR` en `char16_t` .

### <a name="version-1903-may-2019-update"></a>Version 1903 (mai 2019 mise à jour)
Une nouvelle DLL combinée, **icu.dll**, a été ajoutée, qui contient les bibliothèques « communes » et « i18n ». En outre, une nouvelle bibliothèque d’importation a été ajoutée au kit de développement logiciel (SDK) Windows 10 : **ICU. lib**.

À l’avenir, aucune nouvelle API ne sera ajoutée aux anciens en-têtes (icucommon. h et icui18n. h) ou aux anciennes bibliothèques d’importation (icuuc. lib et icuin. lib). Les nouvelles API sont ajoutées uniquement à l’en-tête combiné (ICU. h) et à la bibliothèque d’importation combinée (ICU. lib).

## <a name="getting-started"></a>Mise en route

Il existe trois étapes principales à suivre : (Windows 10 Creators Update ou version ultérieure)

<dl>

1. Votre application doit cibler Windows 10 version 1703 (Creators Update) ou une version ultérieure.

2. Ajoutez les en-têtes :

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   Sur Windows 10 version 1709 et versions ultérieures, vous devez inclure l’en-tête combiné à la place :

   ``` syntax
   #include <icu.h>
   ```
  
3. Lien vers les deux bibliothèques :

   -   icuuc. lib
   -   icuin. lib

   Sur Windows 10 version 1903 et versions ultérieures, vous devez utiliser la bibliothèque combinée à la place :

   -   ICU. lib

</dl>

Ensuite, vous pouvez appeler l’API ICU C à partir de ces bibliothèques. (Aucune API C++ n’est exposée.)

> [!IMPORTANT]
> Si vous utilisez les bibliothèques d’importation héritées, icuuc. lib et icuin. lib, assurez-vous qu’elles sont répertoriées avant les bibliothèques de parapluie, telles que onecoreuap. lib ou WindowsApp. lib, dans le paramètre de l’éditeur de liens dépendances supplémentaires (Voir l’image ci-dessous). Dans le cas contraire, l’éditeur de liens sera lié à ICU. lib, ce qui entraînera une tentative de chargement de icu.dll au moment de l’exécution. Cette DLL est présente uniquement depuis la version 1903. Par conséquent, si un utilisateur met à niveau le kit de développement logiciel (SDK) Windows 10 sur un ordinateur Windows antérieur à la version 1903, l’application ne peut pas se charger et s’exécuter. Pour obtenir un historique des bibliothèques ICU dans Windows, consultez [historique des modifications apportées à la bibliothèque ICU dans Windows](#history-of-changes-to-the-icu-library-in-windows).

![exemple ICU](images/icu-example.png)

> [!Note]  
>
> - Il s’agit de la configuration pour « toutes les plateformes ».
> - Pour que les applications Win32 utilisent ICU, elles doivent d’abord appeler [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .
> - Toutes les données retournées par les API ICU ne sont pas alignées sur le système d’exploitation Windows, car ce travail d’alignement est toujours en cours. 

## <a name="icu-example-app"></a>Exemple d’application ICU

### <a name="example-code-snippet"></a>Exemple d’extrait de code

Voici un exemple illustrant l’utilisation d’API ICU à partir d’une application UWP C++. (Il n’est pas destiné à être une application autonome complète, mais il s’agit simplement d’un exemple d’appel d’une méthode ICU.)

Le petit exemple suivant suppose qu’il existe des méthodes **ErrorMessage** et **OutputMessage** qui génèrent les chaînes à l’utilisateur d’une certaine manière.

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

 

 



