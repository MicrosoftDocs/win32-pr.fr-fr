---
title: À propos de l’objet contrôles
description: À propos de l’objet contrôles
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Windows Media Player, objet Controls
- Windows Media Player Object Model, Controls (objet)
- Object Model, Controls, objet
- Contrôle ActiveX du lecteur Windows Media, objet contrôles
- Contrôle ActiveX, objet Controls
- Contrôle ActiveX mobile pour Windows Media Player, objets Controls
- Windows Media Player Mobile, objet Controls
- Controls (objet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379622"
---
# <a name="about-the-controls-object"></a><span data-ttu-id="e3ab9-111">À propos de l’objet contrôles</span><span class="sxs-lookup"><span data-stu-id="e3ab9-111">About the Controls Object</span></span>

<span data-ttu-id="e3ab9-112">L’objet **Controls** régit le transport de contenu multimédia numérique via le contrôle à l’aide de méthodes telles que **Play** et **Stop**.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-112">The **Controls** object governs the transport of digital media content through the control by using methods such as **Play** and **Stop**.</span></span> <span data-ttu-id="e3ab9-113">Elle est accessible uniquement via la propriété **Controls** de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="e3ab9-113">It is accessed only through the **Controls** property of the **Player** object.</span></span> <span data-ttu-id="e3ab9-114">La propriété **Controls** retourne l’objet **Controls** .</span><span class="sxs-lookup"><span data-stu-id="e3ab9-114">The **Controls** property returns the **Controls** object.</span></span> <span data-ttu-id="e3ab9-115">Vous pouvez uniquement accéder aux propriétés de l’objet **contrôles** après l’avoir créé.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-115">You can only access the properties of the **Controls** object after you have created it.</span></span> <span data-ttu-id="e3ab9-116">Par exemple, pour utiliser la méthode **Play** , vous devez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="e3ab9-116">For example, to use the **Play** method, you must use the following code:</span></span>


```C++
player.controls.play();

```



## <a name="related-topics"></a><span data-ttu-id="e3ab9-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3ab9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ab9-118">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-118">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="e3ab9-119">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




