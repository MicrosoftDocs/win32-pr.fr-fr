---
title: Notions de base de DRM
description: Notions de base de DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media Format SDK, principes de base de DRM
- gestion des droits numériques (DRM), à propos de
- DRM (gestion des droits numériques), à propos de
- gestion des droits numériques (DRM), protection du contenu
- DRM (gestion des droits numériques), protection du contenu
- gestion des droits numériques (DRM), empaquetage de contenu
- DRM (gestion des droits numériques), empaquetage de contenu
- gestion des droits numériques (DRM), lecture de contenu protégé
- DRM (gestion des droits numériques), lecture de contenu protégé
- protection du contenu
- contenu de l’empaquetage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ef4439308868b0d77db1e9cefac7381fb8fd9ee78be50cccbf2a8dc26e4176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086139"
---
# <a name="drm-basics"></a>Notions de base de DRM

les technologies DRM Windows media sont relativement simples du point de vue du kit de développement logiciel (SDK) Windows media Format. Les composants du kit de développement logiciel (SDK) peuvent être utilisés pour protéger du contenu et pour lire du contenu protégé.

## <a name="protecting-content"></a>Protection du contenu

La protection du contenu (également appelé contenu d’empaquetage) consiste à chiffrer la section des données du fichier et à inclure des informations dans l’en-tête de fichier qui permet aux joueurs de déchiffrer le contenu.

Pour chiffrer le contenu, vous avez besoin d’une clé, qui est une valeur utilisée pour amorcer les algorithmes de chiffrement. Une clé est constituée de deux parties : une valeur initiale de clé (ou une clé privée) et un identificateur de clé (ou une clé publique). La valeur initiale de la clé est la valeur secrète avec laquelle vous encodez du contenu. L’identificateur de clé est une valeur publique qui est incluse dans l’en-tête d’un fichier protégé.

Lorsqu’un fichier est protégé, il ne peut pas être déchiffré sans licence. Une licence contient des informations qui spécifient les conditions d’utilisation du contenu protégé. Les termes d’une licence sont choisis par le propriétaire du contenu et peuvent être personnalisés pour répondre à un large éventail de besoins. Une partie du processus d’empaquetage d’un fichier consiste à inclure l’URL d’une page Web où les utilisateurs peuvent acquérir une licence pour accéder au contenu.

## <a name="reading-protected-content"></a>Lecture du contenu protégé

Pour lire du contenu protégé, une licence pour le contenu doit résider sur l’ordinateur client. certaines restrictions de licence sont vérifiées en interne par les composants DRM du kit de développement logiciel (SDK) Windows Media Format, tandis que d’autres doivent être appliqués par votre application.

vous pouvez utiliser les objets du kit de développement logiciel (SDK) de Format multimédia Windows pour aider l’utilisateur à acquérir des licences pour du contenu et à effectuer d’autres tâches administratives, telles que la mise à jour des composants DRM et la sauvegarde des licences.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




