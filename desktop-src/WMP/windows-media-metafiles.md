---
title: Fichiers Windows Media
description: Fichiers Windows Media
ms.assetid: 77af7d15-52ac-496c-8037-51827adf0250
keywords:
- Fichiers Windows Media, à propos de
- Lecteur Windows Media, fichiers
- Windows Media Player, Windows Media
- refichiers, à propos de
- Windows Media, sous-fichiers
- Sélections de métafichiers Windows Media, à propos de
- sélections, à propos de
- sélections de métafichiers, à propos de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 385b149e07e9d30df4e11a21f8e7aa4b05e06910
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310066"
---
# <a name="windows-media-metafiles"></a><span data-ttu-id="5ed7b-111">Fichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="5ed7b-111">Windows Media Metafiles</span></span>

<span data-ttu-id="5ed7b-112">Cette référence décrit les fichiers Windows Media, qui utilisent les extensions de nom de fichier. Wax,. wvx,. WMX et. asx.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-112">This reference documents Windows Media metafiles, which use the .wax, .wvx, .wmx, and .asx file name extensions.</span></span> <span data-ttu-id="5ed7b-113">Elle contient des sections de présentation et de guide de programmation, ainsi qu’une section de référence complète sur les balises d’élément de métafichier, leurs attributs et leurs valeurs, et les conditions spéciales associées à chaque élément.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-113">It contains overview and programming guide sections, and a full reference section on metafile element tags, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="5ed7b-114">Un métafichier est un fichier qui contient des informations sur d’autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-114">A metafile is a file that contains information about other files.</span></span> <span data-ttu-id="5ed7b-115">Un métafichier peut être utilisé pour répertorier un groupe de fichiers de contenu multimédia qui doivent être lus dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-115">A metafile can be used to list a group of media content files that are to be played in order.</span></span> <span data-ttu-id="5ed7b-116">Les sélections de métafichiers Windows Media, simplement appelées « playlists » dans ce document de référence, sont l’une des fonctionnalités les plus puissantes des technologies Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-116">Windows Media metafile playlists, simply referred to as playlists in this reference document, are one of the most powerful features of Microsoft Windows Media Technologies.</span></span> <span data-ttu-id="5ed7b-117">Les sélections vous permettent de contrôler et de personnaliser votre contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-117">Playlists allow you to control and customize your media content.</span></span> <span data-ttu-id="5ed7b-118">Par exemple, avec des sélections, vous pouvez planifier le contenu pour qu’il s’exécute à la suite ou insérer des éléments de publicité ou d’intérêt particulier dans une présentation.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-118">For instance, with playlists you can schedule content to play in succession or insert advertising or special interest clips into a presentation.</span></span> <span data-ttu-id="5ed7b-119">Un autre avantage des sélections est qu’au lieu de lire un flux, d’arrêter, de démarrer le flux suivant, puis d’attendre qu’il termine la mise en mémoire tampon, Windows Media Services et le lecteur Windows Media fonctionnent ensemble pour lire les clips l’un après l’autre, avec un temps de mise en mémoire tampon minimal ou une interruption entre eux.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-119">A further advantage of playlists is that instead of playing a stream, stopping, starting the next stream, and then waiting for it to finish buffering, Windows Media Services and Windows Media Player work together to play the clips one after the other with minimal buffering time or interruption between them.</span></span>

<span data-ttu-id="5ed7b-120">Les technologies Windows Media et d’autres produits Internet vous fournissent les outils nécessaires pour comprendre les données démographiques des utilisateurs et personnaliser dynamiquement une diffusion ou un message pour des utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-120">Windows Media Technologies and other Internet products provide you with the tools to understand user demographics and dynamically customize a broadcast or message for individual users.</span></span>

<span data-ttu-id="5ed7b-121">Cette référence est divisée en sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-121">This reference is divided into the following sections.</span></span>



| <span data-ttu-id="5ed7b-122">Section</span><span class="sxs-lookup"><span data-stu-id="5ed7b-122">Section</span></span>                                                                  | <span data-ttu-id="5ed7b-123">Description</span><span class="sxs-lookup"><span data-stu-id="5ed7b-123">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ed7b-124">À propos des fichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="5ed7b-124">About Windows Media Metafiles</span></span>](about-windows-media-metafiles.md)       | <span data-ttu-id="5ed7b-125">Présente les éléments du métafichier Windows Media et en présente le but.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-125">Introduces Windows Media metafile elements and discusses their purpose.</span></span>                                                                                                             |
| [<span data-ttu-id="5ed7b-126">Guide des métafichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="5ed7b-126">Windows Media Metafile Guide</span></span>](windows-media-metafile-guide.md)         | <span data-ttu-id="5ed7b-127">Décrit en détail les étapes nécessaires à la création de sous-fichiers.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-127">Details the steps necessary for creating metafiles.</span></span> <span data-ttu-id="5ed7b-128">Des exemples montrent comment utiliser des balises d’élément pour des tâches spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-128">Examples illustrate how to use element tags for specific tasks.</span></span>                                                                 |
| [<span data-ttu-id="5ed7b-129">Informations de référence sur les métafichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="5ed7b-129">Windows Media Metafile Reference</span></span>](windows-media-metafile-reference.md) | <span data-ttu-id="5ed7b-130">Explique en détail chacun des éléments de métafichier, leurs attributs et leurs valeurs, ainsi que les conditions spéciales associées à chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-130">Explains in detail each of the metafile elements, their attributes and values, and special conditions related to each.</span></span> <span data-ttu-id="5ed7b-131">Décrit les extensions de nom de fichier de métafichier et leur utilisation appropriée.</span><span class="sxs-lookup"><span data-stu-id="5ed7b-131">Explains metafile file name extensions and their proper use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5ed7b-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ed7b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed7b-133">**SDK du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5ed7b-133">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




