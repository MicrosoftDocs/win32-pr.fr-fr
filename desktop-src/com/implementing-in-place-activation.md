---
title: Implémentation de l’activation In-Place
description: Implémentation de l’activation In-Place
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c075f143c772fe34de0c494664227e892b998387
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998910"
---
# <a name="implementing-in-place-activation"></a>Implémentation de l’activation In-Place

L’activation sur place permet à un utilisateur d’interagir avec un objet incorporé sans quitter le document conteneur. Lorsqu’un utilisateur active l’objet, une *barre de menus composite* comprenant des éléments des barres de menus de l’application de conteneur et de l’application serveur remplace la barre de menus principale du conteneur. Les commandes et les fonctionnalités des deux applications sont donc disponibles pour l’utilisateur, y compris l’aide contextuelle pour l’objet actif. Lorsqu’un utilisateur commence à travailler avec une partie non-objet du document, l’objet est désactivé, ce qui amène le menu d’origine du document conteneur à remplacer le menu composite.

Cette fonctionnalité s’est déroulée à l’origine par le nom de la *modification sur place*. Le nom a été modifié, car la modification n’est qu’une des méthodes permettant à un utilisateur d’interagir avec un objet en cours d’exécution. Par exemple, les clips sonores peuvent être écoutés au lieu d’être modifiés. Les clips vidéo peuvent être affichés au lieu d’être modifiés. L’activation sur place est particulièrement prévue dans le cas de clips vidéo, car elle leur permet de s’exécuter en place, sans appeler une fenêtre distincte. Cela peut être critique si la vidéo devait être affichée, par exemple avec des données texte adjacentes dans le document conteneur.

L’implémentation de l’activation sur place est strictement facultative pour les applications conteneur et serveur. OLE prend toujours en charge le modèle dans lequel l’activation d’un objet entraîne l’ouverture d’une fenêtre distincte par l’application serveur. Les objets liés s’ouvrent toujours dans une fenêtre distincte pour souligner qu’ils se trouvent dans un document distinct.

L’activation sur place commence par l’objet en réponse à un appel à [**IOleObject ::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) à partir de son conteneur. Cet appel se produit généralement en réponse à un utilisateur qui double-clique sur l’objet ou sélectionne une commande (verbe) dans le menu Edition de l’application conteneur.

La fenêtre sur place reçoit l’entrée du clavier et de la souris pendant que l’objet incorporé est actif. Quand un utilisateur sélectionne des commandes à partir de la barre de menus composite, la commande et les messages de menu associés sont envoyés à l’application conteneur ou objet, en fonction de l’élément qui possède le menu déroulant particulier sélectionné. Les entrées à l’aide des règles, des barres d’outils ou des ornements de cadre d’un objet accèdent directement à l’objet incorporé, qui possède ces fenêtres.

Un objet incorporé activé sur place reste actif jusqu’à ce que le conteneur le désactive en réponse à l’entrée utilisateur ou que l’objet abandonne volontairement l’état actif, comme un clip vidéo peut le faire, par exemple. Un utilisateur peut désactiver un objet en cliquant dans le document conteneur, mais en dehors de la fenêtre d’activation sur place de l’objet, ou simplement en cliquant sur un autre objet. Toutefois, un objet activé sur place reste actif si l’utilisateur clique sur la barre de titre du conteneur, sur la barre de défilement ou, en particulier, sur la barre de menus.

Vous pouvez implémenter un serveur d’objets d’activation en place en tant que serveur in-process (DLL) ou serveur local (EXE). Dans les deux cas, la barre de menus composite contient des éléments (généralement des menus déroulants) des processus serveur et conteneur. Dans le cas d’un serveur in-process, la fenêtre d’activation sur place est simplement une autre fenêtre enfant dans la hiérarchie de fenêtre du conteneur, en recevant son entrée via la pompe de messages de l’application conteneur.

Dans le cas d’un serveur local, la fenêtre d’activation sur place appartient au processus d’application serveur de l’objet incorporé, mais sa fenêtre parente appartient au conteneur. L’entrée de la fenêtre d’activation sur place apparaît dans la file d’attente de messages du serveur et est distribuée par la boucle de message du serveur. Les bibliothèques OLE sont chargées de s’y voir que les commandes de menu et les messages sont distribués correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> </dl>

 

 




