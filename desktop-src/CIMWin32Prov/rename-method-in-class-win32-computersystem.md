---
description: Renomme un ordinateur.
ms.assetid: 9d338ebe-caf0-42c4-995f-fd750e5664df
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ca60021c921e47de3c7afd5b8ee0bb2ea5e6d12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033591"
---
# <a name="rename-method-of-the-win32_computersystem-class"></a><span data-ttu-id="a20e4-103">Renommer la méthode de la \_ classe Win32 ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="a20e4-103">Rename method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="a20e4-104">La méthode **Rename** renomme un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a20e4-104">The **Rename** method renames a computer.</span></span>

<span data-ttu-id="a20e4-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a20e4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a20e4-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a20e4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a20e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a20e4-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name,
  [in] string Password,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="a20e4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a20e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a20e4-109">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a20e4-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a20e4-110">Nouveau nom d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a20e4-110">New computer name.</span></span> <span data-ttu-id="a20e4-111">La valeur de ce paramètre ne peut pas inclure des caractères de contrôle, des espaces de début ou de fin, ou l’un des caractères suivants:/ \\ \\ \[ \] .</span><span class="sxs-lookup"><span data-stu-id="a20e4-111">The value of this parameter cannot include control characters, leading or trailing spaces, or any of the following characters: / \\\\ \[ \].</span></span>

</dd> <dt>

<span data-ttu-id="a20e4-112">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a20e4-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a20e4-113">Mot de passe à utiliser lors de la connexion au contrôleur de domaine si le paramètre de *nom d’utilisateur* spécifie un nom de compte.</span><span class="sxs-lookup"><span data-stu-id="a20e4-113">Password to use when connecting to the domain controller if the *UserName* parameter specifies an account name.</span></span> <span data-ttu-id="a20e4-114">Dans le cas contraire, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a20e4-114">Otherwise, this parameter must be **NULL**.</span></span> <span data-ttu-id="a20e4-115">Pour plus d’informations sur les paramètres de *nom d’utilisateur* et de *mot de passe* , consultez la section Remarques de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a20e4-115">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a20e4-116">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a20e4-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a20e4-117">Chaîne qui spécifie le nom du compte à utiliser lors de la connexion au contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="a20e4-117">String that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="a20e4-118">La chaîne doit se terminer par un caractère **null** et doit spécifier un nom de domaine NetBIOS et un compte d’utilisateur, par exemple, « nom_domaine \\ nom_utilisateur » ou « someone@domainname.com », qui est un nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="a20e4-118">The string must be **null**-terminated, and must specify a domain NetBIOS name and user account for example, "DOMAINNAME\\username" or "someone@domainname.com", which is a user principal name (UPN).</span></span> <span data-ttu-id="a20e4-119">Si le paramètre **username** a la **valeur null**, WMI utilise le contexte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="a20e4-119">If the **UserName** parameter is **NULL**, WMI uses the context of the caller.</span></span> <span data-ttu-id="a20e4-120">Pour plus d’informations sur les paramètres de *nom d’utilisateur* et de *mot de passe* , consultez la section Remarques de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a20e4-120">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a20e4-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a20e4-121">Return value</span></span>

<span data-ttu-id="a20e4-122">Retourne une valeur 0 (zéro) en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a20e4-122">Returns a 0 (zero) if successful.</span></span> <span data-ttu-id="a20e4-123">Une valeur de retour différente de zéro indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="a20e4-123">A nonzero return value indicates an error.</span></span> <span data-ttu-id="a20e4-124">En cas de réussite, un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a20e4-124">If successful, a reboot is required.</span></span> <span data-ttu-id="a20e4-125">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a20e4-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a20e4-126">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a20e4-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a20e4-127">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="a20e4-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a20e4-128">**Autre** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="a20e4-128">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a20e4-129">Notes</span><span class="sxs-lookup"><span data-stu-id="a20e4-129">Remarks</span></span>

<span data-ttu-id="a20e4-130">Vous pouvez utiliser la méthode **Rename** pour renommer un ordinateur si vous êtes membre du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="a20e4-130">You can use the **Rename** method to rename a computer if you are a member of the local administrator group.</span></span> <span data-ttu-id="a20e4-131">Toutefois, vous ne pouvez pas utiliser la méthode à distance pour les ordinateurs du domaine.</span><span class="sxs-lookup"><span data-stu-id="a20e4-131">However, you cannot use the method remotely for domain computers.</span></span>

<span data-ttu-id="a20e4-132">Si les paramètres du *mot de passe* et du *nom d’utilisateur* sont spécifiés, la connexion à WMI doit utiliser le niveau d’authentification de la confidentialité (**wbemAuthenticationLevelPktPrivacy** pour script et Visual Basic (VB)) du niveau d’authentification **RPC \_ C \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="a20e4-132">If the *Password* and *UserName* parameters are specified, the connection to WMI must use the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy** for script and Visual Basic (VB)) authentication level.</span></span>

