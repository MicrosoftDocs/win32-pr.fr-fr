---
title: Classe Win32_RDMSDeploymentSettings
description: Gère les paramètres de déploiement pour une collection de bureaux virtuels.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508473"
---
# <a name="win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="f7878-105">\_Classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="f7878-105">Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="f7878-106">Gère les paramètres de déploiement pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-106">Manages deployment settings for a virtual desktop collection.</span></span>

<span data-ttu-id="f7878-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f7878-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7878-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7878-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a><span data-ttu-id="f7878-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f7878-109">Members</span></span>

<span data-ttu-id="f7878-110">La classe **Win32 \_ RDMSDeploymentSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f7878-110">The **Win32\_RDMSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="f7878-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f7878-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f7878-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f7878-112">Methods</span></span>

<span data-ttu-id="f7878-113">La classe **Win32 \_ RDMSDeploymentSettings** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f7878-113">The **Win32\_RDMSDeploymentSettings** class has these methods.</span></span>



| <span data-ttu-id="f7878-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="f7878-114">Method</span></span>                                                                                                  | <span data-ttu-id="f7878-115">Description</span><span class="sxs-lookup"><span data-stu-id="f7878-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7878-116">**GetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-116">**GetBaseVHDPath**</span></span>](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="f7878-117">Récupère le chemin d’accès de base au répertoire dans lequel les disques durs virtuels de la collection de bureaux virtuels sont déployés.</span><span class="sxs-lookup"><span data-stu-id="f7878-117">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="f7878-118">**GetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f7878-118">**GetConnectionString**</span></span>](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | <span data-ttu-id="f7878-119">Récupère la chaîne de connexion de base de données au niveau du déploiement.</span><span class="sxs-lookup"><span data-stu-id="f7878-119">Retrieves the deployment-level database connection string.</span></span><br/>                                                             |
| [<span data-ttu-id="f7878-120">**GetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-120">**GetDiffVHDPath**</span></span>](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="f7878-121">Récupère le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-121">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>            |
| [<span data-ttu-id="f7878-122">**GetExportPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-122">**GetExportPath**</span></span>](getexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="f7878-123">Récupère le chemin d’accès du répertoire dans lequel les ordinateurs virtuels sont déployés pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-123">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                  |
| [<span data-ttu-id="f7878-124">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="f7878-124">**GetInt32Property**</span></span>](getint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="f7878-125">Récupère une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-125">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                             |
| [<span data-ttu-id="f7878-126">**GetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f7878-126">**GetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | <span data-ttu-id="f7878-127">Récupère la chaîne de connexion secondaire de la base de données au niveau du déploiement, qui peut être utilisée pour prendre en charge l’expiration du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f7878-127">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span><br/> |
| [<span data-ttu-id="f7878-128">**GetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-128">**GetSMBPath**</span></span>](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="f7878-129">Récupère le chemin d’accès UNC au partage SMB vers lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.</span><span class="sxs-lookup"><span data-stu-id="f7878-129">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>      |
| [<span data-ttu-id="f7878-130">**GetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="f7878-130">**GetStringArrayDeploymentSetting**</span></span>](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="f7878-131">Récupère les paramètres de déploiement pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-131">Retrieves the deployment settings for a virtual desktop collection.</span></span><br/>                                                    |
| [<span data-ttu-id="f7878-132">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="f7878-132">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="f7878-133">Récupère une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-133">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="f7878-134">**RemoveDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="f7878-134">**RemoveDeploymentSetting**</span></span>](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | <span data-ttu-id="f7878-135">Supprime les paramètres de déploiement pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-135">Deletes the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="f7878-136">**SetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-136">**SetBaseVHDPath**</span></span>](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="f7878-137">Récupère le chemin d’accès de base au répertoire dans lequel les disques durs virtuels de la collection de bureaux virtuels sont déployés.</span><span class="sxs-lookup"><span data-stu-id="f7878-137">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="f7878-138">**SetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f7878-138">**SetConnectionString**</span></span>](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | <span data-ttu-id="f7878-139">Définit la chaîne de connexion de la base de données au niveau du déploiement.</span><span class="sxs-lookup"><span data-stu-id="f7878-139">Sets the deployment-level database connection string.</span></span><br/>                                                                  |
| [<span data-ttu-id="f7878-140">**SetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-140">**SetDiffVHDPath**</span></span>](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="f7878-141">Met à jour le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-141">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>              |
| [<span data-ttu-id="f7878-142">**SetExportPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-142">**SetExportPath**</span></span>](setexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="f7878-143">Met à jour le chemin d’accès au répertoire dans lequel les machines virtuelles sont déployées pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-143">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                    |
| [<span data-ttu-id="f7878-144">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="f7878-144">**SetInt32Property**</span></span>](setint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="f7878-145">Met à jour une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-145">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="f7878-146">**SetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f7878-146">**SetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | <span data-ttu-id="f7878-147">Définit la chaîne de connexion secondaire de la base de données au niveau du déploiement.</span><span class="sxs-lookup"><span data-stu-id="f7878-147">Sets the deployment-level database secondary connection string.</span></span><br/>                                                        |
| [<span data-ttu-id="f7878-148">**SetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="f7878-148">**SetSMBPath**</span></span>](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="f7878-149">Met à jour le chemin d’accès UNC au partage SMB sur lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.</span><span class="sxs-lookup"><span data-stu-id="f7878-149">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>        |
| [<span data-ttu-id="f7878-150">**SetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="f7878-150">**SetStringArrayDeploymentSetting**</span></span>](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="f7878-151">Met à jour les paramètres de déploiement pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-151">Updates the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="f7878-152">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="f7878-152">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="f7878-153">Met à jour une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f7878-153">Updates a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="f7878-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7878-154">Requirements</span></span>



| <span data-ttu-id="f7878-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7878-155">Requirement</span></span> | <span data-ttu-id="f7878-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7878-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7878-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7878-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f7878-158">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7878-158">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f7878-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7878-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f7878-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7878-160">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f7878-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7878-161">Namespace</span></span><br/>                | <span data-ttu-id="f7878-162">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="f7878-162">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f7878-163">MOF</span><span class="sxs-lookup"><span data-stu-id="f7878-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7878-164"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7878-164"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7878-165">DLL</span><span class="sxs-lookup"><span data-stu-id="f7878-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7878-166"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7878-166"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f7878-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7878-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7878-168">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f7878-168">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





