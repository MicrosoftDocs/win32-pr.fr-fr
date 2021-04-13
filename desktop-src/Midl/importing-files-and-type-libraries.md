---
title: Importation de fichiers et de bibliothèques de types
description: Les mots clés MIDL incluent, import et importlib vous permettent de réutiliser du code en référençant des fichiers d’en-tête, IDL et ODL (Object Definition Language) existants, ainsi que des bibliothèques de types compilés.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language MIDL, tâches, importation de fichiers et de bibliothèques de types
- importation de MIDL
- bibliothèques de types MIDL, importation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322573"
---
# <a name="importing-files-and-type-libraries"></a><span data-ttu-id="e14b2-106">Importation de fichiers et de bibliothèques de types</span><span class="sxs-lookup"><span data-stu-id="e14b2-106">Importing Files and Type Libraries</span></span>

<span data-ttu-id="e14b2-107">Les mots clés MIDL [**incluent**](include.md), [**Import**](import.md)et [**importlib**](importlib.md) vous permettent de réutiliser du code en référençant des fichiers d’en-tête, IDL et ODL (Object Definition Language) existants, ainsi que des bibliothèques de types compilés.</span><span class="sxs-lookup"><span data-stu-id="e14b2-107">The MIDL keywords [**include**](include.md), [**import**](import.md), and [**importlib**](importlib.md) let you reuse code by referencing existing header, IDL, and object definition language (ODL) files, and compiled type libraries.</span></span>

<span data-ttu-id="e14b2-108">La directive CCP [**include**](include.md) vous permet de spécifier dans un fichier ACF un ou plusieurs fichiers d’en-tête C à inclure dans le code stub généré par MIDL.</span><span class="sxs-lookup"><span data-stu-id="e14b2-108">The ACF [**include**](include.md) directive lets you specify in an ACF file one or more C-language header files to be included in the MIDL-generated stub code.</span></span> <span data-ttu-id="e14b2-109">Le fichier généré aura une ligne avec une directive de préprocesseur C **\# include** avec le fichier d’en-tête indiqué.</span><span class="sxs-lookup"><span data-stu-id="e14b2-109">The generated file will have a line with a **\#include** C-preprocessor directive with the indicated header file.</span></span> <span data-ttu-id="e14b2-110">Utilisez cette directive **include** pour importer des fichiers d’en-tête spécifiques à un environnement d’exploitation particulier et qui ne contiennent pas les informations nécessaires à l’interface entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="e14b2-110">Use this **include** directive to bring in header files that are specific to a particular operating environment and that do not contain information necessary for the interface between client and server.</span></span> <span data-ttu-id="e14b2-111">N’utilisez pas **include** pour les fichiers d’en-tête contenant des types de données que vous souhaitez accéder au fichier IDL. Utilisez plutôt la directive [**Import**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="e14b2-111">Do not use **include** for header files containing data types that you want available to the IDL file; instead, use the [**import**](import.md) directive.</span></span>

## <a name="example-1"></a><span data-ttu-id="e14b2-112">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e14b2-112">Example 1</span></span>

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

<span data-ttu-id="e14b2-113">La directive d' [**importation**](import.md) IDL est la méthode standard pour placer les définitions de type et d’interface à partir d’autres fichiers IDL (ou ODL) et de fichiers d’en-tête dans votre fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="e14b2-113">The IDL [**import**](import.md) directive is the standard method for bringing type and interface definitions from other IDL (or ODL) files and header files into your IDL file.</span></span> <span data-ttu-id="e14b2-114">Toutes les instructions IDL dans le fichier importé, telles que typedefs, les déclarations [**const**](const.md) et les définitions d’interface, deviennent disponibles dans le fichier IDL d’importation.</span><span class="sxs-lookup"><span data-stu-id="e14b2-114">All IDL statements in the imported file, such as typedefs, [**const**](const.md) declarations, and interface definitions become available to the importing IDL file.</span></span>

