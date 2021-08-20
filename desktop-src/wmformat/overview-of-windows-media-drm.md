---
title: vue d’ensemble de la DRM Windows Media
description: vue d’ensemble de la DRM Windows Media
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Media Format SDK, gestion des droits numériques (DRM)
- Windows Kit de développement logiciel (SDK) Media format, licences DRM
- Windows Media Format SDK, licences pour DRM
- gestion des droits numériques (DRM), à propos de
- DRM (gestion des droits numériques), à propos de
- gestion des droits numériques (DRM), empaquetage Windows fichiers multimédias
- DRM (gestion des droits numériques), empaquetage Windows fichiers multimédias
- gestion des droits numériques (DRM), gestion des licences de fichiers protégés
- DRM (gestion des droits numériques), gestion des licences de fichiers protégés
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), lecture des fichiers protégés
- DRM (gestion des droits numériques), lecture des fichiers protégés
- ASF (Advanced Systems Format), gestion des droits numériques (DRM)
- ASF (format de systèmes avancés), gestion des droits numériques (DRM)
- licences, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6cc882d31873a05361869b9246da1b57ac3d3aebb85073d0b31f24509a615b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846414"
---
# <a name="overview-of-windows-media-drm"></a>vue d’ensemble de la DRM Windows Media

Windows le Rights Management media Digital (DRM) est un système de protection du contenu des fichiers multimédias Windows afin que les utilisateurs non autorisés ne puissent pas y accéder. Il existe trois phases pour le cycle DRM de base : l’empaquetage, la gestion des licences et la lecture.

## <a name="packaging-windows-media-files"></a>empaquetage de fichiers multimédias Windows

Windows media DRM est conçu pour fonctionner avec Windows fichiers multimédias. un fichier multimédia Windows est un fichier conforme à la spécification ASF (Advanced Systems Format) et qui contient uniquement des données Audio et vidéo qui ont été compressées à l’aide des codecs Windows Media Audio et vidéo.

Lorsqu’un fichier ASF est empaqueté, une section spécifique à DRM est ajoutée à l’en-tête. L’en-tête DRM contient un ID de clé qui identifie le contenu à des fins de licence, et une URL d’acquisition de licence, qui est l’adresse d’une page Web qui peut émettre des licences pour lire le contenu protégé. Il existe bien d’autres informations qui peuvent être placées dans l’en-tête DRM, mais elles sont facultatives. L’en-tête DRM est signé afin que le gestionnaire de package puisse être vérifié.

Le contenu du fichier ASF est chiffré pendant le processus de compression. Toutefois, les informations suivantes dans le fichier empaqueté sont disponibles, même pour les clients qui n’ont pas de licence :

-   Métadonnées stockées dans l’en-tête ASF.
-   Certaines métadonnées stockées dans l’en-tête DRM (par exemple, vous pouvez toujours obtenir l’URL d’acquisition de licence).

## <a name="licensing-protected-files"></a>Gestion des licences des fichiers protégés

Pour qu’un fichier empaqueté soit lu, une licence doit être émise sur l’ordinateur client. Une licence est un ensemble de données décrivant les conditions dans lesquelles les données des fichiers protégés peuvent être lues. La plupart du temps, une licence est émise pour un fichier protégé en réponse à l’utilisateur qui tente d’effectuer une opération sur le fichier. Toutefois, il est également possible qu’un émetteur de licence remette des licences à un client avant qu’il ne soit demandé explicitement. Pour plus d’informations sur les licences, consultez [licences](licenses.md).

## <a name="reading-data-from-protected-files"></a>Lecture de données à partir de fichiers protégés

Lorsqu’un utilisateur tente d’effectuer une opération sur un fichier protégé (lire, graver sur un CD-ROM, copier sur un appareil, etc.), l’application doit vérifier les licences du contenu sur l’ordinateur client. Si une licence valide existe sur l’ordinateur client, l’opération peut se poursuivre. S’il n’existe aucune licence pour le contenu, ou si aucune licence pour le contenu de l’ordinateur client n’autorise l’action demandée, une licence doit être acquise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**à propos des api étendues du Client DRM Windows Media**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




