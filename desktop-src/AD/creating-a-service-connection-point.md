---
title: Création d’un point de connexion de service
description: L’exemple de code suivant montre comment créer et initialiser un point de connexion de service.
ms.assetid: 6ab1e72f-22e8-499a-916e-c2ba8e2c2aff
ms.tgt_platform: multiple
keywords:
- Création d’une publicité de point de connexion de service
- Point de connexion de service, création d’AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ec4e9097414ea8131b3dd1cbd832e73b388e5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031037"
---
# <a name="creating-a-service-connection-point"></a><span data-ttu-id="02e53-105">Création d’un point de connexion de service</span><span class="sxs-lookup"><span data-stu-id="02e53-105">Creating a Service Connection Point</span></span>

<span data-ttu-id="02e53-106">L’exemple de code suivant montre comment créer et initialiser un point de connexion de service.</span><span class="sxs-lookup"><span data-stu-id="02e53-106">The following code example shows how to create and initialize a service connection point.</span></span> <span data-ttu-id="02e53-107">L’exemple de code exécute des étapes supplémentaires qui permettent au service de mettre à jour les valeurs SCP au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="02e53-107">The code example performs additional steps that enable the service to update the SCP values at run time.</span></span> <span data-ttu-id="02e53-108">En règle générale, un programme d’installation de service effectue ces étapes dans le cadre de l’installation d’une instance de service sur un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="02e53-108">Typically, a service installer performs these steps as part of installing a service instance on a host computer.</span></span>

