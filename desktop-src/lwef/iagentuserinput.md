---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381876"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Lorsque le serveur notifie le client d’entrée-actif avec [**IAgentNotifySink :: Command**](iagentnotifysink--command.md), il retourne des informations par le biais de l’objet [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) . **IAgentUserInput** définit une interface qui permet aux applications d’interroger ces valeurs.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentUserInput                                         | Description                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Retourne le nombre d’autres commandes retournées dans un événement de [**commande**](command-event.md) .                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | Retourne l’ID d’une autre [**commande**](command-event.md) spécifique.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Retourne la valeur de la propriété [**confidence**](confidence-property.md) pour une alternative de [**commande**](command-event.md) spécifique. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Retourne la valeur du texte [**vocal**](voice-property.md) pour une autre [**commande**](command-event.md) spécifique.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Retourne les données pour toutes les autres [**commandes**](command-event.md) .                                                                  |



 

 

 