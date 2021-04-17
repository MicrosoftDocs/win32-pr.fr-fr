---
description: Topologies d’appareils
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Topologies d’appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524255"
---
# <a name="device-topologies"></a><span data-ttu-id="b0b68-103">Topologies d’appareils</span><span class="sxs-lookup"><span data-stu-id="b0b68-103">Device Topologies</span></span>

<span data-ttu-id="b0b68-104">L' [API DeviceTopology](devicetopology-api.md) permet aux clients de contrôler une variété de fonctions internes des adaptateurs audio qu’ils ne peuvent pas accéder via l' [API MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)ou l' [API EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="b0b68-104">The [DeviceTopology API](devicetopology-api.md) gives clients control over a variety of internal functions of audio adapters that they cannot access through the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), or the [EndpointVolume API](endpointvolume-api.md).</span></span>

<span data-ttu-id="b0b68-105">Comme expliqué précédemment, l’API [MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)et l' [API EndpointVolume](endpointvolume-api.md) présentent des microtéléphones, des haut-parleurs, des casques et d’autres périphériques d’entrée et de sortie audio pour les clients en tant qu’appareils de point de [terminaison audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b0b68-105">As explained previously, the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), and the [EndpointVolume API](endpointvolume-api.md) present microphones, speakers, headphones, and other audio input and output devices to clients as [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="b0b68-106">Le modèle de périphérique de point de terminaison fournit aux clients un accès pratique aux contrôles de volume et de sourdine des périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-106">The endpoint device model provides clients with convenient access to volume and mute controls in audio devices.</span></span> <span data-ttu-id="b0b68-107">Les clients qui n’ont besoin que de ces contrôles simples peuvent éviter de traverser les topologies internes des périphériques matériels des adaptateurs audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-107">Clients that require only these simple controls can avoid traversing the internal topologies of hardware devices in audio adapters.</span></span>

<span data-ttu-id="b0b68-108">Dans Windows Vista, le moteur audio configure automatiquement les topologies des périphériques audio pour une utilisation par les applications audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-108">In Windows Vista, the audio engine automatically configures the topologies of audio devices for use by audio applications.</span></span> <span data-ttu-id="b0b68-109">Ainsi, les applications, si jamais, doivent utiliser l’API DeviceTopology à cet effet.</span><span class="sxs-lookup"><span data-stu-id="b0b68-109">Thus, applications rarely, if ever, need to use the DeviceTopology API for this purpose.</span></span> <span data-ttu-id="b0b68-110">Par exemple, supposons qu’une carte audio contient un multiplexeur d’entrée qui peut capturer un flux à partir d’une entrée de ligne ou d’un microphone, mais qui ne peut pas capturer simultanément des flux à partir des deux appareils de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b0b68-110">For example, assume that an audio adapter contains an input multiplexer that can capture a stream from either a line input or a microphone, but that cannot capture streams from both endpoint devices at the same time.</span></span> <span data-ttu-id="b0b68-111">Supposons que l’utilisateur a activé les applications en mode exclusif pour préempter l’utilisation d’un périphérique de point de terminaison audio par des applications en mode partagé, comme décrit dans [flux en mode exclusif](exclusive-mode-streams.md).</span><span class="sxs-lookup"><span data-stu-id="b0b68-111">Assume that the user has enabled exclusive-mode applications to preempt the use of an audio endpoint device by shared-mode applications, as described in [Exclusive-Mode Streams](exclusive-mode-streams.md).</span></span> <span data-ttu-id="b0b68-112">Si une application en mode partagé enregistre un flux à partir de l’entrée de ligne au moment où une application en mode exclusif commence à enregistrer un flux à partir du microphone, le moteur audio bascule automatiquement le multiplexeur de l’entrée de ligne vers le microphone.</span><span class="sxs-lookup"><span data-stu-id="b0b68-112">If a shared-mode application is recording a stream from the line input at the time that an exclusive-mode application begins recording a stream from the microphone, the audio engine automatically switches the multiplexer from the line input to the microphone.</span></span> <span data-ttu-id="b0b68-113">En revanche, dans les versions antérieures de Windows, y compris Windows XP, l’application en mode exclusif dans cet exemple utilisait les fonctions **mixerXxx** dans l’API multimédia Windows pour parcourir les topologies des périphériques de l’adaptateur, découvrir le multiplexeur et configurer le multiplexeur pour sélectionner l’entrée microphone.</span><span class="sxs-lookup"><span data-stu-id="b0b68-113">In contrast, in earlier versions of Windows, including Windows XP, the exclusive-mode application in this example would use the **mixerXxx** functions in the Windows multimedia API to traverse the topologies of the adapter devices, discover the multiplexer, and configure the multiplexer to select the microphone input.</span></span> <span data-ttu-id="b0b68-114">Dans Windows Vista, ces étapes ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b0b68-114">In Windows Vista, these steps are no longer required.</span></span>

