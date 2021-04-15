---
description: Un profil de stratégie de réseau local sans fil Wi-Fi (WLAN) natif se compose des éléments de schéma suivants.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Éléments de schéma WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525762"
---
# <a name="wlan_policy-schema-elements"></a><span data-ttu-id="fe809-103">\_Éléments du schéma de stratégie WLAN</span><span class="sxs-lookup"><span data-stu-id="fe809-103">WLAN\_policy Schema Elements</span></span>

<span data-ttu-id="fe809-104">Un profil de stratégie de réseau local sans fil Wi-Fi (WLAN) natif se compose des éléments de schéma suivants.</span><span class="sxs-lookup"><span data-stu-id="fe809-104">A Native Wifi wireless LAN (WLAN) policy profile is composed of the following schema elements.</span></span> <span data-ttu-id="fe809-105">Tous les éléments nommés se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="fe809-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

<span data-ttu-id="fe809-106">La liste suivante présente les éléments définis dans l’ordre dans lequel les éléments apparaissent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="fe809-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="fe809-107">L’ordre des éléments est appliqué.</span><span class="sxs-lookup"><span data-stu-id="fe809-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="fe809-108">Tous les éléments ne se trouvent pas dans chaque profil, car certains éléments sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="fe809-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="fe809-109">Cette liste n’affiche pas tous les éléments possibles qui peuvent apparaître dans un profil, car des éléments peuvent être ajoutés dans **XS : n’importe quel** point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="fe809-109">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="fe809-110">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="fe809-110">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
    -   [<span data-ttu-id="fe809-111">**nom (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="fe809-111">**name (WLANPolicy)**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)
    -   [<span data-ttu-id="fe809-112">**Description (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="fe809-112">**description (WLANPolicy)**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)
    -   [<span data-ttu-id="fe809-113">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="fe809-113">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [<span data-ttu-id="fe809-114">**enableAutoConfig (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="fe809-114">**enableAutoConfig (globalFlags)**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [<span data-ttu-id="fe809-115">**showDeniedNetwork (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="fe809-115">**showDeniedNetwork (globalFlags)**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [<span data-ttu-id="fe809-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="fe809-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [<span data-ttu-id="fe809-117">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="fe809-117">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [<span data-ttu-id="fe809-118">**allowList (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="fe809-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [<span data-ttu-id="fe809-119">**réseau (allowList)**</span><span class="sxs-lookup"><span data-stu-id="fe809-119">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
                -   [<span data-ttu-id="fe809-120">**networkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="fe809-120">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="fe809-121">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="fe809-121">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="fe809-122">**Blocage (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="fe809-122">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [<span data-ttu-id="fe809-123">**réseau (de blocage)**</span><span class="sxs-lookup"><span data-stu-id="fe809-123">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
                -   [<span data-ttu-id="fe809-124">**networkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="fe809-124">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="fe809-125">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="fe809-125">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="fe809-126">**denyAllIBSS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="fe809-126">**denyAllIBSS (networkFilter)**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [<span data-ttu-id="fe809-127">**denyAllESS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="fe809-127">**denyAllESS (networkFilter)**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [<span data-ttu-id="fe809-128">**profileList (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="fe809-128">**profileList (WLANPolicy)**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



