---
title: Rôle du gestionnaire de listes de réseaux
description: Rôle du gestionnaire de listes de réseaux
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840825"
---
# <a name="the-role-of-network-list-manager"></a><span data-ttu-id="085a7-103">Rôle du gestionnaire de listes de réseaux</span><span class="sxs-lookup"><span data-stu-id="085a7-103">The Role of Network List Manager</span></span>

<span data-ttu-id="085a7-104">Avant Windows XP et Windows Server 2003, les applications devaient appeler un certain nombre d’API non liées pour obtenir des données sur les attributs réseau tels que l’adresse IP, le contrôleur de domaine ou le système DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="085a7-104">Prior to Windows XP and Windows Server 2003, applications were required to call a number of unrelated APIs to obtain data about network attributes such as the IP address, the domain controller, or the Domain Name System (DNS).</span></span> <span data-ttu-id="085a7-105">À compter de Windows XP et de Windows Server 2003, l’API Winsock de sensibilisation à l’emplacement réseau offre un ensemble limité de fonctionnalités d’emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="085a7-105">Starting with Windows XP and Windows Server 2003, the Network Location Awareness Winsock API featured a limited set of network location functionality.</span></span> <span data-ttu-id="085a7-106">Dans Windows Server 2008 et Windows Vista, le service de reconnaissance réseau capture les attributs réseau dans un emplacement unique et permet aux applications d’interroger et de récupérer des réseaux et des attributs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="085a7-106">In Windows Server 2008 and Windows Vista, the Network Awareness service captures the network attributes in one location and allows applications to query and retrieve specific networks and attributes.</span></span> <span data-ttu-id="085a7-107">Le gestionnaire de listes de réseaux remplace les fonctionnalités de l’API Winsock précédente (disponible en tant que fournisseur d’espace de noms Winsock) tout en conservant la compatibilité avec les anciennes applications à l’aide de l’API Winsock.</span><span class="sxs-lookup"><span data-stu-id="085a7-107">Network List Manager replaces the functionality of the previous Winsock API (available as a Winsock Name Space Provider) while maintaining compatibility with older applications using the Winsock API.</span></span>

 

 




