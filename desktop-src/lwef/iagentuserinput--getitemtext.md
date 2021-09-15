---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521493"
---
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput::GetItemText

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Récupère le texte vocal pour une autre [**commande**](command-event.md) passée au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

L’index d’une alternative de [**commande**](command-event.md) a été passé au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur du texte vocal de la [**commande**](command-event.md).

</dd> </dl>

Si l’entrée vocale n’est pas la source de la commande, par exemple si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, le serveur renvoie la **valeur null** pour le texte vocal de la [**commande**](command-event.md).

## <a name="see-also"></a>Voir aussi

[**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput :: getItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput :: GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




