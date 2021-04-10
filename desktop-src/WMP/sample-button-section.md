---
title: Exemple de section de bouton
description: Exemple de section de bouton
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Windows Media Player Mobile Skins, section Button
- apparences, section de bouton
- référence pour les apparences, section de bouton
- boutons dans les apparences, section de bouton
- fichiers de définition d’apparence, section de bouton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029453"
---
# <a name="sample-button-section"></a><span data-ttu-id="49f74-108">Exemple de section de bouton</span><span class="sxs-lookup"><span data-stu-id="49f74-108">Sample Button Section</span></span>

<span data-ttu-id="49f74-109">Les lignes suivantes affichent une section de boutons standard d’un fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="49f74-109">The following lines show a typical Buttons section of a skin definition file:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



<span data-ttu-id="49f74-110">Ce code définit huit boutons utilisés pour fournir toutes les fonctions suivantes dans une apparence :</span><span class="sxs-lookup"><span data-stu-id="49f74-110">This code defines eight buttons that are used to provide all of the following functions in a skin:</span></span>

-   <span data-ttu-id="49f74-111">Lire, suspendre et arrêter des éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="49f74-111">Play, pause, and stop media items.</span></span>
-   <span data-ttu-id="49f74-112">Lecture aléatoire, répétition et déplacement dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="49f74-112">Shuffle, repeat, and move through the playlist.</span></span>
-   <span data-ttu-id="49f74-113">Désactiver le volume.</span><span class="sxs-lookup"><span data-stu-id="49f74-113">Mute the volume.</span></span>

<span data-ttu-id="49f74-114">Tous les boutons à l’exception du bouton muet sont des boutons région.</span><span class="sxs-lookup"><span data-stu-id="49f74-114">All the buttons except the mute button are region buttons.</span></span> <span data-ttu-id="49f74-115">Le bouton muet obtient ses images ayant fait l’objet d’un push et désactivées à partir du Super bitmap pour plus de commodité.</span><span class="sxs-lookup"><span data-stu-id="49f74-115">The mute button gets its Pushed and Disabled images from the Super bitmap for convenience.</span></span>

> [!Note]  
> <span data-ttu-id="49f74-116">Les types de boutons sont déconseillés dans les habillages pour Windows Media Player 10 mobile ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="49f74-116">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span> <span data-ttu-id="49f74-117">Au lieu d’un type de bouton déclaré dans votre fichier d’apparence, entrez « NA » pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="49f74-117">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="49f74-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49f74-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f74-119">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="49f74-119">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




