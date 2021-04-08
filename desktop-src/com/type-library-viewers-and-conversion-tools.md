---
title: Visionneuses de la bibliothèque de types et outils de conversion
description: Visionneuses de la bibliothèque de types et outils de conversion
ms.assetid: 35c29e2c-3ee3-4e73-b925-6aa0ccb50a00
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bf4ac71b3c2c2ff9cc63b196485b9e0aaa4e13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671550"
---
# <a name="type-library-viewers-and-conversion-tools"></a><span data-ttu-id="27f70-103">Visionneuses de la bibliothèque de types et outils de conversion</span><span class="sxs-lookup"><span data-stu-id="27f70-103">Type Library Viewers and Conversion Tools</span></span>

<span data-ttu-id="27f70-104">Les bibliothèques de types contiennent la spécification d’un ou plusieurs éléments COM, y compris les classes, les interfaces, les énumérations, etc.</span><span class="sxs-lookup"><span data-stu-id="27f70-104">Type libraries contain the specification for one or more COM elements, including classes, interfaces, enumerations, and more.</span></span> <span data-ttu-id="27f70-105">Ces fichiers sont stockés dans un format binaire standard.</span><span class="sxs-lookup"><span data-stu-id="27f70-105">These files are stored in a standard binary format.</span></span> <span data-ttu-id="27f70-106">Une bibliothèque de types peut être un fichier autonome avec l’extension de nom de fichier. tlb, ou elle peut être stockée en tant que ressource dans un fichier exécutable, qui peut avoir une extension de nom de fichier. ocx,. dll ou. exe.</span><span class="sxs-lookup"><span data-stu-id="27f70-106">A type library can be a stand-alone file with the .tlb file name extension, or it can be stored as a resource in an executable file, which can have an .ocx, .dll, or .exe file name extension.</span></span> <span data-ttu-id="27f70-107">Les visionneuses de bibliothèque de types et les outils de conversion décrits ci-après lisent ce format pour obtenir des informations sur les éléments COM dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="27f70-107">The type library viewers and conversion tools described following read this format to gain information about the COM elements in the library.</span></span>

<span data-ttu-id="27f70-108">Avant de pouvoir programmer un objet dans un langage de programmation particulier, vous devez être en mesure d’afficher sa bibliothèque de types dans cette langue.</span><span class="sxs-lookup"><span data-stu-id="27f70-108">Before you can program an object in a particular programming language, you must be able to view its type library in that language.</span></span> <span data-ttu-id="27f70-109">Vous disposez ainsi de la syntaxe appropriée pour les classes, les interfaces, les méthodes, les propriétés et les événements de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="27f70-109">Doing this provides you with the proper syntax for the classes, interfaces, methods, properties, and events of the COM object.</span></span>

<span data-ttu-id="27f70-110">Les produits de développement Microsoft fournissent les outils suivants que vous pouvez utiliser pour générer, extraire et afficher des informations sur la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="27f70-110">Microsoft development products provide the following tools that you can use to generate, extract, and view type library information.</span></span>

## <a name="c"></a><span data-ttu-id="27f70-111">C++</span><span class="sxs-lookup"><span data-stu-id="27f70-111">C++</span></span>

-   [<span data-ttu-id="27f70-112">Explorateur d’objets OLE-COM</span><span class="sxs-lookup"><span data-stu-id="27f70-112">OLE-COM Object Viewer</span></span>](ole-com-object-viewer.md)
-   [<span data-ttu-id="27f70-113">Compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="27f70-113">MIDL compiler</span></span>](midl-compiler.md)
-   [<span data-ttu-id="27f70-114">MkTypLib</span><span class="sxs-lookup"><span data-stu-id="27f70-114">MkTypLib</span></span>](mktyplib-command-line-tool.md)

## <a name="visual-basic"></a><span data-ttu-id="27f70-115">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="27f70-115">Visual Basic</span></span>

-   [<span data-ttu-id="27f70-116">Explorateur d’objets Visual Basic</span><span class="sxs-lookup"><span data-stu-id="27f70-116">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="java"></a><span data-ttu-id="27f70-117">Java</span><span class="sxs-lookup"><span data-stu-id="27f70-117">Java</span></span>

-   [<span data-ttu-id="27f70-118">JActiveX</span><span class="sxs-lookup"><span data-stu-id="27f70-118">JActiveX</span></span>](jactivex-command-line-tool.md)
-   [<span data-ttu-id="27f70-119">Assistant bibliothèque de types Java</span><span class="sxs-lookup"><span data-stu-id="27f70-119">Java Type Library Wizard</span></span>](java-type-library-wizard.md)
-   [<span data-ttu-id="27f70-120">JavaTLB</span><span class="sxs-lookup"><span data-stu-id="27f70-120">JavaTLB</span></span>](javatlb-command-line-tool.md)

<span data-ttu-id="27f70-121">Pour obtenir une vue d’ensemble de la façon dont ces outils interagissent avec les bibliothèques de types, consultez [comment outils de développement utiliser les bibliothèques de types](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="27f70-121">For an overview of how these tools interact with type libraries, see [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

 

 




