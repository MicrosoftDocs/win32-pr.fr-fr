---
title: s’assurer que Lecteur Windows Media ouvre le contenu HTMLView
description: s’assurer que Lecteur Windows Media ouvre le contenu HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Windows sélections de métafichiers multimédia, Lecteur Windows Media ouverture du contenu HTMLView
- sélections, Lecteur Windows Media ouverture du contenu HTMLView
- sélections de métafichiers, Lecteur Windows Media ouverture du contenu HTMLView
- Windows Sélections de métafichiers multimédia, ouverture de contenu HTMLView
- sélections, ouverture de contenu HTMLView
- sélections de métafichiers, ouverture de contenu HTMLView
- ouverture du contenu HTMLView
- Lecteur Windows Media, ouverture du contenu HTMLView
- Lecteur Windows Media, contenu HTMLView
- HTMLView, ouverture du contenu
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192412"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>s’assurer que Lecteur Windows Media ouvre le contenu HTMLView

actuellement, Lecteur Windows Media série 9 et Lecteur Windows Media 10 sont les seuls lecteurs qui prennent en charge le paramètre *HTMLView* dans les fichiers. asx. cela signifie que vous devez prendre des mesures pour vous assurer que votre contenu HTMLView est lu dans ces versions de Lecteur Windows Media.

vous devez d’abord déterminer si Lecteur Windows Media série 9 ou Lecteur Windows Media 10 est installé sur l’ordinateur de l’utilisateur. le kit de développement logiciel (SDK) Lecteur Windows Media comprend un exemple complet qui montre comment détecter les différentes versions de Lecteur Windows Media dans différents navigateurs Web. bien qu’une analyse complète de l’exemple de détection dépasse le cadre de cette section, vous pouvez suivre certaines étapes de base pour déterminer quelle version de Lecteur Windows Media l’ordinateur de l’utilisateur est en cours d’exécution.

dans sa forme la plus simple, la détection de Lecteur Windows Media consiste à incorporer le contrôle du lecteur dans la page web qui établit un lien vers votre contenu HTMLView, puis à inspecter la valeur récupérée par le *lecteur*. propriété **VERSIONINFO** . une fois que vous avez vérifié que l’utilisateur a Lecteur Windows Media série 9 ou Lecteur Windows Media 10 installée, vous pouvez utiliser la méthode [player. openPlayer](player-openplayer.md) pour ouvrir le contenu dans le lecteur en mode complet. La méthode **openPlayer** garantit que votre contenu est initialement affiché dans la fonctionnalité de **lecture** en cours du lecteur en mode plein, plutôt que dans une apparence, en mode mini lecteur ou dans un autre lecteur qui s’est inscrit comme programme par défaut pour les fichiers avec une extension de nom de fichier. asx, mais ne prend pas en charge HTMLView. toutefois, une fois le contenu affiché, l’utilisateur dispose d’un contrôle total de Lecteur Windows Media, ce qui signifie qu’il peut choisir d’afficher une fonctionnalité autre que **lecture en cours**, passer en mode apparence ou même quitter le lecteur.

L’exemple de code suivant crée une page Web pour Internet Explorer. cette page ouvre un fichier. asx, qui spécifie une page web HTMLView qui s’affiche dans le lecteur en mode plein lors de l’installation de Lecteur Windows Media série 9 ou version ultérieure.


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



le code de l’exemple précédent incorpore le contrôle Lecteur Windows Media avec la propriété **uiMode** définie sur « invisible » et les attributs height et width du joueur ayant la valeur zéro. Cela est dû au fait que la page Web ne nécessite pas l’affichage initial de l’interface utilisateur du contrôle du lecteur ; elle nécessite uniquement l’accès au modèle objet du lecteur. La page affiche également un bouton d’entrée qui permet à l’utilisateur de lire le fichier. asx.

quand l’utilisateur clique sur le bouton lire ASX, la fonction Microsoft JScript PlayASX s’exécute. cette fonction récupère d’abord la valeur de la propriété **versionInfo** du joueur, à l’aide de la JScript méthode **parseint** pour inspecter la valeur numérique de la chaîne récupérée. si la valeur numérique est supérieure ou égale à 9 (ce qui signifie que l’utilisateur a Lecteur Windows Media série 9 installée), le code de script appelle la méthode **openPlayer** , en passant l’URL du fichier. asx qui contient le paramètre HTMLView. cette méthode ouvre le fichier. asx à l’aide de Lecteur Windows Media en mode complet, lit le contenu multimédia numérique dans la sélection. asx et affiche le contenu Web HTMLView dans la fonctionnalité de **lecture** en cours.

si la valeur numérique de la chaîne de version n’est pas supérieure ou égale à 9 (ce qui signifie que l’utilisateur n’a pas Lecteur Windows Media série 9 ou une version ultérieure installée sur son ordinateur), le code de script modifie le **uiMode** du contrôle Player en « full », définit une nouvelle largeur et hauteur pour le contrôle, puis ouvre le fichier. asx dans le lecteur incorporé en spécifiant une valeur pour la propriété **URL** . Dans ce cas, le contenu multimédia numérique est lu dans la page Web, mais toutes les valeurs HTMLView spécifiées dans le fichier. asx sont ignorées.

comment le contenu est lu lorsque l’utilisateur ne dispose pas de Lecteur Windows Media série 9 ou Lecteur Windows Media 10. L’exemple précédent montre comment spécifier que le contenu est lu dans la page Web au lieu du lecteur en mode plein, en ignorant tout contenu HTMLView dans le processus. Vous pouvez prendre d’autres approches. par exemple, vous pouvez inviter l’utilisateur à installer une version plus récente de Lecteur Windows Media, ce qui rend cette version du lecteur obligatoire pour la lecture de votre contenu multimédia numérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**affichage des Pages Web dans les Lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 




