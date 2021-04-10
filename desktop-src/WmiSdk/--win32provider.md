---
description: Enregistre des informations sur l’implémentation physique d’un fournisseur dans WMI. Les fournisseurs qui ne définissent pas la propriété HostingModel sont chargés, par défaut, pour s’exécuter dans un processus Wmiprvse.exe en tant que NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: Classe __Win32Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952870"
---
# <a name="__win32provider-class"></a><span data-ttu-id="ad500-104">\_\_Win32Provider, classe</span><span class="sxs-lookup"><span data-stu-id="ad500-104">\_\_Win32Provider class</span></span>

<span data-ttu-id="ad500-105">La classe système **\_ \_ Win32Provider** inscrit des informations sur l’implémentation physique d’un fournisseur dans WMI.</span><span class="sxs-lookup"><span data-stu-id="ad500-105">The **\_\_Win32Provider** system class registers information about the physical implementation of a provider in WMI.</span></span> <span data-ttu-id="ad500-106">Les fournisseurs qui ne définissent pas la propriété **HostingModel** sont chargés, par défaut, pour s’exécuter dans un processus Wmiprvse.exe en tant que **NetworkServiceHostOrSelfHost**.</span><span class="sxs-lookup"><span data-stu-id="ad500-106">Providers that do not set the **HostingModel** property are loaded, by default, to run in a Wmiprvse.exe process as **NetworkServiceHostOrSelfHost**.</span></span>