<span data-ttu-id="e14b2-115">À l’instar de la directive de préprocesseur du langage C **\# include**, la directive [**Import**](import.md) indique au compilateur d’inclure les types de données définis dans les fichiers IDL importés.</span><span class="sxs-lookup"><span data-stu-id="e14b2-115">Like the C-language preprocessor directive **\#include**, the [**import**](import.md) directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="e14b2-116">Contrairement à la directive **\# include** , la directive **Import** ignore les prototypes de procédure, car aucun stub n’est généré pour quoi que ce soit dans le fichier importé.</span><span class="sxs-lookup"><span data-stu-id="e14b2-116">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span> <span data-ttu-id="e14b2-117">Étant donné que le préprocesseur est appelé séparément pour le fichier importé, les directives de préprocesseur (telles que \* \*) ne sont pas reportées dans le fichier IDL d’importation.</span><span class="sxs-lookup"><span data-stu-id="e14b2-117">Because the preprocessor is invoked separately for the imported file, preprocessor directives (such as \*\*) do not carry over to the importing IDL file.</span></span>

<span data-ttu-id="e14b2-118">Pour plus d’informations sur l’utilisation de l' [**importation**](import.md) pour inclure des fichiers d’en-tête système dans un fichier IDL, consultez [importation de fichiers d’en-tête système](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="e14b2-118">For additional information on using [**import**](import.md) to include system header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

## <a name="example-2"></a><span data-ttu-id="e14b2-119">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e14b2-119">Example 2</span></span>

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

<span data-ttu-id="e14b2-120">La directive ODL [**importlib**](importlib.md) vous permet de référencer une bibliothèque de types compilée dans votre fichier IDL ou ODL.</span><span class="sxs-lookup"><span data-stu-id="e14b2-120">The ODL [**importlib**](importlib.md) directive lets you reference a compiled type library in your IDL or ODL file.</span></span> <span data-ttu-id="e14b2-121">La directive **importlib** doit se trouver à l’intérieur d’une instruction [**Library**](library.md) et doit précéder d’autres descriptions de type dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e14b2-121">The **importlib** directive must be inside a [**library**](library.md) statement, and must precede other type descriptions in the library.</span></span> <span data-ttu-id="e14b2-122">La bibliothèque importée, ainsi que la bibliothèque générée, doivent être accessibles à l’application au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e14b2-122">The imported library, as well as the generated library, must be available to the application at runtime.</span></span>

## <a name="example-3"></a><span data-ttu-id="e14b2-123">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="e14b2-123">Example 3</span></span>

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

<span data-ttu-id="e14b2-124">Vous pouvez également utiliser la directive C-preprocesseur **\# include** pour inclure des en-têtes et d’autres fichiers dans votre fichier IDL ou ODL.</span><span class="sxs-lookup"><span data-stu-id="e14b2-124">You can also use the C-preprocessor **\#include** directive to include headers and other files in your IDL or ODL file.</span></span> <span data-ttu-id="e14b2-125">N’oubliez pas, toutefois, que cette directive inclura littéralement le contenu entier du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e14b2-125">Be aware, however, that this directive will literally include the entire contents of the specified file.</span></span> <span data-ttu-id="e14b2-126">Si un fichier d’en-tête contient des prototypes dont vous n’avez pas besoin ou que vous ne souhaitez pas dans les fichiers stub générés par MIDL, ou s’il contient des définitions de type non accessibles à distance, vous devez utiliser la directive d' [**importation**](import.md) MIDL au lieu de la directive **\# include** .</span><span class="sxs-lookup"><span data-stu-id="e14b2-126">If a header file contains prototypes that you do not need or want in the MIDL-generated stub files, or if it contains nonremotable type definitions, you should use the MIDL [**import**](import.md) directive instead of the **\#include** directive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e14b2-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e14b2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e14b2-128">**port**</span><span class="sxs-lookup"><span data-stu-id="e14b2-128">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="e14b2-129">**importlib**</span><span class="sxs-lookup"><span data-stu-id="e14b2-129">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="e14b2-130">**inclusion**</span><span class="sxs-lookup"><span data-stu-id="e14b2-130">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="e14b2-131">Importation de fichiers d’en-tête système</span><span class="sxs-lookup"><span data-stu-id="e14b2-131">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




