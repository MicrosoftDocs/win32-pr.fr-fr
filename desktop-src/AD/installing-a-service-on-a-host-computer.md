---
title: Installation d’un service sur un ordinateur hôte
description: L’exemple de code suivant montre les étapes de base de l’installation d’un service activé pour les annuaires sur un ordinateur hôte.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d687bbbfadb4d1ccb789e9d5f1051ebfbb4484d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462850"
---
# <a name="installing-a-service-on-a-host-computer"></a>Installation d’un service sur un ordinateur hôte

L’exemple de code suivant montre les étapes de base de l’installation d’un service activé pour les annuaires sur un ordinateur hôte. Il effectue les opérations suivantes :

1.  Appelle la fonction [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) pour ouvrir un handle vers le gestionnaire de contrôle des services (SCM) sur l’ordinateur local.
2.  Appelle la fonction [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) pour installer le service dans la base de données SCM. Cet appel spécifie le compte et le mot de passe d’ouverture de session du service, ainsi que l’exécutable du service et d’autres informations sur le service. **CreateService** échoue si le compte d’ouverture de session spécifié n’est pas valide. Toutefois, **CreateService** ne vérifie pas la validité du mot de passe. Il ne vérifie pas non plus que le compte dispose du droit ouvrir une session en tant que service sur l’ordinateur local. Pour plus d’informations, consultez [accorder des droits d’ouverture de session en tant que service sur l’ordinateur hôte](granting-logon-as-service-right-on-the-host-computer.md).
3.  Appelle la sous-routine **ScpCreate** du service qui crée un objet point de connexion de service (SCP) dans le répertoire pour publier l’emplacement de cette instance du service. Pour plus d’informations, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md). Cette routine stocke également les informations de liaison du service dans le SCP, définit une entrée du contrôle d’accès sur le SCP afin que le service puisse y accéder au moment de l’exécution, met en cache le nom unique du SCP dans le registre local et retourne le nom unique du nouveau SCP.
4.  Appelle la sous-routine **SpnCompose** du service qui utilise la chaîne de classe du service et le nom unique du SCP pour composer un nom de principal du service (SPN). Pour plus d’informations, consultez [composition des noms de principal du service pour un service avec SCP](composing-the-spns-for-a-service-with-an-scp.md). Le SPN identifie de manière unique cette instance du service.
5.  Appelle la sous-routine **SpnRegister** du service qui inscrit le SPN sur l’objet de compte associé au compte d’ouverture de session du service. Pour plus d’informations, consultez [enregistrement des noms de principal du service pour un service](registering-the-spns-for-a-service.md). L’inscription du SPN permet aux applications clientes d’authentifier le service.

