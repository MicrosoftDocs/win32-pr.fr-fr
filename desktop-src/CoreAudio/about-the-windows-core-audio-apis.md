---
description: À propos des API audio Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: À propos des API audio Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861694"
---
# <a name="about-the-windows-core-audio-apis"></a><span data-ttu-id="6f100-103">À propos des API audio Windows Core</span><span class="sxs-lookup"><span data-stu-id="6f100-103">About the Windows Core Audio APIs</span></span>

<span data-ttu-id="6f100-104">Cette documentation fournit des informations sur les API audio principales pour la famille de systèmes d’exploitation Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6f100-104">This documentation provides information about Core Audio APIs for the Microsoft Windows family of operating systems.</span></span>

<span data-ttu-id="6f100-105">Les API audio de base ont été introduites dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f100-105">The Core Audio APIs were introduced in Windows Vista.</span></span> <span data-ttu-id="6f100-106">Il s’agit d’un nouvel ensemble de composants audio en mode utilisateur qui fournit aux applications clientes des fonctionnalités audio améliorées.</span><span class="sxs-lookup"><span data-stu-id="6f100-106">This is a new set of user-mode audio components provides client applications with improved audio capabilities.</span></span> <span data-ttu-id="6f100-107">Ces fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f100-107">These capabilities include the following:</span></span>

-   <span data-ttu-id="6f100-108">Diffusion en continu de données audio résistante aux problèmes et à faible latence.</span><span class="sxs-lookup"><span data-stu-id="6f100-108">Low-latency, glitch-resilient audio streaming.</span></span>
-   <span data-ttu-id="6f100-109">Fiabilité améliorée (de nombreuses fonctions audio ont été déplacées du mode noyau au mode utilisateur).</span><span class="sxs-lookup"><span data-stu-id="6f100-109">Improved reliability (many audio functions have moved from kernel mode to user mode).</span></span>
-   <span data-ttu-id="6f100-110">Amélioration de la sécurité (le traitement du contenu audio protégé s’effectue dans un processus sécurisé et à faibles privilèges).</span><span class="sxs-lookup"><span data-stu-id="6f100-110">Improved security (processing of protected audio content takes place in a secure, lower-privilege process).</span></span>
-   <span data-ttu-id="6f100-111">Attribution de rôles spécifiques à l’ensemble du système (console, multimédia et communications) à des périphériques audio individuels.</span><span class="sxs-lookup"><span data-stu-id="6f100-111">Assignment of particular system-wide roles (console, multimedia, and communications) to individual audio devices.</span></span>
-   <span data-ttu-id="6f100-112">Abstraction logicielle des appareils de point de terminaison audio (par exemple, haut-parleurs, casque et microphones) manipulés directement par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f100-112">Software abstraction of the audio endpoint devices (for example, speakers, headphones, and microphones) that the user manipulates directly.</span></span>

<span data-ttu-id="6f100-113">Les API audio de base ont été améliorées dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f100-113">The Core Audio APIs have been improved in Windows 7.</span></span> <span data-ttu-id="6f100-114">Pour plus d’informations sur les améliorations et les nouvelles fonctionnalités ajoutées, consultez [Nouveautés des API audio principales dans Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span><span class="sxs-lookup"><span data-stu-id="6f100-114">For more information about the improvements and new features added, see [What's New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span></span>

<span data-ttu-id="6f100-115">Cette documentation décrit les principales API audio.</span><span class="sxs-lookup"><span data-stu-id="6f100-115">This documentation describes the Core Audio APIs.</span></span> <span data-ttu-id="6f100-116">Ces API servent de base aux API de niveau supérieur suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f100-116">These APIs serve as the foundation for the following higher-level APIs:</span></span>

-   <span data-ttu-id="6f100-117">DirectSound</span><span class="sxs-lookup"><span data-stu-id="6f100-117">DirectSound</span></span>
-   <span data-ttu-id="6f100-118">DirectMusic</span><span class="sxs-lookup"><span data-stu-id="6f100-118">DirectMusic</span></span>
-   <span data-ttu-id="6f100-119">Fonctions **waveXxx** et **mixerXxx** Windows Multimedia</span><span class="sxs-lookup"><span data-stu-id="6f100-119">Windows multimedia **waveXxx** and **mixerXxx** functions</span></span>
-   <span data-ttu-id="6f100-120">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f100-120">Media Foundation</span></span>

<span data-ttu-id="6f100-121">Ces API de niveau supérieur utilisent les API audio de base pour partager l’accès aux périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="6f100-121">These higher-level APIs use the Core Audio APIs to share access to audio devices.</span></span> <span data-ttu-id="6f100-122">Media Foundation est une nouveauté de Windows Vista, tandis que DirectSound, DirectMusic et les fonctions **waveXxx** et **mixerXxx** sont prises en charge dans Windows 98, Windows Millennium Edition et Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6f100-122">Media Foundation is new with Windows Vista, whereas DirectSound, DirectMusic, and the **waveXxx** and **mixerXxx** functions are supported in Windows 98, Windows Millennium Edition, and in Windows 2000 and later.</span></span>

