---
description: Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui effectue l’initialisation COM, se connecte à WMI sur un ordinateur distant, obtient les données semisynchronously, puis nettoie.
ms.assetid: 30e65b9e-9372-46d1-843a-bda0d6ec1c69
ms.tgt_platform: multiple
title: 'Exemple : obtention de données WMI à partir d’un ordinateur distant'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3375bd25073defa92358f697ee4165ddb57793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541199"
---
# <a name="example-getting-wmi-data-from-a-remote-computer"></a><span data-ttu-id="c2271-103">Exemple : obtention de données WMI à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="c2271-103">Example: Getting WMI Data from a Remote Computer</span></span>

<span data-ttu-id="c2271-104">Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui effectue l’initialisation COM, se connecte à WMI sur un ordinateur distant, obtient les données semisynchronously, puis nettoie.</span><span class="sxs-lookup"><span data-stu-id="c2271-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on a remote computer, gets data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="c2271-105">Pour plus d’informations sur l’obtention de données à partir de l’ordinateur local, consultez [exemple : obtention de données WMI à partir de l’ordinateur local](example--getting-wmi-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-105">For more information about how to get data from the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md).</span></span> <span data-ttu-id="c2271-106">Pour plus d’informations sur l’obtention des données de manière asynchrone, consultez [exemple : obtention de données WMI à partir de l’ordinateur local de manière asynchrone](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-106">For more information about how to get the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

> [!Note]  
> <span data-ttu-id="c2271-107">Si vous essayez de vous connecter à un ordinateur distant, reportez-vous aux informations contenues dans[connexion à WMI à distance](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-107">If you are trying to connect to a remote computer refer to the information in[Connecting to WMI Remotely](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

 

<span data-ttu-id="c2271-108">La procédure suivante montre comment exécuter l’application WMI.</span><span class="sxs-lookup"><span data-stu-id="c2271-108">The following procedure shows how to execute the WMI application.</span></span> <span data-ttu-id="c2271-109">Les étapes 1 à 5 contiennent toutes les étapes nécessaires à la configuration et à la connexion à WMI, et les étapes 6 et 7 sont l’endroit où les données sont interrogées et reçues.</span><span class="sxs-lookup"><span data-stu-id="c2271-109">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

<span data-ttu-id="c2271-110">**Pour obtenir des données WMI à partir d’un ordinateur distant**</span><span class="sxs-lookup"><span data-stu-id="c2271-110">**To get WMI data from a remote computer**</span></span>

1.  <span data-ttu-id="c2271-111">Initialisez les paramètres COM avec un appel à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="c2271-111">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="c2271-112">Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-112">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="c2271-113">Initialisez la sécurité des processus COM en appelant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c2271-113">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="c2271-114">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-114">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="c2271-115">Obtenez le localisateur initial pour WMI en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c2271-115">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="c2271-116">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-116">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="c2271-117">Obtenez un pointeur vers [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour l' \\ \\ \\ espace de noms CIMV2 racine sur un ordinateur distant en appelant [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="c2271-117">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the \\\\root\\cimv2 namespace on a remote computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="c2271-118">Lorsque vous vous connectez à un ordinateur distant, vous devez connaître le nom de l’ordinateur, le domaine, le nom d’utilisateur et le mot de passe de l’ordinateur distant auquel vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="c2271-118">When connecting to a remote computer, you need to know the computer name, domain, user name, and password of the remote computer you are connecting to.</span></span> <span data-ttu-id="c2271-119">Ces attributs sont tous passés dans la méthode **IWbemLocator :: ConnectServer** .</span><span class="sxs-lookup"><span data-stu-id="c2271-119">These attributes are all passed into the **IWbemLocator::ConnectServer** method.</span></span> <span data-ttu-id="c2271-120">Vérifiez également que le nom d’utilisateur sur l’ordinateur qui tente de se connecter à l’ordinateur distant dispose des privilèges d’accès appropriés sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c2271-120">Also, ensure the user name on the computer that is trying to connect to the remote computer has the correct access privileges on the remote computer.</span></span> <span data-ttu-id="c2271-121">Pour plus d’informations, consultez [connexion via le pare-feu Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="c2271-121">For more information, see [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="c2271-122">Pour vous connecter à l’ordinateur local, consultez [exemple : obtention de données WMI à partir de l’ordinateur local](example--getting-wmi-data-from-the-local-computer.md) et [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-122">To connect to the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md) and [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="c2271-123">Lors de la gestion des noms d’utilisateur et des mots de passe, il est recommandé que l’utilisateur soit invité à saisir les informations, à utiliser les informations, puis à supprimer les informations, afin qu’il y ait moins de risque que les informations soient interceptées par un utilisateur non autorisé.</span><span class="sxs-lookup"><span data-stu-id="c2271-123">When handling user names and passwords, it is recommended that the user be prompted for the information, use the information, and then delete the information, so that there is less of a chance of the information being intercepted by an unauthorized user.</span></span> <span data-ttu-id="c2271-124">L’étape 4 de l’exemple de code ci-dessous utilise [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) pour obtenir le nom d’utilisateur et le mot de passe, puis utilise [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) pour supprimer les informations une fois qu’elles sont utilisées dans [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="c2271-124">Step 4 in the example code below uses [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to get the user name and password, and then uses [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) to get rid of the information after it is used in [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="c2271-125">Pour plus d’informations, consultez [gestion des mots de passe](/windows/desktop/SecBP/handling-passwords) et [demande d’informations d’identification à l’utilisateur](/windows/desktop/SecBP/asking-the-user-for-credentials) sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="c2271-125">For more information, see [Handling Passwords](/windows/desktop/SecBP/handling-passwords) and [Asking the User for Credentials](/windows/desktop/SecBP/asking-the-user-for-credentials) on MSDN.</span></span>

5.  <span data-ttu-id="c2271-126">Créez une structure [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) pour fournir les informations d’identification permettant de définir la sécurité du proxy.</span><span class="sxs-lookup"><span data-stu-id="c2271-126">Create a [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) structure to provide credentials for setting the proxy security.</span></span>
6.  <span data-ttu-id="c2271-127">Définir la sécurité du proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) afin que le service WMI puisse emprunter l’identité du client en appelant [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="c2271-127">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="c2271-128">Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-128">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

7.  <span data-ttu-id="c2271-129">Utilisez le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour effectuer des demandes WMI.</span><span class="sxs-lookup"><span data-stu-id="c2271-129">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="c2271-130">Une requête est exécutée pour obtenir le nom du système d’exploitation et la quantité de mémoire physique libre en appelant [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="c2271-130">A query is executed to obtain the name of the operating system and the amount of free physical memory by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="c2271-131">La requête WQL suivante est l’un des arguments de méthode.</span><span class="sxs-lookup"><span data-stu-id="c2271-131">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="c2271-132">Le résultat de cette requête est stocké dans un pointeur [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="c2271-132">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="c2271-133">Cela permet aux objets de données de la requête d’être récupérés semisynchronously avec l’interface **IEnumWbemClassObject** .</span><span class="sxs-lookup"><span data-stu-id="c2271-133">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="c2271-134">Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-134">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="c2271-135">Pour obtenir les données de manière asynchrone, consultez [exemple : obtention de données WMI à partir de l’ordinateur local de manière asynchrone](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-135">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="c2271-136">Pour plus d’informations sur la création de requêtes WMI, consultez [manipulation d’informations de classes et d’instances](manipulating-class-and-instance-information.md), [interrogation de WMI](querying-wmi.md)et [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-136">For more information about making requests of WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

8.  <span data-ttu-id="c2271-137">Définir la sécurité du proxy de l’énumérateur [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="c2271-137">Set [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) enumerator proxy security.</span></span> <span data-ttu-id="c2271-138">Veillez à effacer les informations d’identification de la mémoire une fois que vous avez fini de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="c2271-138">Make sure to erase the credentials from memory after you have finished using them.</span></span>

    <span data-ttu-id="c2271-139">Pour plus d’informations, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-139">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

9.  <span data-ttu-id="c2271-140">Obtenir et afficher les données de la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="c2271-140">Get and display the data from the WQL query.</span></span> <span data-ttu-id="c2271-141">Le pointeur [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) est lié aux objets de données retournés par la requête, et les objets de données peuvent être récupérés avec la méthode [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="c2271-141">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="c2271-142">Cette méthode lie les objets de données à un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) passé dans la méthode.</span><span class="sxs-lookup"><span data-stu-id="c2271-142">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="c2271-143">Utilisez la méthode [**IWbemClassObject :: obten**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) pour récupérer les informations souhaitées à partir des objets de données.</span><span class="sxs-lookup"><span data-stu-id="c2271-143">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="c2271-144">L’exemple de code suivant est utilisé pour récupérer la `Name` propriété de l’objet de données, qui fournit le nom du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c2271-144">The following code example is used to get the `Name` property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    wcout << " OS Name : " << vtProp.bstrVal << endl;
    ```

    

    <span data-ttu-id="c2271-145">Une fois que la valeur de la `Name` propriété est stockée dans la variable de [**type Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) `vtProp` , elle peut être affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2271-145">Once the value of the `Name` property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable `vtProp`, it can then be displayed to the user.</span></span>

    <span data-ttu-id="c2271-146">L’exemple de code suivant montre comment la variable [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) peut être réutilisée pour stocker et afficher la valeur de la quantité de mémoire physique disponible.</span><span class="sxs-lookup"><span data-stu-id="c2271-146">The following code example shows how the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable can be used again to store and display the value of the amount of free physical memory.</span></span>

    ```C++
    hr = pclsObj->Get(L"FreePhysicalMemory",
        0, &vtProp, 0, 0);
    wcout << " Free physical memory (in kilobytes): "
        << vtProp.uintVal << endl;
    ```

    

    <span data-ttu-id="c2271-147">Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c2271-147">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="c2271-148">L’exemple de code suivant montre comment obtenir des données WMI semisynchronously à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c2271-148">The following code example shows how to get WMI data semisynchronously from a remote computer.</span></span>


```C++
#define _WIN32_DCOM
#define UNICODE
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "comsuppw.lib")
#include <wincred.h>
#include <strsafe.h>

int __cdecl main(int argc, char **argv)
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

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IDENTIFY,    // Default Impersonation  
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
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;

    // Get the user name and password for the remote computer
    CREDUI_INFO cui;
    bool useToken = false;
    bool useNTLM = true;
    wchar_t pszName[CREDUI_MAX_USERNAME_LENGTH+1] = {0};
    wchar_t pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1] = {0};
    wchar_t pszDomain[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszUserName[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszAuthority[CREDUI_MAX_USERNAME_LENGTH+1];
    BOOL fSave;
    DWORD dwErr;

    memset(&cui,0,sizeof(CREDUI_INFO));
    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    // Ensure that MessageText and CaptionText identify
    // what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Press cancel to use process token");
    cui.pszCaptionText = TEXT("Enter Account Information");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    dwErr = CredUIPromptForCredentials( 
        &cui,                             // CREDUI_INFO structure
        TEXT(""),                         // Target for credentials
        NULL,                             // Reserved
        0,                                // Reason
        pszName,                          // User name
        CREDUI_MAX_USERNAME_LENGTH+1,     // Max number for user name
        pszPwd,                           // Password
        CREDUI_MAX_PASSWORD_LENGTH+1,     // Max number for password
        &fSave,                           // State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |// flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr == ERROR_CANCELLED)
    {
        useToken = true;
    }
    else if (dwErr)
    {
        cout << "Did not get credentials " << dwErr << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;      
    }

    // change the computerName strings below to the full computer name
    // of the remote computer
    if(!useNTLM)
    {
        StringCchPrintf(pszAuthority, CREDUI_MAX_USERNAME_LENGTH+1, L"kERBEROS:%s", L"COMPUTERNAME");
    }

    // Connect to the remote root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    //---------------------------------------------------------
   
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTERNAME\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
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


    // step 5: --------------------------------------------------
    // Create COAUTHIDENTITY that can be used for setting security on proxy

    COAUTHIDENTITY *userAcct =  NULL ;
    COAUTHIDENTITY authIdent;

    if( !useToken )
    {
        memset(&authIdent, 0, sizeof(COAUTHIDENTITY));
        authIdent.PasswordLength = wcslen (pszPwd);
        authIdent.Password = (USHORT*)pszPwd;

        LPWSTR slash = wcschr (pszName, L'\\');
        if( slash == NULL )
        {
            cout << "Could not create Auth identity. No domain specified\n" ;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return 1;               // Program has failed.
        }

        StringCchCopy(pszUserName, CREDUI_MAX_USERNAME_LENGTH+1, slash+1);
        authIdent.User = (USHORT*)pszUserName;
        authIdent.UserLength = wcslen(pszUserName);

        StringCchCopyN(pszDomain, CREDUI_MAX_USERNAME_LENGTH+1, pszName, slash - pszName);
        authIdent.Domain = (USHORT*)pszDomain;
        authIdent.DomainLength = slash - pszName;
        authIdent.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

        userAcct = &authIdent;

    }

    // Step 6: --------------------------------------------------
    // Set security levels on a WMI connection ------------------

    hres = CoSetProxyBlanket(
       pSvc,                           // Indicates the proxy to set
       RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
       COLE_DEFAULT_PRINCIPAL,         // Server principal name 
       RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
       userAcct,                       // client identity
       EOAC_NONE                       // proxy capabilities 
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

    // Step 7: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("Select * from Win32_OperatingSystem"),
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
        return 1;               // Program has failed.
    }

    // Step 8: -------------------------------------------------
    // Secure the enumerator proxy
    hres = CoSetProxyBlanket(
        pEnumerator,                    // Indicates the proxy to set
        RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
        RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
        COLE_DEFAULT_PRINCIPAL,         // Server principal name 
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
        userAcct,                       // client identity
        EOAC_NONE                       // proxy capabilities 
        );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket on enumerator. Error code = 0x" 
             << hex << hres << endl;
        pEnumerator->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // When you have finished using the credentials,
    // erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    SecureZeroMemory(pszUserName, sizeof(pszUserName));
    SecureZeroMemory(pszDomain, sizeof(pszDomain));


    // Step 9: -------------------------------------------------
    // Get the data from the query in step 7 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;

        // Get the value of the FreePhysicalMemory property
        hr = pclsObj->Get(L"FreePhysicalMemory",
            0, &vtProp, 0, 0);
        wcout << " Free physical memory (in kilobytes): "
            << vtProp.uintVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
        pclsObj = NULL;
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    if( pclsObj )
    {
        pclsObj->Release();
    }
    
    CoUninitialize();

    return 0;   // Program successfully completed.
    
}
```



 

 
