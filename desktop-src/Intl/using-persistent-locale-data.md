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
# <a name="using-persistent-locale-data"></a>Utilisation des données de paramètres régionaux persistants

Une application globalisée conserve ou transmet souvent des données, par exemple une heure et une date. Lorsque vous décidez de la manière dont votre application doit gérer la persistance des données, n’oubliez pas que les données ne sont pas nécessairement identiques d’un ordinateur à l’autre ou entre des exécutions de l’application. Cela est vrai pour les deux [paramètres régionaux](locales-and-languages.md) fournis avec Windows et les [paramètres régionaux personnalisés](custom-locales.md).

La conception de l’application doit prendre en compte une variété de modifications de données relatives aux paramètres régionaux qui peuvent se produire. Par exemple :

-   Les symboles monétaires peuvent changer à mesure que les pays adoptent l’euro.
-   Les préférences régionales peuvent changer. Par exemple, le format d/m/y peut passer au format m/d/y pour des paramètres régionaux particuliers.
-   L’orthographe des noms de jours peut changer en raison des réformes orthographiques. En outre, la casse peut changer pour les noms de mois ou de jours.

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a>Utiliser des formats de Locale-Independent pour le stockage et l’échange de données

Une application qui rend les données persistantes doit utiliser des formats indépendants des paramètres régionaux pour le stockage et l’échange de données. Les formats codés en dur ou standard sont des exemples. le [nom des paramètres régionaux des paramètres \_ \_ ](locale-name-constants.md)régionaux invariants et les formats de stockage binaires.

Si des données de tri persistantes sont requises, l’application doit utiliser la fonction [**comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) . N’oubliez pas qu’un format indifférent ne reste pas invariant pour le [Tri](sorting.md), uniquement pour les paramètres régionaux et les données de calendrier.

## <a name="use-the-user-default-locale-for-data-presentation"></a>Utiliser les paramètres régionaux par défaut de l’utilisateur pour la présentation des données

Pour présenter des données persistantes, il est préférable pour l’application de reformater les données à l’aide des paramètres régionaux par défaut de l’utilisateur. L’utilisation de ces paramètres régionaux autorise les remplacements de l’utilisateur. Pour plus d’informations, consultez [paramètres \_ régionaux \_ par défaut](locale-user-default.md)de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> <dt>

[Paramètres régionaux personnalisés](custom-locales.md)
</dt> <dt>

[Tri](sorting.md)
</dt> </dl>

 

 



