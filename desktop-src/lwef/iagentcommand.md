---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c4ba90f7d355a0baa088a78aa05b7a91e14112
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106513522"
---
# <a name="iagentcommand"></a>IAgentCommand

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Un objet [**Command**](/windows/desktop/lwef/the-command-object) est un élément d’une collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Le serveur permet à l’utilisateur d’accéder à vos commandes que votre application cliente devient active. Pour récupérer une **commande**, appelez [**IAgentCommands :: GetCommand**](iagentcommands--getcommand.md).

**IAgentCommand** définit une interface qui permet aux applications de définir et d’interroger des propriétés pour les objets de [**commande**](/windows/desktop/lwef/the-command-object) qui peuvent s’afficher dans le menu contextuel d’un caractère et dans la fenêtre commandes vocales. Ces fonctions sont également disponibles à partir de [**IAgentCommandEx**](iagentcommandex.md). Un objet **Command** est un élément d’une collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Le serveur permet à l’utilisateur d’accéder à vos commandes lorsque votre application cliente devient active.

Une [**commande**](/windows/desktop/lwef/the-command-object) peut apparaître dans le menu contextuel du caractère et dans la fenêtre de commandes vocales. Pour qu’elle s’affiche dans le menu contextuel, elle doit avoir une [**légende**](caption-property.md) et la propriété [**visible**](visible-property.md) doit avoir la valeur **true**. La propriété **visible** de l’objet de collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) doit également avoir la valeur **true** pour que la commande s’affiche dans le menu contextuel lorsque votre application cliente est en entrée active. Pour apparaître dans la fenêtre commandes vocales, les propriétés [**VoiceCaption**](voicecaption-property.md) et [**Voice**](voice-property.md) doivent être définies pour une **commande** . (Pour la compatibilité descendante, s’il n’y a aucun **VoiceCaption**, le paramètre de **légende** est utilisé.)

Les entrées du menu contextuel d’un caractère ne changent pas lors de l’affichage du menu. Si vous ajoutez ou supprimez des commandes ou modifiez leurs propriétés lors de l’affichage du menu contextuel du caractère, le menu affiche ces modifications lorsqu’elles sont réaffichées. Toutefois, la fenêtre commandes vocales affiche des modifications à mesure que vous les apportez.

Le tableau suivant résume la façon dont les propriétés d’une commande affectent sa présentation.



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



 

¹ si le paramètre de la propriété est null. Dans certains langages de programmation, une chaîne vide ne peut pas être interprétée comme une chaîne NULL.

² la commande est toujours accessible en voix.

En règle générale, si vous définissez une [**commande**](/windows/desktop/lwef/the-command-object) avec un paramètre [**vocal**](voice-property.md) , vous définissez également les paramètres de [**légende**](caption-property.md) et de **voix** pour la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) associée. Si la collection **Commands** pour un ensemble de commandes n’a pas de paramètre **Voice** ou no **Caption** et est actuellement en entrée-active, mais que les **commandes** ont des paramètres de **légende** et de **voix** , les **commandes** s’affichent dans la vue de l’arborescence de la fenêtre commandes vocales sous « (commande non définie) » lorsque votre application cliente devient entrée-active.

Lorsque le serveur reçoit une entrée qui correspond à l’un des objets de [**commande**](/windows/desktop/lwef/the-command-object) que vous avez définis pour votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) , il envoie un événement [**IAgentNotifySink :: Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) et transmet l’ID de la commande en tant qu’attribut de l’objet [**IAgentUserInput**](https://www.bing.com/search?q=**IAgentUserInput**) . Vous pouvez ensuite utiliser des instructions conditionnelles pour faire correspondre et traiter la commande.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentCommand                                                   | Description                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Définit la valeur de la [**légende**](caption-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | Retourne la valeur de la propriété [**Caption**](caption-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetVoice**](iagentcommand--setvoice.md)                             | Définit la valeur du texte [**vocal**](voice-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .                        |
| [**GetVoice**](iagentcommand--getvoice.md)                             | Retourne la valeur de la propriété [**Voice**](voice-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .                   |
| [**SetEnabled**](iagentcommand--setenabled.md)                         | Définit la valeur de la propriété [**Enabled**](enabled-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | Retourne la valeur de la propriété [**Enabled**](enabled-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetVisible**](iagentcommand--setvisible.md)                         | Définit la valeur de la propriété [**visible**](visible-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | Retourne la valeur de la propriété [**visible**](visible-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | Définit la valeur de la propriété [**confidence**](confidence-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | Retourne la valeur de la propriété [**confidence**](confidence-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | Définit la valeur de la propriété [**ConfidenceText**](confidencetext-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | Retourne la valeur de la propriété [**ConfidenceText**](confidencetext-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) . |
| [**getID**](iagentcommand--getid.md)                                   | Retourne l’ID d’un objet [**Command**](/windows/desktop/lwef/the-command-object) .                                                                      |



 

 

 