---
title: MkTypLib Command-Line outil
description: MkTypLib est une application de ligne de commande qui traite un fichier IDL pour produire une bibliothèque de types. Il peut également être utilisé pour générer un fichier d’en-tête C ou C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730637"
---
# <a name="mktyplib-command-line-tool"></a><span data-ttu-id="b5afe-104">MkTypLib Command-Line outil</span><span class="sxs-lookup"><span data-stu-id="b5afe-104">MkTypLib Command-Line Tool</span></span>

<span data-ttu-id="b5afe-105">\[L’outil Mktyplib.exe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="b5afe-105">\[The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="b5afe-106">Utilisez plutôt le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="b5afe-106">Use the MIDL compiler instead.</span></span> <span data-ttu-id="b5afe-107">Si vous avez besoin d’une compatibilité descendante avec les anciens programmes d’automatisation, utilisez le compilateur MIDL avec l’option **/mktyplib203** .\]</span><span class="sxs-lookup"><span data-stu-id="b5afe-107">If you need backward compatibility with old Automation programs, use the MIDL compiler with the **/mktyplib203** option.\]</span></span>

<span data-ttu-id="b5afe-108">MkTypLib est une application de ligne de commande qui traite un fichier IDL pour produire une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="b5afe-108">MkTypLib is a command-line application that processes an IDL file to produce a type library.</span></span> <span data-ttu-id="b5afe-109">Il peut également être utilisé pour générer un fichier d’en-tête C ou C++.</span><span class="sxs-lookup"><span data-stu-id="b5afe-109">It can also be used to generate a C or C++ header file.</span></span>

<span data-ttu-id="b5afe-110">Pour générer une bibliothèque de types à partir d’un fichier ODL :</span><span class="sxs-lookup"><span data-stu-id="b5afe-110">To generate a type library from a ODL file:</span></span>

-   <span data-ttu-id="b5afe-111">Exécutez la commande suivante à partir de l'invite de commande :</span><span class="sxs-lookup"><span data-stu-id="b5afe-111">From the command prompt, run the following command:</span></span>

    <span data-ttu-id="b5afe-112">\**mktyplibÂ \* \* \* nom de fichier*</span><span class="sxs-lookup"><span data-stu-id="b5afe-112">\**mktyplibÂ \*\*\*filename*</span></span>

    <span data-ttu-id="b5afe-113">où *filename* est le nom du fichier ODL.</span><span class="sxs-lookup"><span data-stu-id="b5afe-113">where *filename* is the name of the ODL file.</span></span>

<span data-ttu-id="b5afe-114">MkTypLib prend également en charge plusieurs paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b5afe-114">MkTypLib also supports several optional parameters.</span></span> <span data-ttu-id="b5afe-115">Pour obtenir la liste complète, exécutez la ligne de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b5afe-115">For a complete list, run the following command line:</span></span>

<span data-ttu-id="b5afe-116">**mktyplib/ ?**</span><span class="sxs-lookup"><span data-stu-id="b5afe-116">**mktyplib /?**</span></span>

<span data-ttu-id="b5afe-117">Comme MkTypLib est une application obsolète, il ne peut pas analyser des fichiers IDL ou des fichiers avec des interfaces définies en dehors d’une instruction de [**bibliothèque**](/windows/desktop/Midl/library) .</span><span class="sxs-lookup"><span data-stu-id="b5afe-117">Because MkTypLib is an obsolete application, it cannot parse IDL files or files with interfaces defined outside of a [**library**](/windows/desktop/Midl/library) statement.</span></span> <span data-ttu-id="b5afe-118">Pour plus d’informations, consultez [différences entre MIDL et mktyplib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span><span class="sxs-lookup"><span data-stu-id="b5afe-118">For more information, see [Differences Between MIDL and MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5afe-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5afe-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5afe-120">Traduire en C++</span><span class="sxs-lookup"><span data-stu-id="b5afe-120">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 