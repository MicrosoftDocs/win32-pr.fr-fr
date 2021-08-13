---
title: Utilisation de Windows PowerShell pour créer des tâches de transfert BITS
description: Vous pouvez utiliser les applets de commande PowerShell pour créer des tâches de transfert de Service de transfert intelligent en arrière-plan (BITS) synchrones et asynchrones.
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e939342414d62e4e1af0551318dfec0fb9a5ca59a7e310f13de7b6b67b0440cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679891"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>Utilisation de Windows PowerShell pour créer des tâches de transfert BITS

Vous pouvez utiliser les applets de commande PowerShell pour créer des tâches de transfert de Service de transfert intelligent en arrière-plan (BITS) synchrones et asynchrones.

Tous les exemples de cette rubrique utilisent l’applet de commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . Pour utiliser l’applet de commande, vous devez d’abord importer le module. Pour installer le module, exécutez la commande suivante : Import-Module BitsTransfer. Pour plus d’informations, tapez **« obtenir-Help Start-BitsTransfer »** à l’invite de PowerShell.

> [!IMPORTANT]
>
> quand vous utilisez des applets de commande [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) à partir d’un processus qui s’exécute dans un contexte non interactif, tel qu’un service Windows, vous ne pourrez peut-être pas ajouter de fichiers aux tâches BITS, ce qui peut entraîner l’état suspendu. Pour que le travail se poursuive, l’identité qui a été utilisée pour créer une tâche de transfert doit être connectée. Par exemple, lors de la création d’un travail BITS dans un script PowerShell exécuté en tant que tâche de Planificateur de tâches, le transfert BITS ne se termine pas, sauf si le paramètre de tâche de Planificateur de tâches « exécuter uniquement quand l’utilisateur est connecté » est activé.

 

