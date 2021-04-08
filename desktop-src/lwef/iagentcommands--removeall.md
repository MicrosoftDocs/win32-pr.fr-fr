---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727037"
---
# <a name="iagentcommandsremoveall"></a>IAgentCommands :: RemoveAll

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Remove();
```

Supprime toutes les [**commandes**](/windows/desktop/lwef/the-command-object) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

La suppression de toutes les [**commandes**](/windows/desktop/lwef/the-command-object) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) les supprime également du menu contextuel et de la **fenêtre commandes vocales** lorsque votre application est active en entrée. **RemoveAll** ne supprime pas les entrées du serveur ou d’autres clients.

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md), [**IAgentCommands :: Remove**](iagentcommands--remove.md)


 

 