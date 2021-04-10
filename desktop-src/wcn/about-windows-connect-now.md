---
title: À propos de Windows Connect Now
description: Windows Connect Now (WCN) fournit un mécanisme simple et sécurisé pour les points d’accès réseau et les appareils (tels que les imprimantes, les appareils photo et les PC) pour se connecter et échanger des paramètres.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102185"
---
# <a name="about-windows-connect-now"></a><span data-ttu-id="9026e-103">À propos de Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="9026e-103">About Windows Connect Now</span></span>

<span data-ttu-id="9026e-104">Windows Connect Now (WCN) fournit un mécanisme simple et sécurisé pour les points d’accès réseau et les appareils (tels que les imprimantes, les appareils photo et les PC) pour se connecter et échanger des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9026e-104">Windows Connect Now (WCN) provides a simple and secure mechanism for network access points and devices (like printers, camera, and PCs) to connect and exchange settings.</span></span> <span data-ttu-id="9026e-105">Cette API est l’implémentation Microsoft du protocole Wi-Fi Protected Setup (WPS)/Wi-Fi simple configuration (WSC), qui a été créé par l’Alliance Wi-Fi en tant que solution pour la mise en réseau à distance et les petites entreprises.</span><span class="sxs-lookup"><span data-stu-id="9026e-105">This API is the Microsoft implementation of the Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC) protocol, which was created by the Wi-Fi Alliance as a solution for home networking and small businesses.</span></span> <span data-ttu-id="9026e-106">Cette technologie n’est pas destinée aux scénarios d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9026e-106">This technology is not intended for enterprise scenarios.</span></span>

> [!Note]  
> <span data-ttu-id="9026e-107">Le nom de la spécification a été modifié entre la version 1.0 h et la version 2.</span><span class="sxs-lookup"><span data-stu-id="9026e-107">The specification name changed between version 1.0h and version 2.</span></span> <span data-ttu-id="9026e-108">La spécification de la version 1.0 a était nommée Wi-Fi Protected Setup (WPS).</span><span class="sxs-lookup"><span data-stu-id="9026e-108">The version 1.0h specification was named Wi-Fi Protected Setup (WPS).</span></span> <span data-ttu-id="9026e-109">À partir de la spécification de la version 2, la spécification est nommée Wi-Fi configuration simple (WSC).</span><span class="sxs-lookup"><span data-stu-id="9026e-109">Starting with version 2 specification, the specification is named Wi-Fi Simple Configuration (WSC).</span></span> <span data-ttu-id="9026e-110">Dans notre documentation, les termes WPS et WSC sont utilisés indifféremment, sauf mention contraire.</span><span class="sxs-lookup"><span data-stu-id="9026e-110">In our documentation, the terms WPS and WSC are used interchangeably unless noted.</span></span>

 

<span data-ttu-id="9026e-111">Windows Connect permet désormais aux applications de rechercher des appareils qui gèrent WCN à l’aide de l' [API de détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal).</span><span class="sxs-lookup"><span data-stu-id="9026e-111">Windows Connect Now enables applications to search for WCN-capable devices using the [Function Discovery API](/previous-versions/windows/desktop/fundisc/fd-portal).</span></span> <span data-ttu-id="9026e-112">L’étendue d’une recherche peut être limitée à un SSID, un État, une catégorie ou même élargi pour inclure tous les appareils avec la compatibilité WCN.</span><span class="sxs-lookup"><span data-stu-id="9026e-112">The scope of a search can be narrowed down to a specific SSID, state, category, or even broadened to include all WCN-capable devices.</span></span> <span data-ttu-id="9026e-113">Une fois que les appareils sont localisés, l’API WCN autorise la communication avec l’appareil qui prend en charge WCN afin de faciliter la configuration ou la connectivité.</span><span class="sxs-lookup"><span data-stu-id="9026e-113">Once devices are located, the WCN API allows communication with the WCN-capable device in order to facilitate configuration or connectivity.</span></span>

 

 