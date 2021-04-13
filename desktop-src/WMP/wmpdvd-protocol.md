---
title: Protocole WMPDVD
description: Protocole WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Lecteur Windows Media, protocoles
- Modèle d’objet du lecteur Windows Media, protocoles
- modèle objet, protocoles
- Contrôle ActiveX du lecteur Windows Media, protocoles pour le modèle objet
- Contrôle ActiveX, protocoles pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, protocoles pour le modèle objet
- Windows Media Player Mobile, protocoles pour le modèle objet
- protocoles, modèle objet du lecteur Windows Media
- protocoles, WMPDVD
- Protocole WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309873"
---
# <a name="wmpdvd-protocol"></a><span data-ttu-id="ec4ad-113">Protocole WMPDVD</span><span class="sxs-lookup"><span data-stu-id="ec4ad-113">WMPDVD Protocol</span></span>

<span data-ttu-id="ec4ad-114">Le protocole WMPDVD vous permet de spécifier un média à partir d’un DVD à l’aide de la syntaxe d’URL.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-114">The WMPDVD protocol enables you to specify media from a DVD using URL syntax.</span></span> <span data-ttu-id="ec4ad-115">Il s’agit de la forme générale du protocole :</span><span class="sxs-lookup"><span data-stu-id="ec4ad-115">This is the general form of the protocol:</span></span>


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



<span data-ttu-id="ec4ad-116">Le segment de *lecteur* est la lettre du lecteur de DVD ; elle n’inclut pas les deux-points généralement utilisés avec les spécificateurs de lecteur.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-116">The *drive* segment is the letter of the DVD drive; it does not include the colon typically used with drive specifiers.</span></span> <span data-ttu-id="ec4ad-117">Ce segment est toujours requis.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-117">This segment is always required.</span></span>

<span data-ttu-id="ec4ad-118">Le segment de *titre* est le numéro du titre à lire.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-118">The *title* segment is the number of the title to play.</span></span> <span data-ttu-id="ec4ad-119">Ce n’est pas obligatoire, sauf si vous souhaitez commencer la lecture à un titre spécifique ou à un chapitre spécifique d’un titre spécifique.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-119">It is not required unless you want to start playback at a specific title or at a specific chapter of a specific title.</span></span>

<span data-ttu-id="ec4ad-120">Le segment de *chapitre* est le numéro du chapitre à lire.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-120">The *chapter* segment is the number of the chapter to play.</span></span> <span data-ttu-id="ec4ad-121">Ce n’est pas obligatoire, sauf si vous souhaitez démarrer la lecture dans un chapitre spécifique d’un titre spécifique.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-121">It is not required unless you want to start playback at a specific chapter of a specific title.</span></span>

<span data-ttu-id="ec4ad-122">L’argument contentdir est le chemin d’accès à une vidéo \_ TS. Fichier IFO, qui peut être dans un stockage local ou sur un partage réseau.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-122">The contentdir argument is the path to a VIDEO\_TS.IFO file, which may be in local storage or on a network share.</span></span> <span data-ttu-id="ec4ad-123">Si vous incluez ce segment, le segment de *lecteur* est ignoré, même s’il est toujours requis.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-123">If you include this segment, then the *drive* segment is ignored although it is still required.</span></span> <span data-ttu-id="ec4ad-124">Si vous incluez également le segment de *titre* ou les segments de *titre* et de *chapitre* , ils sont relatifs au contenu de DVD spécifié dans le segment contentdir, et non au segment de *disque* .</span><span class="sxs-lookup"><span data-stu-id="ec4ad-124">If you also include the *title* segment or both the *title* and *chapter* segments then they are relative to the DVD content specified in the contentdir segment, not the *drive* segment.</span></span>

<span data-ttu-id="ec4ad-125">L’exemple suivant utilise le protocole WMPDVD pour lire le DVD depuis le début, comme s’il démarrait automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-125">The following example uses the WMPDVD protocol to play the DVD from the beginning, as if it were starting automatically.</span></span>


```C++
player.url = "wmpdvd://F";
```



<span data-ttu-id="ec4ad-126">L’exemple suivant utilise le protocole WMPDVD pour lire le DVD à partir du début du titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-126">The following example uses the WMPDVD protocol to play the DVD from the beginning of the specified title.</span></span>


```C++
player.url = "wmpdvd://F/2";
```



<span data-ttu-id="ec4ad-127">L’exemple suivant utilise le protocole WMPDVD pour lire le DVD à partir du chapitre spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-127">The following example uses the WMPDVD protocol to play the DVD from the specified chapter.</span></span>


```C++
player.url = "wmpdvd://F/2/4";
```



<span data-ttu-id="ec4ad-128">L’exemple suivant utilise le protocole WMPDVD pour lire du contenu DVD à partir du stockage local.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-128">The following example uses the WMPDVD protocol to play DVD content from local storage.</span></span> <span data-ttu-id="ec4ad-129">La chaîne de *chemin d’accès* se termine par le dossier qui contient la vidéo \_ TS. Fichier IFO ; elle n’inclut pas le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-129">The *path* string ends with the folder that contains the VIDEO\_TS.IFO file; it does not include the file name.</span></span> <span data-ttu-id="ec4ad-130">Dans cet exemple, la valeur du segment de *lecteur* n’a aucun effet, bien qu’elle soit requise, et la lecture commence au chapitre 4 du titre 2.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-130">In this example, the value of the *drive* segment has no effect although it is required, and playback begins in chapter 4 of title 2.</span></span>


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



<span data-ttu-id="ec4ad-131">L’attribution d’une chaîne WMPDVD à la propriété **URL** requiert le lecteur Windows Media 9 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-131">Assigning a WMPDVD string to the **url** property requires Windows Media Player 9 Series or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec4ad-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec4ad-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec4ad-133">**Protocoles et types de fichiers pris en charge**</span><span class="sxs-lookup"><span data-stu-id="ec4ad-133">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




