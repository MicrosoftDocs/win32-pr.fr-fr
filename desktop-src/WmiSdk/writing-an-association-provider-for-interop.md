---
description: Un fournisseur d’associations fournit un mécanisme permettant d’inscrire des profils et de les associer à des profils qui sont implémentés dans différents espaces de noms.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Écriture d’un fournisseur d’association pour l’interopérabilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106528585"
---
# <a name="writing-an-association-provider-for-interop"></a><span data-ttu-id="c061b-103">Écriture d’un fournisseur d’association pour l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="c061b-103">Writing an Association Provider for Interop</span></span>

<span data-ttu-id="c061b-104">Un fournisseur d’associations fournit un mécanisme permettant d’inscrire des profils et de les associer à des profils qui sont implémentés dans différents espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="c061b-104">An association provider provides a mechanism to register profiles and associate them with profiles that are implemented in different namespaces.</span></span>

<span data-ttu-id="c061b-105">Les fournisseurs d’associations sont utilisés pour exposer des profils standard, comme un profil d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="c061b-105">Association providers are used to expose standard profiles, like a power profile.</span></span> <span data-ttu-id="c061b-106">Pour ce faire, vous devez écrire un fournisseur d’association dans l’espace de noms racine/Interop qui expose des instances d’association en implémentant une classe dérivée de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c061b-106">This is accomplished by writing an association provider in the root/interop namespace that exposes association instances by implementing a class, which is derived from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span> <span data-ttu-id="c061b-107">Le fournisseur doit être inscrit à la fois dans la racine/l’interopérabilité et dans la racine/l' <implemented> espace de noms pour prendre en charge la traversée d’espaces de noms croisés.</span><span class="sxs-lookup"><span data-stu-id="c061b-107">The provider must be registered in both the root/interop and the root/<implemented> namespace to support cross namespace traversal.</span></span>

<span data-ttu-id="c061b-108">Windows Management Instrumentation (WMI) charge le fournisseur d’associations chaque fois qu’une requête d’association est exécutée dans l’espace de noms racine/Interop.</span><span class="sxs-lookup"><span data-stu-id="c061b-108">Windows Management Instrumentation (WMI) loads the association provider whenever an association query is run in the root/interop namespace.</span></span>

<span data-ttu-id="c061b-109">**Pour implémenter un fournisseur d’association pour l’interopérabilité**</span><span class="sxs-lookup"><span data-stu-id="c061b-109">**To implement an association provider for interop**</span></span>

1.  <span data-ttu-id="c061b-110">Dérivez une classe de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) et créez une instance statique de cette classe dérivée dans l' \\ espace de noms Interop racine.</span><span class="sxs-lookup"><span data-stu-id="c061b-110">Derive a class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and create a static instance of this derived class in the root\\interop namespace.</span></span> <span data-ttu-id="c061b-111">Au minimum, les propriétés suivantes doivent être propagées avec des valeurs valides :</span><span class="sxs-lookup"><span data-stu-id="c061b-111">At a minimum, the following properties must be propagated with valid values:</span></span>

    -   <span data-ttu-id="c061b-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c061b-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="c061b-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c061b-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="c061b-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c061b-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="c061b-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c061b-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span></span>

    <span data-ttu-id="c061b-116">Même si [**InstanceID**](/previous-versions//ee309375(v=vs.85)) définit de manière unique l’instance de **l' \_ RegisteredProfile CIM**, la combinaison de **RegisteredName**, **RegisteredOrganization** et **RegisteredVersion** doit identifier de façon unique le profil inscrit dans l’étendue de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="c061b-116">Even though [**InstanceID**](/previous-versions//ee309375(v=vs.85)) uniquely defines the instance of the **CIM\_RegisteredProfile**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="c061b-117">Pour plus d’informations sur les propriétés individuelles, voir [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c061b-117">For more information about the individual properties, see [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

    <span data-ttu-id="c061b-118">L’exemple de code suivant décrit la syntaxe pour la dérivation de la classe **ProcessProfile** à partir de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) et le remplissage de l’instance statique.</span><span class="sxs-lookup"><span data-stu-id="c061b-118">The following code example describes the syntax for deriving the **ProcessProfile** class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and populating the static instance.</span></span>

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > <span data-ttu-id="c061b-119">Pour les clients Windows, la propriété **RegisteredOrganization** doit avoir la valeur 1 et la propriété **OtherRegisteredOrganization** définie sur « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="c061b-119">For Windows clients, the **RegisteredOrganization** property must be set to 1 and the **OtherRegisteredOrganization** property set to "Microsoft".</span></span>

     

