---
title: Registre IAgent
description: Registre IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f3400e6f29e62b3d8c194186f52591a0f7bb039a858c3d450e8e8332df4313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962669"
---
# <a name="iagentregister"></a>IAgent :: Register

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Inscrit un récepteur de notifications pour l’application cliente.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Adresse de [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) pour votre interface du récepteur de notifications.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

Adresse de l’ID du récepteur de notification (utilisée pour annuler l’inscription du récepteur de notification).

</dd> </dl>

Vous devez inscrire votre récepteur de notification (également appelé récepteur de notification ou récepteur d’événements) pour recevoir des événements du serveur Microsoft Agent.

## <a name="see-also"></a>Voir aussi

[**IAgent :: Unregister**](iagent--unregister.md)


 

 




