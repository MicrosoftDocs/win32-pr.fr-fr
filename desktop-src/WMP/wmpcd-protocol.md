---
title: Protocole WMPCD
description: Protocole WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Lecteur Windows Media, protocoles
- Modèle d’objet du lecteur Windows Media, protocoles
- modèle objet, protocoles
- Contrôle ActiveX du lecteur Windows Media, protocoles pour le modèle objet
- Contrôle ActiveX, protocoles pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, protocoles pour le modèle objet
- Windows Media Player Mobile, protocoles pour le modèle objet
- protocoles, modèle objet du lecteur Windows Media
- protocoles, WMPCD
- Protocole WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196723"
---
# <a name="wmpcd-protocol"></a><span data-ttu-id="92502-113">Protocole WMPCD</span><span class="sxs-lookup"><span data-stu-id="92502-113">WMPCD Protocol</span></span>

<span data-ttu-id="92502-114">Le protocole WMPCD vous permet de spécifier des pistes sur un disque compact à l’aide de la syntaxe d’URL.</span><span class="sxs-lookup"><span data-stu-id="92502-114">The WMPCD protocol enables you to specify tracks on a compact disc using URL syntax.</span></span> <span data-ttu-id="92502-115">Il s’agit de la syntaxe générale du protocole :</span><span class="sxs-lookup"><span data-stu-id="92502-115">This is the general syntax of the protocol:</span></span>


```C++
wmpcd://drive/track
```



<span data-ttu-id="92502-116">Le segment de *lecteur* est l’index du lecteur de CD.</span><span class="sxs-lookup"><span data-stu-id="92502-116">The *drive* segment is the index of the CD drive.</span></span> <span data-ttu-id="92502-117">Le segment de *suivi* est le numéro de la piste. L’exemple suivant illustre l’utilisation du protocole WMPCD.</span><span class="sxs-lookup"><span data-stu-id="92502-117">The *track* segment is the number of the track. The following example demonstrates using the WMPCD protocol.</span></span>


```C++
player.url = "wmpcd://0/4";
```



<span data-ttu-id="92502-118">L’exemple lit la quatrième piste sur le disque dans le premier lecteur de CD (le lecteur dont l’index est 0).</span><span class="sxs-lookup"><span data-stu-id="92502-118">The example plays the fourth track on the disc in the first CD drive (the drive whose index is 0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="92502-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92502-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92502-120">**Protocoles et types de fichiers pris en charge**</span><span class="sxs-lookup"><span data-stu-id="92502-120">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




