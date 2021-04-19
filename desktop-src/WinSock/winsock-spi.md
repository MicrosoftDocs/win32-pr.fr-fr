---
description: L’interface du fournisseur de services (SPI) de Windows Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517895"
---
# <a name="winsock-spi"></a><span data-ttu-id="b96d1-103">SPI Winsock</span><span class="sxs-lookup"><span data-stu-id="b96d1-103">Winsock SPI</span></span>

<span data-ttu-id="b96d1-104">L’interface du fournisseur de services Winsock, ou Winsock SPI, est une discipline spécifique de Winsock utilisée pour créer des fournisseurs. les fournisseurs de transport tels que les piles de protocoles TCP/IP ou IPX/SPX utilisent le SPI Winsock, de même que les fournisseurs d’espaces de noms tels que le système de noms de domaine (DNS) d’Internet.</span><span class="sxs-lookup"><span data-stu-id="b96d1-104">The Winsock Service Provider Interface, or Winsock SPI, is a specialized discipline of Winsock used to create providers; transport providers such as TCP/IP or IPX/SPX protocol stacks use the Winsock SPI, as do namespace providers such as the Internet's Domain Naming System (DNS).</span></span>

<span data-ttu-id="b96d1-105">La programmation réseau traditionnelle, telle que l’activation des applications pour communiquer sur le réseau, ne nécessite pas l’utilisation d’interfaces Winsock SPI. Utilisez à la place des interfaces [Winsock](winsock-reference.md) standard.</span><span class="sxs-lookup"><span data-stu-id="b96d1-105">Traditional network programming, such as enabling applications to communicate over the network, does not require use of Winsock SPI interfaces; use standard [Winsock](winsock-reference.md) interfaces instead.</span></span>

 

<span data-ttu-id="b96d1-106">Le SPI Winsock utilise la Convention d’affectation de noms de préfixe de fonction suivante.</span><span class="sxs-lookup"><span data-stu-id="b96d1-106">The Winsock SPI uses the following function prefix naming convention.</span></span>



| <span data-ttu-id="b96d1-107">Préfixe</span><span class="sxs-lookup"><span data-stu-id="b96d1-107">Prefix</span></span> | <span data-ttu-id="b96d1-108">Signification</span><span class="sxs-lookup"><span data-stu-id="b96d1-108">Meaning</span></span>                          | <span data-ttu-id="b96d1-109">Description</span><span class="sxs-lookup"><span data-stu-id="b96d1-109">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="b96d1-110">WSP</span><span class="sxs-lookup"><span data-stu-id="b96d1-110">WSP</span></span>    | <span data-ttu-id="b96d1-111">Fournisseur de services Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b96d1-111">Windows Sockets Service Provider</span></span> | <span data-ttu-id="b96d1-112">Points d’entrée du fournisseur de services de transport</span><span class="sxs-lookup"><span data-stu-id="b96d1-112">Transport service provider entry points</span></span>           |
| <span data-ttu-id="b96d1-113">WPU</span><span class="sxs-lookup"><span data-stu-id="b96d1-113">WPU</span></span>    | <span data-ttu-id="b96d1-114">Appel du fournisseur de sockets Windows</span><span class="sxs-lookup"><span data-stu-id="b96d1-114">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="b96d1-115">Ws2 \_32.dll points d’entrée pour les fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b96d1-115">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="b96d1-116">WSC</span><span class="sxs-lookup"><span data-stu-id="b96d1-116">WSC</span></span>    | <span data-ttu-id="b96d1-117">Configuration de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b96d1-117">Windows Sockets Configuration</span></span>    | <span data-ttu-id="b96d1-118">WS2 \_32.dll points d’entrée pour les applets d’installation</span><span class="sxs-lookup"><span data-stu-id="b96d1-118">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="b96d1-119">LECTEURS</span><span class="sxs-lookup"><span data-stu-id="b96d1-119">NSP</span></span>    | <span data-ttu-id="b96d1-120">Fournisseur d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="b96d1-120">Namespace Provider</span></span>               | <span data-ttu-id="b96d1-121">Points d’entrée du fournisseur d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="b96d1-121">Namespace provider entry points</span></span>                   |



 

 

 



