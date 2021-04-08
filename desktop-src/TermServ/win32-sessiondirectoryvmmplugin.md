---
title: Classe Win32_SessionDirectoryVMMPlugin
description: Représente un plug-in Virtual Machine Manager (VMM) inscrit auprès d’un service session Broker.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941809"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="70fb8-105">\_Classe SessionDirectoryVMMPlugin Win32</span><span class="sxs-lookup"><span data-stu-id="70fb8-105">Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="70fb8-106">Représente un plug-in Virtual Machine Manager (VMM) inscrit auprès d’un service session Broker.</span><span class="sxs-lookup"><span data-stu-id="70fb8-106">Represents a virtual machine manager (VMM) plug-in registered with a session broker.</span></span>

<span data-ttu-id="70fb8-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="70fb8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70fb8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70fb8-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="70fb8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="70fb8-109">Members</span></span>

<span data-ttu-id="70fb8-110">La classe **Win32 \_ SessionDirectoryVMMPlugin** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70fb8-110">The **Win32\_SessionDirectoryVMMPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="70fb8-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70fb8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="70fb8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70fb8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70fb8-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70fb8-113">Methods</span></span>

<span data-ttu-id="70fb8-114">La classe **Win32 \_ SessionDirectoryVMMPlugin** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="70fb8-114">The **Win32\_SessionDirectoryVMMPlugin** class has these methods.</span></span>



| <span data-ttu-id="70fb8-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="70fb8-115">Method</span></span>                                                                             | <span data-ttu-id="70fb8-116">Description</span><span class="sxs-lookup"><span data-stu-id="70fb8-116">Description</span></span>                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="70fb8-117">**GetCurrentVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="70fb8-117">**GetCurrentVMMPlugin**</span></span>](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="70fb8-118">Obtient le plug-in avec la priorité la plus élevée qui est activé.</span><span class="sxs-lookup"><span data-stu-id="70fb8-118">Gets the highest priority plug-in that is enabled.</span></span><br/> |
| [<span data-ttu-id="70fb8-119">**RegisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="70fb8-119">**RegisterVMMPlugin**</span></span>](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | <span data-ttu-id="70fb8-120">Inscrit un nouveau plug-in VMM.</span><span class="sxs-lookup"><span data-stu-id="70fb8-120">Registers a new VMM plug-in.</span></span><br/>                       |
| [<span data-ttu-id="70fb8-121">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="70fb8-121">**SetEnabled**</span></span>](setenabled-win32-sessiondirectoryvmmplugin.md)                   | <span data-ttu-id="70fb8-122">Active ou désactive le plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-122">Enables or disables the plug-in.</span></span><br/>                   |
| [<span data-ttu-id="70fb8-123">**SetName**</span><span class="sxs-lookup"><span data-stu-id="70fb8-123">**SetName**</span></span>](setname-win32-sessiondirectoryvmmplugin.md)                         | <span data-ttu-id="70fb8-124">Définit le nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-124">Sets the name of the plug-in.</span></span><br/>                      |
| [<span data-ttu-id="70fb8-125">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="70fb8-125">**SetPriority**</span></span>](setpriority-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="70fb8-126">Définit la priorité du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-126">Sets the priority of the plug-in.</span></span><br/>                  |
| [<span data-ttu-id="70fb8-127">**SetProvider**</span><span class="sxs-lookup"><span data-stu-id="70fb8-127">**SetProvider**</span></span>](setprovider-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="70fb8-128">Définit le nom du fournisseur du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-128">Sets the provider name of the plug-in.</span></span><br/>             |
| [<span data-ttu-id="70fb8-129">**SetServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="70fb8-129">**SetServiceLocation**</span></span>](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | <span data-ttu-id="70fb8-130">Définit l’emplacement du service du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-130">Sets the service location of the plug-in.</span></span><br/>          |
| [<span data-ttu-id="70fb8-131">**UnregisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="70fb8-131">**UnregisterVMMPlugin**</span></span>](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="70fb8-132">Annule l’inscription du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-132">Unregisters the plug-in.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="70fb8-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70fb8-133">Properties</span></span>

<span data-ttu-id="70fb8-134">La classe **Win32 \_ SessionDirectoryVMMPlugin** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="70fb8-134">The **Win32\_SessionDirectoryVMMPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70fb8-135">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="70fb8-135">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70fb8-136">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70fb8-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70fb8-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70fb8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70fb8-138">Indique si le plug-in est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="70fb8-138">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="70fb8-139">**True** si le plug-in est activé ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="70fb8-139">**True** if the plug-in is enabled or **false** otherwise.</span></span> <span data-ttu-id="70fb8-140">Le plug-in est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="70fb8-140">The plug-in is disabled by default.</span></span>

</dd> <dt>

<span data-ttu-id="70fb8-141">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="70fb8-141">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70fb8-142">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="70fb8-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="70fb8-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70fb8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70fb8-144">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70fb8-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="70fb8-145">Priorité du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-145">The priority of the plug-in.</span></span> <span data-ttu-id="70fb8-146">Plus la valeur est élevée, plus la priorité du plug-in est élevée.</span><span class="sxs-lookup"><span data-stu-id="70fb8-146">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="70fb8-147">La priorité est égale à zéro par défaut.</span><span class="sxs-lookup"><span data-stu-id="70fb8-147">The priority is zero by default.</span></span>

</dd> <dt>

<span data-ttu-id="70fb8-148">**sClassID**</span><span class="sxs-lookup"><span data-stu-id="70fb8-148">**sClassID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70fb8-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70fb8-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70fb8-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70fb8-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70fb8-151">Identificateur de classe du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-151">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="70fb8-152">**sName**</span><span class="sxs-lookup"><span data-stu-id="70fb8-152">**sName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70fb8-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70fb8-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70fb8-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70fb8-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70fb8-155">Nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="70fb8-155">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="70fb8-156">**sProvider**</span><span class="sxs-lookup"><span data-stu-id="70fb8-156">**sProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70fb8-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70fb8-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70fb8-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70fb8-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70fb8-159">Nom du fournisseur de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="70fb8-159">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="70fb8-160">**sServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="70fb8-160">**sServiceLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70fb8-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70fb8-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70fb8-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70fb8-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70fb8-163">Emplacement du service que le plug-in doit contacter.</span><span class="sxs-lookup"><span data-stu-id="70fb8-163">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70fb8-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70fb8-164">Requirements</span></span>



| <span data-ttu-id="70fb8-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70fb8-165">Requirement</span></span> | <span data-ttu-id="70fb8-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="70fb8-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70fb8-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70fb8-167">Minimum supported client</span></span><br/> | <span data-ttu-id="70fb8-168">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="70fb8-168">None supported</span></span><br/>                                                              |
| <span data-ttu-id="70fb8-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70fb8-169">Minimum supported server</span></span><br/> | <span data-ttu-id="70fb8-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="70fb8-170">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="70fb8-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="70fb8-171">Namespace</span></span><br/>                | <span data-ttu-id="70fb8-172">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="70fb8-172">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="70fb8-173">MOF</span><span class="sxs-lookup"><span data-stu-id="70fb8-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70fb8-174"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70fb8-174"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="70fb8-175">DLL</span><span class="sxs-lookup"><span data-stu-id="70fb8-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70fb8-176"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70fb8-176"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

