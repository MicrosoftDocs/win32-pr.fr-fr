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
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a><span data-ttu-id="08218-103">Utilisation des applets de commande Windows PowerShell WinRM pour gérer les tâches de transfert BITS</span><span class="sxs-lookup"><span data-stu-id="08218-103">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>

<span data-ttu-id="08218-104">Windows Remote Management applets de commande PowerShell peuvent gérer des tâches de transfert Service de transfert intelligent en arrière-plan (BITS).</span><span class="sxs-lookup"><span data-stu-id="08218-104">Windows Remote Management PowerShell cmdlets can manage Background Intelligent Transfer Service (BITS) transfer jobs.</span></span> <span data-ttu-id="08218-105">Pour plus d’informations sur la gestion à distance BITS, consultez la rubrique classes du fournisseur [bits](/previous-versions/windows/desktop/bitsprov/bits-provider) et du [fournisseur bits]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08218-105">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

<span data-ttu-id="08218-106">Les exemples suivants requièrent le [fournisseur bits](/previous-versions/windows/desktop/bitsprov/bits-provider).</span><span class="sxs-lookup"><span data-stu-id="08218-106">The following examples require the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider).</span></span> <span data-ttu-id="08218-107">Le fournisseur BITS est disponible après l’installation de BITS Compact Server.</span><span class="sxs-lookup"><span data-stu-id="08218-107">The BITS provider is available after the BITS Compact server is installed.</span></span> <span data-ttu-id="08218-108">Pour plus d’informations sur l’installation de Compact Server, consultez la documentation de [bits Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="08218-108">For information about installing the Compact server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="08218-109">Créez une tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="08218-109">Create a BITS transfer job.</span></span>

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="08218-110">L’applet de commande [obtient-Credential](/previous-versions//dd315327(v=technet.10)) demande les informations d’identification de l’utilisateur pour se connecter à l’ordinateur distant et assigne les informations d’identification à l’objet $CRED.</span><span class="sxs-lookup"><span data-stu-id="08218-110">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="08218-111">L’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) crée la tâche de transfert bits sur Client1 en créant une instance de la classe [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) et en utilisant les informations de la table de hachage définie dans le paramètre *ValueSet* .</span><span class="sxs-lookup"><span data-stu-id="08218-111">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cmdlet creates the BITS transfer job on Client1 by creating an instance of the [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) class and using the information in the hash table defined in the *Valueset* parameter.</span></span> <span data-ttu-id="08218-112">Le paramètre *ValueSet* spécifie les informations nécessaires pour remplir les paramètres de la méthode [createJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="08218-112">The *Valueset* parameter specifies the information needed to populate the parameters of the [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span> <span data-ttu-id="08218-113">Dans l’exemple précédent, l’utilisateur définit le paramètre de *type* sur 0 (Télécharger).</span><span class="sxs-lookup"><span data-stu-id="08218-113">In the preceding example, the user is sets the *Type* parameter to 0 (download).</span></span> <span data-ttu-id="08218-114">L’utilisateur spécifie également le nom des fichiers locaux et distants pour le travail de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="08218-114">The user also specifies the name of both the remote and local files for the download job.</span></span> <span data-ttu-id="08218-115">Pour plus d’informations sur la création de tâches de transfert BITS et pour obtenir des informations détaillées sur les paramètres, consultez méthode [createJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="08218-115">For more information about creating BITS transfer jobs and for detailed information about parameters, see [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span>

    <span data-ttu-id="08218-116">L’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) assigne le résultat à la variable $result.</span><span class="sxs-lookup"><span data-stu-id="08218-116">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet assigns the result to the $result variable.</span></span>

    > [!Note]  
    > <span data-ttu-id="08218-117">Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="08218-117">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="08218-118">Définissez la priorité de la tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="08218-118">Set the Priority of the BITS transfer job.</span></span>

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="08218-119">L’applet de commande [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) modifie la priorité de la nouvelle tâche de transfert bits à 0 (**priorité du \_ travail BG \_ \_ Foreground**).</span><span class="sxs-lookup"><span data-stu-id="08218-119">The [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cmdlet changes the new BITS transfer job priority to 0 (**BG\_JOB\_PRIORITY\_FOREGROUND**).</span></span> <span data-ttu-id="08218-120">Pour plus d’informations sur les niveaux de priorité, consultez l’énumération de la [**\_ \_ priorité du travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .</span><span class="sxs-lookup"><span data-stu-id="08218-120">For more information about the priority levels, see the [**BG\_JOB\_PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) enumeration.</span></span>

3.  <span data-ttu-id="08218-121">Reprendre la tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="08218-121">Resume the BITS transfer job.</span></span>

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="08218-122">L’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , qui définit l’état du travail sur 2 (reprendre la tâche).</span><span class="sxs-lookup"><span data-stu-id="08218-122">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method, which sets the job state to 2 (Resume the Job).</span></span>

4.  <span data-ttu-id="08218-123">Gérez la tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="08218-123">Manage the BITS transfer job.</span></span>

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

    

    <span data-ttu-id="08218-124">L’exemple précédent est un script permettant d’interroger l’état du travail et d’effectuer une action en fonction de l’État.</span><span class="sxs-lookup"><span data-stu-id="08218-124">The preceding example is a script to poll the status of the job and take an action based on the status.</span></span> <span data-ttu-id="08218-125">Les actions suivantes sont possibles :</span><span class="sxs-lookup"><span data-stu-id="08218-125">The following actions are possible:</span></span>

    -   <span data-ttu-id="08218-126">Si $result. L’État est 4 (erreur de l'**\_ État du travail \_ \_ BG**), l’applet [de commande Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) et annule la tâche.</span><span class="sxs-lookup"><span data-stu-id="08218-126">If $result.State is 4 (**BG\_JOB\_STATE\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="08218-127">Si $result. L’État est 5 **( \_ \_ \_ \_ erreur transitoire** de l’état de la tâche BG), l’applet [de commande Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) et annule la tâche.</span><span class="sxs-lookup"><span data-stu-id="08218-127">If $result.State is 5 (**BG\_JOB\_STATE\_TRANSIENT\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="08218-128">Si $result. L’État est 6 **( \_ État du travail BG \_ \_ transféré**), l’applet de commande [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) appelle la méthode [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) et définit l’État sur terminé.</span><span class="sxs-lookup"><span data-stu-id="08218-128">If $result.State is 6 (**BG\_JOB\_STATE\_TRANSFERRED**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and sets the state to complete.</span></span>

    <span data-ttu-id="08218-129">Pour plus d’informations sur les États de travail, consultez l’énumération de l' [**\_ \_ État de travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .</span><span class="sxs-lookup"><span data-stu-id="08218-129">For more information about job states, see the [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08218-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08218-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="08218-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="08218-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

[<span data-ttu-id="08218-132">Invoke-WsmanAction</span><span class="sxs-lookup"><span data-stu-id="08218-132">Invoke-WsmanAction</span></span>](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[<span data-ttu-id="08218-133">Set-WsmanInstance</span><span class="sxs-lookup"><span data-stu-id="08218-133">Set-WsmanInstance</span></span>](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