-   [Pour créer une tâche de transfert BITS synchrone](#to-create-a-synchronous-bits-transfer-job)
-   [Pour créer une tâche de transfert BITS synchrone avec plusieurs fichiers](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [Pour créer une tâche de transfert BITS synchrone et spécifier les informations d’identification d’un serveur distant](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [Pour créer une tâche de transfert BITS synchrone à partir d’un fichier CSV](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [Pour créer une tâche de transfert BITS asynchrone](#to-create-an-asynchronous-bits-transfer-job)
-   [Pour gérer les sessions à distance PowerShell](#to-manage-powershell-remote-sessions)
-   [Rubriques connexes](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>Pour créer une tâche de transfert BITS synchrone


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne.

 

Dans l’exemple précédent, les noms locaux et distants du fichier sont spécifiés respectivement dans les paramètres *source* et *destination* . L’invite de commandes réapparaît lorsque le transfert de fichiers est terminé ou lorsqu’il indique un état d’erreur.

Le type de transfert par défaut est Download. lorsque vous téléchargez des fichiers vers un emplacement HTTP, le paramètre *TransferType* doit avoir la valeur Télécharger.

Étant donné que la position des paramètres est appliquée pour l’applet de commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) , il n’est pas nécessaire de spécifier les noms des paramètres pour les paramètres source et destination. Par conséquent, cette commande peut être simplifiée comme suit.


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>Pour créer une tâche de transfert BITS synchrone avec plusieurs fichiers


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



Dans l’exemple précédent, la commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crée une tâche de transfert bits. Tous les fichiers sont ajoutés à ce travail et transférés de manière séquentielle au client.

> [!Note]  
> Le chemin de destination ne peut pas utiliser de caractères génériques. Le chemin d’accès de destination prend en charge les répertoires relatifs, les chemins d’accès racine ou les répertoires implicites (autrement dit, le répertoire actif). Les fichiers de destination ne peuvent pas être renommés à l’aide d’un caractère générique. En outre, les URL HTTP et HTTPs ne fonctionnent pas avec des caractères génériques. Les caractères génériques sont valides uniquement pour les chemins UNC et les répertoires locaux.

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>Pour créer une tâche de transfert BITS synchrone et spécifier les informations d’identification d’un serveur distant


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



Dans l’exemple précédent, un utilisateur crée une tâche de transfert BITS pour télécharger un fichier à partir d’un serveur qui requiert une authentification. L’utilisateur est invité à fournir des informations d’identification, et le paramètre *Credential* passe un objet Credential à l’applet de commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . L’utilisateur définit un proxy explicite, et la tâche de transfert BITS utilise uniquement les proxies définis par le paramètre *ProxyList* . Le paramètre *DisplayName* donne à la tâche de transfert bits un nom complet unique.

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>Pour créer une tâche de transfert BITS synchrone à partir d’un fichier CSV


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> « \| » Est le caractère de barre verticale.

 

Dans l’exemple précédent, un utilisateur crée une tâche de transfert BITS qui télécharge plusieurs fichiers à partir d’un client. L’applet de commande [Import-CSV](/previous-versions//dd347665(v=technet.10)) importe les emplacements de fichiers source et de destination et les dirige vers la commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . La commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crée une tâche de transfert bits pour chaque fichier, ajoute les fichiers au travail, puis les transfère de manière séquentielle au serveur.

Le contenu du fichier de Filelist.txt doit être au format suivant :

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>Pour créer une tâche de transfert BITS asynchrone


```PowerShell
$Job = Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip `
       -Destination d:\temp\downloads\ -Asynchronous

while (($Job.JobState -eq "Transferring") -or ($Job.JobState -eq "Connecting")) `
       { sleep 5;} # Poll for status, sleep for 5 seconds, or perform an action.

Switch($Job.JobState)
{
    "Transferred" {Complete-BitsTransfer -BitsJob $Job}
    "Error" {$Job | Format-List } # List the errors.
    default {"Other action"} #  Perform corrective action.
}

```



Dans l’exemple précédent, la tâche de transfert BITS a été assignée à la variable $Job. Les fichiers sont téléchargés séquentiellement. Une fois la tâche de transfert terminée, les fichiers sont immédiatement disponibles. Si $Job. JobState retourne « Transfered », l’objet $Job est envoyé à l’applet de commande [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .

Si $Job. JobState retourne « Error », l’objet $Job est envoyé à l’applet de commande [format-list]( /previous-versions//dd347700(v=technet.10)) pour répertorier les erreurs.

## <a name="to-manage-powershell-remote-sessions"></a>Pour gérer les sessions à distance PowerShell

à partir de Windows 10, la version 1607, vous pouvez exécuter des applets de commande powershell, BITSAdmin ou d’autres applications qui utilisent les [interfaces](bits-interfaces.md) BITS à partir d’une ligne de commande à distance powershell connectée à un autre ordinateur (physique ou virtuel). Cette fonctionnalité n’est pas disponible lors de l’utilisation d’une ligne de commande [PowerShell direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) sur un ordinateur virtuel sur la même machine physique, et elle n’est pas disponible lors de l’utilisation des applets de commande WinRM.

Un travail BITS créé à partir d’une session PowerShell distante s’exécute dans le contexte du compte d’utilisateur de cette session et ne progresse que lorsqu’il existe au moins une session de connexion locale active ou une session PowerShell distante associée à ce compte d’utilisateur. Vous pouvez utiliser les sessions PSSession persistants de PowerShell pour exécuter des commandes distantes sans avoir à maintenir une fenêtre PowerShell ouverte pour chaque travail pour continuer à progresser, comme décrit dans [PowerShell Basics : Remote Management](https://techgenix.com/remote-management-powershell-part1/).

-   [New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) crée une session PowerShell distante persistante. Une fois créé, les objets PSSession persistent sur l’ordinateur distant jusqu’à ce qu’il soit explicitement supprimé. Les travaux BITS initiés dans une session active feront progresser le transfert des données, même après que le client s’est déconnecté de la session.
-   [Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) déconnecte l’ordinateur client d’une session PowerShell distante et l’état de la session continue d’être maintenu par l’ordinateur distant. Plus important encore, les processus de la session distante continuent à s’exécuter, et les travaux BITS continuent à progresser. L’ordinateur client peut même redémarrer et/ou désactiver après l’appel de Disconnect-PSSession.
-   [Connecter-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) reconnecte l’ordinateur client à une session PowerShell à distance active.
-   [Remove-PSSession supprime](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) une session PowerShell distante.

L’exemple ci-dessous montre comment utiliser PowerShell à distance pour travailler avec des tâches de transfert BITS asynchrones d’une manière qui permet à la tâche de continuer à progresser même lorsque vous n’êtes pas activement connecté à la session à distance.


```PowerShell
# Establish a PowerShell Remote session in Server01 with name 'MyRemoteSession'
New-PSSession -ComputerName Server01 -Name MyRemoteSession -Credential Domain01\User01

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# While running in the context of the PowerShell Remote session, start a new BITS transfer
Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip -Destination c:\temp\downloads\ -Asynchronous

# Exit the PowerShell Remote session's context
Exit-PSSession

# Disconnect the 'MyRemoteSession' PowerShell Remote session from the current PowerShell window
# After this command, it is safe to close the current PowerShell window and turn off the local machine
Disconnect-PSSession -Name MyRemoteSession


# The commands below can be executed from a different PowerShell window, even after rebooting the local machine
# Connect the 'MyRemoteSession' PowerShell Remote session to the current PowerShell window
Connect-PSSession -ComputerName Server01 -Name MyRemoteSession

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# Manage BITS transfers on the remote machine via Complete-BitsTransfer, Remove-BitsTransfer, etc.

# Exit the PowerShell Remote session's context
Exit-PSSession

# Destroy the 'MyRemoteSession' PowerShell Remote session when no longer needed
Remove-PSSession -Name MyRemoteSession
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
