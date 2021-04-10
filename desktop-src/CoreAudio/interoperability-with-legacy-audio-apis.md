---
description: Interopérabilité avec les API audio héritées
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interopérabilité avec les API audio héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950753"
---
# <a name="interoperability-with-legacy-audio-apis"></a><span data-ttu-id="f4c44-103">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="f4c44-103">Interoperability with Legacy Audio APIs</span></span>

<span data-ttu-id="f4c44-104">De nombreuses applications existantes utilisent des API audio héritées telles que DirectSound, DirectShow et les fonctions multimédias de Windows.</span><span class="sxs-lookup"><span data-stu-id="f4c44-104">Many existing applications use legacy audio APIs such as DirectSound, DirectShow, and the Windows multimedia functions.</span></span> <span data-ttu-id="f4c44-105">Avec uniquement des modifications mineures, ces applications peuvent être augmentées pour utiliser les [rôles d’appareil](device-roles.md), les contrôles de volume de [session](session-volume-controls.md)et d’autres fonctionnalités des API audio de base dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f4c44-105">With only minor modifications, these applications can be augmented to make use of [device roles](device-roles.md), [session volume controls](session-volume-controls.md), and other features of the core audio APIs in Windows Vista.</span></span>

<span data-ttu-id="f4c44-106">Comme indiqué dans les [composants audio en mode utilisateur](user-mode-audio-components.md), les API audio principales servent de base sur laquelle sont créées les API audio de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="f4c44-106">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), the core audio APIs serve as the foundation on which higher-level audio APIs are built.</span></span> <span data-ttu-id="f4c44-107">Dans Windows Vista, les périphériques audio auxquels les applications accèdent via des API audio héritées telles que DirectSound et les fonctions Windows Media **waveOutXxx** et **waveInXxx** sont, en fait, des [appareils de point de terminaison audio](audio-endpoint-devices.md) qui sont implémentés par les API audio de base.</span><span class="sxs-lookup"><span data-stu-id="f4c44-107">In Windows Vista, the audio devices that applications access through legacy audio APIs such as DirectSound and the Windows media **waveOutXxx** and **waveInXxx** functions are, in fact, [audio endpoint devices](audio-endpoint-devices.md) that are implemented by the core audio APIs.</span></span> <span data-ttu-id="f4c44-108">En raison des limitations inhérentes aux interfaces des API audio héritées, une application peut accéder à certaines des fonctionnalités des appareils de point de terminaison audio via ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="f4c44-108">Because of inherent limitations in the interfaces of legacy audio APIs, an application can access some but not all of the capabilities of audio endpoint devices through these interfaces.</span></span> <span data-ttu-id="f4c44-109">Les sections suivantes décrivent les techniques permettant d’améliorer les applications existantes en accédant aux fonctionnalités supplémentaires des appareils de point de terminaison audio directement via les API audio de base.</span><span class="sxs-lookup"><span data-stu-id="f4c44-109">The following sections describe techniques for enhancing existing applications by accessing additional capabilities of audio endpoint devices directly through the core audio APIs.</span></span> <span data-ttu-id="f4c44-110">Ces améliorations requièrent généralement uniquement des modifications mineures apportées au code d’application existant.</span><span class="sxs-lookup"><span data-stu-id="f4c44-110">These enhancements typically require only minor changes to the existing application code.</span></span>

<span data-ttu-id="f4c44-111">Les sections suivantes décrivent comment incorporer des fonctionnalités des API audio de base dans des applications existantes qui utilisent des API audio héritées :</span><span class="sxs-lookup"><span data-stu-id="f4c44-111">The following sections describe how to incorporate features of the core audio APIs into existing applications that use legacy audio APIs:</span></span>

-   [<span data-ttu-id="f4c44-112">Rôles d’appareil pour les applications DirectSound</span><span class="sxs-lookup"><span data-stu-id="f4c44-112">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)
-   [<span data-ttu-id="f4c44-113">Rôles d’appareil pour les applications DirectShow</span><span class="sxs-lookup"><span data-stu-id="f4c44-113">Device Roles for DirectShow Applications</span></span>](device-roles-for-directshow-applications.md)
-   [<span data-ttu-id="f4c44-114">Rôles d’appareil pour les applications multimédias Windows héritées</span><span class="sxs-lookup"><span data-stu-id="f4c44-114">Device Roles for Legacy Windows Multimedia Applications</span></span>](device-roles-for-legacy-windows-multimedia-applications.md)
-   [<span data-ttu-id="f4c44-115">Événements audio pour les applications audio héritées</span><span class="sxs-lookup"><span data-stu-id="f4c44-115">Audio Events for Legacy Audio Applications</span></span>](audio-events-for-legacy-audio-applications.md)
-   [<span data-ttu-id="f4c44-116">Sons de notification pour les applications audio héritées</span><span class="sxs-lookup"><span data-stu-id="f4c44-116">Notification Sounds for Legacy Audio Applications</span></span>](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a><span data-ttu-id="f4c44-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4c44-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4c44-118">Rôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="f4c44-118">Device Roles</span></span>](device-roles.md)
</dt> </dl>

 

 



