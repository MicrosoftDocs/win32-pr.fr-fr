---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292290"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput :: GetCount

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Récupère le nombre d’alternatives de [**commande**](command-event.md) passées à un rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Adresse d’une variable qui reçoit le nombre d’autres [**commandes**](command-event.md) identifiées par le serveur.

</dd> </dl>

Si l’entrée vocale n’est pas la source de la commande, par exemple, si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, **GetCount** retourne 1. Si **GetCount** retourne la valeur zéro (0), le moteur de reconnaissance vocale a détecté une entrée parlée, mais a déterminé qu’il n’y avait pas de commande correspondante.

 

 