2.  <span data-ttu-id="c061b-120">Créez un fournisseur qui retourne les instances d’association des [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span><span class="sxs-lookup"><span data-stu-id="c061b-120">Create a provider that returns association instances of [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span></span> <span data-ttu-id="c061b-121">Il s’agit d’un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="c061b-121">This is a two-step process.</span></span>

    1.  <span data-ttu-id="c061b-122">Créez une classe dérivée de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans les espaces de noms Interop et implementation.</span><span class="sxs-lookup"><span data-stu-id="c061b-122">Create a class that is derived from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in both the interop and implementation namespaces.</span></span> <span data-ttu-id="c061b-123">Étant donné que le même profil peut être implémenté par des fournisseurs différents, le nom de la classe doit être unique.</span><span class="sxs-lookup"><span data-stu-id="c061b-123">Because the same profile can be implemented by different vendors, the name of the class should be unique.</span></span> <span data-ttu-id="c061b-124">La Convention d’affectation de noms recommandée est « <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ».</span><span class="sxs-lookup"><span data-stu-id="c061b-124">The recommended naming convention is "<Organization>\_<ProductName>\_<ClassName>\_<Version>".</span></span> <span data-ttu-id="c061b-125">La propriété **ConformantStandard** ou **propriété ManagedElement** doit spécifier le qualificateur **\_ targetNamespace de msft** contenant l’espace de noms auquel appartient cette classe.</span><span class="sxs-lookup"><span data-stu-id="c061b-125">Either the **ConformantStandard** or the **ManagedElement** property must specify the **MSFT\_TargetNamespace** qualifier that contains the namespace to which this class belongs.</span></span>

        <span data-ttu-id="c061b-126">L’exemple de code suivant décrit la syntaxe permettant de dériver \_ la \_ classe Microsoft process ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans l' \\ espace de noms Interop racine.</span><span class="sxs-lookup"><span data-stu-id="c061b-126">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\interop namespace.</span></span> <span data-ttu-id="c061b-127">Dans cet exemple, l' \_ élément géré par le processus Win32 fait référence à l' \\ espace de noms CIMV2 racine à l’aide du qualificateur **\_ targetNamespace de msft** .</span><span class="sxs-lookup"><span data-stu-id="c061b-127">In this example, the Win32\_Process managed element references the root\\cimv2 namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="c061b-128">L’exemple de code suivant décrit la syntaxe permettant de dériver \_ la \_ classe Microsoft process ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="c061b-128">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="c061b-129">Dans cet exemple, la norme [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conforme fait référence à l' \\ espace de noms Interop racine à l’aide du qualificateur **\_ targetNamespace de msft** .</span><span class="sxs-lookup"><span data-stu-id="c061b-129">In this example, the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conformant standard references the root\\interop namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="c061b-130">Si le **qualificateur \_ targetNamespace de msft** n’est pas spécifié sur la propriété qui fait référence à l’espace de noms implémenté, le filtre **ResultClass** de l’instruction « associateurs de » ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="c061b-130">If the **MSFT\_TargetNamespace** qualifier is not specified on the property that is referencing the implemented namespace, the **ResultClass** filter of "Associators of" statement will not work.</span></span> <span data-ttu-id="c061b-131">Par exemple, si le **qualificateur \_ targetNamespace msft** n’est pas spécifié, la ligne de commande Windows PowerShell suivante ne retourne pas d’objet : **obtenir-WmiObject-query "ASSOCIATORS of {ProcessProfile. InstanceId = 'Process'} WHERE ResultClass = 'Win32 \_ Process'**.</span><span class="sxs-lookup"><span data-stu-id="c061b-131">For example, if the **MSFT\_TargetNamespace** qualifier is not specified, the following Windows PowerShell command-line will not return an object: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32\_Process'"**.</span></span>

        <span data-ttu-id="c061b-132">Le **qualificateur \_ targetNamespace de msft** ne peut pas pointer vers un espace de noms sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c061b-132">The **MSFT\_TargetNamespace** qualifier cannot point to a namespace on a remote computer.</span></span> <span data-ttu-id="c061b-133">Par exemple, l’espace de noms suivant n’est pas pris en charge : msft \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ Interop racine).</span><span class="sxs-lookup"><span data-stu-id="c061b-133">For example, the following namespace is not supported: MSFT\_TargetNamespace(\\\\\\\\<RemoteMachine>\\\\root\\\\interop).</span></span>

    2.  <span data-ttu-id="c061b-134">Écrivez un fournisseur qui retourne des instances de la classe dérivée créée.</span><span class="sxs-lookup"><span data-stu-id="c061b-134">Write a provider that returns instances of the created derived class.</span></span> <span data-ttu-id="c061b-135">Pour plus d’informations, consultez [écriture d’un fournisseur d’instances](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c061b-135">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span> <span data-ttu-id="c061b-136">Lorsque vous accédez à des instances de plusieurs espaces de noms, vous devrez peut-être accéder aux niveaux de sécurité du client.</span><span class="sxs-lookup"><span data-stu-id="c061b-136">When you access cross-namespace instances, you might have to access the security levels for the client.</span></span> <span data-ttu-id="c061b-137">Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c061b-137">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

        <span data-ttu-id="c061b-138">Le fournisseur d’associations doit implémenter à la fois les méthodes [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) et [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="c061b-138">The association provider should implement both the [**IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) and [**IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span> <span data-ttu-id="c061b-139">L’implémentation de la méthode [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) est facultative.</span><span class="sxs-lookup"><span data-stu-id="c061b-139">Implementing the [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method is optional.</span></span> <span data-ttu-id="c061b-140">Étant donné que ce fournisseur est accessible à la fois à partir de l' \\ interopérabilité racine et des \\ <implemented> espaces de noms racine, il ne doit pas exister de dépendance explicite sur un espace de noms à l’intérieur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c061b-140">Because this provider can be accessed from both the root\\interop and the root\\<implemented> namespaces, there should not be an explicit dependency on a namespace inside the provider.</span></span>

3.  <span data-ttu-id="c061b-141">Inscrivez le fournisseur d’associations à la fois dans l' \\ interopérabilité racine et dans les \\ <implemented> espaces de noms racines.</span><span class="sxs-lookup"><span data-stu-id="c061b-141">Register the association provider in both the root\\interop and the root\\<implemented> namespaces.</span></span> <span data-ttu-id="c061b-142">Pour plus d’informations, consultez [inscription d’un fournisseur d’instances](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c061b-142">For more information, see [Registering an Instance Provider](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="c061b-143">L’exemple de code suivant décrit la syntaxe permettant d’inscrire le fournisseur d’associations dans l' \\ espace de noms Interop racine.</span><span class="sxs-lookup"><span data-stu-id="c061b-143">The following code example describes the syntax to register the association provider in the root\\interop namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    <span data-ttu-id="c061b-144">L’exemple de code suivant décrit la syntaxe permettant d’inscrire le fournisseur d’associations dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="c061b-144">The following code example describes the syntax to register the association provider in the root\\cimv2 namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  <span data-ttu-id="c061b-145">Placez le schéma pour le [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans l’espace de noms implémenté.</span><span class="sxs-lookup"><span data-stu-id="c061b-145">Place the schema for the [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) into the implemented namespace.</span></span> <span data-ttu-id="c061b-146">Pour les clients Windows, il s’agit du fichier Interop. MOF qui se trouve dans le dossier% SystemRoot% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="c061b-146">For Windows clients this is the interop.mof file that is located in the %systemroot%\\system32\\wbem folder.</span></span>
5.  <span data-ttu-id="c061b-147">Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c061b-147">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="c061b-148">WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c061b-148">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="c061b-149">La méthode [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) doit être implémentée d’une manière qui lui permet d’être appelée pour deux espaces de noms différents.</span><span class="sxs-lookup"><span data-stu-id="c061b-149">The [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method should be implemented in a way that allows it to be called for two different namespaces.</span></span> <span data-ttu-id="c061b-150">Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c061b-150">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c061b-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c061b-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c061b-152">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="c061b-152">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

<span data-ttu-id="c061b-153">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c061b-153">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c061b-154">Écriture d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="c061b-154">Writing an Instance Provider</span></span>](writing-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="c061b-155">Inscription d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="c061b-155">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

 
