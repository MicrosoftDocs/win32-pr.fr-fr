---
title: Utilisation des applets de commande Windows PowerShell WinRM pour gérer les tâches de transfert BITS
description: Windows Remote Management applets de commande PowerShell peuvent gérer des tâches de transfert Service de transfert intelligent en arrière-plan (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523780"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Utilisation des applets de commande Windows PowerShell WinRM pour gérer les tâches de transfert BITS

Windows Remote Management applets de commande PowerShell peuvent gérer des tâches de transfert Service de transfert intelligent en arrière-plan (BITS). Pour plus d’informations sur la gestion à distance BITS, consultez la rubrique classes du fournisseur [bits](/previous-versions/windows/desktop/bitsprov/bits-provider) et du [fournisseur bits]( /previous-versions//dd904507(v=vs.85)).

Les exemples suivants requièrent le [fournisseur bits](/previous-versions/windows/desktop/bitsprov/bits-provider). Le fournisseur BITS est disponible après l’installation de BITS Compact Server. Pour plus d’informations sur l’installation de Compact Server, consultez la documentation de [bits Compact Server](bits-compact-server.md) .

1.  Créez une tâche de transfert BITS.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    L’applet de commande [obtient-Credential](/previous-versions//dd315327(v=technet.10)) demande les informations d’identification de l’utilisateur pour se connecter à l’ordinateur distant et assigne les informations d’identification à l’objet $CRED.

    L’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) crée la tâche de transfert bits sur Client1 en créant une instance de la classe [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) et en utilisant les informations de la table de hachage définie dans le paramètre *ValueSet* . Le paramètre *ValueSet* spécifie les informations nécessaires pour remplir les paramètres de la méthode [createJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) . Dans l’exemple précédent, l’utilisateur définit le paramètre de *type* sur 0 (Télécharger). L’utilisateur spécifie également le nom des fichiers locaux et distants pour le travail de téléchargement. Pour plus d’informations sur la création de tâches de transfert BITS et pour obtenir des informations détaillées sur les paramètres, consultez méthode [createJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .

    L’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) assigne le résultat à la variable $result.

    > [!Note]  
    > Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne.

     

2.  Définissez la priorité de la tâche de transfert BITS.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    L’applet de commande [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) modifie la priorité de la nouvelle tâche de transfert bits à 0 (**priorité du \_ travail BG \_ \_ Foreground**). Pour plus d’informations sur les niveaux de priorité, consultez l’énumération de la [**\_ \_ priorité du travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .

3.  Reprendre la tâche de transfert BITS.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    L’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , qui définit l’état du travail sur 2 (reprendre la tâche).

4.  Gérez la tâche de transfert BITS.

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    L’exemple précédent est un script permettant d’interroger l’état du travail et d’effectuer une action en fonction de l’État. Les actions suivantes sont possibles :

    -   Si $result. L’État est 4 (erreur de l'**\_ État du travail \_ \_ BG**), l’applet [de commande Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) et annule la tâche.
    -   Si $result. L’État est 5 **( \_ \_ \_ \_ erreur transitoire** de l’état de la tâche BG), l’applet [de commande Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) et annule la tâche.
    -   Si $result. L’État est 6 **( \_ État du travail BG \_ \_ transféré**), l’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) et définit l’État sur terminé.

    Pour plus d’informations sur les États de travail, consultez l’énumération de l' [**\_ \_ État de travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
