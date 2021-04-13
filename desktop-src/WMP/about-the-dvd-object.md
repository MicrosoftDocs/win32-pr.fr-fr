---
title: À propos de l’objet DVD
description: À propos de l’objet DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Lecteur Windows Media, objet DVD
- Modèle objet lecteur Windows Media, objet DVD
- modèle objet, objet DVD
- Contrôle ActiveX du lecteur Windows Media, objet DVD
- Contrôle ActiveX, objet DVD
- Contrôle ActiveX mobile du lecteur Windows Media, objet DVD
- Windows Media Player Mobile, objet DVD
- Objet DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309302"
---
# <a name="about-the-dvd-object"></a><span data-ttu-id="22020-111">À propos de l’objet DVD</span><span class="sxs-lookup"><span data-stu-id="22020-111">About the DVD Object</span></span>

<span data-ttu-id="22020-112">L’objet **DVD** ajoute des fonctionnalités spécifiques au support DVD.</span><span class="sxs-lookup"><span data-stu-id="22020-112">The **DVD** object adds functionality specific to DVD media.</span></span> <span data-ttu-id="22020-113">Dans un sens général, les DVD sont traités comme d’autres médias numériques dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22020-113">In a general sense, DVD media is treated just like other digital media in Windows Media Player.</span></span> <span data-ttu-id="22020-114">Par exemple, les lecteurs de DVD sont énumérés à l’aide de l’objet **CdromCollection** et les titres des DVD et les chapitres sont manipulés à l’aide des objets de **sélection** et des objets **multimédias** .</span><span class="sxs-lookup"><span data-stu-id="22020-114">For instance, DVD drives are enumerated using the **CdromCollection** object and DVD titles and chapters are manipulated using **Playlist** objects and **Media** objects.</span></span> <span data-ttu-id="22020-115">Toutefois, certaines fonctionnalités sont spécifiques aux DVD et l’objet **DVD** en fournit.</span><span class="sxs-lookup"><span data-stu-id="22020-115">Some functionality is DVD-specific, however, and the **DVD** object provides this.</span></span> <span data-ttu-id="22020-116">Par exemple, le DVD a un concept appelé domaine.</span><span class="sxs-lookup"><span data-stu-id="22020-116">For example, DVD has a concept called domain.</span></span> <span data-ttu-id="22020-117">Pour récupérer le domaine actuel pour un support DVD, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="22020-117">To retrieve the current domain for DVD media, type the following:</span></span>


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a><span data-ttu-id="22020-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22020-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22020-119">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="22020-119">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="22020-120">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="22020-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




