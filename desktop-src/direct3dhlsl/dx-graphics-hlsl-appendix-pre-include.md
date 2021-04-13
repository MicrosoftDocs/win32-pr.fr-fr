---
title: " include (directive)"
description: Directive de préprocesseur qui insère le contenu du fichier spécifié dans le programme source à l’emplacement où la directive apparaît.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- include, directive HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990941"
---
# <a name="include-directive"></a><span data-ttu-id="4fadd-104">\#include (directive)</span><span class="sxs-lookup"><span data-stu-id="4fadd-104">\#include Directive</span></span>

<span data-ttu-id="4fadd-105">Directive de préprocesseur qui insère le contenu du fichier spécifié dans le programme source à l’emplacement où la directive apparaît.</span><span class="sxs-lookup"><span data-stu-id="4fadd-105">Preprocessor directive that inserts the contents of the specified file into the source program at the point where the directive appears.</span></span>


| <span data-ttu-id="4fadd-106">\#inclure «*nom de fichier*»</span><span class="sxs-lookup"><span data-stu-id="4fadd-106">\#include "*filename*"</span></span>       |
|------------------------------|
| <span data-ttu-id="4fadd-107">\#inclure le *nom de fichier* <></span><span class="sxs-lookup"><span data-stu-id="4fadd-107">\#include <*filename*></span></span> |

## <a name="parameters"></a><span data-ttu-id="4fadd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fadd-108">Parameters</span></span>

| <span data-ttu-id="4fadd-109">Élément</span><span class="sxs-lookup"><span data-stu-id="4fadd-109">Item</span></span> | <span data-ttu-id="4fadd-110">Description</span><span class="sxs-lookup"><span data-stu-id="4fadd-110">Description</span></span> |
|------|-------------|
| <span data-ttu-id="4fadd-111">*extension*</span><span class="sxs-lookup"><span data-stu-id="4fadd-111">*filename*</span></span> | <span data-ttu-id="4fadd-112">Nom du fichier à inclure, éventuellement précédé d’une spécification de répertoire.</span><span class="sxs-lookup"><span data-stu-id="4fadd-112">Filename of the file to include, optionally preceded by a directory specification.</span></span> <span data-ttu-id="4fadd-113">Le nom de fichier doit spécifier un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="4fadd-113">The filename must specify an existing file.</span></span> |

## <a name="remarks"></a><span data-ttu-id="4fadd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4fadd-114">Remarks</span></span>

<span data-ttu-id="4fadd-115">La \# directive include provoque le remplacement de la directive par le contenu entier du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="4fadd-115">The \#include directive causes replacement of the directive by the entire contents of the specified file.</span></span> <span data-ttu-id="4fadd-116">Le préprocesseur arrête de Rechercher dès qu’il trouve un fichier avec le nom spécifié ; Si vous spécifiez une spécification de chemin d’accès complète et non ambiguë pour le fichier, le préprocesseur recherche uniquement le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="4fadd-116">The preprocessor stops searching as soon as it finds a file with the specified name; if you specify a complete, unambiguous path specification for the file, the preprocessor searches only the specified path.</span></span>

> [!NOTE]
> <span data-ttu-id="4fadd-117">L' [outil Effect-compiler](/windows/desktop/direct3dtools/fxc) est doté d’un gestionnaire d’inclusion intégré utilisant le commutateur/i.</span><span class="sxs-lookup"><span data-stu-id="4fadd-117">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) has a built-in include handler using the /I switch.</span></span> <span data-ttu-id="4fadd-118">Toutefois, lors de l’exécution du compilateur à partir de l’API, vous pouvez fournir un gestionnaire include personnalisé en implémentant l’interface ID3DXInclude.</span><span class="sxs-lookup"><span data-stu-id="4fadd-118">However, when executing the compiler from the API, you can provide a customized include handler by implementing the ID3DXInclude interface.</span></span>

