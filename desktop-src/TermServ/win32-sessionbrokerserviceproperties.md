---
title: Classe Win32_SessionBrokerServiceProperties
description: Définit la requête pour un service session Broker.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509377"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="472fa-105">\_Classe SessionBrokerServiceProperties Win32</span><span class="sxs-lookup"><span data-stu-id="472fa-105">Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="472fa-106">Définit la requête pour un service session Broker.</span><span class="sxs-lookup"><span data-stu-id="472fa-106">Defines the query for a session broker service.</span></span>

<span data-ttu-id="472fa-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="472fa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="472fa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="472fa-108">Syntax</span></span>

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a><span data-ttu-id="472fa-109">Membres</span><span class="sxs-lookup"><span data-stu-id="472fa-109">Members</span></span>

<span data-ttu-id="472fa-110">La classe **Win32 \_ SessionBrokerServiceProperties** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="472fa-110">The **Win32\_SessionBrokerServiceProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="472fa-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="472fa-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="472fa-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="472fa-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="472fa-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="472fa-113">Methods</span></span>

<span data-ttu-id="472fa-114">La classe **Win32 \_ SessionBrokerServiceProperties** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="472fa-114">The **Win32\_SessionBrokerServiceProperties** class has these methods.</span></span>



| <span data-ttu-id="472fa-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="472fa-115">Method</span></span>                                                                                                | <span data-ttu-id="472fa-116">Description</span><span class="sxs-lookup"><span data-stu-id="472fa-116">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="472fa-117">**DeleteSBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="472fa-117">**DeleteSBDbConnectionString**</span></span>](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | <span data-ttu-id="472fa-118">Supprime du registre les chaînes de connexion à la base de données (primaire et secondaire).</span><span class="sxs-lookup"><span data-stu-id="472fa-118">Deletes DB connection strings (primary and secondary) from the registry.</span></span><br/> <span data-ttu-id="472fa-119">**Windows server 2012 R2, Windows server 2012 et Windows server 2008 R2 :** Cette méthode n’est pas disponible avant Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="472fa-119">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/> |
| [<span data-ttu-id="472fa-120">**InstallBrokerDatabase**</span><span class="sxs-lookup"><span data-stu-id="472fa-120">**InstallBrokerDatabase**</span></span>](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | <span data-ttu-id="472fa-121">Installe la base de gestion du Service Broker pour les connexions Bureau à distance sur le SQL Server central</span><span class="sxs-lookup"><span data-stu-id="472fa-121">Installs RD Connection Broker DB on central SQL Server</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="472fa-122">**IsDbReachable**</span><span class="sxs-lookup"><span data-stu-id="472fa-122">**IsDbReachable**</span></span>](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | <span data-ttu-id="472fa-123">Vérifie si la base de l’accès est accessible</span><span class="sxs-lookup"><span data-stu-id="472fa-123">Checks if DB is reachable</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="472fa-124">**SetBrokerHAMode**</span><span class="sxs-lookup"><span data-stu-id="472fa-124">**SetBrokerHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | <span data-ttu-id="472fa-125">Migre les données de la base de données WID locale vers la nouvelle base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="472fa-125">Migrates data from local WID DB to the new SQL Server based DB.</span></span> <span data-ttu-id="472fa-126">Il configure également le serveur du Service Broker pour qu’il utilise le SQL Server central</span><span class="sxs-lookup"><span data-stu-id="472fa-126">It also configures the broker server to use the central SQL Server</span></span><br/>                                                                                        |
| [<span data-ttu-id="472fa-127">**SetBrokerNonHAMode**</span><span class="sxs-lookup"><span data-stu-id="472fa-127">**SetBrokerNonHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | <span data-ttu-id="472fa-128">Migre les données du SQL Server central vers la base de données locale.</span><span class="sxs-lookup"><span data-stu-id="472fa-128">Migrates data from central SQL Server to local DB.</span></span> <span data-ttu-id="472fa-129">Il configure également le serveur du Service Broker pour qu’il utilise la base de serveurs locale.</span><span class="sxs-lookup"><span data-stu-id="472fa-129">It also configures the broker server to use the local DB.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="472fa-130">**SetSBDbConnectionStrings**</span><span class="sxs-lookup"><span data-stu-id="472fa-130">**SetSBDbConnectionStrings**</span></span>](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | <span data-ttu-id="472fa-131">Enregistre les chaînes de connexion de la base de données (primaire et secondaire) dans le registre.</span><span class="sxs-lookup"><span data-stu-id="472fa-131">Saves DB connection strings (primary and secondary) in the registry.</span></span><br/> <span data-ttu-id="472fa-132">**Windows server 2012 R2, Windows server 2012 et Windows server 2008 R2 :** Cette méthode n’est pas disponible avant Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="472fa-132">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/>     |



 

### <a name="properties"></a><span data-ttu-id="472fa-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="472fa-133">Properties</span></span>

<span data-ttu-id="472fa-134">La classe **Win32 \_ SessionBrokerServiceProperties** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="472fa-134">The **Win32\_SessionBrokerServiceProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="472fa-135">**SBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="472fa-135">**SBDbConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="472fa-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="472fa-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="472fa-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="472fa-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="472fa-138">Chaîne de connexion à la base de données utilisée par le service session Broker.</span><span class="sxs-lookup"><span data-stu-id="472fa-138">Database connection string used by Session Broker service.</span></span>

<span data-ttu-id="472fa-139">**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="472fa-139">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="472fa-140">**SBDbSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="472fa-140">**SBDbSecondaryConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="472fa-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="472fa-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="472fa-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="472fa-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="472fa-143">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="472fa-143">Optional.</span></span> <span data-ttu-id="472fa-144">Chaîne de connexion de base de données secondaire, utilisée par le service session Broker pour prendre en charge l’expiration du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="472fa-144">Secondary database connection string, used by Session Broker service to support password expiration.</span></span>

<span data-ttu-id="472fa-145">**Windows server 2012 R2, Windows server 2012 et Windows server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="472fa-145">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This property is not available prior to Windows Server 2016</span></span>

</dd> <dt>

<span data-ttu-id="472fa-146">**SBNetworkName**</span><span class="sxs-lookup"><span data-stu-id="472fa-146">**SBNetworkName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="472fa-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="472fa-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="472fa-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="472fa-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="472fa-149">Nom de réseau utilisé par le service session Broker.</span><span class="sxs-lookup"><span data-stu-id="472fa-149">The network name used by the session broker service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="472fa-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="472fa-150">Requirements</span></span>



| <span data-ttu-id="472fa-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="472fa-151">Requirement</span></span> | <span data-ttu-id="472fa-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="472fa-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="472fa-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="472fa-153">Minimum supported client</span></span><br/> | <span data-ttu-id="472fa-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="472fa-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="472fa-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="472fa-155">Minimum supported server</span></span><br/> | <span data-ttu-id="472fa-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="472fa-156">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="472fa-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="472fa-157">Namespace</span></span><br/>                | <span data-ttu-id="472fa-158">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="472fa-158">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="472fa-159">MOF</span><span class="sxs-lookup"><span data-stu-id="472fa-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="472fa-160"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="472fa-160"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="472fa-161">DLL</span><span class="sxs-lookup"><span data-stu-id="472fa-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="472fa-162"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="472fa-162"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

