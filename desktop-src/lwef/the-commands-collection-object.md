---
title: Objet de collection Commands
description: Objet de collection Commands
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f7933bd973ae500b75abb51c47899fa60322444d49fe0835f6bfa3efab97f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975659"
---
# <a name="the-commands-collection-object"></a>Objet de collection Commands

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le serveur Microsoft Agent gère une liste de commandes actuellement disponibles pour l’utilisateur. Cette liste comprend les commandes que le serveur définit pour l’interaction générale (par exemple, masquer et ouvrir la fenêtre commandes vocales), la liste des clients disponibles (mais non-entrée-active) et les commandes définies par le client actif actuel. Les deux premiers jeux de commandes sont des commandes globales ; autrement dit, elles sont disponibles à tout moment, quel que soit le client d’entrée-actif. Les commandes définies par le client ne sont disponibles que lorsque ce client est en entrée-actif et que le caractère est visible.

Chaque application cliente peut définir une collection de commandes appelée la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Pour ajouter une commande à la collection, utilisez la méthode [**Add**](add-method.md) ou [**Insert**](insert-method.md) . Bien que vous puissiez spécifier les propriétés d’une commande avec des instructions distinctes, pour optimiser les performances du code, spécifiez toutes les propriétés d’une commande dans l’instruction **Add** ou **Insert** Method. Pour chaque commande de la collection, vous pouvez déterminer si l’accès utilisateur à la commande s’affiche dans le menu contextuel du caractère, dans la fenêtre commandes vocales, dans les deux ou dans aucun des deux. Par exemple, si vous souhaitez qu’une commande apparaisse dans le menu contextuel du caractère, définissez la [**légende**](caption-property.md) et les propriétés [**visibles**](visible-property.md) de la commande. Pour afficher la commande dans la fenêtre commandes vocales, définissez les propriétés [**VoiceCaption**](voicecaption-property.md) et [**Voice**](voice-property.md) de la commande.

Un utilisateur peut accéder aux [**commandes**](/windows/desktop/lwef/the-commands-collection-object)comm individuelles ands dans votre collection uniquement lorsque votre application cliente est en entrée active. Par conséquent, lorsque vous partagez le caractère avec d’autres applications clientes, vous souhaiterez généralement définir les propriétés [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)et [**Voice**](voice-property.md) pour l’objet de collection **Commands** , ainsi que pour les commandes de la collection. Cela place une entrée pour votre collection de **commandes** dans le menu contextuel d’un caractère et dans la fenêtre commandes vocales.

Lorsque l’utilisateur bascule vers votre client en choisissant son entrée [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , le serveur rend automatiquement votre client Input-active, en avertissant votre application cliente à l’aide de l’événement [**ActivateInput**](activateinput-event.md) et rend les commandes de sa collection disponibles. Le serveur signale également au client qu’il n’est plus en cours d’entrée-actif avec l’événement [**DeActivateInput**](deactivateinput-event.md) . Cela permet au serveur de présenter et d’accepter uniquement les commandes qui s’appliquent au contexte du client d’entrée actif. Elle sert également à éviter les collisions de nom de commande entre les clients.

Un client peut également demander explicitement de se rendre lui-même le client d’entrée-actif à l’aide de la méthode [**Activate**](activate-method.md) . Cette méthode prend également en charge la configuration de votre application pour qu’elle ne soit pas le client d’entrée-actif. Vous pouvez utiliser cette méthode lorsque vous partagez un caractère avec une autre application, en définissant votre application de sorte qu’elle soit en entrée-active quand votre fenêtre d’application devient active et non active quand elle perd le focus.

De même, vous pouvez utiliser la méthode [**Activate**](activate-method.md) pour définir votre application comme étant (ou non) le client actif du caractère. Le client actif est le client qui reçoit l’entrée lorsque son caractère est le caractère le plus haut. Lorsque cet état change, le serveur notifie votre application avec l’événement [**ActiveClientChange**](activeclientchange-event.md) .

Lorsque le menu contextuel d’un caractère s’affiche, les modifications apportées aux propriétés d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) ou aux commandes de sa collection ne s’affichent pas tant que l’utilisateur n’a pas réaffiché le menu. Toutefois, la fenêtre commandes affiche des modifications à mesure qu’elles se produisent.

-   [Méthodes de l’objet Commands](commands-object-methods.md)
-   [Propriétés de l’objet Commands](commands-object-properties.md)

 

 