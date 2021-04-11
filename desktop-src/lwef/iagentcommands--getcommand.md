---
title: IAgentCommands GetCommand
description: IAgentCommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e81043bb8dbe8a6d050f226d09f03b396d0f8f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031231"
---
# <a name="iagentcommandsgetcommand"></a>IAgentCommands::GetCommand

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

Récupère un objet [**Command**](/windows/desktop/lwef/the-command-object) de la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

ID d’un objet [**Command**](/windows/desktop/lwef/the-command-object) dans la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Adresse de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommand**](iagentcommand.md)


 

 