---
description: Découvrez les concepts et les fonctionnalités des API audio de base de Windows Vista et comment les utiliser dans la programmation d’applications.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guide de programmation audio de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405872"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="28511-103">Guide de programmation audio de base</span><span class="sxs-lookup"><span data-stu-id="28511-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="28511-104">Cette section du guide explique les concepts et les fonctionnalités des API audio de base de Windows Vista et décrit comment les utiliser dans la programmation d’applications.</span><span class="sxs-lookup"><span data-stu-id="28511-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="28511-105">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="28511-105">This section contains the following topics.</span></span>



| <span data-ttu-id="28511-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="28511-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="28511-107">Description</span><span class="sxs-lookup"><span data-stu-id="28511-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28511-108">Composants audio en mode utilisateur</span><span class="sxs-lookup"><span data-stu-id="28511-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="28511-109">Via les interfaces de bas niveau dans les API audio de base, un client peut accéder aux composants système qui gèrent et combinent des flux audio.</span><span class="sxs-lookup"><span data-stu-id="28511-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="28511-110">PUMA (Protected user mode audio)</span><span class="sxs-lookup"><span data-stu-id="28511-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="28511-111">Décrit les mises à jour apportées à PUMA (Protected user mode audio), le moteur audio en mode utilisateur dans l’environnement protégé (PE), qui fournit un environnement plus sûr pour le traitement et le rendu audio.</span><span class="sxs-lookup"><span data-stu-id="28511-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="28511-112">Périphériques de point de terminaison audio</span><span class="sxs-lookup"><span data-stu-id="28511-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="28511-113">Un périphérique de point de terminaison audio est une abstraction logicielle qui permet des interactions conviviales avec les périphériques audio tels que les microphones et les orateurs.</span><span class="sxs-lookup"><span data-stu-id="28511-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="28511-114">Sessions audio</span><span class="sxs-lookup"><span data-stu-id="28511-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="28511-115">Une session audio est une abstraction logicielle qui permet à un client de gérer une collection de flux audio associés en tant qu’unité unique.</span><span class="sxs-lookup"><span data-stu-id="28511-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="28511-116">Contrôles de volume</span><span class="sxs-lookup"><span data-stu-id="28511-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="28511-117">Le système intègre ses paramètres de volume basés sur des stratégies avec les paramètres de volume de l’utilisateur de manière logique et cohérente.</span><span class="sxs-lookup"><span data-stu-id="28511-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="28511-118">Gestion de flux</span><span class="sxs-lookup"><span data-stu-id="28511-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="28511-119">L’API de session audio Windows (WASAPI) fournit à un client un ensemble complet de méthodes pour créer et gérer des flux audio.</span><span class="sxs-lookup"><span data-stu-id="28511-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="28511-120">Topologies d’appareils</span><span class="sxs-lookup"><span data-stu-id="28511-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="28511-121">L’API DeviceTopology permet à un client de découvrir les contrôles audio qui se trouvent le long des différents chemins de données dans le matériel audio.</span><span class="sxs-lookup"><span data-stu-id="28511-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="28511-122">Utilisation de l’interface IKsControl pour accéder aux propriétés audio</span><span class="sxs-lookup"><span data-stu-id="28511-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="28511-123">Une application audio spécialisée peut nécessiter l’utilisation de l’interface IKsControl pour accéder aux propriétés d’un adaptateur audio.</span><span class="sxs-lookup"><span data-stu-id="28511-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="28511-124">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="28511-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="28511-125">Les principales fonctionnalités des API audio de base dans Windows Vista peuvent être incorporées dans des applications existantes qui utilisent DirectSound, DirectShow et les fonctions **waveOutXxx** et **waveInXxx** de Windows Multimedia.</span><span class="sxs-lookup"><span data-stu-id="28511-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="28511-126">Son spatial</span><span class="sxs-lookup"><span data-stu-id="28511-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="28511-127">Fournit des conseils pour l’utilisation de Windows Sonic, la solution au niveau de la plate-forme de Microsoft pour la prise en charge des sons spatiaux sur Xbox et Windows, ce qui permet l’entourage et l’élévation (au-dessus ou en dessous de l’écouteur) des signaux audio.</span><span class="sxs-lookup"><span data-stu-id="28511-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="28511-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28511-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28511-129">API audio principales</span><span class="sxs-lookup"><span data-stu-id="28511-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



