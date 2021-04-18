---
description: L’API Windows Update Agent (WUA) peut être utilisée par un utilisateur sur un ordinateur distant ou par une application qui s’exécute sur un ordinateur distant. Toutefois, l’utilisateur ou l’application distante doit disposer de privilèges d’administrateur.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Utilisation de WUA à partir d’un ordinateur distant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542889"
---
# <a name="using-wua-from-a-remote-computer"></a><span data-ttu-id="122e6-104">Utilisation de WUA à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="122e6-104">Using WUA From a Remote Computer</span></span>

<span data-ttu-id="122e6-105">L’API Windows Update Agent (WUA) peut être utilisée par un utilisateur sur un ordinateur distant ou par une application qui s’exécute sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="122e6-105">The Windows Update Agent (WUA) API can be used by a user on a remote computer or by an application that is running on a remote computer.</span></span> <span data-ttu-id="122e6-106">Toutefois, l’utilisateur ou l’application distante doit disposer de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="122e6-106">However, the remote user or application must have administrator privileges.</span></span>

<span data-ttu-id="122e6-107">La liste suivante contient les interfaces disponibles pour les utilisateurs et les applications distantes :</span><span class="sxs-lookup"><span data-stu-id="122e6-107">The following list contains interfaces that are available to remote users and applications:</span></span>

