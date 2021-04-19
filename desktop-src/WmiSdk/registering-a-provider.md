---
description: Avant d’implémenter votre fournisseur, vous devez d’abord inscrire votre fournisseur auprès de WMI. L’inscription du fournisseur définit le type du fournisseur et les classes que le fournisseur prend en charge. WMI ne peut accéder qu’aux fournisseurs inscrits.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Inscription d’un fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536735"
---
# <a name="registering-a-provider"></a><span data-ttu-id="72626-105">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="72626-105">Registering a Provider</span></span>

<span data-ttu-id="72626-106">Avant d’implémenter votre fournisseur, vous devez d’abord inscrire votre fournisseur auprès de WMI.</span><span class="sxs-lookup"><span data-stu-id="72626-106">Before implementing your provider, you should first register your provider with WMI.</span></span> <span data-ttu-id="72626-107">L’inscription du fournisseur définit le type du fournisseur et les classes que le fournisseur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="72626-107">Registering the provider defines the type of the provider and the classes that the provider supports.</span></span> <span data-ttu-id="72626-108">WMI ne peut accéder qu’aux fournisseurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="72626-108">WMI can only access registered providers.</span></span>

> [!Note]  
> <span data-ttu-id="72626-109">Pour plus d’informations sur l’inscription d’un fournisseur MI, consultez [procédure : inscrire un fournisseur mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="72626-109">For more information on registering an MI provider, see [How to: Register an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span></span>

 

<span data-ttu-id="72626-110">Vous pouvez écrire votre code de fournisseur avant d’inscrire le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-110">You can write your provider code before you register the provider.</span></span> <span data-ttu-id="72626-111">Toutefois, il est très difficile de déboguer un fournisseur qui n’est pas inscrit auprès de WMI.</span><span class="sxs-lookup"><span data-stu-id="72626-111">However, it is very difficult to debug a provider that is not registered with WMI.</span></span> <span data-ttu-id="72626-112">La détermination des interfaces pour votre fournisseur vous aide également à décrire l’objectif et la structure d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-112">Determining the interfaces for your provider also helps to outline the purpose and structure of a provider.</span></span> <span data-ttu-id="72626-113">Par conséquent, l’inscription de votre fournisseur vous aide à concevoir votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-113">Therefore, registering your provider helps you design your provider.</span></span>

<span data-ttu-id="72626-114">Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-114">Only administrators can register or delete a provider.</span></span>

<span data-ttu-id="72626-115">Un fournisseur doit être inscrit pour tous les différents types de fonctions fournisseur qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="72626-115">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="72626-116">Presque tous les fournisseurs fournissent des instances de classes qu’ils définissent, mais ils peuvent également fournir des données de propriété, des méthodes, des événements ou des classes.</span><span class="sxs-lookup"><span data-stu-id="72626-116">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="72626-117">Le fournisseur peut également être inscrit en tant que fournisseur de consommateur d’événements ou que fournisseur de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="72626-117">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span> <span data-ttu-id="72626-118">Il est recommandé de combiner toutes les fonctionnalités du fournisseur dans un fournisseur plutôt que d’avoir plusieurs fournisseurs distincts pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="72626-118">It is recommended that you combine all provider functionality in one provider rather than having many separate providers for each type.</span></span> <span data-ttu-id="72626-119">Par exemple, le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider), qui fournit des méthodes et des instances, et le [fournisseur de quota de disque](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), qui fournit des instances, des méthodes et des événements.</span><span class="sxs-lookup"><span data-stu-id="72626-119">An example is the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which provides methods and instances, and the [Disk Quota provider](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), which supplies instances, methods, and events.</span></span>

<span data-ttu-id="72626-120">Un fournisseur doit être inscrit pour tous les différents types de fonctions fournisseur qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="72626-120">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="72626-121">Presque tous les fournisseurs fournissent des instances de classes qu’ils définissent, mais ils peuvent également fournir des données de propriété, des méthodes, des événements ou des classes.</span><span class="sxs-lookup"><span data-stu-id="72626-121">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="72626-122">Le fournisseur peut également être inscrit en tant que fournisseur de consommateur d’événements ou que fournisseur de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="72626-122">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span>

<span data-ttu-id="72626-123">La même instance de [**\_ \_ Win32Provider**](--win32provider.md) est utilisée pour chaque type d’inscription :</span><span class="sxs-lookup"><span data-stu-id="72626-123">The same instance of [**\_\_Win32Provider**](--win32provider.md) is used for each type of registration:</span></span>

-   [<span data-ttu-id="72626-124">Inscription d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="72626-124">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
-   [<span data-ttu-id="72626-125">Inscription d’un fournisseur de classe</span><span class="sxs-lookup"><span data-stu-id="72626-125">Registering a Class Provider</span></span>](registering-a-class-provider.md)
-   [<span data-ttu-id="72626-126">Inscription d’un fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="72626-126">Registering a Method Provider</span></span>](registering-a-method-provider.md)
-   [<span data-ttu-id="72626-127">Inscription d’un fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="72626-127">Registering an Event Provider</span></span>](registering-an-event-provider.md)
-   [<span data-ttu-id="72626-128">Inscription d’un fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="72626-128">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
-   [<span data-ttu-id="72626-129">Création d’un fournisseur d’instances dans un fournisseur de High-Performance</span><span class="sxs-lookup"><span data-stu-id="72626-129">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a><span data-ttu-id="72626-130">Exemple : création et inscription d’une instance d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="72626-130">Example: Creating and Registering an Instance of a Provider</span></span>

<span data-ttu-id="72626-131">L’exemple suivant montre un fichier MOF qui crée et inscrit une instance du fournisseur de [Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) dans l’espace de \\ noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="72626-131">The following example shows a MOF file that creates and registers an instance of the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="72626-132">Il affecte l’alias $Reg au fournisseur afin d’éviter le nom de chemin d’accès long requis dans les inscriptions d’instance et de méthode.</span><span class="sxs-lookup"><span data-stu-id="72626-132">It assigns the alias $Reg to the provider to avoid the long pathname required in the instance and method registrations.</span></span> <span data-ttu-id="72626-133">Pour plus d’informations, consultez [création d’un alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="72626-133">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a><span data-ttu-id="72626-134">Exemple : inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="72626-134">Example: Registering a Provider</span></span>

<span data-ttu-id="72626-135">La procédure suivante décrit comment inscrire un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-135">The following procedure describes how to register a provider.</span></span>

<span data-ttu-id="72626-136">**Pour inscrire un fournisseur**</span><span class="sxs-lookup"><span data-stu-id="72626-136">**To register a provider**</span></span>

1.  <span data-ttu-id="72626-137">Inscrivez le fournisseur en tant que serveur COM.</span><span class="sxs-lookup"><span data-stu-id="72626-137">Register the provider as a COM server.</span></span>

    <span data-ttu-id="72626-138">Si nécessaire, vous devrez peut-être créer des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="72626-138">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="72626-139">Ce processus s’applique à tous les serveurs COM et n’est pas lié à WMI.</span><span class="sxs-lookup"><span data-stu-id="72626-139">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="72626-140">Pour plus d’informations, consultez la section COM dans la documentation du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="72626-140">For more information, see the COM section in the Microsoft Windows Software Development Kit (SDK) documentation.</span></span>

2.  <span data-ttu-id="72626-141">Créez un fichier MOF qui contient des instances de [**\_ \_ Win32Provider**](--win32provider.md) et une instance d’une classe dérivée directement ou indirectement de [**\_ \_ ProviderRegistration**](--providerregistration.md), telle que [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="72626-141">Create a MOF file that contains instances of [**\_\_Win32Provider**](--win32provider.md) and an instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), such as [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="72626-142">Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur en créant des instances de classes dérivées de **\_ \_ Win32Provider** ou [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="72626-142">Only administrators can register or delete a provider by creating instances of classes derived from **\_\_Win32Provider** or [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>
3.  <span data-ttu-id="72626-143">Définissez le [**HostingModel**](--win32provider.md) dans l’instance de **\_ \_ Win32Provider** en fonction des valeurs des [modèles d’hébergement](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="72626-143">Set the [**HostingModel**](--win32provider.md) in the instance of **\_\_Win32Provider** according to the values in [Hosting models](provider-hosting-and-security.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="72626-144">À moins que le fournisseur n’ait besoin des privilèges élevés du compte LocalSystem, la propriété [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) doit avoir la valeur « NetworkServiceHost ».</span><span class="sxs-lookup"><span data-stu-id="72626-144">Unless the provider requires the high privileges of the LocalSystem account, the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property should be set to "NetworkServiceHost".</span></span> <span data-ttu-id="72626-145">Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="72626-145">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

     

    <span data-ttu-id="72626-146">L’exemple MOF suivant tiré de l’exemple complet montre le code qui crée une instance de [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="72626-146">The following MOF example from the full example shows the code that creates an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  <span data-ttu-id="72626-147">Instance d’une classe dérivée directement ou indirectement de [**\_ \_ ProviderRegistration**](--providerregistration.md), pour décrire l’implémentation logique du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-147">An instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), to describe the logical implementation of the provider.</span></span> <span data-ttu-id="72626-148">Un fournisseur peut être inscrit pour plusieurs types de fonctionnalités différents.</span><span class="sxs-lookup"><span data-stu-id="72626-148">A provider can be registered for several different types of functionality.</span></span> <span data-ttu-id="72626-149">L’exemple ci-dessus inscrit RegProv en tant que fournisseur d’instance et de méthode.</span><span class="sxs-lookup"><span data-stu-id="72626-149">The example above registers RegProv as an instance and method provider.</span></span> <span data-ttu-id="72626-150">Toutefois, si RegProv prend en charge la fonctionnalité, il peut également être enregistré en tant que propriété ou fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="72626-150">But if RegProv supports the functionality, it could also be registered as a property or event provider.</span></span> <span data-ttu-id="72626-151">Le tableau suivant répertorie les classes qui inscrivent les fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-151">The following table lists the classes that register provider functionality.</span></span>

    

    | <span data-ttu-id="72626-152">Classes d’inscription du fournisseur</span><span class="sxs-lookup"><span data-stu-id="72626-152">Provider registration classes</span></span>                                                        | <span data-ttu-id="72626-153">Description</span><span class="sxs-lookup"><span data-stu-id="72626-153">Description</span></span>                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [<span data-ttu-id="72626-154">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="72626-154">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)           | <span data-ttu-id="72626-155">Inscrit un [fournisseur d’instances](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="72626-155">Registers an [instance provider](registering-an-instance-provider.md).</span></span>             |
    | [<span data-ttu-id="72626-156">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="72626-156">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)                 | <span data-ttu-id="72626-157">Inscrit un [fournisseur d’événements](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="72626-157">Registers an [event provider](registering-an-event-provider.md).</span></span>                   |
    | [<span data-ttu-id="72626-158">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="72626-158">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md) | <span data-ttu-id="72626-159">Inscrit un [fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="72626-159">Registers an [event consumer provider](registering-an-event-consumer-provider.md).</span></span> |
    | [<span data-ttu-id="72626-160">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="72626-160">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)               | <span data-ttu-id="72626-161">Inscrit un [fournisseur de méthode](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="72626-161">Registers a [method provider](registering-an-event-consumer-provider.md).</span></span>          |
    | [<span data-ttu-id="72626-162">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="72626-162">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)           | <span data-ttu-id="72626-163">Inscrit un [fournisseur de propriétés](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="72626-163">Registers a [property provider](registering-a-property-provider.md).</span></span>               |

    

     

5.  <span data-ttu-id="72626-164">Placez le fichier MOF dans un répertoire permanent.</span><span class="sxs-lookup"><span data-stu-id="72626-164">Place the MOF file into a permanent directory.</span></span>

    <span data-ttu-id="72626-165">En règle générale, vous devez placer le fichier dans le répertoire d’installation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72626-165">Typically, you should place the file in the installation directory of the provider.</span></span>

6.  <span data-ttu-id="72626-166">Compilez le fichier MOF à l’aide de [mofcomp](mofcomp.md) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="72626-166">Compile the MOF file using [mofcomp](mofcomp.md) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="72626-167">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="72626-167">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

    <span data-ttu-id="72626-168">**Windows 8 et Windows Server 2012 :** Lors de l’installation des fournisseurs, [**mofcomp**](mofcomp.md) et l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) traitent les \[ \] \[ qualificateurs Key et static \] comme true s’ils sont présents, indépendamment de leurs valeurs réelles.</span><span class="sxs-lookup"><span data-stu-id="72626-168">**Windows 8 and Windows Server 2012:** When installing providers, both [**mofcomp**](mofcomp.md) and the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface treat the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="72626-169">D’autres qualificateurs sont considérés comme false s’ils sont présents, mais ne sont pas explicitement définis sur true.</span><span class="sxs-lookup"><span data-stu-id="72626-169">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72626-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72626-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72626-171">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="72626-171">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="72626-172">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="72626-172">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="72626-173">Sécurisation de votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="72626-173">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
