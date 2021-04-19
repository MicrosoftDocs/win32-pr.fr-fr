---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511027"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a><span data-ttu-id="09ba1-103">IAgentNotifySinkEx ::D efaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="09ba1-103">IAgentNotifySinkEx::DefaultCharacterChange</span></span>

<span data-ttu-id="09ba1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09ba1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

<span data-ttu-id="09ba1-105">Avertit une application cliente lorsque le caractère par défaut change.</span><span class="sxs-lookup"><span data-stu-id="09ba1-105">Notifies a client application when the default character changes.</span></span>

-   <span data-ttu-id="09ba1-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="09ba1-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="09ba1-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span><span class="sxs-lookup"><span data-stu-id="09ba1-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="09ba1-108">Identificateur unique du caractère.</span><span class="sxs-lookup"><span data-stu-id="09ba1-108">The unique identifier for the character.</span></span>

</dd> </dl>

<span data-ttu-id="09ba1-109">Lorsque l’utilisateur modifie le caractère affecté comme caractère par défaut de l’utilisateur, le serveur envoie cet événement aux clients qui ont chargé le caractère par défaut.</span><span class="sxs-lookup"><span data-stu-id="09ba1-109">When the user changes the character assigned as the user's default character, the server sends this event to clients that have loaded the default character.</span></span> <span data-ttu-id="09ba1-110">L’événement retourne l’identificateur unique (GUID) du caractère mis en forme à l’aide d’accolades et de tirets, qui est défini lorsque le caractère est généré avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="09ba1-110">The event returns the character's unique identifier (GUID) formatted with braces and dashes, which is defined when the character is built with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="09ba1-111">Lorsque le nouveau caractère apparaît, il suppose la même taille que toute instance déjà chargée du caractère ou le caractère par défaut précédent (dans cet ordre).</span><span class="sxs-lookup"><span data-stu-id="09ba1-111">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

## <a name="see-also"></a><span data-ttu-id="09ba1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09ba1-112">See Also</span></span>

[<span data-ttu-id="09ba1-113">**IAgent :: Load**</span><span class="sxs-lookup"><span data-stu-id="09ba1-113">**IAgent::Load**</span></span>](iagent--load.md)


 

 




