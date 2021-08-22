---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde65fc10a4cb467bd69f200e3244f1a2a73c0424d64f6a4babbd2cefd18e0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609259"
---
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput::GetItemID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Récupère l’identificateur d’une autre [**commande**](command-event.md) passée à un rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Index de l’alternative de [**commande**](command-event.md) passé au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID d’une [**commande**](command-event.md).

</dd> </dl>

Si l’entrée vocale déclenche le rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) , le serveur retourne les ID des [**commandes**](command-event.md) correspondantes définies par votre application.

## <a name="see-also"></a>Voir aussi

[**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput :: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput :: GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




