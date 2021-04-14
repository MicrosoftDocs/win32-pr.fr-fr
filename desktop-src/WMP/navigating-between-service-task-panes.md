---
title: Navigation entre les volets des tâches de service
description: Navigation entre les volets des tâches de service
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player Online stores, navigation
- magasins en ligne, navigation
- tapez 2 magasins en ligne, navigation
- Magasins en ligne du lecteur Windows Media, volets des tâches du service
- magasins en ligne, volets des tâches de service
- types 2 magasins en ligne, volets de tâches de service
- Windows Media Player Online stores, volets des tâches
- magasins en ligne, volets des tâches
- tapez 2 magasins en ligne, volets des tâches
- navigation dans les magasins de type 2 en ligne
- Windows Media Player, service, volets Office
- Windows Media Player, volets des tâches
- volets de tâches du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310030"
---
# <a name="navigating-between-service-task-panes"></a>Navigation entre les volets des tâches de service

Pour naviguer entre les volets des tâches de service dans le lecteur Windows Media, utilisez la méthode **NavigateTaskPaneURL** , qui est disponible à l’aide de l’objet **Window. external** . Lorsque vous utilisez cette méthode, vous spécifiez des valeurs pour trois paramètres :

-   *bstrKeyName*. Il s’agit du nom de clé du magasin en ligne. Lorsque vous naviguez dans un magasin en ligne, utilisez le nom de clé du magasin actuel.
-   *bstrTaskPane*. Cette chaîne contient le nom du volet de tâches du service auquel vous souhaitez accéder.
-   *bstrParams*. Cette chaîne contient les paramètres de chaîne de requête que vous souhaitez ajouter à l’URL de la page Web hébergée par le volet de tâches du service auquel vous souhaitez accéder.

La navigation est gérée par une page Web que vous créez, appelée page naviguer. L’URL de la page Navigate est spécifiée par l’élément **Navigate** dans le document serviceInfo. Quand vous appelez **NavigateTaskPaneURL**, le lecteur Windows Media ouvre la page naviguer, pas la page Web spécifiée par les éléments **ServiceTask1**, **ServiceTask2** ou **ServiceTask3** . Il s’agit de la page de navigation qui reçoit la chaîne de requête spécifiée par *bstrParams*. La page naviguer doit contenir les règles qui déterminent le contenu qui s’affiche dans un volet de tâches de service après la navigation.

Par exemple, supposons que vous souhaitez que les utilisateurs cliquent sur un lien pour naviguer de **ServiceTask1** à **ServiceTask2**. Vous pouvez utiliser le code HTML suivant pour créer le lien :


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Quand l’utilisateur clique sur le lien vidéo, le lecteur Windows Media bascule vers **ServiceTask2** et ouvre la page naviguer, en ajoutant la chaîne de requête suivante à son URL.


```C++
?From=Music&To=2

```



Le paramètre from identifie la page à partir de laquelle l’utilisateur a cliqué sur le lien et le paramètre to identifie le numéro du volet de tâches du service auquel il souhaite naviguer. (Notez qu’il n’y a rien de spécial concernant ces paramètres. Vous pouvez utiliser tous les paramètres que vous souhaitez pour les besoins de votre choix.)

Par exemple, l’exemple de code suivant montre l’élément **Navigate** dans un document serviceInfo :


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



L’URL qui en résulte, avec la chaîne de requête, est présentée dans l’exemple suivant :


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



L’exemple de code suivant affiche la page naviguer :


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



Le code précédent crée simplement une URL et y redirige le navigateur. Tout d’abord, le code récupère les valeurs à partir de la chaîne de requête d’URL et de la chaîne de requête elle-même. Elle utilise la valeur du paramètre to pour déterminer la page à afficher. Il ajoute ensuite la chaîne de requête d’origine à l’URL. Enfin, il parcourt le navigateur à l’aide d’une URL semblable à la suivante :


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Chaque fois que vous effectuez la navigation de cette manière, veillez à spécifier [External. SelectedTaskPane](external-selectedtaskpane.md) pour vous assurer que le bouton de tâche correct est mis en surbrillance.

-   **Avertissement** Veillez à utiliser les paramètres de chaîne de requête pour la navigation.

Les pages Web HTMLView peuvent être fournies par toute personne qui crée une sélection ASX. Cela signifie que les sites Web malveillants peuvent transmettre des valeurs de chaîne de requête à votre magasin en ligne à l’aide de **NavigateTaskPaneURL**. Vous devez prévoir cette possibilité pour garantir la sécurité de votre magasin en ligne. Par exemple, si votre magasin en ligne affiche simplement une valeur de chaîne de requête à l’utilisateur, un site Web malveillant peut afficher du texte inattendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Affichage des pages Web dans le lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Élément Navigate**](navigate-element.md)
</dt> <dt>

[**Navigation pour les magasins de type 2 en ligne**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




