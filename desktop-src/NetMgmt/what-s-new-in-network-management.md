---
title: Nouveautés de la gestion de réseau
description: Nouveautés de la gestion de réseau
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383232"
---
# <a name="whats-new-in-network-management"></a><span data-ttu-id="32265-103">Nouveautés de la gestion de réseau</span><span class="sxs-lookup"><span data-stu-id="32265-103">What's New in Network Management</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="32265-104">Windows 8 et Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32265-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="32265-105">Microsoft Windows 8 introduit de nouvelles fonctionnalités de programmation de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="32265-105">Microsoft Windows 8 introduces new Network Management programming features.</span></span> <span data-ttu-id="32265-106">Ces nouveaux éléments étendent la capacité de gestion de réseau à créer des packages d’approvisionnement pour les opérations de jonction de domaine hors connexion lors de la configuration d’ordinateurs avec Windows 8.</span><span class="sxs-lookup"><span data-stu-id="32265-106">These new elements extend the capability of Network Management to create provisioning packages for offline domain join operations when provisioning computers with Windows 8.</span></span>

<span data-ttu-id="32265-107">Les nouvelles fonctions de gestion de réseau sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32265-107">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="32265-108">**NetCreateProvisioningPackage**</span><span class="sxs-lookup"><span data-stu-id="32265-108">**NetCreateProvisioningPackage**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="32265-109">**NetRequestProvisioningPackageInstall**</span><span class="sxs-lookup"><span data-stu-id="32265-109">**NetRequestProvisioningPackageInstall**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

<span data-ttu-id="32265-110">Voici les nouvelles structures de gestion de réseau :</span><span class="sxs-lookup"><span data-stu-id="32265-110">The following are new Network Management structures:</span></span>

-   [<span data-ttu-id="32265-111">**paramètres d' \_ approvisionnement netsetup \_**</span><span class="sxs-lookup"><span data-stu-id="32265-111">**NETSETUP\_PROVISIONING\_PARAMS**</span></span>](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [<span data-ttu-id="32265-112">**\_Informations utilisateur \_ 24**</span><span class="sxs-lookup"><span data-stu-id="32265-112">**USER\_INFO\_24**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

<span data-ttu-id="32265-113">La fonction [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) a été améliorée sur Windows 8 pour prendre en charge un nouveau niveau d’informations et retourner une structure informations [**utilisateur \_ \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) avec les informations de compte d’utilisateur pour un compte connecté à une identité Internet.</span><span class="sxs-lookup"><span data-stu-id="32265-113">The [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function has been enhanced on Windows 8 to support a new information level and return a [**USER\_INFO\_24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) structure with user account information for an account connected to an Internet identity.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="32265-114">Windows 7 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32265-114">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="32265-115">Microsoft Windows 7 introduit de nouvelles fonctionnalités de programmation de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="32265-115">Microsoft Windows 7 introduces new Network Management programming features.</span></span> <span data-ttu-id="32265-116">Ces éléments étendent la capacité de gestion de réseau à autoriser les opérations de jonction de domaine hors connexion lors de la configuration d’ordinateurs avec Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32265-116">These elements extend the capability of Network Management to allow offline domain join operations when provisioning computers with Windows 7.</span></span>

<span data-ttu-id="32265-117">Les nouvelles fonctions de gestion de réseau sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32265-117">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="32265-118">**NetProvisionComputerAccount**</span><span class="sxs-lookup"><span data-stu-id="32265-118">**NetProvisionComputerAccount**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="32265-119">**NetRequestOfflineDomainJoin**</span><span class="sxs-lookup"><span data-stu-id="32265-119">**NetRequestOfflineDomainJoin**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

<span data-ttu-id="32265-120">Les fonctions de gestion de réseau existantes suivantes ont été améliorées pour prendre en charge des options supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="32265-120">The following existing Network Management functions were enhanced to support additional options:</span></span>

-   [<span data-ttu-id="32265-121">**NetJoinDomain**</span><span class="sxs-lookup"><span data-stu-id="32265-121">**NetJoinDomain**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a><span data-ttu-id="32265-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32265-122">Windows Server 2003</span></span>

<span data-ttu-id="32265-123">Microsoft Windows Server 2003 introduit de nouvelles fonctionnalités de programmation de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="32265-123">Microsoft Windows Server 2003 introduces new Network Management programming features.</span></span> <span data-ttu-id="32265-124">Ces éléments étendent la capacité des opérations de gestion de réseau sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="32265-124">These elements extend the capability of Network Management operations on Windows Server 2003 and later.</span></span>

## <a name="windows-xp"></a><span data-ttu-id="32265-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="32265-125">Windows XP</span></span>

<span data-ttu-id="32265-126">Microsoft Windows XP introduit de nouvelles fonctionnalités de programmation de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="32265-126">Microsoft Windows XP introduces new Network Management programming features.</span></span> <span data-ttu-id="32265-127">Ces éléments étendent la capacité des opérations de gestion de réseau sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="32265-127">These elements extend the capability of Network Management operations on Windows XP and later.</span></span>

<span data-ttu-id="32265-128">Les nouvelles fonctions de gestion de réseau sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32265-128">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="32265-129">**NetAddAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="32265-129">**NetAddAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [<span data-ttu-id="32265-130">**NetEnumerateComputerNames**</span><span class="sxs-lookup"><span data-stu-id="32265-130">**NetEnumerateComputerNames**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [<span data-ttu-id="32265-131">**NetRemoveAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="32265-131">**NetRemoveAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [<span data-ttu-id="32265-132">**NetSetPrimaryComputerName**</span><span class="sxs-lookup"><span data-stu-id="32265-132">**NetSetPrimaryComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [<span data-ttu-id="32265-133">**SetNetScheduleAccountInformation**</span><span class="sxs-lookup"><span data-stu-id="32265-133">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




