---
title: Méthode Import de la classe Win32_TSGatewayServer
description: Importe une configuration donnée sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode d’importation
- Services Bureau à distance de la méthode d’importation, classe Win32_TSGatewayServer
- Win32_TSGatewayServer de la classe Services Bureau à distance, méthode Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942338"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="9eca1-106">Méthode Import de la \_ classe TSGatewayServer Win32</span><span class="sxs-lookup"><span data-stu-id="9eca1-106">Import method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="9eca1-107">Importe une configuration donnée sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="9eca1-107">Imports a given configuration to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eca1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eca1-108">Syntax</span></span>


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a><span data-ttu-id="9eca1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9eca1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eca1-110">*ImportType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eca1-110">*ImportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eca1-111">Contenu à importer.</span><span class="sxs-lookup"><span data-stu-id="9eca1-111">The content to import.</span></span> <span data-ttu-id="9eca1-112">Définissez le type d’importation en définissant les bits correspondants dans le paramètre *ImportType* .</span><span class="sxs-lookup"><span data-stu-id="9eca1-112">Set the import type by setting the corresponding bits in the *ImportType* parameter.</span></span> <span data-ttu-id="9eca1-113">Vous pouvez définir plusieurs types d’importation.</span><span class="sxs-lookup"><span data-stu-id="9eca1-113">You can set multiple import types.</span></span> <span data-ttu-id="9eca1-114">Par exemple, si le bit 0 est défini, Services Bureau à distance stratégies d’autorisation des connexions (RD Cap) seront importées.</span><span class="sxs-lookup"><span data-stu-id="9eca1-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be imported.</span></span> <span data-ttu-id="9eca1-115">Si les deux bits 0 et 2 sont définis, les stratégies d’autorisation des ressources pour les services Bureau à distance et les Services Bureau à distance RD sont importées.</span><span class="sxs-lookup"><span data-stu-id="9eca1-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be imported.</span></span>

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span data-ttu-id="9eca1-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importer toutes les majuscules** (1)</span><span class="sxs-lookup"><span data-stu-id="9eca1-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Import all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9eca1-117">Importez toutes les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9eca1-117">Import all RD CAPs.</span></span>

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="9eca1-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importer tous les serveurs RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="9eca1-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Import all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9eca1-119">Importez une liste de tous les serveurs NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="9eca1-119">Import a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span data-ttu-id="9eca1-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importer tous les stratégies** (4)</span><span class="sxs-lookup"><span data-stu-id="9eca1-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Import all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9eca1-121">Importez tous les stratégies RD.</span><span class="sxs-lookup"><span data-stu-id="9eca1-121">Import all RD RAPs.</span></span>

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span data-ttu-id="9eca1-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importer tous les RGs** (8)</span><span class="sxs-lookup"><span data-stu-id="9eca1-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Import all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9eca1-123">Importez tous les groupes de ressources.</span><span class="sxs-lookup"><span data-stu-id="9eca1-123">Import all resource groups.</span></span>

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="9eca1-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importer tous les serveurs LoadBalancing** (16)</span><span class="sxs-lookup"><span data-stu-id="9eca1-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Import all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9eca1-125">Importez une liste de tous les serveurs d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="9eca1-125">Import a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="9eca1-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importer tous les paramètres du serveur** (32)</span><span class="sxs-lookup"><span data-stu-id="9eca1-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Import all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9eca1-127">Importez tous les paramètres de serveur liés à la passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9eca1-127">Import all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="9eca1-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importer toutes les stratégies de contrôle d’intégrité** (64)</span><span class="sxs-lookup"><span data-stu-id="9eca1-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Import all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="9eca1-129">Importez toutes les stratégies de contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="9eca1-129">Import all health policies.</span></span>

<span data-ttu-id="9eca1-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 et Windows Server 2008 : \* \*</span><span class="sxs-lookup"><span data-stu-id="9eca1-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="9eca1-131">Cette valeur n’est pas prise en charge avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="9eca1-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9eca1-132">*XmlString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eca1-132">*XmlString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eca1-133">Configuration sous la forme d’une chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="9eca1-133">The configuration as an XML string.</span></span>

</dd> <dt>

<span data-ttu-id="9eca1-134">*MergeOrReplace* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eca1-134">*MergeOrReplace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eca1-135">Indique s’il faut fusionner ou remplacer des données lorsqu’un conflit se produit.</span><span class="sxs-lookup"><span data-stu-id="9eca1-135">Indicates whether to merge or replace data when a conflict occurs.</span></span>

> [!Note]  
> <span data-ttu-id="9eca1-136">La fusion n’est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="9eca1-136">Merge is not yet implemented.</span></span> <span data-ttu-id="9eca1-137">Par conséquent, la valeur de ce paramètre est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9eca1-137">Therefore, this parameter value is ignored.</span></span>

 

</dd> <dt>

<span data-ttu-id="9eca1-138">*LogString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9eca1-138">*LogString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eca1-139">Informations de journal générées pendant l’opération d’importation.</span><span class="sxs-lookup"><span data-stu-id="9eca1-139">The log information that is generated during the import operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9eca1-140">Notes</span><span class="sxs-lookup"><span data-stu-id="9eca1-140">Remarks</span></span>

<span data-ttu-id="9eca1-141">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9eca1-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9eca1-142">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9eca1-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9eca1-143">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9eca1-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9eca1-144">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9eca1-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9eca1-145">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9eca1-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9eca1-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eca1-146">Requirements</span></span>



| <span data-ttu-id="9eca1-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eca1-147">Requirement</span></span> | <span data-ttu-id="9eca1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eca1-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eca1-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eca1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9eca1-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eca1-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9eca1-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eca1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9eca1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eca1-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9eca1-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9eca1-153">Namespace</span></span><br/>                | <span data-ttu-id="9eca1-154">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="9eca1-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9eca1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="9eca1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9eca1-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9eca1-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9eca1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9eca1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eca1-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eca1-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9eca1-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eca1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eca1-160">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="9eca1-160">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

