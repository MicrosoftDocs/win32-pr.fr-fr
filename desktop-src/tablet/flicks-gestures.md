---
description: Windows Vista comprend un ensemble de huit mouvements de raccourci de base. Les raccourcis sont des mouvements de stylet rapides et linéaires associés aux commandes et actions de défilement.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Mouvements de raccourcis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85d519f47b265779741b2f98fcb1b2f5d69df5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554749"
---
# <a name="flicks-gestures"></a>Mouvements de raccourcis

Windows Vista comprend un ensemble de huit *mouvements de raccourci* de base. Les raccourcis sont des mouvements de stylet rapides et linéaires associés aux commandes et actions de défilement.

## <a name="flick-details"></a>Détails du raccourci

La fonctionnalité de raccourcis fournit à l’utilisateur une nouvelle façon d’interagir avec le Tablet PC en autorisant des actions courantes à effectuer en effectuant des mouvements rapides avec le stylet. Les raccourcis coexistent avec et n’interrompent pas les actions normales de l’utilisateur, telles que les robinets gauche et droit, le défilement et l’écriture manuscrite.

Un *raccourci* est un mouvement de stylet unidirectionnel qui requiert que l’utilisateur contacte le digitaliseur dans un mouvement de raccourci rapide. Un raccourci est caractérisé par une vitesse élevée et un degré élevé d’angles. Un raccourci est identifié par sa direction. Les raccourcis peuvent être effectués dans huit directions correspondant aux directions cardinales et secondaires de la boussole.

Une *action ou une* *action* de raccourci est l’action ou le raccourci exécuté en réponse à un raccourci. Les raccourcis sont mappés à des actions. L’illustration suivante montre un diagramme de huit raccourcis stylet qui correspondent à leurs actions de raccourci.

![Illustration montrant le mappage de mouvement](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

Lorsque l’utilisateur déplace le stylet sur le digitaliseur d’un Tablet PC, le matériel génère des paquets de stylet qui sont routés vers le sous-système d’entrée de stylet de la plateforme Tablet PC. Normalement, si le stylet est utilisé comme substitut de la souris, le sous-système d’entrée de stylet utilise ces paquets Pen et les envoie, éventuellement avec des modifications, à User32, le composant Windows responsable du traitement de l’entrée de souris. Si le stylet est utilisé sur une surface d’encrage, l’encre est rendue au lieu de générer des paquets de souris.

La routine de détection de mouvement est implémentée dans le sous-système d’entrée Pen. La détection du raccourci commence au stylet et continue jusqu’à ce que :

1) la séquence de paquets reçus est déterminée comme n’étant pas un raccourci ou

2) le stylet s’affiche.

Pendant que la détection de mouvement se produit, les paquets de stylet sont retenus et ne sont pas envoyés au système. Cela doit être fait car l’envoi de paquets peut interférer avec l’action de raccourci effectuée. Par exemple, l’envoi de paquets au cours d’un raccourci qui mappe à une action de copie fait disparaître ce qui a été sélectionné, ce qui signifie qu’il n’y aura rien à copier lors de l’envoi de l’action.

À mesure que les paquets sont acheminés dans le sous-système d’entrée de stylet, la routine de détection de mouvement calcule les mesures sur la longueur, la vélocité, le temps et la courbure du mouvement en cours d’exécution. Avec chaque paquet qui arrive, la routine de détection met à jour chacune de ces métriques. Dès que l’une des mesures se situe en dehors de ce qui constituerait un raccourci, la détection de mouvement se termine et les paquets sont envoyés via.

## <a name="where-flicks-are-detected"></a>Détection des raccourcis

Les mouvements de raccourcis sont rendus possibles par le fait que les opérations de glisser-déplacer sont généralement effectuées de façon lente. L’utilisateur doit d’abord cibler le point de départ du glissement, effectuer le glissement, puis cibler le point de terminaison. Normalement, cette opération prend trop de temps pour être considérée comme un raccourci. Toutefois, sur les surfaces d’encrage, les traits rapides qui sont qualifiés comme raccourcis se produisent fréquemment. le franchissement d’un « t » est un exemple courant. Par conséquent, par défaut, la détection de mouvement est désactivée sur les surfaces d’encrage et activée à l’ensemble du système.

## <a name="focus-issues"></a>Problèmes de focus

Une fois qu’un mouvement de raccourci a été détecté, une séquence d’événements commence par entraîner l’exécution par le système d’une action spécifique en réponse au raccourci qui s’est produit. Tout d’abord, la routine de détection dans le sous-système d’entrée du stylet détermine la fenêtre à laquelle le raccourci doit être envoyé. Il s’agit généralement de la fenêtre qui a le focus, mais il existe des exceptions. Pour les raccourcis de défilement, le raccourci est envoyé à la fenêtre sur laquelle le raccourci s’est produit. Notez qu’il ne s’agit pas nécessairement de la fenêtre qui a le focus. Lorsqu’un raccourci est envoyé à une fenêtre qui n’a pas le focus, le focus ne passe pas à cette fenêtre.

