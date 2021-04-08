---
title: Classe Win32_SessionBrokerTargetEvent
description: Représente une modification apportée à une cible session Broker.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent de la classe Services Bureau à distance
- Win32_SessionBrokerTargetEvent de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740701"
---
# <a name="win32_sessionbrokertargetevent-class"></a><span data-ttu-id="e0072-105">\_Classe SessionBrokerTargetEvent Win32</span><span class="sxs-lookup"><span data-stu-id="e0072-105">Win32\_SessionBrokerTargetEvent class</span></span>

<span data-ttu-id="e0072-106">Représente une modification apportée à une cible session Broker.</span><span class="sxs-lookup"><span data-stu-id="e0072-106">Represents a change to a session broker target.</span></span>

<span data-ttu-id="e0072-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e0072-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0072-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0072-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="e0072-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e0072-109">Members</span></span>

<span data-ttu-id="e0072-110">La classe **Win32 \_ SessionBrokerTargetEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e0072-110">The **Win32\_SessionBrokerTargetEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e0072-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0072-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0072-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0072-112">Properties</span></span>

<span data-ttu-id="e0072-113">La classe **Win32 \_ SessionBrokerTargetEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e0072-113">The **Win32\_SessionBrokerTargetEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0072-114">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="e0072-114">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-115">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0072-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0072-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-117">Spécifie la modification qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e0072-117">Specifies the change that occurred.</span></span> <span data-ttu-id="e0072-118">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0072-118">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="e0072-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e0072-119">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e0072-120">Le type de modification n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="e0072-120">The type of change is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="e0072-121">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="e0072-121">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="e0072-122">L’adresse IP externe a changé.</span><span class="sxs-lookup"><span data-stu-id="e0072-122">The external IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e0072-123">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="e0072-123">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="e0072-124">L’adresse IP interne a changé.</span><span class="sxs-lookup"><span data-stu-id="e0072-124">The internal IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e0072-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="e0072-125">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="e0072-126">La cible a été jointe.</span><span class="sxs-lookup"><span data-stu-id="e0072-126">The target was joined.</span></span>

</dd> <dt>

<span data-ttu-id="e0072-127">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="e0072-127">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="e0072-128">La cible a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="e0072-128">The target was removed.</span></span>

</dd> <dt>

<span data-ttu-id="e0072-129">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="e0072-129">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="e0072-130">L’état de la cible a changé.</span><span class="sxs-lookup"><span data-stu-id="e0072-130">The state of the target has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e0072-131">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="e0072-131">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="e0072-132">La cible est inactive.</span><span class="sxs-lookup"><span data-stu-id="e0072-132">The target is idle.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0072-133">**Environment**</span><span class="sxs-lookup"><span data-stu-id="e0072-133">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0072-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0072-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-136">Nom d'environnement.</span><span class="sxs-lookup"><span data-stu-id="e0072-136">The environment name.</span></span> <span data-ttu-id="e0072-137">Dans le cas d’une machine virtuelle (VM) cible, il peut s’agir du nom d’hôte de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e0072-137">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

<span data-ttu-id="e0072-138">**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0072-138">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="e0072-139">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="e0072-139">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0072-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0072-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-142">Nom de la batterie à laquelle la cible appartient.</span><span class="sxs-lookup"><span data-stu-id="e0072-142">The name of the farm the target belongs to.</span></span>

<span data-ttu-id="e0072-143">**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0072-143">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="e0072-144">**Uniques**</span><span class="sxs-lookup"><span data-stu-id="e0072-144">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0072-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0072-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-147">GUID de la cible.</span><span class="sxs-lookup"><span data-stu-id="e0072-147">The GUID of the target.</span></span>

<span data-ttu-id="e0072-148">**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0072-148">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="e0072-149">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="e0072-149">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0072-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0072-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-152">Nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="e0072-152">The name of the plug-in.</span></span>

<span data-ttu-id="e0072-153">**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0072-153">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="e0072-154">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="e0072-154">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-155">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="e0072-155">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e0072-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-157">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="e0072-157">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e0072-158">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="e0072-158">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="e0072-159">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="e0072-159">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="e0072-160">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="e0072-160">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0072-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0072-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-163">Nom de la cible.</span><span class="sxs-lookup"><span data-stu-id="e0072-163">The name of the target.</span></span>

<span data-ttu-id="e0072-164">**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0072-164">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="e0072-165">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="e0072-165">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0072-166">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e0072-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e0072-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0072-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0072-168">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="e0072-168">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e0072-169">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="e0072-169">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e0072-170">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="e0072-170">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e0072-171">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="e0072-171">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="e0072-172">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e0072-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0072-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0072-173">Requirements</span></span>



| <span data-ttu-id="e0072-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0072-174">Requirement</span></span> | <span data-ttu-id="e0072-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0072-175">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0072-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0072-176">Minimum supported client</span></span><br/> | <span data-ttu-id="e0072-177">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0072-177">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e0072-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0072-178">Minimum supported server</span></span><br/> | <span data-ttu-id="e0072-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0072-179">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e0072-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e0072-180">Namespace</span></span><br/>                | <span data-ttu-id="e0072-181">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e0072-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="e0072-182">MOF</span><span class="sxs-lookup"><span data-stu-id="e0072-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0072-183"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0072-183"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0072-184">DLL</span><span class="sxs-lookup"><span data-stu-id="e0072-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0072-185"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0072-185"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

