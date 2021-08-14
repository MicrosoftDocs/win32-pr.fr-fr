---
title: Signet IAgentNotifySink
description: Signet IAgentNotifySink
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02562b7cbf42c3445a25edc5071476da1b2d8dc53d80923ad875fddf09e5d31b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477095"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink :: Bookmark

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Avertit une application cliente lorsque son signet se termine.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*
</dt> <dd>

Identificateur du signet qui a entraîné le déclenchement de l’événement.

</dd> </dl>

Lorsque vous incluez des balises de signet dans une méthode [**Speak**](speak-method.md) , vous pouvez suivre le moment où elles se produisent avec cet événement.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: Speak**](iagentcharacter--speak.md), [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md)


 

 




