---
title: Structure MPSIGUPDATE_DATA (MpClient. h)
description: Données de notification transmises à la fonction de rappel de mise à jour de signature.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSIGUPDATE_DATA
- PMPSIGUPDATE_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104539"
---
# <a name="mpsigupdate_data-structure"></a><span data-ttu-id="c29c4-105">\_Structure de données MPSIGUPDATE</span><span class="sxs-lookup"><span data-stu-id="c29c4-105">MPSIGUPDATE\_DATA structure</span></span>

<span data-ttu-id="c29c4-106">Données de notification transmises à la fonction de rappel de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="c29c4-106">Notification data passed to the signature update callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c29c4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c29c4-107">Syntax</span></span>


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a><span data-ttu-id="c29c4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c29c4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c29c4-109">**dwPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="c29c4-109">**dwPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="c29c4-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c29c4-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c29c4-111">Une estimation du pourcentage pour toutes les mises à jour qui ont été téléchargées et/ou installées.</span><span class="sxs-lookup"><span data-stu-id="c29c4-111">An estimate of the percentage across all the updates that have been downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="c29c4-112">**dwTotalUpdates**</span><span class="sxs-lookup"><span data-stu-id="c29c4-112">**dwTotalUpdates**</span></span>
</dt> <dd>

<span data-ttu-id="c29c4-113">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c29c4-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c29c4-114">Nombre total de mises à jour à télécharger et/ou à installer.</span><span class="sxs-lookup"><span data-stu-id="c29c4-114">Total number of updates to download and/or install.</span></span>

</dd> <dt>

<span data-ttu-id="c29c4-115">**dwCurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="c29c4-115">**dwCurrentUpdateIndex**</span></span>
</dt> <dd>

<span data-ttu-id="c29c4-116">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c29c4-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c29c4-117">Valeur d’index de base zéro qui spécifie quelle mise à jour parmi celles requises est actuellement en cours de téléchargement et/ou d’installation.</span><span class="sxs-lookup"><span data-stu-id="c29c4-117">Zero-based index value that specifies which update among those required is currently being downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="c29c4-118">**eType**</span><span class="sxs-lookup"><span data-stu-id="c29c4-118">**eType**</span></span>
</dt> <dd>

<span data-ttu-id="c29c4-119">Type : **MPSIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="c29c4-119">Type: **MPSIGUPDATE\_TYPE**</span></span>

</dd> <dd>

<span data-ttu-id="c29c4-120">Type de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c29c4-120">Update type.</span></span> <span data-ttu-id="c29c4-121">Une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="c29c4-121">One of the following possible values:</span></span>



| <span data-ttu-id="c29c4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c29c4-122">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="c29c4-123">Signification</span><span class="sxs-lookup"><span data-stu-id="c29c4-123">Meaning</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <span data-ttu-id="c29c4-124"><dt>**MPSIGUPDATE \_ type \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-124"><dt>**MPSIGUPDATE\_TYPE\_NONE**</dt></span></span> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <span data-ttu-id="c29c4-125"><dt>**\_type MPSIGUPDATE \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-125"><dt>**MPSIGUPDATE\_TYPE\_MANAGED**</dt></span></span> </dl>                                   | <span data-ttu-id="c29c4-126">Mise à jour WSUS.</span><span class="sxs-lookup"><span data-stu-id="c29c4-126">WSUS update.</span></span> <span data-ttu-id="c29c4-127">L’annulation nécessite des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c29c4-127">Cancel requires administrator rights.</span></span><br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <span data-ttu-id="c29c4-128"><dt>**\_type MPSIGUPDATE \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-128"><dt>**MPSIGUPDATE\_TYPE\_HTTP**</dt></span></span> </dl>                                            | <span data-ttu-id="c29c4-129">Mise à jour HTTP.</span><span class="sxs-lookup"><span data-stu-id="c29c4-129">HTTP update.</span></span> <span data-ttu-id="c29c4-130">Droits d’administrateur non nécessaires pour annuler.</span><span class="sxs-lookup"><span data-stu-id="c29c4-130">Administrator rights not needed to cancel.</span></span><br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <span data-ttu-id="c29c4-131"><dt>**\_type MPSIGUPDATE \_ http \_ SRV**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-131"><dt>**MPSIGUPDATE\_TYPE\_HTTP\_SRV**</dt></span></span> </dl>                               | <span data-ttu-id="c29c4-132">HTTP à partir du service.</span><span class="sxs-lookup"><span data-stu-id="c29c4-132">HTTP from service.</span></span> <span data-ttu-id="c29c4-133">L’annulation nécessite des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c29c4-133">Cancel requires administrator rights.</span></span><br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <span data-ttu-id="c29c4-134"><dt>**MPSIGUPDATE \_ type \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-134"><dt>**MPSIGUPDATE\_TYPE\_UNC**</dt></span></span> </dl>                                               | <span data-ttu-id="c29c4-135">Partage UNC.</span><span class="sxs-lookup"><span data-stu-id="c29c4-135">UNC share.</span></span> <span data-ttu-id="c29c4-136">Droits d’administrateur non nécessaires pour annuler.</span><span class="sxs-lookup"><span data-stu-id="c29c4-136">Administrator rights not needed to cancel.</span></span><br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <span data-ttu-id="c29c4-137"><dt>**\_type MPSIGUPDATE \_ non géré**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-137"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED**</dt></span></span> </dl>                             | <span data-ttu-id="c29c4-138">Mise à jour MU/WU.</span><span class="sxs-lookup"><span data-stu-id="c29c4-138">MU/WU update.</span></span> <span data-ttu-id="c29c4-139">L’annulation nécessite des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c29c4-139">Cancel requires administrator rights.</span></span><br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <span data-ttu-id="c29c4-140"><dt>**\_ \_ plateforme managée de type MPSIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-140"><dt>**MPSIGUPDATE\_TYPE\_MANAGED\_PLATFORM**</dt></span></span> </dl>       | <span data-ttu-id="c29c4-141">Mise à jour WSUS pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="c29c4-141">WSUS update for PLATFORM.</span></span> <span data-ttu-id="c29c4-142">L’annulation nécessite des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c29c4-142">Cancel requires administrator rights.</span></span><br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <span data-ttu-id="c29c4-143"><dt>**\_ \_ plateforme non managée de type MPSIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-143"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED\_PLATFORM**</dt></span></span> </dl> | <span data-ttu-id="c29c4-144">Mise à jour de MU/WU pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="c29c4-144">MU/WU update for PLATFORM.</span></span> <span data-ttu-id="c29c4-145">L’annulation nécessite des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c29c4-145">Cancel requires administrator rights.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c29c4-146">**Étape**</span><span class="sxs-lookup"><span data-stu-id="c29c4-146">**Stage**</span></span>
</dt> <dd>