<span data-ttu-id="a20e4-133">Pour vous connecter à un ordinateur distant et spécifier des informations d’identification, utilisez la connexion à l’objet localisateur, qui est IWbemLocator pour C++ et SWbemLocator pour script et VB.</span><span class="sxs-lookup"><span data-stu-id="a20e4-133">To connect to a remote computer and specify credentials, use the locator object connection, which is IWbemLocator for C++, and SWbemLocator for script and VB.</span></span> <span data-ttu-id="a20e4-134">N’utilisez pas la connexion du moniker.</span><span class="sxs-lookup"><span data-stu-id="a20e4-134">Do not use the moniker connection.</span></span>

<span data-ttu-id="a20e4-135">Pour vous connecter à un ordinateur local, vous ne pouvez pas spécifier un mot de passe ou une autorité d’authentification, tel que Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a20e4-135">To connect to a local computer, you cannot specify a password or an authentication authority, such as Kerberos.</span></span> <span data-ttu-id="a20e4-136">Vous pouvez uniquement spécifier le mot de passe et l’autorité dans connexions aux ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="a20e4-136">You can only specify the password and authority in connections to remote computers.</span></span>

<span data-ttu-id="a20e4-137">Si le niveau d’authentification est trop faible lorsqu’un *mot de passe* et un *nom d’utilisateur* sont spécifiés, WMI renvoie l’erreur de **\_ \_ connexion chiffrée WBEM \_ \_ requise** pour C/C++ et **wbemErrEncryptedConnectionRequired** pour script et VB.</span><span class="sxs-lookup"><span data-stu-id="a20e4-137">If the authentication level is too low when a *Password* and *UserName* are specified, then WMI returns the **WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED** error for C/C++, and **wbemErrEncryptedConnectionRequired** for script and VB.</span></span>

<span data-ttu-id="a20e4-138">Pour plus d’informations, consultez [**SWbemLocator \_ ConnectServer,**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator :: ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver)et [construction d’une chaîne de moniker](/windows/desktop/WmiSdk/constructing-a-moniker-string).</span><span class="sxs-lookup"><span data-stu-id="a20e4-138">For more information, see [**SWbemLocator\_ConnectServer,**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator::ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver), and [Constructing a Moniker String](/windows/desktop/WmiSdk/constructing-a-moniker-string).</span></span>

## <a name="examples"></a><span data-ttu-id="a20e4-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="a20e4-139">Examples</span></span>

<span data-ttu-id="a20e4-140">Le script suivant vous montre comment renommer un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a20e4-140">The following script shows you how to rename a local computer.</span></span>


```VB
Name = "name"
Password = "password"
Username = "username"

Set objWMIService = GetObject("Winmgmts:root\cimv2")

' Call always gets only one Win32_ComputerSystem object.
For Each objComputer in _
    objWMIService.InstancesOf("Win32_ComputerSystem")

        Return = objComputer.rename(Name,Password,Username)
        If Return <> 0 Then
           WScript.Echo "Rename failed. Error = " & Err.Number
        Else
           WScript.Echo "Rename succeeded." & _
               " Reboot for new name to go into effect"
        End If

Next
```



<span data-ttu-id="a20e4-141">L’exemple de code C++ suivant renomme un système informatique.</span><span class="sxs-lookup"><span data-stu-id="a20e4-141">The following C++ code sample renames a computer system.</span></span>


