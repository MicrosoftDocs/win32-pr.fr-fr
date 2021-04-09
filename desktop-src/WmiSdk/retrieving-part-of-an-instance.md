---
description: Une récupération d’instance partielle est lorsque WMI récupère uniquement un sous-ensemble des propriétés d’une instance.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Récupération d’une partie d’une instance WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d547ec2bbb7e3b53e22177cc0c48794dff22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202175"
---
# <a name="retrieving-part-of-a-wmi-instance"></a><span data-ttu-id="0a110-103">Récupération d’une partie d’une instance WMI</span><span class="sxs-lookup"><span data-stu-id="0a110-103">Retrieving Part of a WMI Instance</span></span>

<span data-ttu-id="0a110-104">Une récupération d’instance partielle est lorsque WMI récupère uniquement un sous-ensemble des propriétés d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0a110-104">A partial-instance retrieval is when WMI retrieves only a subset of the properties of an instance.</span></span> <span data-ttu-id="0a110-105">Par exemple, WMI ne peut récupérer que les propriétés **Name** et **Key** .</span><span class="sxs-lookup"><span data-stu-id="0a110-105">For example, WMI could retrieve only the **Name** and **Key** properties.</span></span> <span data-ttu-id="0a110-106">L’utilisation la plus courante de la récupération d’instance partielle est sur les grandes énumérations qui ont plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a110-106">The most common use of partial-instance retrieval is on large enumerations that have multiple properties.</span></span>

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a><span data-ttu-id="0a110-107">Récupération d’une partie d’une instance WMI à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a110-107">Retrieving Part of a WMI Instance Using PowerShell</span></span>

<span data-ttu-id="0a110-108">Vous pouvez récupérer une propriété individuelle d’une instance à l’aide de l’expression [« obtenir-WmiObject »](https://technet.microsoft.com/library/dd315379.aspx). la propriété elle-même peut être récupérée et affichée de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="0a110-108">You can retrieve an individual property of an instance by using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); the property itself can be retrieved and displayed a number of ways.</span></span> <span data-ttu-id="0a110-109">Comme pour la récupération d’une instance, PowerShell retourne par défaut toutes les instances d’une classe donnée ; vous devez spécifier une valeur spécifique si vous souhaitez récupérer une seule instance.</span><span class="sxs-lookup"><span data-stu-id="0a110-109">As with retrieving an instance, PowerShell will by default return all instances of a given class; you must specify a specific value if you wish to retrieve only a single instance.</span></span>

<span data-ttu-id="0a110-110">L’exemple de code suivant affiche le numéro de série du volume pour une instance de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="0a110-110">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a><span data-ttu-id="0a110-111">Récupération d’une partie d’une instance WMI à l’aide de C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="0a110-111">Retrieving Part of a WMI Instance Using C# (System.Management)</span></span>

<span data-ttu-id="0a110-112">Vous pouvez récupérer une propriété individuelle d’une instance en créant un nouveau [ManagementObject](/dotnet/api/system.management.managementobject) à l’aide des détails d’une instance spécifique.</span><span class="sxs-lookup"><span data-stu-id="0a110-112">You can retrieve an individual property of an instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject) using the details of a specific instance.</span></span> <span data-ttu-id="0a110-113">Vous pouvez ensuite récupérer implicitement une ou plusieurs propriétés de l’instance avec la méthode [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) .</span><span class="sxs-lookup"><span data-stu-id="0a110-113">You can then implicitly retrieve one or more properties of the instance with the [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) method.</span></span>

> [!Note]  
> <span data-ttu-id="0a110-114">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="0a110-114">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="0a110-115">L’exemple de code suivant affiche le numéro de série du volume pour une instance de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="0a110-115">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a><span data-ttu-id="0a110-116">Récupération d’une partie d’une instance WMI à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="0a110-116">Retrieving Part of a WMI Instance Using VBScript</span></span>

<span data-ttu-id="0a110-117">Vous pouvez récupérer une propriété individuelle d’une instance à l’aide de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="0a110-117">You can retrieve an individual property of an instance by using [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="0a110-118">L’exemple de code suivant affiche le numéro de série du volume pour une instance de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="0a110-118">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a><span data-ttu-id="0a110-119">Récupération d’une partie d’une instance WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="0a110-119">Retrieving Part of a WMI Instance Using C++</span></span>

<span data-ttu-id="0a110-120">La procédure suivante est utilisée pour demander une récupération d’instance partielle à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="0a110-120">The following procedure is used to request a partial-instance retrieval using C++.</span></span>

<span data-ttu-id="0a110-121">**Pour demander une récupération d’instance partielle à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="0a110-121">**To request a partial-instance retrieval using C++**</span></span>

1.  <span data-ttu-id="0a110-122">Créez un objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="0a110-122">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="0a110-123">Un objet de contexte est un objet que WMI utilise pour transmettre plus d’informations à un fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="0a110-123">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="0a110-124">Dans ce cas, vous utilisez l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) pour indiquer au fournisseur de traiter une récupération d’instance partielle.</span><span class="sxs-lookup"><span data-stu-id="0a110-124">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to process a partial-instance retrieval.</span></span>