<span data-ttu-id="b0b68-115">Toutefois, certains clients peuvent nécessiter un contrôle explicite sur les types de contrôles matériels audio qui ne sont pas accessibles via l’API MMDevice, WASAPI ou l’API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="b0b68-115">However, some clients might require explicit control over types of audio hardware controls that cannot be accessed through the MMDevice API, WASAPI, or the EndpointVolume API.</span></span> <span data-ttu-id="b0b68-116">Pour ces clients, l’API DeviceTopology offre la possibilité de traverser les topologies des périphériques d’adaptateur pour découvrir et gérer les contrôles audio des appareils.</span><span class="sxs-lookup"><span data-stu-id="b0b68-116">For these clients, the DeviceTopology API provides the ability to traverse the topologies of adapter devices to discover and manage the audio controls in the devices.</span></span> <span data-ttu-id="b0b68-117">Les applications qui utilisent l’API DeviceTopology doivent être conçues avec précaution pour éviter toute interférence avec la stratégie audio Windows et perturber les configurations internes des périphériques audio partagés avec d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="b0b68-117">Applications that use the DeviceTopology API must be designed with care to avoid interfering with Windows audio policy and disturbing the internal configurations of audio devices that are shared with other applications.</span></span> <span data-ttu-id="b0b68-118">Pour plus d’informations sur la stratégie audio Windows, consultez [composants audio en mode utilisateur](user-mode-audio-components.md).</span><span class="sxs-lookup"><span data-stu-id="b0b68-118">For more information about Windows audio policy, see [User-Mode Audio Components](user-mode-audio-components.md).</span></span>

<span data-ttu-id="b0b68-119">L’API DeviceTopology fournit des interfaces pour la découverte et la gestion des types de contrôles audio suivants dans une topologie d’appareil :</span><span class="sxs-lookup"><span data-stu-id="b0b68-119">The DeviceTopology API provides interfaces for discovering and managing the following types of audio controls in a device topology:</span></span>

-   <span data-ttu-id="b0b68-120">Contrôle du gain automatique</span><span class="sxs-lookup"><span data-stu-id="b0b68-120">Automatic gain control</span></span>
-   <span data-ttu-id="b0b68-121">Contrôle des basses</span><span class="sxs-lookup"><span data-stu-id="b0b68-121">Bass control</span></span>
-   <span data-ttu-id="b0b68-122">Sélecteur d’entrée (multiplexeur)</span><span class="sxs-lookup"><span data-stu-id="b0b68-122">Input selector (multiplexer)</span></span>
-   <span data-ttu-id="b0b68-123">Contrôle du volume</span><span class="sxs-lookup"><span data-stu-id="b0b68-123">Loudness control</span></span>
-   <span data-ttu-id="b0b68-124">Contrôle du milieu de gamme</span><span class="sxs-lookup"><span data-stu-id="b0b68-124">Midrange control</span></span>
-   <span data-ttu-id="b0b68-125">Contrôle muet</span><span class="sxs-lookup"><span data-stu-id="b0b68-125">Mute control</span></span>
-   <span data-ttu-id="b0b68-126">Sélecteur de sortie (démultiplexeur)</span><span class="sxs-lookup"><span data-stu-id="b0b68-126">Output selector (demultiplexer)</span></span>
-   <span data-ttu-id="b0b68-127">Compteur de pic</span><span class="sxs-lookup"><span data-stu-id="b0b68-127">Peak meter</span></span>
-   <span data-ttu-id="b0b68-128">Contrôle des aigus</span><span class="sxs-lookup"><span data-stu-id="b0b68-128">Treble control</span></span>
-   <span data-ttu-id="b0b68-129">Contrôle du volume</span><span class="sxs-lookup"><span data-stu-id="b0b68-129">Volume control</span></span>

<span data-ttu-id="b0b68-130">En outre, l’API DeviceTopology permet aux clients d’interroger des périphériques d’adaptateur pour obtenir des informations sur les formats de flux qu’ils prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="b0b68-130">In addition, the DeviceTopology API enables clients to query adapter devices for information about the stream formats that they support.</span></span> <span data-ttu-id="b0b68-131">Le fichier d’en-tête Devicetopology. h définit les interfaces dans l’API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="b0b68-131">The header file Devicetopology.h defines the interfaces in the DeviceTopology API.</span></span>

<span data-ttu-id="b0b68-132">Le diagramme suivant montre un exemple de plusieurs topologies d’appareils connectées pour la partie d’une carte PCI qui capture l’audio à partir d’un microphone, d’une entrée de ligne et d’un lecteur de CD.</span><span class="sxs-lookup"><span data-stu-id="b0b68-132">The following diagram shows an example of several connected device topologies for the portion of a PCI adapter that captures audio from a microphone, line input, and CD player.</span></span>

![exemple de quatre topologies d’appareils connectées](images/fig2.jpg)

