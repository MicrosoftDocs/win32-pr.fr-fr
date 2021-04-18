---
title: Types de données dans le corps de l’interface
description: Le corps de l’interface, qui est placé entre accolades (), contient les types de données qui seront utilisés dans les appels de procédure distante et les prototypes pour les fonctions qui seront exécutées à distance.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfaces MIDL, types de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512032"
---
# <a name="data-types-in-the-interface-body"></a><span data-ttu-id="88b99-104">Types de données dans le corps de l’interface</span><span class="sxs-lookup"><span data-stu-id="88b99-104">Data Types in the Interface Body</span></span>

<span data-ttu-id="88b99-105">Le corps de l’interface, qui est placé entre accolades ({}), contient les types de données qui seront utilisés dans les appels de procédure distante et les prototypes pour les fonctions qui seront exécutées à distance.</span><span class="sxs-lookup"><span data-stu-id="88b99-105">The interface body, which is enclosed in braces ({ }), contains the data types that will be used in remote procedure calls and prototypes for the functions that will be executed remotely.</span></span> <span data-ttu-id="88b99-106">Un corps d’interface peut contenir des importations, des pragmas, des déclarations de constantes, des déclarations de type et des déclarations de fonction.</span><span class="sxs-lookup"><span data-stu-id="88b99-106">An interface body can contain imports, pragmas, constant declarations, type declarations, and function declarations.</span></span> <span data-ttu-id="88b99-107">Sauf en mode de compatibilité OSF, le compilateur MIDL autorise également les déclarations implicites sous la forme de définitions de variables.</span><span class="sxs-lookup"><span data-stu-id="88b99-107">Except in OSF-compatibility mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="88b99-108">Notez que la spécification OSF-DCE pour les interfaces RPC n’autorise pas plusieurs interfaces dans un seul fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="88b99-108">Note that the OSF-DCE specification for RPC interfaces does not allow multiple interfaces in a single IDL file.</span></span> <span data-ttu-id="88b99-109">Par conséquent, si vous compilez en mode de compatibilité OSF ( [**/OSF**](-osf.md)) MIDL, votre fichier IDL ne peut contenir qu’une seule interface.</span><span class="sxs-lookup"><span data-stu-id="88b99-109">Therefore, if you are compiling in MIDL's OSF-compatibility mode ( [**/osf**](-osf.md)), your IDL file can contain only one interface.</span></span>

<span data-ttu-id="88b99-110">Pour plus d’informations sur l’utilisation du compilateur MIDL pour produire des bibliothèques de types, consultez [génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md).</span><span class="sxs-lookup"><span data-stu-id="88b99-110">For details on using the MIDL compiler to produce type libraries, see [Generating a Type Library with MIDL](generating-a-type-library-with-midl-2.md).</span></span>

<span data-ttu-id="88b99-111">Dans Microsoft RPC, un fichier IDL peut contenir plusieurs interfaces et ces interfaces peuvent être transmises par progression déclarées (dans le fichier IDL qui les définit).</span><span class="sxs-lookup"><span data-stu-id="88b99-111">In Microsoft RPC, an IDL file can contain multiple interfaces and these interfaces can be forward declared (within the IDL file that defines them).</span></span> <span data-ttu-id="88b99-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88b99-112">For example:</span></span>

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




