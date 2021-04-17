---
description: La méthode la plus courante de mise à jour d’une instance de classe WMI consiste à mettre à jour l’intégralité de l’instance à la fois.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Mise à jour d’une instance entière
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203953"
---
# <a name="updating-an-entire-instance"></a><span data-ttu-id="e8616-103">Mise à jour d’une instance entière</span><span class="sxs-lookup"><span data-stu-id="e8616-103">Updating an Entire Instance</span></span>

<span data-ttu-id="e8616-104">La méthode la plus courante de mise à jour d’une instance de classe WMI consiste à mettre à jour l’intégralité de l’instance à la fois.</span><span class="sxs-lookup"><span data-stu-id="e8616-104">The most common means of updating a WMI class instance is to update the entire instance at once.</span></span> <span data-ttu-id="e8616-105">En mettant à jour une instance entière, WMI n’a pas besoin d’analyser l’instance dans des propriétés individuelles et de les envoyer à votre application.</span><span class="sxs-lookup"><span data-stu-id="e8616-105">By updating an entire instance, WMI does not have to parse the instance into individual properties and send them to your application.</span></span> <span data-ttu-id="e8616-106">Au lieu de cela, WMI peut simplement vous envoyer l’instance entière.</span><span class="sxs-lookup"><span data-stu-id="e8616-106">Instead, WMI can simply send you the entire instance.</span></span> <span data-ttu-id="e8616-107">Lorsque vous avez terminé, WMI peut ensuite copier l’intégralité de votre instance modifiée sur l’instance d’origine.</span><span class="sxs-lookup"><span data-stu-id="e8616-107">When you finish, WMI can then copy your entire changed instance over the original instance.</span></span>

<span data-ttu-id="e8616-108">La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8616-108">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

<span data-ttu-id="e8616-109">**Pour modifier ou mettre à jour une instance à l’aide de PowerShell**</span><span class="sxs-lookup"><span data-stu-id="e8616-109">**To modify or update an instance using PowerShell**</span></span>

1.  <span data-ttu-id="e8616-110">Récupérez une copie locale de l’objet à l’aide d’un appel à la fonction « obtenir-WmiObject ».</span><span class="sxs-lookup"><span data-stu-id="e8616-110">Retrieve a local copy of the object with a call to Get-WmiObject.</span></span>

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  <span data-ttu-id="e8616-111">Si nécessaire, affichez les propriétés de l’objet avec un appel à la collection de propriétés.</span><span class="sxs-lookup"><span data-stu-id="e8616-111">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="e8616-112">Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.</span><span class="sxs-lookup"><span data-stu-id="e8616-112">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  <span data-ttu-id="e8616-113">Apportez des modifications aux propriétés de l’objet local.</span><span class="sxs-lookup"><span data-stu-id="e8616-113">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="e8616-114">Cela modifie uniquement la copie locale.</span><span class="sxs-lookup"><span data-stu-id="e8616-114">Doing so changes only the local copy.</span></span> <span data-ttu-id="e8616-115">Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="e8616-115">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  <span data-ttu-id="e8616-116">Replacez l’objet dans le référentiel WMI à l’aide d’un appel à la méthode put.</span><span class="sxs-lookup"><span data-stu-id="e8616-116">Place the object back into the WMI repository using a call to the Put method.</span></span>

    ```PowerShell
    $mySettings.Put()
    ```

    

<span data-ttu-id="e8616-117">La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de C#.</span><span class="sxs-lookup"><span data-stu-id="e8616-117">The following procedure describes how to modify or update an instance using C#.</span></span>

<span data-ttu-id="e8616-118">**Pour modifier ou mettre à jour une instance à l’aide de C# (Microsoft. Management. infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="e8616-118">**To modify or update an instance using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="e8616-119">Récupérez une copie locale de l’objet à l’aide d’un appel à [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), comme décrit dans [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="e8616-119">Retrieve a local copy of the object with a call to [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), as described in [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  <span data-ttu-id="e8616-120">Si nécessaire, affichez les propriétés de l’objet avec un appel à la collection de propriétés.</span><span class="sxs-lookup"><span data-stu-id="e8616-120">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="e8616-121">Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.</span><span class="sxs-lookup"><span data-stu-id="e8616-121">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="e8616-122">Apportez des modifications aux propriétés de l’objet local.</span><span class="sxs-lookup"><span data-stu-id="e8616-122">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="e8616-123">Cela modifie uniquement la copie locale.</span><span class="sxs-lookup"><span data-stu-id="e8616-123">Doing so changes only the local copy.</span></span> <span data-ttu-id="e8616-124">Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="e8616-124">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  <span data-ttu-id="e8616-125">Replacez l’objet dans le référentiel WMI à l’aide d’un appel à [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e8616-125">Place the object back into the WMI repository using a call to [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span></span>

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

