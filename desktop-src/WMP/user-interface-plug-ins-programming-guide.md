---
title: Guide de programmation de plug-ins d’interface utilisateur
description: Guide de programmation de plug-ins d’interface utilisateur
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Lecteur Windows Media, plug-ins
- Lecteur Windows Media, plug-ins d’interface utilisateur
- plug-ins Lecteur Windows Media, interface utilisateur
- plug-ins, interface utilisateur
- plug-ins d’interface utilisateur, Guide de programmation
- Plug-ins d’interface utilisateur, Guide de programmation
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d417d246e92a642711e8cb02f77ff3795d47c995
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403778"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Guide de programmation de plug-ins d’interface utilisateur

les deux exemples de code décrits dans cette section illustrent le processus d’implémentation d’un plug-in d’interface utilisateur (iu) personnalisé à partir du code généré par l’assistant de plug-in Lecteur Windows Media.

Le plug-in de l’interface utilisateur de recherche est un plug-in de zone de métadonnées qui fournit un bouton de **recherche** . Lorsque vous cliquez sur ce bouton, une page de recherche est lancée dans le navigateur Web par défaut qui contient des informations sur l’artiste de l’élément multimédia en cours.

la première étape de la création de ce plug-in consiste à démarrer un nouveau projet dans Microsoft Visual C++ en sélectionnant **Lecteur Windows Media assistant de plug-** in dans l’onglet **projets** . Nommez le projet « Search », puis cliquez sur **OK**. Choisissez **plug-in d’interface utilisateur** , puis cliquez sur **suivant**. Choisissez ensuite le type de métadonnées dans la liste options, puis cliquez sur **suivant**. Enfin, cliquez sur la case à cocher pour la prise en charge de l’exécution automatique afin que le plug-in se charge automatiquement, puis cliquez sur **Terminer**. L’Assistant génère les fichiers projet requis, y compris les implémentations de base de la classe CSearch et de l’interface **IWMPPluginUI** qu’il prend en charge, ainsi que la classe CPluginWindow qui fournit l’interface utilisateur. Il s’agit du code qui sera modifié pour fournir la fonctionnalité de plug-in décrite dans cette section.

la dernière rubrique de cette section décrit comment créer un plug-in d’interface utilisateur d’arrière-plan pour Lecteur Windows Media 10 Mobile. ce plug-in utilise le code modifié généré à partir de l’assistant de plug-in Lecteur Windows Media pour créer un plug-in pour Lecteur Windows Media 10 Mobile.

Cette section contient les rubriques suivantes :



| Rubrique                                                                                                                                            | Description                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implémentation de CSearch](implementing-csearch.md)                                                                                                 | Décrit les modifications requises pour la classe CSearch.                                |
| [Implémentation de CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Décrit les modifications requises pour la classe CPluginWindow.                          |
| [création d’un Plug-in d’Interface utilisateur pour Lecteur Windows Media 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | décrit comment créer un plug-in d’interface utilisateur d’arrière-plan pour Lecteur Windows Media 10 Mobile. |



 

 

 




