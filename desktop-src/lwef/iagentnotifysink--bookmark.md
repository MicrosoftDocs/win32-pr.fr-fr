---
title: Signet IAgentNotifySink
description: Signet IAgentNotifySink
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672406"
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


 

 




