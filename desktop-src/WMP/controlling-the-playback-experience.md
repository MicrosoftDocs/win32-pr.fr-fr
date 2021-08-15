---
title: Contrôle de l’expérience de lecture
description: Contrôle de l’expérience de lecture
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows Sélections de métafichiers multimédia, contrôle de la lecture
- sélections, contrôle de la lecture
- sélections de métafichiers, contrôle de la lecture
- Windows Sélections de métafichiers multimédia, problèmes de lecture
- sélections, problèmes de lecture
- sélections de métafichiers, problèmes de lecture
- contrôle de la lecture
- Lecteur Windows Media, contrôle de la lecture
- Lecteur Windows Media, problèmes de lecture
- HTMLView, problèmes de lecture
- HTMLView, contrôle de la lecture
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: efca4d299edc40cfb94820fbb1aae7115329c0f3fcbd2859db0bbbc56d7a0d4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341886"
---
# <a name="controlling-the-playback-experience"></a>Contrôle de l’expérience de lecture

Cette section décrit certains des problèmes de lecture que vous pouvez rencontrer lors de l’utilisation de la fonctionnalité HTMLView.

## <a name="requiring-the-user-to-view-web-based-content"></a>Demander à l’utilisateur d’afficher le contenu Web

Vous pouvez décider que vous souhaitez que les utilisateurs puissent bénéficier de votre contenu multimédia numérique lorsque le contenu Web HTMLView est également affiché. Vous pouvez inclure le code de script dans votre page Web HTMLView qui arrête la lecture du contenu multimédia numérique si l’utilisateur quitte la fonctionnalité de **lecture** en cours. Pour ce faire, vous pouvez spécifier un gestionnaire d’événements pour l’événement **Unload** dans le cadre de l’élément **Body** , comme le montre le code HTML suivant :


```XML
<BODY onunload = "UnloadMe();">

```



Vous pouvez ensuite inclure le code de script dans votre fonction de gestionnaire d’événements pour fermer le fichier dans le lecteur. L’exemple de code suivant effectue cette opérations :


```XML
function UnloadMe()
{
   Player.close();
}

```



lorsque l’utilisateur bascule de la **lecture** en cours en cliquant sur un bouton pour ouvrir une autre fonctionnalité Lecteur Windows Media, telle que la bibliothèque, le lecteur ferme le navigateur incorporé. L’événement **onunload** se produit alors, en exécutant le script dans la fonction nommée **UnloadMe**. La méthode [Player. Close](player-close.md) arrête la lecture et décharge le fichier multimédia numérique en cours. Pour réafficher le contenu, l’utilisateur doit rouvrir le fichier. asx d’origine. Cette technique arrête également la lecture lorsque l’utilisateur quitte la page Web HTMLView. Notez que cette technique ne peut pas empêcher l’utilisateur d’afficher le contenu multimédia numérique lorsqu’il bascule en mode apparence.

Vous vous souvenez que le paramètre HTMLView peut être appliqué à chaque élément **entry** dans un fichier. asx. Vous pouvez tirer parti de cette fonctionnalité pour vous assurer que votre contenu HTMLView s’affiche chaque fois qu’un nouveau fichier multimédia numérique démarre. Pour ce faire, associez un élément **param** pour HTMLView à chaque entrée de votre sélection. asx. Quand chaque entrée est lue, le lecteur revient en mode complet et affiche le contenu HTMLView que vous avez spécifié dans la sélection.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>Les types de commandes de script d’URL et de fichier sont désactivés par défaut

Lecteur Windows Media série 9 ou version ultérieure fournit des paramètres qui permettent à l’utilisateur de spécifier si les commandes de script de type URL et fichier peuvent s’exécuter. Par défaut, ces deux types de commandes de script ne s’exécutent pas. Si vous utilisez des types de commande de script personnalisés, ils continuent à s’exécuter, quel que soit le paramètre de l’utilisateur. Si vous devez utiliser des commandes de script de type URL et fichier, vous devez inviter l’utilisateur à modifier les paramètres. Pour modifier les paramètres, cliquez sur **Outils**, puis sur **options** et sur **sécurité**.

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>La réouverture d’un HTMLView ne recharge pas la page Web

lorsque l’utilisateur ouvre un fichier. asx qui comprend un paramètre HTMLView, puis ouvre à nouveau le même fichier, Lecteur Windows Media n’actualise pas la page web HTMLView. Cela signifie également que si vous avez autorisé les utilisateurs à quitter votre page Web HTMLView, le lecteur ne retourne pas le navigateur incorporé à la page Web initiale HTMLView.

## <a name="hiding-the-content-location"></a>Masquage de l’emplacement du contenu

vous pouvez décider que vous ne voulez pas que Lecteur Windows Media affiche l’emplacement de votre contenu multimédia numérique pendant qu’il lit un fichier. asx. en règle générale, Lecteur Windows Media affiche uniquement des informations sur la liste de lecture elle-même lors de la diffusion en continu du contenu à partir d’Internet. Toutefois, il existe des étapes supplémentaires que vous pouvez prendre pour empêcher les utilisateurs de déterminer l’emplacement de votre contenu. par exemple, l’une des méthodes permettant de s’assurer que le lecteur n’affiche pas le chemin d’accès à votre contenu consiste à diffuser votre contenu à l’aide de Services Windows Media sélections côté serveur. Ainsi, lorsque l’utilisateur consulte les propriétés du contenu, il voit l’URL du serveur et non l’URL de votre contenu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**affichage des Pages Web dans les Lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Élément PARAM**](param-element.md)
</dt> </dl>

 

 




