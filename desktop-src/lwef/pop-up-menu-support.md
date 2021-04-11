---
title: Prise en charge des menus contextuels
description: Prise en charge des menus contextuels
ms.assetid: a8a1cf91-c18a-497f-89a7-b47536eaca0a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890d7eab6595200cb00e8422644b10f39807bab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315036"
---
# <a name="pop-up-menu-support"></a>Prise en charge des menus contextuels

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Microsoft Agent comprend un menu contextuel (également appelé menu contextuel) pour chaque caractère. Le serveur affiche automatiquement ce menu contextuel quand un utilisateur clique avec le bouton droit sur le caractère. Vous pouvez ajouter des commandes pour votre application cliente au menu en définissant une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Pour chaque commande de la collection que vous définissez, vous pouvez spécifier la [**légende**](caption-property.md) et les propriétés [**visibles**](visible-property.md) . La **légende** est le texte qui apparaît dans le menu lorsque la propriété **visible** a la valeur **true**. Vous pouvez également utiliser la propriété [**Enabled**](enabled-property.md) pour afficher la commande dans le menu comme Disabled et [**HelpContextID**](helpcontextid-property.md) pour prendre en charge la prise en charge de l’aide pour la propriété. Définissez la touche d’accès pour le texte du menu en incluant une esperluette (&) avant le caractère de texte du paramètre de texte de la **légende** .

Le serveur ajoute automatiquement aux commandes de menu pour ouvrir la fenêtre commandes vocales et masquer le caractère ainsi que les légendes des [**commandes**](/windows/desktop/lwef/the-commands-collection-object) des autres clients du caractère pour permettre aux utilisateurs de basculer entre les clients. Le serveur ajoute automatiquement un séparateur au menu entre ses entrées de menu et celles définies par le client. Les séparateurs s’affichent uniquement lorsqu’il existe des éléments dans le menu à séparer.

Pour supprimer des commandes d’un menu, utilisez la méthode [**Remove**](remove-method.md) . Notez que les entrées de menu ne changent pas pendant que le menu s’affiche. Si vous ajoutez ou supprimez des commandes ou modifiez leurs propriétés, le menu affiche les modifications lorsque l’utilisateur réaffiche le menu.

Si vous préférez fournir vos propres services de menu contextuel pour un caractère, vous pouvez utiliser la propriété [**AutoPopupMenu**](autopopupmenu-property.md) pour désactiver la gestion du serveur de l’action de clic droit. Vous pouvez ensuite utiliser la notification d’événement [**Click**](click-event.md) pour créer votre propre comportement de gestion de menu.

Lorsque l’utilisateur sélectionne une commande dans le menu contextuel d’un caractère ou dans la fenêtre commandes vocales, le serveur déclenche l’événement de [**commande**](command-event.md) du client associé et transmet les paramètres de l’entrée à l’aide de l’objet [**UserInput**](/windows/desktop/lwef/iagentuserinput) .

Le serveur fournit également un menu contextuel pour l’icône de barre des tâches du caractère. Lorsque le caractère est visible, cliquez avec le bouton droit sur ce menu pour afficher les mêmes commandes que celles affichées en cliquant avec le bouton droit sur le caractère. Toutefois, lorsque le caractère est masqué, seules les commandes fournies par le serveur sont incluses.

 

 