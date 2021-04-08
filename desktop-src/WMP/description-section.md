---
title: Section Description
description: Section Description
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player Mobile Skins, section Description
- apparences, section Description
- création d’apparences, section Description
- écriture de code pour les apparences, section Description
- Section Description dans les apparences
- fichiers de définition d’apparence, section Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840681"
---
# <a name="description-section"></a><span data-ttu-id="1f4ac-109">Section Description</span><span class="sxs-lookup"><span data-stu-id="1f4ac-109">Description Section</span></span>

<span data-ttu-id="1f4ac-110">Ensuite, vous devez fournir une section qui décrit la taille et l’orientation de l’apparence lors de la création d’une apparence pour Windows Media Player 9 Series pour Windows Mobile 2003 et versions ultérieures :</span><span class="sxs-lookup"><span data-stu-id="1f4ac-110">Next, you must provide a section that describes the size and orientation of the skin when creating a skin for Windows Media Player 9 Series for Windows Mobile 2003 and later versions:</span></span>


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



<span data-ttu-id="1f4ac-111">La section Description doit commencer par la description du mot entre crochets, puis inclure une ligne qui spécifie les dimensions et la résolution d’affichage de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="1f4ac-111">The Description section must begin with the word Description in brackets, and then include a line that specifies the dimensions and display resolution for the skin.</span></span>

<span data-ttu-id="1f4ac-112">Les lignes commençant par deux barres obliques ne sont pas traitées et peuvent être utilisées pour les commentaires ou, comme indiqué dans le code précédent, un modèle pour vous aider à vous souvenir de ce qui se trouve dans une section.</span><span class="sxs-lookup"><span data-stu-id="1f4ac-112">Lines beginning with two forward slashes are not processed, and can be used for comments or, as shown in the previous code, a template to help you remember what goes in a section.</span></span> <span data-ttu-id="1f4ac-113">Vous pouvez également utiliser des modèles pour faciliter l’alignement de tous les éléments en colonnes.</span><span class="sxs-lookup"><span data-stu-id="1f4ac-113">You can also use templates to help align everything into columns.</span></span>

<span data-ttu-id="1f4ac-114">Pour plus d’informations sur la section Description, consultez [Description](description.md) dans la référence de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="1f4ac-114">For more information about the Description section, see [Description](description.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f4ac-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f4ac-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f4ac-116">**Écriture du code**</span><span class="sxs-lookup"><span data-stu-id="1f4ac-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




