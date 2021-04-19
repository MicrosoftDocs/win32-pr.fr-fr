---
description: Lorsque WUA détecte qu’un appelant n’est pas autorisé à accéder à une interface, une méthode ou une propriété, le HRESULT E \_ ACCESSDENIED est retourné.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Sécurisation des interfaces, des méthodes et des propriétés dans l’API WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517516"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a><span data-ttu-id="e5fbf-103">Sécurisation des interfaces, des méthodes et des propriétés dans l’API WUA</span><span class="sxs-lookup"><span data-stu-id="e5fbf-103">Securing Interfaces, Methods, and Properties in the WUA API</span></span>

<span data-ttu-id="e5fbf-104">Certaines interfaces, méthodes et propriétés de Windows Update Agent (WUA) sont accessibles uniquement aux appelants qui appartiennent aux groupes de sécurité Windows suivants :</span><span class="sxs-lookup"><span data-stu-id="e5fbf-104">Some interfaces, methods, and properties of Windows Update Agent (WUA) are accessible only to callers who belong to the following Windows security groups:</span></span>

-   <span data-ttu-id="e5fbf-105">Administrateur</span><span class="sxs-lookup"><span data-stu-id="e5fbf-105">Administrator</span></span>
-   <span data-ttu-id="e5fbf-106">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="e5fbf-106">User</span></span>
-   <span data-ttu-id="e5fbf-107">Utilisateur avancé</span><span class="sxs-lookup"><span data-stu-id="e5fbf-107">Power User</span></span>

<span data-ttu-id="e5fbf-108">Lorsque WUA détecte qu’un appelant n’est pas autorisé à accéder à une interface, une méthode ou une propriété, le **HRESULT** E \_ ACCESSDENIED est retourné.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-108">When WUA detects that a caller does not have permission to access an interface, method, or property, the **HRESULT** E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="e5fbf-109">Les interfaces suivantes sont disponibles pour les groupes de sécurité administrateur, utilisateur et utilisateur avec pouvoir :</span><span class="sxs-lookup"><span data-stu-id="e5fbf-109">The following interfaces are available to the Administrator, User, and Power User security groups:</span></span>

-   [<span data-ttu-id="e5fbf-110">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-110">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="e5fbf-111">**IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-111">**IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [<span data-ttu-id="e5fbf-112">**IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-112">**IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [<span data-ttu-id="e5fbf-113">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-113">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [<span data-ttu-id="e5fbf-114">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-114">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   <span data-ttu-id="e5fbf-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) et [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span><span class="sxs-lookup"><span data-stu-id="e5fbf-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) and [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span></span>

> [!Note]  
> <span data-ttu-id="e5fbf-116">Si les conditions suivantes sont remplies, une recherche échoue :</span><span class="sxs-lookup"><span data-stu-id="e5fbf-116">If the following conditions are true, a search fails:</span></span>
>
> -   <span data-ttu-id="e5fbf-117">Un utilisateur qui n’est pas un administrateur définit la [**propriété UserLocale de l’interface IUpdateSession2 sur des**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) paramètres régionaux qui correspondent à une langue qui n’est pas installée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-117">A user who is not an administrator sets the [**UserLocale property of the IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) interface to a locale that corresponds to a language that is not installed on the computer.</span></span>
> -   <span data-ttu-id="e5fbf-118">La recherche utilise un objet UpdateSearch créé à partir de l’objet UpdateSession.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-118">The search uses an UpdateSearch object created from the UpdateSession object.</span></span>

 

<span data-ttu-id="e5fbf-119">Les interfaces et les méthodes de téléchargement suivantes sont disponibles pour l’administrateur et les groupes d’utilisateurs avec pouvoir :</span><span class="sxs-lookup"><span data-stu-id="e5fbf-119">The following download interfaces and methods are available to the Administrator and Power User groups:</span></span>

-   [<span data-ttu-id="e5fbf-120">**IUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-120">**IUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [<span data-ttu-id="e5fbf-121">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-121">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="e5fbf-122">**IAutomaticUpdatesSettings2 :: CheckPermission**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-122">**IAutomaticUpdatesSettings2::CheckPermission**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > <span data-ttu-id="e5fbf-123">Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent appeler [**IAutomaticUpdatesSettings2 :: checkPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-123">Administrators, users, and power users can call [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span></span>

     

<span data-ttu-id="e5fbf-124">Les interfaces d’installation, les méthodes et les propriétés suivantes sont disponibles pour les groupes d’administrateurs :</span><span class="sxs-lookup"><span data-stu-id="e5fbf-124">The following installation interfaces, methods, and properties are available to the Administrator groups:</span></span>

-   [<span data-ttu-id="e5fbf-125">**IAutomaticUpdates ::P ause**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-125">**IAutomaticUpdates::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="e5fbf-126">**IAutomaticUpdates :: Resume**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-126">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="e5fbf-127">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-127">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="e5fbf-128">**IUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-128">**IUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [<span data-ttu-id="e5fbf-129">**Propriété IsHidden de IUpdate**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-129">**IsHidden Property of IUpdate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > <span data-ttu-id="e5fbf-130">Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-130">Administrators, users, and power users can retrieve the values of the [**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span></span> <span data-ttu-id="e5fbf-131">Toutefois, seuls les administrateurs et les utilisateurs avec pouvoir peuvent définir les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-131">However, only administrators and power users can set the values.</span></span>

     

-   [<span data-ttu-id="e5fbf-132">**IUpdate :: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-132">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > <span data-ttu-id="e5fbf-133">Les administrateurs et les utilisateurs avec pouvoir peuvent appeler la [**méthode AcceptEula de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-133">Administrators and power users can call the [**AcceptEula method of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span></span>

     

-   [<span data-ttu-id="e5fbf-134">**IAutomaticUpdatesSettings :: enregistrer**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-134">**IAutomaticUpdatesSettings::Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [<span data-ttu-id="e5fbf-135">**Propriété NotificationLevel de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-135">**NotificationLevel Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > <span data-ttu-id="e5fbf-136">Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété NotificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-136">Administrators, users, and power users can retrieve the values of the [**NotificationLevel Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span></span> <span data-ttu-id="e5fbf-137">Toutefois, seuls les administrateurs peuvent définir les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-137">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="e5fbf-138">**Propriété ScheduledInstallationDay de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-138">**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > <span data-ttu-id="e5fbf-139">Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-139">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span></span> <span data-ttu-id="e5fbf-140">Toutefois, seuls les administrateurs peuvent définir les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-140">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="e5fbf-141">**Propriété ScheduledInstallationTime de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-141">**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > <span data-ttu-id="e5fbf-142">Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-142">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="e5fbf-143">Toutefois, seuls les administrateurs peuvent définir les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-143">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="e5fbf-144">**Propriété IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-144">**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > <span data-ttu-id="e5fbf-145">Les administrateurs, les utilisateurs et les utilisateurs avec pouvoir peuvent récupérer les valeurs de la [**propriété IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-145">Administrators, users, and power users can retrieve the values of the [**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span></span> <span data-ttu-id="e5fbf-146">Toutefois, seuls les administrateurs peuvent définir les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-146">However, only administrators can set the values.</span></span>

     

 

 



