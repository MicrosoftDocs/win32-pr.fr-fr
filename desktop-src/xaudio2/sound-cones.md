---
description: Modèle qui décrit le niveau sonore du son orienté.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Cônes audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523414"
---
# <a name="sound-cones"></a><span data-ttu-id="4c25e-103">Cônes audio</span><span class="sxs-lookup"><span data-stu-id="4c25e-103">Sound Cones</span></span>

<span data-ttu-id="4c25e-104">Modèle qui décrit le niveau sonore du son orienté.</span><span class="sxs-lookup"><span data-stu-id="4c25e-104">A model that describes the loudness of oriented sound.</span></span>

<span data-ttu-id="4c25e-105">Un son sans orientation a la même amplitude à une distance donnée dans toutes les directions.</span><span class="sxs-lookup"><span data-stu-id="4c25e-105">A sound with no orientation has the same amplitude at a given distance in all directions.</span></span> <span data-ttu-id="4c25e-106">Un son dont l’orientation est la plus forte dans le sens de l’orientation.</span><span class="sxs-lookup"><span data-stu-id="4c25e-106">A sound with an orientation is loudest in the direction of orientation.</span></span> <span data-ttu-id="4c25e-107">Le modèle qui décrit le niveau sonore du son orienté est appelé cône de son.</span><span class="sxs-lookup"><span data-stu-id="4c25e-107">The model that describes the loudness of the oriented sound is called a sound cone.</span></span> <span data-ttu-id="4c25e-108">Les cônes audio sont constitués d’un cône intérieur (ou interne) et d’un cône extérieur (ou externe).</span><span class="sxs-lookup"><span data-stu-id="4c25e-108">Sound cones are made up of an inside (or inner) cone and an outside (or outer) cone.</span></span> <span data-ttu-id="4c25e-109">L’angle du cône extérieur doit toujours être égal ou supérieur à l’angle conique intérieur.</span><span class="sxs-lookup"><span data-stu-id="4c25e-109">The outside cone angle must always be equal to or greater than the inside cone angle.</span></span>

<span data-ttu-id="4c25e-110">À n’importe quel angle dans le cône interne, le volume du son est défini sur le volume de cône interne.</span><span class="sxs-lookup"><span data-stu-id="4c25e-110">At any angle within the inner cone, the volume of the sound is set to the inner cone volume.</span></span> <span data-ttu-id="4c25e-111">Cela prend en compte le volume de base de la mémoire tampon, la distance de l’écouteur, l’orientation de l’écouteur si l’écouteur a son propre cône, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="4c25e-111">This takes into account the basic volume of the buffer, the distance from the listener, the listener's orientation if the listener has its own cone, and so on.</span></span>

<span data-ttu-id="4c25e-112">À tout angle à l’extérieur du cône externe, le volume normal est atténué par un facteur défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="4c25e-112">At any angle outside the outer cone, the normal volume is attenuated by a factor set by the application.</span></span> <span data-ttu-id="4c25e-113">Le niveau de volume du cône extérieur est exprimé sous la forme d’une échelle linéaire de l’amplitude : 1,0 f ne représente aucune atténuation appliquée au signal d’origine, 0,5 f indique une atténuation de 6 dB, et 0,0 f génère un silence.</span><span class="sxs-lookup"><span data-stu-id="4c25e-113">The outside cone volume level is expressed as a linear amplitude scaler: 1.0 f represents no attenuation applied to the original signal, 0.5 f denotes an attenuation of 6 dB, and 0.0 f results in silence.</span></span> <span data-ttu-id="4c25e-114">L’amplification (volume > 1,0 f) est également autorisée et n’est pas ancrée.</span><span class="sxs-lookup"><span data-stu-id="4c25e-114">Amplification (volume > 1.0 f) is also allowed, and is not clamped.</span></span> <span data-ttu-id="4c25e-115">La plage de volumes valide est en fait 0,0 f à 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="4c25e-115">The valid volume range is actually 0.0 f to 2.0 f.</span></span>

