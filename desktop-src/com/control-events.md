---
title: Événements de contrôle (COM)
description: En plus de fournir des propriétés et des méthodes, un contrôle fournit également des interfaces sortantes pour notifier son client d’événements.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1833e1396847e09366d1e06193196cfcf981d330
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032211"
---
# <a name="control-events-com"></a>Événements de contrôle (COM)

En plus de fournir des propriétés et des méthodes, un contrôle fournit également des interfaces sortantes pour notifier son client d’événements. Le client doit prendre en charge la gestion de ces événements. Pour plus d’informations sur le fonctionnement des objets connectables, consultez [événements dans com et objets connectables](events-in-com-and-connectable-objects.md) .

Un contrôle peut prendre en charge différentes interfaces sortantes à des fins différentes. Toutes les interfaces sortantes sont marquées comme des interfaces sources dans les informations de type du contrôle, mais une seule est marquée default pour indiquer qu’il s’agit de l’interface sortante principale.

Un conteneur peut prendre en charge une ou plusieurs des interfaces sortantes définies par un contrôle. Le contrôle doit être préparé à traiter les conteneurs qui fournissent uniquement la prise en charge de certaines de leurs interfaces sortantes.

Les contrôles prennent en charge quatre types d’événements :

-   Événements de requête. Un contrôle demande à son client l’autorisation d’effectuer une opération en appelant une méthode dans l’interface sortante, déclenchant ainsi un événement de requête. Le client signale le contrôle par le biais d’un paramètre de sortie booléen dans la méthode appelée par le contrôle. Le client peut donc empêcher le contrôle d’exécuter l’action.
-   Avant les événements. Un contrôle avertit son client Hat qu’il va effectuer une opération en appelant une méthode dans l’interface sortante, déclenchant ainsi un événement Before. Le client n’a pas la possibilité d’empêcher l’action, mais il peut prendre les mesures nécessaires en fonction de l’action qui est sur le lieu de se produire.
-   Événements After. Un contrôle notifie à son client qu’il vient d’effectuer une opération en appelant une méthode dans l’interface sortante, déclenchant ainsi un événement after. Là encore, le client ne peut pas annuler cette action, mais il peut prendre les mesures nécessaires en fonction de l’action qui s’est produite.
-   Effectuer des événements. Un contrôle déclenche un événement do pour permettre à son client de remplacer l’action du contrôle et de fournir des actions alternatives ou supplémentaires. En règle générale, la méthode appelée par un contrôle pour un événement do a un certain nombre de paramètres pour négocier avec le client les actions qui se produiront.

Les DISPID suivants sont définis pour les événements standard que les contrôles peuvent prendre en charge : Click, DblClick, keyverse, KeyPress, KeyUp, MouseMove, MouseUp et Error. Tous ces événements standard ont des valeurs DISPID négatives, indiquant leur état standard.

La méthode [**IOleControl :: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) , quand elle est appelée avec la **valeur true**, indique à un contrôle si le conteneur va prendre en charge la gestion des événements du contrôle jusqu’à ce que **FreezeEvents** soit à nouveau appelée avec **false**. Pendant cette période, le contrôle ne peut pas dépendre du conteneur qui gère réellement les événements. Si un événement doit être géré, le contrôle doit mettre l’événement en file d’attente afin de l’activer quand **FreezeEvents** est appelé avec **false**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles ActiveX](activex-controls.md)
</dt> </dl>

 

 




