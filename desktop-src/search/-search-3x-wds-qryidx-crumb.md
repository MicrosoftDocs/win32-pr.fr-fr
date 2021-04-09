---
description: L’argument de navigation prend en charge les instructions de syntaxe de requête avancée (AQS) complète et est particulièrement utile pour contrôler l’étendue d’une recherche.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argument de navigation (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112479"
---
# <a name="crumb-argument-windows-search"></a>Argument de navigation (Windows Search)

L' `crumb` argument prend en charge les instructions de syntaxe de requête avancée (AQS) complète et est particulièrement utile pour contrôler l’étendue d’une recherche. En plus de AQS ements, l' `crumb` argument peut accepter un `location` paramètre spécial sur Windows Vista et `kind` les `store` paramètres et sur XP, comme décrit plus loin dans cette rubrique.

Cette rubrique est organisée comme suit :

-   [Syntaxe de la navigation](#crumb-syntax)
    -   [Exemples généraux](#general-examples)
-   [Utilisation de la navigation avec Vista (emplacement)](#using-crumb-with-vista-location)
    -   [Exemples Vista](#vista-examples)
    -   [Constantes pour les dossiers communs](#constants-for-common-folders)
-   [Utilisation de la navigation avec Windows XP (genre et Store)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Exemples XP](#xp-examples)
-   [Rubriques connexes](#related-topics)

 

## <a name="crumb-syntax"></a>Syntaxe de la navigation

La syntaxe de la navigation est la suivante :


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> partie est toute propriété dans le système de propriétés, et le <value> la partie est une valeur valide pour cette propriété. La <label> partie est un alias facultatif pour la propriété qui s’affiche comme un indicateur d’interface utilisateur.

### <a name="general-examples"></a>Exemples généraux


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Utilisation de la navigation avec Vista (emplacement)

Dans le paramètre de navigation, Windows Vista prend en charge la AQS complète et également la `location` propriété, qui a une implémentation spéciale disponible uniquement sur Windows Vista. Vous pouvez utiliser une chaîne AQS ou la `location` propriété dans un seul paramètre de navigation, mais pas les deux. Si le paramètre de navigation inclut AQS, tout le reste dans ce paramètre de navigation est ignoré.

La `location` propriété vous permet de spécifier un chemin d’accès à rechercher. Windows Vista peut contourner l’indexeur et traverser le répertoire directement si l’emplacement se trouve en dehors de la portée de l’analyse de l’indexeur. Par conséquent, ces recherches peuvent être plus lentes que les recherches qui utilisent l’indexeur.

Lorsque vous spécifiez une `location` propriété, deux paramètres supplémentaires sont pris en charge et facultatifs :



| Paramètre | Valeurs                  | Description                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclusion | inclure, exclure        | Spécifie si la requête doit inclure ou exclure des éléments de ce chemin d’accès. « Include » est la valeur par défaut. Windows Vista ne prend pas en charge les exclusions sans inclusions. (Voir l’exemple) |
| récursivité | récursif, récursif | Spécifie si la recherche doit recurseiser tous les sous-dossiers à partir de la valeur définie dans l’emplacement :<value>. « Recursive » est la valeur par défaut.                             |



 

Pour étendre une recherche à l’aide du protocole search-ms :, vous disposez de différentes options en fonction de la cible de l’étendue.

Dossier sur un ordinateur local :

-   Utilisez AQS (navigation = dossier : <chemin d’accès encodé URL>)
-   Use location argument (navigation = Location : <chemin d’accès encodé URL>)

Dossier sur un ordinateur/réseau distant :

-   Use location argument (navigation = Location : <chemin d’accès encodé URL>)

Dossier accessible via un gestionnaire de protocole UNC connu :

-   Utilisez AQS (navigation = Store : <UNC protocol handler name> )
-   Use location argument (navigation = Location : <chemin d’accès encodé URL>)

### <a name="vista-examples"></a>Exemples Vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Le premier exemple exécute une recherche de « vacances » en commençant à l’emplacement shell://Personal (un raccourci spécial vers le dossier Mes documents de l’utilisateur), y compris ce dossier et tous ses sous-dossiers. Consultez le tableau ci-dessous.

Le deuxième exemple exécute une recherche dans C : \\ images, mais pas dans c : \\ images \\ en double.

Le troisième exemple exécute une recherche dans les documents C : \\ , limitée à des fichiers dont la propriété Kind a la valeur pics.

### <a name="constants-for-common-folders"></a>Constantes pour les dossiers communs

Windows Vista permet l’utilisation de valeurs [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) qui fournissent une méthode unique indépendante du système pour identifier les dossiers spéciaux utilisés fréquemment par les applications, mais qui peuvent ne pas avoir le même nom ou emplacement sur un système donné. Par exemple, le dossier système peut être « C : \\ Windows » sur un système et « c : \\ winnt » sur un autre. Avant Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) étaient utilisés.

Utilisez ces emplacements avec la syntaxe suivante :


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Utilisation de la navigation avec Windows XP (genre et Store)

Pour Windows Search sur Windows XP (WDS 3. x), les termes de AQS « genre » et « Store » ont une implémentation spéciale. Les valeurs « Kind » sont les mêmes que [celles utilisées dans WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md). Les valeurs « Store » sont les suivantes :

-   Protocole
-   fichier
-   outlookexpress
-   n'importe laquelle

### <a name="xp-examples"></a>Exemples XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



Le premier exemple retourne les e-mails Microsoft Outlook Express de John avec l’étiquette personnalisée « OE Mail ». Le deuxième exemple exécute une recherche de toutes les communications de John.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec des arguments Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Arguments de l’identificateur de paramètres régionaux](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argument de syntaxe](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argument STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argument de sous-requête](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