```C++
int set_computer_name(const string &newname/*, const string &username, const string &password*/)
{
 HRESULT hres;


// Step 1: --------------------------------------------------
 // Initialize COM. ------------------------------------------


hres = CoInitializeEx(0, COINIT_MULTITHREADED); 
 if (FAILED(hres))
 {
 cout << "Failed to initialize COM library. Error code = 0x" 
 << hex << hres << endl;
 return 1; // Program has failed.
 }


// Step 2: --------------------------------------------------
 // Set general COM security levels --------------------------
 // Note: If you are using Windows 2000, you need to specify -
 // the default authentication credentials for a user by using
 // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
 // parameter of CoInitializeSecurity ------------------------


hres = CoInitializeSecurity(
 NULL, 
 -1, // COM authentication
 NULL, // Authentication services
 NULL, // Reserved
 RPC_C_AUTHN_LEVEL_DEFAULT, // Default authentication 
 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation 
 NULL, // Authentication info
 EOAC_NONE, // Additional capabilities 
 NULL // Reserved
 );




 if (FAILED(hres))
 {
 cout << "Failed to initialize security. Error code = 0x" 
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
 }

 // Step 3: ---------------------------------------------------
 // Obtain the initial locator to WMI -------------------------


IWbemLocator *pLoc = NULL;


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
 return 1; // Program has failed.
 }


// Step 4: -----------------------------------------------------
 // Connect to WMI through the IWbemLocator::ConnectServer method


IWbemServices *pSvc = NULL;

 // Connect to the root\cimv2 namespace with
 // the current user and obtain pointer pSvc
 // to make IWbemServices calls.
 hres = pLoc->ConnectServer(
 _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
 NULL, // User name. NULL = current user
 NULL, // User password. NULL = current
 0, // Locale. NULL indicates current
 NULL, // Security flags.
 0, // Authority (e.g. Kerberos)
 0, // Context object 
 &pSvc // pointer to IWbemServices proxy
 );

 if (FAILED(hres))
 {
 cout << "Could not connect. Error code = 0x" 
 << hex << hres << endl;
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


/*cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;*/




 // Step 5: --------------------------------------------------
 // Set security levels on the proxy -------------------------


hres = CoSetProxyBlanket(
 pSvc, // Indicates the proxy to set
 RPC_C_AUTHN_WINNT, // RPC_C_AUTHN_xxx
 RPC_C_AUTHZ_NONE, // RPC_C_AUTHZ_xxx
 NULL, // Server principal name 
 RPC_C_AUTHN_LEVEL_CALL, // RPC_C_AUTHN_LEVEL_xxx 
 RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
 NULL, // client identity
 EOAC_NONE // proxy capabilities 
 );


if (FAILED(hres))
 {
 cout << "Could not set proxy blanket. Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 6: --------------------------------------------------
 // Use the IWbemServices pointer to make requests of WMI ----


// For example, get the name of the operating system
 IEnumWbemClassObject* pEnumerator = NULL;
 hres = pSvc->ExecQuery(
 bstr_t("WQL"), 
 bstr_t("SELECT * FROM Win32_ComputerSystem"),
 WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
 NULL,
 &pEnumerator);

 if (FAILED(hres))
 {
 cout << "Query for operating system name failed."
 << " Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release();
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 7: -------------------------------------------------
 // Get the data from the query in step 6 -------------------

 IWbemClassObject *pclsObj;
 ULONG uReturn = 0;

 while (pEnumerator)
 {
 HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
 &pclsObj, &uReturn);


if(0 == uReturn)
 {
 break;
 }


// set up to call the Win32_ComputerSystem::Rename method
 BSTR MethodName = SysAllocString(L"Rename");
 BSTR ClassName = SysAllocString(L"Win32_ComputerSystem");


IWbemClassObject* pClass = NULL;
 hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);


IWbemClassObject* pInParamsDefinition = NULL;
 hres = pClass->GetMethod(MethodName, 0, 
 &pInParamsDefinition, NULL);


IWbemClassObject* pClassInstance = NULL;
 hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);


// Create the values for the in parameters
 wstring val;
 BSTR NewName;
 val.assign(newname.begin(), newname.end());
 NewName = SysAllocString(val.c_str());


VARIANT varName;
 varName.vt = VT_BSTR;
 varName.bstrVal = NewName;


// Store the value for the in parameters
 hres = pClassInstance->Put(L"Name", 0,
 &varName, 0);
 wprintf(L"Set computer name to %s\n", V_BSTR(&varName));


VARIANT var;
 CIMTYPE pType;
 LONG pFlavor;
 pclsObj->Get(L"__PATH",0,&var,&pType,&pFlavor);


// Execute Method
 IWbemClassObject* pOutParams = NULL;
 hres = pSvc->ExecMethod(var.bstrVal, MethodName, 0,
 NULL, pClassInstance, &pOutParams, NULL);


if (FAILED(hres))
 {
 cout << "Could not execute method. Error code = 0x" 
 << hex << hres << endl;
 VariantClear(&varName);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 1; // Program has failed.
 }


// To see what the method returned,
 // use the following code. The return value will
 // be in &varReturnValue
 VARIANT varReturnValue;
 hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
 &varReturnValue, NULL, 0);




 // Clean up
 //--------------------------
 VariantClear(&varName);
 VariantClear(&varReturnValue);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 0;


}


// Cleanup
 // ========

 pSvc->Release();
 pLoc->Release();
 pEnumerator->Release();
 pclsObj->Release();
 CoUninitialize();


return 0; // Program successfully completed.
```



## <a name="requirements"></a><span data-ttu-id="a20e4-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a20e4-142">Requirements</span></span>



| <span data-ttu-id="a20e4-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a20e4-143">Requirement</span></span> | <span data-ttu-id="a20e4-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="a20e4-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a20e4-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a20e4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a20e4-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a20e4-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a20e4-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a20e4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a20e4-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a20e4-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a20e4-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a20e4-149">Namespace</span></span><br/>                | <span data-ttu-id="a20e4-150">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a20e4-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a20e4-151">MOF</span><span class="sxs-lookup"><span data-stu-id="a20e4-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a20e4-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a20e4-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a20e4-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a20e4-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a20e4-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a20e4-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20e4-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a20e4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20e4-156">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="a20e4-156">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="a20e4-157">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="a20e4-157">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> </dl>

 

