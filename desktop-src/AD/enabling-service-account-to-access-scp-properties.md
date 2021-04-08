---
title: Activation du compte de service pour l’accès aux propriétés SCP
description: L’exemple de code suivant définit une paire d’entrées de Access Control (ACE) sur un objet point de connexion de service (SCP).
ms.assetid: 663dcf55-5f0d-49af-8b51-4c1e35b79ef1
ms.tgt_platform: multiple
keywords:
- Activation du compte de service pour accéder aux propriétés SCP AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49adcd1b4747b1c13a64a5af54c6cc6a42e6afe
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842082"
---
# <a name="enabling-service-account-to-access-scp-properties"></a>Activation du compte de service pour l’accès aux propriétés SCP

L’exemple de code suivant définit une paire d’entrées de Access Control (ACE) sur un objet point de connexion de service (SCP). Les ACE accordent un accès en lecture/écriture au compte d’utilisateur ou d’ordinateur sous lequel l’instance de service sera exécutée. Le programme d’installation du service utilise du code semblable au suivant pour s’assurer que le service peut mettre à jour ses propriétés au moment de l’exécution. Si les ACE similaires à celles-ci ne sont pas définies, le service n’aura pas accès aux propriétés du SCP.

En règle générale, un programme d’installation de service définira ces ACE après avoir créé l’objet SCP. Pour plus d’informations et pour obtenir un exemple de code qui crée un SCP et appelle cette fonction, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md). Si le service est reconfiguré pour s’exécuter sous un compte différent, les ACE doivent être mises à jour. Pour s’exécuter correctement, cet exemple de code doit être exécuté dans le contexte de sécurité d’un administrateur de domaine.

Le premier paramètre de l’exemple de fonction spécifie le nom du compte d’utilisateur auquel accorder l’accès. La fonction suppose que le nom est au *format ***\\*** nom d’utilisateur du domaine* . Si aucun compte n’est spécifié, la fonction suppose que le service utilise le compte LocalSystem. Cela signifie que la fonction doit accorder l’accès au compte d’ordinateur du serveur hôte sur lequel le service est en cours d’exécution. Pour ce faire, l’exemple de code appelle la fonction [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) pour obtenir le domaine et le nom d’utilisateur de l’ordinateur local.

L’exemple de code suivant peut être modifié pour accorder au service un accès complet à l’objet SCP, mais la meilleure pratique consiste à accorder uniquement les droits d’accès spécifiques dont le service a besoin au moment de l’exécution. Dans ce cas, la fonction accorde l’accès à deux propriétés.



| Propriété                                                              | Description                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [**serviceDNSName**](/windows/desktop/ADSchema/a-servicednsname)                       | Nom du serveur hôte sur lequel le service est en cours d’exécution.         |
| [**serviceBindingInformation**](/windows/desktop/ADSchema/a-servicebindinginformation) | Informations de liaison privées que le service met à jour lorsqu’il démarre. |



 

Chaque propriété est identifiée par le **schemaIDGUID** de la classe **attributeSchema** de la propriété. Chaque propriété du schéma a son propre **schemaIDGUID** unique. L’exemple de code suivant utilise des chaînes pour spécifier les GUID. Les chaînes GUID ont le format suivant, où chaque « X » est remplacé par un chiffre hexadécimal : {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}.

Reportez-vous aux pages de référence du schéma Active Directory pour les valeurs **schemaIDGUID** affectées aux propriétés auxquelles accorder ou refuser l’accès.

L’exemple de code suivant utilise les interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)et [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) pour effectuer les opérations suivantes.

1.  Obtenez le descripteur de sécurité de l’objet SCP.
2.  Définissez les ACE appropriées dans la liste de contrôle d’accès discrétionnaire (DACL) du descripteur de sécurité.
3.  Modifiez le descripteur de sécurité de l’objet SCP.


