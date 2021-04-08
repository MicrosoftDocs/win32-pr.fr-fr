---
description: Comme avec d’autres langages tels que PowerShell, VBScript ou C++, vous pouvez utiliser C# pour surveiller à distance le matériel et les logiciels sur des ordinateurs distants.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Connexion à WMI à distance avec C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ad9fe2008b52276a8f68149b33ae3729daaf7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034935"
---
# <a name="connecting-to-wmi-remotely-with-c"></a><span data-ttu-id="dbf8d-103">Connexion à WMI à distance avec C #</span><span class="sxs-lookup"><span data-stu-id="dbf8d-103">Connecting to WMI Remotely with C#</span></span>

<span data-ttu-id="dbf8d-104">Comme avec d’autres langages tels que PowerShell, VBScript ou C++, vous pouvez utiliser C# pour surveiller à distance le matériel et les logiciels sur des ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-104">As with other languages such as PowerShell, VBScript, or C++, you can use C# to remotely monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="dbf8d-105">Les connexions à distance pour le code managé sont accomplies par le biais de l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dbf8d-105">Remote connections for managed code are accomplished through the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace.</span></span> <span data-ttu-id="dbf8d-106">(Les versions précédentes de WMI utilisaient l’espace de noms [System. Management](/dotnet/api/system.management) , qui est inclus ici à des fins d’exhaustivité.)</span><span class="sxs-lookup"><span data-stu-id="dbf8d-106">(Previous versions of WMI used the [System.Management](/dotnet/api/system.management) namespace, which is included here for completeness.)</span></span>

> [!Note]  
> <span data-ttu-id="dbf8d-107">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-107">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="dbf8d-108">La connexion à distance à l’aide de classes dans l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) utilise DCOM en tant que mécanisme distant sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-108">Connecting remotely using classes in the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace uses DCOM as the underlying remote mechanism.</span></span> <span data-ttu-id="dbf8d-109">Les connexions distantes WMI doivent être conformes aux critères de sécurité DCOM en matière d'emprunt d'identité et d'authentification.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-109">WMI remote connections must comply with DCOM security requirements for impersonation and authentication.</span></span> <span data-ttu-id="dbf8d-110">Par défaut, une étendue est liée à l’ordinateur local et à l' \\ espace de noms système « root cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="dbf8d-110">By default, a scope is bound to the local computer and the "Root\\CIMv2" system namespace.</span></span> <span data-ttu-id="dbf8d-111">Toutefois, vous pouvez modifier à la fois l’ordinateur, le domaine et l’espace de noms WMI auxquels vous accédez.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-111">However, you can change both the computer, domain, and WMI namespace that you access.</span></span> <span data-ttu-id="dbf8d-112">Vous pouvez également définir l’autorité, l’emprunt d’identité, les informations d’identification et d’autres options de connexion.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-112">You can also set authority, impersonation, credentials, and other connection options.</span></span>

