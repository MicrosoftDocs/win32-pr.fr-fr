---
description: Windows Sockets 2 (Winsock) permet aux programmeurs de créer des applications Internet, intranet et réseau avancées pour transmettre des données d’application sur le câble, indépendamment du protocole réseau utilisé.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114294"
---
# <a name="windows-sockets-2"></a><span data-ttu-id="a7c1d-103">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="a7c1d-103">Windows Sockets 2</span></span>

## <a name="purpose"></a><span data-ttu-id="a7c1d-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="a7c1d-104">Purpose</span></span>

<span data-ttu-id="a7c1d-105">Windows Sockets 2 (Winsock) permet aux programmeurs de créer des applications Internet, intranet et réseau avancées pour transmettre des données d’application sur le câble, indépendamment du protocole réseau utilisé.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-105">Windows Sockets 2 (Winsock) enables programmers to create advanced Internet, intranet, and other network-capable applications to transmit application data across the wire, independent of the network protocol being used.</span></span> <span data-ttu-id="a7c1d-106">Avec Winsock, les programmeurs ont accès aux fonctionnalités avancées de mise en réseau de Microsoft® Windows® telles que la multidiffusion et la qualité de service (QoS).</span><span class="sxs-lookup"><span data-stu-id="a7c1d-106">With Winsock, programmers are provided access to advanced Microsoft® Windows® networking capabilities such as multicast and Quality of Service (QoS).</span></span>

<span data-ttu-id="a7c1d-107">Winsock suit le modèle WOSA (Windows Open System Architecture). Il définit une interface de fournisseur de services (SPI) standard entre l’interface de programmation d’applications (API), ses fonctions exportées et les piles de protocole.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-107">Winsock follows the Windows Open System Architecture (WOSA) model; it defines a standard service provider interface (SPI) between the application programming interface (API), with its exported functions and the protocol stacks.</span></span> <span data-ttu-id="a7c1d-108">Elle utilise le paradigme Sockets qui a été répandu pour la première fois par Berkeley Software Distribution (BSD) UNIX.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-108">It uses the sockets paradigm that was first popularized by Berkeley Software Distribution (BSD) UNIX.</span></span> <span data-ttu-id="a7c1d-109">Il a été ensuite adapté pour Windows dans Windows Sockets 1,1, avec lequel les applications Windows Sockets 2 sont à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-109">It was later adapted for Windows in Windows Sockets 1.1, with which Windows Sockets 2 applications are backward compatible.</span></span> <span data-ttu-id="a7c1d-110">Programmation Winsock précédemment centrée sur TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-110">Winsock programming previously centered around TCP/IP.</span></span> <span data-ttu-id="a7c1d-111">Certaines pratiques de programmation qui fonctionnaient avec TCP/IP ne fonctionnent pas avec tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-111">Some programming practices that worked with TCP/IP do not work with every protocol.</span></span> <span data-ttu-id="a7c1d-112">Par conséquent, l’API Windows Sockets 2 ajoute des fonctions quand cela est nécessaire pour gérer plusieurs protocoles.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-112">As a result, the Windows Sockets 2 API adds functions where necessary to handle several protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a7c1d-113">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="a7c1d-113">Developer audience</span></span>

<span data-ttu-id="a7c1d-114">Windows Sockets 2 est conçu pour être utilisé par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-114">Windows Sockets 2 is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="a7c1d-115">Vous devez être familiarisé avec la mise en réseau Windows.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-115">Familiarity with Windows networking is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a7c1d-116">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="a7c1d-116">Run-time requirements</span></span>

<span data-ttu-id="a7c1d-117">Windows Sockets 2 peut être utilisé sur toutes les plateformes Windows.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-117">Windows Sockets 2 can be used on all Windows platforms.</span></span> <span data-ttu-id="a7c1d-118">Lorsque certaines implémentations ou fonctionnalités des restrictions de plateforme Windows Sockets 2 existent, elles sont clairement notées dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-118">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a7c1d-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="a7c1d-119">In this section</span></span>



| <span data-ttu-id="a7c1d-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a7c1d-120">Topic</span></span>                                                                                             | <span data-ttu-id="a7c1d-121">Description</span><span class="sxs-lookup"><span data-stu-id="a7c1d-121">Description</span></span>                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7c1d-122">Nouveautés de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a7c1d-122">What's New for Windows Sockets</span></span>](what-s-new-for-windows-sockets-2.md)<br/>                 | <span data-ttu-id="a7c1d-123">Informations sur les nouvelles fonctionnalités de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-123">Information on new features for Windows Sockets.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a7c1d-124">Prise en charge du protocole réseau Winsock dans Windows</span><span class="sxs-lookup"><span data-stu-id="a7c1d-124">Winsock Network Protocol Support in Windows</span></span>](network-protocol-support-in-windows.md)<br/> | <span data-ttu-id="a7c1d-125">Informations sur la prise en charge du protocole réseau pour Windows Sockets sur différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-125">Information on network protocol support for Windows Sockets on different versions of Windows.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="a7c1d-126">À propos de Winsock</span><span class="sxs-lookup"><span data-stu-id="a7c1d-126">About Winsock</span></span>](about-winsock.md)<br/>                                                     | <span data-ttu-id="a7c1d-127">Informations générales sur les considérations relatives à la programmation de Windows Sockets, sur l’architecture et les fonctionnalités disponibles pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-127">General information on Windows Sockets programming considerations, architecture, and capabilities available to developers.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="a7c1d-128">Utilisation de Winsock</span><span class="sxs-lookup"><span data-stu-id="a7c1d-128">Using Winsock</span></span>](using-winsock.md)<br/>                                                     | <span data-ttu-id="a7c1d-129">Procédures et techniques de programmation utilisées avec Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-129">Procedures and programming techniques used with Windows Sockets.</span></span> <span data-ttu-id="a7c1d-130">Cette section comprend des techniques de programmation de base de Winsock, telles que [prise en main avec Winsock](getting-started-with-winsock.md), ainsi que des techniques avancées utiles aux développeurs Winsock expérimentés.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-130">This section includes basic Winsock programming techniques, such as [Getting Started With Winsock](getting-started-with-winsock.md), as well as advanced techniques useful for experienced Winsock developers.</span></span><br/> |
| [<span data-ttu-id="a7c1d-131">Informations de référence sur Winsock</span><span class="sxs-lookup"><span data-stu-id="a7c1d-131">Winsock Reference</span></span>](winsock-reference.md)<br/>                                             | <span data-ttu-id="a7c1d-132">Documentation de l’API Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a7c1d-132">Documentation of the Windows Sockets API.</span></span><br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="a7c1d-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7c1d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7c1d-134">Assistance IP</span><span class="sxs-lookup"><span data-stu-id="a7c1d-134">IP Helper</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="a7c1d-135">Qualité de service</span><span class="sxs-lookup"><span data-stu-id="a7c1d-135">Quality of Service</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