<span data-ttu-id="6f100-123">La plupart des applications audio communiquent avec les API de niveau supérieur au lieu de communiquer directement avec les API audio de base.</span><span class="sxs-lookup"><span data-stu-id="6f100-123">Most audio applications communicate with the higher-level APIs instead of communicating directly with the Core Audio APIs.</span></span> <span data-ttu-id="6f100-124">Voici quelques exemples d’applications qui utilisent des API de niveau supérieur :</span><span class="sxs-lookup"><span data-stu-id="6f100-124">Some examples of applications that use higher-level APIs are:</span></span>

-   <span data-ttu-id="6f100-125">Lecteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="6f100-125">Media players</span></span>
-   <span data-ttu-id="6f100-126">Lecteurs de DVD</span><span class="sxs-lookup"><span data-stu-id="6f100-126">DVD players</span></span>
-   <span data-ttu-id="6f100-127">Jeux</span><span class="sxs-lookup"><span data-stu-id="6f100-127">Games</span></span>
-   <span data-ttu-id="6f100-128">Applications d’entreprise, telles que Microsoft Office PowerPoint, qui lisent des fichiers audio</span><span class="sxs-lookup"><span data-stu-id="6f100-128">Business applications, such as Microsoft Office PowerPoint, that play sound files</span></span>

<span data-ttu-id="6f100-129">En règle générale, ces applications communiquent avec les API DirectSound ou Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6f100-129">Typically, these applications communicate with the DirectSound or Media Foundation APIs.</span></span>

<span data-ttu-id="6f100-130">La communication directe avec les API audio de base peut ne pas convenir à de nombreuses applications audio à usage général.</span><span class="sxs-lookup"><span data-stu-id="6f100-130">Direct communication with the Core Audio APIs might not be suitable for many general-purpose audio applications.</span></span> <span data-ttu-id="6f100-131">Par exemple, les API audio de base requièrent des flux audio pour utiliser des formats de données natifs d’un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="6f100-131">For example, the Core Audio APIs require audio streams to use an audio device's native data formats.</span></span> <span data-ttu-id="6f100-132">Toutefois, les développeurs de logiciels tiers qui développent les types de produits suivants peuvent nécessiter les fonctionnalités spéciales des API audio de base :</span><span class="sxs-lookup"><span data-stu-id="6f100-132">However, third-party software developers who are developing the following types of products might require the special capabilities of the Core Audio APIs:</span></span>

-   <span data-ttu-id="6f100-133">Applications audio professionnelles (« Pro Audio »)</span><span class="sxs-lookup"><span data-stu-id="6f100-133">Professional audio ("pro audio") applications</span></span>
-   <span data-ttu-id="6f100-134">Applications de communication en temps réel (RTC)</span><span class="sxs-lookup"><span data-stu-id="6f100-134">Real-time communication (RTC) applications</span></span>
-   <span data-ttu-id="6f100-135">API audio tierces</span><span class="sxs-lookup"><span data-stu-id="6f100-135">Third-party audio APIs</span></span>

<span data-ttu-id="6f100-136">Une application « Pro audio » ou RTC peut avoir besoin d’un accès direct aux fonctionnalités de bas niveau des API audio de base pour atteindre une latence minimale en obtenant un accès exclusif au matériel audio.</span><span class="sxs-lookup"><span data-stu-id="6f100-136">A "pro audio" or RTC application might need direct access to the low-level features of the Core Audio APIs to achieve minimum latency by obtaining exclusive access to audio hardware.</span></span> <span data-ttu-id="6f100-137">Une API audio tierce peut nécessiter un accès direct aux API audio de base pour implémenter un ensemble de fonctionnalités qui ne sont peut-être pas entièrement prises en charge par une seule API audio de haut niveau fournie avec Windows.</span><span class="sxs-lookup"><span data-stu-id="6f100-137">A third-party audio API might require direct access to the Core Audio APIs to implement a set of features that might not be entirely supported by any single high-level audio API that is supplied with Windows.</span></span>

<span data-ttu-id="6f100-138">Une application qui utilise une API audio héritée pour lire ou enregistrer du contenu audio peut nécessiter des fonctionnalités supplémentaires qui ne sont pas prises en charge par l’API audio héritée, mais qui sont prises en charge par les API audio de base.</span><span class="sxs-lookup"><span data-stu-id="6f100-138">An application that uses a legacy audio API to play or record audio might require additional capabilities that are not supported by the legacy audio API, but that are supported by the Core Audio APIs.</span></span> <span data-ttu-id="6f100-139">Dans de nombreux cas, l’application peut accéder à ces fonctionnalités directement par le biais des API audio de base, qui peuvent être utilisées conjointement avec l’API audio héritée.</span><span class="sxs-lookup"><span data-stu-id="6f100-139">In many cases, the application can access these capabilities directly through the Core Audio APIs, which can be used in conjunction with the legacy audio API.</span></span>

