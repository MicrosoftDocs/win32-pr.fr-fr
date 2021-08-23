---
title: Fonctionnement des notifications
description: Fonctionnement des notifications
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e90dfeb6e1df6de50ddaa3264a8c5475d280f30a72ad2d8c6acfffd39d60fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756369"
---
# <a name="how-notifications-work"></a>Fonctionnement des notifications

Les notifications proviennent de l’application d’objet et sont acheminées vers le conteneur par le biais du gestionnaire d’objets. Si l’objet est un objet lié, l’objet lié intercepte les notifications du gestionnaire d’objets et notifie le conteneur directement.

Une application d’objet doit gérer les demandes d’inscription, en effectuant le suivi de l’emplacement des notifications et de l’envoi de ces notifications, le cas échéant. OLE fournit deux objets de composant pour simplifier cette tâche : OleAdviseHolder pour les notifications de document composé et DataAdviseHolder pour les notifications de données.

Les applications d’objet déterminent les conditions qui demandent à l’envoi de chaque notification spécifique et la fréquence à laquelle chaque notification doit être envoyée. Lorsqu’il convient d’envoyer plusieurs notifications, il n’est pas important que la notification soit envoyée en premier ; ils peuvent être envoyés dans n’importe quel ordre.

Le minutage des notifications affecte les performances et la coordination entre une application d’objet et ses conteneurs. Alors que les notifications envoyées sont trop lentes, les notifications envoyées trop rarement génèrent un conteneur hors synchronisation. La fréquence de notification peut être comparée à la fréquence à laquelle une application est redessinée. Par conséquent, l’utilisation d’une logique similaire pour le minutage des notifications (comme utilisé pour le redessin) est judicieuse.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notifications](notifications.md)
</dt> </dl>

 

 