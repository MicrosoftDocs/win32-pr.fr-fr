---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Lecteur Windows Media, migration de DVD
- Windows Media Player Object Model, DVD
- modèle objet, DVD
- Contrôle ActiveX du lecteur Windows Media, DVD
- Contrôle ActiveX, DVD
- Windows Media Player Mobile contrôle ActiveX, DVD
- Windows Media Player Mobile, migration de DVD
- Guide de migration, DVD
- Migration de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673950"
---
# <a name="dvd"></a><span data-ttu-id="9b6d3-112">DVD</span><span class="sxs-lookup"><span data-stu-id="9b6d3-112">DVD</span></span>

<span data-ttu-id="9b6d3-113">Le contrôle ActiveX du lecteur Windows Media 6,4 contient un objet **DVD** qui expose une variété de méthodes et de propriétés, et un événement pour traiter spécifiquement le contenu du DVD.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-113">The Windows Media Player 6.4 ActiveX control contains a **DVD** object that exposes a variety of methods and properties, and one event, for dealing specifically with DVD content.</span></span> <span data-ttu-id="9b6d3-114">Par exemple, pour déterminer le nombre de titres de DVD disponibles, vous utilisez **Player6**. propriété **titlesAvailable** :</span><span class="sxs-lookup"><span data-stu-id="9b6d3-114">For instance, to determine the number of DVD titles available, you use the **Player6**.**titlesAvailable** property:</span></span>


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



<span data-ttu-id="9b6d3-115">Le modèle objet Windows Media Player 7 ou version ultérieure implémente une approche plus intégrée du DVD.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-115">The Windows Media Player 7 or later object model implements a more integrated approach to DVD.</span></span> <span data-ttu-id="9b6d3-116">Les propriétés, méthodes et événements spécifiques aux DVD sont implémentés uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-116">DVD-specific properties, methods, and events are implemented only where needed.</span></span> <span data-ttu-id="9b6d3-117">Dans le cas contraire, la fonctionnalité de modèle objet existante fonctionne avec les supports DVD, comme vous pouvez vous y attendre.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-117">Otherwise, existing object model functionality works with DVD media as you might expect.</span></span> <span data-ttu-id="9b6d3-118">Par exemple, pour déterminer le nombre de titres de DVD disponibles lors de l’utilisation du lecteur Windows Media 7 ou version ultérieure, vous récupérez un objet de **sélection** à partir de l’objet **cdrom** :</span><span class="sxs-lookup"><span data-stu-id="9b6d3-118">For example, to determine the number of DVD titles available when using Windows Media Player 7 or later, you retrieve a **Playlist** object from the **Cdrom** object:</span></span>


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



<span data-ttu-id="9b6d3-119">L’exemple précédent récupère un objet **playlist** avec une première entrée représentant le support DVD dans le premier lecteur.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-119">The preceding example retrieves a **Playlist** object with a first entry representing the DVD media in the first drive.</span></span> <span data-ttu-id="9b6d3-120">Les entrées supplémentaires représentent des titres de DVD individuels.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-120">Additional entries represent individual DVD titles.</span></span> <span data-ttu-id="9b6d3-121">Par conséquent, le nombre de titres disponibles peut être calculé comme suit :</span><span class="sxs-lookup"><span data-stu-id="9b6d3-121">Therefore, the number of titles available can be calculated as follows:</span></span>


```C++
var numTitles = dvdTitles.count - 1;

```



<span data-ttu-id="9b6d3-122">Voici les principales différences à prendre en compte lors de la migration à partir de la version 6,4 :</span><span class="sxs-lookup"><span data-stu-id="9b6d3-122">Here are the main differences to keep in mind when migrating from version 6.4:</span></span>

-   <span data-ttu-id="9b6d3-123">La lecture de DVD est prise en charge uniquement lors de l’utilisation du lecteur Windows Media pour Windows XP ou version ultérieure et du système d’exploitation Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-123">DVD playback is supported only when using Windows Media Player for Windows XP or later and the Windows XP operating system or later.</span></span>
-   <span data-ttu-id="9b6d3-124">Les lecteurs de DVD-ROM sont énumérés exactement comme des lecteurs de CD-ROM à l’aide de l’objet **CdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="9b6d3-124">DVD-ROM drives are enumerated exactly like CD-ROM drives using the **CdromCollection** object.</span></span>
-   <span data-ttu-id="9b6d3-125">Les lecteurs de DVD-ROM individuels sont gérés à l’aide de l’objet **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="9b6d3-125">Individual DVD-ROM drives are managed using the **Cdrom** object.</span></span>
-   <span data-ttu-id="9b6d3-126">L’objet **DVD** étend le modèle objet avec les méthodes et une propriété spécifiquement pour l’utilisation de DVD.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-126">The **DVD** object extends the object model with methods and one property specifically for working with DVD.</span></span>
-   <span data-ttu-id="9b6d3-127">Il existe deux nouveaux événements, **OpenPlaylistSwitch** et **DomainChange**, en particulier pour l’utilisation de DVD.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-127">There are two new events, **OpenPlaylistSwitch** and **DomainChange**, specifically for working with DVD.</span></span>
-   <span data-ttu-id="9b6d3-128">Le contenu DVD est organisé à l’aide d’objets de **sélection** et d’objets **multimédias** .</span><span class="sxs-lookup"><span data-stu-id="9b6d3-128">DVD content is organized using **Playlist** objects and **Media** objects.</span></span>
-   <span data-ttu-id="9b6d3-129">Les langues des DVD sont gérées à l’aide des fonctionnalités de langage disponibles à partir de l’objet **contrôles** (Windows Media Player 9 Series ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="9b6d3-129">DVD languages are managed using the language functionality available from the **Controls** object (Windows Media Player 9 Series or later).</span></span>
-   <span data-ttu-id="9b6d3-130">Les contrôles de transport et les informations de position pour le DVD fonctionnent de la même façon que pour les autres types de médias numériques.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-130">Transport controls and position information for DVD work the same as for other digital media types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b6d3-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b6d3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b6d3-132">**Guide de migration du modèle objet**</span><span class="sxs-lookup"><span data-stu-id="9b6d3-132">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="9b6d3-133">**Utilisation du contrôle du lecteur Windows Media avec Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="9b6d3-133">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




