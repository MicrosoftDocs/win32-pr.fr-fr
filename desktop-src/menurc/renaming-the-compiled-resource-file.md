---
title: Attribution d’un nouveau nom au fichier de ressources compilé
description: Par défaut, lors de la compilation des ressources, RC nomme le fichier de ressources compilé (. res) avec le nom de base du fichier. RC et le place dans le même répertoire que le fichier. rc.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190810"
---
# <a name="renaming-the-compiled-resource-file"></a><span data-ttu-id="9f7f9-103">Attribution d’un nouveau nom au fichier de ressources compilé</span><span class="sxs-lookup"><span data-stu-id="9f7f9-103">Renaming the Compiled Resource File</span></span>

<span data-ttu-id="9f7f9-104">Par défaut, lors de la compilation des ressources, RC nomme le fichier de ressources compilé (. res) avec le nom de base du fichier. RC et le place dans le même répertoire que le fichier. rc.</span><span class="sxs-lookup"><span data-stu-id="9f7f9-104">By default, when compiling resources, RC names the compiled resource (.res) file with the base name of the .rc file and places it in the same directory as the .rc file.</span></span> <span data-ttu-id="9f7f9-105">CVTRES doit ensuite être appelé pour convertir le fichier. res en un format de ressource binaire (. RBJ) qui peut être compris par l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="9f7f9-105">CVTRES must then be invoked to convert the .res file to a binary resource (.rbj) format which can be understood by the linker.</span></span> <span data-ttu-id="9f7f9-106">L’exemple suivant compile MyApp. RC et crée un fichier de ressources compilé nommé MyApp. res dans le même répertoire que MyApp. RC :</span><span class="sxs-lookup"><span data-stu-id="9f7f9-106">The following example compiles MyApp.rc and creates a compiled resource file named MyApp.res in the same directory as MyApp.rc:</span></span>

<span data-ttu-id="9f7f9-107">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="9f7f9-107">**rc myapp.rc**</span></span>

<span data-ttu-id="9f7f9-108">L’option **/FO** donne au fichier. res qui en résulte un nom différent du nom du fichier. RC correspondant.</span><span class="sxs-lookup"><span data-stu-id="9f7f9-108">The **/fo** option gives the resulting .res file a name that differs from the name of the corresponding .rc file.</span></span> <span data-ttu-id="9f7f9-109">Par exemple, pour nommer le fichier. res obtenu NewFile. res, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9f7f9-109">For example, to name the resulting .res file NewFile.res, use the following command:</span></span>

<span data-ttu-id="9f7f9-110">**RC-fo newFile. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="9f7f9-110">**rc -fo newfile.res myapp.rc**</span></span>

<span data-ttu-id="9f7f9-111">L’option **/FO** peut également placer le fichier. res dans un répertoire différent.</span><span class="sxs-lookup"><span data-stu-id="9f7f9-111">The **/fo** option can also place the .res file in a different directory.</span></span> <span data-ttu-id="9f7f9-112">Par exemple, la commande suivante place le fichier de ressources compilé MyApp. res dans le répertoire C : \\ source Resource \\ :</span><span class="sxs-lookup"><span data-stu-id="9f7f9-112">For example, the following command places the compiled resource file MyApp.res in the directory C:\\Source\\Resource:</span></span>

<span data-ttu-id="9f7f9-113">**RC-fo c : \\ \\ ressource source \\ MyApp. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="9f7f9-113">**rc -fo c:\\source\\resource\\myapp.res myapp.rc**</span></span>

 

 




