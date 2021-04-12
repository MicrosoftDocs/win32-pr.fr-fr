---
description: Permet de définir des limites sur l’utilisation des ressources système par le processus hôte.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: Classe __ProviderHostQuotaConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203161"
---
# <a name="__providerhostquotaconfiguration-class"></a><span data-ttu-id="13bf8-103">\_\_ProviderHostQuotaConfiguration, classe</span><span class="sxs-lookup"><span data-stu-id="13bf8-103">\_\_ProviderHostQuotaConfiguration class</span></span>

<span data-ttu-id="13bf8-104">La classe système **\_ \_ ProviderHostQuotaConfiguration** est une classe de configuration pour les processus des fournisseurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="13bf8-104">The **\_\_ProviderHostQuotaConfiguration** system class is a configuration class for host provider processes.</span></span> <span data-ttu-id="13bf8-105">Cette classe réside dans l’espace de noms racine et permet de définir des limites sur l’utilisation des ressources système par le processus hôte.</span><span class="sxs-lookup"><span data-stu-id="13bf8-105">This class resides in the root namespace and allows limits to be set on host process usage of system resources.</span></span>

<span data-ttu-id="13bf8-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="13bf8-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="13bf8-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="13bf8-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13bf8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13bf8-108">Syntax</span></span>

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a><span data-ttu-id="13bf8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="13bf8-109">Members</span></span>

<span data-ttu-id="13bf8-110">La classe **\_ \_ ProviderHostQuotaConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="13bf8-110">The **\_\_ProviderHostQuotaConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="13bf8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13bf8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13bf8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13bf8-112">Properties</span></span>

<span data-ttu-id="13bf8-113">La classe **\_ \_ ProviderHostQuotaConfiguration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="13bf8-113">The **\_\_ProviderHostQuotaConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13bf8-114">**HandlesPerHost**</span><span class="sxs-lookup"><span data-stu-id="13bf8-114">**HandlesPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bf8-115">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13bf8-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13bf8-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13bf8-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13bf8-117">Nombre de handles d’objets noyau que chaque hôte peut avoir.</span><span class="sxs-lookup"><span data-stu-id="13bf8-117">Number of kernel object handles each host can have.</span></span>

</dd> <dt>

<span data-ttu-id="13bf8-118">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="13bf8-118">**MemoryAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bf8-119">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13bf8-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13bf8-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13bf8-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13bf8-121">Quantité combinée de mémoire privée en octets qui peut être détenue par tous les ordinateurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="13bf8-121">Combined amount of private memory in bytes that can be held by all hosts.</span></span>

<span data-ttu-id="13bf8-122">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="13bf8-122">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="13bf8-123">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="13bf8-123">**MemoryPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bf8-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13bf8-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13bf8-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13bf8-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13bf8-126">Quantité de mémoire privée qui peut être détenue par chaque hôte.</span><span class="sxs-lookup"><span data-stu-id="13bf8-126">Amount of private memory that can be held by each host.</span></span>

<span data-ttu-id="13bf8-127">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="13bf8-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="13bf8-128">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="13bf8-128">**ProcessLimitAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bf8-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13bf8-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13bf8-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13bf8-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13bf8-131">Nombre total de processus hôtes qui peuvent s’exécuter simultanément.</span><span class="sxs-lookup"><span data-stu-id="13bf8-131">Total number of host processes that can be executing concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="13bf8-132">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="13bf8-132">**ThreadsPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bf8-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13bf8-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13bf8-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13bf8-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13bf8-135">Nombre de threads appartenant à un hôte.</span><span class="sxs-lookup"><span data-stu-id="13bf8-135">Number of threads owned by any one host.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13bf8-136">Notes</span><span class="sxs-lookup"><span data-stu-id="13bf8-136">Remarks</span></span>

<span data-ttu-id="13bf8-137">Les propriétés qui représentent des limites peuvent être modifiées, mais étant donné que la classe est un singleton, tous les hôtes du fournisseur partagent les mêmes limites.</span><span class="sxs-lookup"><span data-stu-id="13bf8-137">The properties that represent limits can be changed but because the class is a singleton, all the provider hosts share the same limits.</span></span>

<span data-ttu-id="13bf8-138">Les paramètres suivants sont utilisés lors de la configuration des limites de l’objet de tâche pour l’objet de travail hôte :</span><span class="sxs-lookup"><span data-stu-id="13bf8-138">The following parameters are used when configuring the job object limits for the host job object:</span></span>

-   <span data-ttu-id="13bf8-139">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="13bf8-139">**MemoryAllHosts**</span></span>
-   <span data-ttu-id="13bf8-140">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="13bf8-140">**MemoryPerHost**</span></span>
-   <span data-ttu-id="13bf8-141">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="13bf8-141">**ProcessLimitAllHosts**</span></span>
-   <span data-ttu-id="13bf8-142">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="13bf8-142">**ThreadsPerHost**</span></span>

<span data-ttu-id="13bf8-143">Le processus hôte interroge l’utilisation du handle et quitte le processus si le quota **HandlesPerHost** est violé.</span><span class="sxs-lookup"><span data-stu-id="13bf8-143">The host process polls handle usage and exits the process if the **HandlesPerHost** quota is violated.</span></span> <span data-ttu-id="13bf8-144">Les modifications apportées à ces valeurs prennent effet après le redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="13bf8-144">Changes to these values take effect after the computer is restarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bf8-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13bf8-145">Requirements</span></span>



| <span data-ttu-id="13bf8-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13bf8-146">Requirement</span></span> | <span data-ttu-id="13bf8-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="13bf8-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="13bf8-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13bf8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="13bf8-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13bf8-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="13bf8-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13bf8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="13bf8-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13bf8-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="13bf8-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13bf8-152">Namespace</span></span><br/>                | <span data-ttu-id="13bf8-153">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="13bf8-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="13bf8-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13bf8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13bf8-155">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="13bf8-155">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="13bf8-156">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="13bf8-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

