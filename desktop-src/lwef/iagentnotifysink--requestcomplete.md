---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c797232ca968261c5857bec8953c6c76375bafc849b17ebe21bc8f353698f02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976169"
---
# <a name="iagentnotifysinkrequestcomplete"></a>IAgentNotifySink::RequestComplete

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

Avertit une application cliente quand une demande est terminée.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

Identificateur de la demande qui a démarré.

</dd> <dt>

<span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*
</dt> <dd>

Code d’état. Ce paramètre retourne le code d’état de la demande.

</dd> </dl>

Cet événement vous permet de suivre le moment où une méthode en file d’attente se termine à l’aide de son ID de demande.

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySink :: RequestStart**](iagentnotifysink--requeststart.md), [**IAgent :: Load**](iagent--load.md), [**IAgentCharacter :: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter :: Hide**](iagentcharacter--hide.md), [**IAgentCharacter :: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter :: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter ::P**](iagentcharacter--prepare.md)res, [**IAgentCharacter ::P poser**](iagentcharacter--play.md), [**IAgentCharacter :: Show**](iagentcharacter--show.md), [**IAgentCharacter :: Speak**](iagentcharacter--speak.md), [**IAgentCharacter :: wait**](iagentcharacter--wait.md)


 

 




