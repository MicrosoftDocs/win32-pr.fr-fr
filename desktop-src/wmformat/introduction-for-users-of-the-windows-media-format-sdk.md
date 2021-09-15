---
title: présentation des utilisateurs du kit de développement logiciel (SDK) Windows Media Format
description: présentation des utilisateurs du kit de développement logiciel (SDK) Windows Media Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Kit de développement logiciel (SDK) Media format, API étendues clientes DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Windows Media Format SDK, gestion des droits numériques (DRM)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523041"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>présentation des utilisateurs du kit de développement logiciel (SDK) Windows Media Format

la plupart des fonctionnalités fournies par le Windows les api étendues du Client media DRM sont les mêmes que celles fournies par les objets du kit de développement logiciel (SDK) Windows media Format. le kit de développement logiciel (SDK) Windows Media Format fournit aux développeurs les objets nécessaires pour créer, accéder et manipuler des fichiers multimédias qui utilisent la structure de fichiers ASF (Advanced Systems format). étant donné que Windows media drm est conçu pour protéger les fichiers ASF, les fonctionnalités drm côté client ont été incluses dans le kit de développement logiciel (SDK) Windows media Format.

les api étendues du Client media DRM Windows sont publiées conjointement avec la nouvelle génération de plateforme multimédia numérique de Microsoft, le kit de développement logiciel (SDK) Microsoft Media Foundation. Media Foundation inclura des fonctionnalités ASF qui chevauchent certaines des fonctionnalités du kit de développement logiciel (SDK) Windows Media Format. étant donné qu’il existe désormais deux kits de développement logiciel (sdk) Microsoft qui manipulent les fichiers ASF, les fonctionnalités DRM côté client sont séparées de la Windows media Format SDK dans les api étendues du client media DRM Windows. ces api sont accessibles aux utilisateurs du kit de développement logiciel (sdk) Windows Media Format et du kit de développement logiciel (sdk) Media Foundation. à l’heure actuelle, ces api sont incluses dans le package d’installation du kit de développement logiciel (sdk) Windows media format et sont documentées dans le kit de développement logiciel (sdk) Windows media format. toutefois, les api étendues du Client de Media DRM Windows sont implémentées dans leur propre bibliothèque et ont leur propre fichier d’en-tête. après l’installation du kit de développement logiciel (sdk) de format multimédia Windows, ces api peuvent être utilisées une seule fois, sans inclure les en-têtes ou les bibliothèques du kit de développement logiciel (sdk) Windows Media format dans votre application.

si vous développez des applications qui utilisent le kit de développement logiciel (sdk) Windows media Format, vous devez décider s’il faut utiliser les fonctionnalités DRM fournies par le kit de développement logiciel, ou utiliser les api étendues du Client media DRM Windows. alors que la plupart des fonctionnalités de ces deux kits sdk sont très similaires, les api étendues du Client Media DRM Windows offrent les fonctionnalités suivantes qui ne sont pas disponibles pour les utilisateurs des routines drm plus anciennes :

-   Possibilité d’importer du contenu protégé par un système de gestion des droits tiers.
-   possibilité d’exporter le contenu protégé par Windows DRM multimédia vers un système de gestion des droits tiers.
-   Énumération directe des licences dans le magasin de licences.
-   Requêtes de droits simples et agrégées basées sur l’ID de clé (inutile de charger le fichier multimédia).
-   Possibilité de renouveler des composants révoqués à l’aide de l’interface Media Foundation standard, **IMFContentEnabler**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**à propos des api étendues du Client DRM Windows Media**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




