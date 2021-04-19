---
description: Interface de programmation d’applications WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interface de programmation d’applications WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530172"
---
# <a name="wpd-application-programming-interface"></a><span data-ttu-id="25ffb-103">Interface de programmation d’applications WPD</span><span class="sxs-lookup"><span data-stu-id="25ffb-103">WPD Application Programming Interface</span></span>

<span data-ttu-id="25ffb-104">Les applications basées sur des appareils mobiles Windows peuvent explorer un appareil, envoyer et recevoir du contenu et même contrôler l’appareil, par exemple, prendre une photo ou envoyer un SMS.</span><span class="sxs-lookup"><span data-stu-id="25ffb-104">Applications built on Windows Portable Devices can explore a device, send and receive content, and even control the device, for example, take a picture or send a text message.</span></span> <span data-ttu-id="25ffb-105">Le système est conçu pour être flexible afin que de nombreux types d’appareils puissent être explorés et extensibles afin que les développeurs de pilotes puissent définir des propriétés personnalisées et des commandes pour les appareils personnalisés.</span><span class="sxs-lookup"><span data-stu-id="25ffb-105">The system is designed to be flexible so that many types of devices can be explored, and extensible so that driver developers can define custom properties and commands for custom devices.</span></span>

<span data-ttu-id="25ffb-106">Le tableau suivant décrit les rubriques principales de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="25ffb-106">The following table describes the main topics of this documentation.</span></span>



| <span data-ttu-id="25ffb-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="25ffb-107">Topic</span></span>                                                                                                                  | <span data-ttu-id="25ffb-108">Description</span><span class="sxs-lookup"><span data-stu-id="25ffb-108">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25ffb-109">Exigences générales pour le développement d’applications</span><span class="sxs-lookup"><span data-stu-id="25ffb-109">General Requirements for Application Development</span></span>](general-requirements-for-application-development.md)               | <span data-ttu-id="25ffb-110">Configurations matérielle et logicielle requises pour développer des pilotes et des applications à l’aide d’appareils mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="25ffb-110">Hardware and software requirements to develop drivers and applications using Windows Portable Devices.</span></span>     |
| [<span data-ttu-id="25ffb-111">Configuration requise pour les applications Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="25ffb-111">Requirements for Windows Media DRM-Enabled Applications</span></span>](requirements-for-windows-media-drm-enabled-applications.md) | <span data-ttu-id="25ffb-112">Propriétés requises pour activer les transferts de contenu protégés par DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="25ffb-112">Properties that are required to enable Windows Media DRM-protected content transfers.</span></span>                      |
| [<span data-ttu-id="25ffb-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="25ffb-113">Samples</span></span>](sample.md)                                                                                                  | <span data-ttu-id="25ffb-114">Description de deux applications de bureau en ligne de commande fournies avec ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="25ffb-114">Description of two command-line desktop applications that are supplied with this software development kit.</span></span> |
| [<span data-ttu-id="25ffb-115">Vue d’ensemble de l’application</span><span class="sxs-lookup"><span data-stu-id="25ffb-115">Application Overview</span></span>](application-overview.md)                                                                       | <span data-ttu-id="25ffb-116">Concepts clés utilisés dans les appareils mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="25ffb-116">Key concepts used in Windows Portable Devices.</span></span>                                                             |
| [<span data-ttu-id="25ffb-117">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="25ffb-117">Programming Guide</span></span>](programming-guide.md)                                                                             | <span data-ttu-id="25ffb-118">Tâches clés qu’une application exécutera, avec des instructions pas à pas et des extraits de code.</span><span class="sxs-lookup"><span data-stu-id="25ffb-118">Key tasks that an application will perform, with step-by-step instructions and code snippets.</span></span>              |
| [<span data-ttu-id="25ffb-119">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="25ffb-119">Programming Reference</span></span>](programming-reference.md)                                                                     | <span data-ttu-id="25ffb-120">Guide de référence des interfaces et des types de données définis par les appareils mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="25ffb-120">Reference guide to the interfaces and data types defined by Windows Portable Devices.</span></span>                      |



 

<span data-ttu-id="25ffb-121">Les applications basées sur Windows Media Gestionnaire de périphériques ou l’acquisition d’images Windows peuvent accéder aux appareils mobiles Windows par le biais d’une couche de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="25ffb-121">Applications built on Windows Media Device Manager or Windows Image Acquisition can access Windows Portable Devices through a compatibility layer.</span></span>

<span data-ttu-id="25ffb-122">Microsoft fournit plusieurs pilotes pour les protocoles et les périphériques standard, y compris les périphériques MTP (Media Transport Protocol) et les périphériques de classe de stockage de masse (MSC).</span><span class="sxs-lookup"><span data-stu-id="25ffb-122">Microsoft provides several drivers for standard protocols and devices, including Media Transport Protocol (MTP) devices and Mass Storage Class (MSC) devices.</span></span> <span data-ttu-id="25ffb-123">Si vous êtes familiarisé avec l’infrastructure de pilote User-Mode, vous pouvez développer vos propres pilotes pour des appareils personnalisés.</span><span class="sxs-lookup"><span data-stu-id="25ffb-123">If you are familiar with the User-Mode Driver Framework, you can develop your own drivers for custom devices.</span></span>

 

 