2.  <span data-ttu-id="0a110-125">Ajoutez \_ \_ \_ des extensions d’extraction, des \_ \_ \_ \_ \_ demandes de client ext et toutes les autres valeurs nommées qui décrivent les propriétés que vous souhaitez récupérer dans l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="0a110-125">Add \_\_GET\_EXTENSIONS, \_\_GET\_EXT\_CLIENT\_REQUEST, and any other named values that describe the properties you want to retrieve to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object.</span></span>

    <span data-ttu-id="0a110-126">Le tableau suivant répertorie les différentes valeurs nommées utilisées dans votre appel d’extraction.</span><span class="sxs-lookup"><span data-stu-id="0a110-126">The following table lists the different named values use in your retrieval call.</span></span>

    

    | <span data-ttu-id="0a110-127">Valeur nommée</span><span class="sxs-lookup"><span data-stu-id="0a110-127">Named value</span></span>                              | <span data-ttu-id="0a110-128">Description</span><span class="sxs-lookup"><span data-stu-id="0a110-128">Description</span></span>                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0a110-129">\_\_RÉCUPÉRER des \_ Extensions</span><span class="sxs-lookup"><span data-stu-id="0a110-129">\_\_GET\_EXTENSIONS</span></span><br/>           | <span data-ttu-id="0a110-130">**VT \_ BOOL** a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a110-130">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="0a110-131">Utilisé pour signaler que les opérations de récupération d’instance partielle sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="0a110-131">Used to signal that partial-instance retrieval operations are being used.</span></span> <span data-ttu-id="0a110-132">Cela permet une vérification rapide et unique sans avoir à énumérer l’objet de contexte entier.</span><span class="sxs-lookup"><span data-stu-id="0a110-132">This allows a quick, single check without having to enumerate the entire context object.</span></span> <span data-ttu-id="0a110-133">Si l’une des autres valeurs est utilisée, celle-ci doit être.</span><span class="sxs-lookup"><span data-stu-id="0a110-133">If any of the other values are used, this one must be.</span></span><br/> |
    | <span data-ttu-id="0a110-134">\_\_RÉCUPÉRER \_ les \_ Propriétés ext</span><span class="sxs-lookup"><span data-stu-id="0a110-134">\_\_GET\_EXT\_PROPERTIES</span></span><br/>      | <span data-ttu-id="0a110-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de chaînes répertoriant les propriétés à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0a110-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings listing the properties to be retrieved.</span></span> <span data-ttu-id="0a110-136">Ne peut pas être spécifié simultanément avec les \_ \_ clés d’extraction \_ ext \_ \_ uniquement.</span><span class="sxs-lookup"><span data-stu-id="0a110-136">Cannot be simultaneously specified with \_\_GET\_EXT\_KEYS\_ONLY.</span></span><br/> <span data-ttu-id="0a110-137">Un astérisque « \* » est un nom de propriété non valide pour les \_ \_ \_ Propriétés obtenir ext \_ .</span><span class="sxs-lookup"><span data-stu-id="0a110-137">An asterisk "\*" is an invalid property name for \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                    |
    | <span data-ttu-id="0a110-138">\_\_RÉCUPÉRER \_ les \_ clés ext \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="0a110-138">\_\_GET\_EXT\_KEYS\_ONLY</span></span><br/>      | <span data-ttu-id="0a110-139">**VT \_ BOOL** a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a110-139">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="0a110-140">Indique que seules les clés doivent être fournies dans l’objet retourné.</span><span class="sxs-lookup"><span data-stu-id="0a110-140">Indicates that only keys should be provided in the returned object.</span></span> <span data-ttu-id="0a110-141">Ne peut pas être spécifié simultanément avec les \_ \_ propriétés d’extraction \_ ext \_ .</span><span class="sxs-lookup"><span data-stu-id="0a110-141">Cannot be simultaneously specified with \_\_GET\_EXT\_PROPERTIES.</span></span> <span data-ttu-id="0a110-142">Au lieu de cela, a priorité sur les \_ \_ Propriétés de récupération \_ ext \_ .</span><span class="sxs-lookup"><span data-stu-id="0a110-142">Instead, takes precedence over \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                            |
    | <span data-ttu-id="0a110-143">\_\_OBTENIR \_ la \_ demande du client ext \_</span><span class="sxs-lookup"><span data-stu-id="0a110-143">\_\_GET\_EXT\_CLIENT\_REQUEST</span></span><br/> | <span data-ttu-id="0a110-144">**VT \_ BOOL** a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a110-144">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="0a110-145">Indique que l’appelant était celui qui a écrit la valeur dans l’objet de contexte et qu’il n’a pas été propagé à partir d’une autre opération dépendante.</span><span class="sxs-lookup"><span data-stu-id="0a110-145">Indicates that the caller was the one who wrote the value into the context object and that it was not propagated from another dependent operation.</span></span><br/>                                                                        |

    

     

