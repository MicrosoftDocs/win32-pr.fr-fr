---
title: Classe Win32_TSGatewayServer
description: Utilisé pour les opérations spécifiques au serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer de la classe Services Bureau à distance
- Win32_TSGatewayServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465086"
---
# <a name="win32_tsgatewayserver-class"></a><span data-ttu-id="36186-105">\_Classe TSGatewayServer Win32</span><span class="sxs-lookup"><span data-stu-id="36186-105">Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="36186-106">Utilisé pour les opérations spécifiques au serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="36186-106">Used for Remote Desktop Gateway (RD Gateway) server-specific operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="36186-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36186-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a><span data-ttu-id="36186-108">Membres</span><span class="sxs-lookup"><span data-stu-id="36186-108">Members</span></span>

<span data-ttu-id="36186-109">La classe **Win32 \_ TSGatewayServer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36186-109">The **Win32\_TSGatewayServer** class has these types of members:</span></span>

-   [<span data-ttu-id="36186-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="36186-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36186-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="36186-111">Methods</span></span>

<span data-ttu-id="36186-112">La classe **Win32 \_ TSGatewayServer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="36186-112">The **Win32\_TSGatewayServer** class has these methods.</span></span>



| <span data-ttu-id="36186-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="36186-113">Method</span></span>                                                                                   | <span data-ttu-id="36186-114">Description</span><span class="sxs-lookup"><span data-stu-id="36186-114">Description</span></span>                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36186-115">**CreateSelfSignedCertificate**</span><span class="sxs-lookup"><span data-stu-id="36186-115">**CreateSelfSignedCertificate**</span></span>](createselfsignedcertificate-win32-tsgatewayserver.md) | <span data-ttu-id="36186-116">Crée un certificat auto-signé avec un nom d’objet donné et retourne le hachage de certificat en tant que paramètre « out ».</span><span class="sxs-lookup"><span data-stu-id="36186-116">Creates a self-signed certificate with a given subject name and returns the certificate hash as an "out" parameter.</span></span><br/> |
| [<span data-ttu-id="36186-117">**Exporter**</span><span class="sxs-lookup"><span data-stu-id="36186-117">**Export**</span></span>](export-win32-tsgatewayserver.md)                                           | <span data-ttu-id="36186-118">Retourne la configuration du serveur de passerelle Bureau à distance sous la forme d’une chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="36186-118">Returns the RD Gateway server configuration as an XML string.</span></span><br/>                                                       |
| [<span data-ttu-id="36186-119">**Importer**</span><span class="sxs-lookup"><span data-stu-id="36186-119">**Import**</span></span>](import-win32-tsgatewayserver.md)                                           | <span data-ttu-id="36186-120">Importe une configuration donnée sur le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="36186-120">Imports a given configuration to the RD Gateway server.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="36186-121">Notes</span><span class="sxs-lookup"><span data-stu-id="36186-121">Remarks</span></span>

<span data-ttu-id="36186-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="36186-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="36186-123">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="36186-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="36186-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="36186-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="36186-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="36186-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="36186-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36186-126">Requirements</span></span>



| <span data-ttu-id="36186-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36186-127">Requirement</span></span> | <span data-ttu-id="36186-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="36186-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="36186-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36186-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36186-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="36186-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="36186-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36186-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36186-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36186-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="36186-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36186-133">Namespace</span></span><br/>                | <span data-ttu-id="36186-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="36186-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="36186-135">MOF</span><span class="sxs-lookup"><span data-stu-id="36186-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36186-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36186-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="36186-137">DLL</span><span class="sxs-lookup"><span data-stu-id="36186-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36186-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36186-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



 

