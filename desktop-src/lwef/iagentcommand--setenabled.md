---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da164b6603d93496e3381ccc6938a3b6d8f520bcea887cfd11f031cec7d845a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976309"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand::SetEnabled

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Définit la propriété [**Enabled**](enabled-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Valeur booléenne qui définit la valeur du paramètre [**activé**](enabled-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object). **True** active la **commande**; **False** le désactive. Impossible de sélectionner une **commande** désactivée.

</dd> </dl>

La propriété [**Enabled**](enabled-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object) doit être définie sur **true** pour pouvoir être sélectionnée. Elle doit également avoir la propriété [**Caption**](caption-property.md) définie et sa propriété [**visible**](visible-property.md) définie sur **true** pour s’afficher dans le menu contextuel du caractère. Pour que la **commande** s’affiche dans la **fenêtre commandes vocales**, vous devez définir sa propriété [**Voice**](voice-property.md).

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 