<span data-ttu-id="4fadd-119">La différence entre les deux formes de syntaxe est l’ordre dans lequel le préprocesseur recherche les fichiers d’en-tête lorsque le chemin d’accès est spécifié de manière incomplète, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4fadd-119">The difference between the two syntax forms is the order in which the preprocessor searches for header files when the path is incompletely specified, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4fadd-120">Forme syntaxique</span><span class="sxs-lookup"><span data-stu-id="4fadd-120">Syntax form</span></span></th>
<th><span data-ttu-id="4fadd-121">Modèle de recherche de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="4fadd-121">Preprocessor search pattern</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4fadd-122">#inclure le <b>&quot;</b> <em>nom de fichier</em><b>&quot;</b></span><span class="sxs-lookup"><span data-stu-id="4fadd-122">#include <b>&quot;</b><em>filename</em><b>&quot;</b></span></span></td>
<td><span data-ttu-id="4fadd-123">Recherche le fichier include :</span><span class="sxs-lookup"><span data-stu-id="4fadd-123">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="4fadd-124">dans le même répertoire que le fichier qui contient la directive #include.</span><span class="sxs-lookup"><span data-stu-id="4fadd-124">in the same directory as the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="4fadd-125">dans les répertoires de tous les fichiers qui contiennent une directive #include pour le fichier qui contient la directive #include.</span><span class="sxs-lookup"><span data-stu-id="4fadd-125">in the directories of any files that contain a #include directive for the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="4fadd-126">dans les chemins d’accès spécifiés par l’option du compilateur/I, dans l’ordre dans lequel ils sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="4fadd-126">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="4fadd-127">dans les chemins d’accès spécifiés par la variable d’environnement INCLUDe, dans l’ordre dans lequel ils sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="4fadd-127">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="4fadd-128">La variable d’environnement INCLUDe est ignorée dans un environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="4fadd-128">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="4fadd-129">Reportez-vous à la documentation de votre environnement de développement pour plus d’informations sur la façon de définir les chemins d’accès include pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="4fadd-129">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fadd-130">#inclure le <b><</b> <em>nom de fichier</em><b>></b></span><span class="sxs-lookup"><span data-stu-id="4fadd-130">#include <b><</b><em>filename</em><b>></b></span></span></td>
<td><span data-ttu-id="4fadd-131">Recherche le fichier include :</span><span class="sxs-lookup"><span data-stu-id="4fadd-131">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="4fadd-132">dans les chemins d’accès spécifiés par l’option du compilateur/I, dans l’ordre dans lequel ils sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="4fadd-132">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="4fadd-133">dans les chemins d’accès spécifiés par la variable d’environnement INCLUDe, dans l’ordre dans lequel ils sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="4fadd-133">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="4fadd-134">La variable d’environnement INCLUDe est ignorée dans un environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="4fadd-134">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="4fadd-135">Reportez-vous à la documentation de votre environnement de développement pour plus d’informations sur la façon de définir les chemins d’accès include pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="4fadd-135">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a><span data-ttu-id="4fadd-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="4fadd-136">Examples</span></span>

<span data-ttu-id="4fadd-137">L’exemple suivant fait en sorte que le préprocesseur remplace la \# directive include par le contenu de stdio. h.</span><span class="sxs-lookup"><span data-stu-id="4fadd-137">The following example causes the preprocessor to replace the \#include directive with the contents of stdio.h.</span></span> <span data-ttu-id="4fadd-138">Étant donné que l’exemple utilise le format Chevron, le préprocesseur recherche le fichier uniquement dans les répertoires listés par l’option de compilateur/I et la variable d’environnement INCLUDe.</span><span class="sxs-lookup"><span data-stu-id="4fadd-138">Because the example uses the angle bracket format, the preprocessor will search for the file only in the directories listed by the /I compiler option and the INCLUDE environment variable.</span></span>

```cpp
#include <stdio.h>
```

## <a name="see-also"></a><span data-ttu-id="4fadd-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fadd-139">See also</span></span>

- [<span data-ttu-id="4fadd-140">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4fadd-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)

- <span data-ttu-id="4fadd-141">[Interface ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4fadd-141">[ID3D10Include Interface](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>

- [<span data-ttu-id="4fadd-142">Effect-Tool du compilateur</span><span class="sxs-lookup"><span data-stu-id="4fadd-142">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)