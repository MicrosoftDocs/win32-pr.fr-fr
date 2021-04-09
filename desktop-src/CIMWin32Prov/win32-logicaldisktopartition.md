---
description: La \_ classe WMI de l’Association LogicalDiskToPartition Win32 associe un lecteur de disque logique et la partition de disque sur laquelle il se trouve.
ms.assetid: 41161d57-d392-4acc-a22a-10be75aa14a6
ms.tgt_platform: multiple
title: Classe Win32_LogicalDiskToPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskToPartition
- Win32_LogicalDiskToPartition.EndingAddress
- Win32_LogicalDiskToPartition.StartingAddress
- Win32_LogicalDiskToPartition.Antecedent
- Win32_LogicalDiskToPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a32a3ee275c32dde7d9f1484aa99dddeaf97a2e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110162"
---
# <a name="win32_logicaldisktopartition-class"></a><span data-ttu-id="b25d4-103">\_Classe LogicalDiskToPartition Win32</span><span class="sxs-lookup"><span data-stu-id="b25d4-103">Win32\_LogicalDiskToPartition class</span></span>

<span data-ttu-id="b25d4-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LogicalDiskToPartition Win32** associe un lecteur de disque logique et la partition de disque sur laquelle il se trouve.</span><span class="sxs-lookup"><span data-stu-id="b25d4-104">The **Win32\_LogicalDiskToPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk drive and the disk partition it resides on.</span></span>

