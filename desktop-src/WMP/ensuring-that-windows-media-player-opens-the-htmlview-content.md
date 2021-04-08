---
title: S’assurer que le lecteur Windows Media ouvre le contenu HTMLView
description: S’assurer que le lecteur Windows Media ouvre le contenu HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Sélections de métafichiers Windows Media, lecteur Windows Media ouvrant le contenu HTMLView
- sélections, lecteur Windows Media ouvrant le contenu HTMLView
- sélections de métafichiers, lecteur Windows Media ouvrant le contenu HTMLView
- Sélections de métafichiers Windows Media, ouverture de contenu HTMLView
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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673517"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>S’assurer que le lecteur Windows Media ouvre le contenu HTMLView

Actuellement, le lecteur Windows Media série 9 et le lecteur Windows Media 10 sont les seuls lecteurs qui prennent en charge le paramètre *HTMLView* dans les fichiers. asx. Cela signifie que vous devez prendre des mesures pour vous assurer que votre contenu HTMLView est lu dans ces versions du lecteur Windows Media.

Vous devez d’abord déterminer si le lecteur Windows Media série 9 ou le lecteur Windows Media 10 est installé sur l’ordinateur de l’utilisateur. Le kit de développement logiciel (SDK) Windows Media Player comprend un exemple complet qui montre comment détecter les différentes versions de Windows Media Player dans différents navigateurs Web. Bien qu’une analyse complète de l’exemple de détection dépasse le cadre de cette section, vous pouvez suivre certaines étapes de base pour déterminer la version du lecteur Windows Media que l’ordinateur de l’utilisateur exécute.

Dans sa forme la plus simple, la détection du lecteur Windows Media consiste à incorporer le contrôle du lecteur dans la page Web qui établit un lien vers votre contenu HTMLView, puis à inspecter la valeur récupérée par le *lecteur*. propriété **VERSIONINFO** . Une fois que vous avez vérifié que l’utilisateur a installé le lecteur Windows Media série 9 ou le lecteur Windows Media 10, vous pouvez utiliser la méthode [Player. openPlayer](player-openplayer.md) pour ouvrir le contenu dans le lecteur en mode complet. La méthode **openPlayer** garantit que votre contenu est initialement affiché dans la fonctionnalité de **lecture** en cours du lecteur en mode plein, plutôt que dans une apparence, en mode mini lecteur ou dans un autre lecteur qui s’est inscrit comme programme par défaut pour les fichiers avec une extension de nom de fichier. asx, mais ne prend pas en charge HTMLView. Toutefois, une fois le contenu affiché, l’utilisateur dispose d’un contrôle total sur le lecteur Windows Media, ce qui signifie qu’il peut choisir d’afficher une fonctionnalité autre que **lecture en cours**, passer en mode apparence ou même quitter le lecteur.

L’exemple de code suivant crée une page Web pour Internet Explorer. Cette page ouvre un fichier. asx, qui spécifie une page Web HTMLView qui s’affiche dans le lecteur en mode complet lorsque le lecteur Windows Media 9 ou une version ultérieure est installé.


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



Le code de l’exemple précédent incorpore le contrôle du lecteur Windows Media avec la propriété **UIMODE** définie sur « invisible » et les attributs Height et Width du joueur ont la valeur zéro. Cela est dû au fait que la page Web ne nécessite pas l’affichage initial de l’interface utilisateur du contrôle du lecteur ; elle nécessite uniquement l’accès au modèle objet du lecteur. La page affiche également un bouton d’entrée qui permet à l’utilisateur de lire le fichier. asx.

Quand l’utilisateur clique sur le bouton Play ASX, la fonction Microsoft JScript PlayASX s’exécute. Cette fonction récupère d’abord la valeur de la propriété de joueur **VERSIONINFO** , à l’aide de la méthode JScript **parseInt** pour inspecter la valeur numérique de la chaîne récupérée. Si la valeur numérique est supérieure ou égale à 9 (ce qui signifie que l’utilisateur a installé le lecteur Windows Media série 9), le code de script appelle la méthode **openPlayer** , en passant l’URL du fichier. asx qui contient le paramètre HTMLView. Cette méthode ouvre le fichier. asx à l’aide du lecteur Windows Media en mode complet, lit le contenu multimédia numérique dans la sélection. asx et affiche le contenu Web HTMLView dans la fonctionnalité de **lecture** en cours.

Si la valeur numérique de la chaîne de version n’est pas supérieure ou égale à 9 (ce qui signifie que le lecteur Windows Media série 9 ou version ultérieure n’est pas installé sur l’ordinateur), le code de script modifie le **UIMODE** du contrôle Player en « Full », définit une nouvelle largeur et hauteur pour le contrôle, puis ouvre le fichier. asx dans le lecteur incorporé en spécifiant une valeur pour la propriété **URL** . Dans ce cas, le contenu multimédia numérique est lu dans la page Web, mais toutes les valeurs HTMLView spécifiées dans le fichier. asx sont ignorées.

La façon dont le contenu est lu lorsque l’utilisateur n’a pas le lecteur Windows Media série 9 ou le lecteur Windows Media 10 est installé. L’exemple précédent montre comment spécifier que le contenu est lu dans la page Web au lieu du lecteur en mode plein, en ignorant tout contenu HTMLView dans le processus. Vous pouvez prendre d’autres approches. Par exemple, vous pouvez inviter l’utilisateur à installer une version plus récente du lecteur Windows Media, ce qui rend cette version du lecteur obligatoire pour la lecture de votre contenu multimédia numérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Affichage des pages Web dans le lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 




