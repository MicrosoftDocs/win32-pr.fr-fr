---
title: Classe MDM_Policy_Result01_Start02
description: La \_ classe Result01 Start02 de la stratégie MDM \_ \_ représente les stratégies d’écran de démarrage disponibles.
ms.assetid: 997d64f9-b2be-47b8-8a84-97438e7fa842
keywords:
- Classe MDM_Policy_Result01_Start02
- Classe MDM_Policy_Result01_Start02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02.InstanceID
- MDM_Policy_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412e9ccecdc9f691b03a94ba5528eb6b7e3d7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032740"
---
# <a name="mdm_policy_result01_start02-class"></a><span data-ttu-id="d05f3-105">\_Classe Start02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="d05f3-105">MDM\_Policy\_Result01\_Start02 class</span></span>

<span data-ttu-id="d05f3-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d05f3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d05f3-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d05f3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d05f3-108">La **classe \_ \_ Result01 \_ Start02 de la stratégie MDM** représente les stratégies d’écran de démarrage disponibles.</span><span class="sxs-lookup"><span data-stu-id="d05f3-108">The **MDM\_Policy\_Result01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="d05f3-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d05f3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d05f3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d05f3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 AllowPinnedFolderVideos;
  sint32 AllowPinnedFolderSettings;
  sint32 AllowPinnedFolderPictures;
  sint32 AllowPinnedFolderPersonalFolder;
  sint32 AllowPinnedFolderNetwork;
  sint32 AllowPinnedFolderMusic;
  sint32 AllowPinnedFolderHomeGroup;
  sint32 AllowPinnedFolderFileExplorer;
  sint32 AllowPinnedFolderDownloads;
  sint32 AllowPinnedFolderDocuments;
  sint32 ForceStartSize;
  string StartLayout;
  sint32 NoPinningToTaskbar;
  string ImportEdgeAssets;
  sint32 HideUserTile;
  sint32 HideSwitchAccount;
  sint32 HideSleep;
  sint32 HideSignOut;
  sint32 HideShutDown;
  sint32 HideRestart;
  sint32 HideRecentlyAddedApps;
  sint32 HideRecentJumplists;
  sint32 HidePowerButton;
  sint32 HideLock;
  sint32 HideHibernate;
  sint32 HideFrequentlyUsedApps;
  sint32 HideChangeAccountSettings;
  sint32 HideAppList;
};
```

## <a name="members"></a><span data-ttu-id="d05f3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d05f3-111">Members</span></span>

<span data-ttu-id="d05f3-112">La **classe \_ \_ Result01 \_ Start02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d05f3-112">The **MDM\_Policy\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="d05f3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d05f3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d05f3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d05f3-114">Properties</span></span>

<span data-ttu-id="d05f3-115">La **classe \_ \_ Result01 \_ Start02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d05f3-115">The **MDM\_Policy\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d05f3-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="d05f3-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="d05f3-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="d05f3-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="d05f3-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="d05f3-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="d05f3-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="d05f3-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="d05f3-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="d05f3-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="d05f3-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="d05f3-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="d05f3-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="d05f3-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="d05f3-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="d05f3-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="d05f3-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="d05f3-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="d05f3-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-168">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="d05f3-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="d05f3-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-174">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="d05f3-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-177">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="d05f3-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-180">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="d05f3-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-183">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="d05f3-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-186">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="d05f3-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-189">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d05f3-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="d05f3-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d05f3-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d05f3-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d05f3-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d05f3-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d05f3-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-197">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d05f3-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d05f3-198">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d05f3-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="d05f3-199">Pour cette classe, la chaîne est « start ».</span><span class="sxs-lookup"><span data-stu-id="d05f3-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="d05f3-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="d05f3-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-201">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d05f3-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d05f3-203">**ID**</span><span class="sxs-lookup"><span data-stu-id="d05f3-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d05f3-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d05f3-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-206">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d05f3-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d05f3-207">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d05f3-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="d05f3-208">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="d05f3-208">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="d05f3-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="d05f3-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05f3-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d05f3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d05f3-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d05f3-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d05f3-212">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d05f3-212">Requirements</span></span>



| <span data-ttu-id="d05f3-213">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d05f3-213">Requirement</span></span> | <span data-ttu-id="d05f3-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="d05f3-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d05f3-215">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d05f3-215">Minimum supported client</span></span><br/> | <span data-ttu-id="d05f3-216">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d05f3-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d05f3-217">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d05f3-217">Minimum supported server</span></span><br/> | <span data-ttu-id="d05f3-218">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d05f3-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d05f3-219">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d05f3-219">Namespace</span></span><br/>                | <span data-ttu-id="d05f3-220">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d05f3-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d05f3-221">MOF</span><span class="sxs-lookup"><span data-stu-id="d05f3-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d05f3-222"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d05f3-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d05f3-223">DLL</span><span class="sxs-lookup"><span data-stu-id="d05f3-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d05f3-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d05f3-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d05f3-225">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d05f3-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d05f3-226">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d05f3-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

