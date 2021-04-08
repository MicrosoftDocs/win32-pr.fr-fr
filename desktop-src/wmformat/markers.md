---
title: Marqueurs
description: Marqueurs
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marqueurs
- ASF (Advanced Systems Format), marqueurs
- ASF (format des systèmes avancés), marqueurs
- marqueurs, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840777"
---
# <a name="markers"></a><span data-ttu-id="082cf-107">Marqueurs</span><span class="sxs-lookup"><span data-stu-id="082cf-107">Markers</span></span>

<span data-ttu-id="082cf-108">Les marqueurs sont des emplacements nommés sur la chronologie d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="082cf-108">Markers are named places on the timeline of an ASF file.</span></span> <span data-ttu-id="082cf-109">Chaque marqueur a un nom et une heure de présentation que vous attribuez.</span><span class="sxs-lookup"><span data-stu-id="082cf-109">Each marker has a name and a presentation time that you assign.</span></span> <span data-ttu-id="082cf-110">Vous pouvez spécifier autant de marqueurs que nécessaire pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="082cf-110">You can specify as many markers as you need for a file.</span></span>

<span data-ttu-id="082cf-111">Les marqueurs sont utiles pour fractionner des fichiers ASF volumineux en éléments logiques.</span><span class="sxs-lookup"><span data-stu-id="082cf-111">Markers are useful for breaking up large ASF files in to logical pieces.</span></span> <span data-ttu-id="082cf-112">Une application qui utilise l’objet lecteur pour lire des fichiers ASF peut fournir à l’utilisateur la possibilité de passer d’un marqueur à un marqueur, ce qui simplifie la navigation dans les médias numériques.</span><span class="sxs-lookup"><span data-stu-id="082cf-112">An application that uses the reader object to play ASF files can provide the user with the option to skip from marker to marker, simplifying navigation of digital media.</span></span> <span data-ttu-id="082cf-113">Par exemple, si vous créez un fichier ASF en dehors d’une présentation, vous pouvez placer des marqueurs dans la chronologie pour chaque sujet principal abordé.</span><span class="sxs-lookup"><span data-stu-id="082cf-113">For example, if you are making an ASF file out of a presentation, you can put markers in the timeline for each major topic that is discussed.</span></span> <span data-ttu-id="082cf-114">Lors de la lecture, au lieu d’obtenir une chronologie longue et de deviner à l’emplacement à rechercher, un utilisateur peut simplement choisir une rubrique dans une liste et aller directement à la partie pertinente du fichier.</span><span class="sxs-lookup"><span data-stu-id="082cf-114">On playback, instead of getting one long timeline and having to guess at the location to seek to, a user can simply pick a topic from a list and go right to the pertinent portion of the file.</span></span>

<span data-ttu-id="082cf-115">Les marqueurs sont manipulés par l’objet de l’éditeur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="082cf-115">Markers are manipulated by the metadata editor object.</span></span> <span data-ttu-id="082cf-116">Vous pouvez ajouter, supprimer et afficher les marqueurs dans un fichier à tout moment une fois que le fichier a été écrit.</span><span class="sxs-lookup"><span data-stu-id="082cf-116">You can add, remove, and view the markers in a file at any time after the file has been written.</span></span>

## <a name="related-topics"></a><span data-ttu-id="082cf-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="082cf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="082cf-118">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="082cf-118">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="082cf-119">**Pour rechercher des marqueurs**</span><span class="sxs-lookup"><span data-stu-id="082cf-119">**To Seek to Markers**</span></span>](to-seek-to-markers.md)
</dt> <dt>

[<span data-ttu-id="082cf-120">**Utilisation des marqueurs**</span><span class="sxs-lookup"><span data-stu-id="082cf-120">**Using Markers**</span></span>](using-markers.md)
</dt> </dl>

 

 




