---
title: Lecture des fichiers protégés
description: Lecture des fichiers protégés
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, lire les fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), lire les fichiers protégés
- ASF (format des systèmes avancés), lire les fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (format avancé des systèmes), WMStubDRM. lib
- WMStubDRM. lib, lecture des fichiers protégés
- WMStubDRM. lib, fichiers protégés
- gestion des droits numériques (DRM), WMStubDRM. lib
- DRM (gestion des droits numériques), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723410"
---
# <a name="reading-protected-files"></a>Lecture des fichiers protégés

La lecture d’un fichier protégé par DRM ou d’un flux réseau implique la tentative d’ouvrir le fichier (ou de se connecter au flux), puis de gérer les événements qui peuvent être envoyés à partir des composants DRM.

Si un lecteur n’est pas compatible DRM (ne lie pas à une bibliothèque wmstubdrm. lib valide) l’appel de [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) échoue lorsqu’il tente d’ouvrir un fichier protégé et retourne \_ du \_ contenu protégé par le service NS \_ ou une erreur associée.

Quand une application compatible DRM tente d’ouvrir un fichier protégé par DRM, le composant DRM recherche automatiquement une licence valide dans le système local. S’il en existe un, le composant DRM déchiffre automatiquement le fichier d’une manière totalement transparente pour l’application. L’action qu’une application peut effectuer sur le fichier déchiffré dépend des droits spécifiés dans la licence. Pour obtenir une description complète des droits possibles, consultez la documentation du kit de développement logiciel (SDK) Windows Media Rights Manager.

Si l’application ne dispose pas d’une licence valide pour un fichier, le lecteur reçoit une notification d’État du composant DRM. L’application de lecteur peut ensuite lancer le processus d' [*acquisition de licence*](wmformat-glossary.md) . Après la réception d’une licence valide, le fichier est accessible. Les sections suivantes décrivent les tâches de base qu’une application doit effectuer lors de l’implémentation du processus d’acquisition de licence :

-   [Spécification des actions à effectuer](specifying-the-actions-to-be-performed.md)
-   [Gestion des événements d’acquisition de licence](handling-license-acquisition-events.md)
-   [Individualiser des applications DRM](individualizing-drm-applications.md)
-   [Gestion des événements d’individualisation](handling-individualization-events.md)

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Liste des attributs DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




