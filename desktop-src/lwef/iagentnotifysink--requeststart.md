---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d208e732a2e53d574c74f1a6f0b49aa7550b10343f1ed3b8b7348ed798363c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450479"
---
# <a name="iagentnotifysinkrequeststart"></a>IAgentNotifySink::RequestStart

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

Avertit une application cliente qu’une demande commence.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

Identificateur de la demande qui a démarré.

</dd> </dl>

Cet événement vous permet de suivre le moment où une demande en file d’attente commence à utiliser son ID de demande.

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySink :: RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent :: Load**](iagent--load.md), [**IAgentCharacter :: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter :: Hide**](iagentcharacter--hide.md), [**IAgentCharacter :: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter :: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter ::P**](iagentcharacter--prepare.md)res, [**IAgentCharacter ::P poser**](iagentcharacter--play.md), [**IAgentCharacter :: Show**](iagentcharacter--show.md), [**IAgentCharacter :: Speak**](iagentcharacter--speak.md), [**IAgentCharacter :: wait**](iagentcharacter--wait.md)


 

 