<span data-ttu-id="e8616-126">La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8616-126">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

> [!Note]  
> <span data-ttu-id="e8616-127">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="e8616-127">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="e8616-128">**Pour modifier ou mettre à jour une instance à l’aide de C# (Microsoft. Management)**</span><span class="sxs-lookup"><span data-stu-id="e8616-128">**To modify or update an instance using C# (Microsoft.Management)**</span></span>

1.  <span data-ttu-id="e8616-129">Récupérez une copie locale de l’objet à l’aide d’un appel à [ManagementObject. obtenir](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="e8616-129">Retrieve a local copy of the object with a call to [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  <span data-ttu-id="e8616-130">Si nécessaire, affichez les propriétés de l’objet avec un appel à la collection de propriétés.</span><span class="sxs-lookup"><span data-stu-id="e8616-130">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="e8616-131">Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.</span><span class="sxs-lookup"><span data-stu-id="e8616-131">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="e8616-132">Apportez des modifications aux propriétés de l’objet local.</span><span class="sxs-lookup"><span data-stu-id="e8616-132">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="e8616-133">Cela modifie uniquement la copie locale.</span><span class="sxs-lookup"><span data-stu-id="e8616-133">Doing so changes only the local copy.</span></span> <span data-ttu-id="e8616-134">Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="e8616-134">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  <span data-ttu-id="e8616-135">Replacez l’objet dans le référentiel WMI à l’aide d’un appel à la méthode [ManagementObject. put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) ou.</span><span class="sxs-lookup"><span data-stu-id="e8616-135">Place the object back into the WMI repository using a call to the [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) or method.</span></span>

    ```CSharp
    myDisk.Put();
    ```

    

<span data-ttu-id="e8616-136">La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="e8616-136">The following procedure describes how to modify or update an instance using VBScript.</span></span>

<span data-ttu-id="e8616-137">**Pour modifier ou mettre à jour une instance à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="e8616-137">**To modify or update an instance using VBScript**</span></span>

1.  <span data-ttu-id="e8616-138">Récupérez une copie locale de l’objet à l’aide d’un appel à **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="e8616-138">Retrieve a local copy of the object with a call to **GetObject**.</span></span>
2.  <span data-ttu-id="e8616-139">Si nécessaire, affichez les propriétés de l’objet à l’aide d’un appel à la méthode [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="e8616-139">If necessary, view the properties of the object with a call to the [**Properties\_**](swbemobject-properties-.md) method.</span></span>

    <span data-ttu-id="e8616-140">Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.</span><span class="sxs-lookup"><span data-stu-id="e8616-140">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="e8616-141">Apportez des modifications aux propriétés de l’objet avec un appel à la méthode [**SWbemProperty. Value**](swbemproperty-value.md) .</span><span class="sxs-lookup"><span data-stu-id="e8616-141">Make any changes to the object properties with a call to the [**SWbemProperty.Value**](swbemproperty-value.md) method.</span></span>

    <span data-ttu-id="e8616-142">La méthode **value** modifie uniquement la copie locale.</span><span class="sxs-lookup"><span data-stu-id="e8616-142">The **Value** method changes only the local copy.</span></span> <span data-ttu-id="e8616-143">Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="e8616-143">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="e8616-144">Replacez l’objet dans le référentiel WMI avec un appel aux méthodes [**SWbemObject. put \_**](swbemobject-put-.md) ou [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="e8616-144">Place the object back into the WMI repository with a call the [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md) methods.</span></span>

<span data-ttu-id="e8616-145">Comme le nom l’indique [**, \_ Mettez**](swbemobject-put-.md) les mises à jour de façon synchrone pendant que [**PutAsync \_**](swbemobject-putasync-.md) est mis à jour de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e8616-145">As the names imply, [**Put\_**](swbemobject-put-.md) updates synchronously while [**PutAsync\_**](swbemobject-putasync-.md) updates asynchronously.</span></span> <span data-ttu-id="e8616-146">L’une ou l’autre méthode copie l’instance d’origine avec votre instance modifiée.</span><span class="sxs-lookup"><span data-stu-id="e8616-146">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="e8616-147">Toutefois, pour tirer parti du traitement asynchrone, vous devez créer un objet [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="e8616-147">However, to take advantage of asynchronous processing, you must create an [**SWbemSink**](swbemsink.md) object.</span></span> <span data-ttu-id="e8616-148">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="e8616-148">For more information, see [Calling a method](calling-a-method.md).</span></span>

<span data-ttu-id="e8616-149">La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="e8616-149">The following procedure describes how to modify or update an instance using C++.</span></span>

<span data-ttu-id="e8616-150">**Pour modifier ou mettre à jour une instance à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="e8616-150">**To modify or update an instance using C++**</span></span>

1.  <span data-ttu-id="e8616-151">Récupérez une copie locale de l’instance avec un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="e8616-151">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>
2.  <span data-ttu-id="e8616-152">Si nécessaire, affichez les propriétés de l’objet à l’aide d’un appel à [**IWbemClassObject :: obtenir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span><span class="sxs-lookup"><span data-stu-id="e8616-152">If necessary, view the properties of the object with a call to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span></span>

    <span data-ttu-id="e8616-153">Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.</span><span class="sxs-lookup"><span data-stu-id="e8616-153">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="e8616-154">Apportez les modifications nécessaires à la copie à l’aide d’un appel à [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="e8616-154">Make any necessary changes to the copy with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="e8616-155">La méthode **put** modifie uniquement la copie locale.</span><span class="sxs-lookup"><span data-stu-id="e8616-155">The **Put** method changes only the local copy.</span></span> <span data-ttu-id="e8616-156">Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="e8616-156">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="e8616-157">Replacez votre copie dans le référentiel WMI avec un appel aux méthodes [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="e8616-157">Place your copy back into the WMI repository with a call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) methods.</span></span>

    <span data-ttu-id="e8616-158">Comme le nom l’indique, **PutInstance** est mis à jour de façon synchrone pendant que [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) est mis à jour de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e8616-158">As the names imply, **PutInstance** updates synchronously while [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) updates asynchronously.</span></span> <span data-ttu-id="e8616-159">L’une ou l’autre méthode copie l’instance d’origine avec votre instance modifiée.</span><span class="sxs-lookup"><span data-stu-id="e8616-159">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="e8616-160">Toutefois, pour tirer parti du traitement asynchrone, vous devez implémenter l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="e8616-160">However, to take advantage of asynchronous processing, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="e8616-161">Vous devez savoir qu’une opération de mise à jour sur une instance appartenant à une hiérarchie de classes peut échouer en raison d’une erreur impliquant une autre classe dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="e8616-161">You should be aware that an update operation on an instance belonging to a class hierarchy might not succeed due to an error involving another class in the hierarchy.</span></span> <span data-ttu-id="e8616-162">WMI appelle la méthode [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) de chacun des fournisseurs responsables des classes dont dérive la classe propriétaire de l’instance d’origine.</span><span class="sxs-lookup"><span data-stu-id="e8616-162">WMI calls the [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method of each of the providers responsible for the classes from which the class owning the original instance derives.</span></span> <span data-ttu-id="e8616-163">Si l’un de ces fournisseurs échoue, la demande de mise à jour d’origine échoue.</span><span class="sxs-lookup"><span data-stu-id="e8616-163">If any of these providers fail, the original update request fails.</span></span> <span data-ttu-id="e8616-164">Pour plus d’informations, consultez la section Notes de [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="e8616-164">For more information, see the Remarks section of [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

<span data-ttu-id="e8616-165">Pour plus d’informations, consultez [appel d’une méthode de fournisseur](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="e8616-165">For more information, see [Calling a Provider Method](calling-a-provider-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="e8616-166">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e8616-166">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="e8616-167">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="e8616-167">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 
