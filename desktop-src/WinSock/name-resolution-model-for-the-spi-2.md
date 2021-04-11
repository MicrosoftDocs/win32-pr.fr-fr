---
description: Résolution de noms et modèle d’inscription pour l’IPP de Windows Sockets (Winsock).
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modèle de résolution de noms pour le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113034"
---
# <a name="name-resolution-model-for-the-spi"></a><span data-ttu-id="930ba-103">Modèle de résolution de noms pour le SPI</span><span class="sxs-lookup"><span data-stu-id="930ba-103">Name Resolution Model for the SPI</span></span>

<span data-ttu-id="930ba-104">Lors du développement d’une application client/serveur indépendante du protocole, deux exigences de base existent en ce qui concerne la résolution de noms et l’inscription :</span><span class="sxs-lookup"><span data-stu-id="930ba-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="930ba-105">La capacité du serveur à la moitié de l’application (ci-après le terme de service) d’inscrire son existence dans (ou de devenir accessible à) un ou plusieurs espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="930ba-105">The ability of the server half of the application (hereafter referred to as a service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="930ba-106">Capacité de l’application cliente à rechercher le service dans un espace de noms et à obtenir le protocole de transport et les informations d’adressage requis.</span><span class="sxs-lookup"><span data-stu-id="930ba-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="930ba-107">Pour ceux habitués au développement d’applications basées sur TCP/IP, cela peut impliquer un peu plus que la recherche d’une adresse d’hôte, puis l’utilisation d’un numéro de port convenu.</span><span class="sxs-lookup"><span data-stu-id="930ba-107">For those accustomed to developing TCP/IP-based applications, this may involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="930ba-108">Toutefois, d’autres schémas de mise en réseau autorisent l’emplacement du service, le protocole utilisé pour le service et d’autres attributs à découvrir au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="930ba-108">Other networking schemes, however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run-time.</span></span> <span data-ttu-id="930ba-109">Pour prendre en charge l’ensemble des fonctionnalités disponibles dans les services de noms existants, l’interface Windows Sockets 2 adopte le modèle décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="930ba-109">To accommodate the range of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described below.</span></span>

<span data-ttu-id="930ba-110">Un *espace de noms* fait référence à une capacité à associer (au minimum) les attributs de protocole et d’adressage d’un service réseau avec un ou plusieurs noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="930ba-110">A *namespace* refers to some capability to associate (as a minimum) the protocol and addressing attributes of a network service with one or more human-friendly names.</span></span> <span data-ttu-id="930ba-111">De nombreux espaces de noms sont actuellement utilisés en grande partie, y compris le système DNS (Domain Name System), le Services d’annuaire NetWare (NDS) (NDS), le système de noms de domaine (NDS) d’Internet, etc. Ces espaces de noms varient considérablement dans la façon dont ils sont organisés et implémentés.</span><span class="sxs-lookup"><span data-stu-id="930ba-111">Many namespaces are currently in wide use including the Internet's Domain Name System (DNS), NetWare Directory Services (NDS), X.500, etc. These namespaces vary widely in how they are organized and implemented.</span></span> <span data-ttu-id="930ba-112">Certaines de leurs propriétés sont particulièrement importantes pour comprendre le point de vue de la résolution de noms Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="930ba-112">Some of their properties are particularly important to understand from the perspective of Windows Sockets name resolution.</span></span>

 

 



