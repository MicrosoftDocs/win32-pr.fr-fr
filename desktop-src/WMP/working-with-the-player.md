---
title: Utilisation du lecteur
description: Utilisation du lecteur
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Apparences du lecteur Windows Media, attribut Player en JScript
- Skins, attribut Player dans JScript
- attributs, joueur
- attribut Player
- Fichiers JScript pour les apparences, attribut Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380390"
---
# <a name="working-with-the-player"></a><span data-ttu-id="a3fa7-108">Utilisation du lecteur</span><span class="sxs-lookup"><span data-stu-id="a3fa7-108">Working with the Player</span></span>

<span data-ttu-id="a3fa7-109">Lorsque vous utilisez Microsoft JScript pour accéder aux méthodes et aux propriétés du lecteur Windows Media, vous devez utiliser le nom « Player » pour le nom du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a3fa7-109">When using Microsoft JScript to access methods and properties of Windows Media Player, you must use the name "player" for the name of the control.</span></span> <span data-ttu-id="a3fa7-110">Par exemple, pour faire référence à la méthode Stop, vous devez taper :</span><span class="sxs-lookup"><span data-stu-id="a3fa7-110">For example, to reference the Stop method, you must type:</span></span>


```C++
player.Controls.Stop()

```



<span data-ttu-id="a3fa7-111">L’attribut global **Player** est la clé permettant d’accéder au contrôle du lecteur Windows Media par le biais de scripts d’apparence.</span><span class="sxs-lookup"><span data-stu-id="a3fa7-111">The **player** global attribute is the key to accessing the Windows Media Player control through skin scripting.</span></span> <span data-ttu-id="a3fa7-112">Par le biais de cet attribut, tous les objets du contrôle du lecteur Windows Media deviennent accessibles pour la modification au moment de l’exécution par le biais de leurs propriétés et méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3fa7-112">Through this attribute, all the objects of the Windows Media Player control become accessible for run-time modification through their properties and methods.</span></span> <span data-ttu-id="a3fa7-113">En outre, l’élément **Player** est disponible pour vous permettre de spécifier des gestionnaires d’événements et l’attribut **URL** au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="a3fa7-113">Additionally, the **PLAYER** element is available so that you can specify event handlers and the **url** attribute at design time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3fa7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3fa7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3fa7-115">**Utilisation de JScript**</span><span class="sxs-lookup"><span data-stu-id="a3fa7-115">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




