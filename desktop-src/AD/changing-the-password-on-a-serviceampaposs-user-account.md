---
title: Modification du mot de passe sur le compte d’utilisateur d’un service
description: Pour une instance de service qui se connecte avec un compte d’utilisateur, plutôt que le compte LocalSystem, le gestionnaire de contrôle des services (SCM) sur l’ordinateur hôte stocke le mot de passe du compte, qu’il utilise pour se connecter au service au démarrage du service.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Modification du mot de passe sur l’AD du compte d’utilisateur d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66f0d7b4dc668697b7a0a8d5b120735f3a445cf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881623"
---
# <a name="changing-the-password-on-a-services-user-account"></a>Modification du mot de passe sur le compte d’utilisateur d’un service

Pour une instance de service qui se connecte avec un compte d’utilisateur, plutôt que le compte LocalSystem, le gestionnaire de contrôle des services (SCM) sur l’ordinateur hôte stocke le mot de passe du compte, qu’il utilise pour se connecter au service au démarrage du service. Comme pour n’importe quel compte d’utilisateur, vous devez modifier régulièrement le mot de passe pour maintenir la sécurité. Lorsque vous modifiez le mot de passe d’un compte de service, mettez à jour le mot de passe stocké par le SCM. L’exemple de code suivant montre comment effectuer les deux.

Les exemples de code utilisent [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) pour définir le mot de passe du compte. Cette méthode utilise le nom unique du compte. L’exemple ouvre ensuite un handle vers le service installé sur l’ordinateur hôte spécifié et utilise la fonction [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) pour mettre à jour le mot de passe mis en cache par le SCM. Cette fonction utilise le nom Sam (« &lt; domaine &gt; \\ &lt; nom_utilisateur &gt; ») du compte.

> [!Note]  
> Ce code doit être exécuté par un administrateur de domaine.

 

Pour un service réplicable dans lequel chaque réplica utilise un compte d’ouverture de session différent, vous pouvez mettre à jour les mots de passe de tous les réplicas en énumérant les instances de service. Pour plus d’informations et pour obtenir un exemple de code, consultez [énumération des réplicas d’un service](enumerating-the-replicas-of-a-service.md).


```C++
DWORD UpdateAccountPassword(
    LPTSTR szServerDNS,   // DNS name of host computer
    LPTSTR szAccountDN,   // Distinguished name of service 
                          // logon account
    LPTSTR szServiceName, // Name of the service
    LPTSTR szOldPassword, // Old password
    LPTSTR szNewPassword  // New password
    )
{
SC_HANDLE schService = NULL;
SC_HANDLE schSCManager = NULL;
 
DWORD dwLen = MAX_PATH;
TCHAR szAccountPath[MAX_PATH];
IADsUser *pUser = NULL;
HRESULT hr;
 
DWORD dwStatus = 0;
SC_LOCK sclLock = NULL; 

if( !szServerDNS || 
    !szAccountDN || 
    !szServiceName || 
    !szOldPassword || 
    !szNewPassword)
{
    _tprintf(TEXT("Invalid parameter"));
    goto cleanup;
}
 
// Set the password on the account.
// Use the distinguished name to bind to the account object.
_tcsncpy_s(szAccountPath, TEXT("LDAP://"), MAX_PATH);
_tcscat_s(szAccountPath, 
    szAccountDN, 
    MAX_PATH - _tcslen(szAccountPath));
hr = ADsGetObject(szAccountPath, IID_IADsUser, (void**)&pUser);
if (FAILED(hr)) 
{
    _tprintf(TEXT("Get IADsUser failed - 0x%x\n"), dwStatus = hr);
       goto cleanup;
}
 
// Set the password on the account. 
hr = pUser->ChangePassword(CComBSTR(szOldPassword), 
    CComBSTR(szNewPassword));
if (FAILED(hr)) 
{
    _tprintf(TEXT("ChangePassword failed - 0x%x\n"), 
             dwStatus = hr);
    goto cleanup;
}
 
// Update the account and password in the SCM database.
// Open the Service Control Manager on the specified computer.
schSCManager = OpenSCManager(
                szServerDNS,          // DNS name of host computer
                NULL,                 // database (NULL == default)
                SC_MANAGER_ALL_ACCESS // access required
                        );
if (! schSCManager) 
{
    _tprintf(TEXT("OpenSCManager failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Open a handle to the service instance.
schService = OpenService(schSCManager, 
    szServiceName, 
    SERVICE_ALL_ACCESS);
if (! schService) 
{
    _tprintf(TEXT("OpenService failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Get the SCM database lock before changing the password. 
sclLock = LockServiceDatabase(schSCManager); 
if (sclLock == NULL) {
    _tprintf(TEXT("LockServiceDatabase failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Set the account and password that the service uses at startup.
if (! ChangeServiceConfig( 
        schService,        // Handle of service 
        SERVICE_NO_CHANGE, // Service type: no change 
        SERVICE_NO_CHANGE, // Change service start type 
        SERVICE_NO_CHANGE, // Error control: no change 
        NULL,              // Binary path: no change 
        NULL,              // Load order group: no change 
        NULL,              // Tag ID: no change 
        NULL,              // Dependencies: no change 
        NULL,              // Account name: no change 
        szNewPassword,     // New password 
        NULL) )            // Display name: no change
{
    _tprintf(TEXT("ChangeServiceConfig failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
_tprintf(TEXT("Password changed for service instance on: %s\n"), 
    szServerDNS);

cleanup:
 
if (sclLock)
    UnlockServiceDatabase(sclLock); 
if (schService)
    CloseServiceHandle(schService);
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (pUser)
    pUser->Release();
 
return dwStatus;
}
```



 

 
