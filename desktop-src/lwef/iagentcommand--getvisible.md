---
title: IAgentCommand GetVisible
description: IAgentCommand GetVisible
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1058c3855214dada0f1567f9fef81a3efc7e20a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381934"
---
# <a name="iagentcommandgetvisible"></a>IAgentCommand::GetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

Récupère la valeur de la propriété [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse d’une variable qui reçoit la propriété [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 