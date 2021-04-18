---
title: Options du plug-in d’interface utilisateur
description: Options du plug-in d’interface utilisateur
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Plug-ins du lecteur Windows Media, options
- plug-ins, options
- plug-ins d’interface utilisateur, options
- Plug-ins d’interface utilisateur, options
- plug-ins de zone Paramètres
- plug-ins d’arrière-plan
- plug-ins de fenêtre distincts
- plug-ins de zone de métadonnées
- plug-ins de zone d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106526928"
---
# <a name="ui-plug-in-options"></a>Options du plug-in d’interface utilisateur

L’un des cinq types de plug-in d’interface utilisateur peut avoir une page de propriétés dans laquelle l’utilisateur peut modifier des paramètres de plug-in. Cette page de propriétés peut être définie pour s’afficher automatiquement lorsqu’un plug-in est chargé pour la première fois. Vous pouvez également y accéder à partir de l’onglet Plug-ins de la boîte de dialogue Options.

Un plug-in d’interface utilisateur peut être configuré pour être chargé automatiquement après l’installation au démarrage du lecteur Windows Media. S’il n’est pas démarré automatiquement, l’utilisateur peut le charger en le sélectionnant dans la liste des **plug-ins** du menu **Outils** .

Un plug-in de zone d’affichage peut avoir plusieurs présélections, qui sont des vues différentes que le plug-in peut mettre à la disposition de l’utilisateur. L’utilisateur peut modifier la présélection en sélectionnant une entrée différente dans la liste **visualisations et vues** du menu **affichage** , ou en utilisant les boutons fléchés situés en bas du volet de **diffusion en cours** juste au-dessus du message d’État et des contrôles de transport.

Les plug-ins d’interface utilisateur de fenêtre et d’arrière-plan peuvent être programmés pour accepter un élément multimédia ou une sélection que l’utilisateur lui envoie. Si un plug-in prend en charge cette fonctionnalité, son nom s’affiche dans la liste **Envoyer vers** disponible dans le menu contextuel du contrôle de sélection ou de la bibliothèque.

Un plug-in d’interface utilisateur peut être programmé pour intercepter les raccourcis clavier lorsqu’il a le focus clavier. Le focus clavier est nécessaire pour éviter les conflits lorsque plusieurs plug-ins d’interface utilisateur qui interceptent le même raccourci clavier sont chargés. Bien que cela empêche les conflits, elle peut également entraîner des confusions pour les utilisateurs finaux. Pour cette raison, l’utilisation de raccourcis clavier avec les plug-ins de l’interface utilisateur n’est pas recommandée. Toutefois, lorsqu’ils sont utilisés, ils ne doivent pas intercepter les raccourcis clavier utilisés par le lecteur Windows Media. Pour obtenir la liste complète des raccourcis clavier utilisés par le lecteur, consultez l’aide du lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble du plug-in d’interface utilisateur**](ui-plug-in-overview.md)
</dt> </dl>

 

 