<span data-ttu-id="b0b68-134">Le diagramme ci-dessus montre les chemins de données qui mènent aux entrées analogiques vers le bus système.</span><span class="sxs-lookup"><span data-stu-id="b0b68-134">The preceding diagram shows the data paths that lead from the analog inputs to the system bus.</span></span> <span data-ttu-id="b0b68-135">Chacun des appareils suivants est représenté sous la forme d’un objet de topologie d’appareil avec une interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :</span><span class="sxs-lookup"><span data-stu-id="b0b68-135">Each of the following devices is represented as a device-topology object with an [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface:</span></span>

-   <span data-ttu-id="b0b68-136">Périphérique de capture Wave</span><span class="sxs-lookup"><span data-stu-id="b0b68-136">Wave capture device</span></span>
-   <span data-ttu-id="b0b68-137">Périphérique multiplexeur d’entrée</span><span class="sxs-lookup"><span data-stu-id="b0b68-137">Input multiplexer device</span></span>
-   <span data-ttu-id="b0b68-138">Appareil de point de terminaison A</span><span class="sxs-lookup"><span data-stu-id="b0b68-138">Endpoint device A</span></span>
-   <span data-ttu-id="b0b68-139">Périphérique de point de terminaison B</span><span class="sxs-lookup"><span data-stu-id="b0b68-139">Endpoint device B</span></span>

<span data-ttu-id="b0b68-140">Notez que le diagramme de topologie associe les périphériques d’adaptateur (les périphériques de capture d’onde et de multiplexage d’entrée) aux périphériques de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b0b68-140">Note that the topology diagram combines adapter devices (the wave capture and input multiplexer devices) with endpoint devices.</span></span> <span data-ttu-id="b0b68-141">Via les connexions entre les appareils, les données audio passent d’un appareil à l’autre.</span><span class="sxs-lookup"><span data-stu-id="b0b68-141">Through the connections between devices, audio data passes from one device to the next.</span></span> <span data-ttu-id="b0b68-142">À chaque extrémité d’une connexion se trouve un connecteur (intitulé con dans le diagramme) par le biais duquel les données entrent ou quittent un appareil.</span><span class="sxs-lookup"><span data-stu-id="b0b68-142">On each side of a connection is a connector (labeled Con in the diagram) through which data enters or leaves a device.</span></span>

<span data-ttu-id="b0b68-143">Sur le bord gauche du diagramme, les signaux des prises d’entrée et de microphone entrent dans les unités de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b0b68-143">On the left edge of the diagram, signals from the line-input and microphone jacks enter the endpoint devices.</span></span>

<span data-ttu-id="b0b68-144">L’intérieur du périphérique de capture Wave et du multiplexeur d’entrée sont des fonctions de traitement de flux, qui, dans la terminologie de l’API DeviceTopology, sont appelées sous-unités.</span><span class="sxs-lookup"><span data-stu-id="b0b68-144">Inside the wave capture device and input multiplexer device are stream-processing functions, which, in the terminology of the DeviceTopology API, are called subunits.</span></span> <span data-ttu-id="b0b68-145">Les types de sous-unités suivants apparaissent dans le diagramme précédent :</span><span class="sxs-lookup"><span data-stu-id="b0b68-145">The following types of subunits appear in the preceding diagram:</span></span>

-   <span data-ttu-id="b0b68-146">Contrôle du volume (libellé volume)</span><span class="sxs-lookup"><span data-stu-id="b0b68-146">Volume control (labeled Vol)</span></span>
-   <span data-ttu-id="b0b68-147">Contrôle muet (intitulé muet)</span><span class="sxs-lookup"><span data-stu-id="b0b68-147">Mute control (labeled Mute)</span></span>
-   <span data-ttu-id="b0b68-148">Multiplexeur (ou sélecteur d’entrée ; appelé MUX)</span><span class="sxs-lookup"><span data-stu-id="b0b68-148">Multiplexer (or input selector; labeled MUX)</span></span>
-   <span data-ttu-id="b0b68-149">Convertisseur analogique-numérique (étiqueté ADC)</span><span class="sxs-lookup"><span data-stu-id="b0b68-149">Analog-to-digital converter (labeled ADC)</span></span>

<span data-ttu-id="b0b68-150">Les paramètres des sous-unités volume, muet et multiplexer peuvent être contrôlés par les clients, et l’API DeviceTopology fournit des interfaces de contrôle aux clients pour les contrôler.</span><span class="sxs-lookup"><span data-stu-id="b0b68-150">The settings in the volume, mute, and multiplexer subunits can be controlled by clients, and the DeviceTopology API provides control interfaces to clients for controlling them.</span></span> <span data-ttu-id="b0b68-151">Dans cet exemple, la sous-unité ADC n’a aucun paramètre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b0b68-151">In this example, the ADC subunit has no control settings.</span></span> <span data-ttu-id="b0b68-152">Ainsi, l’API DeviceTopology ne fournit aucune interface de contrôle pour le connecteur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0b68-152">Thus, the DeviceTopology API provides no control interface for the ADC.</span></span>

<span data-ttu-id="b0b68-153">Dans la terminologie de l’API DeviceTopology, les connecteurs et les sous-unités appartiennent à la même catégorie générale, parties.</span><span class="sxs-lookup"><span data-stu-id="b0b68-153">In the terminology of the DeviceTopology API, connectors and subunits belong to the same general category—parts.</span></span> <span data-ttu-id="b0b68-154">Toutes les parties, qu’il s’agisse de connecteurs ou de sous-unités, fournissent un ensemble commun de fonctions.</span><span class="sxs-lookup"><span data-stu-id="b0b68-154">All parts, regardless of whether they are connectors or subunits, provide a common set of functions.</span></span> <span data-ttu-id="b0b68-155">L’API DeviceTopology implémente une interface [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) pour représenter les fonctions génériques qui sont communes aux connecteurs et sous-unités.</span><span class="sxs-lookup"><span data-stu-id="b0b68-155">The DeviceTopology API implements an [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface to represent the generic functions that are common to connectors and subunits.</span></span> <span data-ttu-id="b0b68-156">L’API implémente les interfaces [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) et [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) pour représenter les aspects spécifiques des connecteurs et des sous-unités.</span><span class="sxs-lookup"><span data-stu-id="b0b68-156">The API implements the [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) and [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) interfaces to represent the specific aspects of connectors and subunits.</span></span>

<span data-ttu-id="b0b68-157">L’API DeviceTopology construit les topologies du périphérique de capture d’onde et du périphérique multiplexeur d’entrée à partir des filtres de diffusion en continu (KS) du noyau que le pilote audio expose au système d’exploitation pour représenter ces appareils.</span><span class="sxs-lookup"><span data-stu-id="b0b68-157">The DeviceTopology API constructs the topologies of the wave capture device and input multiplexer device from the kernel-streaming (KS) filters that the audio driver exposes to the operating system to represent these devices.</span></span> <span data-ttu-id="b0b68-158">(Le pilote de carte audio implémente les interfaces **IMiniportWaveXxx** et **IMiniportTopology** pour représenter les parties dépendantes du matériel de ces filtres. pour plus d’informations sur ces interfaces et sur les filtres KS, consultez la documentation de Windows DDK.)</span><span class="sxs-lookup"><span data-stu-id="b0b68-158">(The audio adapter driver implements **IMiniportWaveXxx** and **IMiniportTopology** interfaces to represent the hardware-dependent portions of these filters; for more information about these interfaces and about KS filters, see the Windows DDK documentation.)</span></span>

<span data-ttu-id="b0b68-159">L’API DeviceTopology construit des topologies triviales pour représenter les appareils de point de terminaison A et B dans le diagramme précédent.</span><span class="sxs-lookup"><span data-stu-id="b0b68-159">The DeviceTopology API constructs trivial topologies to represent endpoint devices A and B in the preceding diagram.</span></span> <span data-ttu-id="b0b68-160">La topologie de l’appareil d’un appareil de point de terminaison est constituée d’un connecteur unique.</span><span class="sxs-lookup"><span data-stu-id="b0b68-160">The device topology of an endpoint device consists of a single connector.</span></span> <span data-ttu-id="b0b68-161">Cette topologie est simplement un espace réservé pour l’appareil de point de terminaison et ne contient pas de sous-unités pour le traitement des données audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-161">This topology is merely a placeholder for the endpoint device and contains no subunits for processing audio data.</span></span> <span data-ttu-id="b0b68-162">En fait, les périphériques d’adaptateur contiennent toutes les sous-unités utilisées par les applications clientes pour contrôler le traitement audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-162">In fact, adapter devices contain all of the subunits that client applications use to control audio processing.</span></span> <span data-ttu-id="b0b68-163">La topologie d’appareil d’un appareil de point de terminaison sert principalement de point de départ pour l’exploration des topologies d’appareils des périphériques d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b0b68-163">The device topology of an endpoint device serves primarily as a starting point for exploring the device topologies of adapter devices.</span></span>

<span data-ttu-id="b0b68-164">Les connexions internes entre deux parties dans une topologie de périphérique sont appelées liens.</span><span class="sxs-lookup"><span data-stu-id="b0b68-164">Internal connections between two parts in a device topology are called links.</span></span> <span data-ttu-id="b0b68-165">L’API DeviceTopology fournit des méthodes pour parcourir les liens d’un composant à l’autre dans une topologie d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b0b68-165">The DeviceTopology API provides methods for traversing links from one part to the next in a device topology.</span></span> <span data-ttu-id="b0b68-166">L’API fournit également des méthodes pour parcourir les connexions entre les topologies d’appareils.</span><span class="sxs-lookup"><span data-stu-id="b0b68-166">The API also provides methods for traversing the connections between device topologies.</span></span>

<span data-ttu-id="b0b68-167">Pour commencer l’exploration d’un ensemble de topologies d’appareils connectées, une application cliente active l’interface **IDeviceTopology** d’un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-167">To begin exploration of a set of connected device topologies, a client application activates the **IDeviceTopology** interface of an audio endpoint device.</span></span> <span data-ttu-id="b0b68-168">Le connecteur d’un appareil de point de terminaison se connecte à un connecteur dans une carte audio ou à un réseau.</span><span class="sxs-lookup"><span data-stu-id="b0b68-168">The connector in an endpoint device connects either to a connector in an audio adapter or to a network.</span></span> <span data-ttu-id="b0b68-169">Si le point de terminaison se connecte à un appareil sur une carte audio, les méthodes de l’API DeviceTopology permettent à l’application d’effectuer un pas à pas détaillé de la connexion entre le point de terminaison et l’adaptateur en obtenant une référence à l’interface **IDeviceTopology** du périphérique adaptateur de l’autre côté de la connexion.</span><span class="sxs-lookup"><span data-stu-id="b0b68-169">If the endpoint connects to a device on an audio adapter, then the methods in the DeviceTopology API enable the application to step across the connection from the endpoint to the adapter by obtaining a reference to the **IDeviceTopology** interface of the adapter device on the other side of the connection.</span></span> <span data-ttu-id="b0b68-170">Un réseau, en revanche, n’a pas de topologie d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b0b68-170">A network, on the other hand, has no device topology.</span></span> <span data-ttu-id="b0b68-171">Une connexion réseau canalise un flux audio vers un client qui accède au système à distance.</span><span class="sxs-lookup"><span data-stu-id="b0b68-171">A network connection pipes an audio stream to a client that is accessing the system remotely.</span></span>

<span data-ttu-id="b0b68-172">L’API DeviceTopology fournit un accès uniquement aux topologies des périphériques matériels dans une carte audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-172">The DeviceTopology API provides access only to the topologies of the hardware devices in an audio adapter.</span></span> <span data-ttu-id="b0b68-173">Les périphériques externes situés sur le bord gauche du diagramme et les composants logiciels sur le bord droit n’entrent pas dans le cadre de l’API.</span><span class="sxs-lookup"><span data-stu-id="b0b68-173">The external devices on the left edge of the diagram and the software components on the right edge are beyond the scope of the API.</span></span> <span data-ttu-id="b0b68-174">Les lignes en pointillés de chaque côté du diagramme représentent les limites de l’API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="b0b68-174">The dashed lines on either side of the diagram represent the limits of the DeviceTopology API.</span></span> <span data-ttu-id="b0b68-175">Le client peut utiliser l’API pour explorer un chemin de données qui s’étend du jack d’entrée au bus système, mais l’API ne peut pas pénétrer au-delà de ces limites.</span><span class="sxs-lookup"><span data-stu-id="b0b68-175">The client can use the API to explore a data path that stretches from the input jack to the system bus, but the API cannot penetrate beyond these boundaries.</span></span>

<span data-ttu-id="b0b68-176">Chaque connecteur du diagramme précédent est associé à un type de connexion qui indique le type de connexion que le connecteur effectue.</span><span class="sxs-lookup"><span data-stu-id="b0b68-176">Each connector in the preceding diagram has an associated connection type that indicates the type of connection that the connector makes.</span></span> <span data-ttu-id="b0b68-177">Ainsi, les connecteurs sur les deux côtés d’une connexion ont toujours des types de connexion identiques.</span><span class="sxs-lookup"><span data-stu-id="b0b68-177">Thus, the connectors on the two sides of a connection always have identical connection types.</span></span> <span data-ttu-id="b0b68-178">Le type de connexion est indiqué par une valeur d’énumération [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) (physique \_ externe, physique \_ interne, logiciel \_ fixe, \_ e/s logiciel ou réseau).</span><span class="sxs-lookup"><span data-stu-id="b0b68-178">The connection type is indicated by a [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) enumeration value—Physical\_External, Physical\_Internal, Software\_Fixed, Software\_IO, or Network.</span></span> <span data-ttu-id="b0b68-179">Les connexions entre le périphérique multiplexeur d’entrée et les appareils de point de terminaison A et B sont de type externe physique, ce qui \_ signifie que la connexion représente une connexion physique à un périphérique externe (en d’autres termes, une prise jack audio accessible par l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="b0b68-179">The connections between the input multiplexer device and endpoint devices A and B are of type Physical\_External, which means that the connection represents a physical connection to an external device (in other words, a user-accessible audio jack).</span></span> <span data-ttu-id="b0b68-180">La connexion au signal analogique à partir du lecteur CD interne est de type physique \_ interne, ce qui indique une connexion physique à un appareil auxiliaire installé à l’intérieur du châssis du système.</span><span class="sxs-lookup"><span data-stu-id="b0b68-180">The connection to the analog signal from the internal CD player is of type Physical\_Internal, which indicates a physical connection to an auxiliary device that is installed inside the system chassis.</span></span> <span data-ttu-id="b0b68-181">La connexion entre le périphérique de capture d’onde et l’appareil de multiplexage d’entrée est de type logiciel \_ fixe, ce qui indique une connexion permanente qui est fixe et ne peut pas être configurée sous contrôle de logiciel.</span><span class="sxs-lookup"><span data-stu-id="b0b68-181">The connection between the wave capture device and input multiplexer device is of type Software\_Fixed, which indicates a permanent connection that is fixed and cannot be configured under software control.</span></span> <span data-ttu-id="b0b68-182">Enfin, la connexion au bus système sur le côté droit du diagramme est de type logiciel d' \_ e/s, ce qui indique que les e/s de données pour la connexion sont implémentées par un moteur DMA sous contrôle de logiciel.</span><span class="sxs-lookup"><span data-stu-id="b0b68-182">Finally, the connection to the system bus on the right side of the diagram is of type Software\_IO, which indicates that the data I/O for the connection is implemented by a DMA engine under software control.</span></span> <span data-ttu-id="b0b68-183">(Le diagramme n’inclut pas d’exemple de type de connexion réseau.)</span><span class="sxs-lookup"><span data-stu-id="b0b68-183">(The diagram does not include an example of a Network connection type.)</span></span>

<span data-ttu-id="b0b68-184">Le client commence à traverser un chemin de données sur l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b0b68-184">The client begins traversing a data path at the endpoint device.</span></span> <span data-ttu-id="b0b68-185">Tout d’abord, le client obtient une interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) qui représente l’appareil de point de terminaison, comme expliqué dans [énumération des périphériques audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b0b68-185">First, the client obtains an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface that represents the endpoint device, as explained in [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span> <span data-ttu-id="b0b68-186">Pour obtenir l’interface **IDeviceTopology** pour l’appareil de point de terminaison, le client appelle la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) avec l' *IID* de paramètre défini sur REFIID IID \_ IDeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="b0b68-186">To obtain the **IDeviceTopology** interface for the endpoint device, the client calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to REFIID IID\_IDeviceTopology.</span></span>

<span data-ttu-id="b0b68-187">Dans l’exemple du diagramme précédent, le périphérique multiplexeur d’entrée contient tous les contrôles matériels (volume, muet et multiplexeur) des flux de capture des prises d’entrée et de microphone.</span><span class="sxs-lookup"><span data-stu-id="b0b68-187">In the example in the preceding diagram, the input multiplexer device contains all the hardware controls (volume, mute, and multiplexer) for the capture streams from the line-input and microphone jacks.</span></span> <span data-ttu-id="b0b68-188">L’exemple de code suivant montre comment obtenir l’interface **IDeviceTopology** pour le périphérique multiplexeur d’entrée à partir de l’interface **IMMDevice** pour l’appareil de point de terminaison pour l’entrée de ligne ou le microphone :</span><span class="sxs-lookup"><span data-stu-id="b0b68-188">The following code example shows how to obtain the **IDeviceTopology** interface for the input multiplexer device from the **IMMDevice** interface for the endpoint device for the line input or microphone:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



<span data-ttu-id="b0b68-189">La fonction GetHardwareDeviceTopology de l’exemple de code précédent effectue les étapes suivantes pour obtenir l’interface **IDeviceTopology** pour le périphérique multiplexeur d’entrée :</span><span class="sxs-lookup"><span data-stu-id="b0b68-189">The GetHardwareDeviceTopology function in the previous code example performs the following steps to obtain the **IDeviceTopology** interface for the input multiplexer device:</span></span>

1.  <span data-ttu-id="b0b68-190">Appelez la méthode **IMMDevice :: Activate** pour obtenir l’interface **IDeviceTopology** pour l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b0b68-190">Call the **IMMDevice::Activate** method to get the **IDeviceTopology** interface for the endpoint device.</span></span>
2.  <span data-ttu-id="b0b68-191">Avec l’interface **IDeviceTopology** obtenue à l’étape précédente, appelez la méthode [**IDeviceTopology :: GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) pour obtenir l’interface **IConnector** du connecteur unique (numéro de connecteur 0) dans l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b0b68-191">With the **IDeviceTopology** interface obtained in the preceding step, call the [**IDeviceTopology::GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) method to get the **IConnector** interface of the single connector (connector number 0) in the endpoint device.</span></span>
3.  <span data-ttu-id="b0b68-192">Avec l’interface **IConnector** obtenue à l’étape précédente, appelez la méthode [**IConnector :: GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) pour obtenir l’interface **IConnector** du connecteur dans le périphérique multiplexeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b0b68-192">With the **IConnector** interface obtained in the preceding step, call the [**IConnector::GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) method to get the **IConnector** interface of the connector in the input multiplexer device.</span></span>
4.  <span data-ttu-id="b0b68-193">Interrogez l’interface **IConnector** obtenue à l’étape précédente pour son interface **IPart** .</span><span class="sxs-lookup"><span data-stu-id="b0b68-193">Query the **IConnector** interface obtained in the preceding step for its **IPart** interface.</span></span>
5.  <span data-ttu-id="b0b68-194">Avec l’interface **IPart** obtenue à l’étape précédente, appelez la méthode [**IPart :: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) pour obtenir l’interface **IDeviceTopology** pour le périphérique multiplexeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b0b68-194">With the **IPart** interface obtained in the preceding step, call the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method to get the **IDeviceTopology** interface for the input multiplexer device.</span></span>

<span data-ttu-id="b0b68-195">Avant que l’utilisateur puisse enregistrer à partir du microphone dans le diagramme précédent, l’application cliente doit s’assurer que le multiplexeur sélectionne l’entrée microphone.</span><span class="sxs-lookup"><span data-stu-id="b0b68-195">Before the user can record from the microphone in the preceding diagram, the client application must make certain that the multiplexer selects the microphone input.</span></span> <span data-ttu-id="b0b68-196">L’exemple de code suivant montre comment un client peut traverser le chemin de données à partir du microphone jusqu’à ce qu’il trouve le multiplexeur, qu’il programme ensuite pour sélectionner l’entrée microphone :</span><span class="sxs-lookup"><span data-stu-id="b0b68-196">The following code example shows how a client can traverse the data path from the microphone until it finds the multiplexer, which it then programs to select the microphone input:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



<span data-ttu-id="b0b68-197">L’API DeviceTopology implémente une interface [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) pour encapsuler un multiplexeur, tel que celui du diagramme précédent.</span><span class="sxs-lookup"><span data-stu-id="b0b68-197">The DeviceTopology API implements an [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) interface to encapsulate a multiplexer, such as the one in the preceding diagram.</span></span> <span data-ttu-id="b0b68-198">(Une interface [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) encapsule un démultiplexeur.) Dans l’exemple de code précédent, la boucle interne de la fonction SelectCaptureDevice interroge chaque sous-unité trouvée pour déterminer si la sous-unité est un multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="b0b68-198">(An [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) interface encapsulates a demultiplexer.) In the preceding code example, the inner loop of the SelectCaptureDevice function queries each subunit that it finds to discover whether the subunit is a multiplexer.</span></span> <span data-ttu-id="b0b68-199">Si la sous-unité est un multiplexeur, la fonction appelle la méthode [**IAudioInputSelector :: SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) pour sélectionner l’entrée qui se connecte au flux de données à partir de l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b0b68-199">If the subunit is a multiplexer, then the function calls the [**IAudioInputSelector::SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) method to select the input that connects to the stream from the endpoint device.</span></span>

<span data-ttu-id="b0b68-200">Dans l’exemple de code précédent, chaque itération de la boucle externe traverse une topologie d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b0b68-200">In the preceding code example, each iteration of the outer loop traverses one device topology.</span></span> <span data-ttu-id="b0b68-201">Lors du parcours des topologies d’appareil dans le diagramme précédent, la première itération traverse l’appareil de multiplexage d’entrée et la deuxième itération traverse l’appareil de capture d’onde.</span><span class="sxs-lookup"><span data-stu-id="b0b68-201">When traversing the device topologies in the preceding diagram, the first iteration traverses the input multiplexer device and the second iteration traverses the wave capture device.</span></span> <span data-ttu-id="b0b68-202">La fonction se termine lorsqu’elle atteint le connecteur sur le bord droit du diagramme.</span><span class="sxs-lookup"><span data-stu-id="b0b68-202">The function will terminate when it reaches the connector at the right edge of the diagram.</span></span> <span data-ttu-id="b0b68-203">L’arrêt se produit lorsque la fonction détecte un connecteur avec un \_ type de connexion d’e/s logicielles.</span><span class="sxs-lookup"><span data-stu-id="b0b68-203">Termination occurs when the function detects a connector with a Software\_IO connection type.</span></span> <span data-ttu-id="b0b68-204">Ce type de connexion identifie le point auquel l’appareil de l’adaptateur se connecte au bus système.</span><span class="sxs-lookup"><span data-stu-id="b0b68-204">This connection type identifies the point at which the adapter device connects to the system bus.</span></span>

<span data-ttu-id="b0b68-205">L’appel à la méthode [**IPart :: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) dans l’exemple de code précédent obtient une valeur d’énumération **IPartType** qui indique si la partie actuelle est un connecteur ou une sous-unité de traitement audio.</span><span class="sxs-lookup"><span data-stu-id="b0b68-205">The call to the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) method in the preceding code example obtains an **IPartType** enumeration value that indicates whether the current part is a connector or an audio-processing subunit.</span></span>

<span data-ttu-id="b0b68-206">La boucle interne dans l’exemple de code précédent suit le lien entre un composant et le suivant en appelant la méthode [**IPart :: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) .</span><span class="sxs-lookup"><span data-stu-id="b0b68-206">The inner loop in the preceding code example steps across the link from one part to the next by calling the [**IPart::EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) method.</span></span> <span data-ttu-id="b0b68-207">(Il existe également une méthode [**IPart :: EnumPartsIncoming pour effectuer**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) un pas à pas détaillé dans le sens inverse.) Cette méthode récupère un objet [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) qui contient une liste de toutes les Parties sortantes.</span><span class="sxs-lookup"><span data-stu-id="b0b68-207">(There's also an [**IPart::EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) method for stepping in the opposite direction.) This method retrieves an [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) object that contains a list of all the outgoing parts.</span></span> <span data-ttu-id="b0b68-208">Toutefois, toute partie que la fonction SelectCaptureDevice attend à rencontrer dans un appareil de capture aura toujours une seule partie sortante.</span><span class="sxs-lookup"><span data-stu-id="b0b68-208">However, any part that the SelectCaptureDevice function expects to encounter in a capture device will always have exactly one outgoing part.</span></span> <span data-ttu-id="b0b68-209">Ainsi, l’appel suivant à [**IPartsList :: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) demande toujours la première partie de la liste, la partie numéro 0, car la fonction part du principe qu’il s’agit de la seule partie de la liste.</span><span class="sxs-lookup"><span data-stu-id="b0b68-209">Thus, the subsequent call to [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) always requests the first part in the list, part number 0, because the function assumes that this is the only part in the list.</span></span>

<span data-ttu-id="b0b68-210">Si la fonction SelectCaptureDevice rencontre une topologie pour laquelle cette hypothèse n’est pas valide, la fonction peut ne pas réussir à configurer correctement l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b0b68-210">If the SelectCaptureDevice function encounters a topology for which that assumption is not valid, the function might fail to configure the device correctly.</span></span> <span data-ttu-id="b0b68-211">Pour éviter ce type d’échec, une version plus générale de la fonction peut effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0b68-211">To avoid such a failure, a more general-purpose version of the function might do the following:</span></span>

-   <span data-ttu-id="b0b68-212">Appelez la méthode [**IPartsList :: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) pour déterminer le nombre de parties sortantes.</span><span class="sxs-lookup"><span data-stu-id="b0b68-212">Call the [**IPartsList::GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) method to determine the number of outgoing parts.</span></span>
-   <span data-ttu-id="b0b68-213">Pour chaque partie sortante, appelez **IPartsList :: GetPart** pour commencer à parcourir le chemin de données qui amène le composant.</span><span class="sxs-lookup"><span data-stu-id="b0b68-213">For each outgoing part, call **IPartsList::GetPart** to begin to traverse the data path that leads from the part.</span></span>

<span data-ttu-id="b0b68-214">Certains éléments, mais pas nécessairement tous, ont des contrôles matériels associés que les clients peuvent définir ou obtenir.</span><span class="sxs-lookup"><span data-stu-id="b0b68-214">Some, but not necessarily all, parts have associated hardware controls that clients can set or get.</span></span> <span data-ttu-id="b0b68-215">Une partie particulière peut avoir zéro, un ou plusieurs contrôles matériels.</span><span class="sxs-lookup"><span data-stu-id="b0b68-215">A particular part might have zero, one, or more hardware controls.</span></span> <span data-ttu-id="b0b68-216">Un contrôle matériel est représenté par les paires d’interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0b68-216">A hardware control is represented by the following pair of interfaces:</span></span>

-   <span data-ttu-id="b0b68-217">Interface de contrôle générique, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), qui a des méthodes communes à tous les contrôles matériels.</span><span class="sxs-lookup"><span data-stu-id="b0b68-217">A generic control interface, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), which has methods that are common to all hardware controls.</span></span>
-   <span data-ttu-id="b0b68-218">Interface spécifique à une fonction (par exemple, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) qui expose les paramètres de contrôle pour un type particulier de contrôle matériel (par exemple, un contrôle de volume).</span><span class="sxs-lookup"><span data-stu-id="b0b68-218">A function-specific interface (for example, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) that exposes the control parameters for a particular type of hardware control (for example, a volume control).</span></span>

<span data-ttu-id="b0b68-219">Pour énumérer les contrôles matériels d’un composant, le client appelle d’abord la méthode [**IPart :: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) pour déterminer le nombre de contrôles matériels associés à la partie.</span><span class="sxs-lookup"><span data-stu-id="b0b68-219">To enumerate the hardware controls for a part, the client first calls the [**IPart::GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) method to determine the number of hardware controls that are associated with the part.</span></span> <span data-ttu-id="b0b68-220">Ensuite, le client effectue une série d’appels à la méthode [**IPart :: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) pour obtenir l’interface **IControlInterface** pour chaque contrôle matériel.</span><span class="sxs-lookup"><span data-stu-id="b0b68-220">Next, the client makes a series of calls to the [**IPart::GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) method to obtain the **IControlInterface** interface for each hardware control.</span></span> <span data-ttu-id="b0b68-221">Enfin, le client obtient l’interface spécifique à la fonction pour chaque contrôle matériel en appelant la méthode [**IControlInterface :: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) pour obtenir l’ID d’interface.</span><span class="sxs-lookup"><span data-stu-id="b0b68-221">Finally, the client obtains the function-specific interface for each hardware control by calling the [**IControlInterface::GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) method to obtain the interface ID.</span></span> <span data-ttu-id="b0b68-222">Le client appelle la méthode [**IPart :: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) avec cet ID pour obtenir l’interface spécifique à la fonction.</span><span class="sxs-lookup"><span data-stu-id="b0b68-222">The client calls the [**IPart::Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) method with this ID to obtain the function-specific interface.</span></span>

<span data-ttu-id="b0b68-223">Un composant qui est un connecteur peut prendre en charge l’une des interfaces de contrôle spécifiques aux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0b68-223">A part that is a connector might support one of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="b0b68-224">**IKsFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="b0b68-224">**IKsFormatSupport**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [<span data-ttu-id="b0b68-225">**IKsJackDescription**</span><span class="sxs-lookup"><span data-stu-id="b0b68-225">**IKsJackDescription**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

<span data-ttu-id="b0b68-226">Une partie qui est une sous-unité peut prendre en charge une ou plusieurs des interfaces de contrôle spécifiques aux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0b68-226">A part that is a subunit might support one or more of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="b0b68-227">**IAudioAutoGainControl**</span><span class="sxs-lookup"><span data-stu-id="b0b68-227">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [<span data-ttu-id="b0b68-228">**IAudioBass**</span><span class="sxs-lookup"><span data-stu-id="b0b68-228">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [<span data-ttu-id="b0b68-229">**IAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="b0b68-229">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [<span data-ttu-id="b0b68-230">**IAudioInputSelector**</span><span class="sxs-lookup"><span data-stu-id="b0b68-230">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [<span data-ttu-id="b0b68-231">**IAudioLoudness**</span><span class="sxs-lookup"><span data-stu-id="b0b68-231">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [<span data-ttu-id="b0b68-232">**IAudioMidrange**</span><span class="sxs-lookup"><span data-stu-id="b0b68-232">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [<span data-ttu-id="b0b68-233">**IAudioMute**</span><span class="sxs-lookup"><span data-stu-id="b0b68-233">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [<span data-ttu-id="b0b68-234">**IAudioOutputSelector**</span><span class="sxs-lookup"><span data-stu-id="b0b68-234">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [<span data-ttu-id="b0b68-235">**IAudioPeakMeter**</span><span class="sxs-lookup"><span data-stu-id="b0b68-235">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [<span data-ttu-id="b0b68-236">**IAudioTreble**</span><span class="sxs-lookup"><span data-stu-id="b0b68-236">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [<span data-ttu-id="b0b68-237">**IAudioVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="b0b68-237">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [<span data-ttu-id="b0b68-238">**IDeviceSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="b0b68-238">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

<span data-ttu-id="b0b68-239">Une partie prend en charge l’interface **IDeviceSpecificProperty** uniquement si le contrôle matériel sous-jacent a une valeur de contrôle spécifique à l’appareil et que le contrôle ne peut pas être représenté de manière appropriée par une autre interface spécifique à la fonction dans la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="b0b68-239">A part supports the **IDeviceSpecificProperty** interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other function-specific interface in the preceding list.</span></span> <span data-ttu-id="b0b68-240">En règle générale, une propriété spécifique à un appareil est utile uniquement à un client qui peut déduire la signification de la valeur de propriété à partir d’informations telles que le type de partie, le sous-type de partie et le nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="b0b68-240">Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name.</span></span> <span data-ttu-id="b0b68-241">Le client peut obtenir ces informations en appelant les méthodes [**IPart :: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart :: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)et [**IPart :: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .</span><span class="sxs-lookup"><span data-stu-id="b0b68-241">The client can obtain this information by calling the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype), and [**IPart::GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0b68-242">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0b68-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b68-243">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="b0b68-243">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
