---
description: Suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116247"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="ebb4b-103">Suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="ebb4b-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ebb4b-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="ebb4b-104">Affected Platforms</span></span>

<span data-ttu-id="ebb4b-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebb4b-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="ebb4b-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebb4b-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="ebb4b-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ebb4b-107">Feature Impact</span></span>

 <span data-ttu-id="ebb4b-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="ebb4b-108">**Severity** - Low</span></span>  
<span data-ttu-id="ebb4b-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="ebb4b-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="ebb4b-110">Description</span><span class="sxs-lookup"><span data-stu-id="ebb4b-110">Description</span></span>

<span data-ttu-id="ebb4b-111">Microsoft a remplacé le composant mode noyau de la pile de pilotes USB Windows Vista (WPDUSB.SYS) pour les appareils mobiles Windows (WPD) par le pilote de WINUSB.SYS générique.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="ebb4b-112">La communication avec le pilote de WPDUSB.SYS d’origine était par le biais de codes de contrôle d’e/s privés (IOCTL). la prise en charge de ces derniers a également été supprimée.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="ebb4b-113">Tout consommateur de ces codes IOCTL aurait été responsable de l’interprétation et de l’implémentation appropriées du protocole MTP (Media Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="ebb4b-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="ebb4b-114">Windows Vista ne prenait pas en charge l’utilisation de ces codes IOCTL par des applications tierces.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="ebb4b-115">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="ebb4b-115">Manifestation of Impact</span></span>

<span data-ttu-id="ebb4b-116">Toute application qui dépendait de la disponibilité de ces codes IOCTL privés n’aura plus accès aux périphériques MTP connectés par USB.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="ebb4b-117">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="ebb4b-117">Mitigation</span></span>

<span data-ttu-id="ebb4b-118">Les utilisateurs d’une application qui dépend des codes IOCTL privés doivent utiliser une application différente (ou une version mise à jour de l’application) pour accéder à l’appareil MTP USB.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="ebb4b-119">Solution</span><span class="sxs-lookup"><span data-stu-id="ebb4b-119">Solution</span></span>

<span data-ttu-id="ebb4b-120">Les applications doivent utiliser l’API des appareils mobiles Windows (WPD) pour rechercher et interagir avec n’importe quel appareil WPD.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="ebb4b-121">Bien qu’un pourcentage important d’appareils WPD implémentent MTP pour la communication avec le PC, WPD n’est pas limité aux seuls appareils MTP.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="ebb4b-122">En outre, lorsque l’accès direct à l’appareil via les IOCTL privées aurait limité l’application à la communication avec uniquement les périphériques connectés par USB, l’utilisation de l’API WPD étend la liste des options de connectivité à d’autres protocoles de communication (par exemple, Wi-Fi).</span><span class="sxs-lookup"><span data-stu-id="ebb4b-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="ebb4b-123">Dans les rares cas où l’application doit prendre en charge la MTP, l’API WPD fournit un mécanisme direct pour les commandes MTP brutes.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="ebb4b-124">Exploitation des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ebb4b-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="ebb4b-125">L’API WPD est prise en charge dans Windows XP (via le kit de développement logiciel (SDK) Windows format), Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="ebb4b-126">L’implémentation de Windows 7 d’WPD ajoute la prise en charge de MTP sur Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ebb4b-127">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="ebb4b-127">Links to Other Resources</span></span>

[<span data-ttu-id="ebb4b-128">Appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="ebb4b-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
