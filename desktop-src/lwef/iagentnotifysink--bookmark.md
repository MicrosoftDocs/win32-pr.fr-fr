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
# <a name="iagentnotifysinkbookmark"></a><span data-ttu-id="45807-103">IAgentNotifySink :: Bookmark</span><span class="sxs-lookup"><span data-stu-id="45807-103">IAgentNotifySink::Bookmark</span></span>

<span data-ttu-id="45807-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="45807-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

<span data-ttu-id="45807-105">Avertit une application cliente lorsque son signet se termine.</span><span class="sxs-lookup"><span data-stu-id="45807-105">Notifies a client application when its bookmark completes.</span></span>

-   <span data-ttu-id="45807-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="45807-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="45807-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span><span class="sxs-lookup"><span data-stu-id="45807-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span></span>
</dt> <dd>

<span data-ttu-id="45807-108">Identificateur du signet qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="45807-108">Identifier of the bookmark that resulted in triggering the event.</span></span>

</dd> </dl>

<span data-ttu-id="45807-109">Lorsque vous incluez des balises de signet dans une méthode [**Speak**](speak-method.md) , vous pouvez suivre le moment où elles se produisent avec cet événement.</span><span class="sxs-lookup"><span data-stu-id="45807-109">When you include bookmark tags in a [**Speak**](speak-method.md) method, you can track when they occur with this event.</span></span>

## <a name="see-also"></a><span data-ttu-id="45807-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45807-110">See Also</span></span>

<span data-ttu-id="45807-111">[**IAgentCharacter :: Speak**](iagentcharacter--speak.md), [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md)</span><span class="sxs-lookup"><span data-stu-id="45807-111">[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md)</span></span>


 

 




