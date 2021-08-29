---
title: ajout d’un contrôle de Lecteur Windows Media incorporé
description: ajout d’un contrôle de Lecteur Windows Media incorporé
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Windows sélections de métafichiers multimédia, ajout de contrôles de Lecteur Windows Media incorporés
- sélections, ajout de contrôles de Lecteur Windows Media incorporés
- sélections de métafichiers, ajout de contrôles de Lecteur Windows Media incorporés
- Windows sélections de métafichiers multimédias, contrôles Lecteur Windows Media incorporés
- sélections, contrôles de Lecteur Windows Media incorporés
- sélections de métafichiers, contrôles Lecteur Windows Media incorporés
- ajout de contrôles de Lecteur Windows Media incorporés
- contrôles de Lecteur Windows Media incorporés
- Lecteur Windows Media, ajout de contrôles incorporés
- Lecteur Windows Media, contrôles incorporés
- HTMLView, ajout de contrôles de Lecteur Windows Media incorporés
- HTMLView, contrôles Lecteur Windows Media incorporés
- HTMLView, modèle objet Lecteur Windows Media
- HTMLView, modèle objet Player
- Lecteur Windows Media modèle objet, à propos de
- modèle objet, à propos de
- Objet Player
- Windows Support, modèle objet Player
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e6d4b2f6fcbadde7b8914571af7e56f18c546fddfe10cfe0069e795f6f275e39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055517"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>ajout d’un contrôle de Lecteur Windows Media incorporé

il existe deux raisons pour lesquelles vous pouvez envisager d’ajouter une instance incorporée de Lecteur Windows Media à votre présentation HTMLView. tout d’abord, si vous souhaitez afficher du contenu vidéo, vous devez utiliser le contrôle Lecteur Windows Media ActiveX. deuxièmement, si vous souhaitez tirer parti des fonctionnalités du modèle objet Lecteur Windows Media à partir de votre page web HTMLView, vous devez utiliser une instance pour le contrôle du lecteur.

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>Utilisation du contrôle du lecteur pour afficher la vidéo dans le contenu HTMLView

en règle générale, Lecteur Windows Media affiche la vidéo à l’aide du volet vidéo et visualisation de la fonctionnalité de **diffusion en cours** . Comme HTMLView utilise cette zone pour afficher votre page Web, vous devez fournir une zone d’affichage de vidéo supplémentaire si vous souhaitez que le joueur Lise la vidéo. il est facile de le faire à l’aide du contrôle Lecteur Windows Media ActiveX.

Pour utiliser le contrôle Player pour afficher une vidéo, incorporez le contrôle dans votre page Web HTMLView à l’aide de la balise **Object** . Il s’agit de la même technique que celle utilisée pour incorporer le contrôle Player dans une page Web dans laquelle vous souhaitez afficher une vidéo. L’exemple de code suivant illustre la syntaxe de base pour incorporer le contrôle Player dans Internet Explorer :


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



Le paramètre de *démarrage* automatique garantit que le contenu est lu automatiquement chaque fois qu’une nouvelle URL est spécifiée. La valeur que vous spécifiez pour *UIMODE* dépend de vous, mais vous souhaiterez généralement spécifier « None » lors de la création de contenu pour les présentations HTMLView. lorsque vous incorporez le contrôle Lecteur Windows Media pour afficher la vidéo de cette manière, l’utilisateur peut contrôler la lecture à l’aide des contrôles du lecteur en mode plein. il n’est donc pas nécessaire de fournir des contrôles de transport supplémentaires dans la page web. Vous pouvez utiliser l’espace que vous allouez habituellement pour les contrôles de transport pour afficher davantage de texte, de graphiques ou de liens vers d’autres contenus.

ne spécifiez pas de paramètre d' *URL* lors de l’incorporation du contrôle Lecteur Windows Media dans une page web conçue pour s’afficher dans une présentation HTMLView. Au lieu de cela, spécifiez les fichiers multimédias numériques dans le fichier. asx qui ouvre le contenu.

Étant donné que vous fournissez la zone d’affichage vidéo dans votre page Web HTMLView, vous pouvez choisir l’emplacement de la vidéo et la taille de la zone d’affichage. Par exemple, vous pouvez contenir l’objet **Player** dans un élément **div** html, puis spécifier la position de la **balise div** pour placer l’affichage vidéo sur la page Web. Vous pouvez modifier les dimensions de l’affichage vidéo en spécifiant des valeurs pour les attributs de hauteur et de largeur de l’élément **objet** . Vous pouvez également spécifier ces valeurs à l’aide du code de script.

## <a name="using-the-player-object-model"></a>Utilisation du modèle objet Player

le modèle objet Lecteur Windows Media expose des propriétés, des méthodes et des événements que vous pouvez utiliser dans vos pages web HTMLView. lorsque vous incorporez le contrôle ActiveX Lecteur Windows Media dans votre page web HTMLView, vous avez automatiquement accès au modèle objet Player.

si vous incorporez le contrôle Lecteur Windows Media dans votre page web HTMLView, n’utilisez pas le modèle objet de lecteur pour spécifier le fichier multimédia numérique à lire. Par exemple, si vous utilisez le code de script pour spécifier une valeur pour la propriété **URL** du contrôle incorporé, votre page Web HTMLView est déchargée de la fonctionnalité de **lecture** en cours lors de la lecture du fichier multimédia numérique. Pour éviter cela, ouvrez toujours les fichiers. asx qui incluent des paramètres HTMLView quand vous devez utiliser un script pour ouvrir le contenu multimédia numérique à partir de votre page Web HTMLView.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**affichage des Pages Web dans les Lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Paramètres. démarrage automatique**](settings-autostart.md)
</dt> </dl>

 

 




