---
title: Fichiers de bibliothèque, fichiers d’en-tête et paramètres du compilateur
description: Fichiers de bibliothèque, fichiers d’en-tête et paramètres du compilateur
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media Format SDK, fichiers de bibliothèque DRM
- Windows Media Format SDK, fichiers de bibliothèque
- Windows Media Format SDK, fichiers d’en-tête DRM
- Windows Media Format SDK, fichiers d’en-tête
- Windows Media Format SDK, paramètres du compilateur DRM
- Windows Media Format SDK, paramètres du compilateur
- gestion des droits numériques (DRM), fichiers de bibliothèque
- DRM (gestion des droits numériques), fichiers de bibliothèque
- gestion des droits numériques (DRM), fichiers d’en-tête
- DRM (gestion des droits numériques), fichiers d’en-tête
- gestion des droits numériques (DRM), paramètres du compilateur
- DRM (gestion des droits numériques), paramètres du compilateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100740"
---
# <a name="library-files-header-files-and-compiler-settings"></a>Fichiers de bibliothèque, fichiers d’en-tête et paramètres du compilateur

Les composants de programmation des API étendues du client Windows Media DRM sont définis dans le fichier d’en-tête wmdrmsdk. h et implémentés dans les bibliothèques wmdrmsdk. lib et mfuuid. lib.

Certaines fonctionnalités des API étendues du client Windows Media DRM requièrent que vous obteniez une bibliothèque protégée de Microsoft. Cette bibliothèque, appelée bibliothèque stub dans cette documentation, est spécifique au destinataire et spécifie le niveau de sécurité de l’application pour vos applications. La bibliothèque stub remplace wmdrmsdk. lib ; vous ne devez jamais établir de liaison avec les deux.

**Remarque** La bibliothèque de stubs DRM est distincte de la bibliothèque de stubs utilisée par le reste du kit de développement logiciel (SDK) du format Windows Media, mais elle est autorisée à l’aide de la même méthode.

**Remarque** La bibliothèque de stubs DRM doit être liée à votre application après le fichier de bibliothèque Msvcrt. lib pour éviter les erreurs de l’éditeur de liens.

La bibliothèque stub contient un certificat incorporé qui peut être révoqué par Microsoft si vous ne respectez pas les conditions générales du contrat de licence.

Les méthodes spécifiques qui requièrent la bibliothèque stub sont étiquetées dans la documentation. Si vous essayez d’utiliser une telle méthode sans établir de liaison avec la bibliothèque de stubs, elle renverra une erreur de type STUBLIB de la bibliothèque de multiservice (DRM) NS \_ E \_ \_ \_ .

Le sous-système DRM ne peut pas être utilisé dans une version Debug. Si cette tentative est effectuée, les méthodes de l’API retournent l’erreur de débogage de l’interface de ligne de service (DRM) NS \_ E \_ \_ \_ non \_ autorisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](drm-getting-started.md)
</dt> <dt>

[**Fichiers de bibliothèque et paramètres du compilateur**](library-files-and-compiler-settings.md)
</dt> <dt>

[**Obtention de la bibliothèque DRM requise**](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




