---
description: Choix d’un codec vidéo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Choix d’un codec vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201177"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a><span data-ttu-id="75bda-103">Choix d’un codec vidéo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="75bda-103">Choosing a Video Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="75bda-104">L’encodeur Windows Media Video 9 prend en charge trois catégories de sortie encodée : profil principal, profil avancé et image.</span><span class="sxs-lookup"><span data-stu-id="75bda-104">The Windows Media Video 9 Encoder supports three categories of encoded output: Main Profile, Advanced Profile, and Image.</span></span> <span data-ttu-id="75bda-105">La catégorie de profil principale fournit une compression vidéo générale pour un contenu vidéo complexe, tel que des films ou des vidéos musicales.</span><span class="sxs-lookup"><span data-stu-id="75bda-105">The Main Profile category provides general video compression for complex video content, such as movies or music videos.</span></span> <span data-ttu-id="75bda-106">Les fonctionnalités du profil principal fournissent un large éventail de paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="75bda-106">The features of the Main Profile provide for a wide range of encoding settings.</span></span> <span data-ttu-id="75bda-107">Vous pouvez utiliser le profil principal pour créer une vidéo avec des débits très faibles pour la livraison sur des appareils portables ou, à l’autre extrémité du spectre, vous pouvez l’utiliser pour créer une vidéo haute définition pour le cinéma numérique.</span><span class="sxs-lookup"><span data-stu-id="75bda-107">You can use the Main Profile to create video with very low bit rates for delivery on handheld devices or, at the other end of the spectrum, you can use it to create high-definition video for digital cinema.</span></span>

<span data-ttu-id="75bda-108">L’importance des algorithmes d’encodage dans le profil principal est sur le contenu vidéo dynamique, mais ils conviennent également à d’autres contenus vidéo.</span><span class="sxs-lookup"><span data-stu-id="75bda-108">The emphasis of the encoding algorithms in the Main Profile is on dynamic video content, but they are suitable for other video content as well.</span></span> <span data-ttu-id="75bda-109">Le profil principal doit être votre catégorie par défaut pour le contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="75bda-109">The Main Profile should be your default category for video content.</span></span> <span data-ttu-id="75bda-110">Pour répondre à des besoins spécifiques, vous pouvez utiliser la catégorie de profil avancé, la catégorie d’image ou un encodeur distinct appelé « encodeur d’écran Windows Media Video 9 ».</span><span class="sxs-lookup"><span data-stu-id="75bda-110">To meet specific needs, you can use the Advanced Profile category, the Image category, or a separate encoder called the Windows Media Video 9 Screen encoder.</span></span> <span data-ttu-id="75bda-111">Le tableau suivant répertorie les quatre options.</span><span class="sxs-lookup"><span data-stu-id="75bda-111">The following table lists the four options.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75bda-112">Objectif</span><span class="sxs-lookup"><span data-stu-id="75bda-112">Purpose</span></span></th>
<th><span data-ttu-id="75bda-113">Codec</span><span class="sxs-lookup"><span data-stu-id="75bda-113">Codec</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75bda-114">Encodage vidéo à usage général</span><span class="sxs-lookup"><span data-stu-id="75bda-114">General-purpose video encoding</span></span></td>
<td><span data-ttu-id="75bda-115"><a href="windowsmediavideo9encoder.md">Encodeur Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="75bda-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="75bda-116">Profil Main</span><span class="sxs-lookup"><span data-stu-id="75bda-116">Main Profile</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75bda-117">Encodage d’une vidéo ou d’une vidéo haute définition conforme à la norme SMPTE du profil avancé VC-1</span><span class="sxs-lookup"><span data-stu-id="75bda-117">Encoding high definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard</span></span></td>
<td><span data-ttu-id="75bda-118"><a href="windowsmediavideo9encoder.md">Encodeur Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="75bda-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="75bda-119">Profil avancé</span><span class="sxs-lookup"><span data-stu-id="75bda-119">Advanced Profile</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75bda-120">Conversion d’images bitmap en vidéo dynamique</span><span class="sxs-lookup"><span data-stu-id="75bda-120">Converting bitmapped images to dynamic video</span></span></td>
<td><span data-ttu-id="75bda-121"><a href="windowsmediavideo9encoder.md">Encodeur Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="75bda-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="75bda-122">Image</span><span class="sxs-lookup"><span data-stu-id="75bda-122">Image</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75bda-123">Encodage d’une vidéo d’application d’ordinateur (capture d’écran) ou autre vidéo hautement statique</span><span class="sxs-lookup"><span data-stu-id="75bda-123">Encoding computer-application video (screen capture) or other highly static video</span></span></td>
<td><span data-ttu-id="75bda-124"><a href="windowsmediavideo9screenencoder.md"><strong>Encodeur d’écran Windows Media Video 9</strong></a></span><span class="sxs-lookup"><span data-stu-id="75bda-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="75bda-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75bda-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75bda-126">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="75bda-126">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



