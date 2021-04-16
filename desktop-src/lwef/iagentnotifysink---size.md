---
title: Taille de IAgentNotifySink
description: Taille de IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507327"
---
# <a name="iagentnotifysinksize"></a><span data-ttu-id="e8124-103">IAgentNotifySink :: Size</span><span class="sxs-lookup"><span data-stu-id="e8124-103">IAgentNotifySink::Size</span></span>

<span data-ttu-id="e8124-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e8124-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

<span data-ttu-id="e8124-105">Avertit une application cliente lorsque le caractère a été redimensionné.</span><span class="sxs-lookup"><span data-stu-id="e8124-105">Notifies a client application when the character has been resized.</span></span>

-   <span data-ttu-id="e8124-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e8124-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="e8124-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="e8124-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="e8124-108">Identificateur du caractère qui a été redimensionné.</span><span class="sxs-lookup"><span data-stu-id="e8124-108">Identifier of the character that has been resized.</span></span>

</dd> <dt>

<span data-ttu-id="e8124-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="e8124-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="e8124-110">Largeur, en pixels, du cadre d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="e8124-110">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e8124-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="e8124-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="e8124-112">Hauteur, en pixels, du cadre d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="e8124-112">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="e8124-113">Cet événement est envoyé à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="e8124-113">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8124-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8124-114">See Also</span></span>

<span data-ttu-id="e8124-115">[**IAgentCharacter ::**](iagentcharacter--getsize.md) [ **deIAgentCharacter :: deinstalle**](iagentcharacter--setsize.md)</span><span class="sxs-lookup"><span data-stu-id="e8124-115">[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md), [**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)</span></span>


 

 




