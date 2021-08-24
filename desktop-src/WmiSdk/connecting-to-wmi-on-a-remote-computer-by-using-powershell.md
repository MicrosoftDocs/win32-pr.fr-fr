---
description: Connexion à WMI à distance avec PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Connexion à WMI à distance avec PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d499c59ee6774b1e972e192dfc2c0d1228469196c66e8f3feb80d1c9d6339c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679869"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Connexion à WMI à distance avec PowerShell

Windows PowerShell fournit un mécanisme simple pour se connecter à Windows Management Instrumentation (WMI) sur un ordinateur distant. les connexions distantes dans WMI sont affectées par le [pare-feu Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), les paramètres DCOM et le [contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905108(v=msdn.10)). pour plus d’informations sur la configuration des connexions à distance, consultez [connexion à WMI à distance à partir de Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Les exemples de cette rubrique sont basés sur les VBScripts de la [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md). Tous les exemples de cette rubrique utilisent l’applet de commande [« obtient-WmiObject »](/previous-versions//dd315295(v=technet.10)) . Pour plus d’informations, consultez la rubrique [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)).

## <a name="windows-powershell-examples"></a>exemples de Windows PowerShell

Lors de la création d’une connexion à un ordinateur distant, un utilisateur peut spécifier les informations de connexion, telles que le nom de l’ordinateur distant, les informations d’identification et le niveau d’authentification de la connexion. Les exemples suivants montrent comment se connecter à un ordinateur distant à l’aide de différents jeux d’informations d’identification et comment accéder aux informations WMI.

l’exemple de Windows PowerShell suivant illustre la définition du niveau d’emprunt d’identité :


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



Dans l’exemple précédent, l’utilisateur se connecte à un ordinateur distant en utilisant les mêmes informations d’identification (domaine et nom d’utilisateur) avec lesquelles il s’est connecté. L’utilisateur a également demandé à utiliser l’emprunt d’identité. Contrairement à l’exemple VBScript d’origine, une chaîne de moniker n’est pas nécessaire, car le niveau d’emprunt d’identité est défini par la propriété « emprunt d’identité ». Par défaut, le niveau d’emprunt d’identité a la valeur 3 (emprunter l’identité).

L’exemple répertorie toutes les instances de la classe de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui s’exécutent sur l’ordinateur distant.

> [!Note]  
> Vous devez spécifier l’espace de noms WMI auquel se connecter sur l’ordinateur distant, car il est possible que l’espace de noms par défaut ne soit pas le même sur des ordinateurs différents.

 

l’exemple de Windows PowerShell suivant montre comment se connecter à un ordinateur distant avec des informations d’identification différentes et définir le niveau d’emprunt d’identité sur 3, ce qui correspond à l’emprunt d’identité :


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



Dans l’exemple précédent, le nom de l’ordinateur a été affecté à la variable $Computer. L’utilisateur se connecte à un ordinateur distant en utilisant des informations d’identification spécifiques (domaine et nom d’utilisateur) et demande l’emprunt d’identité pour le niveau d’authentification.

> [!Note]  
> Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne. Elle est équivalente au trait de soulignement ( \_ ) dans VBScript.

 

l’exemple de Windows PowerShell suivant se connecte à un groupe d’ordinateurs distants dans le même domaine en créant un tableau de noms d’ordinateurs distants, puis en affichant les noms des appareils Plug-and-Play (instances de [**\_ PnPEntity Win32**](/windows/desktop/CIMWin32Prov/win32-pnpentity)) sur chaque ordinateur :


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> pour exécuter le script de Windows PowerShell précédent, vous devez être administrateur sur les ordinateurs distants. En outre, en rapport avec l’exemple précédent, notez les points suivants :

 

-   Les noms d’ordinateur dans le tableau doivent être placés entre guillemets, car il s’agit de chaînes.
-   Les objets retournés par la [prise en main](/previous-versions//dd315295(v=technet.10)) sont assignés à la variable $ColItems.
-   L’opérateur \[ \] de plage limite la liste des appareils Plug-and-Play à 48 instances. Pour plus d’informations, consultez [à propos des \_ opérateurs](/previous-versions//dd347588(v=technet.10)).
-   « \| » Est le caractère de pipeline. L’objet retourné par ColItems est envoyé à l’applet de commande [format-list]( /previous-versions//dd347700(v=technet.10)) .

l’exemple de Windows PowerShell suivant vous permet de vous connecter à un ordinateur distant situé sur un autre domaine. Cet exemple affiche également les noms des processus pour les instances de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) sur l’ordinateur distant.


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> pour exécuter le script de Windows PowerShell précédent, vous devez être administrateur sur l’ordinateur distant.

 

Dans l’exemple précédent, l’utilisateur se connecte à un ordinateur distant situé sur un autre domaine et spécifie des paramètres régionaux préférés. La commande de [récupération des informations d’identification](/previous-versions//dd315327(v=technet.10)) demande les informations d’identification de l’utilisateur et assigne les informations d’identification à un objet. L’exemple répertorie également les noms des instances de la classe de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui s’exécutent sur l’ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
