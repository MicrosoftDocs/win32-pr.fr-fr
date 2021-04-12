---
title: Classe Win32_SessionDirectorySession
description: Fournit des propriétés pour afficher les propriétés d’une session Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession de la classe Services Bureau à distance
- Win32_SessionDirectorySession de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384148"
---
# <a name="win32_sessiondirectorysession-class"></a><span data-ttu-id="c2e1e-105">\_Classe SessionDirectorySession Win32</span><span class="sxs-lookup"><span data-stu-id="c2e1e-105">Win32\_SessionDirectorySession class</span></span>

<span data-ttu-id="c2e1e-106">Fournit des propriétés pour afficher les propriétés d’une session Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="c2e1e-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) session.</span></span>

> [!Note]  
> <span data-ttu-id="c2e1e-107">Dans Windows Server 2008 R2, le nom de session Broker TS (session Broker TS) a été modifié en service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="c2e1e-108">Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c2e1e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2e1e-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a><span data-ttu-id="c2e1e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c2e1e-110">Members</span></span>

<span data-ttu-id="c2e1e-111">La classe **Win32 \_ SessionDirectorySession** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c2e1e-111">The **Win32\_SessionDirectorySession** class has these types of members:</span></span>

-   [<span data-ttu-id="c2e1e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c2e1e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2e1e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c2e1e-113">Properties</span></span>

<span data-ttu-id="c2e1e-114">La classe **Win32 \_ SessionDirectorySession** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-114">The **Win32\_SessionDirectorySession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2e1e-115">**ApplicationType**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-115">**ApplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-118">L’application a démarré avec cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-118">Application started with this session.</span></span> <span data-ttu-id="c2e1e-119">C’est le même que la propriété **StartProgram** de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="c2e1e-119">This is the same as the **StartProgram** property of [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-120">**La**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-120">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-121">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-123">Profondeur de couleur de la session, mesurée en bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-123">Color depth of the session, measured in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-124">**CreateTime**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-124">**CreateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-125">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-125">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-127">Date et heure de création de la session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-127">Date and time the session was created.</span></span> <span data-ttu-id="c2e1e-128">Cette valeur n’est pas réinitialisée lorsqu’une session est déconnectée et reconnectée.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-128">This value is not reset when a session is disconnected and reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-129">**DisconnectTime**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-129">**DisconnectTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-130">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-130">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-132">Date et heure auxquelles la session a été déconnectée (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="c2e1e-132">Date and time the session was disconnected (if applicable).</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-133">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-133">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-136">Nom de domaine de l’utilisateur connecté à cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-136">Domain name of the user logged on to this session.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-137">**ResolutionHeight**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-137">**ResolutionHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-140">Hauteur de la session, en pixels, pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-140">Height of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-141">**ResolutionWidth**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-141">**ResolutionWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-144">Largeur de la session, en pixels, pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-144">Width of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-145">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-145">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-148">Adresse IP du serveur du Service Broker pour les connexions Bureau à distance pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-148">IP address of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-149">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-149">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2e1e-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-153">Nom du serveur du Service Broker pour les connexions Bureau à distance pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-153">Name of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-154">**IDsession**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-154">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-157">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2e1e-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-158">ID de session pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-158">Session ID for this session.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-159">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-159">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-162">État de cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-162">State of this session.</span></span>

<dt>

<span data-ttu-id="c2e1e-163">0</span><span class="sxs-lookup"><span data-stu-id="c2e1e-163">0</span></span>
</dt> <dd>

<span data-ttu-id="c2e1e-164">La session est active.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-164">The session is active.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-165">1</span><span class="sxs-lookup"><span data-stu-id="c2e1e-165">1</span></span>
</dt> <dd>

<span data-ttu-id="c2e1e-166">La session est déconnectée.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-166">The session is disconnected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c2e1e-167">**TSProtocol**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-167">**TSProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-170">Protocole pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-170">Protocol for this session.</span></span>

<dt>

<span data-ttu-id="c2e1e-171">0</span><span class="sxs-lookup"><span data-stu-id="c2e1e-171">0</span></span>
</dt> <dd>

<span data-ttu-id="c2e1e-172">Cette session s’exécute sur une console physique.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-172">This session is running on a physical console.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-173">1</span><span class="sxs-lookup"><span data-stu-id="c2e1e-173">1</span></span>
</dt> <dd>

<span data-ttu-id="c2e1e-174">Un protocole tiers propriétaire est utilisé pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-174">A proprietary third-party protocol is used for this session.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1e-175">2</span><span class="sxs-lookup"><span data-stu-id="c2e1e-175">2</span></span>
</dt> <dd>

<span data-ttu-id="c2e1e-176">Protocole RDP (Remote Desktop Protocol) (RDP) est utilisé pour cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-176">Remote Desktop Protocol (RDP) is used for this session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c2e1e-177">**UserName**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-177">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e1e-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2e1e-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2e1e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e1e-180">Nom d’utilisateur de l’utilisateur connecté à cette session.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-180">User name of the user logged on to this session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2e1e-181">Notes</span><span class="sxs-lookup"><span data-stu-id="c2e1e-181">Remarks</span></span>

<span data-ttu-id="c2e1e-182">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c2e1e-182">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c2e1e-183">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-183">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c2e1e-184">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-184">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c2e1e-185">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c2e1e-185">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e1e-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2e1e-186">Requirements</span></span>



| <span data-ttu-id="c2e1e-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2e1e-187">Requirement</span></span> | <span data-ttu-id="c2e1e-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2e1e-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e1e-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2e1e-189">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e1e-190">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2e1e-190">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c2e1e-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2e1e-191">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e1e-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2e1e-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c2e1e-193">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c2e1e-193">Namespace</span></span><br/>                | <span data-ttu-id="c2e1e-194">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c2e1e-194">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="c2e1e-195">MOF</span><span class="sxs-lookup"><span data-stu-id="c2e1e-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2e1e-196"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2e1e-196"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2e1e-197">DLL</span><span class="sxs-lookup"><span data-stu-id="c2e1e-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2e1e-198"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2e1e-198"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e1e-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2e1e-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e1e-200">**\_SessionDirectoryCluster Win32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-200">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="c2e1e-201">**\_SessionDirectoryServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c2e1e-201">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> </dl>

 

