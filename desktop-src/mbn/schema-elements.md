---
description: Un profil mobile large bande v1 se compose des éléments suivants.
ms.assetid: 234dd206-7306-4598-bfbb-b0cd9d726ace
title: Éléments v1 du schéma de profil haut débit mobile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4b92e9b1fd9daf3cf843e769a0782f5f1ce1848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517531"
---
# <a name="mobile-broadband-profile-schema-v1-elements"></a><span data-ttu-id="6d55f-103">Éléments v1 du schéma de profil haut débit mobile</span><span class="sxs-lookup"><span data-stu-id="6d55f-103">Mobile Broadband Profile Schema v1 Elements</span></span>

<span data-ttu-id="6d55f-104">Un profil mobile large bande v1 se compose des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="6d55f-104">A Mobile Broadband v1 Profile is comprised of the following elements.</span></span> <span data-ttu-id="6d55f-105">Tous les éléments nommés se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WWAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="6d55f-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1`.</span></span>

-   [<span data-ttu-id="6d55f-106">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="6d55f-106">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-107">**AutoConnectOnInternet (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-107">**AutoConnectOnInternet (MBNProfile)**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-108">**ConnectionMode (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-108">**ConnectionMode (MBNProfile)**</span></span>](schema-connectionmode-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-109">**Contexte (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-109">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
        -   [<span data-ttu-id="6d55f-110">**AccessString (contextType)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-110">**AccessString (contextType)**</span></span>](schema-accessstring-contexttype-element.md)
        -   [<span data-ttu-id="6d55f-111">**AuthProtocol (contextType)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-111">**AuthProtocol (contextType)**</span></span>](schema-authprotocol-contexttype-element.md)
        -   [<span data-ttu-id="6d55f-112">**Compression (contextType)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-112">**Compression (contextType)**</span></span>](schema-compression-contexttype-element.md)
        -   [<span data-ttu-id="6d55f-113">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-113">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
            -   [<span data-ttu-id="6d55f-114">**IgnorePassword (UserLogonCred)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-114">**IgnorePassword (UserLogonCred)**</span></span>](schema-ignorepassword-userlogoncred-element.md)
            -   [<span data-ttu-id="6d55f-115">**Mot de passe (UserLogonCred)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-115">**Password (UserLogonCred)**</span></span>](schema-password-userlogoncred-element.md)
            -   [<span data-ttu-id="6d55f-116">**Nom d’utilisateur (UserLogonCred)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-116">**UserName (UserLogonCred)**</span></span>](schema-username-userlogoncred-element.md)
    -   [<span data-ttu-id="6d55f-117">**DataRoamingPartners (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-117">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
        -   [<span data-ttu-id="6d55f-118">**Fournisseur (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-118">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
            -   [<span data-ttu-id="6d55f-119">**ProviderID (providerType)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-119">**ProviderID (providerType)**</span></span>](schema-providerid-providertype-element.md)
            -   [<span data-ttu-id="6d55f-120">**ProviderName (providerType)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-120">**ProviderName (providerType)**</span></span>](schema-providername-providertype-element.md)
    -   [<span data-ttu-id="6d55f-121">**Description (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-121">**Description (MBNProfile)**</span></span>](schema-description-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-122">**HomeProviderName (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-122">**HomeProviderName (MBNProfile)**</span></span>](schema-homeprovidername-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-123">**ICONFilePath (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-123">**ICONFilePath (MBNProfile)**</span></span>](schema-iconfilepath-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-124">**IsDefault (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-124">**IsDefault (MBNProfile)**</span></span>](schema-isdefault-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-125">**Nom (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-125">**Name (MBNProfile)**</span></span>](schema-name-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-126">**ProfileCreationType (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-126">**ProfileCreationType (MBNProfile)**</span></span>](schema-profilecreationtype-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-127">**SimIccID (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-127">**SimIccID (MBNProfile)**</span></span>](schema-simiccid-mbnprofile-element.md)
    -   [<span data-ttu-id="6d55f-128">**Abonné (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6d55f-128">**SubscriberID (MBNProfile)**</span></span>](schema-subscriberid-mbnprofile-element.md)

 

 



