---
description: Tâches planifiées WMI créez et récupérez des informations sur les tâches planifiées. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Tâches WMI : tâches planifiées'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4051df4348ee47710b5d2d1f5dcc3f59f607d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517007"
---
# <a name="wmi-tasks-scheduled-tasks"></a><span data-ttu-id="f0446-104">Tâches WMI : tâches planifiées</span><span class="sxs-lookup"><span data-stu-id="f0446-104">WMI Tasks: Scheduled Tasks</span></span>

<span data-ttu-id="f0446-105">Tâches planifiées WMI créez et récupérez des informations sur les tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="f0446-105">WMI scheduled tasks create and get information about scheduled tasks.</span></span> <span data-ttu-id="f0446-106">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0446-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="f0446-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f0446-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="f0446-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f0446-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="f0446-109">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="f0446-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="f0446-110">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="f0446-110">**To run a script**</span></span>

1.  <span data-ttu-id="f0446-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="f0446-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="f0446-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="f0446-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="f0446-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="f0446-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="f0446-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="f0446-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="f0446-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="f0446-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="f0446-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="f0446-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="f0446-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="f0446-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="f0446-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="f0446-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="f0446-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="f0446-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="f0446-120">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f0446-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0446-121">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="f0446-121">How do I...</span></span></th>
<th><span data-ttu-id="f0446-122">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="f0446-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0446-123">... créer des tâches planifiées à l’aide de scripts ?</span><span class="sxs-lookup"><span data-stu-id="f0446-123">...create scheduled tasks using scripts?</span></span></td>
<td><span data-ttu-id="f0446-124">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f0446-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method.</span></span> <span data-ttu-id="f0446-125">Si vous avez des difficultés à faire fonctionner cette tâche sur Windows 7 ou une version ultérieure, consultez la section <strong>Win32_ScheduledJob</strong> remarques. vos paramètres vous empêchent probablement d’utiliser la classe.</span><span class="sxs-lookup"><span data-stu-id="f0446-125">If you are having difficulty making this task work on Windows 7 or later, see the <strong>Win32_ScheduledJob</strong> Remarks section; likely your settings are preventing you from using the class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0446-126">VB</span><span class="sxs-lookup"><span data-stu-id="f0446-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="f0446-127">Dans la chaîne \* \* \* \* \* \* \* \* &quot; 143000.000000-420 &quot; (utilisé dans la valeur du paramètre <em>StartTime</em> de la méthode <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> ), \* \* \* \* \* \* \* \* &quot; 143000,000000 &quot; spécifie que la tâche commence à 14,30 (2:30 P.M.) et &quot; -420 &quot; spécifie le fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="f0446-127">In the string &quot;\*\*\*\*\*\*\*\*143000.000000-420&quot; (used in the <em>StartTime</em> parameter value of the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method), &quot;\*\*\*\*\*\*\*\*143000.000000&quot; specifies that the task starts at 14.30 (2:30 P.M.) and &quot;-420&quot; specifies the time zone.</span></span> <span data-ttu-id="f0446-128">Le numéro de fuseau horaire est le décalage actuel de la traduction de l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="f0446-128">The time zone number is the current bias of the local time translation.</span></span> <span data-ttu-id="f0446-129">Le biais correspond à la différence entre l’heure UTC et l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="f0446-129">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="f0446-130">Pour calculer le décalage pour votre fuseau horaire, multipliez le nombre d’heures d’avance ou de retard de l’heure de Greenwich (GMT) par 60 (utilisez un nombre positif comme nombre d’heures avant l’heure GMT et un nombre négatif si votre fuseau horaire est situé en arrière-plan GMT).</span><span class="sxs-lookup"><span data-stu-id="f0446-130">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="f0446-131">Ajoutez un 60 supplémentaire à votre calcul si votre fuseau horaire utilise l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="f0446-131">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="f0446-132">Par exemple, le fuseau horaire Pacifique est de huit heures après l’heure GMT. par conséquent, le décalage est égal à-420 (-8 \* 60 + 60) lorsque l’heure d’été est utilisée et-480 (-8 \* 60) lorsque l’heure d’été n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f0446-132">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="f0446-133">Vous pouvez également déterminer la valeur du décalage en interrogeant la propriété Bias de la classe <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f0446-133">You can also determine the value of the bias by querying the bias property of the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0446-134">... retourner une liste de toutes les tâches planifiées sur un ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="f0446-134">...return a list of all the scheduled tasks on a computer?</span></span></td>
<td><p><span data-ttu-id="f0446-135">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f0446-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class.</span></span> <span data-ttu-id="f0446-136">Notez que cette classe ne peut retourner que des tâches créées à l’aide d’un script ou d’un AT.exe.</span><span class="sxs-lookup"><span data-stu-id="f0446-136">Note that this class can only return jobs that are created using either a script or AT.exe.</span></span> <span data-ttu-id="f0446-137">Elle ne peut pas retourner d’informations sur les travaux qui sont créés ou modifiés par l’Assistant tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="f0446-137">It cannot return information about jobs that are either created by or modified by the Scheduled Task wizard.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0446-138">VB</span><span class="sxs-lookup"><span data-stu-id="f0446-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f0446-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0446-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0446-140">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="f0446-140">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="f0446-141">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="f0446-141">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="f0446-142">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="f0446-142">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

