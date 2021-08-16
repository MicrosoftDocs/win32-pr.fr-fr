---
description: La responsabilité principale de tout élément du panneau de configuration est d’afficher une fenêtre qui permet à l’utilisateur d’afficher et de manipuler des paramètres.
title: Conseils sur l’expérience utilisateur
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ef54d44a466f3c766075eae771ccac9d74e20c0622d6092530f1015a538425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857078"
---
# <a name="user-experience-guidelines"></a>Conseils sur l’expérience utilisateur

La responsabilité principale de tout élément du panneau de configuration est d’afficher une fenêtre qui permet à l’utilisateur d’afficher et de manipuler des paramètres. Consultez les [instructions de l’expérience utilisateur des panneaux](../uxguide/winenv-ctrl-panels.md) de configuration pour connaître le comportement et la conception des éléments du panneau de configuration. Les instructions présentées dans cette rubrique illustrent une méthode de déroulement des tâches qui consiste à organiser un élément du panneau de configuration. Cela place les paramètres les plus importants sur une page d’hébergement. Les paramètres moins fréquemment utilisés sont placés sur les pages spoke ou accessibles à partir de liens dans un volet latéral.

Le panneau de configuration comprend de nombreux éléments qui suivent ces recommandations, telles que la facilité d’accès et le centre réseau et partage. Les autres éléments du panneau de configuration utilisent le format de feuille de propriétés de la boîte de dialogue à onglets, comme dans les versions antérieures de Windows. Les exemples incluent l’élément Mouse et les options Internet. L’utilisation du format de la feuille de propriétés doit être supprimée. Si vous créez des éléments du panneau de configuration, vous devez suivre les instructions relatives au déroulement des tâches.

Par le passé, les éléments du panneau de configuration étaient empaquetés en tant que fichiers .cpl. Cela n’est plus nécessaire. Les nouveaux éléments du panneau de configuration doivent être implémentés en tant que fichier .exe autonome ou en tant qu’option d’indicateur de ligne de commande pour le fichier exécutable principal de l’application.

> [!Note]  
> Sur les systèmes 64 bits, les éléments du panneau de configuration de 32 bits s’affichent dans le panneau de configuration lorsque l’option de **dossier éléments du panneau de configuration de la vue 32** est sélectionnée. Les éléments 32 bits doivent se trouver dans le dossier% SystemRoot% \\ SysWOW64 à afficher. Ils ne nécessitent pas d’inscription supplémentaire.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Utilisation de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Traitement des messages du panneau de configuration](message-processing.md)
</dt> <dt>

[Exécution des éléments du panneau de configuration](executing-control-panel-items.md)
</dt> <dt>

[Extension des éléments du panneau de configuration système](extending-system-control-panel-items.md)
</dt> <dt>

[Affectation des catégories du panneau de configuration](assigning-control-panel-categories.md)
</dt> <dt>

[Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md)
</dt> <dt>

[accès au panneau de configuration en Mode Coffre](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



