---
title: Présentation pour les utilisateurs du kit de développement logiciel (SDK) Windows Media format
description: Présentation pour les utilisateurs du kit de développement logiciel (SDK) Windows Media format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- API étendues du client DRM, à propos de
- API étendues du client, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379987"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Présentation pour les utilisateurs du kit de développement logiciel (SDK) Windows Media format

La plupart des fonctionnalités offertes par les API étendues du client Windows Media DRM sont les mêmes que celles fournies par les objets du kit de développement logiciel (SDK) du format Windows Media. Le kit de développement logiciel (SDK) du format Windows Media offre aux développeurs les objets nécessaires pour créer, accéder et manipuler des fichiers multimédias qui utilisent la structure de fichiers ASF (Advanced Systems Format). Étant donné que Windows Media DRM est conçu pour protéger les fichiers ASF, les fonctionnalités DRM côté client étaient incluses dans le kit de développement logiciel (SDK) Windows Media format.

Les API étendues du client Windows Media DRM sont publiées en même temps que la plateforme multimédia numérique nouvelle génération de Microsoft, le kit de développement logiciel (SDK) Microsoft Media Foundation. Media Foundation inclura des fonctionnalités ASF qui chevauchent certaines des fonctionnalités du kit de développement logiciel (SDK) du format Windows Media. Étant donné qu’il existe désormais deux kits de développement logiciel (SDK) Microsoft qui manipulent les fichiers ASF, les fonctionnalités DRM côté client sont séparées du Windows Media Format SDK dans les API étendues du client Windows Media DRM. Ces API sont accessibles aux utilisateurs du kit de développement logiciel (SDK) du format Windows Media et du kit de développement logiciel (SDK) Media Foundation. À l’heure actuelle, ces API sont incluses dans le package d’installation du SDK Windows Media format et sont documentées dans le cadre du kit de développement logiciel (SDK) du format Windows Media. Toutefois, les API étendues du client Windows Media DRM sont implémentées dans leur propre bibliothèque et ont leur propre fichier d’en-tête. Après l’installation du kit de développement logiciel (SDK) Windows Media format, ces API peuvent être utilisées une seule fois, sans inclure les bibliothèques ou les en-têtes du kit de développement logiciel (SDK) du format Windows Media dans votre application.

Si vous développez des applications qui utilisent le kit de développement logiciel (SDK) Windows Media format, vous devez décider s’il faut utiliser les fonctionnalités DRM fournies par le kit de développement logiciel, ou utiliser les API étendues du client Windows Media DRM. Alors que la plupart des fonctionnalités de ces deux kits SDK sont très similaires, les API étendues du client Windows Media DRM offrent les fonctionnalités suivantes qui ne sont pas disponibles pour les utilisateurs des routines DRM plus anciennes :

-   Possibilité d’importer du contenu protégé par un système de gestion des droits tiers.
-   Possibilité d’exporter du contenu protégé par Windows Media DRM vers un système de gestion des droits tiers.
-   Énumération directe des licences dans le magasin de licences.
-   Requêtes de droits simples et agrégées basées sur l’ID de clé (inutile de charger le fichier multimédia).
-   Possibilité de renouveler des composants révoqués à l’aide de l’interface Media Foundation standard, **IMFContentEnabler**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des API étendues du client Windows Media DRM**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




