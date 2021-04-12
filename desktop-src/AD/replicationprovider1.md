---
title: ReplicationProvider1, classe
description: Classe de base pour l’instance du fournisseur.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory de la classe ReplicationProvider1
- Active Directory de la classe ReplicationProvider1, Description
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032766"
---
# <a name="replicationprovider1-class"></a><span data-ttu-id="80049-105">ReplicationProvider1, classe</span><span class="sxs-lookup"><span data-stu-id="80049-105">ReplicationProvider1 class</span></span>

<span data-ttu-id="80049-106">Classe de base pour l’instance du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80049-106">The base class for the provider instance.</span></span>

<span data-ttu-id="80049-107">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="80049-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80049-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80049-108">Syntax</span></span>

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
  string   HostingModel;
};
```

## <a name="members"></a><span data-ttu-id="80049-109">Membres</span><span class="sxs-lookup"><span data-stu-id="80049-109">Members</span></span>

<span data-ttu-id="80049-110">La classe **ReplicationProvider1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80049-110">The **ReplicationProvider1** class has these types of members:</span></span>

-   [<span data-ttu-id="80049-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80049-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80049-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80049-112">Properties</span></span>

<span data-ttu-id="80049-113">La classe **ReplicationProvider1** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="80049-113">The **ReplicationProvider1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80049-114">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="80049-114">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80049-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80049-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-117">Identificateur de classe utilisé par WMI pour déterminer s’il faut charger un fournisseur de haute performance dans le processus client ou le processus WMI.</span><span class="sxs-lookup"><span data-stu-id="80049-117">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="80049-118">Si le fournisseur et le client se trouvent sur le même ordinateur, WMI charge le fournisseur in-process sur le client en utilisant **ClientLoadableCLSID** comme identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="80049-118">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="80049-119">Lorsque le fournisseur et le client se trouvent sur des ordinateurs différents, WMI charge le fournisseur in-process dans le processus WMI.</span><span class="sxs-lookup"><span data-stu-id="80049-119">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="80049-120">WMI utilise également **ClientLoadableCLSID** pour prendre en charge les opérations d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="80049-120">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="80049-121">Pour plus d’informations, consultez [inscription d’un fournisseur de High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span><span class="sxs-lookup"><span data-stu-id="80049-121">For more information, see [Registering a High-Performance Provider.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span></span>

<span data-ttu-id="80049-122">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-122">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-123">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="80049-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80049-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80049-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-126">**GUID** qui représente l’identificateur de classe (**CLSID**) de l’objet com du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80049-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="80049-127">Cet objet COM doit contenir une implémentation de l’interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="80049-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

<span data-ttu-id="80049-128">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-128">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-129">**Concurrency**</span><span class="sxs-lookup"><span data-stu-id="80049-129">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-130">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80049-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80049-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-132">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-132">Not used.</span></span>

<span data-ttu-id="80049-133">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-133">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-134">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="80049-134">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80049-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80049-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-137">Identifie l’ordinateur sur lequel démarrer le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80049-137">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="80049-138">Si le fournisseur s’exécute sur l’ordinateur local, il a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="80049-138">If the provider runs on the local computer it is **NULL**.</span></span>

<span data-ttu-id="80049-139">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-139">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-140">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="80049-140">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-141">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-143">Si la **valeur est true**, cette instance est activée et peut être utilisée pour effectuer les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="80049-143">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

<span data-ttu-id="80049-144">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-144">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-145">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="80049-145">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80049-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80049-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80049-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80049-148">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span><span class="sxs-lookup"><span data-stu-id="80049-148">Qualifiers: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span></span>
</dt> </dl>

<span data-ttu-id="80049-149">Contient le modèle d’hébergement du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80049-149">Contains the hosting model of the provider.</span></span>

</dd> <dt>

<span data-ttu-id="80049-150">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="80049-150">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-151">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80049-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80049-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-153">Réservé.</span><span class="sxs-lookup"><span data-stu-id="80049-153">Reserved.</span></span> <span data-ttu-id="80049-154">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="80049-154">The default value is zero (0).</span></span>

<span data-ttu-id="80049-155">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-155">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-156">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="80049-156">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-157">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80049-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80049-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-159">Jeu d’indicateurs qui fournissent des informations sur la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="80049-159">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="80049-160">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="80049-160">The default value is zero (0).</span></span>

<span data-ttu-id="80049-161">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-161">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="80049-162"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="80049-162"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="80049-163">Toute l’initialisation de ce fournisseur doit être sérialisée.</span><span class="sxs-lookup"><span data-stu-id="80049-163">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="80049-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="80049-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="80049-165">Toutes les initialisations de ce fournisseur dans le même espace de noms doivent être sérialisées.</span><span class="sxs-lookup"><span data-stu-id="80049-165">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="80049-166"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="80049-166"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="80049-167">Aucune sérialisation d’initialisation n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="80049-167">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80049-168">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="80049-168">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-169">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80049-169">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80049-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-171">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-171">Not used.</span></span>

<span data-ttu-id="80049-172">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-172">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-173">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="80049-173">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-174">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-176">**Windows Server 2003 :** Cette propriété est désactivée.</span><span class="sxs-lookup"><span data-stu-id="80049-176">**Windows Server 2003:** This property is disabled.</span></span>

<span data-ttu-id="80049-177">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-177">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-178">**Nom**</span><span class="sxs-lookup"><span data-stu-id="80049-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80049-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80049-180">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80049-181">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="80049-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="80049-182">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80049-182">The provider name.</span></span>

<span data-ttu-id="80049-183">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-183">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-184">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="80049-184">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-185">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80049-185">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80049-186">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-187">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-187">Not used.</span></span>

<span data-ttu-id="80049-188">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-188">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-189">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="80049-189">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-190">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-191">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-192">Si la **valeur est true**, le fournisseur est initialisé pour chaque paramètre régional lorsqu’un utilisateur se connecte à un même espace de noms plusieurs fois à l’aide de différents paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="80049-192">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="80049-193">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="80049-193">The default value is **FALSE**.</span></span>

<span data-ttu-id="80049-194">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-194">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-195">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="80049-195">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-197">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-198">Si la **valeur est true**, le fournisseur est initialisé une fois pour chaque utilisateur NT LAN Manager (NTLM) qui effectue des demandes au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80049-198">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="80049-199">Si la **valeur est false** (valeur par défaut), le fournisseur est initialisé une fois pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="80049-199">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

<span data-ttu-id="80049-200">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-200">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-201">**FCP**</span><span class="sxs-lookup"><span data-stu-id="80049-201">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-202">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-203">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-203">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-204">Si la **valeur est true**, le fournisseur s’engage à préparer le déchargement en appelant [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur tous les points d’interface en attente lorsque WMI appelle la méthode de mise en **version** de son interface principale.</span><span class="sxs-lookup"><span data-stu-id="80049-204">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="80049-205">Les fournisseurs qui doivent conserver les clients de WMI après qu’ils ne fonctionnent pas comme les fournisseurs doivent définir **pure** sur **false**.</span><span class="sxs-lookup"><span data-stu-id="80049-205">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="80049-206">Le paramètre par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="80049-206">The default setting is **TRUE**.</span></span> <span data-ttu-id="80049-207">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="80049-207">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="80049-208">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-208">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-209">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="80049-209">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80049-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80049-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-212">Le descripteur de sécurité (SD) dans le langage SDDL (Security Descriptor Definition Language) qui détermine l’ensemble des utilisateurs qui peuvent appeler [**IWbemDecoupledRegistrar : Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) pour le fournisseur découplé.</span><span class="sxs-lookup"><span data-stu-id="80049-212">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="80049-213">Pour plus d’informations, consultez la rubrique [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language) dans la section sécurité de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="80049-213">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="80049-214">Ce descripteur de sécurité est utilisé uniquement pour les fournisseurs découplés et n’affecte pas les autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="80049-214">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="80049-215">Pour plus d’informations, consultez [incorporation d’un fournisseur dans une application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span><span class="sxs-lookup"><span data-stu-id="80049-215">For more information, see [Incorporating a Provider in an Application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span></span>

<span data-ttu-id="80049-216">WMI effectue des vérifications d’accès pour les fournisseurs découplés qui utilisent les interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="80049-216">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) interfaces.</span></span> <span data-ttu-id="80049-217">Si le descripteur de sécurité a la **valeur null**, seules les applications ou les services qui s’exécutent sous les comptes LocalSystem, NetworkService et LocalService peuvent exécuter un fournisseur découplé.</span><span class="sxs-lookup"><span data-stu-id="80049-217">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="80049-218">La chaîne suivante montre un fournisseur découplé qui doit être exécuté uniquement par des administrateurs intégrés.» O :BAG : BAD : (A ;; 0 x1 ;;; BA)»</span><span class="sxs-lookup"><span data-stu-id="80049-218">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="80049-219">Pour plus d’informations sur la définition de la propriété **SecurityDescriptor** , consultez maintenance de la [sécurité WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).</span><span class="sxs-lookup"><span data-stu-id="80049-219">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).</span></span>

<span data-ttu-id="80049-220">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-220">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-221">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="80049-221">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-222">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-224">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-224">Not used.</span></span>

<span data-ttu-id="80049-225">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-225">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-226">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="80049-226">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-227">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-228">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-229">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-229">Not used.</span></span>

<span data-ttu-id="80049-230">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-230">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-231">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="80049-231">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-232">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-233">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-233">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-234">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-234">Not used.</span></span>

<span data-ttu-id="80049-235">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-235">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-236">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="80049-236">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-237">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-238">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-239">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-239">Not used.</span></span>

<span data-ttu-id="80049-240">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-240">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-241">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="80049-241">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-242">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-243">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-244">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-244">Not used.</span></span>

<span data-ttu-id="80049-245">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-245">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-246">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="80049-246">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-247">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80049-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80049-248">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-249">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="80049-249">Not used.</span></span>

<span data-ttu-id="80049-250">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-250">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-251">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="80049-251">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-252">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80049-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80049-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-254">[Format de date et d’heure](/windows/desktop/WmiSdk/date-and-time-format) qui spécifie la durée pendant laquelle WMI autorise le fournisseur à rester inactif avant d’être déchargé.</span><span class="sxs-lookup"><span data-stu-id="80049-254">[Date and Time Format](/windows/desktop/WmiSdk/date-and-time-format) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="80049-255">En règle générale, les fournisseurs demandent que WMI n’attende pas plus de cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="80049-255">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="80049-256">Pour la version actuelle de WMI, la valeur de cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="80049-256">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="80049-257">WMI décharge le fournisseur en fonction de la valeur du délai d’attente dans une classe interne de l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="80049-257">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="80049-258">Il est recommandé que les fournisseurs définissent **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="80049-258">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="80049-259">Pour plus d’informations, consultez [déchargement d’un fournisseur](/windows/desktop/WmiSdk/unloading-a-provider).</span><span class="sxs-lookup"><span data-stu-id="80049-259">For more information, see [Unloading a Provider](/windows/desktop/WmiSdk/unloading-a-provider).</span></span>

<span data-ttu-id="80049-260">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-260">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="80049-261">**Version**</span><span class="sxs-lookup"><span data-stu-id="80049-261">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80049-262">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80049-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80049-263">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80049-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80049-264">Version du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80049-264">Version of the provider.</span></span> <span data-ttu-id="80049-265">Les versions prises en charge sont 1 et 2.</span><span class="sxs-lookup"><span data-stu-id="80049-265">The supported versions are 1 and 2.</span></span> <span data-ttu-id="80049-266">La version 2 renforce les contrôles de validité de toutes les inscriptions de propriété associées, en particulier la propriété [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .</span><span class="sxs-lookup"><span data-stu-id="80049-266">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) property.</span></span>

<span data-ttu-id="80049-267">Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="80049-267">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80049-268">Notes</span><span class="sxs-lookup"><span data-stu-id="80049-268">Remarks</span></span>

<span data-ttu-id="80049-269">Une instance de cette classe représente le fournisseur WMI pour les services domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="80049-269">An instance of this class represents the WMI provider for Active Directory Domain services.</span></span> <span data-ttu-id="80049-270">Ces paramètres par défaut sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="80049-270">The defaults are as follows:</span></span>

-   <span data-ttu-id="80049-271">Name = « ReplProv1 »</span><span class="sxs-lookup"><span data-stu-id="80049-271">Name = "ReplProv1"</span></span>
-   <span data-ttu-id="80049-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span><span class="sxs-lookup"><span data-stu-id="80049-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span></span>
-   <span data-ttu-id="80049-273">HostingModel = « NetworkServiceHost »</span><span class="sxs-lookup"><span data-stu-id="80049-273">HostingModel = "NetworkServiceHost"</span></span>

## <a name="requirements"></a><span data-ttu-id="80049-274">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80049-274">Requirements</span></span>



| <span data-ttu-id="80049-275">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80049-275">Requirement</span></span> | <span data-ttu-id="80049-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="80049-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80049-277">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80049-277">Minimum supported client</span></span><br/> | <span data-ttu-id="80049-278">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="80049-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="80049-279">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80049-279">Minimum supported server</span></span><br/> | <span data-ttu-id="80049-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80049-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80049-281">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80049-281">Namespace</span></span><br/>                | <span data-ttu-id="80049-282">\\MicrosoftActiveDirectory racine</span><span class="sxs-lookup"><span data-stu-id="80049-282">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="80049-283">MOF</span><span class="sxs-lookup"><span data-stu-id="80049-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80049-284"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80049-284"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="80049-285">DLL</span><span class="sxs-lookup"><span data-stu-id="80049-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80049-286"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80049-286"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80049-287">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80049-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80049-288">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="80049-288">**\_\_Win32Provider**</span></span>](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

