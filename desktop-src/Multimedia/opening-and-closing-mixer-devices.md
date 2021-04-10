---
title: Ouverture et fermeture des appareils de mixage
description: Ouverture et fermeture des appareils de mixage
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- audio multimédia, ouverture des appareils de mixage
- audio, ouverture des appareils de mixage
- mixages audio, ouverture
- mixages, ouverture
- audio multimédia, fermeture des appareils de mixage
- audio, fermeture des appareils de mixage
- mixages audio, fermeture
- mixageeurs, fermeture
- ouverture des appareils de mixage
- fermeture des appareils de mixage
- identificateurs d’appareil et descripteurs d’appareil
- mixages audio, identificateurs d’appareil et descripteurs d’appareil
- mélangeurs, identificateurs d’appareil et descripteurs d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031088"
---
# <a name="opening-and-closing-mixer-devices"></a><span data-ttu-id="f040b-116">Ouverture et fermeture des appareils de mixage</span><span class="sxs-lookup"><span data-stu-id="f040b-116">Opening and Closing Mixer Devices</span></span>

<span data-ttu-id="f040b-117">Lorsque vous souhaitez utiliser un appareil de mixage, vous pouvez commencer à l’utiliser, ou vous pouvez ouvrir explicitement l’appareil avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="f040b-117">When you want to use a mixer device, you can either simply begin using it or you can explicitly open the device before using it.</span></span> <span data-ttu-id="f040b-118">L’ouverture explicite d’un appareil de mixage offre deux avantages principaux :</span><span class="sxs-lookup"><span data-stu-id="f040b-118">Explicitly opening a mixer device offers two main benefits:</span></span>

-   <span data-ttu-id="f040b-119">Cela garantit l’existence continue de cet appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="f040b-119">It guarantees the continued existence of that mixer device.</span></span>
-   <span data-ttu-id="f040b-120">Elle vous permet de recevoir des notifications de changement de ligne et de contrôle audio.</span><span class="sxs-lookup"><span data-stu-id="f040b-120">It lets you receive notification of audio line and control changes.</span></span>

<span data-ttu-id="f040b-121">Vous pouvez utiliser la fonction [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) pour ouvrir explicitement un appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="f040b-121">You can use the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function to explicitly open a mixer device.</span></span> <span data-ttu-id="f040b-122">Cette fonction prend comme paramètres un identificateur de périphérique, un pointeur vers un emplacement de mémoire et d’autres valeurs propres à chaque type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="f040b-122">This function takes as parameters a device identifier, a pointer to a memory location, and other values unique to each type of device.</span></span> <span data-ttu-id="f040b-123">L’emplacement de la mémoire est rempli avec un handle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="f040b-123">The memory location is filled with a device handle.</span></span> <span data-ttu-id="f040b-124">Utilisez ce handle d’appareil pour identifier l’appareil mixer ouvert lors de l’appel d’autres fonctions de mixage audio.</span><span class="sxs-lookup"><span data-stu-id="f040b-124">Use this device handle to identify the open mixer device when calling other audio mixer functions.</span></span> <span data-ttu-id="f040b-125">Tant qu’il existe un handle de périphérique de mixage, l’appareil continue à exister dans le système.</span><span class="sxs-lookup"><span data-stu-id="f040b-125">As long as a handle of a mixer device exists, the device continues to exist in the system.</span></span> <span data-ttu-id="f040b-126">Si une modification de configuration se produit sur le périphérique de mixage et qu’elle n’a pas été explicitement ouverte, votre application risque de ne pas pouvoir y accéder.</span><span class="sxs-lookup"><span data-stu-id="f040b-126">If a configuration change occurs to the mixer device and it hasn't been explicitly opened, your application might suddenly be unable to access it.</span></span>

> [!Note]  
> <span data-ttu-id="f040b-127">La différence entre les identificateurs d’appareil et les descripteurs d’appareil est importante.</span><span class="sxs-lookup"><span data-stu-id="f040b-127">The difference between device identifiers and device handles is important.</span></span> <span data-ttu-id="f040b-128">Des descripteurs d’appareil sont retournés lorsque vous ouvrez un pilote de périphérique à l’aide de **mixerOpen**.</span><span class="sxs-lookup"><span data-stu-id="f040b-128">Device handles are returned when you open a device driver by using **mixerOpen**.</span></span> <span data-ttu-id="f040b-129">Les identificateurs d’appareil sont déterminés implicitement à partir du nombre d’appareils présents dans un système. ce nombre est obtenu à l’aide de la fonction [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="f040b-129">Device identifiers are determined implicitly from the number of devices present in a system; this number is obtained by using the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function.</span></span>

 

<span data-ttu-id="f040b-130">Vous pouvez utiliser la fonction [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) pour fermer un appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="f040b-130">You can use the [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) function to close a mixer device.</span></span> <span data-ttu-id="f040b-131">Vous devez fermer l’appareil une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="f040b-131">You should close the device after you finish using it.</span></span>

 

 