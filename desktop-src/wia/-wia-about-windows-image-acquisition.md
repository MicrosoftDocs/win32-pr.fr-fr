---
description: L’interface WIA (Windows Image Acquisition) est à la fois une API et une interface de pilote de périphérique (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: À propos de l’acquisition d’images Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517097"
---
# <a name="about-windows-image-acquisition"></a><span data-ttu-id="af940-103">À propos de l’acquisition d’images Windows</span><span class="sxs-lookup"><span data-stu-id="af940-103">About Windows Image Acquisition</span></span>

<span data-ttu-id="af940-104">L’interface WIA (Windows Image Acquisition) est à la fois une API et une interface de pilote de périphérique (DDI).</span><span class="sxs-lookup"><span data-stu-id="af940-104">The Windows Image Acquisition (WIA) interface is both an API and a device driver interface (DDI).</span></span> <span data-ttu-id="af940-105">L’API WIA est conçue pour permettre aux applications d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="af940-105">The WIA API is designed to allow applications to:</span></span>

-   <span data-ttu-id="af940-106">S’exécute dans un environnement robuste et stable.</span><span class="sxs-lookup"><span data-stu-id="af940-106">Run in a robust and stable environment.</span></span>
-   <span data-ttu-id="af940-107">Réduire les problèmes d’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="af940-107">Minimize interoperability problems.</span></span>
-   <span data-ttu-id="af940-108">Énumérer les appareils d’acquisition d’images disponibles.</span><span class="sxs-lookup"><span data-stu-id="af940-108">Enumerate available image acquisition devices.</span></span>
-   <span data-ttu-id="af940-109">Créer des connexions à plusieurs appareils simultanément.</span><span class="sxs-lookup"><span data-stu-id="af940-109">Create connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="af940-110">Interrogez les propriétés des appareils de manière standard et extensible.</span><span class="sxs-lookup"><span data-stu-id="af940-110">Query properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="af940-111">Acquérir des données d’appareil à l’aide de mécanismes de transfert standard et hautes performances.</span><span class="sxs-lookup"><span data-stu-id="af940-111">Acquire device data using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="af940-112">Conserver les propriétés de l’image entre les transferts de données.</span><span class="sxs-lookup"><span data-stu-id="af940-112">Maintain image properties across data transfers.</span></span>
-   <span data-ttu-id="af940-113">Être informé d’un grand nombre d’événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="af940-113">Be notified of a wide variety of device events.</span></span>

<span data-ttu-id="af940-114">Le WIADDI est conçu pour réduire la quantité de code qu’un fournisseur de matériel doit écrire, tout en conservant la flexibilité nécessaire pour concevoir des solutions individuelles.</span><span class="sxs-lookup"><span data-stu-id="af940-114">The WIADDI is designed to minimize the amount of code a hardware vendor must write, while maintaining the flexibility to craft individual solutions.</span></span> <span data-ttu-id="af940-115">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="af940-115">This is accomplished by:</span></span>

-   <span data-ttu-id="af940-116">Fournir une bibliothèque de services d’appareils standard qui effectue la plupart des opérations de pilote.</span><span class="sxs-lookup"><span data-stu-id="af940-116">Providing a standard device service library that performs most driver operations.</span></span>
-   <span data-ttu-id="af940-117">Promouvoir les normes de communication des appareils de l’industrie pour qu’un pilote WIA prenne en charge la plupart des appareils WIA.</span><span class="sxs-lookup"><span data-stu-id="af940-117">Promoting industry device communications standards so that one WIA driver supports most WIA devices.</span></span> <span data-ttu-id="af940-118">Par exemple, le protocole PTP (Image Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="af940-118">For example, Picture Transfer Protocol (PTP).</span></span>
-   <span data-ttu-id="af940-119">Autoriser le pilote de périphérique à prendre en charge des interfaces personnalisées, sans exiger qu’il utilise la bibliothèque de service d’appareil standard.</span><span class="sxs-lookup"><span data-stu-id="af940-119">Allowing the device driver to support custom interfaces, while not requiring that it use the standard device service library.</span></span> <span data-ttu-id="af940-120">Toutefois, les pilotes doivent toujours implémenter les interfaces WIA standard.</span><span class="sxs-lookup"><span data-stu-id="af940-120">However, drivers still need to implement the standard WIA interfaces.</span></span>

<span data-ttu-id="af940-121">Cette section présente une vue d’ensemble de l’interface WIA dans les domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="af940-121">This section presents a brief overview of the WIA interface in the following areas:</span></span>

-   [<span data-ttu-id="af940-122">Architecture WIA</span><span class="sxs-lookup"><span data-stu-id="af940-122">WIA Architecture</span></span>](-wia-wia-architecture.md)
-   [<span data-ttu-id="af940-123">Compatibilité STI</span><span class="sxs-lookup"><span data-stu-id="af940-123">STI Compatibility</span></span>](-wia-sti-compatibility.md)
-   [<span data-ttu-id="af940-124">Compatibilité avec TWAIN</span><span class="sxs-lookup"><span data-stu-id="af940-124">TWAIN Compatibility</span></span>](-wia-twain-compatibility.md)
-   [<span data-ttu-id="af940-125">Gestionnaire de périphériques WIA</span><span class="sxs-lookup"><span data-stu-id="af940-125">WIA Device Manager</span></span>](-wia-wia-device-manager.md)
-   [<span data-ttu-id="af940-126">Bibliothèque du service WIA minipilote</span><span class="sxs-lookup"><span data-stu-id="af940-126">WIA Minidriver Service Library</span></span>](-wia-wia-minidriver-service-library.md)
-   [<span data-ttu-id="af940-127">Minipilote WIA</span><span class="sxs-lookup"><span data-stu-id="af940-127">WIA Minidriver</span></span>](-wia-wia-minidriver.md)

 

 



