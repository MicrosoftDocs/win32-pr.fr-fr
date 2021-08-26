---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b43a9e449e16a3be3017a67082da20cb31eb1352a81f699908b0b94267ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961819"
---
# <a name="iagentcommandsexinsertex"></a>IAgentCommandsEx::InsertEx

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

Insère un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR qui spécifie la valeur du texte de [**légende**](caption-property.md) affiché pour la [**commande**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR qui spécifie la valeur du paramètre de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR qui spécifie la valeur du texte [**VoiceCaption**](voicecaption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Expression booléenne qui spécifie le paramètre [**activé**](enabled-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object). Si le paramètre a la **valeur true**, la **commande** est activée et peut être sélectionnée. Si la **valeur est false**, la **commande** est désactivée.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Expression booléenne qui spécifie le paramètre [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object). Si le paramètre a la **valeur true**, la **commande** est visible dans le menu contextuel du caractère (si la propriété [**Caption**](caption-property.md) est également définie).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) . utilisé pour fournir une aide contextuelle pour la commande.

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

ID d’une [**commande**](/windows/desktop/lwef/the-command-object) utilisée comme référence pour l’insertion relative de la nouvelle **commande**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Expression booléenne qui spécifie où placer la [**commande**](/windows/desktop/lwef/the-command-object). Si ce paramètre a la **valeur true**, la nouvelle **commande** est insérée avant la **commande** référencée ; Si la **valeur est false**, la nouvelle **commande** est placée après la **commande** référencée.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de la [**commande**](/windows/desktop/lwef/the-command-object)insérée.

</dd> </dl>

[**IAgentCommandsEx :: InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) étend [**IAgentCommands :: Insert**](iagentcommands--insert.md) en incluant la propriété [**HelpContextID**](helpcontextid-property.md) . Vous pouvez également définir la propriété à l’aide de [ **IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx :: Addex**](iagentcommandsex--addex.md), [**IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Remove**](iagentcommands--remove.md), [**IAgentCommands :: RemoveAll**](iagentcommands--removeall.md)


 

 