<span data-ttu-id="c29c4-147">Type : **\_ \_ phase de mise à jour du pack d’installation**</span><span class="sxs-lookup"><span data-stu-id="c29c4-147">Type: **MP\_UPDATE\_STAGE**</span></span>

</dd> <dd>

<span data-ttu-id="c29c4-148">Étape de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c29c4-148">Update stage.</span></span> <span data-ttu-id="c29c4-149">Une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="c29c4-149">One of the following possible values:</span></span>



| <span data-ttu-id="c29c4-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="c29c4-150">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="c29c4-151">Signification</span><span class="sxs-lookup"><span data-stu-id="c29c4-151">Meaning</span></span>                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <span data-ttu-id="c29c4-152"><dt>**étape de point de gestion \_ \_ inconnue**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-152"><dt>**MP\_STAGE\_UNKNOWN**</dt></span></span> </dl>       | <span data-ttu-id="c29c4-153">Étape de mise à jour inconnue.</span><span class="sxs-lookup"><span data-stu-id="c29c4-153">Update stage unknown.</span></span><br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <span data-ttu-id="c29c4-154"><dt>**\_ \_ mise à jour de recherche de Pack d’e**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-154"><dt>**MP\_SEARCH\_UPDATE**</dt></span></span> </dl>       | <span data-ttu-id="c29c4-155">Étape de recherche de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c29c4-155">Update search stage.</span></span><br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <span data-ttu-id="c29c4-156"><dt>**\_ \_ mise à jour du téléchargement du pack d’e**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-156"><dt>**MP\_DOWNLOAD\_UPDATE**</dt></span></span> </dl> | <span data-ttu-id="c29c4-157">Étape de téléchargement de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c29c4-157">Update download stage.</span></span><br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <span data-ttu-id="c29c4-158"><dt>**\_ \_ mise à jour d’installation du pack d’installation**</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-158"><dt>**MP\_INSTALL\_UPDATE**</dt></span></span> </dl>    | <span data-ttu-id="c29c4-159">Mettez à jour l’étape d’installation.</span><span class="sxs-lookup"><span data-stu-id="c29c4-159">Update install stage.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="c29c4-160">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="c29c4-160">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="c29c4-161">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="c29c4-161">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="c29c4-162">Mettre à jour le chemin.</span><span class="sxs-lookup"><span data-stu-id="c29c4-162">Update path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c29c4-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c29c4-163">Requirements</span></span>



| <span data-ttu-id="c29c4-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c29c4-164">Requirement</span></span> | <span data-ttu-id="c29c4-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="c29c4-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c29c4-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c29c4-166">Minimum supported client</span></span><br/> | <span data-ttu-id="c29c4-167">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c29c4-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c29c4-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c29c4-168">Minimum supported server</span></span><br/> | <span data-ttu-id="c29c4-169">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c29c4-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c29c4-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="c29c4-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="c29c4-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c29c4-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





