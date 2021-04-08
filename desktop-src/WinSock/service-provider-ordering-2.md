---
description: L’ordre dans lequel les fournisseurs de services de transport sont installés initialement régit l’ordre dans lequel ils sont énumérés via WSCEnumProtocols et WSCEnumProtocols32 au niveau de l’interface du fournisseur de services, ou via WSAEnumProtocols au niveau de l’interface de l’application. Plus important encore, cet ordre régit également l’ordre dans lequel les protocoles et les fournisseurs de services sont pris en compte lorsqu’un client demande la création d’un socket en fonction de sa famille d’adresses, de son type et de son identificateur de protocole.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Classement des fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863810"
---
# <a name="service-provider-ordering"></a><span data-ttu-id="1a6a6-104">Classement des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1a6a6-104">Service Provider Ordering</span></span>

<span data-ttu-id="1a6a6-105">L’ordre dans lequel les fournisseurs de services de transport sont installés initialement régit l’ordre dans lequel ils sont énumérés via [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) et [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) au niveau de l’interface du fournisseur de services, ou via [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) au niveau de l’interface de l’application.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-105">The order in which transport service providers are initially installed governs the order in which they are enumerated through [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) and [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) at the service provider interface, or through [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) at the application interface.</span></span> <span data-ttu-id="1a6a6-106">Plus important encore, cet ordre régit également l’ordre dans lequel les protocoles et les fournisseurs de services sont pris en compte lorsqu’un client demande la création d’un socket en fonction de sa famille d’adresses, de son type et de son identificateur de protocole.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-106">More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.</span></span>

<span data-ttu-id="1a6a6-107">Windows Sockets 2 comprend une applet appelée Sporder.exe qui permet de réorganiser de manière interactive le catalogue des protocoles installés une fois que les protocoles ont déjà été installés.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-107">Windows Sockets 2 includes an applet called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed.</span></span> <span data-ttu-id="1a6a6-108">Winsock comprend également une DLL auxiliaire, Sporder.dll, qui exporte une interface procédurale pour la réorganisation des protocoles.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-108">Winsock also includes an auxiliary DLL, Sporder.dll, that exports a procedural interface for reordering protocols.</span></span> <span data-ttu-id="1a6a6-109">Cette interface procédurale se compose d’une procédure unique appelée [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span><span class="sxs-lookup"><span data-stu-id="1a6a6-109">This procedural interface consists of a single procedure called [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span></span>

<span data-ttu-id="1a6a6-110">La définition d’interface peut être importée dans un programme C ou C++ au moyen du fichier include WebOrder. h.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-110">The interface definition may be imported into a C or C++ program by means of the include file Sporder.h.</span></span> <span data-ttu-id="1a6a6-111">Le point d’entrée peut être lié par le biais du fichier lib WebOrder. lib.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-111">The entry point may be linked by means of the lib file Sporder.lib.</span></span>

 

 