<span data-ttu-id="4c25e-116">Entre le cône interne et le cône externe est une zone de transition du volume intérieur au volume extérieur.</span><span class="sxs-lookup"><span data-stu-id="4c25e-116">Between the inner and outer cones is a zone of transition from the inside volume to the outside volume.</span></span> <span data-ttu-id="4c25e-117">Le volume s’approche du volume externe du cône lorsque l’angle augmente.</span><span class="sxs-lookup"><span data-stu-id="4c25e-117">The volume approaches the cone's outer volume as the angle increases.</span></span>

<span data-ttu-id="4c25e-118">Les cônes peuvent affecter des paramètres autres que le volume.</span><span class="sxs-lookup"><span data-stu-id="4c25e-118">Cones can affect parameters other than volume.</span></span> <span data-ttu-id="4c25e-119">Le filtre passe-bas et le niveau d’envoi de réverbération peuvent également être affectés, ce qui rend la technique encore plus spectaculaire.</span><span class="sxs-lookup"><span data-stu-id="4c25e-119">Low pass filter and reverb send level may also be affected, making the technique even more dramatic.</span></span> <span data-ttu-id="4c25e-120">Par exemple, avec un cône sur l’écouteur, vous pouvez spécifier tous les sons situés derrière l’écouteur se trouver un peu atténué, et avoir un contenu de réverbe vers direct légèrement supérieur.</span><span class="sxs-lookup"><span data-stu-id="4c25e-120">For example, with a cone on the listener, one can specify all sounds behind the listener get a bit muffled, and have slightly higher reverb-to-direct ratio content.</span></span> <span data-ttu-id="4c25e-121">Celles-ci fournissent des indications supplémentaires que le son est derrière l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c25e-121">These provide more cues that the sound is behind the user.</span></span> <span data-ttu-id="4c25e-122">Cela améliore le réalisme.</span><span class="sxs-lookup"><span data-stu-id="4c25e-122">This enhances realism.</span></span>

<span data-ttu-id="4c25e-123">L’illustration suivante montre le concept de cônes audio.</span><span class="sxs-lookup"><span data-stu-id="4c25e-123">The following illustration shows the concept of sound cones.</span></span>

![cônes audio](images/common-audio-concepts-sound-cones.png)

<span data-ttu-id="4c25e-125">La création correcte de cônes audio peut ajouter des effets spectaculaires à votre application.</span><span class="sxs-lookup"><span data-stu-id="4c25e-125">Designing sound cones properly can add dramatic effects to your application.</span></span> <span data-ttu-id="4c25e-126">Par exemple, vous pouvez positionner une source sonore au centre d’une pièce, en définissant son orientation vers une porte ouverte dans un couloir.</span><span class="sxs-lookup"><span data-stu-id="4c25e-126">For example, you could position a sound source in the center of a room, setting its orientation toward an open door in a hallway.</span></span> <span data-ttu-id="4c25e-127">Définissez ensuite l’angle du cône intérieur afin qu’il s’étende à la largeur de la porte, rendez le cône extérieur un peu plus grand, puis définissez le volume conique extérieur sur inaudible.</span><span class="sxs-lookup"><span data-stu-id="4c25e-127">Then set the angle of the inside cone so that it extends to the width of the doorway, make the outside cone a bit wider, and finally set the outside cone volume to inaudible.</span></span> <span data-ttu-id="4c25e-128">Un écouteur se déplaçant le long du couloir commence à entendre le son uniquement lorsqu’il est près de la porte.</span><span class="sxs-lookup"><span data-stu-id="4c25e-128">A listener moving along the hallway will begin to hear the sound only when near the doorway.</span></span> <span data-ttu-id="4c25e-129">Le son sera le plus fort, car l’écouteur passe devant la porte ouverte.</span><span class="sxs-lookup"><span data-stu-id="4c25e-129">The sound will be loudest as the listener passes in front of the open door.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c25e-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c25e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c25e-131">Concepts audio courants</span><span class="sxs-lookup"><span data-stu-id="4c25e-131">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="4c25e-132">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="4c25e-132">X3DAudio</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="4c25e-133">**\_Cône X3DAUDIO**</span><span class="sxs-lookup"><span data-stu-id="4c25e-133">**X3DAUDIO\_CONE**</span></span>](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



