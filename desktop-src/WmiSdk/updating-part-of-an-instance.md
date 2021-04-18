---
description: Il peut arriver que vous souhaitiez mettre à jour uniquement une partie d’une instance.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Mise à jour d’une partie d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519609"
---
# <a name="updating-part-of-an-instance"></a><span data-ttu-id="0ccd2-103">Mise à jour d’une partie d’une instance</span><span class="sxs-lookup"><span data-stu-id="0ccd2-103">Updating Part of an Instance</span></span>

<span data-ttu-id="0ccd2-104">Il peut arriver que vous souhaitiez mettre à jour uniquement une partie d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-104">Occasionally, you may want to update only part of an instance.</span></span> <span data-ttu-id="0ccd2-105">Par exemple, certaines instances ont un grand nombre de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-105">For example, some instances have a large number of properties.</span></span> <span data-ttu-id="0ccd2-106">Si vous deviez mettre à jour un grand nombre de ces instances, vous risquez de réduire les performances du système.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-106">If you had to update a large number of these instances, you may reduce system performance.</span></span> <span data-ttu-id="0ccd2-107">Par conséquent, vous pouvez choisir de mettre à jour une partie de l’instance et, par conséquent, réduire la quantité d’informations que vous devez envoyer et récupérer vers et à partir de WMI.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-107">Therefore, you can choose to update only part of the instance, and thus reduce the amount of information you must send and retrieve to and from WMI.</span></span> <span data-ttu-id="0ccd2-108">Toutefois, WMI ne prend pas directement en charge les opérations d’instance partielle, ni la plupart des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-108">However, WMI does not directly support partial-instance operations, nor do most providers.</span></span> <span data-ttu-id="0ccd2-109">Par conséquent, si vous écrivez une application qui utilise des opérations d’instance partielle, préparez-vous à ce que vos appels échouent avec le code d’erreur **WBEM \_ e \_ \_ non \_ compatible** ou **WBEM \_ e \_ non \_ pris en charge** en C++.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-109">Therefore, if you write an application that uses partial-instance operations, be prepared for your calls to fail with either the **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** or **WBEM\_E\_NOT\_SUPPORTED** error code in C++.</span></span> <span data-ttu-id="0ccd2-110">Dans les langages de script, les codes d’erreur sont **wbemErrProviderNotCapable** ou **wbemErrNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-110">In scripting languages the error codes are either **wbemErrProviderNotCapable** or **wbemErrNotSupported**.</span></span>

<span data-ttu-id="0ccd2-111">Dans les scripts, cette opération n’est nécessaire que pour faciliter les performances lors de la mise à jour d’une ou de deux propriétés accessibles en écriture dans un très grand nombre d’objets au sein d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-111">In scripting, this operation is only necessary to aid performance when updating one or two writeable properties in a very large number of objects over an enterprise.</span></span> <span data-ttu-id="0ccd2-112">Dans le cas contraire, les appels classiques de VBScript à [**SWbemObject. put \_**](swbemobject-put-.md) ou [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md), tout en semblant d’écrire l’objet entier, sont en fait uniquement des mises à jour des propriétés pour lesquelles le fournisseur est activé en écriture.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-112">Otherwise, the normal VBScript calls to [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md), while seeming to write the entire object, are actually only updating the properties which the provider has write-enabled.</span></span>

<span data-ttu-id="0ccd2-113">La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-113">The following procedure describes how to request a partial-instance update using PowerShell.</span></span>

<span data-ttu-id="0ccd2-114">**Pour demander une mise à jour d’instance partielle à l’aide de PowerShell**</span><span class="sxs-lookup"><span data-stu-id="0ccd2-114">**To request a partial-instance update using PowerShell**</span></span>

