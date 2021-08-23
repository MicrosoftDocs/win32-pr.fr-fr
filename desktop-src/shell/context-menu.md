---
description: Cette section décrit la création de menus contextuels (contextuels) et l’implémentation des gestionnaires de menu contextuel (verbe).
title: Menus contextuels (menu contextuel) et gestionnaires de menus contextuels
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c091588ff3fefb94d7cd06656c4d7206156b03932c4876f20ad0f26aa03b8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715729"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>Menus contextuels (menu contextuel) et gestionnaires de menus contextuels

Cette section décrit la création de menus contextuels (contextuels) et l’implémentation des gestionnaires de menu contextuel (verbe).

Cette section sur les types de fichiers et les associations de fichiers est organisée comme suit :

-   [Verbes et associations de fichiers](fa-verbs.md)
-   [Choix d’une méthode de menu contextuel statique ou dynamique](shortcut-choose-method.md)
-   [Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes multiples](verbs-best-practices.md)
-   [Création de gestionnaires de menu contextuel](context-menu-handlers.md)
-   [Création de menus en cascade statiques](creating-static-cascading-menus.md)
-   [Comment supprimer et contrôler la visibilité des verbes](how-to-suppress-and-control-visibility.md)
-   [Comment utiliser le modèle de sélection de verbe](how-to-employ-the-verb-selection-model.md)
-   [Utilisation des attributs d’élément](how-to-use-item-attributes.md)
-   [Comment implémenter des verbes personnalisés pour les dossiers via Desktop.ini](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md)
-   [Comment implémenter l’interface IContextMenu](how-to-implement-the-icontextmenu-interface.md)
-   [Référence du menu contextuel](context-menu-reference.md)

## <a name="additional-resources"></a>Ressources supplémentaires

Pour en savoir plus sur l’arrière-plan conceptuel, consultez les rubriques suivantes :

-   [Présentation des associations de fichiers](fa-intro.md).
-   Pour étendre l’interpréteur de commandes avec des gestionnaires de types de fichiers, consultez [création de gestionnaires d’extension de Shell](handlers.md).
-   Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](nse-implement.md).

Pour obtenir des informations de référence connexes documentation, consultez les rubriques suivantes :

-   Pour exécuter un verbe sur un élément de Shell, consultez la méthode [**InvokeVerb**](folderitem-invokeverb.md) .
-   Pour récupérer une collection de verbes qui peuvent être exécutés sur un élément de Shell, consultez la méthode [**Verbs**](folderitem-verbs.md) .
-   Pour effectuer une opération sur un fichier spécifié, consultez les fonctions [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

 

 



