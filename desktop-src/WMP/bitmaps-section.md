---
title: Section bitmaps
description: Section bitmaps
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Apparences mobiles du lecteur Windows Media, bitmaps
- habillages, images bitmap
- création d’habillages, section bitmaps
- écriture de code pour les habillages, section bitmaps
- bitmaps dans une apparence, section bitmaps
- fichiers de définition d’apparence, section bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029127"
---
# <a name="bitmaps-section"></a><span data-ttu-id="29086-109">Section bitmaps</span><span class="sxs-lookup"><span data-stu-id="29086-109">Bitmaps Section</span></span>

<span data-ttu-id="29086-110">Ensuite, vous devez disposer d’une section qui définit chacun de vos fichiers bitmap.</span><span class="sxs-lookup"><span data-stu-id="29086-110">Next, you must have a section that defines each of your bitmap files.</span></span> <span data-ttu-id="29086-111">Un fichier doit être assigné à chaque type de bitmap que vous allez utiliser, même si vous pouvez avoir plusieurs types utilisant la même bitmap.</span><span class="sxs-lookup"><span data-stu-id="29086-111">Each type of bitmap you will use must have a file assigned to it, though you can have more than one type using the same bitmap.</span></span>


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="29086-112">La section bitmaps doit commencer par le mot bitmaps entre crochets, puis une ligne pour chaque type de bitmap que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="29086-112">The Bitmaps section must begin with the word Bitmaps in brackets and then a line for each bitmap type you want to define.</span></span> <span data-ttu-id="29086-113">Dans cet exemple, cinq types de bitmaps ont été définis.</span><span class="sxs-lookup"><span data-stu-id="29086-113">In this example, five types of bitmaps were defined.</span></span> <span data-ttu-id="29086-114">Pour plus d’informations sur la section bitmaps, consultez [bitmaps](bitmaps.md) dans la référence d’apparence.</span><span class="sxs-lookup"><span data-stu-id="29086-114">For more about the Bitmaps section, see [Bitmaps](bitmaps.md) in the Skin Reference.</span></span>

> [!Note]  
> <span data-ttu-id="29086-115">La région et les super bitmaps sont déconseillées dans les habillages Windows Media Player 10 mobile ou ultérieur.</span><span class="sxs-lookup"><span data-stu-id="29086-115">The Region and Super bitmaps are deprecated in Windows Media Player 10 Mobile or later skins.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="29086-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29086-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29086-117">**Écriture du code**</span><span class="sxs-lookup"><span data-stu-id="29086-117">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