<span data-ttu-id="dbf8d-113">**Pour vous connecter à WMI à distance avec C# (Microsoft. Management. infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="dbf8d-113">**To connect to WMI remotely with C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="dbf8d-114">Créez une session sur l’ordinateur distant avec un appel à [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbf8d-114">Create a session on the remote machine with a call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span></span>

    <span data-ttu-id="dbf8d-115">Si vous vous connectez à un ordinateur distant en utilisant les mêmes informations d’identification (domaine et nom d’utilisateur) que vous avez ouvert une session, vous pouvez spécifier le nom de l’ordinateur dans l’appel de [création](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dbf8d-115">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the name of the computer in the [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) call.</span></span> <span data-ttu-id="dbf8d-116">Une fois que vous avez l’objet [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) retourné, vous pouvez créer votre requête WMI.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-116">Once you have the returned [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object, you can then make your WMI query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    <span data-ttu-id="dbf8d-117">Pour plus d’informations sur la création de requêtes WMI avec l’API **Microsoft. Management. infrastructure** en C#, consultez [récupération des données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8d-117">For more information on making WMI queries with the **Microsoft.Management.Infrastructure** API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="dbf8d-118">Si vous souhaitez définir des options différentes pour votre connexion, telles que des informations d’identification différentes, des paramètres régionaux ou des niveaux d’emprunt d’identité, vous devez utiliser un objet [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) dans votre appel à [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbf8d-118">If you wish to set different options for your connection, such as different credentials, locale or Impersonation levels, you need to use a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) object in your call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span></span>

    <span data-ttu-id="dbf8d-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) est une classe de base pour [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) et [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbf8d-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) is a base class for [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) and [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span></span> <span data-ttu-id="dbf8d-120">Vous pouvez utiliser l’un ou l’autre pour définir les options de vos sessions WS-Man et DCOM, respectivement.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-120">You can use either to set the options on your WS-Man and DCOM sessions, respectively.</span></span> <span data-ttu-id="dbf8d-121">L’exemple de code suivant décrit l’utilisation d’un objet [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) pour définir le niveau d’emprunt d’identité sur emprunter l’identité.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-121">The following code sample describes using a [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) object to set the Impersonation level to Impersonate.</span></span>

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  <span data-ttu-id="dbf8d-122">Si vous souhaitez définir les informations d’identification de votre connexion, vous devez créer et ajouter un objet [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) à votre [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbf8d-122">If you wish to set the credentials for your connection, you will need to create and add a [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) object to your [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span></span>

    <span data-ttu-id="dbf8d-123">L’exemple de code suivant décrit la création d’une classe [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , son remplissage avec le [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))approprié et son utilisation dans un appel [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dbf8d-123">The following code sample describes creating a [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) class, filling it with the proper [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)), and using it in a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) call.</span></span>

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    <span data-ttu-id="dbf8d-124">Il est généralement recommandé de ne pas coder en dur un mot de passe dans vos applications. comme l’illustre l’exemple de code ci-dessus, chaque fois que cela est possible, essayez d’interroger votre utilisateur pour obtenir le mot de passe et de le stocker en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-124">It is generally recommended that you do not hardcode a password into your applications; as the above code sample indicates, whenever possible try to query your user for the password, and store it securely.</span></span>

<span data-ttu-id="dbf8d-125">WMI a été conçu pour contrôler le matériel et les logiciels sur des ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-125">WMI is intended to monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="dbf8d-126">Les connexions à distance pour WMI v1 s’effectuent via l’objet [ManagementScope](/dotnet/api/system.management.managementscope) .</span><span class="sxs-lookup"><span data-stu-id="dbf8d-126">Remote connections for WMI v1 is accomplished through the [ManagementScope](/dotnet/api/system.management.managementscope) object.</span></span>

<span data-ttu-id="dbf8d-127">**Pour vous connecter à WMI à distance avec C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="dbf8d-127">**To connect to WMI remotely with C# (System.Management)**</span></span>

1.  <span data-ttu-id="dbf8d-128">Créez un objet [ManagementScope](/dotnet/api/system.management.managementscope) , en utilisant le nom de l’ordinateur et le chemin d’accès WMI, et connectez-vous à votre cible à l’aide d’un appel à ManagementScope. Connect ().</span><span class="sxs-lookup"><span data-stu-id="dbf8d-128">Create a [ManagementScope](/dotnet/api/system.management.managementscope) object, using the name of the computer and the WMI path, and connect to your target with a call to ManagementScope.Connect().</span></span>

    <span data-ttu-id="dbf8d-129">Si vous vous connectez à un ordinateur distant en utilisant les mêmes informations d’identification (domaine et nom d’utilisateur) que vous utilisez pour vous connecter, vous devez uniquement spécifier le chemin d’accès WMI.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-129">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you only have to specify the WMI path.</span></span> <span data-ttu-id="dbf8d-130">Une fois que vous êtes connecté, vous pouvez effectuer votre requête WMI.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-130">Once you have connected, you can make your WMI query.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    <span data-ttu-id="dbf8d-131">Pour plus d’informations sur la création de requêtes WMI avec l’API [System. Management](/dotnet/api/system.management) en C#, consultez [extraction de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8d-131">For more information on making WMI queries with the [System.Management](/dotnet/api/system.management) API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="dbf8d-132">Si vous vous connectez à un ordinateur distant dans un autre domaine ou à l’aide d’un nom d’utilisateur et d’un mot de passe différents, vous devez utiliser un objet [ConnectionOptions](/dotnet/api/system.management.connectionoptions) dans l’appel à [ManagementScope](/dotnet/api/system.management.managementscope).</span><span class="sxs-lookup"><span data-stu-id="dbf8d-132">If you connect to a remote computer in a different domain or using a different user name and password, then you must use a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) object in the call to the [ManagementScope](/dotnet/api/system.management.managementscope).</span></span>

    <span data-ttu-id="dbf8d-133">Le [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contient des propriétés pour décrire l’authentification, l’emprunt d’identité, le nom d’utilisateur, le mot de passe et d’autres options de connexion.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-133">The [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contains properties for describing the Authentication, Impersonation, username, password, and other connection options.</span></span> <span data-ttu-id="dbf8d-134">L’exemple de code suivant décrit l’utilisation d’un [ConnectionOptions](/dotnet/api/system.management.connectionoptions) pour définir le niveau d’emprunt d’identité sur emprunter l’identité.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-134">The following code sample describes using a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) to set the Impersonation Level to Impersonate.</span></span>

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    <span data-ttu-id="dbf8d-135">En règle générale, il est recommandé de définir le niveau d’emprunt d’identité sur emprunter l’identité, sauf si cela est explicitement requis.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-135">Generally speaking, it is recommended that you set your Impersonation level to Impersonate unless explicitly needed otherwise.</span></span> <span data-ttu-id="dbf8d-136">Essayez également d’éviter d’écrire votre nom et votre mot de passe dans le code C#.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-136">Further, try to avoid writing your name and password into C# code.</span></span> <span data-ttu-id="dbf8d-137">(Si possible, consultez si vous pouvez demander à l’utilisateur de le fournir dynamiquement au moment de l’exécution.)</span><span class="sxs-lookup"><span data-stu-id="dbf8d-137">(If possible, see if you can query the user to dynamically supply them at runtime.)</span></span>

    <span data-ttu-id="dbf8d-138">Pour obtenir plus d’exemples de définition de propriétés différentes sur une connexion WMI distante, consultez la section Exemples de la page de référence [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="dbf8d-138">For more examples of setting different properties on a remote WMI connection, see the Examples section of the [ConnectionOptions](/dotnet/api/system.management.connectionoptions) reference page.</span></span>

## <a name="microsoftmanagementinfrastructure-example"></a><span data-ttu-id="dbf8d-139">Exemple Microsoft. Management. infrastructure</span><span class="sxs-lookup"><span data-stu-id="dbf8d-139">Microsoft.Management.Infrastructure Example</span></span>

<span data-ttu-id="dbf8d-140">L’exemple de code C# suivant, basé sur le billet [de blog suivant sur TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), explique comment utiliser [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) et [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) pour définir des informations d’identification sur une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-140">The following C# code example, based on the following [blog post on TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), describes how to use [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) and [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) to set credentials on a remote connection.</span></span>


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a><span data-ttu-id="dbf8d-141">Exemple System. Management</span><span class="sxs-lookup"><span data-stu-id="dbf8d-141">System.Management Example</span></span>

<span data-ttu-id="dbf8d-142">L’exemple de code C# suivant décrit une connexion à distance générale, à l’aide des objets System. Management.</span><span class="sxs-lookup"><span data-stu-id="dbf8d-142">The following C# code sample describes a general remote connection, using the System.Management objects.</span></span>


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="dbf8d-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbf8d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf8d-144">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="dbf8d-144">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
