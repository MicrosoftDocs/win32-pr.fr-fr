---
title: Classe Win32_VirtualDesktopSession
description: Gère une session de bureau virtuel.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession de la classe Services Bureau à distance
- Win32_VirtualDesktopSession de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464463"
---
# <a name="win32_virtualdesktopsession-class"></a><span data-ttu-id="2c7b4-105">\_Classe VirtualDesktopSession Win32</span><span class="sxs-lookup"><span data-stu-id="2c7b4-105">Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="2c7b4-106">Gère une session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-106">Manages a virtual desktop session.</span></span>

<span data-ttu-id="2c7b4-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7b4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c7b4-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a><span data-ttu-id="2c7b4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2c7b4-109">Members</span></span>

<span data-ttu-id="2c7b4-110">La classe **Win32 \_ VirtualDesktopSession** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c7b4-110">The **Win32\_VirtualDesktopSession** class has these types of members:</span></span>

-   [<span data-ttu-id="2c7b4-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c7b4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2c7b4-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c7b4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2c7b4-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c7b4-113">Methods</span></span>

<span data-ttu-id="2c7b4-114">La classe **Win32 \_ VirtualDesktopSession** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-114">The **Win32\_VirtualDesktopSession** class has these methods.</span></span>



| <span data-ttu-id="2c7b4-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="2c7b4-115">Method</span></span>                                                         | <span data-ttu-id="2c7b4-116">Description</span><span class="sxs-lookup"><span data-stu-id="2c7b4-116">Description</span></span>                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="2c7b4-117">**Déconnecter**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-117">**Disconnect**</span></span>](disconnect-win32-virtualdesktopsession.md)   | <span data-ttu-id="2c7b4-118">Déconnecte la session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-118">Disconnects the virtual desktop session.</span></span><br/>                        |
| [<span data-ttu-id="2c7b4-119">**Fermeture**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-119">**Logoff**</span></span>](logoff-win32-virtualdesktopsession.md)           | <span data-ttu-id="2c7b4-120">Déconnecte l’utilisateur de la session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-120">Logs off the user from the virtual desktop session.</span></span><br/>             |
| [<span data-ttu-id="2c7b4-121">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-121">**SendMessage**</span></span>](sendmessage-win32-virtualdesktopsession.md) | <span data-ttu-id="2c7b4-122">Envoyer un message à l’utilisateur via la session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-122">Send a message to the user through the virtual desktop session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2c7b4-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c7b4-123">Properties</span></span>

<span data-ttu-id="2c7b4-124">La classe **Win32 \_ VirtualDesktopSession** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-124">The **Win32\_VirtualDesktopSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c7b4-125">**ClientMachineName**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-125">**ClientMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-128">Obtient le nom de l’ordinateur client qui est connecté à la session.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-128">Gets the name of the client machine that is connected to the session.</span></span>

</dd> <dt>

<span data-ttu-id="2c7b4-129">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-129">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-132">Obtient le nom de la collection de bureaux virtuels qui héberge l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-132">Gets the name of the virtual desktop collection that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2c7b4-133">**ConnectState**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-133">**ConnectState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-136">Obtient l’état de la connexion à la session.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-136">Gets the state of the connection to the session.</span></span>

</dd> <dt>

<span data-ttu-id="2c7b4-137">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-137">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-140">Obtient le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-140">Gets the domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="2c7b4-141">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-141">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-144">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c7b4-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-145">Obtient l’ID de la session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-145">Gets the ID of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="2c7b4-146">**UserName**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-146">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-149">Obtient le nom du compte d’utilisateur affecté à la session.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-149">Gets the name of the user account that is assigned to the session.</span></span>

</dd> <dt>

<span data-ttu-id="2c7b4-150">**VMHostName**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-150">**VMHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-153">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c7b4-153">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-154">Obtient le nom du serveur hôte de virtualisation Bureau à distance qui héberge l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-154">Gets the name of the Remote Desktop virtualization host server that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2c7b4-155">**VMName**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-155">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7b4-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7b4-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c7b4-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7b4-158">Obtient le nom de l’ordinateur virtuel affecté à la session.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-158">Gets the name of the virtual machine that is assigned to the session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c7b4-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c7b4-159">Requirements</span></span>



| <span data-ttu-id="2c7b4-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c7b4-160">Requirement</span></span> | <span data-ttu-id="2c7b4-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c7b4-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7b4-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c7b4-162">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7b4-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c7b4-163">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2c7b4-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c7b4-164">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7b4-165">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c7b4-165">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2c7b4-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c7b4-166">Namespace</span></span><br/>                | <span data-ttu-id="2c7b4-167">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="2c7b4-167">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2c7b4-168">MOF</span><span class="sxs-lookup"><span data-stu-id="2c7b4-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c7b4-169"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c7b4-169"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c7b4-170">DLL</span><span class="sxs-lookup"><span data-stu-id="2c7b4-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c7b4-171"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c7b4-171"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2c7b4-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c7b4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7b4-173">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="2c7b4-173">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

