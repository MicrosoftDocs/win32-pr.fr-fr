---
description: Rôles d’appareil
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Rôles d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110786"
---
# <a name="device-roles"></a><span data-ttu-id="a95ab-103">Rôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="a95ab-103">Device Roles</span></span>

<span data-ttu-id="a95ab-104">Si un système contient au moins deux appareils de point de terminaison de rendu audio, un appareil peut être idéal pour la lecture d’un seul type de contenu audio, et un autre pour la lecture d’un autre type de contenu.</span><span class="sxs-lookup"><span data-stu-id="a95ab-104">If a system contains two or more audio-rendering endpoint devices, then one device might be best for playing one type of audio content, and another device might be best for playing another type of content.</span></span> <span data-ttu-id="a95ab-105">Par exemple, si un système a deux périphériques de rendu, l’utilisateur peut choisir de lire la musique sur un appareil et de lire les sons de notification du système.</span><span class="sxs-lookup"><span data-stu-id="a95ab-105">For example, if a system has two rendering devices, the user might choose to play music on one device and to play system notification sounds on the other.</span></span>

<span data-ttu-id="a95ab-106">De même, si un système contient au moins deux périphériques de point de terminaison de capture audio, un périphérique peut être le mieux adapté à la capture d’un type de contenu audio, et un autre périphérique peut être idéal pour capturer un autre type de contenu.</span><span class="sxs-lookup"><span data-stu-id="a95ab-106">Similarly, if a system contains two or more audio-capture endpoint devices, then one device might be best for capturing one type of audio content, and another device might be best for capturing another type of content.</span></span> <span data-ttu-id="a95ab-107">Par exemple, si un système a deux périphériques de capture, l’utilisateur peut choisir d’enregistrer la musique en direct sur un appareil et d’utiliser l’autre appareil pour les commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="a95ab-107">For example, if a system has two capture devices, the user might choose to record live music on one device and to use the other device for voice commands.</span></span>

<span data-ttu-id="a95ab-108">Les appareils peuvent avoir trois rôles : console, communications et multimédia. le tableau suivant décrit les rôles d’appareil identifiés par les trois constantes (eConsole, eCommunications et eMultimedia) dans l’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="a95ab-108">Devices can have three roles: Console, Communications, and Multimedia.The following table describes the device roles identified by the three constants—eConsole, eCommunications, and eMultimedia—in the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>



| <span data-ttu-id="a95ab-109">ERole constante)</span><span class="sxs-lookup"><span data-stu-id="a95ab-109">ERole constant</span></span>  | <span data-ttu-id="a95ab-110">Rôle de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a95ab-110">Device role</span></span>                              | <span data-ttu-id="a95ab-111">Exemples de rendu</span><span class="sxs-lookup"><span data-stu-id="a95ab-111">Rendering examples</span></span>             | <span data-ttu-id="a95ab-112">Exemples de capture</span><span class="sxs-lookup"><span data-stu-id="a95ab-112">Capture examples</span></span>                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| <span data-ttu-id="a95ab-113">eConsole</span><span class="sxs-lookup"><span data-stu-id="a95ab-113">eConsole</span></span>        | <span data-ttu-id="a95ab-114">Interaction avec l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a95ab-114">Interaction with the computer</span></span>            | <span data-ttu-id="a95ab-115">Jeux et notifications système</span><span class="sxs-lookup"><span data-stu-id="a95ab-115">Games and system notifications</span></span> | <span data-ttu-id="a95ab-116">Commandes vocales</span><span class="sxs-lookup"><span data-stu-id="a95ab-116">Voice commands</span></span>                     |
| <span data-ttu-id="a95ab-117">eCommunications</span><span class="sxs-lookup"><span data-stu-id="a95ab-117">eCommunications</span></span> | <span data-ttu-id="a95ab-118">Communications vocales avec une autre personne</span><span class="sxs-lookup"><span data-stu-id="a95ab-118">Voice communications with another person</span></span> | <span data-ttu-id="a95ab-119">Conversation et VoIP</span><span class="sxs-lookup"><span data-stu-id="a95ab-119">Chat and VoIP</span></span>                  | <span data-ttu-id="a95ab-120">Conversation et VoIP</span><span class="sxs-lookup"><span data-stu-id="a95ab-120">Chat and VoIP</span></span>                      |
| <span data-ttu-id="a95ab-121">eMultimedia</span><span class="sxs-lookup"><span data-stu-id="a95ab-121">eMultimedia</span></span>     | <span data-ttu-id="a95ab-122">Lecture ou enregistrement de contenu audio</span><span class="sxs-lookup"><span data-stu-id="a95ab-122">Playing or recording audio content</span></span>       | <span data-ttu-id="a95ab-123">Musique et films</span><span class="sxs-lookup"><span data-stu-id="a95ab-123">Music and movies</span></span>               | <span data-ttu-id="a95ab-124">Narration et enregistrement de musique en direct</span><span class="sxs-lookup"><span data-stu-id="a95ab-124">Narration and live music recording</span></span> |



 

