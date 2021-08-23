---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff4ff8e6dc87eb1a5fa5c3e79fe26b00d8bd3c8eb18a5fc6ca7cac22d3dfd07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976259"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

[**IAgentCommandsEx**](iagentcommandex.md) définit une interface qui étend l’interface [**IAgentCommands**](iagentcommands.md) .

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentCommandsEx                                                             | Description                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | Définit la commande par défaut pour le menu contextuel du caractère.                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | Retourne la commande par défaut pour le menu contextuel du caractère.                                                  |
| [**SetHelpContextID**](iagentcommandex--sethelpcontextid.md)                        | Définit l’ID de la rubrique d’aide contextuelle pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .                     |
| [**GetHelpContextID**](iagentcommandex--gethelpcontextid.md)                        | Retourne l’ID de la rubrique d’aide contextuelle pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .                  |
| [SetFontName](iagentcommandsex--setfontname.md)                                     | Définit la police à utiliser dans le menu contextuel du caractère.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Retourne la police utilisée dans le menu contextuel du caractère.                                                         |
| [SetFontSize](iagentcommandsex--setfontsize.md)                                     | Définit la taille de police à utiliser dans le menu contextuel du caractère.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Retourne la taille de police utilisée dans le menu contextuel du caractère.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Définit la légende vocale pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) du caractère.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Retourne la légende vocale de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) du caractère.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Ajoute un objet [**Command**](/windows/desktop/lwef/the-command-object) à une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Insère un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Active la grammaire vocale pour les commandes globales de l’agent.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Retourne une valeur indiquant si la grammaire vocale pour les commandes globales de l’agent est activée.                                     |



 

 

 