<span data-ttu-id="6f100-140">Les API audio principales sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f100-140">The Core Audio APIs are:</span></span>

-   <span data-ttu-id="6f100-141">[API de périphérique multimédia (MMDevice)](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f100-141">[Multimedia Device (MMDevice) API](mmdevice-api.md).</span></span> <span data-ttu-id="6f100-142">Les clients utilisent cette API pour énumérer les périphériques de point de terminaison audio dans le système.</span><span class="sxs-lookup"><span data-stu-id="6f100-142">Clients use this API to enumerate the audio endpoint devices in the system.</span></span>
-   <span data-ttu-id="6f100-143">[API de session audio Windows (WASAPI)](wasapi.md).</span><span class="sxs-lookup"><span data-stu-id="6f100-143">[Windows Audio Session API (WASAPI)](wasapi.md).</span></span> <span data-ttu-id="6f100-144">Les clients utilisent cette API pour créer et gérer des flux audio vers et depuis des appareils de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="6f100-144">Clients use this API to create and manage audio streams to and from audio endpoint devices.</span></span>
-   <span data-ttu-id="6f100-145">[API DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f100-145">[DeviceTopology API](devicetopology-api.md).</span></span> <span data-ttu-id="6f100-146">Les clients utilisent cette API pour accéder directement aux fonctionnalités topologiques (par exemple, les contrôles de volume et les multiplexeurs) qui se trouvent le long des chemins de données à l’intérieur des périphériques matériels des adaptateurs audio.</span><span class="sxs-lookup"><span data-stu-id="6f100-146">Clients use this API to directly access the topological features (for example, volume controls and multiplexers) that lie along the data paths inside hardware devices in audio adapters.</span></span>
-   <span data-ttu-id="6f100-147">[API EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f100-147">[EndpointVolume API](endpointvolume-api.md).</span></span> <span data-ttu-id="6f100-148">Les clients utilisent cette API pour accéder directement aux contrôles du volume sur les périphériques de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="6f100-148">Clients use this API to directly access the volume controls on audio endpoint devices.</span></span> <span data-ttu-id="6f100-149">Cette API est principalement utilisée par les applications qui gèrent des flux audio en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="6f100-149">This API is primarily used by applications that manage exclusive-mode audio streams.</span></span>

<span data-ttu-id="6f100-150">Ces API prennent en charge la notion conviviale d’un périphérique de point de terminaison, qui est décrite dans [périphériques de point de terminaison audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="6f100-150">These APIs support the user-friendly notion of an endpoint device, which is described in [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="6f100-151">Microsoft ne prévoit pas de créer les API audio de base décrites ici pour une utilisation avec les versions antérieures de Windows, notamment Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 et Windows 98.</span><span class="sxs-lookup"><span data-stu-id="6f100-151">Microsoft does not plan to make the Core Audio APIs that are described here available for use with earlier versions of Windows, including Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000, and Windows 98.</span></span>

<span data-ttu-id="6f100-152">Cette vue d’ensemble contient les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f100-152">This overview contains the following topics.</span></span>



| <span data-ttu-id="6f100-153">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="6f100-153">**Topic**</span></span>                                                                                      | <span data-ttu-id="6f100-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="6f100-154">**Description**</span></span>                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f100-155">Nouveautés des API audio principales dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f100-155">What's New for Core Audio APIs in Windows 7</span></span>](what-s-new-for-core-audio-apis-in-windows-7.md) | <span data-ttu-id="6f100-156">Résume les nouvelles fonctionnalités et les améliorations apportées aux API audio principales.</span><span class="sxs-lookup"><span data-stu-id="6f100-156">Summarizes the new features and the improvements to the Core Audio APIs</span></span>                   |
| [<span data-ttu-id="6f100-157">Fichiers d’en-tête et composants système</span><span class="sxs-lookup"><span data-stu-id="6f100-157">Header Files and System Components</span></span>](header-files-and-system-components.md)                   | <span data-ttu-id="6f100-158">Décrit les fichiers d’en-tête et les composants système pour les API audio principales.</span><span class="sxs-lookup"><span data-stu-id="6f100-158">Describes the header files and system components for the Core Audio APIs.</span></span>                 |
| [<span data-ttu-id="6f100-159">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="6f100-159">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)       | <span data-ttu-id="6f100-160">Répertorie les exemples de la SDK Windows qui utilisent les API audio de base.</span><span class="sxs-lookup"><span data-stu-id="6f100-160">Lists the samples in the Windows SDK that use the Core Audio APIs.</span></span>                        |




 

## <a name="related-topics"></a><span data-ttu-id="6f100-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f100-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f100-162">API audio principales</span><span class="sxs-lookup"><span data-stu-id="6f100-162">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