3.  <span data-ttu-id="0a110-146">Transmettez l’objet de contexte [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) dans tous les appels à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) par le biais du paramètre *pctX* .</span><span class="sxs-lookup"><span data-stu-id="0a110-146">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) through the *pCtx* parameter.</span></span>

    <span data-ttu-id="0a110-147">Le passage de l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) demande au fournisseur d’autoriser les récupérations d’instance partielle.</span><span class="sxs-lookup"><span data-stu-id="0a110-147">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance retrievals.</span></span> <span data-ttu-id="0a110-148">Dans une récupération d’instance complète, vous devez définir *pctX* sur une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="0a110-148">In a full-instance retrieval, you would set *pCtx* to a **null** value.</span></span> <span data-ttu-id="0a110-149">Si le fournisseur ne prend pas en charge la récupération de l’instance partielle, vous recevrez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0a110-149">If the provider does not support partial-instance retrieval, you will receive an error message.</span></span>

<span data-ttu-id="0a110-150">Si le fournisseur ne peut pas se conformer à l’opération d’instance partielle, le fournisseur se poursuit comme si vous n’aviez pas entré l’objet de contexte, ou sinon retourne un **\_ \_ \_ paramètre non pris en charge par WBEM**.</span><span class="sxs-lookup"><span data-stu-id="0a110-150">If the provider cannot comply with the partial-instance operation, the provider either proceeds as if you did not enter the context object, or else returns **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="0a110-151">L’exemple suivant décrit comment effectuer une récupération d’instance complète du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), puis effectue une récupération d’instance partielle de la propriété **Win32 \_ LogicalDisk. Caption** .</span><span class="sxs-lookup"><span data-stu-id="0a110-151">The following example describes how to perform a full instance retrieval of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), and then performs a partial-instance retrieval of the **Win32\_LogicalDisk.Caption** property.</span></span>


