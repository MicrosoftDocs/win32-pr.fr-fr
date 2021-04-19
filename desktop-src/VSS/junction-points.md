---
description: Dans Windows Vista et Windows Server 2008, les emplacements par défaut des données utilisateur et des données système ont changé.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Points de jonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518197"
---
# <a name="junction-points"></a>Points de jonction

Dans Windows Vista et Windows Server 2008, les emplacements par défaut des données utilisateur et des données système ont changé. Par exemple, les données utilisateur précédemment stockées dans le répertoire% SystemDrive% \\ Documents and Settings sont maintenant stockées dans le répertoire% SystemDrive% \\ users. Pour la compatibilité descendante, les anciens emplacements ont des points de jonction qui pointent vers les nouveaux emplacements. Par exemple, C : \\ Documents and Settings est maintenant un point de jonction qui pointe vers C : \\ users. Les applications de sauvegarde doivent être en charge de la sauvegarde et de la restauration des points de jonction.

Ces points de jonction peuvent être identifiés comme suit :

-   Ils disposent du point d’analyse, de l’attribut de fichier \_ \_ \_ \_ \_ masqué et des \_ attributs de fichier \_ système d’attribut de fichier définis.
-   Ils ont également leurs listes de contrôle d’accès (ACL) définies pour refuser l’accès en lecture à tout le monde.

Les applications qui appellent un chemin d’accès spécifique peuvent traverser ces points de jonction s’ils ont les autorisations requises. Toutefois, toute tentative d’énumération du contenu des points de jonction entraîne des échecs. Il est important que les applications de sauvegarde ne traversent pas ces points de jonction ou ne tentent pas de sauvegarder les données sous elles, pour deux raisons :

-   Cela peut entraîner l’application de sauvegarde à sauvegarder les mêmes données plusieurs fois.
-   Cela peut également entraîner des cycles (références circulaires).

## <a name="per-user-junctions-and-system-junctions"></a>Jonctions de Per-User et jonctions système

Les points de jonction utilisés pour assurer la virtualisation des fichiers et du Registre dans Windows Vista et Windows Server 2008 peuvent être divisés en deux classes : jonctions par utilisateur et jonctions système.

Les jonctions par utilisateur sont créées dans chaque profil d’utilisateur individuel pour fournir une compatibilité descendante pour les applications utilisateur. Le point de jonction sur C : \\ Users \\ *username* \\ My documents qui pointe vers c : \\ Users \\ *username* \\ documents est un exemple de jonction par utilisateur. Les jonctions par utilisateur sont créées par le service de profil lors de la création du profil de l’utilisateur.

Les autres jonctions sont des jonctions système qui ne se trouvent pas dans le \\ répertoire du *nom d’utilisateur* de l’utilisateur. Voici quelques exemples de jonctions système :

-   Documents et paramètres
-   Jonctions dans tous les profils utilisateur, public et utilisateur par défaut

Les jonctions système sont créées par userenv.dll quand elles sont appelées par l’accueil de Windows (également appelé ordinateur out-of-Box-Experience, ou mOOBE).

> [!Note]  
> Si l’utilisateur change la langue du système dans une langue autre que l’anglais, les points de jonction système et par utilisateur sont créés avec des noms localisés.

 

 

 



