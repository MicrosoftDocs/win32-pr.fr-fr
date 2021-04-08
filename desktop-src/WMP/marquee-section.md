---
title: Section de texte défilant
description: Section de texte défilant
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Windows Media Player Mobile Skins, palissades
- apparences, rectangles de sélection
- création d’apparences, section de texte défilant
- écriture de code pour les apparences, section de texte défilant
- textes défilant dans les enveloppes, section de texte défilant
- fichiers de définition d’apparence, section de texte défilant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675878"
---
# <a name="marquee-section"></a><span data-ttu-id="5ecf6-109">Section de texte défilant</span><span class="sxs-lookup"><span data-stu-id="5ecf6-109">Marquee Section</span></span>

<span data-ttu-id="5ecf6-110">La section Marquee contient des informations sur la zone de texte Marquee, qui affiche le texte de défilement :</span><span class="sxs-lookup"><span data-stu-id="5ecf6-110">The Marquee section contains information about the marquee text box, which will display scrolling text:</span></span>


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



<span data-ttu-id="5ecf6-111">Le titre et l’auteur de l’élément multimédia actuel s’affichent, même si vous pouvez afficher n’importe quel type de texte dans le texte défilant.</span><span class="sxs-lookup"><span data-stu-id="5ecf6-111">This will display the title and author of the current media item although you can display any text type in the marquee.</span></span> <span data-ttu-id="5ecf6-112">Par exemple, vous pouvez également inclure le nom de fichier, l’État et la sélection dans votre texte défilant.</span><span class="sxs-lookup"><span data-stu-id="5ecf6-112">For example, you could also include Filename, Status, and Playlist in your marquee.</span></span>

> [!Note]  
> <span data-ttu-id="5ecf6-113">Pour assurer la compatibilité avec les versions de Windows Media Player Mobile antérieures à Windows Media Player 10 mobile, l’utilisation de « marquis » dans un fichier de définition d’apparence est toujours considérée comme valide.</span><span class="sxs-lookup"><span data-stu-id="5ecf6-113">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="5ecf6-114">Pour plus d’informations sur la section de texte défilant, consultez [texte défilant](marquee.md) dans la référence d’apparence.</span><span class="sxs-lookup"><span data-stu-id="5ecf6-114">For more about the Marquee section, see [Marquee](marquee.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ecf6-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ecf6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ecf6-116">**Écriture du code**</span><span class="sxs-lookup"><span data-stu-id="5ecf6-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




