---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512496"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand::GetVoice

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Récupère la valeur de la propriété de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Adresse d’un BSTR qui reçoit la propriété de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Une [**commande**](/windows/desktop/lwef/the-command-object) dont la propriété [**Voice**](voice-property.md) est définie et dont la propriété [**Enabled**](enabled-property.md) a la valeur **true** est accessible en voix. Si sa propriété [**Caption**](caption-property.md) est également définie, elle apparaît dans la fenêtre commandes vocales. Si sa propriété [**visible**](visible-property.md) a la valeur **true**, elle apparaît dans le menu contextuel du caractère.

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 