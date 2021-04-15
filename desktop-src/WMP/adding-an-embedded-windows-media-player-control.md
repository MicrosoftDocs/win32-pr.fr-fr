---
title: Ajout d’un contrôle de lecteur Windows Media incorporé
description: Ajout d’un contrôle de lecteur Windows Media incorporé
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Sélections de métafichiers Windows Media, ajout de contrôles de lecteur Windows Media incorporés
- sélections, ajout de contrôles de lecteur Windows Media intégrés
- sélections de métafichiers, ajout de contrôles de lecteur Windows Media incorporés
- Sélections de métafichiers Windows Media, contrôles de lecteur Windows Media intégrés
- sélections, contrôles du lecteur Windows Media intégrés
- sélections de métafichiers, contrôles de lecteur Windows Media intégrés
- ajout de contrôles de lecteur Windows Media incorporés
- contrôles du lecteur Windows Media incorporés
- Lecteur Windows Media, ajout de contrôles incorporés
- Windows Media Player, contrôles incorporés
- HTMLView, ajout de contrôles de lecteur Windows Media intégrés
- HTMLView, contrôles Windows Media Player intégrés
- HTMLView, modèle objet du lecteur Windows Media
- HTMLView, modèle objet Player
- Windows Media Player Object Model, à propos de
- modèle objet, à propos de
- Objet Player
- Windows Media, modèle objet Player
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380144"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>Ajout d’un contrôle de lecteur Windows Media incorporé

Il existe deux raisons pour lesquelles vous pouvez envisager d’ajouter une instance incorporée du lecteur Windows Media à votre présentation HTMLView. Tout d’abord, si vous souhaitez afficher du contenu vidéo, vous devez utiliser le contrôle ActiveX du lecteur Windows Media. Deuxièmement, si vous souhaitez tirer parti des fonctionnalités du modèle objet du lecteur Windows Media à partir de votre page Web HTMLView, vous devez utiliser une instance pour le contrôle du lecteur.

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>Utilisation du contrôle du lecteur pour afficher la vidéo dans le contenu HTMLView

En règle générale, le lecteur Windows Media affiche la vidéo à l’aide du volet vidéo et visualisation de la fonctionnalité de **lecture** en cours. Comme HTMLView utilise cette zone pour afficher votre page Web, vous devez fournir une zone d’affichage de vidéo supplémentaire si vous souhaitez que le joueur Lise la vidéo. Il est facile de le faire à l’aide du contrôle ActiveX du lecteur Windows Media.

Pour utiliser le contrôle Player pour afficher une vidéo, incorporez le contrôle dans votre page Web HTMLView à l’aide de la balise **Object** . Il s’agit de la même technique que celle utilisée pour incorporer le contrôle Player dans une page Web dans laquelle vous souhaitez afficher une vidéo. L’exemple de code suivant illustre la syntaxe de base pour incorporer le contrôle Player dans Internet Explorer :


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



Le paramètre de *démarrage* automatique garantit que le contenu est lu automatiquement chaque fois qu’une nouvelle URL est spécifiée. La valeur que vous spécifiez pour *UIMODE* dépend de vous, mais vous souhaiterez généralement spécifier « None » lors de la création de contenu pour les présentations HTMLView. Lorsque vous incorporez le contrôle du lecteur Windows Media pour afficher la vidéo de cette manière, l’utilisateur peut contrôler la lecture à l’aide des contrôles du lecteur en mode plein. il n’est donc pas nécessaire de fournir des contrôles de transport supplémentaires dans la page Web. Vous pouvez utiliser l’espace que vous allouez habituellement pour les contrôles de transport pour afficher davantage de texte, de graphiques ou de liens vers d’autres contenus.

Ne spécifiez pas de paramètre d' *URL* lors de l’incorporation du contrôle du lecteur Windows Media dans une page Web conçue pour s’afficher dans une présentation HTMLView. Au lieu de cela, spécifiez les fichiers multimédias numériques dans le fichier. asx qui ouvre le contenu.

Étant donné que vous fournissez la zone d’affichage vidéo dans votre page Web HTMLView, vous pouvez choisir l’emplacement de la vidéo et la taille de la zone d’affichage. Par exemple, vous pouvez contenir l’objet **Player** dans un élément **div** html, puis spécifier la position de la **balise div** pour placer l’affichage vidéo sur la page Web. Vous pouvez modifier les dimensions de l’affichage vidéo en spécifiant des valeurs pour les attributs de hauteur et de largeur de l’élément **objet** . Vous pouvez également spécifier ces valeurs à l’aide du code de script.

## <a name="using-the-player-object-model"></a>Utilisation du modèle objet Player

Le modèle objet du lecteur Windows Media expose des propriétés, des méthodes et des événements que vous pouvez utiliser dans vos pages Web HTMLView. Lorsque vous incorporez le contrôle ActiveX du lecteur Windows Media dans votre page Web HTMLView, vous avez automatiquement accès au modèle objet du lecteur.

Si vous incorporez le contrôle du lecteur Windows Media dans votre page Web HTMLView, n’utilisez pas le modèle objet de lecteur pour spécifier le fichier multimédia numérique à lire. Par exemple, si vous utilisez le code de script pour spécifier une valeur pour la propriété **URL** du contrôle incorporé, votre page Web HTMLView est déchargée de la fonctionnalité de **lecture** en cours lors de la lecture du fichier multimédia numérique. Pour éviter cela, ouvrez toujours les fichiers. asx qui incluent des paramètres HTMLView quand vous devez utiliser un script pour ouvrir le contenu multimédia numérique à partir de votre page Web HTMLView.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Affichage des pages Web dans le lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Paramètres. démarrage automatique**](settings-autostart.md)
</dt> </dl>

 

 




