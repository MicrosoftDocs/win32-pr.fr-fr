---
title: Génération d’une bibliothèque de types avec MIDL
description: L’élément de niveau supérieur de la syntaxe ODL est l’instruction de bibliothèque (bloc de bibliothèque).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language MIDL, tâches, génération d’une bibliothèque de types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d9084631dc30eb1cff7f61f6f3f090f95bb92cff357b3902cb0959f2c4142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013847"
---
# <a name="generating-a-type-library-with-midl"></a>Génération d’une bibliothèque de types avec MIDL

L’élément de niveau supérieur de la syntaxe ODL est l’instruction de bibliothèque (bloc de bibliothèque). Chaque autre instruction ODL, à l’exception des attributs qui sont appliqués à l’instruction Library, doit être définie dans le bloc de bibliothèque. Lorsque le compilateur MIDL voit un bloc de bibliothèque, il génère une bibliothèque de types à peu près de la même façon que MkTypLib. À quelques exceptions près, décrites dans [différences entre MIDL et mktyplib](differences-between-midl-and-mktyplib.md), les instructions du bloc de bibliothèque doivent respecter la même syntaxe que dans le langage ODL et mktyplib.

> [!Note]  
> L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.

 

Vous pouvez appliquer des attributs ODL à des éléments définis à l’intérieur ou à l’extérieur du bloc de bibliothèque. Ces attributs n’ont aucun effet en dehors du bloc de bibliothèque, à moins que l’élément auquel ils sont appliqués soit référencé à partir du bloc de bibliothèque. Les instructions à l’intérieur du bloc de bibliothèque peuvent faire référence à un élément extérieur en l’utilisant comme type de base, en héritant de celle-ci ou en la référençant sur une ligne comme indiqué ci-dessous :

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

Si un élément défini en dehors du bloc de bibliothèque est référencé dans le bloc de bibliothèque, sa définition sera placée dans la bibliothèque de types générée. Le compilateur MIDL traite les instructions en dehors d’un bloc de bibliothèque comme un fichier IDL standard et analyse ces instructions à mesure qu’elles sont toujours effectuées. Normalement, cela implique la génération de stubs C pour une application RPC.

Pour plus d’informations sur la syntaxe générale d’un fichier ODL, consultez [syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax).

 

 