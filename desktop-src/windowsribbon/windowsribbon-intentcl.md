---
title: Compilation du balisage du ruban
description: Pour que l’infrastructure du ruban Windows utilise le fichier de balisage du ruban, le fichier de balisage doit être compilé dans un fichier de ressources au format binaire.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Ruban Windows, compiler le balisage
- Ruban, compiler le balisage
- Ruban Windows, flux de travail du compilateur
- Ruban, flux de travail du compilateur
- Ruban Windows, compilateur de commandes d’interface utilisateur (UICC.exe)
- Ruban, compilateur de commandes d’interface utilisateur (UICC.exe)
- Compilateur de commandes d’interface utilisateur (UICC.exe)
- UICC.exe (compilateur de commandes d’interface utilisateur)
- compilation du balisage du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507355"
---
# <a name="compiling-ribbon-markup"></a><span data-ttu-id="7c66c-112">Compilation du balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="7c66c-112">Compiling Ribbon Markup</span></span>

<span data-ttu-id="7c66c-113">Pour que l’infrastructure du ruban Windows utilise le fichier de [balisage du ruban](windowsribbon-schema.md) , le fichier de balisage doit être compilé dans un fichier de ressources au format binaire.</span><span class="sxs-lookup"><span data-stu-id="7c66c-113">For the Windows Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="7c66c-114">Un compilateur de balisage dédié, le compilateur de commandes d’interface utilisateur (UICC), est inclus dans le kit de développement logiciel (SDK) Windows (7,0 ou version ultérieure) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="7c66c-114">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="7c66c-115">En plus de compiler la version binaire du balisage, UICC génère un fichier d’en-tête de définition d’ID (. h) qui expose tous les éléments de balisage à l’application hôte du ruban et un fichier de ressources (. RC) qui est utilisé pour lier des ressources d’image et de chaîne à l’application hôte au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="7c66c-115">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

