---
title: Méthode CheckStatus de la classe Win32_TSGatewayConnection
description: Vérifie l’état d’une connexion de serveur de passerelle Bureau à distance (passerelle Bureau à distance) à un autre ordinateur et détermine si l’ordinateur cible est configuré pour l’équilibrage de charge.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CheckStatus
- Services Bureau à distance de la méthode CheckStatus, classe Win32_TSGatewayConnection
- Win32_TSGatewayConnection de la classe Services Bureau à distance, méthode CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511743"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="db239-106">Méthode CheckStatus de la \_ classe Win32 TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="db239-106">CheckStatus method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="db239-107">Vérifie l’état d’une connexion de serveur de passerelle Bureau à distance (passerelle Bureau à distance) à un autre ordinateur et détermine si l’ordinateur cible est configuré pour l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="db239-107">Checks the status of a Remote Desktop Gateway (RD Gateway) server connection to another computer, and determines whether the target computer is configured for load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="db239-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db239-108">Syntax</span></span>


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a><span data-ttu-id="db239-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db239-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db239-110">*Nom du serveur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db239-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db239-111">Nom du serveur de passerelle Bureau à distance source à partir duquel la connexion est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="db239-111">The name of the source RD Gateway server from which the connection is checked.</span></span>

</dd> <dt>

<span data-ttu-id="db239-112">*EndpointName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db239-112">*EndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db239-113">Nom du serveur cible (point de terminaison) sur lequel l’accès est vérifié à partir du serveur source.</span><span class="sxs-lookup"><span data-stu-id="db239-113">The name of the target server (the endpoint) to which access is checked from the source server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db239-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db239-114">Return value</span></span>

<span data-ttu-id="db239-115">Cette méthode retourne les valeurs de retour possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="db239-115">This method returns the following possible return values.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="db239-116">0</span><span class="sxs-lookup"><span data-stu-id="db239-116">0</span></span>

<span data-ttu-id="db239-117">L’état de la connexion est OK.</span><span class="sxs-lookup"><span data-stu-id="db239-117">The connection status is OK.</span></span> <span data-ttu-id="db239-118">Le point de terminaison est accessible et configuré pour l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="db239-118">The endpoint is reachable and is configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db239-119">1</span><span class="sxs-lookup"><span data-stu-id="db239-119">1</span></span>

<span data-ttu-id="db239-120">L’état de la connexion est inconnu.</span><span class="sxs-lookup"><span data-stu-id="db239-120">The connection status is unknown.</span></span> <span data-ttu-id="db239-121">Probablement, une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="db239-121">Most likely, an exception occurred.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db239-122">0x80075c34</span><span class="sxs-lookup"><span data-stu-id="db239-122">0x80075c34</span></span>

<span data-ttu-id="db239-123">Le point de terminaison n’est pas accessible ou n’est pas configuré pour l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="db239-123">The endpoint is either not reachable, or it is not configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db239-124">0x80075c32</span><span class="sxs-lookup"><span data-stu-id="db239-124">0x80075c32</span></span>

<span data-ttu-id="db239-125">Une erreur d’État s’est produite.</span><span class="sxs-lookup"><span data-stu-id="db239-125">A status error occurred.</span></span> <span data-ttu-id="db239-126">Le point de terminaison est accessible, mais le service d’équilibrage de charge RPC/HTTP (RPCHTTPLBS) n’est pas démarré sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="db239-126">The endpoint is reachable, but the RPC/HTTP Load Balancing Service (RPCHTTPLBS) service is not started on the target computer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db239-127">Notes</span><span class="sxs-lookup"><span data-stu-id="db239-127">Remarks</span></span>

<span data-ttu-id="db239-128">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="db239-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="db239-129">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="db239-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="db239-130">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="db239-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="db239-131">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="db239-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="db239-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db239-132">Requirements</span></span>



| <span data-ttu-id="db239-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db239-133">Requirement</span></span> | <span data-ttu-id="db239-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="db239-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db239-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db239-135">Minimum supported client</span></span><br/> | <span data-ttu-id="db239-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="db239-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="db239-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db239-137">Minimum supported server</span></span><br/> | <span data-ttu-id="db239-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db239-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="db239-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="db239-139">Namespace</span></span><br/>                | <span data-ttu-id="db239-140">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="db239-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="db239-141">MOF</span><span class="sxs-lookup"><span data-stu-id="db239-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db239-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db239-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="db239-143">DLL</span><span class="sxs-lookup"><span data-stu-id="db239-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db239-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db239-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="db239-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db239-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db239-146">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="db239-146">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

