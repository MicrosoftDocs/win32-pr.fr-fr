---
title: Guide de programmation de plug-ins d’interface utilisateur
description: Guide de programmation de plug-ins d’interface utilisateur
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Lecteur Windows Media, plug-ins
- Lecteur Windows Media, plug-ins d’interface utilisateur
- Plug-ins du lecteur Windows Media, interface utilisateur
- plug-ins, interface utilisateur
- plug-ins d’interface utilisateur, Guide de programmation
- Plug-ins d’interface utilisateur, Guide de programmation
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d417d246e92a642711e8cb02f77ff3795d47c995
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840369"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Guide de programmation de plug-ins d’interface utilisateur

Les deux exemples de code décrits dans cette section illustrent le processus d’implémentation d’un plug-in d’interface utilisateur (IU) personnalisé à partir du code généré par l’Assistant de plug-in du lecteur Windows Media.

Le plug-in de l’interface utilisateur de recherche est un plug-in de zone de métadonnées qui fournit un bouton de **recherche** . Lorsque vous cliquez sur ce bouton, une page de recherche est lancée dans le navigateur Web par défaut qui contient des informations sur l’artiste de l’élément multimédia en cours.

La première étape de la création de ce plug-in consiste à démarrer un nouveau projet dans Microsoft Visual C++ en sélectionnant **Assistant de plug-in Windows Media Player sous** l’onglet **projets** . Nommez le projet « Search », puis cliquez sur **OK**. Choisissez **plug-in d’interface utilisateur** , puis cliquez sur **suivant**. Choisissez ensuite le type de métadonnées dans la liste options, puis cliquez sur **suivant**. Enfin, cliquez sur la case à cocher pour la prise en charge de l’exécution automatique afin que le plug-in se charge automatiquement, puis cliquez sur **Terminer**. L’Assistant génère les fichiers projet requis, y compris les implémentations de base de la classe CSearch et de l’interface **IWMPPluginUI** qu’il prend en charge, ainsi que la classe CPluginWindow qui fournit l’interface utilisateur. Il s’agit du code qui sera modifié pour fournir la fonctionnalité de plug-in décrite dans cette section.

La dernière rubrique de cette section décrit comment créer un plug-in d’IU d’arrière-plan pour le lecteur Windows Media 10 mobile. Ce plug-in utilise le code modifié généré à partir de l’Assistant de plug-in du lecteur Windows Media pour créer un plug-in pour le lecteur Windows Media 10 mobile.

Cette section contient les rubriques suivantes :



| Rubrique                                                                                                                                            | Description                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implémentation de CSearch](implementing-csearch.md)                                                                                                 | Décrit les modifications requises pour la classe CSearch.                                |
| [Implémentation de CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Décrit les modifications requises pour la classe CPluginWindow.                          |
| [Création d’un plug-in d’interface utilisateur pour Windows Media Player 10 mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Décrit comment créer un plug-in d’IU d’arrière-plan pour le lecteur Windows Media 10 mobile. |



 

 

 




