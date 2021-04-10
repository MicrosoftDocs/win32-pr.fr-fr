---
title: IAgentCommands supprimer
description: IAgentCommands supprimer
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198962"
---
# <a name="iagentcommandsremove"></a>IAgentCommands :: Remove

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Supprime la [**commande**](/windows/desktop/lwef/the-command-object) spécifiée d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

ID d’une [**commande**](/windows/desktop/lwef/the-command-object) à supprimer de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

La suppression d’une [**commande**](/windows/desktop/lwef/the-command-object) d’une collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) la supprime également du menu contextuel et de la **fenêtre commandes vocales** lorsque votre application est active en entrée.

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md), [**IAgentCommands :: RemoveAll**](iagentcommands--removeall.md)


 

 