```C++
#include <stdio.h>
#define _WIN32_DCOM
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#include <iostream>
using namespace std;
#include <comdef.h>


void main(void)
{
    HRESULT hr;
    _bstr_t bstrNamespace;
    IWbemLocator *pWbemLocator = NULL;
    IWbemServices *pServices = NULL;
    IWbemClassObject *pDrive = NULL;
    

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                         RPC_C_AUTHN_LEVEL_CONNECT,
                         RPC_C_IMP_LEVEL_IMPERSONATE,
                         NULL, EOAC_NONE, 0);
 
    if (FAILED(hr))
    {
       CoUninitialize();
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       return;
    }

    hr = CoCreateInstance(CLSID_WbemLocator, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemLocator, 
                          (void**) &pWbemLocator);
    if( FAILED(hr) ) 
    {
        CoUninitialize();
        printf("failed CoCreateInstance\n");
        return;
    }
    
    bstrNamespace = L"root\\cimv2";
    hr = pWbemLocator->ConnectServer(bstrNamespace, 
              NULL, NULL, NULL, 0, NULL, NULL, &pServices);
    if( FAILED(hr) ) 
    {
        pWbemLocator->Release();
        CoUninitialize();
        printf("failed ConnectServer\n");
        return;
    }
    pWbemLocator->Release();
    printf("Successfully connected to namespace.\n");

    
    BSTR bstrPath = 
         SysAllocString(L"Win32_LogicalDisk.DeviceID=\"C:\"");
   // *******************************************************//
   // Perform a full-instance retrieval. 
   // *******************************************************//
    hr = pServices->GetObject(bstrPath,
                              0,0, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed GetObject\n");
        return;
    }    
    // Display the object
    BSTR  bstrDriveObj;
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    pDrive->Release();
    pDrive = NULL;

   // *****************************************************//
   // Perform a partial-instance retrieval. 
   // *****************************************************//
    
    IWbemContext  *pctxDrive; // Create context object
    hr = CoCreateInstance(CLSID_WbemContext, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemContext, 
                          (void**) &pctxDrive);
    if (FAILED(hr))
    {
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("create instance failed for context object.\n");
        return;
    }
    
    VARIANT  vExtensions;
    VARIANT  vClient;
    VARIANT  vPropertyList;
    VARIANT  vProperty;
    SAFEARRAY  *psaProperties;
    SAFEARRAYBOUND saBounds;
    LONG  lArrayIndex = 0;
    
    // Add named values to the context object. 
    VariantInit(&vExtensions);
    V_VT(&vExtensions) = VT_BOOL;
    V_BOOL(&vExtensions) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXTENSIONS"), 
        0, &vExtensions);
    VariantClear(&vExtensions);

    VariantInit(&vClient);
    V_VT(&vClient) = VT_BOOL;
    V_BOOL(&vClient) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_CLIENT_REQUEST"), 
       0, &vClient);
    VariantClear(&vClient);
    // Create an array of properties to return.
    saBounds.cElements = 1;
    saBounds.lLbound = 0;
    psaProperties = SafeArrayCreate(VT_BSTR, 1, &saBounds);

    // Add the Caption property to the array.
    VariantInit(&vProperty);
    V_VT(&vProperty) = VT_BSTR;
    V_BSTR(&vProperty) = _bstr_t(L"Caption");
    SafeArrayPutElement(psaProperties, &lArrayIndex, 
       V_BSTR(&vProperty));
    VariantClear(&vProperty);
    
    VariantInit(&vPropertyList);
    V_VT(&vPropertyList) = VT_ARRAY | VT_BSTR;
    V_ARRAY(&vPropertyList) = psaProperties;
    // Put the array in the named value __GET_EXT_PROPERTIES.
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_PROPERTIES"), 
        0, &vPropertyList);
    VariantClear(&vPropertyList);
    SafeArrayDestroy(psaProperties);

    // Pass the context object as the pCtx parameter of GetObject.
    hr = pServices->GetObject(bstrPath, 0, pctxDrive, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed property GetObject\n");
        return;
    }    
    // Display the object
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    SysFreeString(bstrPath);

    VARIANT vFileSystem;
    // Attempt to get a property that was not requested.
    // The following should return a NULL property if
    // the partial-instance retrieval succeeded.

    hr = pDrive->Get(_bstr_t(L"FileSystem"), 0,
                       &vFileSystem, NULL, NULL);

    if( FAILED(hr) )
    { 
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("failed get for file system\n");
        return;
    }    
 
    if (V_VT(&vFileSystem) == VT_NULL)
        printf("file system variable is null - expected\n");
    else
        printf("FileSystem = %S\n", V_BSTR(&vFileSystem));
    
    VariantClear(&vFileSystem);

    pDrive->Release();    
    pctxDrive->Release();
    pServices->Release();
    pServices = NULL;    // MUST be set to NULL
    CoUninitialize();
    return;  // -- program successfully completed
};
```



<span data-ttu-id="0a110-152">Une fois exécuté, l’exemple de code précédent écrit les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a110-152">When executed, the previous code example writes the following information.</span></span> <span data-ttu-id="0a110-153">La description du premier objet provient de la récupération de l’instance complète.</span><span class="sxs-lookup"><span data-stu-id="0a110-153">The first object description is from the full-instance retrieval.</span></span> <span data-ttu-id="0a110-154">La deuxième Description de l’objet provient de la récupération de l’instance partielle.</span><span class="sxs-lookup"><span data-stu-id="0a110-154">The second object description is from the partial-instance retrieval.</span></span> <span data-ttu-id="0a110-155">La dernière section indique que vous recevez une valeur **null** si vous demandez une propriété qui n’a pas été demandée dans l’appel [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) d’origine.</span><span class="sxs-lookup"><span data-stu-id="0a110-155">The last section shows that you receive a **null** value if you request a property that was not requested in the original [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) call.</span></span>

``` syntax
Successfully connected to namespace

instance of Win32_LogicalDisk
{
        Caption = "C:";
        Compressed = FALSE;
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        FileSystem = "NTFS";
        FreeSpace = "3085668352";
        MaximumComponentLength = 255;
        MediaType = 12;
        Name = "C:";
        Size = "4581445632";
        SupportsFileBasedCompression = TRUE;
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "TITUS";
        VolumeName = "titus-c";
        VolumeSerialNumber = "7CB4B90E";
};

instance of Win32_LogicalDisk
{
        Caption = "C:";
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        MediaType = 12;
        Name = "C:";
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "MySystem";
};
```

<span data-ttu-id="0a110-156">La sortie suivante est générée par l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0a110-156">The following output is generated by the previous example.</span></span>

``` syntax
file system variable is null - expected
Press any key to continue
```

 

