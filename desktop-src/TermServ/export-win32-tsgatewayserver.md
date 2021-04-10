---
title: Méthode Export de la classe Win32_TSGatewayServer
description: Retourne la configuration du serveur de passerelle Bureau à distance (passerelle Bureau à distance) sous la forme d’une chaîne XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode d’exportation
- Méthode d’exportation Services Bureau à distance, classe Win32_TSGatewayServer
- Services Bureau à distance de la classe Win32_TSGatewayServer, méthode d’exportation
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942890"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="88747-106">Méthode Export de la \_ classe TSGatewayServer Win32</span><span class="sxs-lookup"><span data-stu-id="88747-106">Export method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="88747-107">Retourne la configuration du serveur de passerelle Bureau à distance (passerelle Bureau à distance) sous la forme d’une chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="88747-107">Returns the Remote Desktop Gateway (RD Gateway) server configuration as an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="88747-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88747-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a><span data-ttu-id="88747-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88747-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88747-110">*ExportType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88747-110">*ExportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88747-111">Contenu à exporter.</span><span class="sxs-lookup"><span data-stu-id="88747-111">The content to export.</span></span> <span data-ttu-id="88747-112">Définissez le type d’exportation en définissant les bits correspondants dans le paramètre *ExportType* .</span><span class="sxs-lookup"><span data-stu-id="88747-112">Set the export type by setting the corresponding bits in the *ExportType* parameter.</span></span> <span data-ttu-id="88747-113">Vous pouvez définir plusieurs types d’exportation.</span><span class="sxs-lookup"><span data-stu-id="88747-113">You can set multiple export types.</span></span> <span data-ttu-id="88747-114">Par exemple, si le bit 0 est défini, Services Bureau à distance stratégies d’autorisation des connexions (RD Cap) seront exportées.</span><span class="sxs-lookup"><span data-stu-id="88747-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be exported.</span></span> <span data-ttu-id="88747-115">Si les deux bits 0 et 2 sont définis, les stratégies d’autorisation des ressources pour les services Bureau à distance et les Services Bureau à distance RD sont exportées.</span><span class="sxs-lookup"><span data-stu-id="88747-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be exported.</span></span>

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span data-ttu-id="88747-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Exporter toutes les majuscules** (1)</span><span class="sxs-lookup"><span data-stu-id="88747-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Export all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="88747-117">Exporter toutes les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="88747-117">Export all RD CAPs.</span></span>

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="88747-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Exporter tous les serveurs RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="88747-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Export all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="88747-119">Exportez une liste de tous les serveurs NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="88747-119">Export a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span data-ttu-id="88747-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Exporter tous les stratégies** (4)</span><span class="sxs-lookup"><span data-stu-id="88747-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Export all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="88747-121">Exporter tous les stratégies RD.</span><span class="sxs-lookup"><span data-stu-id="88747-121">Export all RD RAPs.</span></span>

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span data-ttu-id="88747-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Exporter tous les RGs** (8)</span><span class="sxs-lookup"><span data-stu-id="88747-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Export all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="88747-123">Exportez tous les groupes de ressources.</span><span class="sxs-lookup"><span data-stu-id="88747-123">Export all resource groups.</span></span>

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="88747-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Exporter tous les serveurs LoadBalancing** (16)</span><span class="sxs-lookup"><span data-stu-id="88747-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Export all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="88747-125">Exporter une liste de tous les serveurs d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="88747-125">Export a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="88747-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Exporter tous les paramètres du serveur** (32)</span><span class="sxs-lookup"><span data-stu-id="88747-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Export all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="88747-127">Exportez tous les paramètres de serveur liés à la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="88747-127">Export all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="88747-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Exporter toutes les stratégies de contrôle d’intégrité** (64)</span><span class="sxs-lookup"><span data-stu-id="88747-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Export all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="88747-129">Exporter toutes les stratégies de contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="88747-129">Export all health policies.</span></span>

<span data-ttu-id="88747-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 et Windows Server 2008 : \* \*</span><span class="sxs-lookup"><span data-stu-id="88747-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="88747-131">Cette valeur n’est pas prise en charge avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="88747-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="88747-132">*XmlString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="88747-132">*XmlString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88747-133">Chaîne du XML.</span><span class="sxs-lookup"><span data-stu-id="88747-133">The XML string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88747-134">Notes</span><span class="sxs-lookup"><span data-stu-id="88747-134">Remarks</span></span>

<span data-ttu-id="88747-135">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="88747-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="88747-136">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="88747-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="88747-137">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="88747-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="88747-138">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="88747-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="88747-139">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="88747-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="88747-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88747-140">Requirements</span></span>



| <span data-ttu-id="88747-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88747-141">Requirement</span></span> | <span data-ttu-id="88747-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="88747-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88747-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88747-143">Minimum supported client</span></span><br/> | <span data-ttu-id="88747-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="88747-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="88747-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88747-145">Minimum supported server</span></span><br/> | <span data-ttu-id="88747-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88747-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="88747-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="88747-147">Namespace</span></span><br/>                | <span data-ttu-id="88747-148">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="88747-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="88747-149">MOF</span><span class="sxs-lookup"><span data-stu-id="88747-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88747-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88747-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="88747-151">DLL</span><span class="sxs-lookup"><span data-stu-id="88747-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88747-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88747-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="88747-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88747-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88747-154">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="88747-154">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

