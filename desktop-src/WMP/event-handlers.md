---
title: Gestionnaires d'événements
description: Gestionnaires d'événements
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Apparences du lecteur Windows Media, gestionnaires d’événements dans JScript
- apparences, gestionnaires d’événements dans JScript
- événements, JScript
- Fichiers JScript pour les apparences, gestionnaires d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517935"
---
# <a name="event-handlers"></a><span data-ttu-id="b69ce-107">Gestionnaires d'événements</span><span class="sxs-lookup"><span data-stu-id="b69ce-107">Event Handlers</span></span>

<span data-ttu-id="b69ce-108">Microsoft JScript est utilisé pour traiter les événements dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="b69ce-108">Microsoft JScript is used to process events in the skin definition file.</span></span> <span data-ttu-id="b69ce-109">Pour plus d’informations sur les gestionnaires d’événements, consultez [gestion des événements](handling-events.md) .</span><span class="sxs-lookup"><span data-stu-id="b69ce-109">See [Handling Events](handling-events.md) for more information about event handlers.</span></span>

<span data-ttu-id="b69ce-110">Vous pouvez avoir plusieurs lignes de code dans un gestionnaire d’événements, mais vous devez veiller à ne pas dépasser la longueur de ligne autorisée par JScript.</span><span class="sxs-lookup"><span data-stu-id="b69ce-110">You can have more than one line of code in an event handler, but care must be taken not to exceed the line length that JScript permits.</span></span> <span data-ttu-id="b69ce-111">Séparez les lignes par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="b69ce-111">Separate the lines by semicolons.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a><span data-ttu-id="b69ce-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b69ce-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b69ce-113">**Utilisation de JScript**</span><span class="sxs-lookup"><span data-stu-id="b69ce-113">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