<span data-ttu-id="a95ab-125">Il se peut qu’un appareil de rendu ou de capture particulier soit affecté d’un ou de plusieurs rôles dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="a95ab-125">A particular rendering or capture device might be assigned none, one, some, or all of the roles in the preceding table.</span></span> <span data-ttu-id="a95ab-126">À tout moment, chaque rôle de la table est affecté à un seul périphérique de rendu (et un seul) et à un seul périphérique de capture.</span><span class="sxs-lookup"><span data-stu-id="a95ab-126">At any time, each role in the table is assigned to one (and only one) rendering device and to one (and only one) capture device.</span></span> <span data-ttu-id="a95ab-127">Autrement dit, l’affectation de rôles aux périphériques de rendu est indépendante de l’attribution de rôles aux périphériques de capture.</span><span class="sxs-lookup"><span data-stu-id="a95ab-127">That is, the assignment of roles to rendering devices is independent of the assignment of roles to capture devices.</span></span>

<span data-ttu-id="a95ab-128">Une application peut choisir de lire tous ses flux de sortie via un seul appareil de point de terminaison de rendu et d’enregistrer tous ses flux d’entrée à partir d’un seul appareil de point de terminaison de capture.</span><span class="sxs-lookup"><span data-stu-id="a95ab-128">An application might choose to play all of its output streams through a single rendering endpoint device, and to record all of its input streams from a single capture endpoint device.</span></span> <span data-ttu-id="a95ab-129">Une application peut également choisir de lire certains de ses flux de sortie via un appareil de rendu et de lire d’autres flux de sortie via un autre appareil de rendu.</span><span class="sxs-lookup"><span data-stu-id="a95ab-129">Alternatively, an application might choose to play some of its output streams through one rendering device and to play other output streams through another rendering device.</span></span> <span data-ttu-id="a95ab-130">De même, il peut choisir d’enregistrer certains de ses flux d’entrée via un appareil de capture et d’enregistrer d’autres flux d’entrée via un autre appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="a95ab-130">Similarly, it might choose to record some of its input streams through one capture device and to record other input streams through another capture device.</span></span> <span data-ttu-id="a95ab-131">Dans tous les cas, l’application peut attribuer chaque flux à l’appareil dont le rôle est le plus approprié pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="a95ab-131">In all cases, the application can assign each stream to the device whose role is most appropriate for that stream.</span></span>

<span data-ttu-id="a95ab-132">Par exemple, une application VoIP peut affecter le flux de sortie qui contient la notification de sonnerie à l’appareil de point de terminaison de rendu avec le rôle eConsole.</span><span class="sxs-lookup"><span data-stu-id="a95ab-132">For example, a VoIP application might assign the output stream that contains the ring-in notification to the rendering endpoint device with the eConsole role.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a95ab-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a95ab-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a95ab-134">Périphériques de point de terminaison audio</span><span class="sxs-lookup"><span data-stu-id="a95ab-134">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="a95ab-135">Utilisation des rôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="a95ab-135">Working with Device Roles</span></span>](device-roles-in-windows-vista.md)
</dt> <dt>

[<span data-ttu-id="a95ab-136">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="a95ab-136">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