```C++
#include <atlbase.h>

//******************************
//
//  AllowAccessToScpProperties()
//
//******************************

HRESULT AllowAccessToScpProperties(
    LPWSTR wszAccountSAM,   // Service account to allow access.
    IADs *pSCPObject)       // IADs pointer to the SCP object.
{
    HRESULT hr = E_FAIL;
    IADsAccessControlList *pACL = NULL;
    IADsSecurityDescriptor *pSD = NULL;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE1 = NULL;
    IADsAccessControlEntry *pACE2 = NULL;
    IDispatch *pDispACE = NULL;
    long lFlags = 0L;
    CComBSTR sbstrTrustee;
    CComBSTR sbstrSecurityDescriptor = L"nTSecurityDescriptor";
    VARIANT varSD;

    if(NULL == pSCPObject)
    {
        return E_INVALIDARG;
    }
    
    VariantInit(&varSD);
     
    /*
    If no service account is specified, service runs under 
    LocalSystem. Allow access to the computer account of the 
    service's host.
    */
    if (wszAccountSAM) 
    {
        sbstrTrustee = wszAccountSAM;
    }
    else
    {
        LPWSTR pwszComputerName;
        DWORD dwLen;
        
        // Get the size required for the SAM account name.
        dwLen = 0;
        GetComputerObjectNameW(NameSamCompatible, 
            NULL, &dwLen);
        
        pwszComputerName = new WCHAR[dwLen + 1];
        if(NULL == pwszComputerName)
        {
            hr = E_OUTOFMEMORY;
            goto cleanup;
        }

        /*
        Get the SAM account name of the computer object for 
        the server.
        */
        if(!GetComputerObjectNameW(NameSamCompatible,
            pwszComputerName, &dwLen))
        {
            delete pwszComputerName;
            
            hr = HRESULT_FROM_WIN32(GetLastError());
            goto cleanup;
        }

        sbstrTrustee = pwszComputerName;
        wprintf(L"GetComputerObjectName: %s\n", pwszComputerName);
        delete pwszComputerName;
    } 

    // Get the nTSecurityDescriptor.
    hr = pSCPObject->Get(sbstrSecurityDescriptor, &varSD);
    if (FAILED(hr) || (varSD.vt != VT_DISPATCH)) 
    {
        _tprintf(TEXT("Get nTSecurityDescriptor failed: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    /*
    Use the V_DISPATCH macro to get the IDispatch pointer from 
    VARIANT structure and QueryInterface for an 
    IADsSecurityDescriptor pointer.
    */
    hr = V_DISPATCH( &varSD )->QueryInterface(
        IID_IADsSecurityDescriptor,
        (void**)&pSD);
    if (FAILED(hr)) 
    {
        _tprintf(
            TEXT("Cannot get IADsSecurityDescriptor: 0x%x\n"), 
            hr);
        goto cleanup;
    } 
     
    /*
    Get an IADsAccessControlList pointer to the security 
    descriptor's DACL.
    */
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(
            IID_IADsAccessControlList,
            (void**)&pACL);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot get DACL: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Create the COM object for the first ACE.
    hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE1);
     
    // Create the COM object for the second ACE.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE2);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot create ACEs: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Set the properties of the two ACEs.
                                
    // Allow read and write access to the property.
    hr = pACE1->put_AccessMask(
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
    hr = pACE2->put_AccessMask( 
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
                                
    // Set the trustee, which is either the service account or the 
    // host computer account.
    hr = pACE1->put_Trustee( sbstrTrustee );
    hr = pACE2->put_Trustee( sbstrTrustee );
                                
    // Set the ACE type.
    hr = pACE1->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
    hr = pACE2->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
                                
    // Set AceFlags to zero because ACE is not inheritable.
    hr = pACE1->put_AceFlags( 0 );
    hr = pACE2->put_AceFlags( 0 );
     
    // Set Flags to indicate an ACE that protects a specified object.
    hr = pACE1->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
    hr = pACE2->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
     
    // Set ObjectType to the schemaIDGUID of the attribute.
    // serviceDNSName
    hr = pACE1->put_ObjectType( 
        L"{28630eb8-41d5-11d1-a9c1-0000f80367c1}"); 
    // serviceBindingInformation
    hr = pACE2->put_ObjectType( 
        L"{b7b1311c-b82e-11d0-afee-0000f80367c1}"); 
     
    /*
    Add the ACEs to the DACL. Need an IDispatch pointer for 
    each ACE to pass to the AddAce method.
    */
    hr = pACE1->QueryInterface(IID_IDispatch,(void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add first ACE: 0x%x\n"), hr);
        goto cleanup;
    }
    else 
    {
        if (pDispACE)
            pDispACE->Release();
    
        pDispACE = NULL;
    }
     
    // Repeat for the second ACE.
    hr = pACE2->QueryInterface(IID_IDispatch, (void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add second ACE: 0x%x\n"), hr);
        goto cleanup;
    }
     
    // Write the modified DACL back to the security descriptor.
    hr = pSD->put_DiscretionaryAcl(pDisp);
    if (SUCCEEDED(hr))
    {
        /*
        Write the ntSecurityDescriptor property to the 
        property cache.
        */
        hr = pSCPObject->Put(sbstrSecurityDescriptor, varSD);
        if (SUCCEEDED(hr))
        {
            // SetInfo updates the SCP object in the directory.
            hr = pSCPObject->SetInfo();
        }
    }
                                    
    cleanup:
    if (pDispACE)
        pDispACE->Release();
                        
    if (pACE1)
        pACE1->Release();
                    
    if (pACE2)
        pACE2->Release();
                    
    if (pACL)
        pACL->Release();
               
    if (pDisp)
        pDisp->Release();
            
    if (pSD)
        pSD->Release();
 
    VariantClear(&varSD);
 
    return hr;
}
```



 

 