-   [<span data-ttu-id="122e6-108">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="122e6-108">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [<span data-ttu-id="122e6-109">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="122e6-109">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="122e6-110">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="122e6-110">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [<span data-ttu-id="122e6-111">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="122e6-111">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="122e6-112">**ISearchResult**</span><span class="sxs-lookup"><span data-stu-id="122e6-112">**ISearchResult**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [<span data-ttu-id="122e6-113">**IUpdateCollection**</span><span class="sxs-lookup"><span data-stu-id="122e6-113">**IUpdateCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [<span data-ttu-id="122e6-114">**IUpdate**</span><span class="sxs-lookup"><span data-stu-id="122e6-114">**IUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [<span data-ttu-id="122e6-115">**IUpdate2**</span><span class="sxs-lookup"><span data-stu-id="122e6-115">**IUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [<span data-ttu-id="122e6-116">**IWindowsDriverUpdate**</span><span class="sxs-lookup"><span data-stu-id="122e6-116">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [<span data-ttu-id="122e6-117">**IWindowsDriverUpdate2**</span><span class="sxs-lookup"><span data-stu-id="122e6-117">**IWindowsDriverUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [<span data-ttu-id="122e6-118">**IUpdateIdentity**</span><span class="sxs-lookup"><span data-stu-id="122e6-118">**IUpdateIdentity**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [<span data-ttu-id="122e6-119">**IImageInformation**</span><span class="sxs-lookup"><span data-stu-id="122e6-119">**IImageInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [<span data-ttu-id="122e6-120">**IInstallationBehavior**</span><span class="sxs-lookup"><span data-stu-id="122e6-120">**IInstallationBehavior**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [<span data-ttu-id="122e6-121">**IStringCollection**</span><span class="sxs-lookup"><span data-stu-id="122e6-121">**IStringCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [<span data-ttu-id="122e6-122">**IUpdateHistoryEntryCollection**</span><span class="sxs-lookup"><span data-stu-id="122e6-122">**IUpdateHistoryEntryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [<span data-ttu-id="122e6-123">**IUpdateHistoryEntry**</span><span class="sxs-lookup"><span data-stu-id="122e6-123">**IUpdateHistoryEntry**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [<span data-ttu-id="122e6-124">**ICategoryCollection**</span><span class="sxs-lookup"><span data-stu-id="122e6-124">**ICategoryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [<span data-ttu-id="122e6-125">**ICategory**</span><span class="sxs-lookup"><span data-stu-id="122e6-125">**ICategory**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [<span data-ttu-id="122e6-126">**IUpdateExceptionCollection**</span><span class="sxs-lookup"><span data-stu-id="122e6-126">**IUpdateExceptionCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [<span data-ttu-id="122e6-127">**IUpdateException**</span><span class="sxs-lookup"><span data-stu-id="122e6-127">**IUpdateException**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [<span data-ttu-id="122e6-128">**IUpdateDownloadContentCollection**</span><span class="sxs-lookup"><span data-stu-id="122e6-128">**IUpdateDownloadContentCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [<span data-ttu-id="122e6-129">**IUpdateDownloadContent**</span><span class="sxs-lookup"><span data-stu-id="122e6-129">**IUpdateDownloadContent**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [<span data-ttu-id="122e6-130">**IUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="122e6-130">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [<span data-ttu-id="122e6-131">**IUpdateServiceCollection**</span><span class="sxs-lookup"><span data-stu-id="122e6-131">**IUpdateServiceCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [<span data-ttu-id="122e6-132">**IUpdateService**</span><span class="sxs-lookup"><span data-stu-id="122e6-132">**IUpdateService**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [<span data-ttu-id="122e6-133">**IWindowsUpdateAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="122e6-133">**IWindowsUpdateAgentInfo**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

<span data-ttu-id="122e6-134">La liste suivante contient des interfaces et des propriétés qui ne sont pas disponibles pour les applications et les utilisateurs distants :</span><span class="sxs-lookup"><span data-stu-id="122e6-134">The following list contains interfaces and properties that are not available to remote users and applications:</span></span>

-   [<span data-ttu-id="122e6-135">**IUpdateSession::CreateUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="122e6-135">**IUpdateSession::CreateUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [<span data-ttu-id="122e6-136">**IUpdateSession::CreateUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="122e6-136">**IUpdateSession::CreateUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [<span data-ttu-id="122e6-137">**Propriété WebProxy de IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="122e6-137">**WebProxy Property of IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [<span data-ttu-id="122e6-138">**IUpdateSearcher::BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="122e6-138">**IUpdateSearcher::BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [<span data-ttu-id="122e6-139">**IUpdateSearcher::EndSearch**</span><span class="sxs-lookup"><span data-stu-id="122e6-139">**IUpdateSearcher::EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   <span data-ttu-id="122e6-140">La [**propriété IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** est en lecture seule quand elle est appelée à distance.)</span><span class="sxs-lookup"><span data-stu-id="122e6-140">[**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** is read-only when it is called remotely.)</span></span>
-   [<span data-ttu-id="122e6-141">**IUpdate :: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="122e6-141">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [<span data-ttu-id="122e6-142">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="122e6-142">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="122e6-143">**IUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="122e6-143">**IUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [<span data-ttu-id="122e6-144">**IWindowsDriverUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="122e6-144">**IWindowsDriverUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [<span data-ttu-id="122e6-145">**IUpdateServiceManager :: AddService**</span><span class="sxs-lookup"><span data-stu-id="122e6-145">**IUpdateServiceManager::AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [<span data-ttu-id="122e6-146">**IUpdateServiceManager::RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="122e6-146">**IUpdateServiceManager::RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [<span data-ttu-id="122e6-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="122e6-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [<span data-ttu-id="122e6-148">**IAutomaticUpdate ::P ause**</span><span class="sxs-lookup"><span data-stu-id="122e6-148">**IAutomaticUpdate::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="122e6-149">**IAutomaticUpdates :: Resume**</span><span class="sxs-lookup"><span data-stu-id="122e6-149">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="122e6-150">**IAutomaticUpdates::ShowSettingsDialog**</span><span class="sxs-lookup"><span data-stu-id="122e6-150">**IAutomaticUpdates::ShowSettingsDialog**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [<span data-ttu-id="122e6-151">**Propriété Settings de IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="122e6-151">**Settings Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [<span data-ttu-id="122e6-152">**Propriété ServiceEnabled de IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="122e6-152">**ServiceEnabled Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [<span data-ttu-id="122e6-153">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="122e6-153">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="122e6-154">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="122e6-154">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

<span data-ttu-id="122e6-155">Les ports et exceptions suivants doivent être ajoutés aux paramètres du pare-feu Windows pour Windows Vista et Windows Server 2008 pour que l’API WUA soit appelée à distance.</span><span class="sxs-lookup"><span data-stu-id="122e6-155">The following ports and exceptions must be added to the Windows firewall settings for Windows Vista and Windows Server 2008 for the WUA API to be called remotely.</span></span>

<dl> <dt>

<span data-ttu-id="122e6-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span><span class="sxs-lookup"><span data-stu-id="122e6-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="122e6-157">Port local : 135</span><span class="sxs-lookup"><span data-stu-id="122e6-157">Local port: 135</span></span></dd> <dd><span data-ttu-id="122e6-158">Port distant : tous</span><span class="sxs-lookup"><span data-stu-id="122e6-158">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="122e6-159">Numéro de protocole : 6</span><span class="sxs-lookup"><span data-stu-id="122e6-159">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="122e6-160">Fichier exécutable :% windir% \\ system32 \\svchost.exe</span><span class="sxs-lookup"><span data-stu-id="122e6-160">Executable: %windir%\\system32\\svchost.exe</span></span></dd> <dd><span data-ttu-id="122e6-161">Service : RPCSS</span><span class="sxs-lookup"><span data-stu-id="122e6-161">Service: rpcss</span></span></dd> <dd><span data-ttu-id="122e6-162">Privilège distant : administrateur</span><span class="sxs-lookup"><span data-stu-id="122e6-162">Remote privilege: Administrator</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="122e6-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span><span class="sxs-lookup"><span data-stu-id="122e6-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="122e6-164">Port local : RPC dynamique</span><span class="sxs-lookup"><span data-stu-id="122e6-164">Local port: Dynamic RPC</span></span></dd> <dd><span data-ttu-id="122e6-165">Port distant : tous</span><span class="sxs-lookup"><span data-stu-id="122e6-165">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="122e6-166">Numéro de protocole : 6</span><span class="sxs-lookup"><span data-stu-id="122e6-166">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="122e6-167">Fichier exécutable :% windir% \\ system32 \\dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="122e6-167">Executable: %windir%\\system32\\dllhost.exe</span></span></dd> <dd><span data-ttu-id="122e6-168">Privilège distant : administrateur</span><span class="sxs-lookup"><span data-stu-id="122e6-168">Remote privilege: Administrator</span></span></dd> </dl> </dd> </dl>

<span data-ttu-id="122e6-169">La liste suivante contient les outils qui peuvent être utilisés pour configurer les paramètres du pare-feu Windows :</span><span class="sxs-lookup"><span data-stu-id="122e6-169">The following list contains tools that can be used to configure Windows Firewall settings:</span></span>

-   <span data-ttu-id="122e6-170">Pare-feu Windows avec le composant logiciel enfichable Sécurité avancée</span><span class="sxs-lookup"><span data-stu-id="122e6-170">Windows Firewall with Advanced Security snap-in</span></span>
-   <span data-ttu-id="122e6-171">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="122e6-171">Group Policy</span></span>
-   <span data-ttu-id="122e6-172">Outil en ligne de commande netsh advfirewall</span><span class="sxs-lookup"><span data-stu-id="122e6-172">Netsh advfirewall command-line tool</span></span>

<span data-ttu-id="122e6-173">Pour plus d’informations sur l’utilisation des outils pour configurer les paramètres du pare-feu Windows, consultez [prise en main avec le pare-feu Windows avec fonctions avancées de sécurité](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="122e6-173">For more information about how to use tools to configure Windows Firewall settings, see [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span></span>

 

 
