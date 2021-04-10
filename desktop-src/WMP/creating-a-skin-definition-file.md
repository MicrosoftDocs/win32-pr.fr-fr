---
title: Création d’un fichier de définition d’apparence
description: Création d’un fichier de définition d’apparence
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player Mobile Skins, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, création
- créer des apparences, à propos de
- création d’apparences, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674014"
---
# <a name="creating-a-skin-definition-file"></a><span data-ttu-id="300f6-109">Création d’un fichier de définition d’apparence</span><span class="sxs-lookup"><span data-stu-id="300f6-109">Creating a Skin Definition File</span></span>

<span data-ttu-id="300f6-110">Un fichier de définition d’apparence est un fichier texte qui définit une apparence et tous ses éléments composites.</span><span class="sxs-lookup"><span data-stu-id="300f6-110">A skin definition file is a text file that defines a skin and all its composite parts.</span></span> <span data-ttu-id="300f6-111">L’extension de nom de fichier doit être. skn.</span><span class="sxs-lookup"><span data-stu-id="300f6-111">The file name extension must be .skn.</span></span>

<span data-ttu-id="300f6-112">Chaque fichier de définition d’apparence doit commencer par la ligne suivante, qui spécifie le numéro de version du fichier d’apparence.</span><span class="sxs-lookup"><span data-stu-id="300f6-112">Every skin definition file must start with the following line, which specifies the skin file version number.</span></span> <span data-ttu-id="300f6-113">Le tableau suivant présente les versions du lecteur Windows Media et la ligne de code qui doit être utilisée pour identifier chacune d’elles dans un fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="300f6-113">The following table shows Windows Media Player versions and the code line that should be used to identify each in a skin definition file.</span></span> <span data-ttu-id="300f6-114">Bien que certains nombres dans les lignes de code ne soient pas conformes à vos attentes, ils sont corrects, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="300f6-114">Although some of the numbers in the code lines are not what you would expect, they are correct as shown in the following table.</span></span>



