---
title: À propos de Bluetooth
description: Bluetooth est un protocole standard qui permet la connectivité sans fil pour une multitude d’appareils, notamment des ordinateurs, des imprimantes, des téléphones portables et des appareils portables.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, Description
- Bluetooth Bluetooth, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030851"
---
# <a name="about-bluetooth"></a><span data-ttu-id="99e6f-105">À propos de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="99e6f-105">About Bluetooth</span></span>

<span data-ttu-id="99e6f-106">Bluetooth est un protocole standard qui permet la connectivité sans fil pour une multitude d’appareils, notamment des ordinateurs, des imprimantes, des téléphones portables et des appareils portables.</span><span class="sxs-lookup"><span data-stu-id="99e6f-106">Bluetooth is an industry-standard protocol that enables wireless connectivity for a multitude of devices, including computers, printers, mobile phones, and handheld devices.</span></span>

<span data-ttu-id="99e6f-107">Les principales fonctionnalités de Bluetooth sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="99e6f-107">Key Bluetooth features include:</span></span>

-   <span data-ttu-id="99e6f-108">Protocole sans fil à faible consommation d’énergie et à faible coût avec prise en charge standard et acceptation mondiale.</span><span class="sxs-lookup"><span data-stu-id="99e6f-108">A low-cost, low-power consumption wireless protocol with industry-standard support and worldwide acceptance.</span></span>
-   <span data-ttu-id="99e6f-109">Interface de programmation définie et familière que les développeurs peuvent utiliser pour développer ou porter rapidement sur des applications.</span><span class="sxs-lookup"><span data-stu-id="99e6f-109">A defined and familiar programming interface that developers can use to quickly develop or port applications.</span></span>
-   <span data-ttu-id="99e6f-110">Un site Web officiel et une organisation coopérative à l’ensemble du secteur qui explique, encourage et standardise la technologie Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="99e6f-110">An official Web site and an industry-wide cooperative organization that explains, promotes, and standardizes Bluetooth technology.</span></span> <span data-ttu-id="99e6f-111">Pour plus d’informations, consultez [www.Bluetooth.com](https://www.bluetooth.com/).</span><span class="sxs-lookup"><span data-stu-id="99e6f-111">For more information, see [www.bluetooth.com](https://www.bluetooth.com/).</span></span>

<span data-ttu-id="99e6f-112">Bluetooth sur Windows fournit des services essentiels similaires à ceux exposés par le protocole de contrôle de transmission (TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="99e6f-112">Bluetooth on Windows provides core services that are similar to those exposed by Transmission Control Protocol (the TCP part of TCP/IP).</span></span> <span data-ttu-id="99e6f-113">À l’instar de nombreux protocoles et services de mise en réseau, la connectivité Bluetooth et le transfert de données sont programmés via des appels de fonction Windows Sockets, à l’aide de techniques de programmation Windows Sockets courantes et d’extensions Bluetooth spécifiques.</span><span class="sxs-lookup"><span data-stu-id="99e6f-113">Like many networking protocols and services, Bluetooth connectivity and data transfer are programmed through Windows Sockets function calls, using common Windows Sockets programming techniques and specific Bluetooth extensions.</span></span> <span data-ttu-id="99e6f-114">Toutefois, étant donné que des différences significatives existent entre un réseau câblé, un réseau fixe et un réseau ad hoc sans fil, Bluetooth fournit des extensions telles que la détection de service/appareil et la notification qui permettent aux applications de fonctionner correctement dans l’environnement sans fil.</span><span class="sxs-lookup"><span data-stu-id="99e6f-114">However, because significant differences exist between a wired, fixed network and a wireless ad-hoc network, Bluetooth provides extensions such as service/device discovery and notification that enable applications to operate properly in the wireless environment.</span></span> <span data-ttu-id="99e6f-115">Ces extensions vous permettent également d’effectuer un Portage simple vers des technologies similaires, telles que IrDA, ou de futurs transports sans fil.</span><span class="sxs-lookup"><span data-stu-id="99e6f-115">These extensions also pave the way for simple porting to similar technologies, such as IrDA, or future wireless transports.</span></span>

<span data-ttu-id="99e6f-116">Microsoft assure la prise en charge de Bluetooth sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures, sur Windows XP Embedded avec Service Pack 2 et sur Windows CE.</span><span class="sxs-lookup"><span data-stu-id="99e6f-116">Microsoft provides support for Bluetooth on Windows XP with Service Pack 1 (SP1) and later, on Windows XP Embedded with Service Pack 2, and on Windows CE.</span></span> <span data-ttu-id="99e6f-117">Les applications Bluetooth qui s’exécutent sur Windows XP doivent pouvoir s’exécuter sur une image d’exécution basée sur Windows XP Embedded qui comprend les dépendances requises.</span><span class="sxs-lookup"><span data-stu-id="99e6f-117">Bluetooth applications that run on Windows XP should be able to run on a Windows XP Embedded-based run-time image that includes the required dependencies.</span></span> <span data-ttu-id="99e6f-118">Pour plus d’informations sur Windows XP Embedded, consultez la documentation de l’aide de Windows XP Embedded sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="99e6f-118">For more information about Windows XP Embedded, see the Windows XP Embedded Help documentation on MSDN.</span></span> <span data-ttu-id="99e6f-119">Pour plus d’informations sur la programmation de Windows CE, consultez le kit de développement logiciel (SDK) Windows CE.</span><span class="sxs-lookup"><span data-stu-id="99e6f-119">For more information about Windows CE programming, consult the Windows CE SDK.</span></span>

<span data-ttu-id="99e6f-120">Microsoft propose deux approches pour la programmation de Bluetooth sur Windows :</span><span class="sxs-lookup"><span data-stu-id="99e6f-120">Microsoft provides two approaches for programming Bluetooth on Windows:</span></span>

-   <span data-ttu-id="99e6f-121">Utilisation de l’interface Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="99e6f-121">Using the Windows Sockets interface</span></span>
-   <span data-ttu-id="99e6f-122">Gestion des appareils directement à l’aide des interfaces Bluetooth à l’aide d’interfaces</span><span class="sxs-lookup"><span data-stu-id="99e6f-122">Managing devices directly by using nonsocket Bluetooth interfaces</span></span>

<span data-ttu-id="99e6f-123">Cette section fournit des informations générales sur ces deux approches dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="99e6f-123">This section provides overview information about both of these approaches in the following topics.</span></span> <span data-ttu-id="99e6f-124">Pour plus d’informations sur l’utilisation des éléments de l’API Windows Sockets pour programmer Bluetooth, consultez la page [programmation Bluetooth avec Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="99e6f-124">For more information about using Windows Sockets API elements to program Bluetooth, see [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span></span>



| <span data-ttu-id="99e6f-125">Section</span><span class="sxs-lookup"><span data-stu-id="99e6f-125">Section</span></span>                                                                                | <span data-ttu-id="99e6f-126">Content</span><span class="sxs-lookup"><span data-stu-id="99e6f-126">Content</span></span>                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="99e6f-127">Prise en charge de Windows Sockets pour Bluetooth</span><span class="sxs-lookup"><span data-stu-id="99e6f-127">Windows Sockets Support for Bluetooth</span></span>](windows-sockets-support-for-bluetooth.md)     | <span data-ttu-id="99e6f-128">Décrit la relation entre Bluetooth et Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="99e6f-128">Describes the relationship between Bluetooth and Windows Sockets.</span></span> |
| [<span data-ttu-id="99e6f-129">Gestion des appareils et des services Bluetooth</span><span class="sxs-lookup"><span data-stu-id="99e6f-129">Managing Bluetooth Devices and Services</span></span>](managing-bluetooth-devices-and-services.md) | <span data-ttu-id="99e6f-130">Décrit comment gérer des appareils et des services Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="99e6f-130">Describes how to manage Bluetooth devices and services.</span></span>           |



 

 

 




