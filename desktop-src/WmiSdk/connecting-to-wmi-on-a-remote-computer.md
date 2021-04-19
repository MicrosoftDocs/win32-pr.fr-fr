---
description: Décrit comment les scripts, les applications et les fournisseurs peuvent établir des connexions à WMI sur des ordinateurs distants pour obtenir des données ou contrôler le matériel et les logiciels.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Connexion à WMI sur un ordinateur distant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536760"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a>Connexion à WMI sur un ordinateur distant

WMI peut être utilisé pour gérer et accéder aux données WMI sur des ordinateurs distants. Les connexions distantes dans WMI sont affectées par les paramètres du [pare-feu Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) et de DCOM. [Le contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905108(v=msdn.10)) peut également nécessiter des modifications de certains paramètres. Toutefois, une fois que vos paramètres sont corrects, l’appel à un système distant est très similaire à un appel WMI local. Toutefois, vous pouvez choisir de le rendre plus complexe en utilisant des informations d’identification différentes, des protocoles d’authentification supplémentaires et d’autres fonctionnalités de sécurité.

## <a name="configuring-a-computer-for-a-remote-connection"></a>Configuration d’un ordinateur pour une connexion à distance

Avant de pouvoir accéder à un système distant avec WMI, vous devrez peut-être vérifier certains paramètres de sécurité pour confirmer que vous disposez d’un accès. Plus précisément :

-   Windows contient un certain nombre de fonctionnalités de sécurité qui peuvent bloquer l’accès aux scripts sur les systèmes distants. Par conséquent, vous devrez peut-être modifier les paramètres de Active Directory et du pare-feu Windows de votre système avant d’effectuer un appel WMI. Pour plus d’informations, consultez [configuration d’une connexion WMI à distance](connecting-to-wmi-remotely-starting-with-vista.md) et [résolution des problèmes liés à une connexion WMI à distance](troubleshooting-a-remote-wmi-connection.md).

-   Les paramètres DCOM corrects doivent être activés pour qu’une connexion à distance fonctionne. La modification des paramètres DCOM peut permettre aux utilisateurs avec des droits limités d’accéder à un ordinateur pour une connexion à distance. Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md).

En outre, dans certains cas, vous pouvez souhaiter exécuter WMI via un port fixe. Pour ce faire, vous devez également modifier vos paramètres. Pour plus d’informations, consultez [configuration d’un port fixe pour WMI](setting-up-a-fixed-port-for-wmi.md).

## <a name="connecting-to-a-remote-computer"></a>Connexion à un ordinateur distant

Le cœur de la connexion à un système distant avec WMI consiste à s’assurer que vous disposez des autorisations appropriées pour accéder au système et que votre connexion est correctement configurée. Une fois que vous avez ces deux éléments, la connexion elle-même est relativement simple. Par exemple, si vous utilisez vos informations d’identification de sécurité par défaut, vous pouvez accéder à WMI sur un système distant à l’aide du code suivant :

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connexion à WMI à distance avec PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

Utilisez le paramètre *-ComputerName* commun à la plupart des applets de commande WMI, telles que l’applet de commande- [WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connexion à WMI à distance avec VBScript](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

Utilisez un moniker qui contient le nom du système distant dans l’appel à [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connexion à WMI à distance avec C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Pour la version actuelle de l’interface managée WMI ([Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), utilisez l’objet [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) pour représenter une connexion à un hôte distant.


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connexion à WMI à distance avec C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Pour la version V1 de l’interface managée WMI ([System. Management](/dotnet/api/system.management)), utilisez l’objet [ManagementScope](/dotnet/api/system.management.managementscope) pour représenter une connexion à un hôte distant.


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Exemple : obtention de données WMI à partir d’un ordinateur distant (C++)](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

Utilisez la méthode [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) pour spécifier le nom de l’ordinateur distant dans le paramètre *strNetworkResource* .


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

Les exemples de code précédents sont sans doute la connexion à distance la plus simple que vous pouvez effectuer avec WMI. Plus précisément, les exemples supposent les éléments suivants :

-   Vous êtes un administrateur sur la machine distante. En raison du [contrôle de compte d’utilisateur](/previous-versions/aa905108(v=msdn.10)), le compte sur le système distant doit être un compte de domaine dans le groupe administrateurs. Pour plus d’informations, consultez contrôle de compte d’utilisateur et WMI.
-   Le mot de passe sur votre ordinateur local actuel n’est pas vide. Il s’agit essentiellement d’une exigence de sécurité Windows que vous devez avoir connecté à votre système avec un mot de passe.
-   Vos ordinateurs locaux et distants se trouvent dans le même domaine. Si vous avez besoin de franchir les limites d’un domaine, vous devez fournir des informations supplémentaires ou utiliser un modèle de programmation légèrement différent.
-   Vous utilisez votre propre compte pour accéder à la machine distante. Si vous essayez d’accéder à un autre compte, vous devez fournir des informations d’identification supplémentaires. (Notez que la tentative d’accès à WMI localement avec des informations d’identification différentes de votre compte actuel n’est pas autorisée.)
-   Les deux ordinateurs exécutent IPv6. WMI prend en charge les connexions aux ordinateurs exécutant IPv6. Toutefois, votre ordinateur local et « ordinateur \_ B » doivent exécuter IPv6. Les deux ordinateurs peuvent également exécuter IPv4. Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md).
-   Votre script n’a pas besoin de déléguer-autrement dit, il n’a pas besoin d’accéder à des ordinateurs distants supplémentaires par le biais de l’ordinateur distant ciblé. Pour plus d’informations, consultez [délégation avec WMI](connecting-to-a-3rd-computer-delegation.md).
-   Vous essayez d’effectuer un appel spécifique, plutôt que de créer un processus distant. Pour plus d’informations, consultez [création de processus à distance à l’aide de WMI](creating-processes-remotely.md).

Avec ces restrictions à l’esprit, un appel WMI distant est très similaire à un appel WMI local. la seule différence réside dans le fait que vous devez spécifier le nom du système distant. Toutefois, vous pouvez choisir de modifier un grand nombre de ces fonctionnalités : en utilisant des informations d’identification différentes ou en acheminant votre appel via un ordinateur tiers, ou en accédant à un autre domaine.

 

 
