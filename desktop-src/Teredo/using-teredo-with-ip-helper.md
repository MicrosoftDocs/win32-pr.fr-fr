---
title: Utilisation de Teredo avec l’assistance IP
description: L’API d’assistance IP est utilisée par une application pour collecter et fournir des informations importantes sur la configuration réseau de l’ordinateur local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728477"
---
# <a name="using-teredo-with-ip-helper"></a><span data-ttu-id="0ef41-103">Utilisation de Teredo avec l’assistance IP</span><span class="sxs-lookup"><span data-stu-id="0ef41-103">Using Teredo with IP Helper</span></span>

<span data-ttu-id="0ef41-104">L' [API d’assistance IP](/windows/desktop/IpHlp/about-ip-helper) est utilisée par une application pour collecter et fournir des informations importantes sur la configuration réseau de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0ef41-104">The [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) API is utilized by an application to gather and provide important information regarding the networking configuration of the local machine.</span></span> <span data-ttu-id="0ef41-105">En cas de fonctionnement sur la plateforme Windows Vista, ces informations incluent le port UDP dynamique affecté à l’interface Teredo et les modifications qui peuvent se produire sur le port désigné.</span><span class="sxs-lookup"><span data-stu-id="0ef41-105">When operating on the Windows Vista platform, this information includes the dynamic UDP port assigned to the Teredo interface and changes that may occur to the designated port.</span></span>

<span data-ttu-id="0ef41-106">Les fonctions suivantes sont utilisées par l’API d’assistance IP pour faciliter l’utilisation de l’interface Teredo :</span><span class="sxs-lookup"><span data-stu-id="0ef41-106">The following functions are utilized by the IP Helper API to facilitate the use of the Teredo interface:</span></span>

-   [<span data-ttu-id="0ef41-107">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="0ef41-107">**GetTeredoPort**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="0ef41-108">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="0ef41-108">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="0ef41-109">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="0ef41-109">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 