---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1bcc40f80e9a10301ec305fdc3e8f3e83984ceb0de5d36121e13c3d823b8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961889"
---
# <a name="iagentcommands"></a>IAgentCommands

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le serveur Microsoft Agent gère une liste de commandes actuellement disponibles pour l’utilisateur. Cette liste comprend les commandes que le serveur définit pour les interactions générales, telles que les propriétés Hide et Microsoft Agent, la liste des clients disponibles (mais non-en entrée) et les commandes définies par le client actif actuel. Les deux premiers jeux de commandes sont des commandes globales ; autrement dit, elles sont disponibles à tout moment, quel que soit le client d’entrée-actif. Les commandes définies par le client ne sont disponibles que lorsque le client est en entrée-actif.

Récupérez une interface **IAgentCommands** en interrogeant l’interface [**IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**) pour **IAgentCommands**. Chaque application cliente Microsoft Agent peut définir une collection de commandes appelée une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Pour ajouter une [**commande**](/windows/desktop/lwef/the-command-object) à la collection, utilisez la méthode [**Add**](add-method.md) ou [**Insert**](insert-method.md) . Bien que vous puissiez spécifier les propriétés **d’une commande** à l’aide des méthodes [**IAgentCommand**](iagentcommand.md) , pour optimiser les performances du code, spécifiez toutes les propriétés d’une **commande** dans les méthodes [**IAgentCommands :: Add**](iagentcommands--add.md) ou [**IAgentCommands :: Insert**](iagentcommands--insert.md) lors de la définition initiale des propriétés d’une nouvelle **commande**. Vous pouvez utiliser les méthodes **IAgentCommand** pour interroger ou modifier les paramètres de propriété.

Pour chaque [**commande**](/windows/desktop/lwef/the-command-object) de la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , vous pouvez déterminer si la commande apparaît dans le menu contextuel du caractère, dans la fenêtre commandes vocales, dans les deux ou dans aucun des deux. Par exemple, si vous souhaitez qu’une commande apparaisse dans le menu contextuel du caractère, définissez la [**légende**](caption-property.md) et les propriétés [**visibles**](visible-property.md) de la commande. Pour afficher la commande dans la **fenêtre commandes vocales**, définissez la **légende** et les propriétés [**vocales**](voice-property.md) de la commande.

Un utilisateur peut accéder aux commandes individuelles de votre collection de commandes uniquement lorsque votre application cliente est en entrée-active et que le caractère est visible. Par conséquent, vous souhaiterez généralement définir les propriétés [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)et [**Voice**](voice-property.md) pour l’objet de collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , ainsi que pour les commandes de la collection, car cette opération place une entrée pour votre collection **Commands** dans le menu contextuel d’un caractère et dans la fenêtre commandes vocales. Lorsque l’utilisateur bascule vers votre client en choisissant son entrée **Commands** , le serveur rend automatiquement votre client Input-active, en avertissant votre application cliente à l’aide de [**IAgentNotifySink :: ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) et rend les **commandes** de sa collection disponibles. Le serveur notifie également le client qui n’est plus en entrée-actif avec l’événement **IAgentNotifySink :: ActivateInputState** . Cela permet au serveur de présenter et d’accepter uniquement les **commandes** qui s’appliquent au contexte du client d’entrée actif. Elle sert également à éviter les collisions de nom de [**commande**](/windows/desktop/lwef/the-command-object)entre les clients.

Un client peut également demander explicitement de se rendre lui-même le client d’entrée-actif à l’aide de la méthode [**IAgentCharacter :: Activate**](iagentcharacter--activate.md) . Cette méthode prend également en charge la configuration de votre application pour qu’elle ne soit pas le client d’entrée-actif. Vous pouvez utiliser cette méthode lors du partage d’un caractère avec une autre application, en définissant votre application pour qu’elle soit en entrée-active lorsque votre fenêtre d’application devient active et non active quand elle perd le focus.

De même, vous pouvez utiliser [**IAgentCharacter :: Activate**](iagentcharacter--activate.md) pour définir votre application en tant que client actif du caractère. Le client actif est le client qui reçoit l’entrée lorsque son caractère est le caractère le plus haut. Lorsque cet état change, le serveur notifie votre application avec l’événement [**IAgentNotifySinkEx :: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md) .

