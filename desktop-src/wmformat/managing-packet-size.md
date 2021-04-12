---
title: Gestion de la taille des paquets
description: Gestion de la taille des paquets
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK, gestion des tailles de paquets
- Windows Media Format SDK, tailles de paquets
- profils, tailles de paquets
- profils, gestion des tailles de paquets
- paquets, tailles
- paquets, interface IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381692"
---
# <a name="managing-packet-size"></a><span data-ttu-id="51860-110">Gestion de la taille des paquets</span><span class="sxs-lookup"><span data-stu-id="51860-110">Managing Packet Size</span></span>

<span data-ttu-id="51860-111">Le writer est conçu pour gérer la taille des paquets en interne.</span><span class="sxs-lookup"><span data-stu-id="51860-111">The writer is designed to manage the size of packets internally.</span></span> <span data-ttu-id="51860-112">Toutefois, vous pouvez avoir des exigences spécifiques pour votre application qui appellent un contrôle manuel sur la taille des paquets dans les fichiers ASF que vous écrivez.</span><span class="sxs-lookup"><span data-stu-id="51860-112">However, you may have specific requirements for your application that call for some manual control over the size of packets in the ASF files that you write.</span></span> <span data-ttu-id="51860-113">Le kit de développement logiciel (SDK) du format Windows Media fournit deux interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) et [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , qui vous permettent de contrôler la taille maximale et minimale des paquets.</span><span class="sxs-lookup"><span data-stu-id="51860-113">The Windows Media Format SDK provides two interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) and [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) that enable you to control the maximum and minimum size of packets.</span></span>

<span data-ttu-id="51860-114">Les deux interfaces de taille de paquet sont exposées dans l’objet de profil.</span><span class="sxs-lookup"><span data-stu-id="51860-114">Both packet size interfaces are exposed in the profile object.</span></span> <span data-ttu-id="51860-115">Ils sont également disponibles pour l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="51860-115">They are also available to the reader object.</span></span> <span data-ttu-id="51860-116">Comme avec d’autres interfaces liées aux profils, le lecteur peut accéder uniquement aux méthodes de lecture.</span><span class="sxs-lookup"><span data-stu-id="51860-116">As with other profile-related interfaces, the reader can access only the reading methods.</span></span>

<span data-ttu-id="51860-117">La taille des paquets a un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="51860-117">The size of packets has some effect on performance.</span></span> <span data-ttu-id="51860-118">En général, plus la taille du paquet est faible, plus les données sont fragmentées dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="51860-118">In general, the smaller the packet size, the more fragmented the data is within a file.</span></span> <span data-ttu-id="51860-119">Plus un fichier est fragmenté, moins il sera efficace de le reconstruire.</span><span class="sxs-lookup"><span data-stu-id="51860-119">The more fragmented a file is, the less efficient it will be to reconstruct it.</span></span> <span data-ttu-id="51860-120">Dans un scénario de diffusion en continu, ce n’est peut-être pas une considération importante, car le processus de lecture d’un fichier à partir d’une source Internet est généralement inefficace.</span><span class="sxs-lookup"><span data-stu-id="51860-120">In a streaming scenario, this may not be an important consideration, as the process of reading a file from an Internet source is generally inefficient.</span></span> <span data-ttu-id="51860-121">Toutefois, lorsque vous traitez un fichier localement, cela peut être une considération.</span><span class="sxs-lookup"><span data-stu-id="51860-121">When dealing with a file locally however, this might be a consideration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51860-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51860-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51860-123">**Interface IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="51860-123">**IWMPacketSize Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[<span data-ttu-id="51860-124">**Interface IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="51860-124">**IWMPacketSize2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[<span data-ttu-id="51860-125">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="51860-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




