---
description: Découvrez comment étendre le ruban de l’Explorateur Windows.
title: Extension du ruban
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525323"
---
# <a name="extending-the-ribbon"></a>Extension du ruban

Dans l’Explorateur Windows, le ruban permet de rendre les activités de gestion des fichiers de l’utilisateur final courantes plus simples et plus détectables, mais il existe des modifications ouverts pour les développeurs d’applications. Par exemple, l’ancienne barre de commandes était librement extensible, mais le ruban est plus restreint pour l’instant. En outre, le ruban n’est pas affiché par défaut pour toutes les extensions d’espace de noms. vous devez donc vous abonner pour obtenir le ruban. dans le cas contraire, vous recevez l’ancienne barre de commandes.

Les actions disponibles pour les utilisateurs sur le ruban se répartissent en trois catégories d’extensibilité :

-   L’extensibilité n’est pas nécessaire. Exemples : copier, coller, supprimer. Windows gère ces verbes pour vous.
-   L’extensibilité n’est pas autorisée actuellement : des exemples : zip, Close session et d’autres actions personnalisées. Utilisez le menu contextuel pour couvrir ces scénarios.
-   L’extensibilité est intégrée à l’action elle-même. Exemples : recherche, courrier électronique, impression, nouvel élément. Vous devez vous inscrire pour que ces verbes incluent votre application ou le format de fichier dans le ruban.

Ce document décrit comment vous pouvez vous abonner pour accéder au ruban et comment s’inscrire pour gérer des verbes de ruban spécifiques.

## <a name="opting-in-to-the-ribbon"></a>S’abonner au ruban

Pour s’abonner au ruban, votre implémentation de [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) doit spécifier le **\_ ruban EP** dans [**IExplorerPaneVisibility :: GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) et retourner **EPS \_ force** \| **EPS \_ par défaut \_**.

## <a name="extending-the-ribbon-for-file-extensions"></a>Extension du ruban pour les extensions de fichier

Ces boutons de ruban sont extensibles en fonction des extensions de fichier :

-   Extraire tout
-   Montage \| de la gravure (ISO)
-   Lire \| lire tout \| Ajouter à la sélection (verbe : emqueue)
-   Ouvrir
-   Modifier
-   Propriétés

Lorsque vous vous inscrivez pour gérer statiquement les verbes pertinents pour les nouveaux types de fichiers, le ruban gère les verbes de manière appropriée. Vous vous inscrivez comme vous le feriez pour les verbes de menu contextuel. Pour plus d’informations sur les associations de fichiers et l’inscription pour les verbes, consultez [verbes et associations de fichiers](fa-verbs.md) et [création de gestionnaires de menu contextuel](context-menu-handlers.md).

## <a name="registering-as-a-default-handler-for-actionids"></a>Inscription en tant que gestionnaire par défaut pour ActionIds

Tout d’abord, inscrivez votre ProgId sous la sous-clé AssocActionId appropriée. Chaque sous-clé AssocActionId représente un verbe ou une action que les utilisateurs peuvent appeler à partir du ruban. Dans cet exemple, l’application s’inscrit pour l’ActionID ZipSelection pour étendre le bouton « extraire tout » sur le ruban.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

Une fois l’inscription terminée, vous devez vous inscrire pour gérer les protocoles de la même façon que vous le feriez normalement, comme décrit dans [programmes par défaut](default-programs.md).

 

 