<span data-ttu-id="b25d4-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b25d4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b25d4-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b25d4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b25d4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDiskToPartition : CIM_LogicalDiskBasedOnPartition
{
  uint64                  EndingAddress;
  uint64                  StartingAddress;
  Win32_DiskPartition REF Antecedent;
  Win32_LogicalDisk   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b25d4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b25d4-108">Members</span></span>

<span data-ttu-id="b25d4-109">La classe **Win32 \_ LogicalDiskToPartition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b25d4-109">The **Win32\_LogicalDiskToPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="b25d4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b25d4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b25d4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b25d4-111">Properties</span></span>

<span data-ttu-id="b25d4-112">La classe **Win32 \_ LogicalDiskToPartition** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b25d4-112">The **Win32\_LogicalDiskToPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b25d4-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b25d4-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25d4-114">Type de données : **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="b25d4-114">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="b25d4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b25d4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25d4-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="b25d4-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="b25d4-117">Référence à l’instance de qui représente les propriétés d’une partition de disque sur laquelle réside le disque logique.</span><span class="sxs-lookup"><span data-stu-id="b25d4-117">Reference to the instance representing the properties of a disk partition where the logical disk resides.</span></span>

</dd> <dt>

<span data-ttu-id="b25d4-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b25d4-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25d4-119">Type de données **: \_ disque logique Win32**</span><span class="sxs-lookup"><span data-stu-id="b25d4-119">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="b25d4-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b25d4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25d4-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ LogicalDisk »)</span><span class="sxs-lookup"><span data-stu-id="b25d4-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="b25d4-122">Référence à l’instance de qui représente les propriétés d’un disque logique résidant sur une partition de disque physique.</span><span class="sxs-lookup"><span data-stu-id="b25d4-122">Reference to the instance representing the properties of a logical disk that resides on a physical disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="b25d4-123">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="b25d4-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25d4-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b25d4-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b25d4-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b25d4-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25d4-126">Indique la fin de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="b25d4-126">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="b25d4-127">Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="b25d4-127">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="b25d4-128">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b25d4-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="b25d4-129">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="b25d4-129">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25d4-130">**De la**</span><span class="sxs-lookup"><span data-stu-id="b25d4-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25d4-131">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b25d4-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b25d4-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b25d4-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25d4-133">Indique le début de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="b25d4-133">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="b25d4-134">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b25d4-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="b25d4-135">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="b25d4-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b25d4-136">Notes</span><span class="sxs-lookup"><span data-stu-id="b25d4-136">Remarks</span></span>

<span data-ttu-id="b25d4-137">La classe **Win32 \_ LogicalDiskToPartition** est dérivée de [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md).</span><span class="sxs-lookup"><span data-stu-id="b25d4-137">The **Win32\_LogicalDiskToPartition** class is derived from [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md).</span></span>

<span data-ttu-id="b25d4-138">Pour plus d’informations sur le mappage entre un lecteur logique et un disque physique, consultez Comment puis- [je mettre en corrélation des disques logiques et des disques physiques ?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx).</span><span class="sxs-lookup"><span data-stu-id="b25d4-138">For more information on mapping between a logical drive and a physical disk, see [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="b25d4-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="b25d4-139">Examples</span></span>

<span data-ttu-id="b25d4-140">L’exemple de code C++ suivant décrit comment récupérer les lettres de lecteur pour un lecteur de disque spécifié.</span><span class="sxs-lookup"><span data-stu-id="b25d4-140">The following C++ code sample describes how to retrieve the drive letters for a specified disk drive.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>


#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")


  
BOOL wmi_run();
BOOL wmi_getDriveLetters();
BOOL wmi_close();


  
IWbemLocator *pLoc = NULL;
IWbemServices *pSvc = NULL;


  
int main(int argc, char **argv)
{
    wmi_run();
    wmi_getDriveLetters();

    system("pause");
    wmi_close();
}


  
//
// Step 1-5 at:
// https://msdn.microsoft.com/library/aa390423(VS.85).aspx
BOOL wmi_run()
{
     HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------
    // Note: If you are using Windows 2000, you need to specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );


  
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }

    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    //IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);

    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    //IWbemServices *pSvc = NULL;

    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (e.g. Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );

    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;

    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
 return 0;
}


  
//
// get Drives, logical Drives and Driveletters
BOOL wmi_getDriveLetters()
{

    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:
    HRESULT hres;
    IEnumWbemClassObject* pEnumerator = NULL;

    // get localdrives
    hres = pSvc->ExecQuery(
                    bstr_t("WQL"), 
                    bstr_t("SELECT * FROM Win32_DiskDrive"),
                    WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                    NULL,
                    &pEnumerator);

    if (FAILED(hres)) {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return FALSE;               // Program has failed.
    }
    else { 

        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
        while (pEnumerator) {
           hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                                 &pclsObj, &uReturn);
           if(0 == uReturn) break;

           VARIANT vtProp;
           hres = pclsObj->Get(_bstr_t(L"DeviceID"), 0, &vtProp, 0, 0);

           // adjust string
           wstring tmp = vtProp.bstrVal;
           tmp = tmp.substr(4);

           wstring wstrQuery = L"Associators of {Win32_DiskDrive.DeviceID='\\\\.\\";
           wstrQuery += tmp;
           wstrQuery += L"'} where AssocClass=Win32_DiskDriveToDiskPartition";

           // reference drive to partition
           IEnumWbemClassObject* pEnumerator1 = NULL;
           hres = pSvc->ExecQuery(
                             bstr_t("WQL"), 
                             bstr_t( wstrQuery.c_str()),
                             WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                             NULL,
                             &pEnumerator1 );

           if ( FAILED(hres) ) {
            cout << "Query for processes failed. "
                          << "Error code = 0x" 
                          << hex << hres << endl;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return FALSE;               // Program has failed.
           } else {

                IWbemClassObject *pclsObj1;
                ULONG uReturn1 = 0;
                while( pEnumerator1 ) {
                     hres = pEnumerator1->Next( WBEM_INFINITE, 1, 
                     &pclsObj1, &uReturn1 );
                     if(0 == uReturn1) break;

                     // reference logical drive to partition
                     VARIANT vtProp1;
                     hres = pclsObj1->Get( _bstr_t(L"DeviceID"), 0, &vtProp1, 0, 0 );
                     wstring wstrQuery = L"Associators of {Win32_DiskPartition.DeviceID='";
                     wstrQuery += vtProp1.bstrVal;
                     wstrQuery += L"'} where AssocClass=Win32_LogicalDiskToPartition";


  
                     IEnumWbemClassObject* pEnumerator2 = NULL;
                     hres = pSvc->ExecQuery(
                                       bstr_t("WQL"), 
                                       bstr_t(wstrQuery.c_str()),
                                       WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                                       NULL,
                                       &pEnumerator2 );





                    if ( FAILED(hres) ) {
                        cout << "Query for processes failed. "
                                << "Error code = 0x" 
                                << hex << hres << endl;
                        pSvc->Release();
                        pLoc->Release();     
                        CoUninitialize();
                        return FALSE;               // Program has failed.
                     } else {

                        // get driveletter
                        IWbemClassObject *pclsObj2;
                        ULONG uReturn2 = 0;
                        while( pEnumerator2 ) {
                            hres = pEnumerator2->Next( WBEM_INFINITE, 1, 
                            &pclsObj2, &uReturn2 );
                            if(0 == uReturn2) break;

                            VARIANT vtProp2;
                            hres = pclsObj2->Get( _bstr_t(L"DeviceID"), 0, &vtProp2, 0, 0 );


  
                            // print result
                            printf("%ls : %ls\n", vtProp.bstrVal, vtProp2.bstrVal);

                            VariantClear( &vtProp2 );
                        }
                        pclsObj1->Release();
                    }
                    VariantClear( &vtProp1 );
                    pEnumerator2->Release();
                }
                pclsObj->Release();
            }
            VariantClear( &vtProp );
            pEnumerator1->Release();
        }
     }
     pEnumerator->Release();
     return TRUE;
}






BOOL wmi_close()
{
 // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed. 
}
```



## <a name="requirements"></a><span data-ttu-id="b25d4-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b25d4-141">Requirements</span></span>



| <span data-ttu-id="b25d4-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b25d4-142">Requirement</span></span> | <span data-ttu-id="b25d4-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="b25d4-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b25d4-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b25d4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b25d4-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b25d4-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b25d4-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b25d4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b25d4-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b25d4-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b25d4-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b25d4-148">Namespace</span></span><br/>                | <span data-ttu-id="b25d4-149">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b25d4-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b25d4-150">MOF</span><span class="sxs-lookup"><span data-stu-id="b25d4-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b25d4-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b25d4-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b25d4-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b25d4-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b25d4-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b25d4-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b25d4-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b25d4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25d4-155">**\_LOGICALDISKBASEDONPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="b25d4-155">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dt>

<span data-ttu-id="b25d4-156">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b25d4-156">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b25d4-157">Tâches WMI : disques et systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="b25d4-157">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

