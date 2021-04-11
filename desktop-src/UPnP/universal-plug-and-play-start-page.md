---
title: API UPnP
description: L’infrastructure UPnP permet la mise en réseau dynamique d’appareils intelligents, de périphériques sans fil et de PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102504"
---
# <a name="upnp-apis"></a><span data-ttu-id="47999-104">API UPnP</span><span class="sxs-lookup"><span data-stu-id="47999-104">UPnP APIs</span></span>

## <a name="purpose"></a><span data-ttu-id="47999-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="47999-105">Purpose</span></span>

<span data-ttu-id="47999-106">L’infrastructure UPnP permet la mise en réseau dynamique d’appareils intelligents, de périphériques sans fil et de PC.</span><span class="sxs-lookup"><span data-stu-id="47999-106">The UPnP  framework enables dynamic networking of intelligent appliances, wireless devices, and PCs.</span></span> <span data-ttu-id="47999-107">Il existe deux API pour l’utilisation d’appareils certifiés UPnP :</span><span class="sxs-lookup"><span data-stu-id="47999-107">There are two APIs for working with UPnP-certified devices:</span></span>

-   <span data-ttu-id="47999-108">L’API du point de contrôle, qui se compose d’un ensemble d’interfaces COM utilisées pour rechercher et contrôler des appareils.</span><span class="sxs-lookup"><span data-stu-id="47999-108">The Control Point API, which consists of a set of COM interfaces used to find and control devices.</span></span>
-   <span data-ttu-id="47999-109">L’API d’hôte d’appareil, qui se compose d’un ensemble d’interfaces COM utilisées pour implémenter des appareils hébergés par un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="47999-109">The Device Host API, which consists of a set of COM interfaces used to implement devices that are hosted by a computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="47999-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="47999-110">Where applicable</span></span>

<span data-ttu-id="47999-111">L’API du point de contrôle permet aux développeurs d’écrire des applications qui recherchent et contrôlent les appareils certifiés UPnP.</span><span class="sxs-lookup"><span data-stu-id="47999-111">The Control Point API enables developers to write applications that search for and control UPnP-certified devices.</span></span> <span data-ttu-id="47999-112">L’API d’hôte d’appareil permet aux développeurs d’implémenter les fonctionnalités des appareils certifiés UPnP et d’utiliser l’hôte d’appareil pour gérer les fonctions de découverte, de description, de contrôle, de présentation et d’événement d’un appareil certifié UPnP.</span><span class="sxs-lookup"><span data-stu-id="47999-112">The Device Host API enables developers to implement the functionality of UPnP-certified devices, and use the device host to manage the discovery, description, control, presentation, and eventing functions of a UPnP-certified device.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="47999-113">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="47999-113">Developer audience</span></span>

