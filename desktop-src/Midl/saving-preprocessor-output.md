---
title: Enregistrement de la sortie du préprocesseur
description: L’affichage de la sortie du préprocesseur peut être une méthode de résolution des problèmes efficace, par exemple quand une syntaxe de préprocesseur IDL, C ou C non valide se produit, ou lorsque des valeurs factices-D sur la ligne de commande MIDL génèrent des erreurs obscures de création de rapports.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL du compilateur MIDL, enregistrement de la sortie du préprocesseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380057"
---
# <a name="saving-preprocessor-output"></a><span data-ttu-id="d2b6c-104">Enregistrement de la sortie du préprocesseur</span><span class="sxs-lookup"><span data-stu-id="d2b6c-104">Saving Preprocessor Output</span></span>

<span data-ttu-id="d2b6c-105">L’affichage de la sortie du préprocesseur peut être une méthode de résolution des problèmes efficace, par exemple quand une syntaxe de préprocesseur IDL, C ou C non valide se produit, ou lorsque des valeurs factices-D sur la ligne de commande MIDL génèrent des erreurs obscures de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-105">Viewing preprocessor output can be an effective troubleshooting method, such as when invalid IDL, C, or C-preprocessor syntax occurs, or when bogus -D values on the MIDL command line result in MIDL reporting arcane errors.</span></span> <span data-ttu-id="d2b6c-106">Les développeurs peuvent également examiner la sortie du préprocesseur pour déterminer les fichiers et définitions qui étaient présents dans le flux d’entrée du compilateur, par exemple lorsqu’une casse difficile de conflit de redéfinition de type doit être résolue.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-106">Developers may also want to examine preprocessor output to determine which files and definitions were present in the compiler input stream, such as when a difficult case of type redefinition conflict must be resolved.</span></span> <span data-ttu-id="d2b6c-107">Ou moins souvent, certains développeurs peuvent vouloir forcer des commutateurs privés sur le préprocesseur avec [**/CPP \_ OPT**](-cpp-opt.md), ou peuvent souhaiter voir le fonctionnement des commutateurs.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-107">Or less commonly, certain developers may want to force private switches on the preprocessor with [**/cpp\_opt**](-cpp-opt.md), or may want to see how the switches work.</span></span>

<span data-ttu-id="d2b6c-108">Le moyen le plus simple et le moins gênant d’obtenir les fichiers prétraités à partir d’une exécution de compilation MIDL consiste à utiliser le commutateur [**-savePP**](-savepp.md) .</span><span class="sxs-lookup"><span data-stu-id="d2b6c-108">The easiest and the least obtrusive way to obtain the preprocessed files from a MIDL compile run is to use the [**-savePP**](-savepp.md) switch.</span></span> <span data-ttu-id="d2b6c-109">Le commutateur **-savePP** empêche simplement MIDL de supprimer les fichiers temporaires que le préprocesseur renvoie à MIDL.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-109">The **-savePP** switch simply prevents MIDL from deleting the temporary files that the preprocessor passes back to MIDL.</span></span> <span data-ttu-id="d2b6c-110">Tenez compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d2b6c-110">Consider the following:</span></span>

<span data-ttu-id="d2b6c-111">**MIDL-savePP-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1-Oicf-env Win32 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="d2b6c-111">**midl -savePP -Id:\\nt\\public\\sdk\\inc -DNTENV=1 -Oicf -env win32 stub.idl**</span></span>

<span data-ttu-id="d2b6c-112">Cette directive compile stub. idl tout en préservant tous les fichiers de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-112">This directive compiles Stub.idl, yet preserves all preprocessor files.</span></span>

> [!Note]  
> <span data-ttu-id="d2b6c-113">MIDL génère des exécutions distinctes du préprocesseur pour les fichiers IDL et ACF (le cas échéant), ainsi que pour chaque fichier importé.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-113">MIDL spawns separate preprocessor runs for IDL and ACF file (if present) as well as for every imported file.</span></span>

 

