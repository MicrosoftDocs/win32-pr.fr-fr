---
description: Cet ensemble de rubriques explique comment implémenter les gestionnaires d’extension qui vous permettent de modifier diverses actions de l’interpréteur de commandes.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Utilisation des extensions de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb696f4536cdb0fb6869be073771d431bd8d2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973698"
---
# <a name="working-with-shell-extensions"></a>Utilisation des extensions de Shell

Les fonctionnalités de l’interpréteur de commandes peuvent être étendues avec des entrées de Registre et des fichiers. ini. Bien que cette approche de l’extension de l’interpréteur de commandes soit simple et adaptée à de nombreuses fins, elle est limitée. Par exemple, si vous utilisez le registre pour spécifier une icône personnalisée pour un type de fichier, la même icône s’affiche pour chaque fichier de ce type. L’extension de l’interpréteur de commandes avec le registre ne vous permet pas de faire varier l’icône pour différents membres du type de fichier. D’autres aspects de l’interpréteur de commandes, tels que la feuille de propriétés des **Propriétés** qui peuvent être affichées lorsqu’un utilisateur clique avec le bouton droit, ne peuvent pas être modifiés du tout à l’aide du Registre.

Une approche plus puissante et flexible pour étendre l’interpréteur de commandes consiste à implémenter des *gestionnaires d’extensions de Shell*. Ces gestionnaires peuvent être implémentés pour diverses actions que l’interpréteur de commandes peut prendre. Avant d’entreprendre l’action, l’interpréteur de commandes interroge le gestionnaire d’extensions, en lui donnant la possibilité de modifier l’action. Un gestionnaire d’extensions de menu contextuel est un exemple courant. Si l’une d’elles est implémentée pour un type de fichier, elle est interrogée chaque fois que l’utilisateur clique avec le bouton droit sur l’un des fichiers. Le gestionnaire peut ensuite spécifier des éléments de menu supplémentaires pour chaque fichier, au lieu d’avoir le même ensemble pour tous les fichiers de ce type de fichier.

Cet ensemble de rubriques explique comment implémenter les gestionnaires d’extension qui vous permettent de modifier diverses actions de l’interpréteur de commandes. Les gestionnaires suivants sont associés à un type de fichier particulier et vous permettent de spécifier la base de données fichier par fichier.



| Handler                                               | Description                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestionnaire de menu contextuel](context-menu-handlers.md)    | Appelé avant l’affichage du menu contextuel d’un fichier. Elle vous permet d’ajouter des éléments au menu contextuel, fichier par fichier.                                               |
| [Gestionnaire de données](how-to-create-data-handlers.md)       | Appelé lorsqu’une opération de glisser-déplacer est exécutée sur des objets Shell. Elle vous permet de fournir des formats de presse-papiers supplémentaires à la cible de déplacement.                            |
| [Supprimer le gestionnaire](how-to-create-drop-handlers.md)       | Appelé lorsqu’un objet de données est déplacé ou déplacé sur un fichier. Elle vous permet de créer un fichier dans une cible de déplacement.                                                          |
| [Gestionnaire d’icône](how-to-create-icon-handlers.md)       | Appelé avant l’affichage de l’icône d’un fichier. Elle vous permet de remplacer l’icône par défaut du fichier par une icône personnalisée, fichier par fichier.                                    |
| [Gestionnaire de feuille de propriétés](propsheet-handlers.md)      | Appelé avant l’affichage de la feuille de propriétés des **Propriétés** d’un objet. Elle vous permet d’ajouter ou de remplacer des pages.                                                              |
| [**Gestionnaire d’images miniatures**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fournit une image pour représenter l’élément.                                                                                                                                   |
| [**Gestionnaire d'info-bulle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fournit du texte contextuel lorsque l’utilisateur place le pointeur de la souris sur l’objet.                                                                                               |
| [**Gestionnaire de métadonnées**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Fournit un accès en lecture et en écriture aux métadonnées (propriétés) stockées dans un fichier. Cela peut être utilisé pour étendre le mode Détails, info-bulles, la page de propriétés et les fonctionnalités de regroupement. |



 

D’autres ne sont pas associées à un type de fichier particulier, mais sont appelées avant certaines opérations de Shell.



| Handler                                                            | Description                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestionnaire de colonnes](../lwef/column-handlers.md)                             | Appelée par l’Explorateur Windows avant d’afficher la vue Détails d’un dossier. Elle vous permet d’ajouter des colonnes personnalisées à la vue Détails.        |
| [Gestionnaire de raccordement de copie](how-to-create-copy-hook-handlers.md)          | Appelé lorsqu’un objet de dossier ou d’imprimante est sur le lieu d’être déplacé, copié, supprimé ou renommé. Elle vous permet d’approuver ou de refuser l’opération.   |
| [Gestionnaire de glisser-déplacer](context-menu-handlers.md)                 | Appelé lorsqu’un fichier est glissé avec le bouton droit de la souris. Elle vous permet de modifier le menu contextuel qui s’affiche.                     |
| [Gestionnaire de superposition d’icône](how-to-implement-icon-overlay-handlers.md) | Appelé avant l’affichage de l’icône d’un fichier. Elle vous permet de spécifier une superposition pour l’icône du fichier.                                          |
| [Gestionnaire de recherche](../lwef/search-handlers.md)                             | Appelé pour lancer un moteur de recherche. Elle vous permet d’implémenter un moteur de recherche personnalisé accessible à partir du menu **Démarrer** ou de l’Explorateur Windows. |



 

Les détails sur la façon d’implémenter des gestionnaires d’extensions spécifiques sont traités dans les sections répertoriées ci-dessus. Pour connaître les problèmes d’implémentation qui sont communs à tous les gestionnaires d’extensions de Shell, consultez les rubriques suivantes :

-   [Initialisation des gestionnaires d’extensions de Shell](int-shell-exts.md)
-   [Inscription des gestionnaires d’extensions de Shell](reg-shell-exts.md)

 

 