Cet exemple de code fonctionne correctement, que le compte d’ouverture de session soit un compte d’utilisateur local ou de domaine ou le compte LocalSystem. Pour un compte d’utilisateur de domaine, le paramètre *szServiceAccountSAM* contient le nom d’utilisateur de *domaine ***\\**** du compte et le paramètre *szServiceAccountDN* contient le nom unique de l’objet de compte d’utilisateur dans l’annuaire. Pour le compte LocalSystem, *szServiceAccountSAM* et *szPassword* sont **null**, et *szServiceAccountSN* est le nom unique de l’objet compte de l’ordinateur local dans l’annuaire. Si *szServiceAccountSAM* spécifie un compte d’utilisateur local (le format du nom est «». \\ *Nom d'* utilisateur»), l’exemple de code ignore l’inscription du nom de principal du service, car l’authentification mutuelle n’est pas prise en charge pour les comptes d’utilisateurs locaux.

N’oubliez pas que la configuration de sécurité par défaut autorise uniquement les administrateurs de domaine à exécuter ce code.

Sachez également que cet exemple de code, tel qu’il est écrit, doit être exécuté sur l’ordinateur sur lequel le service est installé. Par conséquent, il s’agit généralement d’un exécutable d’installation distinct de votre code d’installation de service, le cas échéant, qui étend le schéma, étend l’interface utilisateur ou configure la stratégie de groupe. Ces opérations installent des composants de service pour l’ensemble d’une forêt, tandis que ce code installe le service sur un seul ordinateur.


```C++
void InstallServiceOnLocalComputer(
            LPTSTR szServiceAccountDN,  // Distinguished name of logon account.
            LPTSTR szServiceAccountSAM, // SAM name of logon account.
            LPTSTR szPassword)          // Password of logon account.
{
SC_HANDLE   schService = NULL;
SC_HANDLE   schSCManager = NULL;
TCHAR szPath[512];
LPTSTR lpFilePart;
TCHAR szDNofSCP[MAX_PATH];
TCHAR szServiceClass[]=TEXT("ADSockAuth");
 
DWORD dwStatus;
TCHAR **pspn=NULL;
ULONG ulSpn=1;
 
// Get the full path of the service's executable.
// The code example assumes that the executable is in the current directory.
dwStatus = GetFullPathName(TEXT("service.exe"), 512, szPath, &lpFilePart);
if (dwStatus == 0) {
    _tprintf(TEXT("Unable to install %s - %s\n"), 
            TEXT(SZSERVICEDISPLAYNAME), GetLastErrorText(szErr, 256));
    return;
}
_tprintf(TEXT("path of service.exe: %s\n"), szPath);
 
// Open the Service Control Manager on the local computer.
schSCManager = OpenSCManager(
                NULL,                   // Computer (NULL == local)
                NULL,                   // Database (NULL == default)
                SC_MANAGER_ALL_ACCESS   // Access required
                );
if (! schSCManager) {
    _tprintf(TEXT("OpenSCManager failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
        
// Install the service in the SCM database.
schService = CreateService(
            schSCManager,               // SCManager database
            TEXT(SZSERVICENAME),        // Name of service
            TEXT(SZSERVICEDISPLAYNAME), // Name to display
            SERVICE_ALL_ACCESS,         // Desired access
            SERVICE_WIN32_OWN_PROCESS,  // Service type
            SERVICE_DEMAND_START,       // Start type
            SERVICE_ERROR_NORMAL,       // Error control type
            szPath,                     // Service binary
            NULL,                       // No load ordering group
            NULL,                       // No tag identifier
            TEXT(SZDEPENDENCIES),       // Dependencies
            szServiceAccountSAM,        // Service account
            szPassword);                // Account password
if (! schService) {
    _tprintf(TEXT("CreateService failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
 
_tprintf(TEXT("%s installed.\n"), TEXT(SZSERVICEDISPLAYNAME) );
 
// Create the service's Service Connection Point (SCP).
dwStatus = ScpCreate(
        2000,                 // Service default port number
        szServiceClass,       // Specifies the service class string
        szServiceAccountSAM,  // SAM name of logon account for ACE
        szDNofSCP             // Buffer returns the DN of the SCP
        );
if (dwStatus != 0) {
    _tprintf(TEXT("ScpCreate failed: %d\n"), dwStatus );
    DeleteService(schService);
    goto cleanup;
}
 
// Compose and register a service principal name for this service.
// This is performed on the install path because this requires elevated
// privileges for updating the directory.
// If a local account of the format ".\user name", skip the SPN.
if ( szServiceAccountSAM[0] == '.' ) 
{
    _tprintf(TEXT("Do not register SPN for a local account.\n"));
    goto cleanup;
}
 
dwStatus = SpnCompose(
        &pspn,            // Receives pointer to the SPN array.
        &ulSpn,           // Receives number of SPNs returned.
        szDNofSCP,        // Input: DN of the SCP.
        szServiceClass);  // Input: the service's class string.
 
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
        szServiceAccountDN,  // Account on which SPNs are registered.
        pspn,                // Array of SPNs to register.
        ulSpn,               // Number of SPNs in array.
        DS_SPN_ADD_SPN_OP);  // Operation code: Add SPNs.
 
if (dwStatus != NO_ERROR) 
{
    _tprintf(TEXT("Failed to compose SPN: Error was %X\n"), 
                  dwStatus);
    DeleteService(schService);
    ScpDelete(szDNofSCP, szServiceClass, szServiceAccountDN);
    goto cleanup;
}
 
cleanup:
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (schService)
    CloseServiceHandle(schService);
DsFreeSpnArray(ulSpn, pspn);
return;
}
```



Pour plus d’informations sur l’exemple de code précédent, consultez [composition des noms de principal du service pour un service avec un SCP](composing-the-spns-for-a-service-with-an-scp.md) et [enregistrement des noms de principal du service pour un service](registering-the-spns-for-a-service.md).

 

 