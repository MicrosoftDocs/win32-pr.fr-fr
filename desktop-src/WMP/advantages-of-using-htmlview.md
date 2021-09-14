---
title: Avantages de l’utilisation de HTMLView
description: Avantages de l’utilisation de HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Windows Playlists de métafichiers multimédias, avantages HTMLView
- sélections, avantages HTMLView
- sélections de métafichiers, avantages HTMLView
- Windows Playlists de métafichiers multimédias, avantages de HTMLView
- sélections, avantages de HTMLView
- playlists de métafichiers, avantages de HTMLView
- avantages de HTMLView
- Lecteur Windows Media, avantages de HTMLView
- Lecteur Windows Media, HTMLView avantages
- HTMLView, avantages
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5e5409db969f5e9a8e0df18738f4995490b1d83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856330"
---
# <a name="advantages-of-using-htmlview"></a>Avantages de l’utilisation de HTMLView

La fonctionnalité HTMLView facilite la création d’une expérience utilisateur Web intégrée qui lit le contenu multimédia numérique en utilisant l’apparence familière du Web. lorsque vous combinez du contenu Web avec du contenu multimédia numérique dans l’interface utilisateur Lecteur Windows Media, le résultat peut avoir un impact plus important sur l’utilisateur que lorsque les éléments sont affichés séparément. Le contenu multimédia numérique est amélioré par des informations intéressantes, tandis que la page Web peut fournir des liens vers du contenu similaire, créant ainsi de nouvelles opportunités commerciales.

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView offre une meilleure expérience utilisateur

Les utilisateurs veulent accéder aux informations qui peuvent être proposées avec le contenu multimédia numérique, mais ils ne souhaitent pas faire face à une série apparemment infinie de publicités publicitaires. L’utilisation de fenêtres de navigateur contextuelles pour afficher des publicités sur le Web est devenue tellement courante qu’il y a maintenant un logiciel qui empêche ces fenêtres de s’ouvrir. Ce logiciel peut avoir un effet secondaire indésirable qui empêche l’affichage des pages Web légitimes, ce qui entraîne parfois la suppression d’une présentation multimédia numérique entière.

Lorsque vous utilisez la fonctionnalité HTMLView, les utilisateurs n’ont plus à gérer les fenêtres indépendantes. au lieu d’ouvrir une fenêtre de navigateur distincte pour fournir des informations supplémentaires à l’utilisateur, vous pouvez afficher du contenu Web personnalisé dans la fonctionnalité de **lecture** en cours de l’interface utilisateur du Lecteur Windows Media, tandis que le joueur lit le contenu audio ou vidéo souhaité par l’utilisateur. les utilisateurs peuvent contrôler la lecture à l’aide des contrôles Lecteur Windows Media. Dans la mesure où votre contenu est lu dans le lecteur en mode plein, les logiciels conçus pour empêcher les publicités publicitaires intempestives n’empêchent pas les utilisateurs de profiter du contenu.

## <a name="htmlview-content-is-easy-to-create"></a>Le contenu HTMLView est facile à créer

Comme le nom de la fonctionnalité l’indique, vous créez un contenu Web affiché à l’aide de la fonctionnalité HTMLView à l’aide de langage HTML (HTML). Si vous avez déjà créé du contenu pour le Web, cela signifie que vous n’avez pas besoin d’apprendre un nouveau langage de programmation pour créer facilement du contenu riche avec la fonctionnalité HTMLView. si vous avez déjà des pages web avec un contrôle Lecteur Windows Media incorporé ActiveX, vous pouvez faire en sorte que ces pages s’affichent dans l’interface utilisateur du lecteur en pointant simplement sur ces pages web à partir d’un métafichier Windows Media (fichier. asx) à l’aide d’un paramètre spécial.

Lecteur Windows Media utilise une instance incorporée de Microsoft Internet Explorer pour afficher le contenu HTMLView. Cela signifie que vous n’avez pas à tenir compte de différents navigateurs Internet, de plusieurs modèles de script ou de différents langages de script lors de la création de vos pages Web. Même si l’utilisateur n’utilise pas Internet Explorer comme navigateur par défaut, votre page Web est toujours affichée correctement dans le lecteur.

il est possible qu’un programme autre que Lecteur Windows Media puisse s’inscrire en tant que programme par défaut pour ouvrir des fichiers. asx. le modèle objet série Lecteur Windows Media 9 ou version ultérieure comprend une nouvelle méthode, **openPlayer**, qui vous permet de spécifier une Uniform Resource Locator (URL) pour le contenu que vous souhaitez lire. lorsque vous utilisez la méthode **openPlayer** , Lecteur Windows Media s’ouvre toujours en mode complet pour lire le contenu spécifié. à l’aide de cette méthode, vous pouvez vous assurer que votre contenu HTMLView est affiché dans Lecteur Windows Media, plutôt qu’une autre application ayant pris en charge l’association de type de fichier. asx.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**affichage des Pages Web dans les Lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




