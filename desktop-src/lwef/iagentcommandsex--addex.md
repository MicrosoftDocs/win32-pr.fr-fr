---
title: IAgentCommandsEx AddEx
description: IAgentCommandsEx AddEx
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725933"
---
# <a name="iagentcommandsexaddex"></a>IAgentCommandsEx :: AddEx

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

Ajoute une [**commande**](/windows/desktop/lwef/the-command-object) à une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR qui spécifie la valeur du texte de [**légende**](caption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR qui spécifie la valeur du paramètre de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR qui spécifie la valeur du texte [**VoiceCaption**](voicecaption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Expression booléenne qui spécifie le paramètre [**activé**](enabled-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Si le paramètre a la **valeur true**, la **commande** est activée et peut être sélectionnée. Si la **valeur est false**, la **commande** est désactivée.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Expression booléenne qui spécifie le paramètre [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Si le paramètre a la **valeur true**, la **commande** est visible dans le menu contextuel du caractère (si la propriété [**Caption**](caption-property.md) est également définie).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) . utilisé pour fournir une aide contextuelle pour la commande.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de la [**commande**](/windows/desktop/lwef/the-command-object)ajoutée.

</dd> </dl>

[**IAgentCommandsEx :: Addex**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) étend [**IAgentCommands :: Add**](iagentcommands--add.md) en incluant la propriété [**HelpContextID**](helpcontextid-property.md) . Vous pouvez également définir la propriété à l’aide de [ **IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand :: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md), [**IAgentCommandsEx :: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands :: Remove**](iagentcommands--remove.md), [**IAgentCommands :: RemoveAll**](iagentcommands--removeall.md)


 

 