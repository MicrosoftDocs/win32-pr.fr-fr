---
title: Génération d’une bibliothèque de types avec MIDL
description: L’élément de niveau supérieur de la syntaxe ODL est l’instruction de bibliothèque (bloc de bibliothèque).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language MIDL, tâches, génération d’une bibliothèque de types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510882"
---
# <a name="generating-a-type-library-with-midl"></a><span data-ttu-id="69a7c-104">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="69a7c-104">Generating a Type Library with MIDL</span></span>

<span data-ttu-id="69a7c-105">L’élément de niveau supérieur de la syntaxe ODL est l’instruction de bibliothèque (bloc de bibliothèque).</span><span class="sxs-lookup"><span data-stu-id="69a7c-105">The top-level element of the ODL syntax is the library statement (library block).</span></span> <span data-ttu-id="69a7c-106">Chaque autre instruction ODL, à l’exception des attributs qui sont appliqués à l’instruction Library, doit être définie dans le bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="69a7c-106">Every other ODL statement, with the exception of the attributes that are applied to the library statement, must be defined within the library block.</span></span> <span data-ttu-id="69a7c-107">Lorsque le compilateur MIDL voit un bloc de bibliothèque, il génère une bibliothèque de types à peu près de la même façon que MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="69a7c-107">When the MIDL compiler sees a library block, it generates a type library in much the same way that MkTypLib does.</span></span> <span data-ttu-id="69a7c-108">À quelques exceptions près, décrites dans [différences entre MIDL et mktyplib](differences-between-midl-and-mktyplib.md), les instructions du bloc de bibliothèque doivent respecter la même syntaxe que dans le langage ODL et mktyplib.</span><span class="sxs-lookup"><span data-stu-id="69a7c-108">With a few exceptions, described in [Differences Between MIDL and MKTYPLIB](differences-between-midl-and-mktyplib.md), the statements within the library block should follow the same syntax as in the ODL language and MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="69a7c-109">L’outil Mktyplib.exe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="69a7c-109">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="69a7c-110">Utilisez plutôt le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="69a7c-110">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="69a7c-111">Vous pouvez appliquer des attributs ODL à des éléments définis à l’intérieur ou à l’extérieur du bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="69a7c-111">You can apply ODL attributes to elements that are defined either inside or outside the library block.</span></span> <span data-ttu-id="69a7c-112">Ces attributs n’ont aucun effet en dehors du bloc de bibliothèque, à moins que l’élément auquel ils sont appliqués soit référencé à partir du bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="69a7c-112">These attributes have no effect outside the library block unless the element they are applied to is referenced from within the library block.</span></span> <span data-ttu-id="69a7c-113">Les instructions à l’intérieur du bloc de bibliothèque peuvent faire référence à un élément extérieur en l’utilisant comme type de base, en héritant de celle-ci ou en la référençant sur une ligne comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="69a7c-113">Statements inside the library block can reference an outside element either by using it as a base type, inheriting from it, or by referencing it on a line as shown:</span></span>

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

<span data-ttu-id="69a7c-114">Si un élément défini en dehors du bloc de bibliothèque est référencé dans le bloc de bibliothèque, sa définition sera placée dans la bibliothèque de types générée.</span><span class="sxs-lookup"><span data-stu-id="69a7c-114">If an element defined outside the library block is referenced within the library block, then its definition will be put into the generated type library.</span></span> <span data-ttu-id="69a7c-115">Le compilateur MIDL traite les instructions en dehors d’un bloc de bibliothèque comme un fichier IDL standard et analyse ces instructions à mesure qu’elles sont toujours effectuées.</span><span class="sxs-lookup"><span data-stu-id="69a7c-115">The MIDL compiler treats the statements outside of a library block as a typical IDL file and parses those statements as it has always done.</span></span> <span data-ttu-id="69a7c-116">Normalement, cela implique la génération de stubs C pour une application RPC.</span><span class="sxs-lookup"><span data-stu-id="69a7c-116">Normally, this means generating C-language stubs for an RPC application.</span></span>

<span data-ttu-id="69a7c-117">Pour plus d’informations sur la syntaxe générale d’un fichier ODL, consultez [syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax).</span><span class="sxs-lookup"><span data-stu-id="69a7c-117">For more information about the general syntax for an ODL file see [ODL File Syntax](/previous-versions/windows/desktop/automat/odl-file-syntax).</span></span>

 

 