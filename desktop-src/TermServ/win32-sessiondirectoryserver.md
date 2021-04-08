---
title: Classe Win32_SessionDirectoryServer
description: Fournit des propriétés pour afficher les propriétés d’un serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer de la classe Services Bureau à distance
- Win32_SessionDirectoryServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941985"
---
# <a name="win32_sessiondirectoryserver-class"></a><span data-ttu-id="ab127-105">\_Classe SessionDirectoryServer Win32</span><span class="sxs-lookup"><span data-stu-id="ab127-105">Win32\_SessionDirectoryServer class</span></span>

<span data-ttu-id="ab127-106">Fournit des propriétés pour afficher les propriétés d’un serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="ab127-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) server.</span></span>

> [!Note]  
> <span data-ttu-id="ab127-107">Dans Windows Server 2008 R2, le nom de session Broker TS (session Broker TS) a été modifié en service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ab127-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="ab127-108">Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="ab127-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ab127-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab127-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a><span data-ttu-id="ab127-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ab127-110">Members</span></span>

<span data-ttu-id="ab127-111">La classe **Win32 \_ SessionDirectoryServer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ab127-111">The **Win32\_SessionDirectoryServer** class has these types of members:</span></span>

-   [<span data-ttu-id="ab127-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab127-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab127-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab127-113">Properties</span></span>

<span data-ttu-id="ab127-114">La classe **Win32 \_ SessionDirectoryServer** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ab127-114">The **Win32\_SessionDirectoryServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab127-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="ab127-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab127-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab127-118">Nom de la batterie de serveurs qui comprend le serveur.</span><span class="sxs-lookup"><span data-stu-id="ab127-118">Name of the farm that includes the server.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-119">**LoadIndicator**</span><span class="sxs-lookup"><span data-stu-id="ab127-119">**LoadIndicator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab127-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab127-122">Nombre relatif qui représente la charge du serveur hôte de session Bureau à distance lorsque l’algorithme d’équilibrage de charge par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ab127-122">A relative number that represents the RD Session Host server load when the default load-balancing algorithm is used.</span></span> <span data-ttu-id="ab127-123">La valeur de la propriété *LoadIndicator* est basée sur le nombre de sessions, le nombre de demandes de redirection en attente et la valeur de poids du serveur.</span><span class="sxs-lookup"><span data-stu-id="ab127-123">The *LoadIndicator* property value is based on the number of sessions, the number of pending redirection requests, and the server weight value.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-124">**NumberOfSessions**</span><span class="sxs-lookup"><span data-stu-id="ab127-124">**NumberOfSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab127-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab127-127">Nombre de sessions sur le serveur du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ab127-127">Number of sessions in the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-128">**NumPendRedir**</span><span class="sxs-lookup"><span data-stu-id="ab127-128">**NumPendRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab127-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab127-131">Nombre de demandes de redirection en attente.</span><span class="sxs-lookup"><span data-stu-id="ab127-131">Number of pending redirection requests.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-132">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="ab127-132">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab127-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab127-135">Adresse IP du serveur du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ab127-135">IP address of the RD Connection Broker server.</span></span> <span data-ttu-id="ab127-136">Si le serveur est configuré pour les adresses IPv4 et IPv6, il contient l’adresse IPv4.</span><span class="sxs-lookup"><span data-stu-id="ab127-136">If the server is configured for both IPv4 and IPv6 addresses, this will contain the IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-137">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="ab127-137">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab127-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab127-140">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab127-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ab127-141">Nom du serveur du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ab127-141">Name of the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-142">**ServerWeight**</span><span class="sxs-lookup"><span data-stu-id="ab127-142">**ServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab127-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab127-145">Valeur de poids du serveur, utilisée dans l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="ab127-145">Server weight value, used in load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-146">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="ab127-146">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab127-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab127-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab127-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab127-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab127-149">Paramètre de mode de session unique du serveur du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ab127-149">Single session mode setting of the RD Connection Broker server.</span></span>

<dt>

<span data-ttu-id="ab127-150">0</span><span class="sxs-lookup"><span data-stu-id="ab127-150">0</span></span>
</dt> <dd>

<span data-ttu-id="ab127-151">La batterie de serveurs n’est pas en mode de session unique.</span><span class="sxs-lookup"><span data-stu-id="ab127-151">The farm is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="ab127-152">1</span><span class="sxs-lookup"><span data-stu-id="ab127-152">1</span></span>
</dt> <dd>

<span data-ttu-id="ab127-153">La batterie de serveurs de est en mode de session unique.</span><span class="sxs-lookup"><span data-stu-id="ab127-153">The farm in is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab127-154">Notes</span><span class="sxs-lookup"><span data-stu-id="ab127-154">Remarks</span></span>

<span data-ttu-id="ab127-155">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ab127-155">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ab127-156">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ab127-156">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ab127-157">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ab127-157">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ab127-158">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ab127-158">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab127-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab127-159">Requirements</span></span>



| <span data-ttu-id="ab127-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab127-160">Requirement</span></span> | <span data-ttu-id="ab127-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab127-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab127-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab127-162">Minimum supported client</span></span><br/> | <span data-ttu-id="ab127-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab127-163">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ab127-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab127-164">Minimum supported server</span></span><br/> | <span data-ttu-id="ab127-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab127-165">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ab127-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ab127-166">Namespace</span></span><br/>                | <span data-ttu-id="ab127-167">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ab127-167">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="ab127-168">MOF</span><span class="sxs-lookup"><span data-stu-id="ab127-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab127-169"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab127-169"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab127-170">DLL</span><span class="sxs-lookup"><span data-stu-id="ab127-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab127-171"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab127-171"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab127-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab127-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab127-173">**\_SessionDirectoryCluster Win32**</span><span class="sxs-lookup"><span data-stu-id="ab127-173">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="ab127-174">**\_SessionDirectorySession Win32**</span><span class="sxs-lookup"><span data-stu-id="ab127-174">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

