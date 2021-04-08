---
description: Options SSPI pour les applications distribuées
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Options SSPI pour les applications distribuées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861882"
---
# <a name="sspi-options-for-distributed-applications"></a><span data-ttu-id="9f3f8-103">Options SSPI pour les applications distribuées</span><span class="sxs-lookup"><span data-stu-id="9f3f8-103">SSPI Options for Distributed Applications</span></span>

<span data-ttu-id="9f3f8-104">Les développeurs disposent de nombreuses options pour créer des applications distribuées.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-104">Developers have many options for building distributed applications.</span></span> <span data-ttu-id="9f3f8-105">SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) fournit une couche d’abstraction entre les protocoles de niveau application et les [*protocoles de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9f3f8-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) provides an abstraction layer between application-level protocols and [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="9f3f8-106">Les applications peuvent tirer parti des protocoles de sécurité SSPI de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="9f3f8-106">Applications can take advantage of the SSPI security protocols in several ways:</span></span>

-   <span data-ttu-id="9f3f8-107">Appelez les routines SSPI directement (pour les applications traditionnelles basées sur les Sockets).</span><span class="sxs-lookup"><span data-stu-id="9f3f8-107">Call SSPI routines directly (for traditional, socket-based applications).</span></span>

    <span data-ttu-id="9f3f8-108">Les routines utilisent des messages de demande/réponse pour implémenter le [*protocole d’application*](../secgloss/a-gly.md) qui transmet les données liées à la sécurité SSPI.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-108">The routines use request/response messages to implement the [*application protocol*](../secgloss/a-gly.md) that carries SSPI security-related data.</span></span>

-   <span data-ttu-id="9f3f8-109">Utilisez COM pour appeler des options de sécurité implémentées à l’aide de RPC authentifié et de SSPI à des niveaux inférieurs.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-109">Use COM to call security options that are implemented by using authenticated RPC and SSPI at lower levels.</span></span>

    <span data-ttu-id="9f3f8-110">Ces applications n’appellent pas directement les fonctions SSPI.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-110">These applications do not call SSPI functions directly.</span></span>

-   <span data-ttu-id="9f3f8-111">Utilisez [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) avec l’interface Winsock étendue pour permettre aux fournisseurs de transport d’utiliser les fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) with the extended WinSock interface to allow transport providers to use security features.</span></span>

    <span data-ttu-id="9f3f8-112">Cette approche intègre le fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) dans la pile réseau et fournit des services de sécurité et de transport par le biais d’une interface commune.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-112">This approach integrates the [*security support provider*](../secgloss/s-gly.md) (SSP) into the network stack and provides both security and transport services through a common interface.</span></span>

-   <span data-ttu-id="9f3f8-113">Utilisez l' [API Windows Internet extensions](../wininet/portal.md) (WinInet) et une interface conçue pour prendre en charge les protocoles de sécurité Internet, tels que le protocole [*SSL (Secure Sockets Layer)*](../secgloss/s-gly.md) (SSL).</span><span class="sxs-lookup"><span data-stu-id="9f3f8-113">Use the [Windows Internet Extensions API](../wininet/portal.md) (WinInet) and an interface designed to support Internet security protocols such as the [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) protocol.</span></span>

    <span data-ttu-id="9f3f8-114">Les applications utilisent l’interface SSPI sur le fournisseur de sécurité de [canal sécurisé](secure-channel.md) (SChannel) pour implémenter la sécurité wininet.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-114">Applications use the SSPI interface to the [Secure Channel](secure-channel.md) (Schannel) security provider to implement WinInet security.</span></span> <span data-ttu-id="9f3f8-115">Schannel est l’implémentation Microsoft de SSL.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-115">Schannel is the Microsoft implementation of SSL.</span></span>

<span data-ttu-id="9f3f8-116">Plusieurs fonctions SSPI renvoient des horodatages qui représentent l’étendue de la durée de vie de divers objets.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-116">Several SSPI functions return time stamps that represent the life span of various objects.</span></span> <span data-ttu-id="9f3f8-117">Les [*packages de sécurité*](../secgloss/s-gly.md) peuvent conserver du temps et fournir des horodatages de différentes façons, mais l’utilisation de l’heure locale simplifie le travail des applications qui utilisent des fonctions SSPI.</span><span class="sxs-lookup"><span data-stu-id="9f3f8-117">[*Security packages*](../secgloss/s-gly.md) can maintain time and provide time stamps in different ways, but using local time simplifies the work of applications that use SSPI functions.</span></span>

 

 
