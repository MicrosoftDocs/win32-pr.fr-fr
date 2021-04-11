---
title: Choix des fichiers
description: Choix des fichiers
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- création d’apparences, sélection de fichiers
- Apparences du lecteur Windows Media, choix des fichiers
- apparences, choix des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197220"
---
# <a name="choosing-files"></a><span data-ttu-id="8a7cc-106">Choix des fichiers</span><span class="sxs-lookup"><span data-stu-id="8a7cc-106">Choosing Files</span></span>

<span data-ttu-id="8a7cc-107">Si vous souhaitez choisir un fichier, vous pouvez utiliser du code similaire à l’exemple de sélection, mais substituez ce qui suit à la section PLAYELEMENT :</span><span class="sxs-lookup"><span data-stu-id="8a7cc-107">If you want to choose a file, you can use code similar to the Playlist example, but substitute the following for the PLAYELEMENT section:</span></span>


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



<span data-ttu-id="8a7cc-108">Cette ligne utilise la méthode **openDialog** de **thème** pour définir une **URL** pour le lecteur.</span><span class="sxs-lookup"><span data-stu-id="8a7cc-108">This line will use the **openDialog** method of **THEME** to define a **URL** for the player.</span></span> <span data-ttu-id="8a7cc-109">Vous pouvez l’utiliser pour choisir des fichiers qui ne se trouvent pas dans les sélections.</span><span class="sxs-lookup"><span data-stu-id="8a7cc-109">You can use this to choose files that are not in playlists.</span></span>

<span data-ttu-id="8a7cc-110">Vous pouvez voir un exemple de **openDialog** de travail similaire dans la section exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="8a7cc-110">You can see a similar working **openDialog** example in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a7cc-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a7cc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a7cc-112">**Guide de création d’apparence**</span><span class="sxs-lookup"><span data-stu-id="8a7cc-112">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