## <a name="flick-actions"></a>Actions de raccourci

Une fois la fenêtre cible déterminée, cette fenêtre peut gérer le raccourci lui-même en fonction du comportement de l’événement programmé ou par défaut. Les applications peuvent répondre à l’action qui est la plus appropriée en fonction de l’application et de la direction et de la position du raccourci. Par exemple, dans une application de mappage, les raccourcis vers le haut et vers le haut peuvent effectuer un zoom avant ou arrière au lieu de faire défiler verticalement, comme le ferait le comportement par défaut.

Pour avertir une application qu’un raccourci s’est produit, un message de fenêtre lui est envoyé. Ce message de fenêtre contient à la fois le point de départ du raccourci et le sens du raccourci. Si l’application gère ce message de fenêtre, aucune action supplémentaire n’est effectuée par le sous-système d’entrée du stylet.

Une fois le raccourci détecté, un commentaire visuel représentant l’action de raccourci est affiché à l’écran. Ce feedback a deux objectifs. Tout d’abord, il confirme à l’utilisateur que le mouvement a réussi. Deuxièmement, il rappelle à l’utilisateur quelle action a été effectuée, aidant l’utilisateur à connecter la direction du raccourci avec l’action qui lui est associée.

Les commentaires du raccourci sont constitués de deux parties : icône représentant l’action et une étiquette contenant le nom de l’action. L’étiquette s’affiche sous l’icône. Les commentaires s’affichent immédiatement après la détection du raccourci. Bien que les applications puissent personnaliser leur comportement en réponse aux raccourcis en gérant le message de fenêtre de raccourci, l’application ne peut pas désactiver ou modifier les commentaires du raccourci.

Il est prévu que la plupart des applications ne soient pas compatibles avec le scintillement et ne gère donc pas le message de fenêtre décrit ci-dessus. Si le message n’est pas géré, le sous-système d’entrée de stylet effectue une action supplémentaire. Tout d’abord, il recherche l’action associée à la direction du raccourci détecté. Ensuite, il prend des mesures (décrites dans le tableau ci-dessous) pour faire en sorte que la fenêtre cible effectue cette action. Pour la plupart des actions de raccourci, cela implique l’envoi d’une commande d’application, mais certaines actions implémentées ne le sont pas.

## <a name="processing-application-commands"></a>Traitement des commandes de l’application

Votre application doit répondre à toutes les commandes de l’application qui pourraient être potentiellement affectées à un mouvement de raccourci. Si une application ne parvient pas à répondre au [**\_ message de \_ scintillement de tablette WM**](wm-tablet-flick-message.md), Windows Vista suit en envoyant la notification [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand) applicable, suivie d’une notification [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown) .

La liste suivante répertorie les commandes d’application qui peuvent être assignées aux raccourcis, avec le message de séquence de touches de sauvegarde qui peut être envoyé.



| Commande                                  | Séquence de touches de sauvegarde  |
|------------------------------------------|-------------------|
| navigateur APPCOMMAND vers l' \_ \_ arrière<br/> | Aucun<br/>   |
| APPCOMMAND \_ navigateur \_ suivant<br/>  | Aucun<br/>   |
| \_copie APPCOMMAND<br/>              | Ctrl+C<br/> |
| APPCOMMAND \_ coller<br/>             | Ctrl+V<br/> |
| APPCOMMAND \_ Annuler<br/>              | Ctrl+Z<br/> |
| APPCOMMAND \_ Supprimer<br/>            | Suppr<br/>    |
| APPCOMMAND \_ couper<br/>               | Ctrl+X<br/> |
| APPCOMMAND \_ ouvrir<br/>              | Ctrl+O<br/> |
| \_Imprimer APPCOMMAND<br/>             | Ctrl+P<br/> |
| APPCOMMAND \_ Enregistrer<br/>              | Ctrl+S<br/> |
| APPCOMMAND \_ rétablir<br/>              | Ctrl+Y<br/> |
| APPCOMMAND \_ Fermer<br/>             |                   |



 

Les commandes de modification telles que copier, coller, couper et supprimer peuvent être dirigées vers une sélection ou sur l’objet situé à la base du mouvement de raccourci. Si aucune sélection n’est effectuée, vous pouvez utiliser les données de [**la \_ structure du point de mouvement**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) pour déterminer l’objet, le cas échéant, qui peut avoir été la cible de la commande d’édition.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur l’API raccourcis](flicks-api-reference.md)
</dt> <dt>

[Réponse aux mouvements de raccourcis](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

