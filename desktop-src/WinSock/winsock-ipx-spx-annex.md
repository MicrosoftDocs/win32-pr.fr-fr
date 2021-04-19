---
description: Cette section décrit les extensions Winsock spécifiques à l’échange de paquets par interréseau (IPX/SPX). Il décrit également les aspects des fonctions Winsock de base qui requièrent une attention particulière ou qui peuvent présenter un comportement unique.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Annexe IPX/SPX Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529714"
---
# <a name="winsock-ipxspx-annex"></a><span data-ttu-id="4cde8-104">Annexe IPX/SPX Winsock</span><span class="sxs-lookup"><span data-stu-id="4cde8-104">Winsock IPX/SPX Annex</span></span>

<span data-ttu-id="4cde8-105">Cette section décrit les extensions Winsock spécifiques à l’échange de paquets par interréseau (IPX/SPX).</span><span class="sxs-lookup"><span data-stu-id="4cde8-105">This section describes Winsock extensions specific to Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span></span> <span data-ttu-id="4cde8-106">Il décrit également les aspects des fonctions Winsock de base qui requièrent une attention particulière ou qui peuvent présenter un comportement unique.</span><span class="sxs-lookup"><span data-stu-id="4cde8-106">It also describes aspects of base Winsock functions that either require special consideration or may exhibit unique behavior.</span></span>



| <span data-ttu-id="4cde8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4cde8-107">Element</span></span>          | <span data-ttu-id="4cde8-108">Description</span><span class="sxs-lookup"><span data-stu-id="4cde8-108">Description</span></span>                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cde8-109">Nom (s) de protocole</span><span class="sxs-lookup"><span data-stu-id="4cde8-109">Protocol name(s)</span></span> | <span data-ttu-id="4cde8-110">IPX, SPX</span><span class="sxs-lookup"><span data-stu-id="4cde8-110">IPX, SPX</span></span>                                                                                                                                        |
| <span data-ttu-id="4cde8-111">Description</span><span class="sxs-lookup"><span data-stu-id="4cde8-111">Description</span></span>      | <span data-ttu-id="4cde8-112">Fournit des services de transport sur la couche de mise en réseau IPX : IPX pour les datagrammes non fiables, SPX pour les flux de messages fiables et orientés connexion.</span><span class="sxs-lookup"><span data-stu-id="4cde8-112">Provides transport services over the IPX networking layer: IPX for unreliable datagrams, SPX for reliable, connection-oriented message streams.</span></span> |
| <span data-ttu-id="4cde8-113">Famille d’adresses</span><span class="sxs-lookup"><span data-stu-id="4cde8-113">Address family</span></span>   | <span data-ttu-id="4cde8-114">\_protocole IPX AF</span><span class="sxs-lookup"><span data-stu-id="4cde8-114">AF\_IPX</span></span>                                                                                                                                         |
| <span data-ttu-id="4cde8-115">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4cde8-115">Header file</span></span>      | <span data-ttu-id="4cde8-116">Wsipx. h</span><span class="sxs-lookup"><span data-stu-id="4cde8-116">Wsipx.h</span></span>                                                                                                                                         |



 

<span data-ttu-id="4cde8-117">Cette section explique comment utiliser Winsock avec la famille de protocoles IPX, ce qui permet de porter les applications IPX traditionnelles vers Winsock.</span><span class="sxs-lookup"><span data-stu-id="4cde8-117">This section discusses how to use Winsock with the IPX family of protocols, enabling traditional IPX applications to be ported to Winsock.</span></span> <span data-ttu-id="4cde8-118">Comme les réseaux IPX fonctionnent de manière fondamentalement différente des réseaux IP, ces différences doivent être prises en compte lors de l’utilisation du protocole IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="4cde8-118">IPX networks operate in a fundamentally different manner than IP networks, so such differences must be considered when using IPX/SPX.</span></span>

 

 



