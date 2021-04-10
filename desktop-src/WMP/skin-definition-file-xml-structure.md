---
title: Structure XML du fichier de définition d’apparence
description: Structure XML du fichier de définition d’apparence
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- création d’apparences, de fichiers de définition d’apparence
- Apparences du lecteur Windows Media, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, structure XML
- Structure XML pour les fichiers de définition d’apparence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029476"
---
# <a name="skin-definition-file-xml-structure"></a><span data-ttu-id="7f8b6-109">Structure XML du fichier de définition d’apparence</span><span class="sxs-lookup"><span data-stu-id="7f8b6-109">Skin Definition File XML Structure</span></span>

<span data-ttu-id="7f8b6-110">Le fichier de définition d’apparence est écrit en XML.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-110">The skin definition file is written in XML.</span></span> <span data-ttu-id="7f8b6-111">L’une des fonctionnalités importantes de XML est qu’elle est entièrement structurée et est similaire à un plan.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-111">One of the important features of XML is that it is completely structured, and is similar to an outline.</span></span> <span data-ttu-id="7f8b6-112">Le code XML est simplement une série d’éléments tels que **View** et **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-112">The XML code is simply a series of elements such as **VIEW** and **BUTTONGROUP**.</span></span> <span data-ttu-id="7f8b6-113">Vous allez commencer par les éléments, puis les définir avec des attributs.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-113">You will start with the elements and then define them with attributes.</span></span> <span data-ttu-id="7f8b6-114">Le reste de ce didacticiel vous donne des détails sur les attributs, mais voici le contour des éléments qui seront utilisés :</span><span class="sxs-lookup"><span data-stu-id="7f8b6-114">The rest of this tutorial will give you details on the attributes, but here is the outline of the elements that will be used:</span></span>


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



<span data-ttu-id="7f8b6-115">En gardant à l’esprit la structure simple des éléments, vous pouvez avoir un sens des attributs qui rendent chaque élément unique.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-115">By keeping in mind the simple structure of the elements, you can make sense of the attributes that make each element unique.</span></span> <span data-ttu-id="7f8b6-116">Les détails de chaque élément seront traités dans les rubriques restantes de cette section.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-116">Details of each element will be covered in the remaining topics of this section.</span></span> <span data-ttu-id="7f8b6-117">Pour plus d’informations sur les éléments et les attributs, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7f8b6-117">For more information about elements and attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f8b6-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f8b6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f8b6-119">**Création du fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="7f8b6-119">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