<span data-ttu-id="d2b6c-114">Pour une compilation DCOM, plusieurs fichiers de préprocesseur sont généralement générés, même s’ils sont traités par MIDL comme un flux d’entrée contigu virtuel.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-114">For a DCOM compile, several preprocessor files are typically produced, even though they are processed by MIDL as a virtual contiguous input stream.</span></span> <span data-ttu-id="d2b6c-115">Dans un environnement de programmation Windows classique, les fichiers temporaires se trouvent dans le répertoire Temp sous la forme de noms de fichiers tels que MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-115">In a typical Windows programming environment, the temporary files can be found in the Temp directory as file names such as MID\*.tmp.</span></span> <span data-ttu-id="d2b6c-116">En cas de préservation de la sortie du préprocesseur, il est recommandé de surveiller les fichiers récents dans le répertoire Temp pour identifier les fichiers qui sont associés à l’exécution du préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-116">If preserving preprocessor output, it is good practice to watch for recent files in the Temp directory to identify which files are associated with which preprocessor run.</span></span>

<span data-ttu-id="d2b6c-117">Dans les cas simples, par exemple lorsque le fichier IDL compilé n’importe pas d’autres fichiers directement ou indirectement, ou lorsque vous examinez le fichier de niveau supérieur, le préprocesseur peut être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-117">In simple cases, such as when the compiled IDL file does not import other files directly or indirectly, or when examining the top-level file, the preprocessor can be invoked directly.</span></span> <span data-ttu-id="d2b6c-118">L’exécution directe du préprocesseur C/C++ peut révéler des erreurs masquées ou confuses par MIDL.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-118">Executing C/C++ preprocessor directly can reveal errors masked or confused by MIDL.</span></span> <span data-ttu-id="d2b6c-119">Par exemple, les deux lignes de commande de préprocesseur suivantes peuvent être utilisées pour la ligne MIDL précédemment citée :</span><span class="sxs-lookup"><span data-stu-id="d2b6c-119">For example, the following two preprocessor command lines can be used for the previously quoted MIDL line:</span></span>

<span data-ttu-id="d2b6c-120">**CL/E/nologo-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. pp**</span><span class="sxs-lookup"><span data-stu-id="d2b6c-120">**cl /E /nologo -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl > stub.pp**</span></span>

<span data-ttu-id="d2b6c-121">**CL/E/P-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="d2b6c-121">**cl /E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl**</span></span>

<span data-ttu-id="d2b6c-122">Dans le premier de ces deux exemples, **/e** [**/nologo**](-nologo.md) sont les commutateurs ajoutés par MIDL lors de l’appel du préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-122">In the first of these two examples, **/E** [**/nologo**](-nologo.md) are the switches that MIDL adds when invoking the preprocessor.</span></span> <span data-ttu-id="d2b6c-123">La sortie du préprocesseur est envoyée à stdout (l’écran) et nécessite donc une redirection vers un fichier à des fins d’examen.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-123">The preprocessor output is sent to stdout (the screen), and therefore requires redirection to a file for examination.</span></span> <span data-ttu-id="d2b6c-124">Dans le deuxième exemple, **/p** indique au préprocesseur de rediriger la sortie vers un \* fichier. i. dans ce cas, un fichier stub. i serait créé dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-124">In the second of these examples, **/P** directs the preprocessor to redirect the output to a \*.i file; in this case a Stub.i file would be created in the current directory.</span></span>

<span data-ttu-id="d2b6c-125">Le commutateur [**/CPP \_ OPT**](-cpp-opt.md) peut également être utilisé pour obtenir un fichier prétraité, mais il est difficile et inférieur aux méthodes mentionnées précédemment.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-125">The [**/cpp\_opt**](-cpp-opt.md) switch can also be used to obtain a preprocessed file, but is difficult and inferior to the previously mentioned methods.</span></span> <span data-ttu-id="d2b6c-126">L’exemple suivant génère également un fichier stub. i, comme le faisait l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-126">The following example also produces a Stub.i file, as did the previous example.</span></span> <span data-ttu-id="d2b6c-127">Les guillemets dans l’exemple suivant sont essentiels :</span><span class="sxs-lookup"><span data-stu-id="d2b6c-127">The quotes in the following example are essential:</span></span>

<span data-ttu-id="d2b6c-128">**MIDL-Oicf-Win32-CPP \_ OPT "/E/p-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1" stub. idl**</span><span class="sxs-lookup"><span data-stu-id="d2b6c-128">**Midl -Oicf -win32 -cpp\_opt "/E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1" stub.idl**</span></span>

 

 




