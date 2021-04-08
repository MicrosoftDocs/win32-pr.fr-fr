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
ms.openlocfilehash: af4879d1fc8f1b25fa0b1b51816432aad3bed8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748508"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a><span data-ttu-id="50f05-103">Utilisation de Windows PowerShell pour créer des tâches de transfert BITS</span><span class="sxs-lookup"><span data-stu-id="50f05-103">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>

<span data-ttu-id="50f05-104">Vous pouvez utiliser les applets de commande PowerShell pour créer des tâches de transfert de Service de transfert intelligent en arrière-plan (BITS) synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="50f05-104">You can use PowerShell cmdlets to create synchronous and asynchronous Background Intelligent Transfer Service (BITS) transfer jobs.</span></span>

<span data-ttu-id="50f05-105">Tous les exemples de cette rubrique utilisent l’applet de commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="50f05-105">All of the examples in this topic use the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="50f05-106">Pour utiliser l’applet de commande, vous devez d’abord importer le module.</span><span class="sxs-lookup"><span data-stu-id="50f05-106">To use the cmdlet, be sure to import the module first.</span></span> <span data-ttu-id="50f05-107">Pour installer le module, exécutez la commande suivante : Import-Module BitsTransfer.</span><span class="sxs-lookup"><span data-stu-id="50f05-107">To install the module, run the following command: Import-Module BitsTransfer.</span></span> <span data-ttu-id="50f05-108">Pour plus d’informations, tapez **« obtenir-Help Start-BitsTransfer »** à l’invite de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="50f05-108">For more information, type **Get-Help Start-BitsTransfer** at the PowerShell prompt.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="50f05-109">Quand vous utilisez des applets de commande [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) à partir d’un processus qui s’exécute dans un contexte non interactif, tel qu’un service Windows, il est possible que vous ne puissiez pas ajouter de fichiers aux tâches bits, ce qui peut entraîner un état suspendu.</span><span class="sxs-lookup"><span data-stu-id="50f05-109">When you use [\*-BitsTransfer](/previous-versions//dd819413(v=technet.10)) cmdlets from within a process that runs in a noninteractive context, such as a Windows service, you may not be able to add files to BITS jobs, which can result in a suspended state.</span></span> <span data-ttu-id="50f05-110">Pour que le travail se poursuive, l’identité qui a été utilisée pour créer une tâche de transfert doit être connectée.</span><span class="sxs-lookup"><span data-stu-id="50f05-110">For the job to proceed, the identity that was used to create a transfer job must be logged on.</span></span> <span data-ttu-id="50f05-111">Par exemple, lors de la création d’un travail BITS dans un script PowerShell exécuté en tant que tâche de Planificateur de tâches, le transfert BITS ne se termine pas, sauf si le paramètre de tâche de Planificateur de tâches « exécuter uniquement quand l’utilisateur est connecté » est activé.</span><span class="sxs-lookup"><span data-stu-id="50f05-111">For example, when creating a BITS job in a PowerShell script that was executed as a Task Scheduler job, the BITS transfer will never complete unless the Task Scheduler's task setting "Run only when user is logged on" is enabled.</span></span>

 

-   [<span data-ttu-id="50f05-112">Pour créer une tâche de transfert BITS synchrone</span><span class="sxs-lookup"><span data-stu-id="50f05-112">To create a synchronous BITS transfer job</span></span>](#to-create-a-synchronous-bits-transfer-job)
-   [<span data-ttu-id="50f05-113">Pour créer une tâche de transfert BITS synchrone avec plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="50f05-113">To create a synchronous BITS transfer job with multiple files</span></span>](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [<span data-ttu-id="50f05-114">Pour créer une tâche de transfert BITS synchrone et spécifier les informations d’identification d’un serveur distant</span><span class="sxs-lookup"><span data-stu-id="50f05-114">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [<span data-ttu-id="50f05-115">Pour créer une tâche de transfert BITS synchrone à partir d’un fichier CSV</span><span class="sxs-lookup"><span data-stu-id="50f05-115">To create a synchronous BITS transfer job from a CSV file</span></span>](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [<span data-ttu-id="50f05-116">Pour créer une tâche de transfert BITS asynchrone</span><span class="sxs-lookup"><span data-stu-id="50f05-116">To create an asynchronous BITS transfer job</span></span>](#to-create-an-asynchronous-bits-transfer-job)
-   [<span data-ttu-id="50f05-117">Pour gérer les sessions à distance PowerShell</span><span class="sxs-lookup"><span data-stu-id="50f05-117">To manage PowerShell Remote sessions</span></span>](#to-manage-powershell-remote-sessions)
-   [<span data-ttu-id="50f05-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50f05-118">Related topics</span></span>](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a><span data-ttu-id="50f05-119">Pour créer une tâche de transfert BITS synchrone</span><span class="sxs-lookup"><span data-stu-id="50f05-119">To create a synchronous BITS transfer job</span></span>


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> <span data-ttu-id="50f05-120">Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="50f05-120">The grave-accent character (\`) is used to indicate a line break.</span></span>

 

<span data-ttu-id="50f05-121">Dans l’exemple précédent, les noms locaux et distants du fichier sont spécifiés respectivement dans les paramètres *source* et *destination* .</span><span class="sxs-lookup"><span data-stu-id="50f05-121">In the preceding example, the local and remote names of the file are specified in the *Source* and *Destination* parameters, respectively.</span></span> <span data-ttu-id="50f05-122">L’invite de commandes réapparaît lorsque le transfert de fichiers est terminé ou lorsqu’il indique un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="50f05-122">The command prompt returns when the file transfer is complete or when it enters an error state.</span></span>

<span data-ttu-id="50f05-123">Le type de transfert par défaut est Download.</span><span class="sxs-lookup"><span data-stu-id="50f05-123">The default transfer type is Download.</span></span> <span data-ttu-id="50f05-124">Lorsque vous téléchargez des fichiers vers un emplacement HTTP, le paramètre *TransferType* doit avoir la valeur upload.</span><span class="sxs-lookup"><span data-stu-id="50f05-124">When you upload files to an HTTP location, the *TransferType* parameter must be set to Upload.</span></span>

<span data-ttu-id="50f05-125">Étant donné que la position des paramètres est appliquée pour l’applet de commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) , il n’est pas nécessaire de spécifier les noms des paramètres pour les paramètres source et destination.</span><span class="sxs-lookup"><span data-stu-id="50f05-125">Because parameter position is enforced for the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet, the parameter names do not need to be specified for the Source and Destination parameters.</span></span> <span data-ttu-id="50f05-126">Par conséquent, cette commande peut être simplifiée comme suit.</span><span class="sxs-lookup"><span data-stu-id="50f05-126">Therefore, this command can be simplified as follows.</span></span>


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a><span data-ttu-id="50f05-127">Pour créer une tâche de transfert BITS synchrone avec plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="50f05-127">To create a synchronous BITS transfer job with multiple files</span></span>


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



<span data-ttu-id="50f05-128">Dans l’exemple précédent, la commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crée une tâche de transfert bits.</span><span class="sxs-lookup"><span data-stu-id="50f05-128">In the preceding example, the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job.</span></span> <span data-ttu-id="50f05-129">Tous les fichiers sont ajoutés à ce travail et transférés de manière séquentielle au client.</span><span class="sxs-lookup"><span data-stu-id="50f05-129">All of the files are added to this job and transferred sequentially to the client.</span></span>

> [!Note]  
> <span data-ttu-id="50f05-130">Le chemin de destination ne peut pas utiliser de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="50f05-130">The destination path cannot use wildcard characters.</span></span> <span data-ttu-id="50f05-131">Le chemin d’accès de destination prend en charge les répertoires relatifs, les chemins d’accès racine ou les répertoires implicites (autrement dit, le répertoire actif).</span><span class="sxs-lookup"><span data-stu-id="50f05-131">The destination path supports relative directories, root paths, or implicit directories (that is, the current directory).</span></span> <span data-ttu-id="50f05-132">Les fichiers de destination ne peuvent pas être renommés à l’aide d’un caractère générique.</span><span class="sxs-lookup"><span data-stu-id="50f05-132">Destination files cannot be renamed by using a wildcard character.</span></span> <span data-ttu-id="50f05-133">En outre, les URL HTTP et HTTPs ne fonctionnent pas avec des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="50f05-133">Additionally, HTTP and HTTPS URLs do not work with wildcards.</span></span> <span data-ttu-id="50f05-134">Les caractères génériques sont valides uniquement pour les chemins UNC et les répertoires locaux.</span><span class="sxs-lookup"><span data-stu-id="50f05-134">Wildcards are only valid for UNC paths and local directories.</span></span>

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a><span data-ttu-id="50f05-135">Pour créer une tâche de transfert BITS synchrone et spécifier les informations d’identification d’un serveur distant</span><span class="sxs-lookup"><span data-stu-id="50f05-135">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



<span data-ttu-id="50f05-136">Dans l’exemple précédent, un utilisateur crée une tâche de transfert BITS pour télécharger un fichier à partir d’un serveur qui requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="50f05-136">In the preceding example, a user creates a BITS transfer job to download a file from a server that requires authentication.</span></span> <span data-ttu-id="50f05-137">L’utilisateur est invité à fournir des informations d’identification, et le paramètre *Credential* passe un objet Credential à l’applet de commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="50f05-137">The user is prompted for credentials, and the *Credential* parameter passes a credential object to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="50f05-138">L’utilisateur définit un proxy explicite, et la tâche de transfert BITS utilise uniquement les proxies définis par le paramètre *ProxyList* .</span><span class="sxs-lookup"><span data-stu-id="50f05-138">The user sets an explicit proxy, and the BITS transfer job uses only the proxies that are defined by the *ProxyList* parameter.</span></span> <span data-ttu-id="50f05-139">Le paramètre *DisplayName* donne à la tâche de transfert bits un nom complet unique.</span><span class="sxs-lookup"><span data-stu-id="50f05-139">The *DisplayName* parameter gives the BITS transfer job a unique display name.</span></span>

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a><span data-ttu-id="50f05-140">Pour créer une tâche de transfert BITS synchrone à partir d’un fichier CSV</span><span class="sxs-lookup"><span data-stu-id="50f05-140">To create a synchronous BITS transfer job from a CSV file</span></span>


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> <span data-ttu-id="50f05-141">« \| » Est le caractère de barre verticale.</span><span class="sxs-lookup"><span data-stu-id="50f05-141">The "\|" is the pipe character.</span></span>

 

<span data-ttu-id="50f05-142">Dans l’exemple précédent, un utilisateur crée une tâche de transfert BITS qui télécharge plusieurs fichiers à partir d’un client.</span><span class="sxs-lookup"><span data-stu-id="50f05-142">In the preceding example, a user creates a BITS transfer job that uploads multiple files from a client.</span></span> <span data-ttu-id="50f05-143">L’applet de commande [Import-CSV](/previous-versions//dd347665(v=technet.10)) importe les emplacements de fichiers source et de destination et les dirige vers la commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="50f05-143">The [Import-CSV](/previous-versions//dd347665(v=technet.10)) cmdlet imports the source and destination file locations and pipes them to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command.</span></span> <span data-ttu-id="50f05-144">La commande [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crée une tâche de transfert bits pour chaque fichier, ajoute les fichiers au travail, puis les transfère de manière séquentielle au serveur.</span><span class="sxs-lookup"><span data-stu-id="50f05-144">The [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job for each file, adds the files to the job, and then transfers them sequentially to the server.</span></span>

<span data-ttu-id="50f05-145">Le contenu du fichier de Filelist.txt doit être au format suivant :</span><span class="sxs-lookup"><span data-stu-id="50f05-145">The contents of the Filelist.txt file should be in the following format:</span></span>

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a><span data-ttu-id="50f05-146">Pour créer une tâche de transfert BITS asynchrone</span><span class="sxs-lookup"><span data-stu-id="50f05-146">To create an asynchronous BITS transfer job</span></span>


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



<span data-ttu-id="50f05-147">Dans l’exemple précédent, la tâche de transfert BITS a été assignée à la variable $Job.</span><span class="sxs-lookup"><span data-stu-id="50f05-147">In the preceding example, the BITS transfer job was assigned to the $Job variable.</span></span> <span data-ttu-id="50f05-148">Les fichiers sont téléchargés séquentiellement.</span><span class="sxs-lookup"><span data-stu-id="50f05-148">The files are downloaded sequentially.</span></span> <span data-ttu-id="50f05-149">Une fois la tâche de transfert terminée, les fichiers sont immédiatement disponibles.</span><span class="sxs-lookup"><span data-stu-id="50f05-149">After the transfer job is complete, the files are immediately available.</span></span> <span data-ttu-id="50f05-150">Si $Job. JobState retourne « Transfered », l’objet $Job est envoyé à l’applet de commande [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="50f05-150">If $Job.JobState returns "Transferred", the $Job object is sent to the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="50f05-151">Si $Job. JobState retourne « Error », l’objet $Job est envoyé à l’applet de commande [format-list]( /previous-versions//dd347700(v=technet.10)) pour répertorier les erreurs.</span><span class="sxs-lookup"><span data-stu-id="50f05-151">If $Job.JobState returns "Error", the $Job object is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet to list the errors.</span></span>

## <a name="to-manage-powershell-remote-sessions"></a><span data-ttu-id="50f05-152">Pour gérer les sessions à distance PowerShell</span><span class="sxs-lookup"><span data-stu-id="50f05-152">To manage PowerShell Remote sessions</span></span>

<span data-ttu-id="50f05-153">À compter de Windows 10, version 1607, vous pouvez exécuter des applets de commande PowerShell, BITSAdmin ou d’autres applications qui utilisent les [interfaces](bits-interfaces.md) bits à partir d’une ligne de commande à distance PowerShell connectée à un autre ordinateur (physique ou virtuel).</span><span class="sxs-lookup"><span data-stu-id="50f05-153">Starting with Windows 10, version 1607, you can run PowerShell Cmdlets, BITSAdmin, or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="50f05-154">Cette fonctionnalité n’est pas disponible lors de l’utilisation d’une ligne de commande [PowerShell direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) sur un ordinateur virtuel sur la même machine physique, et elle n’est pas disponible lors de l’utilisation des applets de commande WinRM.</span><span class="sxs-lookup"><span data-stu-id="50f05-154">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>

<span data-ttu-id="50f05-155">Un travail BITS créé à partir d’une session PowerShell distante s’exécute dans le contexte du compte d’utilisateur de cette session et ne progresse que lorsqu’il existe au moins une session de connexion locale active ou une session PowerShell distante associée à ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50f05-155">A BITS Job created from a Remote PowerShell session runs under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="50f05-156">Vous pouvez utiliser les sessions PSSession persistants de PowerShell pour exécuter des commandes distantes sans avoir à maintenir une fenêtre PowerShell ouverte pour chaque travail pour continuer à progresser, comme décrit dans [PowerShell Basics : Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span><span class="sxs-lookup"><span data-stu-id="50f05-156">You can use PowerShell's persistent PSSessions to run remote commands without the need to keep a PowerShell window open for each job to continue making progress, as described in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span></span>

-   <span data-ttu-id="50f05-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) crée une session PowerShell distante persistante.</span><span class="sxs-lookup"><span data-stu-id="50f05-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) creates a persistent Remote PowerShell session.</span></span> <span data-ttu-id="50f05-158">Une fois créé, les objets PSSession persistent sur l’ordinateur distant jusqu’à ce qu’il soit explicitement supprimé.</span><span class="sxs-lookup"><span data-stu-id="50f05-158">Once created, the PSSession objects persist in the remote machine until explicitly deleted.</span></span> <span data-ttu-id="50f05-159">Les travaux BITS initiés dans une session active feront progresser le transfert des données, même après que le client s’est déconnecté de la session.</span><span class="sxs-lookup"><span data-stu-id="50f05-159">Any BITS jobs initiated in an active session will make progress transferring data, even after the client has disconnected from the session.</span></span>
-   <span data-ttu-id="50f05-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) déconnecte l’ordinateur client d’une session PowerShell distante et l’état de la session continue d’être maintenu par l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="50f05-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnects the client machine from a Remote PowerShell session and the session’s state continues to be maintained by the remote machine.</span></span> <span data-ttu-id="50f05-161">Plus important encore, les processus de la session distante continuent à s’exécuter, et les travaux BITS continuent à progresser.</span><span class="sxs-lookup"><span data-stu-id="50f05-161">Most importantly, the remote session’s processes will continue executing, and BITS jobs will continue to make progress.</span></span> <span data-ttu-id="50f05-162">L’ordinateur client peut même redémarrer et/ou désactiver après l’appel de Disconnect-PSSession.</span><span class="sxs-lookup"><span data-stu-id="50f05-162">The client machine can even reboot and/or turn off after calling Disconnect-PSSession.</span></span>
-   <span data-ttu-id="50f05-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) reconnecte l’ordinateur client à une session PowerShell à distance active.</span><span class="sxs-lookup"><span data-stu-id="50f05-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) re-connects the client machine to an active Remote PowerShell session.</span></span>
-   <span data-ttu-id="50f05-164">[Remove-PSSession supprime](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) une session PowerShell distante.</span><span class="sxs-lookup"><span data-stu-id="50f05-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) tears down a Remote PowerShell session.</span></span>

<span data-ttu-id="50f05-165">L’exemple ci-dessous montre comment utiliser PowerShell à distance pour travailler avec des tâches de transfert BITS asynchrones d’une manière qui permet à la tâche de continuer à progresser même lorsque vous n’êtes pas activement connecté à la session à distance.</span><span class="sxs-lookup"><span data-stu-id="50f05-165">The example below shows how to use PowerShell Remote to work with asynchronous BITS transfer jobs in a way that allows the job to continue to make progress even when you are not actively connected to the remote session.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="50f05-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50f05-166">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="50f05-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="50f05-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="50f05-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="50f05-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span></span>
</dt> </dl>

 

 
