---
title: Méthodes IPaperSink
description: Le présentateur expose l’interface IConnectionPointContainer afin que les clients puissent se connecter au colivre afin de recevoir des notifications d’événements spécifiés qui se produisent dans le codocument.
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8dee615b278c5214ad1efa3c10d22759620103
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199325"
---
# <a name="ipapersink-methods"></a>Méthodes IPaperSink

Le présentateur expose l’interface [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) afin que les clients puissent se connecter au colivre afin de recevoir des notifications d’événements spécifiés qui se produisent dans le codocument. En exposant cette interface, le colivre devient un objet connectable. Un client peut appeler [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour cette interface et l’utiliser pour obtenir les points de connexion de l’objet. La participation du client dans ce schéma est traitée dans l’exemple **StoClien** associé.

Fondamentalement, le client implémente ce qui est appelé récepteur sous la forme d’un objet récepteur avec une interface de récepteur. L’interface du récepteur reçoit les appels de notifications d’événements sortants du codocument une fois que le récepteur est correctement connecté par le client à une instance de codocument. Le client établit la connexion à l’aide d’un objet point de connexion qui est géré par le codocument. Il peut y avoir de nombreux points de connexion sur un seul objet COM connectable. Dans l’exemple **StoServe** , le colivre n’a qu’un seul point de connexion, qui gère le dessin des événements de papier.

Un nombre quelconque de clients peuvent se connecter à un point de connexion unique. Le \_ point de connexion CONNPOINT PAPERSINK dans le colivre gère un groupe de connexions qui peuvent croître de manière dynamique au moment de l’exécution. Les détails complets sur la prise en charge des objets connectables du codocument sont codés dans fichiers CONNECT. H et CONNECT. CPP et ne seront pas couverts ici. La construction est très similaire à ce qui a été étudié dans l’exemple de code de préservation.

Le client **StoClien** implémente les objets récepteurs appropriés pour les points de connexion qu’il s’attend à trouver dans le codocument. À partir du contexte d’un colivre, l’objet récepteur important que **StoClien** implémente expose l’interface **IPaperSink** . Il s’agit de l’interface sortante utilisée par le **StoClien** pour notifier les différents événements du colivre.

Voici un résumé des méthodes dans **IPaperSink** à partir de IPAPER. H dans le \\ répertoire frère Inc.



| Méthode   | Description                                                   |
|----------|---------------------------------------------------------------|
| Verrouillé   | Un client a pris le contrôle du papier et l’a verrouillé.           |
| Accessible | Un client a abandonné le contrôle du papier.               |
| Loaded   | Un client a chargé du contenu papier à partir de son propre fichier composé. |
| Enregistré    | Un client a enregistré du contenu papier dans son propre fichier composé.    |
| InkStart | Un client a démarré une séquence de dessin d’encre couleur sur le papier.   |
| InkDraw  | Un client met des points de données d’encre sur l’aire du papier.     |
| InkStop  | Un client a arrêté la séquence de dessin de son entrée manuscrite sur le papier.   |
| Effacé   | Un client a effacé toutes les données d’encre du papier.              |
| Redimensionné  | Un client a redimensionné le papier.                               |



 

Ces méthodes sont en grande partie explicites. Bien que le récepteur doive implémenter toutes ces méthodes d’une certaine manière, un grand nombre sont implémentées en tant que stubs et ne sont pas utilisés dans les exemples **StoServe** / **StoClien** .

Une méthode importante utilisée dans ces exemples est la méthode chargée. Lorsque le client est invité à charger un nouveau dessin à partir d’un fichier, il a besoin d’un moyen d’informer le client lorsque les nouvelles données sont chargées. Pour ce faire, le codocument appelle **IPaperSink :: Loaded** sur le récepteur client. Le client peut ensuite appeler [**IPaper :: Redraw**](ipaper--redraw.md) pour demander que le présentateur lise les nouvelles données au client. Redessine provoque la recréation du dessin chargé dans l’affichage du client. Une fois le chargement terminé, le dessin qui vient d’être chargé s’affiche automatiquement dans la fenêtre fournie par le client.

Pour obtenir des informations complètes sur la connectivité de cette méthode IPaper à **IPaperSink**, consultez [**IPaper :: Redraw**](ipaper--redraw.md) .

Les  méthodes IPaperSink **InkStart**, **InkDraw** et **InkStop** sont utilisées pour renvoyer des paquets de données d’encre au client. Lors de la réception, le client les peint dans son affichage de la même manière que lorsqu’il les a envoyés à l’origine sur le codocument. La logique ci-dessus est suffisamment générale pour permettre à plusieurs clients qui écoutent sur le même \_ point de connexion CONNPOINT PAPERSINK. Si une instance de colivre commun a été partagée par ces clients, elle peut afficher le même dessin en se connectant à ce point de connexion.

 

 