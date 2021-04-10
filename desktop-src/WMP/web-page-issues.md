---
title: Problèmes de page Web
description: Problèmes de page Web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Sélections de métafichiers Windows Media, pages Web
- sélections, pages Web
- sélections de métafichiers, pages Web
- Sélections de métafichiers Windows Media, personnalisation de HTMLView
- sélections, personnalisation de HTMLView
- sélections de métafichiers, personnalisation de HTMLView
- Sélections de métafichiers Windows Media, personnalisation de HTMLView
- sélections, HTMLView personnalisation
- sélections de métafichiers, personnalisation de HTMLView
- personnalisation de HTMLView
- Windows Media Player, pages Web
- Lecteur Windows Media, personnalisation de HTMLView
- Lecteur Windows Media, personnalisation de HTMLView
- HTMLView, personnalisation
- HTMLView, pages Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675134"
---
# <a name="web-page-issues"></a>Problèmes de page Web

Certains éléments sont à prendre en compte lorsque vous créez une page Web à afficher dans la fonctionnalité de **lecture à présent** du lecteur Windows Media. Cette section présente certains des problèmes que vous pouvez rencontrer lors de la création de votre contenu Web.

## <a name="customizing-htmlview"></a>Personnalisation de HTMLView

Votre page Web HTMLView peut être aussi simple ou complexe que vous le souhaitez. Vous pouvez inclure l’un des éléments que vous utilisez généralement dans votre contenu Web. Si vous incorporez le contrôle du lecteur Windows Media, vous pouvez afficher l’une des interfaces utilisateur fournies par le contrôle, créer votre propre interface utilisateur à l’aide de code HTML et de script ou ne fournir aucune interface utilisateur (ce qui signifie que l’utilisateur peut utiliser les contrôles de transport du lecteur en mode complet).

La taille recommandée pour les pages Web affichées à l’aide de la fonctionnalité HTMLView est de 575 x 345 pixels. Toutefois, l’utilisateur a la possibilité de redimensionner le lecteur Windows Media et de choisir la résolution d’écran. Si la page Web HTMLView est supérieure à la taille prise en charge par la fonctionnalité de **lecture** en cours, le lecteur affiche des barres de défilement horizontales et verticales qui permettent à l’utilisateur de voir la page entière. Vous devez tester votre contenu HTMLView à l’aide d’une variété de résolutions d’écran et de tailles de lecteur pour déterminer la taille optimale de votre page Web.

Le lecteur Windows Media ne fournit pas de méthode qui vous permet de spécifier une taille pour le lecteur en mode plein.

## <a name="web-page-navigation"></a>Navigation entre les pages Web

Le lecteur Windows Media ne fournit pas de barre d’outils de navigation pour les pages Web affichées dans la fonctionnalité de **lecture** en cours. Cela signifie que vous avez un contrôle total sur le fait que les utilisateurs puissent quitter votre page Web HTMLView. Si vous souhaitez permettre aux utilisateurs d’accéder à d’autres pages Web, vous devez inclure des éléments dans votre code HTML pour fournir cette fonctionnalité.

## <a name="retrieving-the-parent-window"></a>Récupération de la fenêtre parente

Si votre code de script existant utilise **Window. parent** pour récupérer l’objet de fenêtre parente, ce code ne fonctionnera pas dans votre page Web HTMLView. Quand vous utilisez HTMLView, il n’y a pas d’objet de fenêtre parente. par conséquent, cette fonctionnalité de script n’est pas disponible.

## <a name="about-the-embedded-browser"></a>À propos du navigateur incorporé

Étant donné que le lecteur Windows Media utilise une instance incorporée d’Internet Explorer pour afficher le contenu de HTMLView, les paramètres et stratégies utilisateur pour Internet Explorer s’appliquent à toutes les pages Web affichées dans le lecteur. Par exemple, si l’utilisateur a configuré Internet Explorer pour empêcher les pages Web de télécharger des cookies sur l’ordinateur, il est également interdit à votre page Web HTMLView de le faire.

Les pages Web ouvertes à l’aide de la fonctionnalité HTMLView s’exécutent toujours dans la zone de sécurité **Internet** d’Internet Explorer.

Le contrôle de navigateur Web incorporé utilise les mêmes règles pour mettre en cache les pages Web que la version autonome d’Internet Explorer. Il est judicieux d’utiliser des pages de Active Server (ASP) lors de la création de votre contenu pour vous assurer que le contenu est remis à partir de votre serveur Web chaque fois que le lecteur Windows Media accède à la page Web HTMLView. L’utilisation de pages ASP peut être aussi simple que l’attribution d’un nouveau nom à votre page Web pour utiliser une extension de nom de fichier. asp.

## <a name="about-local-web-content"></a>À propos du contenu Web local

La fonctionnalité HTMLView ne vous permet pas d’ouvrir des pages Web qui sont stockées sur l’ordinateur de l’utilisateur.

## <a name="prompting-the-user"></a>Invitation de l’utilisateur

Vous pouvez utiliser **Window. prompt** pour inviter l’utilisateur à fournir des informations. Toutefois, **Window. Alert** et **Window. Confirm** ne sont pas disponibles lors de l’utilisation de HTMLView.

## <a name="timing-issues"></a>Problèmes de synchronisation

Vous pouvez rencontrer des problèmes de synchronisation lors de l’utilisation d’un contrôle de lecteur Windows Media incorporé dans votre page Web HTMLView. Dans HTMLView, un contrôle de lecteur incorporé partage son moteur de lecture avec le lecteur Windows Media autonome. Il est possible que le joueur autonome puisse ouvrir et commencer la lecture de la première entrée de la sélection avant que la page Web (et, par conséquent, le contrôle du lecteur) termine le chargement. Cela signifie que si vous gérez les événements **OpenStateChange** ou **PlayStateChange** , le code de script ne recevra pas de notifications d’événements pour ces événements tant que le contrôle du lecteur et ses objets associés ne seront pas chargés.

Vous pouvez prendre des mesures dans votre code pour retarder la lecture jusqu’à ce que le contrôle du lecteur Windows Media soit instancié. Pour ce faire, vous pouvez faire en sorte que la première entrée de votre sélection de métafichier pointe vers un fichier image et définir la durée du fichier sur une durée qui autorise le chargement du contrôle du lecteur. L’exemple de code suivant illustre cette option :


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Lorsque la sélection précédente s’ouvre, le lecteur Windows Media attend la première entrée de la sélection pendant une minute maximum pendant que le lecteur charge la page Web HTMLView.

Ensuite, dans votre page Web HTMLView, écrivez le code de script pour gérer l’événement **OnLoad** de l’élément **Body** . Dans la fonction de gestionnaire d’événements, appelez la méthode Player **Controls. Next** pour commencer la lecture de la deuxième entrée de la playlist.


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



À la fin du chargement de la page Web de l’exemple précédent, le lecteur Windows Media passe immédiatement à la deuxième entrée de la sélection. Cette valeur remplace la durée spécifiée pour le premier élément de la sélection, ce qui signifie que l’utilisateur n’a pas besoin d’attendre la totalité d’une minute avant de voir le contenu souhaité. il doit attendre la fin du chargement de la page Web. Étant donné que le contrôle Player est entièrement instancié à ce stade, les événements **OpenStateChange** et **PlayStateChange** peuvent être gérés de la manière habituelle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Affichage des pages Web dans le lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Événement Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Événement Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 




