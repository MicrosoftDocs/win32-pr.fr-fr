---
title: Fonctionnement des notifications
description: Fonctionnement des notifications
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382991"
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

 

 