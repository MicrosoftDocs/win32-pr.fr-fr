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
# <a name="installing-a-service-on-a-host-computer"></a><span data-ttu-id="628b0-103">Installation d’un service sur un ordinateur hôte</span><span class="sxs-lookup"><span data-stu-id="628b0-103">Installing a Service on a Host Computer</span></span>

<span data-ttu-id="628b0-104">L’exemple de code suivant montre les étapes de base de l’installation d’un service activé pour les annuaires sur un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="628b0-104">The following code example shows the basic steps of installing a directory-enabled service on a host computer.</span></span> <span data-ttu-id="628b0-105">Il effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="628b0-105">It performs the following operations:</span></span>

1.  <span data-ttu-id="628b0-106">Appelle la fonction [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) pour ouvrir un handle vers le gestionnaire de contrôle des services (SCM) sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="628b0-106">Calls the [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) function to open a handle to the service control manager (SCM) on the local computer.</span></span>
2.  <span data-ttu-id="628b0-107">Appelle la fonction [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) pour installer le service dans la base de données SCM.</span><span class="sxs-lookup"><span data-stu-id="628b0-107">Calls the [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) function to install the service in the SCM database.</span></span> <span data-ttu-id="628b0-108">Cet appel spécifie le compte et le mot de passe d’ouverture de session du service, ainsi que l’exécutable du service et d’autres informations sur le service.</span><span class="sxs-lookup"><span data-stu-id="628b0-108">This call specifies the service's logon account and password, as well as the service's executable and other information about the service.</span></span> <span data-ttu-id="628b0-109">**CreateService** échoue si le compte d’ouverture de session spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="628b0-109">**CreateService** fails if the specified logon account is invalid.</span></span> <span data-ttu-id="628b0-110">Toutefois, **CreateService** ne vérifie pas la validité du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="628b0-110">However, **CreateService** does not check the validity of the password.</span></span> <span data-ttu-id="628b0-111">Il ne vérifie pas non plus que le compte dispose du droit ouvrir une session en tant que service sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="628b0-111">It also does not verify that the account has the logon as a service right on the local computer.</span></span> <span data-ttu-id="628b0-112">Pour plus d’informations, consultez [accorder des droits d’ouverture de session en tant que service sur l’ordinateur hôte](granting-logon-as-service-right-on-the-host-computer.md).</span><span class="sxs-lookup"><span data-stu-id="628b0-112">For more information, see [Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md).</span></span>
3.  <span data-ttu-id="628b0-113">Appelle la sous-routine **ScpCreate** du service qui crée un objet point de connexion de service (SCP) dans le répertoire pour publier l’emplacement de cette instance du service.</span><span class="sxs-lookup"><span data-stu-id="628b0-113">Calls the service's **ScpCreate** subroutine that creates a service connection point object (SCP) in the directory to publish the location of this instance of the service.</span></span> <span data-ttu-id="628b0-114">Pour plus d’informations, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="628b0-114">For more information, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="628b0-115">Cette routine stocke également les informations de liaison du service dans le SCP, définit une entrée du contrôle d’accès sur le SCP afin que le service puisse y accéder au moment de l’exécution, met en cache le nom unique du SCP dans le registre local et retourne le nom unique du nouveau SCP.</span><span class="sxs-lookup"><span data-stu-id="628b0-115">This routine also stores the service's binding information in the SCP, sets an ACE on the SCP so the service can access it at run time, caches the distinguished name of the SCP in the local registry, and returns the distinguished name of the new SCP.</span></span>
4.  <span data-ttu-id="628b0-116">Appelle la sous-routine **SpnCompose** du service qui utilise la chaîne de classe du service et le nom unique du SCP pour composer un nom de principal du service (SPN).</span><span class="sxs-lookup"><span data-stu-id="628b0-116">Calls the service's **SpnCompose** subroutine that uses the service's class string and the distinguished name of the SCP to compose a service principal name (SPN).</span></span> <span data-ttu-id="628b0-117">Pour plus d’informations, consultez [composition des noms de principal du service pour un service avec SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="628b0-117">For more information, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="628b0-118">Le SPN identifie de manière unique cette instance du service.</span><span class="sxs-lookup"><span data-stu-id="628b0-118">The SPN uniquely identifies this instance of the service.</span></span>
5.  <span data-ttu-id="628b0-119">Appelle la sous-routine **SpnRegister** du service qui inscrit le SPN sur l’objet de compte associé au compte d’ouverture de session du service.</span><span class="sxs-lookup"><span data-stu-id="628b0-119">Calls the service's **SpnRegister** subroutine that registers the SPN on the account object associated with service's logon account.</span></span> <span data-ttu-id="628b0-120">Pour plus d’informations, consultez [enregistrement des noms de principal du service pour un service](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="628b0-120">For more information, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span> <span data-ttu-id="628b0-121">L’inscription du SPN permet aux applications clientes d’authentifier le service.</span><span class="sxs-lookup"><span data-stu-id="628b0-121">Registration of the SPN enables client applications to authenticate the service.</span></span>

<span data-ttu-id="628b0-122">Cet exemple de code fonctionne correctement, que le compte d’ouverture de session soit un compte d’utilisateur local ou de domaine ou le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="628b0-122">This code example works correctly regardless of whether the logon account is a local or domain user account or the LocalSystem account.</span></span> <span data-ttu-id="628b0-123">Pour un compte d’utilisateur de domaine, le paramètre *szServiceAccountSAM* contient le nom d’utilisateur de \*domaine \*\*\*\\*\*\*\* du compte et le paramètre *szServiceAccountDN* contient le nom unique de l’objet de compte d’utilisateur dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="628b0-123">For a domain user account, the *szServiceAccountSAM* parameter contains the *Domain ***\\*** UserName* name of the account, and the *szServiceAccountDN* parameter contains the distinguished name of the user account object in the directory.</span></span> <span data-ttu-id="628b0-124">Pour le compte LocalSystem, *szServiceAccountSAM* et *szPassword* sont **null**, et *szServiceAccountSN* est le nom unique de l’objet compte de l’ordinateur local dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="628b0-124">For the LocalSystem account, *szServiceAccountSAM* and *szPassword* are **NULL**, and *szServiceAccountSN* is the distinguished name of the local computer's account object in the directory.</span></span> <span data-ttu-id="628b0-125">Si *szServiceAccountSAM* spécifie un compte d’utilisateur local (le format du nom est «». \\ *Nom d'* utilisateur»), l’exemple de code ignore l’inscription du nom de principal du service, car l’authentification mutuelle n’est pas prise en charge pour les comptes d’utilisateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="628b0-125">If *szServiceAccountSAM* specifies a local user account (name format is ".\\*UserName*"), the code example skips the SPN registration because mutual authentication is not supported for local user accounts.</span></span>

<span data-ttu-id="628b0-126">N’oubliez pas que la configuration de sécurité par défaut autorise uniquement les administrateurs de domaine à exécuter ce code.</span><span class="sxs-lookup"><span data-stu-id="628b0-126">Be aware that the default security configuration allows only domain administrators to execute this code.</span></span>

<span data-ttu-id="628b0-127">Sachez également que cet exemple de code, tel qu’il est écrit, doit être exécuté sur l’ordinateur sur lequel le service est installé.</span><span class="sxs-lookup"><span data-stu-id="628b0-127">Also, be aware that this code example, as written, must be executed on the computer where the service is being installed.</span></span> <span data-ttu-id="628b0-128">Par conséquent, il s’agit généralement d’un exécutable d’installation distinct de votre code d’installation de service, le cas échéant, qui étend le schéma, étend l’interface utilisateur ou configure la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="628b0-128">Consequently, it is typically in a separate installation executable from your service installation code, if any, that extends the schema, extends the UI, or sets up group policy.</span></span> <span data-ttu-id="628b0-129">Ces opérations installent des composants de service pour l’ensemble d’une forêt, tandis que ce code installe le service sur un seul ordinateur.</span><span class="sxs-lookup"><span data-stu-id="628b0-129">Those operations install service components for an entire a forest, whereas this code installs the service on a single computer.</span></span>


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



<span data-ttu-id="628b0-130">Pour plus d’informations sur l’exemple de code précédent, consultez [composition des noms de principal du service pour un service avec un SCP](composing-the-spns-for-a-service-with-an-scp.md) et [enregistrement des noms de principal du service pour un service](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="628b0-130">For more information about the previous code example, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md) and [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

 

 