| <span data-ttu-id="300f6-115">Version du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="300f6-115">Windows Media Player version</span></span> | <span data-ttu-id="300f6-116">Première ligne du fichier de définition d’apparence</span><span class="sxs-lookup"><span data-stu-id="300f6-116">First line of skin definition file</span></span> |
|------------------------------|------------------------------------|
| <span data-ttu-id="300f6-117">1.01.1</span><span class="sxs-lookup"><span data-stu-id="300f6-117">1.01.1</span></span><br/>            | <span data-ttu-id="300f6-118">\[Fichier d’apparence Pocket WMP v 1.0\]</span><span class="sxs-lookup"><span data-stu-id="300f6-118">\[Pocket WMP Skin File v1.0\]</span></span>      |
| <span data-ttu-id="300f6-119">1.2</span><span class="sxs-lookup"><span data-stu-id="300f6-119">1.2</span></span>                          | <span data-ttu-id="300f6-120">\[Fichier d’apparence Pocket WMP v 1.2\]</span><span class="sxs-lookup"><span data-stu-id="300f6-120">\[Pocket WMP Skin File v1.2\]</span></span>      |
| <span data-ttu-id="300f6-121">7.0</span><span class="sxs-lookup"><span data-stu-id="300f6-121">7.0</span></span>                          | <span data-ttu-id="300f6-122">\[Fichier d’apparence Pocket WMP v 2.0\]</span><span class="sxs-lookup"><span data-stu-id="300f6-122">\[Pocket WMP Skin File v2.0\]</span></span>      |
| <span data-ttu-id="300f6-123">7.1</span><span class="sxs-lookup"><span data-stu-id="300f6-123">7.1</span></span>                          | <span data-ttu-id="300f6-124">\[Fichier d’apparence Pocket WMP v 8.0\]</span><span class="sxs-lookup"><span data-stu-id="300f6-124">\[Pocket WMP Skin File v8.0\]</span></span>      |
| <span data-ttu-id="300f6-125">série 9</span><span class="sxs-lookup"><span data-stu-id="300f6-125">9 Series</span></span>                     | <span data-ttu-id="300f6-126">\[Fichier d’apparence Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="300f6-126">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="300f6-127">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="300f6-127">10 Mobile</span></span>                    | <span data-ttu-id="300f6-128">\[Fichier d’apparence Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="300f6-128">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="300f6-129">10,1 mobile</span><span class="sxs-lookup"><span data-stu-id="300f6-129">10.1 Mobile</span></span>                  | <span data-ttu-id="300f6-130">\[Fichier d’apparence Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="300f6-130">\[Pocket WMP Skin File v9.0.1\]</span></span>    |



 

<span data-ttu-id="300f6-131">Le numéro de version 9.0.1 est destiné aux apparences créées spécifiquement pour le lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="300f6-131">The version number 9.0.1 is for skins created specifically for Windows Media Player 9 Series or later.</span></span> <span data-ttu-id="300f6-132">Les enveloppes ayant un numéro de version antérieure sont ouvertes par le lecteur Windows Media série 9 ou une version ultérieure en mode portrait, 96 points par pouce (DPI).</span><span class="sxs-lookup"><span data-stu-id="300f6-132">Skins having an earlier version number are opened by Windows Media Player 9 Series or later as portrait mode, 96 dots per inch (DPI) skins.</span></span>

<span data-ttu-id="300f6-133">Le fichier de définition d’apparence est constitué de plusieurs sections.</span><span class="sxs-lookup"><span data-stu-id="300f6-133">The skin definition file consists of several sections.</span></span> <span data-ttu-id="300f6-134">Chaque section définit une zone particulière de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="300f6-134">Each section defines a particular area of the skin.</span></span> <span data-ttu-id="300f6-135">Les sections doivent être placées dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="300f6-135">The sections must be placed in the following order:</span></span>

1.  <span data-ttu-id="300f6-136">Description</span><span class="sxs-lookup"><span data-stu-id="300f6-136">Description</span></span>
2.  <span data-ttu-id="300f6-137">Images bitmap</span><span class="sxs-lookup"><span data-stu-id="300f6-137">Bitmaps</span></span>
3.  <span data-ttu-id="300f6-138">Vidéo</span><span class="sxs-lookup"><span data-stu-id="300f6-138">Video</span></span>
4.  <span data-ttu-id="300f6-139">Boutons</span><span class="sxs-lookup"><span data-stu-id="300f6-139">Buttons</span></span>
5.  <span data-ttu-id="300f6-140">Statut</span><span class="sxs-lookup"><span data-stu-id="300f6-140">Status</span></span>
6.  <span data-ttu-id="300f6-141">Texte</span><span class="sxs-lookup"><span data-stu-id="300f6-141">Text</span></span>
7.  <span data-ttu-id="300f6-142">Chapiteau</span><span class="sxs-lookup"><span data-stu-id="300f6-142">Marquee</span></span>
8.  <span data-ttu-id="300f6-143">Trackbars</span><span class="sxs-lookup"><span data-stu-id="300f6-143">Trackbars</span></span>

<span data-ttu-id="300f6-144">Chaque section commence par le nom de la section entre crochets, par exemple :</span><span class="sxs-lookup"><span data-stu-id="300f6-144">Each section starts with the name of the section in square brackets, for example:</span></span>


```C++
[ Bitmaps ]

```



> [!Note]  
> <span data-ttu-id="300f6-145">Votre fichier de définition d’apparence n’est pas analysé correctement sauf si vous incluez des espaces entre les crochets et le nom de la section.</span><span class="sxs-lookup"><span data-stu-id="300f6-145">Your skin definition file will not be parsed correctly unless you include spaces between the brackets and the name of the section.</span></span>

 

<span data-ttu-id="300f6-146">Ensuite, une ou plusieurs lignes définissent des images, des boutons et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="300f6-146">Then, one or more lines define individual images, buttons, and so on.</span></span> <span data-ttu-id="300f6-147">Par exemple, une section bitmaps peut inclure les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="300f6-147">For example, a Bitmaps section might include the following:</span></span>


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="300f6-148">Il n’est pas nécessaire d’aligner les valeurs dans les colonnes, mais cela permet d’améliorer la lisibilité de votre code.</span><span class="sxs-lookup"><span data-stu-id="300f6-148">It is not necessary to line up the values in columns, but it will help your code to be more readable.</span></span> <span data-ttu-id="300f6-149">Pour plus d’informations sur chaque section du fichier de définition d’apparence, consultez la référence de l' [apparence](skin-reference.md).</span><span class="sxs-lookup"><span data-stu-id="300f6-149">For more details about each section of the skin definition file, see the [Skin Reference](skin-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="300f6-150">N’utilisez pas d’onglets n’importe où dans le fichier ; Utilisez à la place des espaces supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="300f6-150">Do not use tabs anywhere in the file; use extra spaces instead.</span></span> <span data-ttu-id="300f6-151">C’est très important, car l’utilisation de la touche TAB lors de l’écriture ou de la modification de votre fichier de définition d’apparence entraîne l’échec de la totalité de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="300f6-151">This is very important, because pressing the TAB key while writing or editing your skin definition file will cause the entire skin to fail.</span></span> <span data-ttu-id="300f6-152">Chaque ligne doit être terminée et ne peut pas se poursuivre sur une deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="300f6-152">Each line must be complete and cannot continue onto a second line.</span></span> <span data-ttu-id="300f6-153">En outre, la région et les super valeurs sont dépréciées pour les apparences utilisées avec le lecteur Windows Media 10 mobile ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="300f6-153">Also, the Region and Super values are deprecated for skins used with Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="300f6-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="300f6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="300f6-155">**Fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="300f6-155">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 





