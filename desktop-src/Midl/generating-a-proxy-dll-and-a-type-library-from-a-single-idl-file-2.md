---
title: Génération d’une DLL de proxy et d’une bibliothèque de types à partir d’un seul fichier IDL
description: Vous pouvez utiliser un seul fichier IDL pour générer des fichiers stub proxy et des fichiers d’en-tête pour le marshaling de code et une bibliothèque de types.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft Interface Definition Language MIDL, tâches, génération d’une DLL de proxy et d’une bibliothèque de types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029584"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a><span data-ttu-id="e6dc1-104">Génération d’une DLL de proxy et d’une bibliothèque de types à partir d’un seul fichier IDL</span><span class="sxs-lookup"><span data-stu-id="e6dc1-104">Generating a Proxy DLL and a Type Library from a Single IDL File</span></span>

<span data-ttu-id="e6dc1-105">Vous pouvez utiliser un seul fichier IDL pour générer des fichiers stub proxy et des fichiers d’en-tête pour le marshaling de code et une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="e6dc1-105">You can use a single IDL file to generate both the proxy stubs and header files for marshaling code, and a type library.</span></span> <span data-ttu-id="e6dc1-106">Pour ce faire, définissez une interface en dehors du bloc de bibliothèque, puis référencez cette interface à l’intérieur du bloc de bibliothèque, comme illustré dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="e6dc1-106">You do this by defining an interface outside the library block and then referencing that interface from inside the library block, as shown in this example:</span></span>

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

<span data-ttu-id="e6dc1-107">Pour plus d’informations, consultez [marshaling de types de données OLE](marshaling-ole-data-types.md) et [fichiers supplémentaires requis pour générer une bibliothèque de types](additional-files-required-to-generate-a-type-library-2.md).</span><span class="sxs-lookup"><span data-stu-id="e6dc1-107">For more information, see [Marshaling OLE Data Types](marshaling-ole-data-types.md) and [Additional Files Required To Generate a Type Library](additional-files-required-to-generate-a-type-library-2.md).</span></span>

 

 