-   [<span data-ttu-id="7c66c-116">Flux de travail du compilateur</span><span class="sxs-lookup"><span data-stu-id="7c66c-116">Compiler Workflow</span></span>](#compiler-workflow)
-   [<span data-ttu-id="7c66c-117">Syntaxe de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="7c66c-117">Command-Line Syntax</span></span>](#command-line-syntax)
    -   [<span data-ttu-id="7c66c-118">Arguments et options</span><span class="sxs-lookup"><span data-stu-id="7c66c-118">Arguments and Options</span></span>](#arguments-and-options)
    -   [<span data-ttu-id="7c66c-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c66c-119">Example</span></span>](#example)
-   [<span data-ttu-id="7c66c-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c66c-120">Related topics</span></span>](#related-topics)

## <a name="compiler-workflow"></a><span data-ttu-id="7c66c-121">Flux de travail du compilateur</span><span class="sxs-lookup"><span data-stu-id="7c66c-121">Compiler Workflow</span></span>

<span data-ttu-id="7c66c-122">Le flux de travail du compilateur de balisage du ruban est illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="7c66c-122">The workflow of the Ribbon markup compiler is illustrated in the following diagram.</span></span>

![Diagramme montrant le flux de travail du compilateur de balisage du ruban.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a><span data-ttu-id="7c66c-124">Syntaxe de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="7c66c-124">Command-Line Syntax</span></span>

<span data-ttu-id="7c66c-125">La syntaxe de la ligne de commande pour le compilateur de balisage du ruban est illustrée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7c66c-125">The command-line syntax for the Ribbon markup compiler is shown in the following example.</span></span>


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a><span data-ttu-id="7c66c-126">Arguments et options</span><span class="sxs-lookup"><span data-stu-id="7c66c-126">Arguments and Options</span></span>

<span data-ttu-id="7c66c-127">Les arguments et les options de cet outil sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7c66c-127">The arguments and options for this tool are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="7c66c-128">Les options de ligne de commande indiquées doivent être spécifiées dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="7c66c-128">The command-line options listed must be specified in the order given.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c66c-129">Option</span><span class="sxs-lookup"><span data-stu-id="7c66c-129">Option</span></span></th>
<th><span data-ttu-id="7c66c-130">Description</span><span class="sxs-lookup"><span data-stu-id="7c66c-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7c66c-131">/Header<headerFile></span><span class="sxs-lookup"><span data-stu-id="7c66c-131">/header:<headerFile></span></span></td>
<td><span data-ttu-id="7c66c-132">Générez un fichier d’en-tête appelé <headerFile> qui contient les symboles de ressource ID de commande de balisage.</span><span class="sxs-lookup"><span data-stu-id="7c66c-132">Generate a header file called <headerFile> that contains the markup Command ID resource symbols.</span></span> <span data-ttu-id="7c66c-133">En cas d’omission, un fichier d’en-tête n’est pas généré.</span><span class="sxs-lookup"><span data-stu-id="7c66c-133">If omitted, a header file is not generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c66c-134">/res<resourceFile></span><span class="sxs-lookup"><span data-stu-id="7c66c-134">/res:<resourceFile></span></span></td>
<td><span data-ttu-id="7c66c-135">Générez un fichier de ressources appelé <resourceFile> qui lie toutes les ressources d’image et de chaîne, le fichier de balisage binaire et le fichier d’en-tête à l’application hôte au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="7c66c-135">Generate a resource file called <resourceFile> that links all image and string resources, the binary markup file, and the header file to the host application at build time.</span></span> <span data-ttu-id="7c66c-136">En cas d’omission, un fichier de ressources n’est pas généré.</span><span class="sxs-lookup"><span data-stu-id="7c66c-136">If omitted, a resource file is not generated.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c66c-137">/Name<ribbonName></span><span class="sxs-lookup"><span data-stu-id="7c66c-137">/name:<ribbonName></span></span></td>
<td><span data-ttu-id="7c66c-138">Nom de la ressource pour le fichier de balisage binaire qui est enregistré dans le <resourceFile> .</span><span class="sxs-lookup"><span data-stu-id="7c66c-138">The resource name for the binary markup file that is logged in the <resourceFile>.</span></span> <span data-ttu-id="7c66c-139">La valeur par défaut est APPLICATION_RIBBON.</span><span class="sxs-lookup"><span data-stu-id="7c66c-139">The default is APPLICATION_RIBBON.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c66c-140">/W{0\1\2}</span><span class="sxs-lookup"><span data-stu-id="7c66c-140">/W{0\1\2}</span></span></td>
<td><span data-ttu-id="7c66c-141">Filtrer les messages d’événement en fonction de leur gravité.</span><span class="sxs-lookup"><span data-stu-id="7c66c-141">Filter the event messages based on severity.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7c66c-142">0</span><span class="sxs-lookup"><span data-stu-id="7c66c-142">0</span></span><br/></td>
<td><span data-ttu-id="7c66c-143">Messages d'erreur uniquement.</span><span class="sxs-lookup"><span data-stu-id="7c66c-143">Error messages only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c66c-144">1</span><span class="sxs-lookup"><span data-stu-id="7c66c-144">1</span></span><br/></td>
<td><span data-ttu-id="7c66c-145">Messages d’erreur et d’avertissement uniquement.</span><span class="sxs-lookup"><span data-stu-id="7c66c-145">Error and Warning messages only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c66c-146"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="7c66c-146"><strong>2</strong></span></span><br/></td>
<td><span data-ttu-id="7c66c-147">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="7c66c-147">Default.</span></span> <br/> <span data-ttu-id="7c66c-148">Messages d’erreur, d’avertissement et d’information.</span><span class="sxs-lookup"><span data-stu-id="7c66c-148">Error, Warning, and Informational messages.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a><span data-ttu-id="7c66c-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c66c-149">Example</span></span>

<span data-ttu-id="7c66c-150">L’exemple suivant montre comment utiliser le compilateur de balisage du ruban pour générer un ensemble classique de fichiers de ressources pour une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="7c66c-150">The following example demonstrates how to use the Ribbon markup compiler to generate a typical set of resource files for a Ribbon application.</span></span>

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a><span data-ttu-id="7c66c-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c66c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c66c-152">Déclaration des commandes et des contrôles avec le balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="7c66c-152">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="7c66c-153">Création d’une application de ruban</span><span class="sxs-lookup"><span data-stu-id="7c66c-153">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





