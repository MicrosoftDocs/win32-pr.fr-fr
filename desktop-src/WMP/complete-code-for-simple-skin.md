---
title: Code complet pour la peau simple
description: Code complet pour la peau simple
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- créer des apparences, des exemples de code
- Apparences du lecteur Windows Media, exemples de code
- apparences, exemples de code
- fichiers de définition d’apparence, exemples de code
- création d’apparences, exemples
- Apparences du lecteur Windows Media, exemples
- Skins, exemples
- fichiers de définition d’apparence, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840326"
---
# <a name="complete-code-for-simple-skin"></a><span data-ttu-id="3a08a-111">Code complet pour la peau simple</span><span class="sxs-lookup"><span data-stu-id="3a08a-111">Complete Code for Simple Skin</span></span>

<span data-ttu-id="3a08a-112">Voici le code complet pour le premier exemple d’apparence :</span><span class="sxs-lookup"><span data-stu-id="3a08a-112">Here is the complete code for the first sample skin:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



<span data-ttu-id="3a08a-113">Vous avez maintenant tous les éléments réunis.</span><span class="sxs-lookup"><span data-stu-id="3a08a-113">Now you have all the pieces put together.</span></span>

<span data-ttu-id="3a08a-114">Créez un fichier compressé avec une extension de nom de fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="3a08a-114">Create a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="3a08a-115">Ce fichier compressé contient votre fichier de définition d’apparence, vos bitmaps et tous les fichiers multimédias numériques que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="3a08a-115">This compressed file contains your skin definition file, bitmaps, and any digital media files you want to include.</span></span> <span data-ttu-id="3a08a-116">Renommez le fichier afin qu’il ait une extension de nom de fichier. WMZ.</span><span class="sxs-lookup"><span data-stu-id="3a08a-116">Rename the file so that it has a .wmz file name extension.</span></span> <span data-ttu-id="3a08a-117">Ensuite, double-cliquez sur l’apparence compressée pour la lancer.</span><span class="sxs-lookup"><span data-stu-id="3a08a-117">Then double-clicking your compressed skin will start it playing.</span></span>

<span data-ttu-id="3a08a-118">Vous pouvez voir une apparence simple de travail similaire dans la section exemples du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="3a08a-118">You can see a similar working simple skin in the samples section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a08a-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a08a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a08a-120">**Création du fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="3a08a-120">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




