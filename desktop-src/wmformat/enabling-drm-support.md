---
title: Activation de la prise en charge de DRM
description: Activation de la prise en charge de DRM
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows Media Format SDK, activation de la prise en charge de DRM
- ASF (Advanced Systems Format), activation de la prise en charge de DRM
- ASF (format de systèmes avancés), activation de la prise en charge de DRM
- gestion des droits numériques (DRM), activation de la prise en charge
- DRM (Digital Rights Management), activation de la prise en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dca900089e93b9f2c149f1e349bdf5b91f88a7c3d549b5f54147839a8ed9296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089749"
---
# <a name="enabling-drm-support"></a>Activation de la prise en charge de DRM

vous pouvez utiliser le kit de développement logiciel (SDK) Microsoft Windows Media Format pour créer des applications qui peuvent appliquer la protection drm (gestion des droits numériques) et lire des flux drm actifs ou des fichiers protégés par drm. La prise en charge est également fournie pour la sauvegarde et la restauration des licences DRM d’un joueur et pour l' [*individualisation*](wmformat-glossary.md) des joueurs.

Cette documentation suppose que vous avez une connaissance de base de la technologie de gestion des droits numériques de Microsoft. une vue d’ensemble de Windows Media DRM est fournie dans la section [fonctionnalités de Rights Management numérique](digital-rights-management-features.md) de cette documentation. Pour plus d’informations sur DRM, consultez la page Digital Rights Management sur le [site Web de Microsoft](https://windows.microsoft.com/windows/products/windows-media).

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

Les sections suivantes décrivent comment activer la prise en charge de DRM.



| Section                                                                                                                        | Description                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtention de la bibliothèque DRM requise](obtaining-the-required-drm-library.md)                                                   | Décrit les étapes nécessaires à l’obtention de la bibliothèque statique requise pour créer des applications compatibles DRM.                                                                               |
| [Protection DRM et distribution des licences de contenu](drm-protection-and-content-license-distribution.md)                         | compare les fonctionnalités DRM de Windows media Format sdk avec le kit de développement logiciel (sdk) media Rights Manager Windows.                                                                                        |
| [Opérations de réseau DRM](drm-network-operations.md)                                                                           | Décrit comment votre application doit gérer les opérations DRM qui communiquent sur Internet ou sur d’autres réseaux.                                                                          |
| [Création de fichiers protégés](creating-protected-files.md)                                                                       | Décrit comment créer des fichiers protégés par DRM.                                                                                                                                                    |
| [Lecture des fichiers protégés](reading-protected-files.md)                                                                         | Décrit les façons d’acquérir des licences pour le contenu et les avantages de l’implémentation de l’acquisition de licence en mode silencieux.                                                                                     |
| [Affichage des attributs des fichiers protégés](viewing-attributes-of-protected-files.md)                                             | Décrit comment utiliser l’interface [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) sur l’objet de l’éditeur de métadonnées pour afficher les attributs des fichiers protégés sans disposer de la bibliothèque statique requise pour DRM. |
| [Utilisation des listes de révocation](working-with-revocation-lists.md)                                                             | Décrit les listes de révocation et la façon dont elles sont implémentées.                                                                                                                                        |
| [Sauvegarde et restauration de licences](backing-up-and-restoring-licenses.md)                                                     | Décrit comment les utilisateurs peuvent gérer leurs licences de contenu en les sauvegardant et en les restaurant sur leur ordinateur actuel ou sur d’autres ordinateurs.                                                         |
| [Individualiser des applications DRM](individualizing-drm-applications.md)                                                       | Décrit comment la fonctionnalité d' [*individualisation*](wmformat-glossary.md) augmente la sécurité dans un système DRM.                                                           |
| [Utilisation des niveaux de protection de sortie](working-with-output-protection-levels.md)                                             | Décrit comment prendre en charge les niveaux de protection de sortie, qui sont utilisés pour enregistrer les actions autorisées dans les licences DRM version 10.                                                                         |
| [utilisation du protocole Windows Media DRM 10 pour les périphériques réseau](using-the-windows-media-drm-10-for-network-devices-protocol.md) | décrit comment prendre en charge la diffusion en continu d’appareils sécurisés à l’aide du protocole Windows Media DRM 10 pour les périphériques réseau.                                                                                |
| [Implémentation de la révocation des licences](implementing-license-revocation.md)                                                         | Décrit le processus de révocation de licence, ainsi que les actions que votre application doit effectuer pour l’implémenter.                                                                                        |
| [Gravure de playlists contenant des fichiers sécurisés](burning-playlists-that-contain-secure-files.md)                                 | Décrit comment implémenter la gravure de sélections dans votre application.                                                                                                                                |



 

Le kit de développement logiciel (SDK) contient plusieurs exemples d’applications qui montrent comment lire des fichiers protégés. l’exemple le plus complet est DRMShow. Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités**](features.md)
</dt> </dl>

 

 