<span data-ttu-id="47999-114">Les développeurs qui utilisent les API de point de contrôle et les API d’hôte d’appareil doivent être familiarisés avec l’architecture de périphérique UPnP.</span><span class="sxs-lookup"><span data-stu-id="47999-114">Developers using the Control Point APIs and Device Host APIs must be familiar with the UPnP device architecture.</span></span> <span data-ttu-id="47999-115">Pour plus d’informations, consultez la [documentation relative](https://openconnectivity.org/resources/upnpresources.zip) à l’implémentation d’UPnP et le [Forum UPnP](https://openconnectivity.org/).</span><span class="sxs-lookup"><span data-stu-id="47999-115">For more information, see the [UPnP Implementation Documentation](https://openconnectivity.org/resources/upnpresources.zip) and the [UPnP Forum](https://openconnectivity.org/).</span></span>

<span data-ttu-id="47999-116">Les développeurs qui utilisent les API d’hôte d’appareil doivent être familiarisés avec les interfaces Active Template Library (ATL) et COM.</span><span class="sxs-lookup"><span data-stu-id="47999-116">Developers who are using the Device Host APIs should be familiar with the Active Template Library (ATL) and COM interfaces.</span></span>

<span data-ttu-id="47999-117">Les API de point de contrôle et les API d’hôte d’appareil sont utilisées par diverses applications, des scripts incorporés dans les pages HTML aux programmes C++ et Microsoft Visual Basic à part entière.</span><span class="sxs-lookup"><span data-stu-id="47999-117">The Control Point APIs and Device Host APIs are used by a variety of applications, from scripts embedded in HTML pages to full-fledged C++ and Microsoft Visual Basic programs.</span></span>

<span data-ttu-id="47999-118">Seule l’API du point de contrôle prend en charge les Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="47999-118">Only the Control Point API supports Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="47999-119">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="47999-119">Run-time requirements</span></span>

<span data-ttu-id="47999-120">L’API du point de contrôle est utilisée sur les ordinateurs qui exécutent Microsoft Windows Millennium Edition, Windows XP, Windows XP professionnel et Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="47999-120">The Control Point API is used on computers running Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="47999-121">L’API de l’hôte d’appareil est utilisée sur les ordinateurs exécutant Windows XP, Windows XP professionnel et Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="47999-121">The Device Host API is used on computers running Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="47999-122">Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous à « conditions requises » dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="47999-122">For more specific information about which operating systems support a particular function, refer to "Requirements" in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="47999-123">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="47999-123">In this section</span></span>



| <span data-ttu-id="47999-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="47999-124">Topic</span></span>                                                                                          | <span data-ttu-id="47999-125">Description</span><span class="sxs-lookup"><span data-stu-id="47999-125">Description</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47999-126">Vue d’ensemble de l’architecture UPnP</span><span class="sxs-lookup"><span data-stu-id="47999-126">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)<br/>            | <span data-ttu-id="47999-127">Informations générales et arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="47999-127">General information and background.</span></span><br/>                                                     |
| [<span data-ttu-id="47999-128">Vue d’ensemble du point de contrôle</span><span class="sxs-lookup"><span data-stu-id="47999-128">Control Point Overview</span></span>](control-point-api.md)<br/>                                     | <span data-ttu-id="47999-129">Informations générales sur l’API du point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="47999-129">General information about the Control Point API.</span></span><br/>                                        |
| [<span data-ttu-id="47999-130">Utilisation de l’API de point de contrôle</span><span class="sxs-lookup"><span data-stu-id="47999-130">Using the Control Point API</span></span>](using-the-control-point-api-with-upnp-technology.md)<br/> | <span data-ttu-id="47999-131">Exemple de code qui montre comment développer des applications qui contrôlent les appareils certifiés UPnP.</span><span class="sxs-lookup"><span data-stu-id="47999-131">Sample code that shows how to develop applications that control UPnP-certified devices.</span></span><br/> |
| [<span data-ttu-id="47999-132">Informations de référence sur l’API point de contrôle</span><span class="sxs-lookup"><span data-stu-id="47999-132">Control Point API Reference</span></span>](control-point-api-with-upnp-technology-reference.md)<br/> | <span data-ttu-id="47999-133">Documentation des interfaces, des méthodes et des événements du composant de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="47999-133">Documentation of Control Point component interfaces, methods, and events.</span></span><br/>               |
| [<span data-ttu-id="47999-134">Vue d’ensemble de l’API Device Host</span><span class="sxs-lookup"><span data-stu-id="47999-134">Device Host API Overview</span></span>](device-host-api.md)<br/>                                     | <span data-ttu-id="47999-135">Informations générales sur l’API de l’hôte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="47999-135">General information about the Device Host API.</span></span><br/>                                          |
| [<span data-ttu-id="47999-136">Utilisation de l’API de l’hôte d’appareil</span><span class="sxs-lookup"><span data-stu-id="47999-136">Using the Device Host API</span></span>](using-the-device-host-api-with-upnp-technology.md)<br/>     | <span data-ttu-id="47999-137">Exemple de code qui montre comment développer une application pour les appareils certifiés UPnP.</span><span class="sxs-lookup"><span data-stu-id="47999-137">Sample code that shows how to develop an application for UPnP-certified devices.</span></span><br/>        |
| [<span data-ttu-id="47999-138">Informations de référence sur l’API d’hôte d’appareil</span><span class="sxs-lookup"><span data-stu-id="47999-138">Device Host API Reference</span></span>](device-host-api-with-upnp-technology-reference.md)<br/>     | <span data-ttu-id="47999-139">Documentation des interfaces, des méthodes et des événements du composant hôte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="47999-139">Documentation of Device Host component interfaces, methods, and events.</span></span><br/>                 |



 

 

 