<span data-ttu-id="ad500-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ad500-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ad500-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ad500-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad500-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad500-109">Syntax</span></span>

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
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
};
```

## <a name="members"></a><span data-ttu-id="ad500-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ad500-110">Members</span></span>

<span data-ttu-id="ad500-111">La classe **\_ \_ Win32Provider** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ad500-111">The **\_\_Win32Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="ad500-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad500-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad500-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad500-113">Properties</span></span>

<span data-ttu-id="ad500-114">La classe **\_ \_ Win32Provider** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ad500-114">The **\_\_Win32Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad500-115">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="ad500-115">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ad500-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-118">Identificateur de classe utilisé par WMI pour déterminer s’il faut charger un fournisseur de haute performance dans le processus client ou le processus WMI.</span><span class="sxs-lookup"><span data-stu-id="ad500-118">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="ad500-119">Si le fournisseur et le client se trouvent sur le même ordinateur, WMI charge le fournisseur in-process sur le client en utilisant **ClientLoadableCLSID** comme identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="ad500-119">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="ad500-120">Lorsque le fournisseur et le client se trouvent sur des ordinateurs différents, WMI charge le fournisseur in-process dans le processus WMI.</span><span class="sxs-lookup"><span data-stu-id="ad500-120">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="ad500-121">WMI utilise également **ClientLoadableCLSID** pour prendre en charge les opérations d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="ad500-121">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="ad500-122">Pour plus d’informations, consultez [inscription d’un fournisseur de High-Performance.](registering-a-high-performance-provider.md)</span><span class="sxs-lookup"><span data-stu-id="ad500-122">For more information, see [Registering a High-Performance Provider.](registering-a-high-performance-provider.md)</span></span>

</dd> <dt>

<span data-ttu-id="ad500-123">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="ad500-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ad500-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-126">**GUID** qui représente l’identificateur de classe (**CLSID**) de l’objet com du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad500-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="ad500-127">Cet objet COM doit contenir une implémentation de l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="ad500-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-128">**Concurrency**</span><span class="sxs-lookup"><span data-stu-id="ad500-128">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad500-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-131">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-131">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-132">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="ad500-132">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ad500-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-135">Identifie l’ordinateur sur lequel démarrer le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad500-135">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="ad500-136">Si le fournisseur s’exécute sur l’ordinateur local, il a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ad500-136">If the provider runs on the local computer it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-137">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="ad500-137">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-140">Si la **valeur est true**, cette instance est activée et peut être utilisée pour effectuer les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="ad500-140">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-141">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="ad500-141">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ad500-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-144">Cette propriété est composée de valeurs des propriétés **HostingGroup** et **HostingSpecification** des [**\_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .</span><span class="sxs-lookup"><span data-stu-id="ad500-144">This property is composed of values from the [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** and **HostingSpecification** properties.</span></span> <span data-ttu-id="ad500-145">La valeur de cette propriété spécifie comment WMI charge le fournisseur et le compte de sécurité sous lequel il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="ad500-145">The value of this property specifies how WMI loads the provider and the security account it runs under.</span></span> <span data-ttu-id="ad500-146">Pour plus d’informations sur la définition de la propriété **HostingModel** , consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md) et [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ad500-146">For more information about setting the **HostingModel** property, see [Provider Hosting and Security](provider-hosting-and-security.md) and [Registering a Provider](registering-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad500-147">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="ad500-147">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-148">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad500-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-150">Réservé.</span><span class="sxs-lookup"><span data-stu-id="ad500-150">Reserved.</span></span> <span data-ttu-id="ad500-151">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="ad500-151">The default value is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ad500-152">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="ad500-152">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad500-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-155">Jeu d’indicateurs qui fournissent des informations sur la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="ad500-155">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="ad500-156">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="ad500-156">The default value is zero (0).</span></span>

<dt>

<span data-ttu-id="ad500-157">0</span><span class="sxs-lookup"><span data-stu-id="ad500-157">0</span></span>
</dt> <dd>

<span data-ttu-id="ad500-158">Toute l’initialisation de ce fournisseur doit être sérialisée.</span><span class="sxs-lookup"><span data-stu-id="ad500-158">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-159">1</span><span class="sxs-lookup"><span data-stu-id="ad500-159">1</span></span>
</dt> <dd>

<span data-ttu-id="ad500-160">Toutes les initialisations de ce fournisseur dans le même espace de noms doivent être sérialisées.</span><span class="sxs-lookup"><span data-stu-id="ad500-160">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-161">2</span><span class="sxs-lookup"><span data-stu-id="ad500-161">2</span></span>
</dt> <dd>

<span data-ttu-id="ad500-162">Aucune sérialisation d’initialisation n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ad500-162">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad500-163">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="ad500-163">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-164">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad500-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-166">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-167">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="ad500-167">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-168">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-170">TBD</span><span class="sxs-lookup"><span data-stu-id="ad500-170">TBD</span></span>

</dd> <dt>

<span data-ttu-id="ad500-171">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ad500-171">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ad500-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad500-174">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ad500-174">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ad500-175">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad500-175">The provider name.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-176">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="ad500-176">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-177">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad500-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-179">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-180">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="ad500-180">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-181">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-183">Si la **valeur est true**, le fournisseur est initialisé pour chaque paramètre régional lorsqu’un utilisateur se connecte à un même espace de noms plusieurs fois à l’aide de différents paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ad500-183">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="ad500-184">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ad500-184">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-185">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="ad500-185">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-186">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-188">Si la **valeur est true**, le fournisseur est initialisé une fois pour chaque utilisateur NT LAN Manager (NTLM) qui effectue des demandes au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad500-188">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="ad500-189">Si la **valeur est false** (valeur par défaut), le fournisseur est initialisé une fois pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ad500-189">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-190">**FCP**</span><span class="sxs-lookup"><span data-stu-id="ad500-190">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-191">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-193">Si la **valeur est true**, le fournisseur s’engage à préparer le déchargement en appelant [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur tous les points d’interface en attente lorsque WMI appelle la méthode de mise en **version** de son interface principale.</span><span class="sxs-lookup"><span data-stu-id="ad500-193">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="ad500-194">Les fournisseurs qui doivent conserver les clients de WMI après qu’ils ne fonctionnent pas comme les fournisseurs doivent définir **pure** sur **false**.</span><span class="sxs-lookup"><span data-stu-id="ad500-194">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="ad500-195">Le paramètre par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="ad500-195">The default setting is **TRUE**.</span></span> <span data-ttu-id="ad500-196">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ad500-196">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-197">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ad500-197">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ad500-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-199">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-200">Le descripteur de sécurité (SD) dans le langage SDDL (Security Descriptor Definition Language) qui détermine l’ensemble des utilisateurs qui peuvent appeler [**IWbemDecoupledRegistrar : Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) pour le fournisseur découplé.</span><span class="sxs-lookup"><span data-stu-id="ad500-200">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="ad500-201">Pour plus d’informations, consultez la rubrique [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language) dans la section sécurité de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ad500-201">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="ad500-202">Ce descripteur de sécurité est utilisé uniquement pour les fournisseurs découplés et n’affecte pas les autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="ad500-202">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="ad500-203">Pour plus d’informations, consultez [incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="ad500-203">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="ad500-204">WMI effectue des vérifications d’accès pour les fournisseurs découplés qui utilisent les interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="ad500-204">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](iwbemobjectsink.md) interfaces.</span></span> <span data-ttu-id="ad500-205">Si le descripteur de sécurité a la **valeur null**, seules les applications ou les services qui s’exécutent sous les comptes LocalSystem, NetworkService et LocalService peuvent exécuter un fournisseur découplé.</span><span class="sxs-lookup"><span data-stu-id="ad500-205">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="ad500-206">La chaîne suivante montre un fournisseur découplé qui doit être exécuté uniquement par des administrateurs intégrés.» O :BAG : BAD : (A ;; 0 x1 ;;; BA)»</span><span class="sxs-lookup"><span data-stu-id="ad500-206">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="ad500-207">Pour plus d’informations sur la définition de la propriété **SecurityDescriptor** , consultez maintenance de la [sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="ad500-207">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad500-208">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="ad500-208">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-209">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-210">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-211">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-212">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="ad500-212">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-213">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-215">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-216">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="ad500-216">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-217">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-218">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-219">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-219">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-220">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="ad500-220">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-221">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-222">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-223">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-223">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-224">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="ad500-224">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-225">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-227">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-227">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-228">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="ad500-228">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-229">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ad500-229">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-230">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-230">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-231">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad500-231">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad500-232">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="ad500-232">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-233">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad500-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-234">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-234">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-235">[Format de date et d’heure](date-and-time-format.md) qui spécifie la durée pendant laquelle WMI autorise le fournisseur à rester inactif avant d’être déchargé.</span><span class="sxs-lookup"><span data-stu-id="ad500-235">[Date and Time Format](date-and-time-format.md) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="ad500-236">En règle générale, les fournisseurs demandent que WMI n’attende pas plus de cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="ad500-236">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="ad500-237">Pour la version actuelle de WMI, la valeur de cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ad500-237">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="ad500-238">WMI décharge le fournisseur en fonction de la valeur du délai d’attente dans une classe interne de l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="ad500-238">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="ad500-239">Il est recommandé que les fournisseurs définissent **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="ad500-239">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="ad500-240">Pour plus d’informations, consultez [déchargement d’un fournisseur](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ad500-240">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad500-241">**Version**</span><span class="sxs-lookup"><span data-stu-id="ad500-241">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad500-242">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad500-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad500-243">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ad500-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad500-244">Version du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad500-244">Version of the provider.</span></span> <span data-ttu-id="ad500-245">Les versions prises en charge sont 1 et 2.</span><span class="sxs-lookup"><span data-stu-id="ad500-245">The supported versions are 1 and 2.</span></span> <span data-ttu-id="ad500-246">La version 2 renforce les contrôles de validité de toutes les inscriptions de propriété associées, en particulier la propriété [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="ad500-246">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad500-247">Notes</span><span class="sxs-lookup"><span data-stu-id="ad500-247">Remarks</span></span>

<span data-ttu-id="ad500-248">La classe **\_ \_ Win32Provider** est dérivée du [**\_ \_ fournisseur**](--provider.md).</span><span class="sxs-lookup"><span data-stu-id="ad500-248">The **\_\_Win32Provider** class is derived from [**\_\_Provider**](--provider.md).</span></span>

<span data-ttu-id="ad500-249">La plupart des fournisseurs peuvent accepter les valeurs par défaut de la propriété **InitializationReentrancy** .</span><span class="sxs-lookup"><span data-stu-id="ad500-249">Most providers can accept the default values for the **InitializationReentrancy** property.</span></span> <span data-ttu-id="ad500-250">Toutefois, si un fournisseur peut prendre en charge l’initialisation simultanée pour des utilisateurs distincts, cette propriété peut avoir la valeur 1 (un).</span><span class="sxs-lookup"><span data-stu-id="ad500-250">However, if a provider can support simultaneous initialization for separate users, this property can be set to 1 (one).</span></span> <span data-ttu-id="ad500-251">Si l’initialisation sérialisée est nécessaire, **InitializationReentrancy** reste 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ad500-251">If serialized initialization is necessary, **InitializationReentrancy** remains 0 (zero).</span></span> <span data-ttu-id="ad500-252">Dans les deux instances, **PerUserInitialization** a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="ad500-252">In both instances, **PerUserInitialization** is set to **TRUE**.</span></span>

<span data-ttu-id="ad500-253">Un fournisseur pur ou un fournisseur qui affecte à la propriété **pure** la **valeur true**, existe uniquement pour les demandes de service d’applications et WMI.</span><span class="sxs-lookup"><span data-stu-id="ad500-253">A pure provider or a provider that sets the **Pure** property to **TRUE**, exists only to service requests from applications and WMI.</span></span> <span data-ttu-id="ad500-254">La plupart des fournisseurs sont des fournisseurs purs.</span><span class="sxs-lookup"><span data-stu-id="ad500-254">Most providers are pure providers.</span></span> <span data-ttu-id="ad500-255">Un fournisseur non pur est l’exception.</span><span class="sxs-lookup"><span data-stu-id="ad500-255">A nonpure provider is the exception.</span></span> <span data-ttu-id="ad500-256">Les fournisseurs non purs effectuent la transition vers le rôle du client une fois qu’ils ont terminé de traiter les demandes.</span><span class="sxs-lookup"><span data-stu-id="ad500-256">Nonpure providers transition to the role of client after they complete servicing requests.</span></span>

<span data-ttu-id="ad500-257">Un fournisseur d’émission qui commence à émettre des requêtes et effectue des demandes de WMI une fois l’initialisation terminée est un exemple de fournisseur non pur.</span><span class="sxs-lookup"><span data-stu-id="ad500-257">An example of a nonpure provider is a push provider that starts to issue queries, and makes requests of WMI after it completes initialization.</span></span> <span data-ttu-id="ad500-258">Un fournisseur de notifications push n’a pas de responsabilités, sauf pour mettre à jour le référentiel CIM avec des données au moment de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="ad500-258">A push provider does not have responsibilities except to update the CIM repository with data at initialization time.</span></span> <span data-ttu-id="ad500-259">Après la mise à jour du référentiel, un fournisseur d’émission peut attendre le déchargement ou la transition vers le rôle de client.</span><span class="sxs-lookup"><span data-stu-id="ad500-259">After updating the repository, a push provider can wait to be unloaded, or transition to the role of client.</span></span> <span data-ttu-id="ad500-260">Le fournisseur push qui attend le déchargement est un fournisseur pur.</span><span class="sxs-lookup"><span data-stu-id="ad500-260">The push provider that waits to be unloaded is a pure provider.</span></span> <span data-ttu-id="ad500-261">Le fournisseur push qui participe aux activités des clients est non pur.</span><span class="sxs-lookup"><span data-stu-id="ad500-261">The push provider that participates in client activities is nonpure.</span></span>

<span data-ttu-id="ad500-262">WMI doit être en mesure de distinguer les fournisseurs purs des fournisseurs non purs afin qu’il puisse déterminer quand il est possible de s’arrêter en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="ad500-262">WMI must be able to distinguish pure providers from non-pure providers so that it can determine when it is safe to shut down.</span></span> <span data-ttu-id="ad500-263">WMI doit attendre la fin de toutes les opérations qui impliquent des fournisseurs non purs avant de pouvoir s’arrêter en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="ad500-263">WMI must wait for all operations that involve non-pure providers to complete before it can shut down safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad500-264">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad500-264">Requirements</span></span>



| <span data-ttu-id="ad500-265">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad500-265">Requirement</span></span> | <span data-ttu-id="ad500-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad500-266">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ad500-267">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad500-267">Minimum supported client</span></span><br/> | <span data-ttu-id="ad500-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad500-268">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ad500-269">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad500-269">Minimum supported server</span></span><br/> | <span data-ttu-id="ad500-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad500-270">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ad500-271">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad500-271">Namespace</span></span><br/>                | <span data-ttu-id="ad500-272">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="ad500-272">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ad500-273">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad500-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad500-274">**\_\_Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="ad500-274">**\_\_Provider**</span></span>](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[<span data-ttu-id="ad500-275">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="ad500-275">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ad500-276">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="ad500-276">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

