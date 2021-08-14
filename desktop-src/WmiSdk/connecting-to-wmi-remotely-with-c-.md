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
ms.openlocfilehash: 9f9ed735a1440d124a065a9f509eac7c58b1fded9be0683e361903b9f02fc1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319437"
---
# <a name="connecting-to-wmi-remotely-with-c"></a>Connexion à WMI à distance avec C #

Comme avec d’autres langages tels que PowerShell, VBScript ou C++, vous pouvez utiliser C# pour surveiller à distance le matériel et les logiciels sur des ordinateurs distants. Les connexions à distance pour le code managé sont accomplies par le biais de l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) . (Les versions précédentes de WMI utilisaient l’espace de noms [System. Management](/dotnet/api/system.management) , qui est inclus ici à des fins d’exhaustivité.)

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

La connexion à distance à l’aide de classes dans l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) utilise DCOM en tant que mécanisme distant sous-jacent. Les connexions distantes WMI doivent être conformes aux critères de sécurité DCOM en matière d'emprunt d'identité et d'authentification. Par défaut, une étendue est liée à l’ordinateur local et à l' \\ espace de noms système « root cimv2 ». Toutefois, vous pouvez modifier à la fois l’ordinateur, le domaine et l’espace de noms WMI auxquels vous accédez. Vous pouvez également définir l’autorité, l’emprunt d’identité, les informations d’identification et d’autres options de connexion.

**Pour vous connecter à WMI à distance avec C# (Microsoft. Management. infrastructure)**

1.  Créez une session sur l’ordinateur distant avec un appel à [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).

    Si vous vous connectez à un ordinateur distant en utilisant les mêmes informations d’identification (domaine et nom d’utilisateur) que vous avez ouvert une session, vous pouvez spécifier le nom de l’ordinateur dans l’appel de [création](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) . Une fois que vous avez l’objet [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) retourné, vous pouvez créer votre requête WMI.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    Pour plus d’informations sur la création de requêtes WMI avec l’API **Microsoft. Management. infrastructure** en C#, consultez [récupération des données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).

2.  Si vous souhaitez définir des options différentes pour votre connexion, telles que des informations d’identification différentes, des paramètres régionaux ou des niveaux d’emprunt d’identité, vous devez utiliser un objet [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) dans votre appel à [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).

    [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) est une classe de base pour [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) et [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)). Vous pouvez utiliser l’un ou l’autre pour définir les options de vos sessions WS-Man et DCOM, respectivement. L’exemple de code suivant décrit l’utilisation d’un objet [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) pour définir le niveau d’emprunt d’identité sur emprunter l’identité.

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  Si vous souhaitez définir les informations d’identification de votre connexion, vous devez créer et ajouter un objet [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) à votre [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).

    L’exemple de code suivant décrit la création d’une classe [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , son remplissage avec le [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))approprié et son utilisation dans un appel [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .

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

    

    Il est généralement recommandé de ne pas coder en dur un mot de passe dans vos applications. comme l’illustre l’exemple de code ci-dessus, chaque fois que cela est possible, essayez d’interroger votre utilisateur pour obtenir le mot de passe et de le stocker en toute sécurité.

WMI a été conçu pour contrôler le matériel et les logiciels sur des ordinateurs distants. Les connexions à distance pour WMI v1 s’effectuent via l’objet [ManagementScope](/dotnet/api/system.management.managementscope) .

**Pour vous connecter à WMI à distance avec C# (System. Management)**

1.  Créez un objet [ManagementScope](/dotnet/api/system.management.managementscope) , en utilisant le nom de l’ordinateur et le chemin d’accès WMI, et connectez-vous à votre cible à l’aide d’un appel à ManagementScope. Connecter ().

    Si vous vous connectez à un ordinateur distant en utilisant les mêmes informations d’identification (domaine et nom d’utilisateur) que vous utilisez pour vous connecter, vous devez uniquement spécifier le chemin d’accès WMI. Une fois que vous êtes connecté, vous pouvez effectuer votre requête WMI.

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    Pour plus d’informations sur la création de requêtes WMI avec l’API [System. Management](/dotnet/api/system.management) en C#, consultez [extraction de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).

2.  Si vous vous connectez à un ordinateur distant dans un autre domaine ou à l’aide d’un nom d’utilisateur et d’un mot de passe différents, vous devez utiliser un objet [ConnectionOptions](/dotnet/api/system.management.connectionoptions) dans l’appel à [ManagementScope](/dotnet/api/system.management.managementscope).

    Le [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contient des propriétés pour décrire l’authentification, l’emprunt d’identité, le nom d’utilisateur, le mot de passe et d’autres options de connexion. L’exemple de code suivant décrit l’utilisation d’un [ConnectionOptions](/dotnet/api/system.management.connectionoptions) pour définir le niveau d’emprunt d’identité sur emprunter l’identité.

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    En règle générale, il est recommandé de définir le niveau d’emprunt d’identité sur emprunter l’identité, sauf si cela est explicitement requis. Essayez également d’éviter d’écrire votre nom et votre mot de passe dans le code C#. (Si possible, consultez si vous pouvez demander à l’utilisateur de le fournir dynamiquement au moment de l’exécution.)

    Pour obtenir plus d’exemples de définition de propriétés différentes sur une connexion WMI distante, consultez la section Exemples de la page de référence [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .

## <a name="microsoftmanagementinfrastructure-example"></a>Exemple Microsoft. Management. infrastructure

L’exemple de code C# suivant, basé sur le billet [de blog suivant sur TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), explique comment utiliser [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) et [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) pour définir des informations d’identification sur une connexion à distance.


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



## <a name="systemmanagement-example"></a>Exemple System. Management

L’exemple de code C# suivant décrit une connexion à distance générale, à l’aide des objets System. Management.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
