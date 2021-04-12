---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309141"
---
# <a name="iagentuserinputgetitemconfidence"></a>IAgentUserInput::GetItemConfidence

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

Récupère la valeur de confiance pour une [**commande**](command-event.md) passée à un rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

L’index d’une alternative de [**commande**](command-event.md) a été passé au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*
</dt> <dd>

Adresse d’une variable qui reçoit le score de confiance pour une autre [**commande**](command-event.md) passée au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Si l’entrée vocale n’est pas la source de la commande, par exemple si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, le serveur Microsoft Agent renvoie la valeur de confiance de la meilleure correspondance comme 100 et les valeurs de confiance pour toutes les autres alternatives comme zéro (0).

## <a name="see-also"></a>Voir aussi

[**IAgentUserInput :: getItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput :: GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput :: GetItemText**](iagentuserinput--getitemtext.md)


 

 




