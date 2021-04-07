---
title: À propos de l’objet réseau
description: À propos de l’objet réseau
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Lecteur Windows Media, objet réseau
- Modèle objet du lecteur Windows Media, objet réseau
- modèle objet, objet réseau
- Contrôle ActiveX du lecteur Windows Media, objet réseau
- Contrôle ActiveX, objet réseau
- Contrôle ActiveX Windows Media Player Mobile, objet réseau
- Windows Media Player Mobile, objet réseau
- Objet réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671401"
---
# <a name="about-the-network-object"></a><span data-ttu-id="aae61-111">À propos de l’objet réseau</span><span class="sxs-lookup"><span data-stu-id="aae61-111">About the Network Object</span></span>

<span data-ttu-id="aae61-112">L’objet **réseau** régit les propriétés qui vous permettent de déterminer le degré de diffusion du contenu sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="aae61-112">The **Network** object governs the properties that allow you to determine how well the content is streaming through the network.</span></span> <span data-ttu-id="aae61-113">Par exemple, vous pouvez déterminer si les paquets sont perdus et prendre les mesures appropriées.</span><span class="sxs-lookup"><span data-stu-id="aae61-113">For example, you can find out whether packets are being lost and take appropriate action.</span></span> <span data-ttu-id="aae61-114">L’objet **réseau** est accessible uniquement par le biais de la propriété **réseau** de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="aae61-114">The **Network** object is accessed only through the **network** property of the **Player** object.</span></span> <span data-ttu-id="aae61-115">La propriété **Network** retourne l’objet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="aae61-115">The **network** property returns the **Network** object.</span></span> <span data-ttu-id="aae61-116">Vous pouvez uniquement accéder aux propriétés de l’objet **réseau** après l’avoir créé.</span><span class="sxs-lookup"><span data-stu-id="aae61-116">You can only access the properties of the **Network** object after you have created it.</span></span> <span data-ttu-id="aae61-117">Par exemple, pour utiliser la propriété **Bandwidth** , vous devez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="aae61-117">For example, to use the **Bandwidth** property, you must use the following code:</span></span>


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a><span data-ttu-id="aae61-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aae61-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aae61-119">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="aae61-119">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="aae61-120">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="aae61-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




