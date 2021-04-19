---
title: Exemple simple de script dans une page Web
description: Exemple simple de script dans une page Web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- Contrôle ActiveX du lecteur Windows Media, exemple de script
- Contrôle ActiveX mobile pour Windows Media Player, exemple de script
- Contrôle ActiveX, exemple de script
- incorporation, pages Web
- Incorporation de page Web, exemple de script
- exemple de script pour l’incorporation de pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106510850"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a>Exemple simple de script dans une page Web

Vous pouvez facilement incorporer le contrôle du lecteur Windows Media dans un fichier HTML à l’aide de n’importe quel langage de script reconnu par votre navigateur. L’exemple simple suivant utilise Microsoft JScript pour créer une page qui lit un fichier lorsque vous cliquez sur un bouton et arrête la lecture du fichier lorsque vous cliquez sur un autre bouton.

Vous pouvez incorporer le contrôle ActiveX du lecteur Windows Media dans une page Web en suivant les quatre étapes suivantes :

1.  Créez la page Web.
2.  Ajoutez la balise OBJECT.
3.  Ajoutez une interface utilisateur. Dans ce cas, deux boutons.
4.  Ajoutez quelques lignes de code pour répondre quand l’utilisateur clique sur l’un des boutons que vous avez créés.

## <a name="creating-the-web-page"></a>Création de la page web

La première étape consiste à créer une page Web HTML valide. Le code suivant est le minimum nécessaire pour créer une page HTML vide mais valide :


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a>Ajout de la balise OBJECT

Une fois que vous avez créé une page Web, vous devez ajouter une balise d’objet. Cela identifie le contrôle ActiveX dans le navigateur et définit toutes les définitions initiales. Vous devez placer la balise OBJECT dans le corps du code. Si vous le placez dans le corps, l’interface utilisateur par défaut du lecteur Windows Media sera visible. Si vous souhaitez créer votre propre interface utilisateur, définissez les attributs Height et Width sur 0 (zéro). Vous pouvez également définir le *lecteur*. propriété **UIMODE** sur « invisible » lorsque vous souhaitez masquer le contrôle, tout en réserve de l’espace pour celui-ci sur la page. Le code suivant est recommandé lorsque vous fournissez une interface utilisateur personnalisée :


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



Les attributs de balise d’objet suivants sont requis :

id

Nom qui sera utilisé par d’autres parties du code pour identifier et utiliser le contrôle ActiveX. Vous pouvez choisir le nom de votre choix, à condition qu’il s’agit d’un nom qui n’est pas déjà utilisé par le HTML, les extensions HTML ou le langage de script que vous utilisez. Dans cet exemple, le nom « Player » est utilisé, mais vous pouvez également l’appeler « MyPlayer » ou autre chose. Choisissez simplement un nom qui est unique à cette page Web.

CLASSID

Nombre hexadécimal très grand qui est unique pour le contrôle. Un seul contrôle a ce nombre et il s’agit du contrôle ActiveX du lecteur Windows Media. Pour éviter les erreurs typographiques, vous pouvez copier et coller ce numéro dans la documentation. Les versions du contrôle du lecteur Windows Media antérieures à la version 7,0 ont un CLASSID différent.

## <a name="adding-a-user-interface"></a>Ajout d’une interface utilisateur

HTML offre une multitude d’éléments d’interface utilisateur, ce qui permet à l’utilisateur d’interagir avec votre page Web en cliquant sur les touches et sur les autres actions de l’utilisateur. L’ajout de quelques boutons d’entrée est le moyen le plus simple de fournir une interface utilisateur rapide. Le code suivant crée deux boutons qui peuvent répondre à l’utilisateur. Le fait de cliquer sur un bouton démarre la diffusion du flux multimédia, et l’autre bouton l’arrête :


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



Le nom du bouton est utilisé pour identifier le bouton dans votre code ; la valeur est l’étiquette qui s’affiche sur le bouton et l’attribut OnClick identifie la partie de votre code de script qui sera appelée lorsque l’utilisateur clique sur le bouton.

## <a name="adding-scripting-code"></a>Ajout de code de script

Le code de script ajoute l’interactivité à votre page. Le code de script peut répondre aux événements, appeler des méthodes et modifier les propriétés au moment de l’exécution. Les scripts étendus sont placés dans un ensemble de balises de SCRIPT. La balise SCRIPT indique au navigateur où se trouve votre code de script et identifie le langage de script. Si vous n’identifiez pas une langue, la langue par défaut est Microsoft JScript.

Il est recommandé de placer votre script dans des balises de commentaire HTML pour que les navigateurs qui ne prennent pas en charge les scripts n’affichent pas votre code sous forme de texte. Placez la balise de SCRIPT n’importe où dans le corps de votre fichier HTML et incorporez le code entouré de commentaires dans les balises de SCRIPT d’ouverture et de fermeture.

L’exemple de code Microsoft JScript suivant appelle le contrôle du lecteur Windows Media et exécute une action appropriée en réponse au clic de bouton correspondant.


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



L’exemple de fonction, StartMeUp, est appelé quand l’utilisateur clique sur le bouton de lecture et que la fonction ShutMeDown est appelée quand l’utilisateur clique sur le bouton arrêter.

Le code à l’intérieur de StartMeUp utilise la propriété URL pour définir un chemin d’accès au média. Le média commence à s’exécuter immédiatement.

Le code ShutMeDown appelle la méthode **Stop** de l’objet **Controls** . Notez que l’objet **Controls** est appelé via la propriété **Controls** de l’objet **Player** , qui a la valeur d’ID « Player ».

L'exemple de code suivant illustre l'exemple complet.


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



Notez que vous devez fournir une URL valide à un nom de fichier valide dans la propriété URL. Dans ce cas, il est supposé que le fichier Laure. WMA se trouve dans le même répertoire que le fichier HTML.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans une page Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