<span data-ttu-id="02e53-109">Cet exemple de code crée l’objet SCP en tant qu’objet enfant pour l’objet de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="02e53-109">This code example creates the SCP object as a child object for the object of the local computer.</span></span> <span data-ttu-id="02e53-110">Elle utilise la fonction [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) pour récupérer le DN de l’objet ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="02e53-110">It uses the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the DN of the local computer object.</span></span> <span data-ttu-id="02e53-111">Il utilise ensuite le DN pour établir une liaison avec un pointeur [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pour l’objet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="02e53-111">It then uses the DN to bind to an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pointer for the computer object.</span></span> <span data-ttu-id="02e53-112">La méthode [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) crée le SCP et spécifie des valeurs initiales pour les attributs SCP importants.</span><span class="sxs-lookup"><span data-stu-id="02e53-112">The [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method creates the SCP and specifies initial values for the important SCP attributes.</span></span>

<span data-ttu-id="02e53-113">[**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) retourne un pointeur vers le nouveau SCP, que l’exemple de code utilise pour récupérer un pointeur [**IADs**](/windows/desktop/api/iads/nn-iads-iads) pour le SCP.</span><span class="sxs-lookup"><span data-stu-id="02e53-113">[**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) returns a pointer to the new SCP, which the code example uses to retrieve an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) pointer for the SCP.</span></span> <span data-ttu-id="02e53-114">L’exemple de code utilise des méthodes **IADs** pour récupérer les attributs **objectGUID** et **distinguishedName** du SCP.</span><span class="sxs-lookup"><span data-stu-id="02e53-114">The code example uses **IADs** methods to retrieve the **objectGUID** and **distinguishedName** attributes of the SCP.</span></span> <span data-ttu-id="02e53-115">L’exemple de code utilise l' **objectGUID** pour composer une chaîne utilisée pour effectuer une liaison au SCP, puis met en cache la chaîne de liaison GUID dans le registre local où elle peut être récupérée par le service au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="02e53-115">The code example uses the **objectGUID** to compose a string used to bind to the SCP, and then caches the GUID binding string in the local registry where it can be retrieved by the service at run time.</span></span> <span data-ttu-id="02e53-116">Le **distinguishedName** est retourné à l’appelant de fonction pour une utilisation dans la composition d’un nom de principal du service (SPN) pour l’instance de service.</span><span class="sxs-lookup"><span data-stu-id="02e53-116">The **distinguishedName** is returned to the function caller for use in composing a service principal name (SPN) for the service instance.</span></span>

<span data-ttu-id="02e53-117">L’exemple de code suivant appelle cette fonction dans le cadre des étapes de base de l’installation d’un service prenant en charge les annuaires.</span><span class="sxs-lookup"><span data-stu-id="02e53-117">The following code example calls this function as part of the basic steps of installing a directory-enabled service.</span></span> <span data-ttu-id="02e53-118">Pour plus d’informations, consultez [installation d’un service sur un ordinateur hôte](installing-a-service-on-a-host-computer.md).</span><span class="sxs-lookup"><span data-stu-id="02e53-118">For more information, see [Installing a Service on a Host Computer](installing-a-service-on-a-host-computer.md).</span></span>


```C++
// ScpCreate
//
// Create a new service connection point as a child object of the 
// local server computer object.
//
DWORD
ScpCreate(
       USHORT usPort, // Service's default port to store in SCP.
       LPTSTR szClass, // Service class string to store in SCP.
       LPTSTR szAccount, // Logon account that must access SCP.
       UINT ccDN, // Length of the pszDN buffer in characters
       TCHAR *pszDN) // Returns distinguished name of SCP.
{
DWORD dwStat, dwAttr, dwLen;
HRESULT hr;
IDispatch *pDisp;          // Returned dispinterface of new object.
IDirectoryObject *pComp;   // Computer object; parent of SCP.
IADs *pIADsSCP;            // IADs interface on new object.

if(!szClass || !szAccount || !pszDN || !(ccDN > 0))
{
       hr = ERROR_INVALID_PARAMETER;
       ReportError(TEXT("Invalid parameter."), hr);
       return hr;
}

// Values for SCPs keywords attribute.
TCHAR* KwVal[]={
        TEXT("83C29870-1DFC-11d3-A193-0000F87A9099"), // Vendor GUID.
        TEXT("A762885A-AA44-11d2-81F1-00C04FB9624E"), // Product GUID.
        TEXT("Microsoft"), // Vendor Name.
        TEXT("Windows 2000 Auth-O-Matic"), // Product Name.
};

TCHAR       szServer[MAX_PATH];
TCHAR       szDn[MAX_PATH];
TCHAR       szAdsPath[MAX_PATH];
TCHAR       szPort[6];

HKEY        hReg;
DWORD       dwDisp;

ADSVALUE cn,objclass,keywords[4],binding,classname,dnsname,nametype;

// SCP attributes to set during creation of SCP.
ADS_ATTR_INFO   ScpAttribs[] = 
{
    {
        TEXT("cn"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &cn,
        1
    },
    {
        TEXT("objectClass"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &objclass,
        1
    },
    {
         TEXT("keywords"),
         ADS_ATTR_UPDATE,
         ADSTYPE_CASE_IGNORE_STRING,
         keywords,
         4
    },
    {
         TEXT("serviceDnsName"),
         ADS_ATTR_UPDATE,
         ADSTYPE_CASE_IGNORE_STRING,
         &dnsname,
         1
    },
    {
        TEXT("serviceDnsNameType"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &nametype,
        1
    },
    {
        TEXT("serviceClassName"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &classname,
        1
    },
    {
        TEXT("serviceBindingInformation"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &binding,
        1
    },
};

BSTR bstrGuid = NULL;
TCHAR pwszBindByGuidStr[1024]; 
VARIANT var;

// Get the DNS name of the local computer.
dwLen = sizeof(szServer);
if (!GetComputerNameEx(ComputerNameDnsFullyQualified,szServer,&dwLen))
    return GetLastError();
_tprintf(TEXT("GetComputerNameEx: %s\n"), szServer);
    
// Enter the attribute values to be stored in the SCP.
keywords[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[2].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[3].dwType = ADSTYPE_CASE_IGNORE_STRING;

keywords[0].CaseIgnoreString=KwVal[0];
keywords[1].CaseIgnoreString=KwVal[1];
keywords[2].CaseIgnoreString=KwVal[2];
keywords[3].CaseIgnoreString=KwVal[3];

cn.dwType                   = ADSTYPE_CASE_IGNORE_STRING;
cn.CaseIgnoreString         = TEXT("SockAuthAD");
objclass.dwType             = ADSTYPE_CASE_IGNORE_STRING;
objclass.CaseIgnoreString   = TEXT("serviceConnectionPoint");

dnsname.dwType              = ADSTYPE_CASE_IGNORE_STRING;
dnsname.CaseIgnoreString    = szServer;
classname.dwType            = ADSTYPE_CASE_IGNORE_STRING;
classname.CaseIgnoreString  = szClass;

_stprintf_s(szPort,TEXT("%d"),usPort);
binding.dwType              = ADSTYPE_CASE_IGNORE_STRING;
binding.CaseIgnoreString    = szPort;
nametype.dwType             = ADSTYPE_CASE_IGNORE_STRING;
nametype.CaseIgnoreString   = TEXT("A");

/*
Get the distinguished name of the computer object for the local 
computer.
*/
dwLen = sizeof(szDn);
if (!GetComputerObjectName(NameFullyQualifiedDN,szDn,&dwLen))
    return GetLastError();
_tprintf(TEXT("GetComputerObjectName: %s\n"), szDn);

/*
Compose the ADSpath and bind to the computer object for the local 
computer.
*/
_tcsncpy_s(szAdsPath,TEXT("LDAP://"),MAX_PATH);
_tcsncat_s(szAdsPath,szDn,MAX_PATH - _tcslen(szAdsPath));
hr = ADsGetObject(szAdsPath, IID_IDirectoryObject, (void **)&pComp);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to bind Computer Object."),hr);
    return hr;
}

//*******************************************************************
// Publish the SCP as a child of the computer object
//*******************************************************************

// Calculate attribute count.
dwAttr = sizeof(ScpAttribs)/sizeof(ADS_ATTR_INFO);  

// Complete the action.
hr = pComp->CreateDSObject(TEXT("cn=SockAuthAD"),
                           ScpAttribs, dwAttr, &pDisp);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to create SCP:"), hr);
    pComp -> Release();
    return hr;
}

pComp -> Release();

// Query for an IADs pointer on the SCP object.
hr = pDisp->QueryInterface(IID_IADs,(void **)&pIADsSCP);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to QueryInterface for IADs:"),hr);
    pDisp->Release();
    return hr;
}
pDisp->Release();

// Set ACEs on the SCP so a service can modify it.
hr = AllowAccessToScpProperties(
        szAccount,     // Service account to allow access.
        pIADsSCP);     // IADs pointer to the SCP object.
if (FAILED(hr)) {
    ReportError(TEXT("Failed to set ACEs on SCP DACL:"), hr);
    return hr;
}

// Get the distinguished name of the SCP.
VariantInit(&var); 
hr = pIADsSCP->Get(CComBSTR("distinguishedName"), &var); 
if (FAILED(hr)) {
    ReportError(TEXT("Failed to get distinguishedName:"), hr);
    pIADsSCP->Release();
    return hr;
}
_tprintf(TEXT("distinguishedName via IADs: %s\n"), var.bstrVal);

// Return the DN of the SCP, which is used to compose the SPN.
// The best practice is to either accept and return the buffer
// size or do this in a _try / _except block, both omitted here
// for clarity.
_tcsncpy_s(pszDN, var.bstrVal, ccDN);

// Retrieve the SCP objectGUID in format suitable for binding. 
hr = pIADsSCP->get_GUID(&bstrGuid); 
if (FAILED(hr)) {
    ReportError(TEXT("Failed to get GUID:"), hr);
    pIADsSCP->Release();
    return hr;
}

// Build a string for binding to the object by GUID.
_tcsncpy_s(pwszBindByGuidStr, 
    TEXT("LDAP://<GUID="),
    1024);
_tcsncat_s(pwszBindByGuidStr, 
    bstrGuid, 
    1024 -_tcslen(pwszBindByGuidStr));
_tcsncat_s(pwszBindByGuidStr, 
    TEXT(">"), 
    1024 -_tcslen(pwszBindByGuidStr));
_tprintf(TEXT("GUID binding string: %s\n"), 
    pwszBindByGuidStr);

pIADsSCP->Release();

// Create a registry key under 
// HKEY_LOCAL_MACHINE\SOFTWARE\Vendor\Product.
dwStat = RegCreateKeyEx(HKEY_LOCAL_MACHINE,
            TEXT("Software\\Fabrikam\\Auth-O-Matic"),
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            KEY_ALL_ACCESS,
            NULL,
            &hReg,
            &dwDisp);
if (dwStat != NO_ERROR) {
    ReportError(TEXT("RegCreateKeyEx failed:"), dwStat);
    return dwStat;
}

// Cache the GUID binding string under the registry key.
dwStat = RegSetValueEx(hReg, TEXT("GUIDBindingString"), 0, REG_SZ,
                           (const BYTE *)pwszBindByGuidStr, 
                           2*(_tcslen(pwszBindByGuidStr)));
if (dwStat != NO_ERROR) {
    ReportError(TEXT("RegSetValueEx failed:"), dwStat);
    return dwStat;
}

RegCloseKey(hReg);

// Cleanup should delete the SCP and registry key if an error occurs.

return dwStat;
}
```



 

 