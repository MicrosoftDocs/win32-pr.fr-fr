---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511228"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a><span data-ttu-id="fec15-103">IAgentNotifySink::BalloonVisibleState</span><span class="sxs-lookup"><span data-stu-id="fec15-103">IAgentNotifySink::BalloonVisibleState</span></span>

<span data-ttu-id="fec15-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fec15-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

<span data-ttu-id="fec15-105">Avertit une application cliente lorsque l’état de visibilité de la bulle de texte du caractère change.</span><span class="sxs-lookup"><span data-stu-id="fec15-105">Notifies a client application when the visibility state of the character's word balloon changes.</span></span>

-   <span data-ttu-id="fec15-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fec15-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="fec15-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="fec15-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="fec15-108">Identificateur du caractère dont l’état de visibilité de l’info-bulle du mot a changé.</span><span class="sxs-lookup"><span data-stu-id="fec15-108">Identifier of the character whose word balloon's visibility state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="fec15-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="fec15-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="fec15-110">Indicateur de visibilité.</span><span class="sxs-lookup"><span data-stu-id="fec15-110">Visibility flag.</span></span> <span data-ttu-id="fec15-111">Cette valeur booléenne est **true** lorsque la bulle de texte du caractère devient visible ; et **false** lorsqu’il devient masqué.</span><span class="sxs-lookup"><span data-stu-id="fec15-111">This Boolean value is **True** when character's word balloon becomes visible; and **False** when it becomes hidden.</span></span>

</dd> </dl>

<span data-ttu-id="fec15-112">Cet événement est envoyé à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="fec15-112">This event is sent to all clients of the character.</span></span>

 

 




