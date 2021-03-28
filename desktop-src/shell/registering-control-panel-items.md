---
description: Les éléments du panneau de configuration doivent être enregistrés afin d’apparaître dans la fenêtre du panneau de configuration.
title: Inscription des éléments du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115727"
---
# <a name="registering-control-panel-items"></a>Inscription des éléments du panneau de configuration

Les éléments du panneau de configuration doivent être enregistrés afin d’apparaître dans la fenêtre du panneau de configuration. Si l’élément du panneau de configuration est implémenté dans le cadre d’un fichier. exe, il est inscrit en tant qu’objet de commande. L’inscription diffère si l’élément est implémenté en tant que fichier. dll qui exporte la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .

Des exigences spécifiques sont décrites dans les rubriques suivantes :

-   [Comment inscrire des éléments du panneau de configuration exécutables](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Comment inscrire les éléments du panneau de configuration de la DLL](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
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

[Accès au panneau de configuration en mode sans échec sous Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
