---
description: Une récupération d’instance partielle est lorsque WMI récupère uniquement un sous-ensemble des propriétés d’une instance.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Récupération d’une partie d’une instance WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cce9d809e5203b7c00f2b2297403f835d98f37ff86641e297673ee50e579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316213"
---
# <a name="retrieving-part-of-a-wmi-instance"></a>Récupération d’une partie d’une instance WMI

Une récupération d’instance partielle est lorsque WMI récupère uniquement un sous-ensemble des propriétés d’une instance. Par exemple, WMI ne peut récupérer que les propriétés **Name** et **Key** . L’utilisation la plus courante de la récupération d’instance partielle est sur les grandes énumérations qui ont plusieurs propriétés.

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a>Récupération d’une partie d’une instance WMI à l’aide de PowerShell

Vous pouvez récupérer une propriété individuelle d’une instance à l’aide de l’expression [« obtenir-WmiObject »](https://technet.microsoft.com/library/dd315379.aspx). la propriété elle-même peut être récupérée et affichée de plusieurs façons. Comme pour la récupération d’une instance, PowerShell retourne par défaut toutes les instances d’une classe donnée ; vous devez spécifier une valeur spécifique si vous souhaitez récupérer une seule instance.

L’exemple de code suivant affiche le numéro de série du volume pour une instance de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a>Récupération d’une partie d’une instance WMI à l’aide de C# (System. Management)

Vous pouvez récupérer une propriété individuelle d’une instance en créant un nouveau [ManagementObject](/dotnet/api/system.management.managementobject) à l’aide des détails d’une instance spécifique. Vous pouvez ensuite récupérer implicitement une ou plusieurs propriétés de l’instance avec la méthode [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) .

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

L’exemple de code suivant affiche le numéro de série du volume pour une instance de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a>Récupération d’une partie d’une instance WMI à l’aide de VBScript

Vous pouvez récupérer une propriété individuelle d’une instance à l’aide de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

L’exemple de code suivant affiche le numéro de série du volume pour une instance de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a>Récupération d’une partie d’une instance WMI à l’aide de C++

La procédure suivante est utilisée pour demander une récupération d’instance partielle à l’aide de C++.

**Pour demander une récupération d’instance partielle à l’aide de C++**

1.  Créez un objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Un objet de contexte est un objet que WMI utilise pour transmettre plus d’informations à un fournisseur WMI. Dans ce cas, vous utilisez l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) pour indiquer au fournisseur de traiter une récupération d’instance partielle.

2.  Ajoutez \_ \_ \_ des extensions d’extraction, des \_ \_ \_ \_ \_ demandes de client ext et toutes les autres valeurs nommées qui décrivent les propriétés que vous souhaitez récupérer dans l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .

    Le tableau suivant répertorie les différentes valeurs nommées utilisées dans votre appel d’extraction.

    

    | Valeur nommée                              | Description                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_\_RÉCUPÉRER des \_ Extensions<br/>           | **VT \_ BOOL** a la valeur **Variant \_ true**. Utilisé pour signaler que les opérations de récupération d’instance partielle sont utilisées. Cela permet une vérification rapide et unique sans avoir à énumérer l’objet de contexte entier. Si l’une des autres valeurs est utilisée, celle-ci doit être.<br/> |
    | \_\_RÉCUPÉRER \_ les \_ Propriétés ext<br/>      | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de chaînes répertoriant les propriétés à récupérer. Ne peut pas être spécifié simultanément avec les \_ \_ clés d’extraction \_ ext \_ \_ uniquement.<br/> Un astérisque « \* » est un nom de propriété non valide pour les \_ \_ \_ Propriétés obtenir ext \_ .<br/>                    |
    | \_\_RÉCUPÉRER \_ les \_ clés ext \_ uniquement<br/>      | **VT \_ BOOL** a la valeur **Variant \_ true**. Indique que seules les clés doivent être fournies dans l’objet retourné. Ne peut pas être spécifié simultanément avec les \_ \_ propriétés d’extraction \_ ext \_ . Au lieu de cela, a priorité sur les \_ \_ Propriétés de récupération \_ ext \_ .<br/>                            |
    | \_\_OBTENIR \_ la \_ demande du client ext \_<br/> | **VT \_ BOOL** a la valeur **Variant \_ true**. Indique que l’appelant était celui qui a écrit la valeur dans l’objet de contexte et qu’il n’a pas été propagé à partir d’une autre opération dépendante.<br/>                                                                        |

    

     

3.  Transmettez l’objet de contexte [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) dans tous les appels à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) par le biais du paramètre *pctX* .

    Le passage de l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) demande au fournisseur d’autoriser les récupérations d’instance partielle. Dans une récupération d’instance complète, vous devez définir *pctX* sur une valeur **null** . Si le fournisseur ne prend pas en charge la récupération de l’instance partielle, vous recevrez un message d’erreur.

Si le fournisseur ne peut pas se conformer à l’opération d’instance partielle, le fournisseur se poursuit comme si vous n’aviez pas entré l’objet de contexte, ou sinon retourne un **\_ \_ \_ paramètre non pris en charge par WBEM**.

L’exemple suivant décrit comment effectuer une récupération d’instance complète du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), puis effectue une récupération d’instance partielle de la propriété **Win32 \_ LogicalDisk. Caption** .


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



Une fois exécuté, l’exemple de code précédent écrit les informations suivantes. La description du premier objet provient de la récupération de l’instance complète. La deuxième Description de l’objet provient de la récupération de l’instance partielle. La dernière section indique que vous recevez une valeur **null** si vous demandez une propriété qui n’a pas été demandée dans l’appel [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) d’origine.

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

La sortie suivante est générée par l’exemple précédent.

``` syntax
file system variable is null - expected
Press any key to continue
```

 

