---
description: Cette section décrit les fonctions, les structures de données et les contrôles de protocole TCP/IP (Transmission Control Protocol/Internet Protocol).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock TCP/IP annexe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201823"
---
# <a name="winsock-tcpip-annex"></a><span data-ttu-id="26121-103">Winsock TCP/IP annexe</span><span class="sxs-lookup"><span data-stu-id="26121-103">Winsock TCP/IP Annex</span></span>

<span data-ttu-id="26121-104">Cette section décrit les fonctions, les structures de données et les contrôles de protocole TCP/IP (Transmission Control Protocol/Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="26121-104">This section describes Transmission Control Protocol/Internet Protocol (TCP/IP) functions, data structures, and controls.</span></span>



| <span data-ttu-id="26121-105">Élément</span><span class="sxs-lookup"><span data-stu-id="26121-105">Element</span></span>          | <span data-ttu-id="26121-106">Description</span><span class="sxs-lookup"><span data-stu-id="26121-106">Description</span></span>                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26121-107">Nom (s) de protocole</span><span class="sxs-lookup"><span data-stu-id="26121-107">Protocol name(s)</span></span> | <span data-ttu-id="26121-108">TCP, UDP</span><span class="sxs-lookup"><span data-stu-id="26121-108">TCP, UDP</span></span>                                                                                                                                    |
| <span data-ttu-id="26121-109">Description</span><span class="sxs-lookup"><span data-stu-id="26121-109">Description</span></span>      | <span data-ttu-id="26121-110">Fournit des services de transport sur la couche de mise en réseau IP : UDP pour les datagrammes non fiables, TCP pour les flux d’octets orientés connexion fiables.</span><span class="sxs-lookup"><span data-stu-id="26121-110">Provides transport services over the IP networking layer: UDP for unreliable datagrams, TCP for reliable, connection-oriented byte streams.</span></span> |
| <span data-ttu-id="26121-111">Famille d’adresses</span><span class="sxs-lookup"><span data-stu-id="26121-111">Address family</span></span>   | <span data-ttu-id="26121-112">**AF \_ INET**, **AF \_ inet6**</span><span class="sxs-lookup"><span data-stu-id="26121-112">**AF\_INET**, **AF\_INET6**</span></span>                                                                                                                 |
| <span data-ttu-id="26121-113">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="26121-113">Header file</span></span>      | <span data-ttu-id="26121-114">*Ws2tcpip. h*</span><span class="sxs-lookup"><span data-stu-id="26121-114">*Ws2tcpip.h*</span></span>                                                                                                                                |



 

<span data-ttu-id="26121-115">Deux types de services de transport de base sont proposés : les datagrammes non fiables (UDP) et les flux d’octets (TCP) fiables basés sur les connexions.</span><span class="sxs-lookup"><span data-stu-id="26121-115">Two basic types of transport services are offered: unreliable datagrams (UDP), and reliable connection oriented–byte streams (TCP).</span></span> <span data-ttu-id="26121-116">En outre, un socket brut est éventuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26121-116">In addition, a raw socket is optionally supported.</span></span> <span data-ttu-id="26121-117">Les sockets bruts permettent à une application de communiquer via des protocoles autres que TCP et UDP tels que ICMP.</span><span class="sxs-lookup"><span data-stu-id="26121-117">Raw sockets allow an application to communicate through protocols other than TCP and UDP such as ICMP.</span></span> <span data-ttu-id="26121-118">Les sockets bruts sont pris en charge sur les familles d’adresses **AF \_ inet** et **AF \_ inet6** avec certaines limitations.</span><span class="sxs-lookup"><span data-stu-id="26121-118">Raw sockets are supported on the **AF\_INET** and **AF\_INET6** address families with some limitations.</span></span>

<span data-ttu-id="26121-119">Cette section décrit les extensions de Winsock qui sont spécifiques aux protocoles TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="26121-119">This section covers extensions to Winsock that are specific to TCP/IP protocols.</span></span> <span data-ttu-id="26121-120">Il décrit également les aspects des fonctions Winsock de base qui requièrent une attention particulière ou qui peuvent présenter un comportement unique lors de l’utilisation de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="26121-120">It also describes aspects of base Winsock functions that require special consideration or that may exhibit unique behavior when using TCP/IP.</span></span>

 

 



