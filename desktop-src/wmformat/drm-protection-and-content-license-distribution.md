---
title: Protection DRM et distribution des licences de contenu
description: Protection DRM et distribution des licences de contenu
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media Format SDK, protection de contenu DRM
- Windows Kit de développement logiciel (SDK) Media format, licences DRM
- ASF (Advanced Systems Format), protection du contenu DRM
- ASF (format de systèmes avancés), protection de contenu DRM
- ASF (Advanced Systems Format), distribution de licences DRM
- ASF (format de systèmes avancés), distribution de licences DRM
- gestion des droits numériques (DRM), protection du contenu
- DRM (gestion des droits numériques), protection du contenu
- gestion des droits numériques (DRM), distribution de licences
- DRM (gestion des droits numériques), distribution de licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2b0c666136d3713a0b725bfa9d8ff7dd25e84f3cc9d82fd3a97b66137e47d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704313"
---
# <a name="drm-protection-and-content-license-distribution"></a>Protection DRM et distribution des licences de contenu

Du côté de la création, la technologie de gestion des droits numériques implique deux processus principaux : (1) la protection du contenu et (2) la fourniture de licences pour le contenu. La protection d’un fichier implique essentiellement le chiffrement du contenu, ainsi que l’ajout d’une URL dans l’en-tête de fichier qui spécifie l’emplacement où une licence pour le contenu peut être obtenue. si vous souhaitez protéger des fichiers avec, puis distribuer les fichiers à d’autres ordinateurs ou périphériques, vous pouvez utiliser le kit de développement logiciel (sdk) du Format de média Windows ou le kit de développement logiciel (sdk) media Rights Manager Windows pour protéger le fichier. pour les scénarios de DRM dynamiques, vous devez utiliser le kit de développement logiciel (SDK) de Format multimédia Windows pour protéger le contenu lors de son encodage.

pour créer et émettre des licences pour du contenu protégé, vous pouvez créer votre propre solution personnalisée à l’aide des objets du kit de développement logiciel (SDK) Windows Media Rights Manager, ou vous pouvez utiliser un service exécuté par un tiers.

Quelle que soit la méthode utilisée, les fichiers protégés que vous créez contiendront, dans l’en-tête DRM, une URL qui indique aux applications clientes où obtenir une licence pour le contenu.

> [!Note]  
> le kit de développement logiciel (SDK) Windows Media Format ne prend pas en charge la création ou l’émission de licences.

 

Du côté de la lecture, une application DRM doit être en mesure d’obtenir des licences pour du contenu protégé, de déchiffrer ce contenu à l’aide de la clé contenue dans la licence et d’appliquer les restrictions de licence, telles que le nombre de fois où un fichier peut être lu ou si le fichier peut être copié sur un autre appareil. le kit de développement logiciel (SDK) Windows Media Format fournit la prise en charge requise pour créer une application de lecture DRM entièrement activée.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




