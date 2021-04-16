---
title: Appel de fonctions
description: Appel de fonctions
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Apparences du lecteur Windows Media, appel de fonctions dans JScript
- apparences, appeler des fonctions dans JScript
- appel de fonctions dans JScript
- Fichiers JScript pour les apparences, appels de fonctions
- Apparences du lecteur Windows Media, attribut scriptFile en JScript
- Skins, attribut scriptFile dans JScript
- attributs, scriptFile en JScript
- attribut scriptFile dans JScript
- Fichiers JScript pour les apparences, attribut scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507442"
---
# <a name="calling-functions"></a><span data-ttu-id="e8473-112">Appel de fonctions</span><span class="sxs-lookup"><span data-stu-id="e8473-112">Calling Functions</span></span>

<span data-ttu-id="e8473-113">Si vous devez appeler plus de quelques lignes de code, vous pouvez charger un fichier de script à l’aide de l’attribut **scriptFile** de l’élément **View** , puis appeler les fonctions dans le script.</span><span class="sxs-lookup"><span data-stu-id="e8473-113">If you need to call more than a few lines of code, you can load a script file using the **scriptFile** attribute of the **VIEW** element, and call the functions in the script.</span></span> <span data-ttu-id="e8473-114">Vous pouvez charger plusieurs fichiers par vue :</span><span class="sxs-lookup"><span data-stu-id="e8473-114">You can load more than one file per view:</span></span>


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



<span data-ttu-id="e8473-115">Une fois les fichiers de script chargés, vous pouvez appeler les fonctions qu’ils contiennent à partir de la section de votre vue.</span><span class="sxs-lookup"><span data-stu-id="e8473-115">After the script files are loaded, you can call functions in them from inside your View section.</span></span> <span data-ttu-id="e8473-116">Par exemple, pour appeler une fonction appelée *MyFunction* quand un utilisateur clique sur un événement, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e8473-116">For example, to call a function called *myfunction* when something is clicked, type the following:</span></span>


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> <span data-ttu-id="e8473-117">Si vous avez plusieurs vues, seules les fonctions des fichiers chargés dans l’affichage actuel sont disponibles pour le code XML et JScript s’exécutant avec la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="e8473-117">If you have more than one view, only the functions in files loaded into the current view are available to the XML and JScript code running with the current view.</span></span> <span data-ttu-id="e8473-118">Les fichiers chargés dans d’autres vues ne sont pas dans la portée de l’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="e8473-118">Files loaded in other views are not in scope with the current view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e8473-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8473-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8473-120">**Utilisation de JScript**</span><span class="sxs-lookup"><span data-stu-id="e8473-120">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




