---
title: Ajout d’une sélection
description: Ajout d’une sélection
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- création d’apparences, de sélections
- Apparences du lecteur Windows Media, sélections
- apparences, sélections
- sélections, habillages
- sélections de métafichiers, apparences
- Sélections de métafichiers Windows Media, apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106540753"
---
# <a name="adding-a-playlist"></a><span data-ttu-id="60c40-109">Ajout d’une sélection</span><span class="sxs-lookup"><span data-stu-id="60c40-109">Adding a Playlist</span></span>

<span data-ttu-id="60c40-110">Vous pouvez utiliser les sélections pour choisir parmi les collections de vos données audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="60c40-110">You can use playlists to choose from collections of your audio and video.</span></span>

<span data-ttu-id="60c40-111">À l’aide de l’illustration de votre première apparence, vous pouvez apporter quelques modifications au fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="60c40-111">Using the artwork from your first skin, you can make a few changes to the skin definition file.</span></span>

<span data-ttu-id="60c40-112">La première étape consiste à utiliser l’interpréteur de commandes que vous allez utiliser pour la plupart des habillages :</span><span class="sxs-lookup"><span data-stu-id="60c40-112">The first step is to use the shell you will use for most skins:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



<span data-ttu-id="60c40-113">Ajoutez maintenant une deuxième **vue**, qui contient une sélection.</span><span class="sxs-lookup"><span data-stu-id="60c40-113">Now add a second **VIEW**, which contains a playlist.</span></span> <span data-ttu-id="60c40-114">Placez le code suivant après le </VIEW> du code Shell.</span><span class="sxs-lookup"><span data-stu-id="60c40-114">Place the following code after the </VIEW> of the shell code.</span></span>


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



<span data-ttu-id="60c40-115">Vous devez donner à cette deuxième vue un ID pour pouvoir vous y référer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="60c40-115">You will need to give this second view an ID so you can refer to it later.</span></span> <span data-ttu-id="60c40-116">Ajoutez un PLAYELEMENT et un STOPELEMENT.</span><span class="sxs-lookup"><span data-stu-id="60c40-116">Add a PLAYELEMENT and a STOPELEMENT.</span></span> <span data-ttu-id="60c40-117">Ces boutons prédéfinis facilitent la vie.</span><span class="sxs-lookup"><span data-stu-id="60c40-117">These predefined buttons make life easier.</span></span>


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



<span data-ttu-id="60c40-118">Enfin, ajoutez un événement onClick à PLAYELEMENT pour afficher une sélection dans la deuxième vue :</span><span class="sxs-lookup"><span data-stu-id="60c40-118">Finally, add an onClick event to the PLAYELEMENT to display a playlist in the second view:</span></span>


```C++
            onClick = "JScript: theme.openView('playview');" />

```



<span data-ttu-id="60c40-119">Vous pouvez voir une apparence de sélection de travail similaire dans la section exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="60c40-119">You can see a similar working playlist skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60c40-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60c40-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60c40-121">**Guide de création d’apparence**</span><span class="sxs-lookup"><span data-stu-id="60c40-121">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