1.  <span data-ttu-id="0ccd2-115">Récupérez le chemin d’accès de l’objet que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-115">Retrieve the path of the object you wish to update.</span></span>

    <span data-ttu-id="0ccd2-116">Vous pouvez décrire le chemin d’accès manuellement ou interroger l’objet, puis récupérer la propriété **\_ \_ path** .</span><span class="sxs-lookup"><span data-stu-id="0ccd2-116">You can describe the path either manually, or else query the object and then retrieve the **\_\_Path** property.</span></span>

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  <span data-ttu-id="0ccd2-117">Configurez une table de hachage qui répertorie les noms des propriétés à mettre à jour et utilisez cette table de hachage dans un appel à [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="0ccd2-117">Set up a hash table listing the names of the properties to be updated, and use this hash table in a call to [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

<span data-ttu-id="0ccd2-118">La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de C#.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-118">The following procedure describes how to request a partial-instance update using C#.</span></span>

> [!Note]  
> <span data-ttu-id="0ccd2-119">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="0ccd2-120">**Pour demander une mise à jour d’instance partielle à l’aide de C #**</span><span class="sxs-lookup"><span data-stu-id="0ccd2-120">**To request a partial-instance update using C#**</span></span>

1.  <span data-ttu-id="0ccd2-121">Créez un nouvel objet [ManagementObject](/dotnet/api/system.management.managementobject) qui représente l’instance spécifique à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-121">Create a new [ManagementObject](/dotnet/api/system.management.managementobject) object that represents the specific instance to update.</span></span>

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  <span data-ttu-id="0ccd2-122">Définissez la valeur de la propriété avec un appel à [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span><span class="sxs-lookup"><span data-stu-id="0ccd2-122">Set the property value with a call to [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span></span>

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

<span data-ttu-id="0ccd2-123">La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-123">The following procedure describes how to request a partial-instance update using VBScript.</span></span>

<span data-ttu-id="0ccd2-124">**Pour demander une mise à jour d’instance partielle à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="0ccd2-124">**To request a partial-instance update using VBScript**</span></span>

1.  <span data-ttu-id="0ccd2-125">Créez un objet de contexte [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="0ccd2-125">Create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object.</span></span>

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  <span data-ttu-id="0ccd2-126">Ajoutez les valeurs d’extension put « \_ \_ put \_ extensions » et « \_ \_ put \_ ext \_ client \_ Request » à l’objet Context à l’aide de la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="0ccd2-126">Add the Put extension values "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" to the context object using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span>

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  <span data-ttu-id="0ccd2-127">Configurez un tableau répertoriant les noms des propriétés à mettre à jour et ajoutez ce tableau à l’objet de contexte [**SWbemNamedValueSet**](swbemnamedvalueset.md) avec la valeur d’extension put « \_ \_ put \_ ext \_ Properties ».</span><span class="sxs-lookup"><span data-stu-id="0ccd2-127">Set up an array listing the names of the properties to be updated and add this array to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object with the Put extension value "\_\_PUT\_EXT\_PROPERTIES".</span></span>

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  <span data-ttu-id="0ccd2-128">Définissez le paramètre *IFlags* de l’appel [**SWbemObject. \_ put**](swbemobject-put-.md) sur **wbemChangeFlagUpdateOnly**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-128">Set the *iFlags* parameter of the [**SWbemObject.Put\_**](swbemobject-put-.md) call to **wbemChangeFlagUpdateOnly**.</span></span> <span data-ttu-id="0ccd2-129">Sans cet indicateur, l’appel échoue avec un contexte non valide.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-129">Without this flag the call will fail with an invalid context.</span></span>

5.  <span data-ttu-id="0ccd2-130">Transmettez votre indicateur et l’objet de contexte au fournisseur dans le paramètre *objwbemNamedValueSet* de [**SWbemObject. \_ put**](swbemobject-put-.md) ou [**SWbemObject. \_ PutAsync**](swbemobject-putasync-.md).</span><span class="sxs-lookup"><span data-stu-id="0ccd2-130">Pass your flag and context object to the provider in the *objwbemNamedValueSet* parameter of either [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md).</span></span>

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

<span data-ttu-id="0ccd2-131">La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-131">The following procedure describes how to request a partial-instance update using C++.</span></span>

<span data-ttu-id="0ccd2-132">**Pour demander une mise à jour d’instance partielle à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="0ccd2-132">**To request a partial-instance update using C++**</span></span>

1.  <span data-ttu-id="0ccd2-133">Créez un objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="0ccd2-133">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="0ccd2-134">Un objet de contexte est un objet que WMI utilise pour transmettre plus d’informations à un fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-134">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="0ccd2-135">Dans ce cas, vous utilisez l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) pour indiquer au fournisseur d’accepter les mises à jour de l’instance partielle.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-135">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to accept partial-instance updates.</span></span>

2.  <span data-ttu-id="0ccd2-136">Ajoutez les \_ \_ \_ valeurs nommées « put extensions » et « \_ \_ put \_ ext \_ client \_ Request » à l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) à l’aide d’un appel à [**IWbemContext :: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="0ccd2-136">Add the "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" named values to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="0ccd2-137">Le tableau suivant répertorie la signification des « \_ \_ put \_ extensions » et « \_ \_ put \_ ext \_ client \_ Request ».</span><span class="sxs-lookup"><span data-stu-id="0ccd2-137">The following table lists the meaning of "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST".</span></span>

    

    | <span data-ttu-id="0ccd2-138">Valeur nommée</span><span class="sxs-lookup"><span data-stu-id="0ccd2-138">Named value</span></span>                     | <span data-ttu-id="0ccd2-139">Description</span><span class="sxs-lookup"><span data-stu-id="0ccd2-139">Description</span></span>                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0ccd2-140">« \_ \_ Placer les \_ Extensions »</span><span class="sxs-lookup"><span data-stu-id="0ccd2-140">"\_\_PUT\_EXTENSIONS"</span></span>           | <span data-ttu-id="0ccd2-141">**VT \_ BOOL** a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-141">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="0ccd2-142">Valeur indiquant qu’une ou plusieurs des autres valeurs de contexte ont été spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-142">A value indicating that one or more of the other context values has been specified.</span></span> <span data-ttu-id="0ccd2-143">Cela permet une vérification rapide de l’objet de contexte dans le fournisseur pour déterminer si des mises à jour de l’instance partielle sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-143">This allows a quick check of the context object inside the provider to determine if partial-instance updates are being used.</span></span> |
    | <span data-ttu-id="0ccd2-144">« \_ \_ put \_ ext \_ client \_ Request »</span><span class="sxs-lookup"><span data-stu-id="0ccd2-144">"\_\_PUT\_EXT\_CLIENT\_REQUEST"</span></span> | <span data-ttu-id="0ccd2-145">**VT \_ BOOL** a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-145">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="0ccd2-146">Défini par le client lors de la demande initiale.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-146">Set by the client during the initial request.</span></span> <span data-ttu-id="0ccd2-147">Cette valeur est utilisée pour empêcher les erreurs de réentrance.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-147">This value is used to prevent reentrancy errors.</span></span>                                                                                                                   |

    

     

3.  <span data-ttu-id="0ccd2-148">Ajoutez les \_ \_ \_ valeurs put ext \_ Strictly \_ , \_ \_ put \_ ext \_ ou \_ \_ put \_ ext \_ atomique dans n’importe quelle combinaison en fonction des besoins de l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec un autre appel à [**IWbemContext :: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="0ccd2-148">Add the \_\_PUT\_EXT\_STRICT\_NULLS, \_\_PUT\_EXT\_PROPERTIES, or \_\_PUT\_EXT\_ATOMIC in any combination as needed to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with another call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="0ccd2-149">Le tableau suivant répertorie la signification des valeurs nommées.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-149">The following table lists the meaning of the named values.</span></span>

    

    | <span data-ttu-id="0ccd2-150">Valeur nommée</span><span class="sxs-lookup"><span data-stu-id="0ccd2-150">Named value</span></span>                   | <span data-ttu-id="0ccd2-151">Description</span><span class="sxs-lookup"><span data-stu-id="0ccd2-151">Description</span></span>                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0ccd2-152">« \_ \_ put \_ ext \_ Strictly \_ NULLS »</span><span class="sxs-lookup"><span data-stu-id="0ccd2-152">"\_\_PUT\_EXT\_STRICT\_NULLS"</span></span> | <span data-ttu-id="0ccd2-153">**VT \_ BOOL** a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-153">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="0ccd2-154">Indique que le client a défini intentionnellement des propriétés sur **VT \_ null** et s’attend à ce que l’opération d’écriture aboutisse.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-154">Indicates that the client has intentionally set properties to **VT\_NULL** and expects the write operation to succeed.</span></span> <span data-ttu-id="0ccd2-155">Si le fournisseur ne peut pas définir les valeurs sur **null**, une erreur doit être signalée.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-155">If the provider cannot set the values to **NULL**, an error should be reported.</span></span> |
    | <span data-ttu-id="0ccd2-156">« \_ \_ Placer \_ les \_ Propriétés ext »</span><span class="sxs-lookup"><span data-stu-id="0ccd2-156">"\_\_PUT\_EXT\_PROPERTIES"</span></span>    | <span data-ttu-id="0ccd2-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de chaînes contenant une liste de noms de propriétés à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings containing a list of property names to be updated.</span></span> <span data-ttu-id="0ccd2-158">Peut être utilisé seul ou en combinaison avec « \_ \_ put \_ ext \_ Properties ».</span><span class="sxs-lookup"><span data-stu-id="0ccd2-158">May be used alone or in combination with "\_\_PUT\_EXT\_PROPERTIES".</span></span> <span data-ttu-id="0ccd2-159">Les valeurs se trouvent dans l’instance en cours d’écriture.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-159">The values are in the instance being written.</span></span>                           |
    | <span data-ttu-id="0ccd2-160">« \_ \_ put \_ ext \_ atomique »</span><span class="sxs-lookup"><span data-stu-id="0ccd2-160">"\_\_PUT\_EXT\_ATOMIC"</span></span>        | <span data-ttu-id="0ccd2-161">**VT \_ BOOL** a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-161">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="0ccd2-162">Indique que toutes les mises à jour doivent être exécutées simultanément (sémantique atomique) ou que le fournisseur doit être restauré.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-162">Indicates that all updates must succeed simultaneously (atomic semantics) or the provider must revert back.</span></span> <span data-ttu-id="0ccd2-163">Il ne peut pas y avoir de succès partiel.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-163">There can be no partial success.</span></span> <span data-ttu-id="0ccd2-164">Peut être utilisé seul ou en combinaison avec d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-164">May be used alone or in combination with other flags.</span></span>     |

    

     

4.  <span data-ttu-id="0ccd2-165">Définissez le paramètre *IFlags* sur **la \_ \_ mise à jour \_ de l’indicateur WBEM uniquement**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-165">Set the *iFlags* parameter to **WBEM\_FLAG\_UPDATE\_ONLY**.</span></span> <span data-ttu-id="0ccd2-166">Sans cet indicateur, l’appel échoue avec un contexte non valide.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-166">Without this flag the call will fail with an invalid context.</span></span>
5.  <span data-ttu-id="0ccd2-167">Transmettez l’objet de contexte [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) dans n’importe quel appel à [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) dans le paramètre *pctX* .</span><span class="sxs-lookup"><span data-stu-id="0ccd2-167">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) in the *pCtx* parameter.</span></span>

    <span data-ttu-id="0ccd2-168">Le passage de l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) demande au fournisseur d’autoriser les mises à jour d’instance partielle.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-168">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance updates.</span></span> <span data-ttu-id="0ccd2-169">Dans une mise à jour d’instance complète, vous devez affecter à *pctX* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-169">In a full-instance update, you would set *pCtx* to **NULL**.</span></span>

    <span data-ttu-id="0ccd2-170">Le fournisseur peut écrire toutes les propriétés nécessaires si l’objet de contexte présent dans l’appel ne contient pas d' \_ \_ \_ Extensions put.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-170">The provider may write any necessary properties if the context object present in the call does not contain "\_\_PUT\_EXTENSIONS".</span></span> <span data-ttu-id="0ccd2-171">Si « \_ \_ Placer \_ des extensions » est présent dans l’objet de contexte, WMI requiert que le fournisseur obéit exactement à la sémantique de l’opération ou qu’il ne fasse pas échouer l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-171">If "\_\_PUT\_EXTENSIONS" is present in the context object, WMI requires the provider to either obey the semantics of the operation exactly or else fail the call.</span></span> <span data-ttu-id="0ccd2-172">Pour plus d’informations, consultez [gestion des messages d’accès refusé dans un fournisseur](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="0ccd2-172">For more information, see [Handling Access Denied Messages in a Provider](impersonating-a-client.md).</span></span>

 

 