Lorsque le menu contextuel d’un caractère s’affiche, les modifications apportées aux propriétés d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) ou aux commandes de sa collection ne s’affichent pas tant que l’utilisateur n’a pas réaffiché le menu. Toutefois, lorsqu’elle est ouverte, la fenêtre commandes vocales affiche les modifications à mesure qu’elles se produisent.

**IAgentCommands** définit une interface qui permet aux applications d’ajouter, de supprimer, de définir et d’interroger les propriétés d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Ces fonctions sont également disponibles à partir de [**IAgentCommandsEx**](iagentcommandsex.md).

Une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) peut apparaître sous la forme d’une commande dans le menu contextuel et dans la fenêtre commandes vocales pour un caractère. Pour que la collection de **commandes** s’affiche, vous devez définir sa propriété [**Caption**](caption-property.md) . Le tableau suivant résume la façon dont les propriétés d’une collection de **commandes** affectent sa présentation.



| Propriété Caption | Voice-Caption, propriété | Voice, propriété | Propriété visible | Apparaît dans le menu contextuel du caractère             | Apparaît dans la fenêtre commandes vocales                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Oui              | Oui                    | Oui            | Vrai             | Oui, à l’aide de la [ **légende**](caption-property.md) | Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md) |
| Oui              | Oui                    | Non ¹            | Vrai             | Oui, à l’aide de la [ **légende**](caption-property.md) | Non                                                       |
| Oui              | Oui                    | Oui            | False            | Non                                             | Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md) |
| Oui              | Oui                    | Non ¹            | False            | Non                                             | Non                                                       |
| Non ¹              | Oui                    | Oui            | True             | Non                                             | Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md) |
| Non ¹              | Oui                    | Oui            | False            | Non                                             | Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md) |
| Non ¹              | Oui                    | Non ¹            | True             | Non                                             | Non                                                       |
| Non ¹              | Oui                    | Non ¹            | False            | Non                                             | Non                                                       |
| Oui              | Non ¹                    | Oui            | Vrai             | Oui, à l’aide de la [ **légende**](caption-property.md) | Oui, à l’aide de la [ **légende**](caption-property.md)           |
| Oui              | Non ¹                    | Non ¹            | True             | Oui                                            | Non                                                       |
| Oui              | Non ¹                    | Oui            | False            | Non                                             | Oui, à l’aide de la [ **légende**](caption-property.md)           |
| Oui              | Non ¹                    | Non ¹            | False            | Non                                             | Non                                                       |
| Non ¹              | Non ¹                    | Oui            | True             | Non                                             | Non²                                                      |
| Non ¹              | Non ¹                    | Oui            | False            | Non                                             | Non²                                                      |
| Non ¹              | Non ¹                    | Non ¹            | True             | Non                                             | Non                                                       |
| Non ¹              | Non ¹                    | Non ¹            | False            | Non                                             | Non                                                       |



 

¹ si le paramètre de la propriété est null. Dans certains langages de programmation, une chaîne vide ne peut pas être interprétée de la même façon qu’une chaîne NULL.

² la commande est toujours accessible en voix.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentCommands                           | Description                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Récupère un objet [**Command**](/windows/desktop/lwef/the-command-object) de la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .              |
| [**GetCount**](iagentcommands--getcount.md)     | Retourne la valeur du nombre de [**commandes**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . |
| [**SetCaption**](iagentcommands--setcaption.md) | Définit la valeur de la propriété [**Caption**](caption-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetCaption**](iagentcommands--getcaption.md) | Retourne la valeur de la propriété [**Caption**](caption-property.md) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**SetVoice**](iagentcommands--setvoice.md)     | Définit la valeur de la propriété [**Voice**](voice-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .        |
| [**GetVoice**](iagentcommands--getvoice.md)     | Retourne la valeur de la propriété [**Voice**](voice-property.md) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .      |
| [**SetVisible**](iagentcommands--setvisible.md) | Définit la valeur de la propriété [**visible**](visible-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetVisible**](iagentcommands--getvisible.md) | Retourne la valeur de la propriété [**visible**](visible-property.md) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**Ajouter**](iagentcommands--add.md)               | Ajoute un objet [**Command**](/windows/desktop/lwef/the-command-object) à une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .                       |
| [**Insérer**](iagentcommands--insert.md)         | Insère un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**Installez**](iagentcommands--remove.md)         | Supprime un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | Supprime tous les objets de [**commande**](/windows/desktop/lwef/the-command-object) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .               |



 

 

 